# 🚨 EVAC — Adaptive Emergency Evacuation Intelligence

> **The safest exit is not always the nearest exit.**

<p align="center">
  <b>SIH 2026 • AICTE Student Innovation • Disaster Management</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Team-SYGNIX-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Team%20ID-119351-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Problem%20Statement-SIH26223-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Prototype-orange?style=for-the-badge" />
</p>

---

## 👑 Project Leadership

| Field                    | Details                                           |
| ------------------------ | ------------------------------------------------- |
| **Team Name**            | SYGNIX                                            |
| **Team ID**              | `119351`                                          |
| **Team Leader**          | **Swadeep Bansode**                               |
| **Problem Statement ID** | `SIH26223`                                        |
| **Domain**               | Disaster Management                               |
| **Project Name**         | EVAC — Adaptive Emergency Evacuation Intelligence |
| **Event**                | Smart India Hackathon 2026                        |

---

## 🌍 The Big Problem

During an emergency, the **nearest exit may not always be the safest exit**.

Fire, smoke, blocked corridors, crowd congestion, changing environmental conditions and communication failures can make traditional fixed evacuation systems less effective.

Many buildings still depend on:

* Static evacuation maps
* Fixed emergency exit signs
* Manual announcements
* Human decision-making under pressure
* Evacuation routes that do not adapt to changing conditions

In a real emergency, conditions can change within seconds.

That creates one critical question:

> **How can people be guided toward a safer route as the situation changes?**

---

## ⚡ Our Solution

**EVAC** is an adaptive, offline-first emergency evacuation intelligence system designed for high-occupancy buildings.

It aims to combine distributed sensing, local intelligence, risk assessment, dynamic route calculation and adaptive physical guidance into one integrated evacuation layer.

```text
Sensors
   ↓
Local Communication
   ↓
Edge Intelligence
   ↓
Zone Risk Assessment
   ↓
Dynamic Route Engine
   ↓
Adaptive Signage + Local Dashboard
```

EVAC does not simply search for the shortest path.

> 🧠 **EVAC aims to identify the safest available route based on changing zone conditions.**

---

## 🔥 Why EVAC?

Traditional evacuation systems generally provide fixed instructions.

But during an emergency:

* A corridor may become unsafe.
* An exit may become blocked.
* Smoke may spread to a particular zone.
* A staircase may become overcrowded.
* Internet connectivity may fail.
* People may become confused by static signage.

EVAC explores a more responsive approach in which evacuation guidance can change according to the current simulated building state.

---

## 🧩 How EVAC Works

### 1. 🛰️ Sense

Distributed nodes can collect environmental and occupancy-related information.

Potential inputs include:

* 🌡️ Temperature and humidity
* 🌫️ Air-quality or smoke anomalies
* 👥 Occupancy and motion
* 🚧 Corridor obstruction
* 📍 Zone-level environmental changes

### 2. 📡 Communicate

The system is designed around local and resilient communication options, including:

* Wi-Fi / local LAN
* ESP-NOW
* Bluetooth Low Energy
* LoRa-based fallback communication

The objective is to reduce dependence on cloud connectivity during critical situations.

### 3. 🧠 Assess Risk

A lightweight edge-intelligence layer evaluates zone conditions.

Possible zone states include:

| State               | Meaning                          |
| ------------------- | -------------------------------- |
| 🟢 Safe             | Normal operating condition       |
| 🟡 Caution          | Early abnormality detected       |
| 🟠 High Risk        | Significant hazard or congestion |
| 🔴 Blocked / Unsafe | Route should be avoided          |

The planned embedded intelligence direction includes:

* TinyML
* TensorFlow Lite for Microcontrollers
* Lightweight quantized models
* Rule-based fallback logic
* Local inference

> **Note:** Resource-constrained devices such as ESP32 are intended to use lightweight TinyML models. Larger models may require a more capable local gateway or edge computer.

### 4. 🗺️ Calculate Dynamic Routes

The building can be represented as a graph:

* **Nodes** → rooms, corridors, staircases, exits and zones
* **Edges** → accessible paths
* **Weights** → distance, risk, congestion and obstruction

A graph-based route engine can update route costs as the simulated building conditions change.

The prototype direction includes algorithms such as:

* Dijkstra’s shortest-path algorithm
* Risk-weighted routing
* Dynamic edge-cost updates
* Zone-level state transitions

### 5. 💡 Guide People

The calculated route can be represented through:

* Adaptive LED arrows
* Dynamic exit indicators
* Local alarms or buzzers
* Zone-status dashboards
* Emergency monitoring interfaces

---

## 🏗️ System Architecture

