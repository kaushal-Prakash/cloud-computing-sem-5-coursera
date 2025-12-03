# ☁ Introduction to Cloud Computing: Complete Course Notes
## Module 1: Overview of Cloud Computing
### 1. What is Cloud Computing?
**Definition**: Cloud Computing is the on-demand delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the Internet ("the cloud") with pay-as-you-go pricing.
### 2. Essential Characteristics (NIST - National Institute of Standards and Technology, Definition)
 * **On-Demand Self-Service**: Consumers can unilaterally provision computing capabilities, such as server time and network storage, without requiring human interaction with each service provider.
 * Broad Network Access: Capabilities are available over the network and accessed through standard mechanisms (e.g., mobile phones, laptops).
 * Resource Pooling: The provider's computing resources are pooled to serve multiple consumers using a multi-tenant model, with resources dynamically assigned and reassigned according to consumer demand. (e.g., storage, processing, memory, network bandwidth).
 *** Rapid Elasticity**: Capabilities can be rapidly and elastically provisioned and released, sometimes automatically, to scale rapidly outward and inward commensurate with demand.
 * **Measured Service**: Cloud systems automatically control and optimize resource usage by leveraging a metering capability. Resources are monitored, controlled, and reported, providing transparency for both the provider and consumer.
### 3. The Business Case for Cloud
 * Reduced Capital Expenditure (CapEx): Shift from buying hardware/software (CapEx) to paying for services as consumed (Operating Expenditure/OpEx).
 * Increased Speed and Agility: Faster deployment of resources means quicker time-to-market.
 * Scalability: Easily handle spikes in demand without over-provisioning.
 * Focus on Core Business: IT staff can focus on innovation rather than infrastructure maintenance.
 * Cost Savings: Economy of scale offered by providers leads to lower costs.
## Module 2: Cloud Computing Service and Deployment Models
### 1. Cloud Service Models (The "As a Service" Stack)
These models define the level of management provided by the vendor.

| Model | Abbreviation | Description | Management Responsibility | Example |
|---|---|---|---|---|
| Software as a Service | SaaS | The complete application is managed and hosted by the vendor. Users interact via a web browser or client. | Vendor manages everything (Application, Data, OS, Infrastructure). | Salesforce, Gmail, Office 365. |
| Platform as a Service | PaaS | Provides an environment for building, testing, and deploying software applications. Users manage code and data, but not the underlying infrastructure. | Vendor manages OS, Runtime, Middleware, Infrastructure. User manages Applications and Data. | AWS Elastic Beanstalk, Google App Engine, IBM Cloud Foundry. |
| Infrastructure as a Service | IaaS | Provides fundamental computing resources over the internet, including virtual machines, storage, and networks. Users manage the OS and applications. | Vendor manages Networking, Storage, Servers, Virtualization. User manages OS, Applications, and Data. | Amazon EC2, Microsoft Azure VMs, IBM Cloud Virtual Servers. |
### 2. Cloud Deployment Models
 * **Public Cloud**: Services are delivered over the public internet and are available to the general public. Owned and operated by a third-party cloud service provider (e.g., AWS, Azure, GCP).
 * **Private Cloud**: Cloud infrastructure is operated solely for a single organization. It may be managed by the organization or a third party and may exist on or off premises. Offers high control and security.
 * **Hybrid Cloud**: A composition of two or more distinct cloud infrastructures (private, public) that remain unique entities but are bound together by proprietary technology that enables data and application portability.
 * **Multicloud**: The use of multiple cloud services from different providers (e.g., using AWS for compute and Azure for identity management). This is often used to avoid vendor lock-in.
## Module 3: Components of Cloud Architecture (Cloud Infrastructure)
Cloud architecture relies heavily on Virtualization to deliver its core services.
### 1. Virtualization and Virtual Machines (VMs)
 * **Virtualization**: Technology that allows a single physical resource (like a server) to be partitioned into multiple logical resources (like Virtual Machines). This is the key enabler of resource pooling.
 * **Hypervisor**: Software that creates and runs Virtual Machines (VMs). It manages the host machine's resources and allocates them to the VMs.
   * Type 1 (Bare Metal): Runs directly on the host hardware (e.g., VMware ESXi).
   * Type 2 (Hosted): Runs on top of a conventional operating system (e.g., VMware Workstation).
 * Virtual Machine (VM): An emulation of a computer system. It is a software-defined computer that runs an OS and applications, completely independent of the physical hardware.
