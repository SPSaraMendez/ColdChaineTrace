# Success Criteria

## 1. Physical Prototype

- [ ] A refrigerated environment has been physically instrumented.
- [ ] A temperature sensor acquires real measurements.
- [ ] The embedded system processes the measurements correctly.
- [ ] The device can transmit telemetry to the software platform.

## 2. IoT Communication

- [ ] Telemetry can be transmitted from the physical prototype to the backend.
- [ ] Each telemetry record contains a device identifier.
- [ ] Measurements contain timestamps.
- [ ] Telemetry can be associated with a shipment.
- [ ] Communication failures can be detected or handled.

## 3. Backend

- [ ] The ASP.NET Core API is operational.
- [ ] Products can be registered.
- [ ] Lots can be registered.
- [ ] Shipments can be created.
- [ ] Monitoring devices can be registered.
- [ ] Telemetry can be received and stored.
- [ ] Logistics events can be registered.
- [ ] Alerts can be generated.

## 4. Traceability

- [ ] A shipment maintains a chronological history of relevant events.
- [ ] Environmental measurements can be associated with a shipment.
- [ ] Environmental deviations can be identified.
- [ ] Alerts can be associated with the corresponding shipment and device.
- [ ] The history of a shipment can be queried.

## 5. Blockchain / Integrity

- [ ] Selected critical records can generate cryptographic hashes.
- [ ] The system can associate integrity evidence with the corresponding record.
- [ ] A verification mechanism can detect whether the referenced record has been modified.
- [ ] The blockchain or distributed-ledger component can be demonstrated in a controlled scenario.

## 6. Operational Modes

- [ ] The system supports a common cold-chain core.
- [ ] Pharmaceutical mode can be configured.
- [ ] Food mode can be configured.
- [ ] Mode-specific environmental rules can be applied without modifying the core logistics entities.

## 7. Integration

- [ ] The physical prototype can send real telemetry.
- [ ] The backend receives the telemetry.
- [ ] The telemetry is associated with a shipment.
- [ ] An environmental deviation generates an alert.
- [ ] The deviation is registered as a traceability event.
- [ ] The selected critical event generates integrity evidence.
- [ ] The complete event can be visualized through the software interface.

## 8. Final Demonstration

The final prototype must demonstrate the following scenario:

1. A shipment is created.
2. A monitoring device is associated with the shipment.
3. The physical cold-chain prototype generates temperature measurements.
4. Telemetry is transmitted to the backend.
5. The system detects an environmental deviation.
6. An alert is generated.
7. The event is added to the shipment history.
8. Integrity evidence is generated for the selected critical record.
9. The user can review the complete traceability history.

## 9. Documentation

- [ ] System architecture is documented.
- [ ] Hardware architecture is documented.
- [ ] Software architecture is documented.
- [ ] API is documented.
- [ ] Database model is documented.
- [ ] IoT communication flow is documented.
- [ ] Blockchain/integrity mechanism is documented.
- [ ] Testing results are documented.
- [ ] Final prototype limitations are documented.