```text
┌───────────────────────────────────┐
│        DISTRIBUTED SENSOR NODES   │
│ Temperature | Air Quality          │
│ Occupancy   | Obstruction          │
└──────────────────┬────────────────┘
                   │
                   ▼
┌───────────────────────────────────┐
│       LOCAL COMMUNICATION LAYER   │
│ Wi-Fi | ESP-NOW | BLE | LoRa       │
└──────────────────┬────────────────┘
                   │
                   ▼
┌───────────────────────────────────┐
│         EDGE INTELLIGENCE         │
│ TinyML | Rules | Local Inference  │
└──────────────────┬────────────────┘
                   │
                   ▼
┌───────────────────────────────────┐
│          BUILDING WORLD STATE     │
│ Zone Risk | Blockages | Occupancy │
│ Route Status | Environmental Data │
└──────────────────┬────────────────┘
                   │
                   ▼
┌───────────────────────────────────┐
│          DYNAMIC ROUTE ENGINE     │
│ Risk-Aware Path Calculation        │
└──────────────────┬────────────────┘
                   │
             ┌─────┴─────┐
             ▼           ▼
┌─────────────────┐ ┌──────────────────┐
│ ADAPTIVE        │ │ LOCAL DASHBOARD  │
│ LED SIGNAGE     │ │ & MONITORING     │
└─────────────────┘ └──────────────────┘
```

---

## 🖥️ Live Software Demonstration

The current prototype includes a **browser-based simulation / digital-twin-style interface** for exploring changing emergency scenarios.

### Demonstration focus

* 🏢 Building-zone visualization
* 🔥 Simulated hazard activation
* 🚦 Zone risk updates
* 🧭 Dynamic route recalculation
* 💡 Adaptive direction indicators
* 📊 Local monitoring dashboard
* 🔄 Scenario reset and recovery

### 🔗 Live Demo

👉 https://evac-adaptive-emergency-evacuation-intelligence.ai.studio

---

## 🧪 Prototype Status

| Component                           | Status                         |
| ----------------------------------- | ------------------------------ |
| Browser-based evacuation simulation | ✅ Demonstration available      |
| Building-zone visualization         | ✅ Implemented in software      |
| Hazard scenario simulation          | ✅ Implemented in software      |
| Dynamic route logic                 | ✅ Prototype direction          |
| Dashboard concept                   | ✅ Demonstrated                 |
| ESP32 hardware integration          | 🔄 Planned / under development |
| Physical adaptive LED signage       | 🔄 Planned / under development |
| TinyML deployment                   | 🔄 Planned / under development |
| Real-building validation            | 🔄 Future work                 |
| Safety certification                | ❌ Not yet certified            |

> The current demonstration should be understood as a software prototype. Hardware integration and real-world validation are part of the planned development roadmap.

---

## 🔌 Planned Hardware Layer

The planned hardware prototype may include:

* ESP32 development boards
* Temperature and humidity sensors
* Air-quality / smoke-anomaly sensors
* PIR or motion sensors
* ToF / distance sensors for obstruction detection
* Adaptive LED arrow indicators
* Buzzers
* Local gateway or edge computer
* Battery-backed power support

### ⚠️ Hardware Design Considerations

Before real-world deployment, the system would require:

* Industrial-grade components
* Sensor calibration
* Redundancy
* Fail-safe operation
* Power backup
* Network-failure handling
* Cybersecurity review
* Fire-safety expert validation
* Required testing and certification

---

## 🚀 What Makes EVAC Interesting?

EVAC is not intended to replace certified fire-safety infrastructure.

Instead, it explores an intelligent and retrofit-friendly evacuation layer that combines:

* 📍 Zone-level sensing
* 🧠 Local risk intelligence
* 🗺️ Dynamic route optimization
* 💡 Adaptive physical guidance
* 🌐 Offline-first operation
* 🏗️ Retrofit-oriented deployment
* 📊 Local monitoring
* 🔄 Scenario-based simulation

### 🔍 Research and Design Opportunity

Global research and commercial systems already explore areas such as:

* Dynamic emergency signage
* Adaptive evacuation
* Fire-evacuation simulation
* Intelligent routing
* Building digital twins
* Sensor-based hazard detection

EVAC focuses on exploring a bridge between:

> **Live local sensing + distributed intelligence + deterministic route optimization + physical guidance**

with attention to:

* Indian high-occupancy buildings
* Retrofit-friendly deployment
* Affordability
* Local processing
* Network resilience
* Clear human-centred guidance

---

## 🇮🇳 Why This Matters in India

Many buildings may still depend heavily on:

* Static evacuation maps
* Fixed emergency signage
* Manual instructions
* Human coordination
* Infrastructure that does not adapt dynamically

