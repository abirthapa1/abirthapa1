<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=00B4D8&center=true&vCenter=true&width=700&lines=Hey%2C+I'm+Abir+Thapa+%F0%9F%91%8B;Cybersecurity+Analyst;SOC+%7C+Incident+Response+%7C+Threat+Detection;Defender+XDR+%E2%80%A2+Sentinel+%E2%80%A2+KQL;Cloud+Security+%7C+Detection+%7C+Automation" alt="Typing SVG" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/abirthapa)
[![GitHub](https://img.shields.io/badge/GitHub-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/abirthapa1)
![CompTIA Security+](https://img.shields.io/badge/CompTIA_Security%2B-In_Progress-E31937?style=for-the-badge)

</div>

---

## 🛡️ About Me

> Cybersecurity analyst focused on **threat detection**, **incident response**, and **cloud security**. I learn by building: I run hands-on SOC labs where I simulate attacks, investigate the alerts they trigger, contain the threat, and document the whole response the way a real security team would.
>
> My cloud and DevOps background (Terraform, Kubernetes, AWS) helps me understand the infrastructure I'm defending, and I use automation to make detection and response repeatable.

- 🎯 Targeting roles in **SOC Analyst**, **Security Analyst**, and **Cloud Security**
- 🔎 Hands-on with **Microsoft Defender XDR**, **Sentinel**, **Entra ID**, and **KQL**
- 🧪 Practicing with **Atomic Red Team** and mapping findings to **MITRE ATT&CK**
- 📝 Documenting incidents in **NIST SP 800-61** format
- 📜 Currently working on **CompTIA Security+**
- 💬 Ask me about **KQL hunting**, **incident response**, **Entra ID**, or **securing cloud environments**

---

## 🔎 Featured Project: SOC-Lab

### [Incident Response with Microsoft Defender XDR, Sentinel, and Entra ID](https://github.com/abirthapa1/SOC-Lab)

A home SOC lab where I simulated a compromised-account attack and handled it end to end, from alert to recovery.

| Phase | What I did |
|:--|:--|
| **Detect** | Defender XDR raised a High-severity "hands-on-keyboard" incident after a remote logon followed by repeated PowerShell execution |
| **Investigate** | Rebuilt the attack timeline with KQL and script block telemetry: remote logon, execution-policy bypass, 49 PowerShell scripts in 10 minutes, network discovery |
| **Map** | Tagged the activity to MITRE ATT&CK (T1078.003, T1059.001, T1016) and listed indicators of compromise |
| **Contain and recover** | Isolated the endpoint, quarantined the artifact and removed the account through Live response, then re-imaged and re-onboarded the VM |
| **Learn** | Root cause: a local account sat outside Entra MFA and Identity Protection. Added detections for execution-policy bypass and remote PowerShell |

**Tools:** Defender XDR · Sentinel · Entra ID · KQL · PowerShell · Atomic Red Team · MITRE ATT&CK · NIST SP 800-61

The activity was an authorized lab simulation, and the report treats it as a real credential compromise.

### Example hunt from the project

```kql
// PowerShell started with the execution policy bypassed from a remote session
DeviceProcessEvents
| where FileName =~ "powershell.exe"
| where ProcessCommandLine has_any ("-exec bypass", "-executionpolicy bypass", "-ep bypass")
| where IsProcessRemoteSession == true
| project Timestamp, DeviceName, AccountName, ProcessCommandLine, ProcessRemoteSessionIP
| order by Timestamp desc
```

---

## 🎯 Security Focus Areas

| Area | What I work on | Tools |
|:--|:--|:--|
| **Threat Detection & Hunting** | Alert triage, KQL hunting, custom detection rules | Defender XDR · Sentinel · KQL |
| **Incident Response** | Investigation, containment, eradication, recovery, post-incident reports | NIST SP 800-61 · Live response · Device isolation |
| **Adversary Emulation** | Safe attack simulation to test and tune detections | Atomic Red Team · MITRE ATT&CK |
| **Identity & Access** | Understanding sign-in risk, MFA coverage, local vs Entra accounts | Entra ID · IAM · Conditional Access |
| **Cloud Security** | Securing network access, logging, and workloads | Azure · AWS · NSG / VPC · Firewall · VPN |
| **Automation** | Scripting response actions and repeatable tooling | PowerShell · Python · Bash · Terraform |

---

## 🛠️ Tech Stack

### 🛡️ Security Operations
![Microsoft Defender XDR](https://img.shields.io/badge/Defender_XDR-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Microsoft Sentinel](https://img.shields.io/badge/Sentinel-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Entra ID](https://img.shields.io/badge/Entra_ID-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![KQL](https://img.shields.io/badge/KQL-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE_ATT%26CK-ED1C24?style=for-the-badge)
![Atomic Red Team](https://img.shields.io/badge/Atomic_Red_Team-B22222?style=for-the-badge)
![NIST](https://img.shields.io/badge/NIST_SP_800--61-003366?style=for-the-badge)

`SIEM` `EDR` `Incident Response` `Threat Hunting` `Alert Triage` `Detection Engineering`

### 🔐 Networking & Security Fundamentals
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

`IAM` `Encryption` `Firewall` `VPC` `VPN` `Policy Enforcement` `Load Balancing`

### 💻 Scripting & Languages
![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white)
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Bash](https://img.shields.io/badge/Bash-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Java](https://img.shields.io/badge/Java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Go](https://img.shields.io/badge/Go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)

### ☁️ Cloud & Infrastructure (the environments I help secure)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-%23326CE5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-%231A1918.svg?style=for-the-badge&logo=ansible&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![VMware](https://img.shields.io/badge/VMware-%23607078.svg?style=for-the-badge&logo=vmware&logoColor=white)

### 📊 Monitoring & Observability
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)
![Datadog](https://img.shields.io/badge/Datadog-%23632CA6.svg?style=for-the-badge&logo=datadog&logoColor=white)
![CloudWatch](https://img.shields.io/badge/CloudWatch-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
`Zabbix`

---

## 🌱 Currently

- 📜 Working towards **CompTIA Security+** certification.
- 🧪 Building more SOC lab scenarios and writing up each incident in **NIST SP 800-61** format
- 🔍 Deepening knowledge in networking, threat detection, and incident response
- ☁️ Applying security thinking to **Terraform** and **Kubernetes** work

---

<div align="center">

*"Detect early, respond fast, document everything."*

![Profile Views](https://komarev.com/ghpvc/?user=abirthapa1&color=00B4D8&style=flat-square)

</div>
