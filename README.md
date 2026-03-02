# Microsfot Sentinel Honeypot SOC Lab

## Objective
The objective of this project was to deploy a vulnerable Windows virtual machine in Microsoft Azure, foward security logs using Azure Monitor Agent, and analyze real world attack activity using the Microsoft Sentinel SIEM.

## Skills Demonstrated:

• Azure cloud infrastructure deployment

• Virtual network configuration

• Network Security Group configuration

• Azure Monitor Agent configuration

• Log Analytics Workspace integration

• Microsoft Sentinel SIEM deployment

• Security event log analysis

• Threat detection using KQL queries

• Incident investigation fundamentals


## Tools Used:

• Microsoft Azure

• Microsoft Sentinel

• Azure Monitor Agent

• Log Analytics Workspace

• Windows Event Viewer

• Remote Desktop Protocol (RDP)

• Kusto Query Language (KQL)


## Architecture Overview
Windows VM -> Azure Monitor Agent -> Log Analytics Workspace -> Microsoft Sentinel -> Threat Detection

## Deployment Steps
1. Created Resource Group
2. Created Virtual Network
3. Deployed Windows Virtual Machine
4. Configured Network Security Group
5. Installed Azure Monitor Agent
6. Connected Log Analytics Workspace
7. Enabled Microsoft Sentinel
8. Observed attack activity

## Evidence
### This screenshot shows the Microsoft Azure Portal, which serves as the cloud management interface. This portal allows administrators to deploy and manage cloud infrastructure such as virtual machines, networks, and security resources.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/9f16d4391cf8830bae94308c51fd57330601a18d/Azure%20Portal%20Home.jpg)

### This screenshot shows the creation of a Resource Group, which is a logical container that holds related Azure resources. Resource groups allow administrators to organize and manage infrastructure components efficiently.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/Resource%20Group%20Created.jpg)

### This screenshot shows the Virtual Network configuration. Virtual networks allow cloud resources to communicate securely with each other and simulate enterprise network environments.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/Virtual%20Network%20Created.jpg)

### These screenshots show the successful deployment of a Windows virtual machine. This virtual machine serves as the honeypot target that attackers attempt to access.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/4_Created%20VM.jpg)
![image alt](https://github.com/Medina703/Sentinel-Lab/blob/6679d9caf8924528f3b727bf089d67aa7a492680/4_VM%20Proof.jpg)

### This screenshot shows the Network Security Group configured to allow all inbound traffic. This intentionally vulnerable configuration allows attackers to discover and attempt to access the system, simulating a real-world attack target.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/5_Network%20Security%20Group%20Showing%20Open%20Access.jpg)

### This screenshot shows successful Remote Desktop access to the virtual machine using its public IP address. This confirms the system is externally accessible.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/6_Remote%20Desktop%20Connection%20to%20VM.jpg)

### This screenshot shows failed login attempts recorded in Windows Event Viewer. Event ID 4625 indicates failed authentication attempts, which are commonly associated with brute-force attacks.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/7_Event%20Viewer%20showing%20failed%20login%20attempts%20Event%20ID_4625.jpg)

### This screenshot shows the Log Analytics Workspace, which collects and stores security logs from the virtual machine.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/8_Log%20Analystics%20Workspace%20Created.jpg)

### This screenshot shows Microsoft Sentinel connected to the Log Analytics Workspace. Sentinel serves as a SIEM platform that enables threat detection and analysis.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/9_Microsoft%20Sentinel%20Connected.jpg)

### This screenshot shows security logs successfully ingested into Log Analytics Workspace. This confirms that Azure Monitor Agent is forwarding logs correctly.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/10_Logs%20appearing%20in%20Log%20Analytics.jpg)

### This screenshot shows a global attack map visualizing real-world attack sources. This demonstrates continuous automated attack attempts from multiple geographic locations, with mine showing that most attacks are coming from Poland.

![image alt](https://github.com/Medina703/Sentinel-Lab/blob/e9010e71e470584327256349a23c6a9606f2592f/11_Windows%2011%20Attack%20Map%20VM%20Real%20Attackers.jpg)
