# Nebulae Microservice Anatomy Overview

## Table of Contents
- [Introduction](#introduction)
- [Core Architecture Principles](#core-architecture-principles)
- [Framework Components](#framework-components)
- [Directory Structure and Organization](#directory-structure-and-organization)
- [Data Flow Patterns](#data-flow-patterns)
- [Development Lifecycle](#development-lifecycle)
- [Deployment and Operations](#deployment-and-operations)
- [Best Practices](#best-practices)

## Introduction

The Nebulae Framework is a comprehensive, full-stack microservice development platform designed for building scalable, reactive, and event-driven distributed systems. It implements Domain-Driven Design (DDD) principles with Command Query Responsibility Segregation (CQRS) and Event Sourcing patterns at its core.

### Key Characteristics
- **Full-Stack Approach**: Integrated backend, API gateway, and micro-frontend architecture
- **Event-Driven**: Asynchronous communication through NATS.io message broker
- **Reactive Programming**: RxJS-based reactive streams throughout the stack
- **Domain-Centric**: Business logic organized around domain aggregates
- **Composable**: Shell-based composition for UI and API layers

## Core Architecture Principles

### 1. Hexagonal Architecture (Ports & Adapters)
The framework enforces clean separation between business logic and external concerns:
- **Domain Layer**: Pure business logic with aggregates and domain services
- **Application Layer**: Use cases and application services coordinating domain operations
- **Infrastructure Layer**: External adapters for databases, message brokers, and APIs
- **Interface Layer**: GraphQL/REST endpoints and micro-frontend components

### 2. CQRS (Command Query Responsibility Segregation)
Commands and queries are handled through separate pathways:
- **Commands**: Modify state through domain aggregates and event sourcing
- **Queries**: Read from optimized materialized views
- **Event Sourcing**: Commands generate events that are stored as the source of truth
- **Materialized Views**: Query models are built from event streams

### 3. Event-Driven Communication
- **Domain Events**: Business events published when domain state changes
- **Integration Events**: Cross-service communication through message broker
- **Event Store**: Immutable event log as the primary data store
- **Reactive Streams**: RxJS observables for handling asynchronous event flows

## Framework Components

### 1. Micro-Frontends
Composable UI components organized by domain:

```
frontend/
├── emi/                     # Enterprise management system micro-frontends
│   ├── {domain-management}/ # Domain-specific UI modules
│   │   ├── MicroFrontendConfig.js  # Route and navigation config
│   │   ├── components/      # React components
│   │   ├── store/          # Redux state management
│   │   └── i18n/           # Internationalization
├── pis/                    # Passenger interface micro-frontends
└── pis-abt/               # Account-based ticketing micro-frontends
```

**Micro-Frontend Features:**
- **Route Configuration**: React Router integration with lazy loading
- **Navigation Integration**: Menu structure and permissions
- **State Management**: Redux with domain-specific slices
- **Internationalization**: Multi-language support per domain
- **Permission-Based Access**: Role-based component rendering

### 2. API Gateways (Backend-for-Frontend)
The `api/` directory holds micro-APIs per specific gateway, implementing the Backend-for-Frontend pattern. Multiple specialized gateways handle different client contexts:

```
api/
├── emi-gateway/              # Enterprise management system api (backend-for-frondend)
├── external-network-gateway/ # External network integrations api (backend-for-frondend)
├── external-system-gateway/  # Third-party system APIs api (backend-for-frondend)
├── pis-gateway/             # Passenger Information System api (backend-for-frondend)
└── pis-abt-gateway/         # Account-Based Ticketing PIS api (backend-for-frondend)
```

**Gateway Responsibilities:**
- **GraphQL Schema Composition**: Aggregate schemas from multiple microservices
- **Authentication & Authorization**: Enforce security policies
- **Request Routing**: Direct requests to appropriate backend services
- **API Versioning**: Manage API evolution and compatibility

### 3. Backend Services
Each microservice backend follows a consistent structure:

```
backend/
├── {backend-name}/
│   ├── bin/                    # Executable entry points
│   │   ├── domain/            # Domain layer implementation
│   │   ├── services/          # Application services
│   │   ├── tools/             # Utilities and tools
│   │   └── entry-point/       # Bootstrap and startup
│   ├── Dockerfile            # Container definition
│   ├── entrypoint.sh        # Container entry point
│   └── package.json          # Dependencies and scripts
```

**Key Backend Patterns:**
- **Domain Registration**: Domains register CQRS and Event Sourcing handlers
- **Service Bootstrap**: `server.js` initializes services and message broker connections
- **State Synchronization**: `sync_state.js` rebuilds materialized views from events
- **Pre-start Actions**: `get_ready.js` provides readiness and do pre-start actions

## Directory Structure and Organization

### Standard Microservice Layout
```
{microservice-name}/
├── api/                     # API gateway integrations
│   ├── {gateway-name}/     
│   │   ├── graphql/        # GraphQL schema and resolvers
│   │   └── rest/           # REST API definitions
├── backend/                # Business logic services
│   ├── {service-name}/     # Individual backend services
├── frontend/               # Micro-frontend modules
│   ├── {client-type}/      # Client-specific frontends
├── deployment/             # Infrastructure as code
│   ├── gke/               # Kubernetes manifests
│   └── compose/           # Docker Compose for local dev
├── etc/                    # Configuration files
│   ├── mapi-setup.json    # API gateway setup
│   └── mfe-setup.json     # Micro-frontend setup
└── playground/             # Local development environment
```

### Domain Structure Pattern
Each domain within a service follows this pattern:

```javascript
// domain/index.js
module.exports = {
  start$: startEvent$ => ...,        // Domain initialization
  stop$: stopEvent$ => ...,          // Graceful shutdown
  eventSourcingProcessorMaps: {      // Event handlers
    CommandName: commandHandler$,
    EventName: eventHandler$
  },
  cqrsRequestProcessorMaps: {        // CQRS query handlers
    QueryName: queryHandler$
  }
};
```

## Data Flow Patterns

### 1. Command Flow (WRITE Operations)
```
Client Request → API Gateway → Command Bus → Domain Aggregate → Event Store → Event Bus
                                                      ↓
                              Event Handlers ← Event Bus ← Domain Events
```

**Key Components:**
- **Command Validation**: Input validation and business rule checks
- **Aggregate Loading**: Reconstitute aggregate state from events
- **Business Logic**: Execute domain operations and enforce invariants
- **Event Generation**: Create domain events representing state changes
- **Event Persistence**: Store events in immutable event store

### 2. Query Flow (READ Operations)
```
Client Query → API Gateway → Query Handler → Materialized View → Response
```

**Optimization Strategies:**
- **Materialized Views**: Pre-computed projections optimized for queries
- **CQRS Separation**: Separate read and write models
- **Caching Layers**: Redis or in-memory caching for frequently accessed data
- **GraphQL Optimization**: Field-level resolution and batching

### 3. Event Sourcing Pattern
```
Command → Aggregate → Events → Event Store
                         ↓
                   Event Projectors → Read Models
```

**Benefits:**
- **Complete Audit Trail**: Every state change is recorded
- **Temporal Queries**: Query system state at any point in time
- **Replay Capability**: Rebuild system state from events
- **Integration Events**: Natural publication of business events

### 4. Reactive Streams
The framework uses RxJS extensively for handling asynchronous operations:

```javascript
// Example reactive handler
const handleCommand$ = (command$) =>
  command$.pipe(
    mergeMap(command => validateCommand$(command)),
    mergeMap(command => loadAggregate$(command.aggregateId)),
    map(aggregate => aggregate.executeCommand(command)),
    mergeMap(events => persistEvents$(events)),
    mergeMap(events => publishEvents$(events))
  );
```


## Deployment and Operations

### 1. Container Strategy
Each service is containerized with:
- **Multi-stage builds** for optimized production images
- **Health check endpoints** for Kubernetes liveness/readiness probes
- **Environment-based configuration** through environment variables
- **Graceful shutdown** handling for zero-downtime deployments

### 2. Kubernetes Deployment
```yaml
# Standard deployment pattern
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-service
spec:
  replicas: 3
  template:
    spec:
      containers:
      - name: my-service
        image: my-service:latest
        ports:
        - containerPort: 3000
        env:
        - name: MONGODB_URL
          valueFrom:
            secretKeyRef:
              name: mongodb-secret
              key: url
        livenessProbe:
          httpGet:
            path: /api/my-service/graphql/liveness
            port: 3000
        readinessProbe:
          httpGet:
            path: /api/my-service/graphql/readiness
            port: 3000
```
