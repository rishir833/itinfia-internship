# Microsoft Azure

## Introduction
Microsoft Azure is a cloud computing platform developed by Microsoft that provides a wide range of cloud services for building, deploying, managing, and scaling applications through Microsoft-managed data centers across the globe.

Azure offers over 200 cloud services, including virtual machines, storage, databases, networking, artificial intelligence, analytics, security, and DevOps tools. It enables organizations to reduce infrastructure costs, improve scalability, enhance security, and accelerate application development.

Azure supports multiple programming languages, frameworks, and operating systems, making it suitable for businesses of all sizes—from startups to large enterprises.

## Key Features of Microsoft Azure
- Scalability: Increase or decrease resources based on business requirements.
- High Availability: Built-in redundancy ensures applications remain available even during failures.
- Global Presence: Azure operates data centers in multiple regions worldwide, allowing applications to be deployed closer to users.
- Security: Offers advanced identity management, encryption, firewalls, compliance certifications, and threat protection.
- Hybrid Cloud Support: Seamlessly integrates on-premises infrastructure with cloud resources using services like Azure Arc and Azure Site Recovery.
- Disaster Recovery and Backup: Built-in backup and replication services help protect business-critical workloads.
- Pay-as-you-go Pricing: Customers only pay for the resources they consume.
- Automation: Supports infrastructure automation using Azure CLI, Azure PowerShell, ARM Templates, Bicep, and Terraform.


# Azure VM
How to create Azure VM and its reources

<img width="1022" height="455" alt="image" src="https://github.com/user-attachments/assets/43da2a9b-cc67-438a-b287-985bef9051ac" />

## Azure Subscription
### What is it?

An Azure Subscription is a logical container that provides access to Microsoft Azure services. It serves as the billing, management, and security boundary for all Azure resources. Every resource created in Azure must belong to a subscription. Organizations can create multiple subscriptions to separate projects, departments, or environments such as Development, Testing, and Production.

### Why do we use it?

Subscriptions are used to manage billing, monitor resource usage, control user access through Azure RBAC, and apply governance policies. They also help organizations organize resources efficiently while maintaining security and cost control.

## Resource Group
### What is it?

A Resource Group is a logical container that holds related Azure resources such as Virtual Machines, Storage Accounts, Virtual Networks, and Databases. Resources within the same project or application are usually placed in one Resource Group. It simplifies the management of resources throughout their lifecycle.

### Why do we use it?

Resource Groups help organize related resources, simplify deployment and management, assign permissions, monitor costs, and allow multiple resources to be updated or deleted together.

## Virtual Machine Name
### What is it?

The Virtual Machine Name is the unique identifier assigned to a VM when it is created. It helps distinguish one virtual machine from another within a Resource Group or subscription. The name appears in the Azure portal and is used in monitoring, automation, and management tools.

### Why do we use it?

A meaningful VM name makes it easier to identify, manage, monitor, and troubleshoot virtual machines. It also supports automation, reporting, and follows organizational naming conventions.

## Region
### What is it?

An Azure Region is a geographical location where Azure resources are deployed and hosted. Each region contains one or more Microsoft data centers that provide Azure services. The selected region determines where the Virtual Machine physically resides and which Azure services are available.

### Why do we use it?

Selecting the appropriate region reduces network latency, improves application performance, meets compliance and data residency requirements, and supports disaster recovery planning.

## Availability Options
### What is it?

Availability Options determine how Azure protects a Virtual Machine from hardware failures, planned maintenance, and unexpected outages. Azure offers options such as Availability Zones and Availability Sets to improve the reliability and availability of applications. These options distribute workloads across fault-tolerant infrastructure.

### Why do we use it?

Availability Options are used to minimize downtime, improve application uptime, protect workloads from infrastructure failures, and ensure business continuity for production environments.

## Zone Options
### What is it?

Zone Options define how the Availability Zone is assigned during Virtual Machine deployment. Users can either manually select an availability zone (Self-selected Zone) or allow Azure to automatically choose the most suitable zone (Azure-selected Zone). Availability Zones are physically separate data centers within the same Azure region, providing better fault tolerance.

### Why do we use it?

