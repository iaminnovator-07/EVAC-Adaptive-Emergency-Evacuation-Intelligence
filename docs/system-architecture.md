# System Architecture

## Current Demonstration Architecture

```text
Simulated Sensors
        ↓
Local Data Processing
        ↓
Zone Risk Assessment
        ↓
Digital Twin / Building Graph
        ↓
Dijkstra-Based Route Simulation
        ↓
Dynamic EVAC Signage
        ↓
Local Dashboard and Alerts
```

## Explanation

1. **Simulated Sensors** provide synthetic values for hazard and occupancy conditions.
2. **Local Data Processing** transforms raw simulated inputs into normalized zone signals.
3. **Zone Risk Assessment** assigns each zone a state (safe/caution/blocked).
4. **Digital Twin / Building Graph** models floor topology and connectivity.
5. **Dijkstra-Based Route Simulation** computes best available evacuation path under current risk assumptions.
6. **Dynamic EVAC Signage** updates directional recommendations.
7. **Local Dashboard and Alerts** displays status, events, and operator controls.

## Planned Hardware + Edge Architecture

```text
ESP32 Sensor Nodes
        ↓
Wi-Fi / ESP-NOW / BLE / LoRa
        ↓
Local Gateway
        ↓
TinyML / Edge AI
        ↓
Risk Engine + Dijkstra
        ↓
Physical EVAC Signs
```

## Future Considerations

- Resilience during partial communication loss
- Sensor calibration and drift monitoring
- Failsafe behavior and conservative routing
- Integration with existing fire safety systems
- Compliance-oriented logging and auditability
