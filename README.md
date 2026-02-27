## ISOLAX – AI-Based Endpoint Isolation and Remote Security Monitoring System
A lightweight and secure endpoint monitoring solution that combines real-time screen viewing, process inspection, remote command execution, AI-based threat detection, automated alerting, and intelligent endpoint isolation to support SOC analysts in faster and more effective incident response.

## About
<!--Detailed Description about the project-->
ISOLAX is a cloud-driven endpoint isolation and monitoring platform built to enhance cybersecurity incident handling. Traditional SOC workflows require multiple tools for remote investigation, isolation, and forensic data retrieval, which often results in delays and operational complexity.

This project introduces a lightweight Go-based endpoint agent and a centralized web dashboard, enabling analysts to remotely view live screens, browse file systems, execute shell commands, inspect processes, and instantly isolate compromised endpoints through automated OS-native firewall controls.

By using encrypted polling-based communication, ISOLAX works reliably across NAT networks, restrictive firewalls, and diverse operating environments—making it suitable for enterprise SOC teams, cybersecurity labs, and remote forensic investigations.

## Features
<!--List the features of the project as shown below-->
- Lightweight, cross-platform endpoint agent built in Go.

- Real-time screen streaming using JPEG frame compression.

- Remote shell execution with command output retrieval.

- File browser with directory and metadata listing.

- Process viewer with support for remote termination.

- One-click isolation using Windows Netsh and Linux iptables.

- Secure encrypted communication between server and endpoints.

- Multi-endpoint dashboard for SOC-style monitoring.

- Immutable audit logging for investigation and compliance.

## AI Detection and Alerts

Automatically analyzes running processes when an AI scan is triggered.

Detects malicious or suspicious behavior using AI-based threat evaluation.

Generates real-time security alerts upon detection.

Displays detailed alert information including severity level, file path, process ID, and threat summary.

Updates the Security Inbox instantly for SOC analyst review.

Enables rapid threat assessment and decision-making.

Supports direct action such as process termination or endpoint isolation from the alert panel.

<img width="651" height="273" alt="image" src="https://github.com/user-attachments/assets/ed578590-35d1-4f60-bb83-5b859d24cf27" />

## AI Auto Isolation

Automatically isolates endpoints when the AI engine classifies a process as malicious with high confidence.

Triggers firewall-based isolation rules (Windows netsh / Linux iptables) without manual SOC intervention.

Maintains a secure control channel with the ISOLAX server during isolation.

Updates the Security Dashboard in real time, marking the device status as “Isolated.”

Blocks inbound and outbound traffic to prevent lateral movement.

Preserves full monitoring visibility for further forensic investigation.

Reduces response time and minimizes potential damage during active attacks.

<img width="654" height="315" alt="image" src="https://github.com/user-attachments/assets/f5533963-9dd2-49ef-bf92-1831f1dadb24" />


## Requirements
<!--List the requirements of the project as shown below-->
#### Server Requirements:

Operating System: Linux (Ubuntu 20.04 or later recommended)

Runtime: Go 1.18+

Backend Hosting: AWS EC2 / Local Linux server

Firewall: Allow inbound HTTPS for dashboard and client polling

Database: MongoDB Atlas or local MongoDB instance

Reverse Proxy (optional): Nginx for SSL termination

#### Client (Endpoint Agent) Requirements:

Supported OS: Windows 10+, Windows Server, Ubuntu 18+, Kali Linux

Runtime: Go executable (no installation needed)

Permissions: Requires admin/root privileges for isolation operations

Screen Capture Libraries: OS-native screen APIs



#### Frontend Requirements:

Frameworks: HTML, CSS, JavaScript, Bootstrap

Browser Compatibility: Chrome, Edge, Firefox

#### Development Tools:

Version Control: Git + GitHub

IDE: VSCode or GoLand

Dependencies:

Go net/http

Go os/exec

encoding/json

WebSocket/HTTP for streaming frames

## System Architecture
<!--Embed the system architecture diagram as shown below-->

