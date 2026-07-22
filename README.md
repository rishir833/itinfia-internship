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


## Availability Zone

<img width="987" height="388" alt="image" src="https://github.com/user-attachments/assets/83a1caad-e4cc-45e8-bc69-79fe824cc4d1" />


### What is it?

An Availability Zone is a physically separate data center within an Azure region, equipped with its own power, cooling, and networking infrastructure. Azure regions typically contain multiple availability zones to provide redundancy and fault isolation. When you deploy a Virtual Machine, you can choose the availability zone in which it will run. This ensures that workloads are distributed across independent data centers within the same region. Availability Zones are designed to provide high availability for critical applications.

### Why do we use it?

Availability Zones are used to protect applications from data center failures and planned maintenance events. They improve application uptime by ensuring that if one zone becomes unavailable, resources deployed in other zones continue to operate. This helps organizations build highly available and fault-tolerant cloud solutions.

### Types of Availability Zones
* **Zone 1**
  * Deploys the Virtual Machine in the first physically isolated data center within the selected Azure region.
  * Used to host workloads independently or as part of a multi-zone deployment for high availability.
* **Zone 2**
  * Deploys the Virtual Machine in the second physically isolated data center.
  * Commonly used to distribute applications across multiple zones, ensuring continuity if another zone fails.
* **Zone 3**
  * Deploys the Virtual Machine in the third physically isolated data center.
  * Provides additional redundancy and is typically used with Zones 1 and 2 for mission-critical applications.

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


## OS Disk

<img width="1025" height="280" alt="image" src="https://github.com/user-attachments/assets/dd9cb906-fda0-41b1-aea7-7df53b66fe10" />

### What is it?

The Operating System (OS) Disk is the primary storage disk attached to a Virtual Machine that contains the operating system, boot files, and system applications required to start and run the VM. During VM creation, you can configure the OS disk size, disk type, key management, and whether the disk should be deleted along with the VM. Azure also provides options such as Premium SSD, Standard SSD, and Standard HDD to meet different performance and cost requirements. Proper OS disk configuration ensures optimal performance, security, and storage management.

### Why do we use it?

The OS Disk stores all files required for the operating system to function and boot successfully. Configuring the appropriate disk size and type improves VM performance, while features like encryption and key management enhance data security. Additional settings such as Delete with VM and Ultra Disk Compatibility provide better storage lifecycle management and flexibility based on workload requirements.

### OS Disk Settings
* **OS Disk Size**
  * OS Disk Size specifies the amount of storage allocated to the operating system disk of the Virtual Machine. It determines how much space is available for the operating system, system files, updates, and installed applications. The size can be increased later if additional storage is required.
* **OS Disk Type**
  * OS Disk Type defines the storage performance and redundancy of the operating system disk. Azure offers options such as Standard HDD, Standard SSD, Premium SSD, Premium SSD v2, and Ultra Disk (for supported workloads), allowing users to choose the best balance between performance and cost.
* **Delete with VM**
  * Delete with VM determines whether the operating system disk is automatically deleted when the Virtual Machine is removed. Enabling this option helps avoid unused storage resources and unnecessary storage costs. If disabled, the disk remains available for backup or future use.
* **Key Management**
  * Key Management controls how the OS disk is encrypted to protect the data stored on it. Azure supports Platform-managed keys, where Microsoft manages encryption automatically, and Customer-managed keys, where organizations control their own encryption keys for enhanced security and compliance.
* **Enable Ultra Disk Compatibility**
  * Enable Ultra Disk Compatibility allows the Virtual Machine to attach Azure Ultra Disks, which provide very high IOPS, low latency, and configurable throughput. This option is typically enabled for performance-intensive applications such as large databases, SAP HANA, and enterprise workloads requiring high-speed storage.


# Network interface

## Virtual Network

<img width="1002" height="70" alt="image" src="https://github.com/user-attachments/assets/399ded03-3b9a-4da4-8a0b-07df96ad9b76" />

### What is it?

A Virtual Network (VNet) is a logically isolated network in Azure that enables Azure resources, such as Virtual Machines, Storage Accounts, and Databases, to communicate securely with each other. It functions similarly to a traditional on-premises network but is hosted in the Azure cloud. A VNet can be divided into multiple subnets to organize and manage network traffic efficiently.

### Why do we use it?

A Virtual Network provides secure communication between Azure resources and allows controlled access to the internet, on-premises networks, and other Azure services. It also enables network isolation, improves security, and supports services such as Network Security Groups (NSGs), VPN Gateway, and Azure Load Balancer for efficient network management.


## Subnet
<img width="952" height="42" alt="image" src="https://github.com/user-attachments/assets/8d6b2af0-1b8f-483d-b699-835e1dd22f9e" />

### What is it?

A Subnet is a smaller network created within an Azure Virtual Network (VNet). It divides the VNet into multiple logical sections, allowing resources such as Virtual Machines, databases, and application servers to be grouped based on their function. Each subnet is assigned a specific range of IP addresses (CIDR block), such as 10.0.0.0/24.

### Why do we use it?

Subnets help organize and isolate network resources, making the network more secure and easier to manage. They enable administrators to apply different security rules, route traffic efficiently, and separate workloads such as web servers, application servers, and databases within the same Virtual Network.