Zone Options help improve high availability by distributing workloads across different availability zones. They reduce the impact of data center failures and provide flexibility by allowing either manual or automatic zone selection during deployment.

<img width="987" height="388" alt="image" src="https://github.com/user-attachments/assets/83a1caad-e4cc-45e8-bc69-79fe824cc4d1" />
## Availability Zone
### What is it?

An Availability Zone is a physically separate data center within an Azure region, equipped with its own power, cooling, and networking infrastructure. Azure regions typically contain multiple availability zones to provide redundancy and fault isolation. When you deploy a Virtual Machine, you can choose the availability zone in which it will run. This ensures that workloads are distributed across independent data centers within the same region. Availability Zones are designed to provide high availability for critical applications.

### Why do we use it?

Availability Zones are used to protect applications from data center failures and planned maintenance events. They improve application uptime by ensuring that if one zone becomes unavailable, resources deployed in other zones continue to operate. This helps organizations build highly available and fault-tolerant cloud solutions.

## Security Type
### What is it?

The Security Type determines the level of security applied to a Virtual Machine during deployment. Azure offers different security options to protect VMs from malware, unauthorized access, and boot-level attacks. The available options are:

* Standard
  * Provides the default security features for a Virtual Machine.
  * Suitable for development, testing, and general-purpose workloads.
  * Does not include advanced security features like Secure Boot or virtual TPM.
* Trusted Launch
  * Provides enhanced security for Gen2 Virtual Machines.
  * Enables Secure Boot, which prevents unauthorized operating systems and bootloaders from loading during startup.
  * Includes a Virtual Trusted Platform Module (vTPM) to securely store encryption keys and credentials.
  * Protects against bootkits, rootkits, and firmware-level attacks.
  * Recommended for production environments requiring higher security.
* Confidential Virtual Machines
  * Designed for highly sensitive and confidential workloads.
  * Uses hardware-based memory encryption to protect data while it is being processed.
  * Prevents cloud administrators and unauthorized users from accessing data stored in memory.
  * Commonly used in healthcare, banking, government, and financial sectors where data privacy is critical.

### Why do we use it?

The Security Type is used to protect Virtual Machines from security threats and unauthorized access. It helps secure the operating system, applications, and sensitive data by enabling different levels of protection based on workload requirements. Choosing the appropriate security type improves compliance, strengthens security, and reduces the risk of cyberattacks.


## Image
### What is it?

An Image is a pre-configured operating system or software template used to create a Virtual Machine. Azure provides a wide range of images, including Windows Server, Ubuntu, Red Hat Enterprise Linux, Debian, and other operating systems. Some images also include pre-installed software such as SQL Server or Visual Studio. Selecting an image determines the operating system and initial configuration of the Virtual Machine.

### Why do we use it?

Images simplify and speed up VM deployment by providing ready-to-use operating systems and application environments. They eliminate the need for manual installation and configuration, ensuring consistency across deployments. Users can also create custom images to deploy identical virtual machines for specific workloads.

## VM Architecture
### What is it?

VM Architecture specifies the processor architecture on which the Virtual Machine will run. Azure currently supports x64 (64-bit) and Arm64 architectures. The selected architecture must be compatible with the operating system image and the applications you intend to run. Most enterprise applications and operating systems are designed for x64, while Arm64 is optimized for specific workloads and energy efficiency.

### Why do we use it?

VM Architecture ensures compatibility between the hardware platform, operating system, and applications. Selecting the correct architecture improves performance, optimizes resource utilization, and ensures that software runs without compatibility issues. For most workloads, x64 is the recommended and widely supported architecture.


## Size 
<img width="1037" height="75" alt="image" src="https://github.com/user-attachments/assets/1dc0d5e7-9a64-46f4-a45b-6a82d705c4e6" />

### What is it?

The Size of a Virtual Machine determines the amount of computing resources allocated to it, including the number of Virtual CPUs (vCPUs), Memory (RAM), Storage Performance, and Network Bandwidth. Azure offers a wide range of VM sizes, each designed for different workloads such as development, web hosting, databases, high-performance computing, and AI applications. Choosing the correct VM size ensures that the application has sufficient resources while maintaining cost efficiency.

### Why do we use it?

