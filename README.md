# 🔐 CVE to MITRE ATT&CK Mapping Tool

## 📌 Overview

This project is a simple Python-based tool that takes a **CVE ID as input** and retrieves:

* 📄 CVE Description
* 📊 CVSS Score
* 🎯 MITRE ATT&CK Technique & Tactic

The tool demonstrates how vulnerability data can be mapped to attacker behavior using basic automation.

---

## 🎯 Objectives

* Automate retrieval of vulnerability details from the NVD API
* Analyze CVE descriptions
* Map vulnerabilities to relevant MITRE ATT&CK techniques
* Demonstrate practical application of threat intelligence concepts

---

## ⚙️ Technologies Used

* Python 3
* `requests` library
* NVD (National Vulnerability Database) API

---

## 🚀 How It Works

1. User enters a CVE ID (e.g., `CVE-2021-3156`)
2. The tool fetches CVE data from the NVD API
3. It extracts:

   * Description
   * CVSS Score
4. The description is analyzed using keyword matching
5. The tool maps it to a relevant MITRE ATT&CK technique and tactic

---

## 🛠 Installation & Usage

### Step 1: Install dependencies

```bash
pip install requests
```

### Step 2: Run the script

```bash
python script.py
```

### Step 3: Enter CVE ID

```
Enter CVE ID: CVE-2021-3156
```

---

## 📊 Example Output

```
===== CVE DETAILS =====
Description: Heap-based buffer overflow in sudo...
CVSS Score: 7.8

===== MITRE ATT&CK Mapping =====
Technique: T1068 - Exploitation for Privilege Escalation
Tactic: Privilege Escalation
```

---

## 🧠 MITRE Mapping Logic

The tool uses a simple keyword-based mapping approach.
For example:

| Keyword               | MITRE Technique | Tactic               |
| --------------------- | --------------- | -------------------- |
| remote code execution | T1190           | Initial Access       |
| privilege escalation  | T1068           | Privilege Escalation |
| authentication bypass | T1190           | Initial Access       |
| command execution     | T1059           | Execution            |

---

## ⚠️ Limitations

* Mapping is rule-based (not using full MITRE database)
* Depends on keywords in CVE description
* Not all CVEs may map correctly

---

## 🔮 Future Improvements

* Integration with MITRE ATT&CK STIX/TAXII feeds
* Machine learning-based mapping
* GUI interface
* Risk classification (Low, Medium, High, Critical)
* Support for batch CVE analysis

---

## 🎓 Academic Context

This project was developed as part of coursework for **MS Information Security**, demonstrating:

* Vulnerability analysis
* CVSS understanding
* MITRE ATT&CK framework application
* Basic threat intelligence automation

---

## 📌 Author

Raffay Ahmed Khan
MS Information Security Student
NED University

---

## ⭐ Contribution

Feel free to fork, improve, or extend this project for learning purposes.
