# OpenCDI: Open Containerized Desktop Infrastructure

OpenCDI (Open Containerized Desktop Infrastructure) is an open-source project dedicated to building a modern, secure, and scalable container-based desktop delivery platform. Leveraging the power of containerization and Kubernetes, OpenCDI aims to provide a flexible and efficient alternative to traditional Virtual Desktop Infrastructure (VDI), with a strong focus on supporting domestic Chinese operating systems and hardware for enhanced information security.

## Project Mission

In the era of cloud computing, big data, and AI, traditional desktop management systems often struggle to meet evolving demands for flexibility, security, and scalability. Container technology offers a lightweight, portable, efficient, and secure paradigm for application deployment and migration, reducing operational costs and improving user experience. OpenCDI embraces container technology to offer a unified desktop environment and management platform, boosting office efficiency and supporting multi-terminal access and collaborative work, particularly tailored for the digital transformation needs of enterprises within the domestic ecosystem.

OpenCDI seeks to address the limitations of existing solutions by providing a container-native approach that is performant, secure, and easy to manage at scale, while ensuring compatibility with domestic technology stacks.

## Why OpenCDI? Addressing the Challenges

OpenCDI is specifically designed to tackle the critical challenges faced by traditional VDI and existing container-based desktop solutions:

* **Simplified Management:** Reducing the steep learning curve of Linux/Containers for users and administrators through intuitive UI, centralized image management, and automated operations.
* **High-Performance Persistence:** Overcoming the I/O bottlenecks of traditional NFS for user data by integrating high-performance distributed storage.
* **Efficient Application Handling:** Providing a unified, efficient solution for persistent application data and facilitating reuse across containers using layered storage.
* **Optimized Remote Access:** Developing a container-native, low-latency, high-concurrency remote protocol (H5/WebSocket based).
* **Enhanced Peripheral Support:** Enabling seamless mapping of USB devices, printers, UKeys, and reliable audio redirection within containers.
* **Robust Security:** Strengthening container isolation beyond standard namespaces/cgroups using micro-virtualization (gVisor/Kata Containers) to prevent escapes.
* **VM-like User Experience:** Abstracting container lifecycle to mimic traditional VM "power on/off" and providing simplified snapshot and recovery capabilities.
* **Broad Software Compatibility:** Improving support for traditional desktop software, including security suites (Antivirus, EDR) and office applications, within the container environment.
* **Granular Monitoring:** Providing deep visibility into the internal state of desktop containers, similar to VM consoles.
* **Large-Scale Management:** Architected for managing tens of thousands of desktop containers across multiple clusters with automation.
* **Domestic OS/Hardware Compatibility:** Ensuring compatibility with various domestic Linux kernel versions and hardware components.
* **Streamlined Deployment:** Offering simplified, cost-effective deployment models (integrated hyper-converged and decoupled).
* **Feature Parity:** Matching core VDI features like clipboard sharing, dynamic resolution, SSO, and watermarking.
* **High Availability & Fast Recovery:** Ensuring platform and desktop resilience with rapid recovery from failures.
* **Stable Long-Term Operation:** Mitigating issues like process leaks and log accumulation in long-running containers.
* **Rapid Client Connection:** Achieving fast desktop access times comparable to traditional VMs.

## Key Features

* **Container-Native Desktop Delivery:** Desktops are delivered as secure, isolated containers orchestrated by Kubernetes.
* **Flexible Desktop Environments:** Support for various Linux distributions and desktop environments (inspired by Webtop [1]).
* **High-Performance Distributed Storage Integration:** Seamless integration with modern distributed storage systems (e.g., Longhorn, Ceph) via CSI for user data persistence.
* **Layered Image and Application Management:** Efficient management and reuse of base OS and application layers using OverlayFS techniques (inspired by Kasm Workspaces [2]).
* **Modern Remote Protocol:** Low-latency, high-framerate remote access via H5/WebSocket.
* **Enhanced Security Isolation:** Utilizing gVisor or Kata Containers for strong container sandboxing.
* **Simplified Lifecycle Management:** Abstracting container operations to provide a user-friendly "VM-like" experience.
* **Integrated Peripheral & Audio Support:** Reliable forwarding of USB devices, printers, and audio.
* **Centralized Management Platform:** Intuitive web interface for administrators to manage users, images, desktops, and policies.
* **Scalability:** Designed for large-scale deployments using Kubernetes multi-cluster strategies.
* **Domestic Ecosystem Support:** Prioritizing compatibility with国产 (domestic) operating systems and hardware.
* **Automation & Orchestration:** Leveraging Kubernetes and automation tools for simplified operations.

## Architecture

OpenCDI adopts a layered architecture to ensure modularity, maintainability, and flexibility. The architecture includes Presentation, Application Logic, Core Logic, and Infrastructure layers, integrating with external components like Kubernetes, storage systems, and identity providers.

For a detailed breakdown of the architecture, please refer to the [Architecture Document](docs/architecture.md).

## Getting Started

**(Note: This section contains placeholder instructions. Detailed setup guides will be provided as the project develops.)**

1.  **Prerequisites:**
    * A Kubernetes cluster (version 1.20.x or later recommended).
    * A compatible distributed storage system (e.g., Longhorn, Ceph) configured with a CSI driver.
    * Go programming language (version 1.20.2 or later) if building from source.
    * Docker or other container build tools.

2.  **Building:**
    ```bash
    git clone [https://github.com/turtacn/opencdi.git](https://github.com/turtacn/opencdi.git)
    cd opencdi
    make build # Placeholder: This command will be implemented in build/Makefile
    ```

3.  **Deployment:**
    ```bash
    make deploy # Placeholder: This command will deploy OpenCDI to your K8s cluster
    ```
    Refer to the `docs/deployment.md` (to be created) for detailed deployment instructions.

## Documentation

* **Architecture Document:** [docs/architecture.md](docs/architecture.md)
* **Development Guide:** (Coming Soon)
* **Deployment Guide:** (Coming Soon)
* **API Reference:** (Coming Soon)

## Contributing

We welcome contributions to the OpenCDI project! Please see the [CONTRIBUTING.md](CONTRIBUTING.md) (to be created) file for details on how to get involved.

## License

OpenCDI is licensed under the [Apache 2.0 License](LICENSE) (to be created). See the `LICENSE` file for details.

## References

- [1] linuxserver/docker-webtop: <https://github.com/linuxserver/docker-webtop>

- [2] linuxserver/docker-kasm: <https://github.com/linuxserver/docker-kasm>

