# Azure-Sentinel-SOC-Lab
A Cloud-Native SOC with Automated Incident Response (SIEM/SOAR).
# 🛡️ Cloud-Native SOC & Automation Lab
An end-to-end Security Operations Center (SOC) project using **Microsoft Sentinel** (SIEM) and **Azure Logic Apps** (SOAR).

## 🚀 Project Overview
In this project, I built a live SOC environment in Azure to detect and automatically respond to security threats.

### 🛠️ Technologies Used
- **Azure Sentinel (SIEM)**
- **Azure Logic Apps (SOAR)**
- **Microsoft Defender for Cloud**
- **Kusto Query Language (KQL)**
- **Windows Server 2022 (Victim VM)**

## 📈 Architecture Diagram
1. **Detection:** VM -> Azure Monitor Agent -> Log Analytics -> Sentinel.
2. **Automation:** Sentinel Trigger -> Logic App -> RBAC/Managed Identity -> Auto-Triage -> Email Alert.

## 🕵️ Attack Simulations
- **RDP Brute Force:** Simulated external attacks using incorrect login attempts.
- **Defense Evasion:** Cleared Windows Security Logs (`Event ID 1102`) to test stealth detection.
- **Honeytoken Trap:** Monitored unauthorized access to a "decoy" sensitive file.

## 🔧 Troubleshooting (The "Real World" Experience)
One of the key challenges was resolving **400 BadRequest** errors in the SOAR pipeline. I resolved this by:
- Configuring **System-Assigned Managed Identities**.
- Granting **Microsoft Sentinel Responder** roles via Azure IAM.
- Using **KQL** to retrieve raw **ARM IDs** when dynamic content failed.<img width="1825" height="757" alt="Sentinel_KQL" src="https://github.com/user-attachments/assets/70f55035-ab41-4b13-9bca-afa7376bde73" />
<img width="1726" height="870" alt="Incident_2" src="https://github.com/user-attachments/assets/503af9c5-c168-463a-b0a4-8c44c83404e8" />
<img width="1432" height="740" alt="ATTACK_1" src="https://github.com/user-attachments/assets/d61f0e6e-3840-4b1b-aea9-9e6810393485" />
<img width="1809" height="821" alt="Analytics_rules" src="https://github.com/user-attachments/assets/1f461bab-b93a-4e99-aac0-7b97d8c03302" />
<img width="1910" height="865" alt="LogicApp_Success " src="https://github.com/user-attachments/assets/d61e330d-562c-4a23-98f7-b8421f6b8dab" />
<img width="1847" height="863" alt="Incidents" src="https://github.com/user-attachments/assets/905e0b39-75d1-4179-9736-905570cba316" />
<img width="1658" height="883" alt="SOCLAB1" src="https://github.com/user-attachments/assets/856f457e-7339-454d-bd0d-599d020da537" />