<img width="857" height="400" alt="image" src="https://github.com/user-attachments/assets/8f7fe4c7-ab64-497e-90a0-9bd791ff38f7" />



## Output

<!--Embed the Output picture at respective places as shown below as shown below-->
#### Output1 - Live Screen Monitoring Dashboard

<img width="1027" height="474" alt="image" src="https://github.com/user-attachments/assets/a8521440-ec68-4fba-b26b-cdf49366a96e" />

#### Output2 - Network Isolation Interface
<img width="1027" height="474" alt="image" src="https://github.com/user-attachments/assets/a65c3b43-ea24-4131-9162-a8727be5e2a0" />

System Stability: 99.2%
Isolation Success Rate: 98.5%
Screen Streaming Reliability: 97.8%

Note: These performance values are sample metrics and can be adjusted based on real-world testing, endpoint conditions, and network environments.

## Results and Impact
<!--Give the results and impact as shown below-->
ISOLAX enhances cybersecurity operations by enabling SOC analysts to remotely observe, analyze, and contain potential threats in real time. Its lightweight agent design and secure cloud architecture allow for rapid deployment across diverse systems without requiring heavy EDR infrastructure.

The system significantly reduces incident response time by centralizing screen access, process control, command execution, and network isolation within a unified interface. Its forensic logging and multi-endpoint support make it suitable for cybersecurity training, enterprise SOC workflows, and remote digital investigations.

This project serves as a foundation for further innovation in endpoint security, enabling future integration with AI-based threat detection, automated remediation playbooks, and advanced behavioral analytics.

## Articles published / References
1. Arfeen, A., Ahmed, S., Khan, M.A. and Jafri, S.F.A., 2021, November. Endpoint detection & response: A malware identification solution. In 2021 International Conference on Cyber Warfare and Security (ICCWS) (pp. 1–8). IEEE.

2. Cappello, M., 2024. A comprehensive analysis of EDR (Endpoint Detection & Response), EPP (Endpoint Protection Platform), and antivirus security technologies (Master's thesis, Πανεπιστήμιο Πειραιώς).

3. Del Piccolo, V., Amamou, A., Haddadou, K. and Pujolle, G., 2016. A survey of network isolation solutions for multi-tenant data centers. IEEE Communications Surveys & Tutorials, 18(4), pp.2787–2821.

4. Fernandes, N.C., Moreira, M.D., Moraes, I.M., Ferraz, L.H.G., Couto, R.S., Carvalho, H.E., Campista, M.E.M., Costa, L.H.M. and Duarte, O.C.M., 2011. Virtual networks: Isolation, performance, and trends. Annals of Telecommunications, 66(5), pp.339–355.

5. Kaur, H., SL, D.S., Paul, T., Thakur, R.K., Reddy, K.V.K., Mahato, J. and Naveen, K., 2024. Evolution of endpoint detection and response (EDR) in cybersecurity: A comprehensive review. In E3S Web of Conferences (Vol. 556, p. 01006). EDP Sciences.

6. Nugraha, I.P.E.D., 2021. A review on the role of modern SOC in cybersecurity operations. Int. J. Current Sci. Res. Rev, 4(5), pp.408–414.

7. Park, S.H., Yun, S.W., Jeon, S.E., Park, N.E., Shim, H.Y., Lee, Y.R., Lee, S.J., Park, T.R., Shin, N.Y., Kang, M.J. and Lee, I.G., 2022. Performance evaluation of open-source endpoint detection and response combining Google Rapid Response and OSquery for threat detection. IEEE Access, 10, pp.20259–20269.

8. Siji, F.G. and Uche, O.P., 2023. An improved model for comparing different endpoint detection and response tools for mitigating insider threat. Indian J. Eng, 20(53), pp.1–13.

9. Wittig, A. and Wittig, M., 2023. Amazon Web Services in Action: An in-depth guide to AWS. Simon and Schuster.

10. Zimmerman, C., 2014. Cybersecurity Operations Center. The MITRE Corporation.