During an emergency, changing conditions and confusion can make evacuation difficult.

EVAC aims to investigate whether an adaptive local system can provide:

> **Clearer, faster and more context-aware evacuation guidance.**

The intended approach is to work **alongside existing safety systems**, not replace them.

---

## 🛠️ Technology Stack Direction

### 💻 Software

* Browser-based simulation
* Building graph representation
* Dynamic risk-state management
* Route optimization
* Dashboard visualization
* Scenario-based testing

### 🔧 Hardware

* ESP32
* Environmental sensors
* Occupancy and motion sensors
* Obstruction detection
* LED indicators
* Local gateway

### 🧠 Edge Intelligence

* TinyML
* TensorFlow Lite for Microcontrollers
* Lightweight quantized models
* Rule-based fallback logic
* Local inference

### 🗺️ Algorithms

* Graph-based building representation
* Dijkstra’s algorithm
* Risk-weighted routing
* Dynamic edge-cost updates
* Zone-level state transitions

---

## 📁 Repository Structure

```text
EVAC/
├── README.md
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
├── simulation/
│   ├── scenarios/
│   ├── route-engine/
│   └── test-cases/
├── hardware/
│   ├── esp32/
│   ├── sensors/
│   └── signage/
├── docs/
│   ├── architecture/
│   ├── research/
│   └── screenshots/
├── models/
│   └── tinyml/
└── LICENSE
```

---

## 🧭 Development Roadmap

### Phase 1 — Software Validation

* [x] Build browser-based simulation
* [x] Visualize building zones
* [x] Simulate hazard conditions
* [x] Demonstrate route changes
* [ ] Add more emergency scenarios
* [ ] Add automated route-validation tests

### Phase 2 — Hardware Prototype

* [ ] Connect ESP32 nodes
* [ ] Integrate environmental sensors
* [ ] Add occupancy and obstruction sensing
* [ ] Build adaptive LED signage
* [ ] Establish local communication

### Phase 3 — Edge Intelligence

* [ ] Collect controlled sensor data
* [ ] Train lightweight classification models
* [ ] Quantize and deploy TinyML models
* [ ] Add rule-based fallback behaviour
* [ ] Evaluate false positives and false negatives

### Phase 4 — Controlled Testing

* [ ] Create a college-floor test environment
* [ ] Test simulated corridor blockages
* [ ] Compare static and adaptive routing
* [ ] Measure route recalculation time
* [ ] Evaluate signage understanding
* [ ] Document limitations and failure cases

### Phase 5 — Deployment Readiness

* [ ] Evaluate industrial-grade components
* [ ] Design redundancy and fail-safe behaviour
* [ ] Plan backup power
* [ ] Conduct cybersecurity review
* [ ] Assess compliance requirements
* [ ] Consult fire-safety experts
* [ ] Evaluate certification requirements

---

## 📊 Future Evaluation Metrics

EVAC can be evaluated using measurable indicators such as:

* ⏱️ Route recalculation latency
* 🧭 Route distance
* 🚧 Blockage detection accuracy
* 📡 Communication reliability
* 🧠 Risk-classification accuracy
* 💡 Signage response time
* 👥 User route comprehension
* 🔋 Operation during network disruption
* 🛑 Safe fallback behaviour

---

## ⚠️ Safety and Scope Disclaimer

> **EVAC is currently a prototype and software demonstration. Sensor readings, hazards, routes and building conditions shown in the demo may be simulated. EVAC is not a certified emergency-response or life-safety system and must not be used for real emergency evacuation. It is intended to enhance—not replace—existing fire-safety systems, emergency procedures, trained personnel and legally required infrastructure.**

---

## 👥 Team SYGNIX

| Role                     | Name                                              |
| ------------------------ | ------------------------------------------------- |
| **Team Leader**          | **Swadeep Bansode**                               |
| **Team ID**              | `119351`                                          |
| **Problem Statement ID** | `SIH26223`                                        |
| **Project**              | EVAC — Adaptive Emergency Evacuation Intelligence |

---

## 🤝 Contributions

Suggestions, technical feedback and collaboration are welcome.

This project is especially relevant to people interested in:

* IoT
* Embedded Systems
* TinyML
* Disaster Management
* Graph Algorithms
* Edge Computing
* Digital Twins
* Human-Centred Safety Design
* Emergency Systems

---

## 📜 License

This project is currently intended for educational, research and prototype-development purposes.

A formal open-source license may be added as the project evolves.

---

<p align="center">

## 🚨 Build smarter systems. Guide safer decisions. 🚨

### **EVAC — Because the safest exit is not always the nearest exit.**

<b>Built with ambition by Team SYGNIX.</b>

</p>
