# Project Scope

## 1. Scope Definition

ColdChainTrace will be developed as a functional engineering prototype that integrates a physical cold-chain monitoring environment with a modular software platform for environmental monitoring, logistics management and traceability.

The project will be developed over a period of 21 days and will focus on demonstrating the technical feasibility of integrating embedded systems, IoT communication, backend software, data management and blockchain-based data integrity mechanisms within a common architecture.

---

## 2. Functional Scope

### 2.1. Product and Lot Management

The system will allow the registration and management of:

- Products.
- Product categories.
- Lots.
- Product conservation requirements.
- Configurable environmental thresholds.

Each product or product type may have its own environmental parameters, allowing the platform to support different cold-chain scenarios.

---

### 2.2. Shipment Management

The platform will allow the creation and monitoring of shipments.

A shipment will contain information such as:

- Shipment identifier.
- Product.
- Lot.
- Origin.
- Destination.
- Associated monitoring device.
- Current status.
- Creation and completion timestamps.

The system will maintain the relationship between the shipment and the environmental information generated during its journey.

---

### 2.3. Physical Cold-Chain Prototype

The project will include a physical refrigerated environment used as an experimental cold-chain scenario.

The prototype will include:

- Refrigerated enclosure or refrigerator.
- Temperature sensor.
- Embedded microcontroller.
- Communication module or integrated wireless connectivity.
- Power supply.
- Physical arrangement for sensor installation and monitoring.

The prototype will be capable of acquiring environmental measurements and transmitting them to the software platform.

Additional sensors may be incorporated if time, budget and technical feasibility allow.

---

### 2.4. Embedded Monitoring System

The embedded system will be responsible for:

- Reading environmental sensors.
- Processing measurements.
- Generating timestamps.
- Identifying the monitoring device.
- Preparing telemetry messages.
- Transmitting telemetry to the backend.
- Handling basic communication or sensor errors.

The initial implementation will prioritize temperature monitoring.

---

### 2.5. IoT Communication

The system will implement an IoT communication mechanism between the physical prototype and the backend.

The communication layer may use protocols such as:

- MQTT.
- HTTP/REST.

The final protocol will be selected during implementation based on technical requirements and project constraints.

Telemetry will contain information such as:

- Device identifier.
- Shipment identifier.
- Temperature.
- Optional humidity.
- Timestamp.
- Device status.

---

### 2.6. Backend Platform

The backend will be developed using:

- C#.
- .NET / ASP.NET Core.
- Entity Framework Core.
- SQL Server.

The backend will provide services for:

- Product management.
- Lot management.
- Shipment management.
- Device management.
- Telemetry ingestion.
- Environmental rule evaluation.
- Alert management.
- Logistics event management.
- Traceability queries.

The backend will expose a REST API for communication with external clients and devices.

---

### 2.7. Environmental Monitoring and Alerts

The system will evaluate incoming telemetry against configurable environmental parameters.

When a measurement exceeds the configured limits, the system will be capable of:

1. Detecting the deviation.
2. Registering the incident.
3. Generating an alert.
4. Associating the alert with the corresponding shipment and device.
5. Maintaining the event in the shipment history.

Example:

Temperature range:

2 °C – 8 °C

Measurement:

9.4 °C

Result:

```text
Environmental deviation detected
        ↓
Alert generated
        ↓
Event registered
        ↓
Shipment history updated
```
