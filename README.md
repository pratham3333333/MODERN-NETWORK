# Unit 4 - README: Quality of Service (QoS), Quality of Experience (QoE), and Cloud Computing

---

## Chapter 10: Architectural Framework and Integrated Services

### 1. **Architectural Framework for QoS Support**

**Explanation:**
The Architectural Framework for QoS (Quality of Service) support provides mechanisms and models to ensure reliable, predictable network performance for different applications like video conferencing, VoIP, etc.

**Key Components:**
- **Traffic Classifier**: Identifies and classifies the traffic into flows.
- **Admission Control**: Determines whether new traffic flows can be admitted.
- **Resource Reservation**: Reserves necessary resources along the path.
- **Packet Scheduler**: Manages transmission of packets based on priority.
- **QoS Management & Monitoring**: Monitors performance and manages QoS policies.

**Diagram:**
```
+------------------------+
|    QoS Management     |
+------------------------+
           |
+------------------------+
|  Traffic Classification|
+------------------------+
           |
+------------------------+
|    Admission Control   |
+------------------------+
           |
+------------------------+
| Resource Reservation  |
+------------------------+
           |
+------------------------+
|   Packet Scheduling    |
+------------------------+
```

---

### 2. **Integrated Service Architecture (ISA) and Background Functions**

**Explanation:**
ISA is a QoS model designed to provide end-to-end QoS guarantees. It works by reserving resources for individual data flows across the network using protocols like RSVP (Resource Reservation Protocol).

**Principles:**
- **Per-flow resource reservation**
- **Use of RSVP for signaling**
- **Admission control and traffic policing**

**Background Functions:**
- **Routing**: Determines paths for data flows.
- **Reservation Protocols (RSVP)**: Establishes and maintains resource reservations.
- **Traffic Control**: Enforces policies using queuing and shaping.

**Diagram:**
```
+----------+     +----------+     +----------+
|  Sender  |<--->| Routers  |<--->| Receiver |
+----------+     +----------+     +----------+
     |               |               |
     |<- RSVP PATH ->|               |
     |               |<- RESV MSG ->|
```

---

## Chapter 11: Quality of Experience (QoE)

### 1. **QoE/QoS Layered Model**

**Explanation:**
The layered model bridges the technical QoS metrics with the human-perceived QoE. It includes various abstraction layers:

**Layers:**
- **Application Layer**: User perception (e.g., video clarity)
- **Service Layer**: Service metrics (e.g., buffering time)
- **Network Layer**: QoS metrics (e.g., delay, jitter)
- **Infrastructure Layer**: Physical layer performance

**Diagram:**
```
+---------------------+
|  Application Layer  |
+---------------------+
|    Service Layer    |
+---------------------+
|    Network Layer    |
+---------------------+
| Infrastructure Layer|
+---------------------+
```

---

### 2. **Subjective Assessment of QoE**

**Explanation:**
Subjective assessment refers to methods that gather direct user feedback on the perceived quality of a service.

**Methods Include:**
- **MOS (Mean Opinion Score)**: Rating from 1 (bad) to 5 (excellent)
- **Paired Comparison Tests**: Comparing different service versions
- **User Surveys/Feedback**: Collects real user opinions

**Advantages:**
- Captures real user experience
- Reflects human perception accurately

**Limitations:**
- Time-consuming
- Expensive
- Subject to user bias

---

### 3. **Objective Assessment of QoE**

**Explanation:**
Objective assessment uses mathematical models and metrics to estimate QoE without user involvement.

**Techniques:**
- **PSNR (Peak Signal to Noise Ratio)**
- **SSIM (Structural Similarity Index)**
- **VQM (Video Quality Model)**
- **Network QoS Parameters**: Delay, jitter, packet loss

**Advantages:**
- Automated and fast
- Scalable and reproducible

**Limitations:**
- May not align with user perception
- Needs calibration with subjective data

---

## Chapter 13: Cloud Computing

### 1. **Cloud Computing Elements**

**Explanation:**
Cloud computing involves delivering computing services like storage, processing, and networking over the internet.

**Key Elements:**
- **Clients**: End users accessing services
- **Datacenters**: Resource pool and infrastructure
- **Distributed Servers**: Deliver services globally

**Diagram:**
```
+----------+       +------------------+
|  Client  |<----->|  Cloud Services  |
+----------+       +------------------+
                        |
               +------------------+
               |   Data Centers   |
               +------------------+
```

---

### 2. **Short Note on Cloud Networking and Cloud Storage**

**Cloud Networking:**
Cloud networking enables scalable and flexible connectivity between cloud-based services. It involves using virtual networks, VPNs, and SDN (Software Defined Networking) for dynamic routing and secure access.

**Cloud Storage:**
Cloud storage offers on-demand data storage managed by cloud providers. It allows scalability, remote access, and durability. Examples include Google Drive, Dropbox, AWS S3.

---

### 3. **Cloud Service Models**

**Explanation:**
Cloud services are categorized based on the level of abstraction and control provided.

**Models:**
- **IaaS (Infrastructure as a Service)**: Hardware-level resources (e.g., AWS EC2)
- **PaaS (Platform as a Service)**: Application platforms (e.g., Google App Engine)
- **SaaS (Software as a Service)**: End-user applications (e.g., Gmail, Office 365)

**Diagram:**
```
+------------------+
|     SaaS         |
+------------------+
|     PaaS         |
+------------------+
|     IaaS         |
+------------------+
```

---

### 4. **Separation of Responsibility in Cloud Operation**

**Explanation:**
In cloud operations, responsibilities are shared between the cloud provider and the customer based on the service model.

**Responsibility Distribution:**
- **IaaS**: Customer manages OS, apps, data. Provider manages virtualization, storage.
- **PaaS**: Customer manages apps, data. Provider manages OS, platform.
- **SaaS**: Provider manages everything. Customer just uses the app.

**Diagram:**
```
+--------------+-------------------------+----------------------+
| Responsibility|     Cloud Provider     |      Customer        |
+--------------+-------------------------+----------------------+
| IaaS         | Network, Storage        | OS, Apps, Data       |
| PaaS         | Platform, OS            | Applications, Data   |
| SaaS         | All (infra to app)      | Just uses the app    |
+--------------+-------------------------+----------------------+
```

---



