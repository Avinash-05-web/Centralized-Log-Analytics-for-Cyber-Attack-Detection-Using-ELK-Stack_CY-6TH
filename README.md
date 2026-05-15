🚨 Quantarix Labs SIEM Project

🛡️ Implementation of Centralized Log Analytics for Multi-Vector Cyber Attack Detection Using ELK Stack

«🔍 A complete Security Information and Event Management (SIEM) solution built using the ELK Stack, Docker, and a vulnerable Node.js application to simulate and detect real-world cyber attacks.»

---

📌 Project Overview

This project demonstrates how organizations can centralize application logs, detect cyber attacks in real time, and visualize security events using open-source technologies.

A vulnerable web application was developed using Node.js and Express.js, deployed in Docker, and attacked using brute-force login attempts, SQL Injection, and successful authentication. Logs were collected by Filebeat, processed by Logstash, stored in Elasticsearch, and visualized in Kibana through custom dashboards and detection rules.

---

🎯 Objectives

- 🧱 Develop a vulnerable web application for attack simulation
- 📄 Generate security logs for multiple attack vectors
- 🚚 Collect logs using Filebeat
- 🔄 Process logs using Logstash
- 🗄️ Store events in Elasticsearch
- 📊 Visualize attack activity in Kibana
- 🚨 Create detection rules and alerts
- 🧠 Map attacks to MITRE ATT&CK
- 🔗 Map attack stages to the Cyber Kill Chain

---

🏗️ System Architecture

Attacker Machine (Kali Linux / PowerShell)
                │
                ▼
      Malicious HTTP Requests
                │
                ▼
 Vulnerable Web Application (Node.js + Express)
                │
                ▼
          app.log File
                │
                ▼
            Filebeat
                │
                ▼
            Logstash
                │
                ▼
         Elasticsearch
                │
                ▼
     Kibana Dashboards & Alerts

---

🌐 Network Ports Used

Port| Service| Description
3000| 🌍 Web Application| Vulnerable Node.js application
5044| 📥 Logstash| Beats input for Filebeat
9200| 🗄️ Elasticsearch| Log storage and indexing
5601| 📊 Kibana| Dashboards and analysis

---

🧰 Technologies Used

- 🐳 Docker & Docker Compose
- 🟢 Node.js & Express.js
- 📦 Filebeat 7.17.0
- 🔄 Logstash 7.17.0
- 🔍 Elasticsearch 7.17.0
- 📈 Kibana 7.17.0
- 🖥️ PowerShell / Git Bash / Kali Linux
- 🪟 Windows 11

---

⚔️ Simulated Attacks

🔐 Brute Force Attack

Repeated login attempts using invalid passwords.

💉 SQL Injection

Payload used:

' OR 1=1

✅ Successful Login

Valid credentials:

Username: admin
Password: admin123

🚫 Unauthorized Access

Attempt to access restricted resources without authorization.

---

📄 Sample Log Events

LOGIN ATTEMPT: admin - wrong15
Invalid credentials
LOGIN SUCCESSFUL: admin
SEARCH QUERY: ' OR 1=1

---

📊 Kibana Dashboard Features

- 📈 Total log records
- 🔐 Brute-force attack count
- 💉 SQL Injection count
- ✅ Successful login count
- 🕒 Timeline of attack activity
- 🚨 Security alerts

---

🚨 Detection Rules

Rule Name| Detection Logic| Severity
🔐 Brute Force Detection| Multiple "Invalid credentials" events| High
💉 SQL Injection Detection| Query contains "OR 1=1"| Critical
✅ Successful Login Detection| Message contains "Login successful"| Medium
🚫 Unauthorized Access Detection| Restricted resource access attempt| High

---

🧠 MITRE ATT&CK Mapping

Attack| Technique ID| Technique Name| Tactic
🔐 Brute Force| T1110| Brute Force| Credential Access
💉 SQL Injection| T1190| Exploit Public-Facing Application| Initial Access
✅ Successful Login| T1078| Valid Accounts| Persistence
🚫 Unauthorized Access| T1078| Valid Accounts| Privilege Escalation

---

🔗 Cyber Kill Chain Mapping

1. 🕵️ Reconnaissance
2. 🛠️ Weaponization
3. 📤 Delivery
4. 💥 Exploitation
5. 📥 Installation
6. 📡 Command and Control (optional)
7. 🎯 Actions on Objectives

---

📈 Project Results

- 📄 296+ log events ingested
- 🔐 132 brute-force attempts detected
- 💉 10 SQL Injection attempts identified
- ✅ Successful login events captured
- 📊 Interactive dashboards operational
- 🚨 Real-time alerting enabled

---

📂 Project Structure

quantarix-labs-project/
├── app/
│   ├── app.js
│   ├── package.json
│   └── Dockerfile
├── filebeat/
│   └── filebeat.yml
├── logstash/
│   └── logstash.conf
├── logs/
│   └── app.log
├── docker-compose.yml
└── README.md

---

▶️ How to Run

1️⃣ Clone the Repository

git clone <your-repository-url>
cd quantarix-labs-project

2️⃣ Start the Project

docker compose up -d

3️⃣ Open the Services

- 🌍 Web App: "http://localhost:3000"
- 📊 Kibana: "http://localhost:5601"

---

🧪 Attack Simulation Commands

🔐 Brute Force

curl -X POST http://localhost:3000/login -d "username=admin&password=wrong1"

✅ Successful Login

curl -X POST http://localhost:3000/login -d "username=admin&password=admin123"

💉 SQL Injection

curl "http://localhost:3000/search?q=' OR 1=1"

---

📘 Academic Significance

This project demonstrates practical knowledge of:

- 🛡️ Security Information and Event Management (SIEM)
- 📈 Log analytics and threat detection
- 🐳 Containerized deployment
- 🔍 Threat intelligence mapping
- 🚨 Alerting and incident monitoring

---

🚀 Future Enhancements

- 📧 Email and Slack notifications
- 🌐 Suricata or Zeek integration
- 🤖 Machine learning anomaly detection
- 🔐 TLS and Role-Based Access Control (RBAC)
- ☁️ Cloud deployment (AWS/Azure)

---

👨‍🎓 Author

Avinash Das Manikpuri
🎓 B.Tech CSE (Cyber Security)
🏫 Quantarix Labs Project
🆔 ERP: 6604666

---

📜 License

This project is intended for educational and research purposes only.

---

⭐ Acknowledgments

- Elastic Stack (ELK)
- Docker
- MITRE ATT&CK Framework
- Lockheed Martin Cyber Kill Chain

---

«🛡️ “Centralized logging transforms raw application events into actionable security intelligence.”»
