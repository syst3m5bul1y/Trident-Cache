# Project Trident Cache Overview

### NAME: PROJECT TRIDENT CACHE

### BRIEF DESCRIPTION:

Setting up a Network Attached Storage (NAS) system using Raspberry Pi 4 Model B and a 2.5 SATA 3 SSD.

### SYSTEM TYPE:

NETWORK ATTACHED STORAGE (NAS)

### PRIMARY FUNCTION

To provide centralized and secure file storage and sharing capabilities on the host network.

### PURPOSE & GOALS

*created on 26/11/2023*

#### Primary Goals:

1. **File Storage and Sharing**: Establish a reliable and efficient NAS system within the host network for storing and sharing files.

2. **Network Integration**: Seamlessly integrate the NAS into the host network (192.168.1.0/24), ensuring compatibility and optimal performance.

#### Secondary Goals:

1. **Research and Development**: To explore and test new storage technologies, staying up-to-date with current trends and advancements in the field.

2. **Documentation and Reporting Skills**: To enhance skills in documenting technical processes and creating comprehensive reports, an essential skill in cybersecurity and network engineering professions.


### HIGH LEVEL ARCHITECTURE

*created on 26/11/2023*

#### Components:

- **Raspberry Pi 4 Model B (8GB)**: Acts as the brain of the NAS, running the NAS operating system and managing storage and network communications.

- **2.5 SATA 3 SSD (240GB)**: Serves as the primary storage medium for the NAS, holding all shared files and data.

- **USB to SATA 3 Converter**: Facilitates the connection between the Raspberry Pi and the SSD, ensuring high-speed data transfer.


#### Operating System & Software

![[Trident Cache Schematic.drawio.png]]


- **OpenMediaVault (OMV)**: Chosen for its ease of use, flexibility, and strong community support. It will manage file sharing, user accounts, security settings, and other NAS services.

- **Additional Software**:

	- Network services like SMB/CIFS, NFS for file sharing.
	
	- Security tools for firewall management, SSH, VPN, and other security measures.
	
	- Monitoring tools for real-time system monitoring and performance analysis.

Full set of services: [[Project Trident Cache - LoS]]
#### Network Integration

![[Pasted image 20231128195042.png]]

- **Host Network**: The NAS is integrated into the host network with the IP range 192.168.1.0/24.

- **Connection**: Wired Ethernet connection to ensure stability and high data transfer speeds.

- **Network Role**: The NAS will be accessible to all /selected (TBD) devices on the host network, providing a centralized storage solution.


#### Security Architecture

- **Firewall and Network Security**: Implemented at the network level to protect the NAS from unauthorized access.

- **Data Security**: Encompasses encryption, user authentication, and access controls to safeguard stored data.

- **Backup and Redundancy**: Strategies to ensure data integrity and availability.


### Key Components

#### Hardware Components

1. Raspberry Pi 4 Model B (8GB RAM)**:

	- Function: Serves as the central processing unit of the NAS system.
	- Features: High-performance CPU, ample RAM for multitasking, and USB 3.0 ports for high-speed data transfer.

2. **2.5 SATA 3 SSD (240GB)**:

	- Function: Acts as the primary storage medium for the NAS.
	- Features: Offers quick data access speeds, reliability, and sufficient storage capacity for file sharing and media streaming.

3. **USB to SATA 3 Converter**:

	- Function: Connects the SSD to the Raspberry Pi.
	- Features: Ensures compatibility and maximizes data transfer rates between the Raspberry Pi and the SSD.

4. **Network Interface (Ethernet Port on Raspberry Pi)**:

	- Function: Provides network connectivity to integrate the NAS with the home network.
	- Features: Gigabit Ethernet for fast network communication.

5. **Power Supply Unit**:

	- Function: Powers the Raspberry Pi.
	- Features: Stable and reliable power source to ensure uninterrupted NAS operation.


#### Software Components 

1. **OpenMediaVault**:

	- Function: Operating system specifically designed for NAS.
	- Features: User-friendly web interface, plug-in support, and comprehensive file-sharing and security features.

2. **File Sharing Services**:

	- **Samba (SMB/CIFS)**: For Windows network file sharing.
	- **NFS**: For Unix/Linux network file sharing.
	- **OpenSSH's SFTP**: For secure file transfers.

3. **Media Server**:

	- **Subsonic**: For music streaming within the network.

4. **Security and Firewall**:

	- **iptables**: Network firewall for security.
	- **Fail2Ban**: Protection against brute-force attacks.
	- **OpenVPN**: Secure VPN access to the NAS.
	- **SELinux**: Access control and policy enforcement.

5. **Monitoring and Management**:

	- **Cockpit**: For web-based system administration.
	- **Grafana**: For advanced system monitoring and analytics.

6. **Logging and Analysis**:

	- **Syslog**: System logging.
	- **Logwatch**: Log analysis and reporting.

7. **Scheduled Task Management**:

	- **Cron**: For automating system tasks and maintenance.
