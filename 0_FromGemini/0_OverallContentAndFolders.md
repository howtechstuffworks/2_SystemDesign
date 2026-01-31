# High-Signal System Design Reading List

### 1. General Distributed Systems (The Foundation)
* **[System Design Primer (Donne Martin)](https://github.com/donnemartin/system-design-primer)**
  > The industry-standard open-source textbook. It serves as your dictionary for core concepts like scalability, consistent hashing, and CAP theorem.
* **[ByteByteGo (Alex Xu)](https://bytebytego.com/)**
  > The best visual resource for system design. It excels at breaking down complex components (like Kafka, Redis, or API Gateways) into single, high-clarity architectural diagrams.
* **[Discord Engineering: How We Stored Trillions of Messages](https://discord.com/blog/how-discord-stores-trillions-of-messages)**
  > A definitive "War Story" blog. It explains **why** Discord failed with MongoDB, moved to Cassandra, and finally built a custom ScyllaDB architecture. It teaches trade-offs (Latency vs. Consistency) better than any textbook.

### 2. Machine Learning Systems (The Software Stack)
* **[Designing Machine Learning Systems (Chip Huyen)](https://www.amazon.com/Designing-Machine-Learning-Systems-Production-Ready/dp/1098107969)**
  > The comprehensive guide to the ML lifecycle. It covers the crucial "Data Engineering" and "Serving" layers that exist before and after the compute.
* **[PyTorch 2.0: The Journey to TorchDynamo](https://pytorch.org/blog/pytorch-2.0-release/)**
  > The definitive engineering blog on the **"Graph Capture"** problem. It explains how PyTorch 2.0 captures dynamic Python code into static graphs for compilation without breaking the user experience.
* **[OpenXLA: The Compiler for the AI Era](https://opensource.googleblog.com/2023/03/openxla-is-ready-to-accelerate-and-simplify-ml-development.html)**
  > This explains the **"Optimization"** layer. It details how the XLA compiler acts as the bridge between software (PyTorch/JAX) and hardware (TPU/GPU) via operator fusion.

### 3. TPU & Hardware Architecture (The Google Stack)
* **[TPU v4: An Optically Reconfigurable Supercomputer](https://cloud.google.com/blog/products/compute/tpu-v4-enables-high-performance-ml-at-scale)**
  > The deep dive on **Optical Circuit Switching (OCS)**. It explains how Google uses mirrors to dynamically reconfigure the network topology of a supercomputer to match the model's shape.
* **[Pathways: Asynchronous Distributed Dataflow for ML](https://blog.google/technology/ai/introducing-pathways-next-generation-ai-architecture/)**
  > The architecture behind Gemini. It explains the **"Single Controller"** model (building on GSPMD) that allows a single Python program to orchestrate thousands of chips asynchronously.

### 4. Memory Systems & Tiering (The VMM Angle)
* **[Meta Engineering: Transparent Page Placement (TPP)](https://engineering.fb.com/2022/06/20/data-center-engineering/transparent-page-placement/)**
  > A perfect "System Design" case study for memory architects. It details how Meta modified the Linux Kernel to handle **Tiered Memory** (CXL/Slow RAM) using intelligent page promotion/demotion logic.
* **[Google: Warehouse-Scale Memory (Tiered Memory at Scale)](https://research.google/pubs/pub50360/)**
  > A foundational paper explaining the "Stranded Memory" problem in data centers, which led to the modern trend of memory disaggregation.

### 5. Writing Venues (Examples of "Good" Articles)
* **[InfoQ: "Netflix Conductor: A Microservices Orchestrator"](https://www.infoq.com/articles/netflix-conductor/)**
  > A strong example of an "EB1A-style" architectural article. It follows a clear structure: Problem → Failed Attempts → New Architecture → Results.
* **[ACM Queue: "Real-time Data Processing at Facebook"](https://queue.acm.org/detail.cfm?id=2945077)**
  > A prestigious technical publication. This article demonstrates how to write about complex systems trade-offs without revealing proprietary code.