### 2. **Containers**
 * Containers: An alternative to VMs. They package an application with all its dependencies (libraries, configs) but share the host OS kernel.
 * Key Advantage: Lightweight and fast to start because they don't include an entire OS, just the necessary components to run the application.
 * Docker is the most popular container platform; Kubernetes is the most popular container orchestration tool.
### 3. **Networking**
Cloud networks ensure secure and high-speed communication between components:
 * Virtual Private Cloud (VPC): A logically isolated virtual network dedicated to a single cloud customer, within a public cloud environment.
 * Load Balancing: Distributes incoming application traffic across multiple servers to increase capacity and fault tolerance.
## Module 4: Cloud Storage
Cloud storage is defined by how the data is accessed and managed.
### 1. Types of Cloud Storage

| **Type**           | **Access Method**                                                               | **Use Case**                                                                     | **Key Features**                                                                           |
| ------------------ | ------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| **Block Storage**  | Raw, unformatted volume access; mounted as a disk and managed by OS file system | Virtual machine root disks, transactional databases requiring high performance   | High-speed & low-latency access, typically attached to a single VM or server               |
| **File Storage**   | Standard file-sharing protocols like NFS/SMB                                    | Shared storage for multiple users/servers, web content hosting, home directories | Hierarchical directory structure, POSIX-like permissions, supports collaboration           |
| **Object Storage** | API-based access using HTTP/HTTPS; data stored as objects in flat namespace     | Backups, big data, media storage, static website assets, data lakes              | Highly durable and scalable, metadata-rich objects, tiered storage (Standard, IA, Archive) |

### 2. Content Delivery Networks (CDNs)
 * CDN: A geographically distributed network of proxy servers and their data centers.
 * Purpose: To distribute content (like images, videos, or web pages) closer to users to reduce latency and improve load times.
## Module 5: Cloud Native and Emergent Cloud Trends
### 1. Hybrid Multicloud
 * Hybrid Cloud: Mixing one public and one private cloud.
 * Multicloud: Using services from multiple public cloud providers (e.g., AWS, Azure, GCP).
 * Hybrid Multicloud: The use of multiple cloud providers, including at least one public cloud and one private cloud environment, working together. This maximizes resilience and minimizes vendor lock-in.
### 2. Cloud Native
 * An approach to building and running applications to take full advantage of the cloud computing model.
 * Key Concepts: Containers, Microservices, and Serverless Computing.
### 3. Microservices
 * An architectural style where a single application is composed of many smaller, loosely coupled services.
 * Each service is independently deployable, manageable, and scalable, communicating via lightweight APIs (e.g., REST).
### 4. Serverless Computing (Function as a Service - FaaS)
 * A cloud execution model where the cloud provider dynamically manages the allocation and provisioning of servers.
 * The user only writes and deploys code (functions) and pays only when the code is executing. No need to provision or manage VMs/servers.
 * Examples: AWS Lambda, Azure Functions, IBM Cloud Functions.
### 5. DevOps
 * A set of practices that combines software development (Dev) and IT operations (Ops) to shorten the development lifecycle and provide continuous delivery with high software quality.
 * Automation and Continuous Integration/Continuous Delivery (CI/CD) pipelines are central to DevOps in the cloud.
## Module 6: Cloud Security and Monitoring
### 1. The Shared Responsibility Model
A core concept in cloud security:
 * Cloud Provider (AWS, IBM, etc.) is responsible for Security of the Cloud (physical facilities, hardware, network infrastructure, virtualization layer).
 * Cloud Customer is responsible for Security in the Cloud (Guest OS patching, application security, identity and access management, data encryption).
### 2. Key Security Concepts
 * Identity and Access Management (IAM): Defines and manages users and their access levels (permissions) to cloud resources.
 * Cloud Encryption: Protecting data both at rest (in storage, databases) and in transit (over the network) using encryption keys.
### 3. Cloud Monitoring
 * The process of tracking and evaluating the operational metrics, performance, and health of cloud resources and applications.
 * Benefits: Proactive detection of issues, performance optimization, and tracking resource utilization for cost control.
### 4. Career Opportunities
Cloud computing has created numerous specialized roles:
 * Cloud Architect: Designs and plans cloud environments and strategy.
 * Cloud Developer: Builds and deploys applications using cloud services.
 * Cloud Administrator/Engineer: Manages and maintains the cloud infrastructure and operations.
 * Cloud Security Engineer: Focuses on securing cloud resources and ensuring compliance.
