# Charles Chow

I build real-time systems that stay reliable under load, failure, and imperfect conditions.

Backend • Distributed Systems • Real-Time Infrastructure  
San Jose, California  
Portfolio: https://yaochongchow.github.io/

---

## What I Care About

Most systems work when everything is ideal.  
The systems I build are designed for when things go wrong.

Requests arrive out of order.  
Devices drop packets.  
Latency spikes under load.  
Backends fail at the tail.

I focus on making systems **observable, debuggable, and stable under these conditions**.

---

## Recent Production Impact

- Handled ~900 req/sec during peak telemetry ingestion from live device streams while maintaining **sub-180ms p95 latency** (Node.js + Redis, NeuroLeap)
- Reduced slow query latency (p95) from **420ms → 110ms** on a production dataset (8M+ rows), eliminating dashboard timeouts under load (PostgreSQL optimization)
- Scaled telemetry ingestion to **~1.2M records/hour** across 8 channels with stable downstream processing
- Reduced BLE packet loss from **9.2% → 1.8%**, enabling long-duration, reliable test sessions for embedded systems
- Reduced recurring production incidents by **32%** and improved MTTR by **60%** through validation, observability, and API reliability improvements

---

## Selected Work

### Distributed Rate Limiter  
https://github.com/yaochongchow/distributed-rate-limiter  

Built a distributed rate limiter to enforce consistent request limits across services under high concurrency.  
Uses Redis Cluster and Lua scripts for atomic decision-making across nodes.

- Sustained ~12K req/sec with ~12ms p95 latency under concurrent load
- Designed for correctness under race conditions and partial failures
- Includes observability (Prometheus + Grafana) and fault-injection testing

---

### ShopCloud E-Commerce Platform  
https://github.com/yaochongchow/ecommerce-microservice  

Designed an event-driven microservices architecture to coordinate distributed transactions across services.

- 7 services with Saga-based orchestration for consistency
- AWS-based infrastructure (SQS, SNS, Lambda, DynamoDB)
- Designed for failure recovery and eventual consistency in real-world workflows

---

### Interactive SQL Tutor  
https://github.com/yaochongchow/interactive-sql-tutor  

Built a learning platform that evaluates SQL submissions and provides structured AI-generated hints.

- Django + React full-stack system
- Per-submission sandboxing for safe query execution
- AI hinting with controlled context and output structure
- Focus on reliability and predictable behavior in LLM-assisted systems

---

### Warehouse Delivery Robot  
https://github.com/yaochongchow/warehouse-delivery-robot  

Developed a ROS2-based robotics system for navigation and task execution in simulation.

- Differential-drive robot modeled in URDF/xacro
- Nav2-based waypoint navigation with tuned planner/controller
- rosbag2 logging for replayable debugging and failure analysis
- Diagnostics pipeline for system-level observability

---

### Traffic Monitoring System  
https://github.com/yaochongchow/traffic-monitor  

Built a real-time video processing pipeline for traffic analysis.

- OpenCV + YOLO-based detection pipeline
- Real-time inference and frame processing
- Designed for performance under streaming conditions

---

## Systems I’ve Worked With

- Real-time telemetry pipelines from embedded devices (BLE)
- Distributed backend services under concurrent load
- Robotics systems (ROS2, Nav2, simulation, diagnostics)
- ML pipelines with real-time inference constraints
- Cloud-native systems on AWS (Lambda, SQS, SNS, DynamoDB, S3)

---

## How I Debug Systems

- Instrument first (metrics, logs, traces)
- Reproduce issues under realistic load conditions
- Focus on tail latency, not averages
- Isolate bottlenecks (database, network, concurrency, I/O)
- Fix root causes, not surface symptoms

---

## Engineering Approach

- Measure before optimizing  
- Instrument before guessing  
- Design for failure modes, not just happy paths  
- Keep systems explainable under load  

---

## Contact

Email: yaochong.chow.20@gmail.com  
LinkedIn: https://www.linkedin.com/in/charles-chow-yc  
GitHub: https://github.com/yaochongchow
