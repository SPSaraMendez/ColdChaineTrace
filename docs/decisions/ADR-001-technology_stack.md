# ADR-001: Technology Stack

## Status

Accepted

## Date

2026-08-11

## Context

ColdChainTrace requires a technology stack capable of integrating a physical cold-chain monitoring prototype with an IoT communication layer, backend services, data storage, traceability mechanisms, and a future monitoring dashboard.

The selected technologies must support rapid prototyping while maintaining a scalable and maintainable architecture.

## Decisions

### Embedded Controller — ESP32

The ESP32 will be used as the primary embedded controller.

Reasons:

- Integrated Wi-Fi connectivity
- Low cost
- Sufficient processing capabilities
- Multiple communication interfaces
- Large IoT ecosystem
- Suitable for sensor acquisition and telemetry

### Communication Protocol — MQTT

MQTT will be used for telemetry communication between the embedded system and backend infrastructure.

Reasons:

- Lightweight protocol
- Designed for IoT environments
- Publish/subscribe communication model
- Efficient communication for sensor data
- Supports future multi-device expansion

### Backend — C# / .NET

The backend will be implemented using C# and .NET with ASP.NET Core.

Reasons:

- Strong object-oriented programming support
- Suitable for scalable APIs
- Strong dependency injection capabilities
- Good support for Clean Architecture
- Integration with databases and external services
- Consistent with the project's software engineering objectives

### Database — SQL Server

SQL Server will be used for structured telemetry and application data.

Reasons:

- Relational data model
- Strong integration with .NET
- Suitable for historical telemetry
- Support for structured queries and reporting

### Architecture — Clean Architecture

The backend will follow Clean Architecture principles.

The main layers will be:

- API
- Application
- Domain
- Infrastructure

This separation will improve maintainability, testability, and dependency management.

### Physical Design — Fusion 360

Fusion 360 will be used to design the physical prototype and its hardware integration.

The CAD model will represent:

- Cooler enclosure
- Sensor mounting
- Electronics enclosure
- Cable routing
- Hardware integration

### Documentation — PlantUML

PlantUML will be used for system and software architecture diagrams.

Reasons:

- Version-controlled diagrams
- Text-based source files
- Easy integration with Git
- Reproducible documentation

### Data Integrity — Integrity Layer

ColdChainTrace will include a dedicated data-integrity mechanism for selected traceability records.

The implementation will be determined during the development phase after evaluating the project's requirements and constraints.

The objective is to provide evidence that relevant historical records have not been modified after their registration.

## Consequences

The selected stack allows ColdChainTrace to combine:

Embedded Systems → IoT → Software Engineering → Data Management → Physical Design → Data Integrity

The architecture also allows additional sensors, cold-chain units, and monitoring capabilities to be added in future iterations without redesigning the entire system.

## Initial Technology Stack

| Area                | Technology         |
| ------------------- | ------------------ |
| Embedded Controller | ESP32              |
| Sensor              | Thermocouple       |
| Communication       | MQTT               |
| Backend             | C# / .NET          |
| API                 | ASP.NET Core       |
| Database            | SQL Server         |
| Architecture        | Clean Architecture |
| CAD                 | Fusion 360         |
| Diagrams            | PlantUML           |
| Version Control     | Git / GitHub       |
| Data Integrity      | Integrity Layer    |