VM Size is selected based on the performance requirements of the workload. It helps optimize resource utilization, improve application performance, and control infrastructure costs. Azure allows VM sizes to be changed later if workload requirements increase or decrease, providing flexibility and scalability.

 ### Common Azure VM Size Series
* B-Series (Burstable)
  * Best for development, testing, and small web servers.
  * Low-cost VMs that can temporarily burst CPU performance when needed.
* D-Series (General Purpose)
  * Balanced CPU and memory.
  * Suitable for enterprise applications, web servers, and business workloads.
* E-Series (Memory Optimized)
  * Provides a higher memory-to-CPU ratio.
  * Ideal for databases, in-memory applications, and analytics.
* F-Series (Compute Optimized)
  * Offers higher CPU performance with less memory.
  * Best for batch processing, gaming servers, and compute-intensive applications.
* L-Series (Storage Optimized)
  * High disk throughput and storage capacity.
  * Used for big data, NoSQL databases, and storage-intensive workloads.
* N-Series (GPU Enabled)
  * Equipped with NVIDIA GPUs.
  * Suitable for AI, Machine Learning, deep learning, graphics rendering, and video processing.
 
## Authentication Type
<img width="577" height="68" alt="image" src="https://github.com/user-attachments/assets/6b564fe4-eaa7-49b2-b417-b20b6966f103" />

#### What is it?

The Authentication Type defines how users authenticate and securely connect to a Virtual Machine after deployment. Azure provides two authentication methods: SSH Public Key and Password. The selected method verifies the user's identity before allowing access to the VM. For Linux Virtual Machines, SSH Public Key is the recommended option because it offers stronger security than passwords.

### Why do we use it?

Authentication Type is used to secure access to the Virtual Machine and prevent unauthorized logins. It ensures that only authenticated users can access the VM while improving overall security and reducing the risk of unauthorized access.

### Authentication Methods
* SSH Public Key
  * Uses a public and private key pair for secure authentication.
  * More secure than passwords and recommended for Linux VMs.
* Password
  * Uses a username and password to access the VM.
  * Simple to configure and suitable for testing or Windows VMs.
 
 ## Username

 <img width="1012" height="32" alt="image" src="https://github.com/user-attachments/assets/d7f293a7-8fea-4264-b9cc-19b00e231749" />

### What is it?

The Username is the administrator account created for the Virtual Machine during deployment. It is used to log in and manage the operating system after the VM is created. The username must be unique within the VM and follow Azure's naming rules. It works together with the selected authentication method, such as an SSH key or password, to provide secure access.

### Why do we use it?

The Username is used to identify the administrator who accesses the Virtual Machine. It provides a secure way to manage the VM, install software, configure settings, and perform administrative tasks. Choosing a meaningful username also helps maintain consistency and simplifies VM management.

## SSH Key Type

<img width="528" height="72" alt="image" src="https://github.com/user-attachments/assets/22ae42be-3fdc-474b-a365-ebbc8c9f7658" />

### What is it?

The SSH Key Type determines the encryption algorithm used to generate the SSH key pair for secure access to the Virtual Machine. Azure supports two SSH key formats: RSA and Ed25519. The selected key type is used during authentication when connecting to the VM using SSH. Both methods provide secure, passwordless access to Linux Virtual Machines.

### Why do we use it?

The SSH Key Type is used to establish secure communication between the user and the Virtual Machine. It enhances security by replacing passwords with cryptographic keys, reducing the risk of unauthorized access and brute-force attacks.

### SSH Key Types
* RSA SSH Format
  * Widely supported and compatible with most SSH clients and systems.
  * Recommended when broad compatibility is required.
* Ed25519 SSH Format
  * Uses a modern encryption algorithm with stronger security.
  * Generates smaller keys and provides faster authentication.


## Key Pair Name

<img width="1016" height="35" alt="image" src="https://github.com/user-attachments/assets/b24425ac-358f-4988-8986-f74bca03070f" />


The Key Pair Name is the name assigned to the SSH key pair that is used to authenticate and securely access the Virtual Machine. It helps identify and manage the SSH key within Azure. The key pair consists of a public key, which is stored on the VM, and a private key, which is downloaded and kept securely by the user. Using a meaningful key pair name makes it easier to identify the correct key when managing multiple Virtual Machines.
