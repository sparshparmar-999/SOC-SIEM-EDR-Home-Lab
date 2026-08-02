# EDR-SOC-SIEM Home Lab: LimaCharlie & Wazuh Integration

This project demonstrates the deployment, configuration, and monitoring of an enterprise-grade security stack. It showcases the integration of **LimaCharlie (EDR)** and **Wazuh (SIEM)** to detect, analyze, and visualize security events—specifically targeting unauthorized privilege escalation attempts.

---

## 🚀 Deployment & Architecture

### 1. LimaCharlie EDR Setup
A cloud-native Endpoint Detection and Response (EDR) environment was established to provide continuous monitoring and behavioral analysis.

*Insert your screenshot showing the newly created organization below:*
![LimaCharlie New Organization Created](<img width="1598" height="862" alt="wazuh new organization" src="https://github.com/user-attachments/assets/a02e081c-83c9-4b0c-bf17-3026f4b8ae83" />
)

### 2. Wazuh Cross-Platform Agent Deployment
The Wazuh agent was deployed alongside LimaCharlie to ensure telemetry co-existence and unified log collection.

*Insert your screenshot showing the agent running under LimaCharlie monitoring:*
![Wazuh Agent Working on LimaCharlie](<img width="1600" height="820" alt="wazuh-agent first machine live feed" src="https://github.com/user-attachments/assets/51d3f75a-8674-4f06-a485-f86418e89bd8" />
)

---

## 📊 Security Operations Center (SOC) Dashboard

### 1. Wazuh Manager Overview
The centralized Wazuh Manager dashboard provides real-time visibility into the health of the infrastructure, agent connectivity, and security posture alerts.

*Insert your screenshot of the main manager overview:*
![Wazuh Manager Dashboard](<img width="1593" height="829" alt="wazuh-manager dashboard" src="https://github.com/user-attachments/assets/d3091c8f-20ea-4bbd-8091-57882ee32ae5" />
)

### 2. Active Endpoint Verification
Confirmation of the active telemetry pipeline, proving that the endpoint is successfully checking in and streaming system events.

*Insert your screenshot showing the active agent status:*
![Agent Working in Wazuh Manager](<img width="1600" height="834" alt="redhatagent-01 active" src="https://github.com/user-attachments/assets/bafcb4d7-4baf-4553-aa79-cfe536a1fa88" />
)

---

## 🏹 Threat Hunting & Incident Detection

### 1. High-Severity Alert: Unauthorized Sudo Attempt (Rule Level 10)
During active monitoring, a **Rule Level 10 (High Severity)** alert was triggered, catching a failed attempt by a non-privileged user to execute commands via `sudo`.

*Insert your screenshot of the specific rule alert:*
![Alert of Failed Sudo Attempt Rule Level 10](<img width="1600" height="829" alt="threat hunting alert" src="https://github.com/user-attachments/assets/3a43257a-4168-4fe8-bc4d-90376b888b64" />
)

---

## 🔍 Deep-Dive Alert Analysis

### 1. Structured Document Details
A granular look into the JSON metadata of the alert payload parsed into a readable table structure. This highlights critical fields like `syscheck`, user context, and command targets.

*Insert your screenshot of the structured data table:*
![Document Details of Alert Table Section](<img width="799" height="764" alt="detail of wazuh-manager" src="https://github.com/user-attachments/assets/0f39759c-3694-487d-85ef-8ae5e9d7815c" />
)

### 2. Alert Lifecycle Tree-View
The attack chain mapped out visually. This hierarchical tree-view shows the parent-child process relationship, demonstrating exactly how the unauthorized command was spawned.

*Insert your screenshot of the execution tree-view:*
![Alert Tree View](<img width="1347" height="383" alt="tree-view" src="https://github.com/user-attachments/assets/1c08b388-f43b-4211-a777-f8977852a17b" />
<img width="1344" height="354" alt="limacharlie-process-tree" src="https://github.com/user-attachments/assets/00e0f71b-8eae-435f-87e0-167b373623c0" />)