## NIC Network Security Group (NSG)
<img width="496" height="117" alt="image" src="https://github.com/user-attachments/assets/a66b89ae-b9f1-49a7-a253-de64fe7518c7" />
### What is it?

A Network Security Group (NSG) is a security feature in Azure that controls inbound and outbound network traffic for a Virtual Machine's Network Interface Card (NIC). It acts as a virtual firewall by allowing or denying traffic based on defined security rules. During VM creation, Azure provides three NSG options: None, Basic, and Advanced.

### Why do we use it?

An NSG is used to protect Virtual Machines from unauthorized network access by controlling which traffic is allowed or blocked. It helps secure Azure resources, restrict unnecessary ports, and improve the overall network security of the environment.

### NSG Options
* **None** 
  * No Network Security Group is associated with the VM's network interface.
  * The VM is not protected by NSG rules unless one is attached later.
* **Basic**
  * Azure creates a new NSG with default inbound and outbound security rules.
  * Suitable for most deployments and allows basic configuration during VM creation.
* **Advanced**
  * Allows you to select an existing NSG or create a custom one.
  * Recommended when you need specific security rules for production or enterprise environments.

## Public Inbound Ports

<img width="561" height="87" alt="image" src="https://github.com/user-attachments/assets/a1bf7ba2-5af2-49d9-ac94-762ecd5e56de" />

### What is it?

Public Inbound Ports determine whether the Virtual Machine can receive incoming network traffic from the internet. Azure allows you to either block all public inbound connections (None) or allow traffic through selected ports (Allow selected ports). These ports are protected and managed using Network Security Group (NSG) rules.

### Why do we use it?

Public Inbound Ports are used to provide remote access and allow external users or applications to connect to the Virtual Machine. Only the required ports should be opened to minimize security risks and protect the VM from unauthorized access.

### Public Inbound Port Options
* **None**
  * Blocks all inbound traffic from the internet.
  * Recommended for VMs that do not require direct public access or are accessed through VPN, Bastion, or private networks.
* **Allow Selected Ports**
  * Allows inbound traffic only through the ports selected during VM creation.
  * Common examples include SSH (Port 22) for Linux VMs and RDP (Port 3389) for Windows VMs. It provides controlled access while maintaining network security.

## Inbound Ports

<img width="1002" height="52" alt="image" src="https://github.com/user-attachments/assets/f137b753-9bcb-4c74-a4f7-27fa1be55d24" />


### What is it?

Select Inbound Ports allows you to choose which network ports should be open for incoming traffic to the Virtual Machine. These ports enable specific services, such as remote access or web hosting, to communicate with external users. Azure automatically creates the required Network Security Group (NSG) rules for the selected ports.

### Why do we use it?

Selecting the appropriate inbound ports ensures that only the required services are accessible from the internet. This improves security by limiting unnecessary network access while allowing users to connect to the Virtual Machine for administration or application access.

### Common Inbound Ports
* **SSH (22)**
  * Used for secure remote access to Linux Virtual Machines.
  * Allows administrators to manage the VM using SSH clients such as OpenSSH or PuTTY.
* **HTTP (80)**
  * Used to host and access websites over an unencrypted connection.
  * Suitable for basic web applications and websites.
* **HTTPS (443)**
  * Used to host websites over a secure, encrypted connection using SSL/TLS.
  * Recommended for production websites and web applications.
*  **RDP (3389)**
   * Used for remote desktop access to Windows Virtual Machines.
   * Allows administrators to manage Windows VMs through the Remote Desktop Protocol (RDP).


 ## Boot Diagnostics

  <img width="927" height="140" alt="image" src="https://github.com/user-attachments/assets/4e5782e2-41b0-4406-8eb9-44df59fa2001" />

### What is it?

Boot Diagnostics is an Azure monitoring feature that captures boot logs and screenshots of a Virtual Machine during the startup process. It helps administrators diagnose boot failures, operating system errors, and startup issues. Azure allows you to store these diagnostic logs in either a managed storage account or a custom storage account, or you can disable the feature if it is not required.

### Why do we use it?

Boot Diagnostics is used to troubleshoot Virtual Machine startup problems when a VM fails to boot or becomes unresponsive. It provides valuable diagnostic information that helps administrators quickly identify and resolve issues, reducing downtime and improving VM availability.

### Boot Diagnostics Options
* Enable with Managed Storage Account (Recommended)
  * Azure automatically creates and manages the storage account used for boot diagnostics.
  * Simplifies configuration and is the recommended option for most deployments.
* Enable with Custom Storage Account
  * Allows you to store boot diagnostics data in an existing Azure Storage Account.
  * Useful when you want more control over storage location, access, or compliance requirements.
* Disable
  * Turns off Boot Diagnostics and no boot logs or screenshots are collected.
  * Suitable only when diagnostic information is not required.
 


After That Just Do Review+Create 

<img width="792" height="640" alt="image" src="https://github.com/user-attachments/assets/7cc32f6a-c18c-431e-a9fe-8df0998e4766" />

<img width="732" height="537" alt="image" src="https://github.com/user-attachments/assets/a583e4bc-7671-4e99-8352-2c103ae77804" />
<img width="1813" height="502" alt="image" src="https://github.com/user-attachments/assets/c591735a-c09c-42e0-b31c-4fb9e44a4320" />


# VM is created





