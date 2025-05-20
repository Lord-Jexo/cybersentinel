# CyberSentinel IDS

```
 ██████╗██╗   ██╗██████╗ ███████╗██████╗ ███████╗███████╗███╗   ██╗████████╗██╗███╗   ██╗███████╗██╗     
██╔════╝╚██╗ ██╔╝██╔══██╗██╔════╝██╔══██╗██╔════╝██╔════╝████╗  ██║╚══██╔══╝██║████╗  ██║██╔════╝██║     
██║      ╚████╔╝ ██████╔╝█████╗  ██████╔╝███████╗█████╗  ██╔██╗ ██║   ██║   ██║██╔██╗ ██║█████╗  ██║     
██║       ╚██╔╝  ██╔══██╗██╔══╝  ██╔══██╗╚════██║██╔══╝  ██║╚██╗██║   ██║   ██║██║╚██╗██║██╔══╝  ██║     
╚██████╗   ██║   ██████╔╝███████╗██║  ██║███████║███████╗██║ ╚████║   ██║   ██║██║ ╚████║███████╗███████╗
 ╚═════╝   ╚═╝   ╚═════╝ ╚══════╝╚═╝  ╚═╝╚══════╝╚══════╝╚═╝  ╚═══╝   ╚═╝   ╚═╝╚═╝  ╚═══╝╚══════╝╚══════╝
                                                                   
                JEXO (Long Life PAKISTAN)
```
![Black Blue Modern Gradient Cybersecurity Presentation](https://github.com/user-attachments/assets/66301be1-6677-4d70-933b-149f2fac62f1)



## 📋 Overview

CyberSentinel is an advanced open-source Intrusion Detection System (IDS) designed to safeguard systems against unauthorized access and malicious activities. This security tool continuously monitors system logs, network connections, running processes, and file system changes to identify suspicious patterns that could indicate a cyber attack in progress.

### What Does CyberSentinel Do?

CyberSentinel acts as your digital security guard, constantly watching for signs of:
- Hackers attempting to break into your system
- Malware trying to compromise your security
- Unusual network traffic patterns
- Suspicious changes to sensitive files
- Unauthorized access attempts
- Potential data breaches

When a security threat is detected, CyberSentinel immediately alerts you through multiple channels (dashboard, email, SMS) and can even take automated actions to block the attack.

**IMPORTANT:** This is a cybersecurity framework that you are encouraged to customize and extend according to your specific security needs. Feel free to modify, enhance, or build upon it!

## ✨ Features

- **Real-time Monitoring**
  - System log analysis
  - Network connection tracking
  - Process monitoring
  - File system integrity checking

- **Detection Capabilities**
  - Brute force attacks
  - SQL injection attempts
  - Cross-site scripting (XSS)
  - Command injection
  - File inclusion exploits
  - Port scanning
  - Privilege escalation
  - Backdoor/remote access attempts
  - DDoS attack signatures
  - Malware activity

- **Alert System**
  - Email notifications
  - SMS alerts
  - Web dashboard notifications
  - Detailed logging

- **Interactive Dashboard**
  - Real-time security status
  - Attack visualization
  - System performance metrics
  - Alert history and management

- **Automated Response (Optional)**
  - Malicious IP blocking
  - Suspicious process termination

## 🚀 Installation

### Prerequisites
- Python 3.6 or higher
- pip (Python package manager)

### Setup Steps

1. **Extract the detector.zip file**
   ```bash
   unzip detector.zip
   cd detector
   ```

2. **Install required packages**
   ```bash
   pip install psutil flask requests
   ```

3. **Verify file structure**
   Ensure you have the following structure:
   ```
   detector/
   │
   ├── cybersentinel.py       - Main Python file
   ├── config.json            - Configuration file
   │
   ├── signatures/
   │   ├── attack_signatures.json  - Attack patterns
   │   └── vulnerabilities.json    - Vulnerability database
   │
   ├── templates/
   │   └── index.html         - Dashboard HTML template
   │
   ├── static/
   │   ├── css/
   │   │   └── styles.css     - Dashboard styling
   │   └── js/
   │       └── dashboard.js   - Dashboard functionality
   │
   └── logs/                  - Log files directory
   ```

4. **Configure the system**
   - Edit `config.json` to set your monitoring preferences
   - Update email/SMS notification settings if needed
   - Adjust log file paths based on your operating system

## 🔧 Usage

### Starting the System

1. **Launch CyberSentinel**
   ```bash
   python cybersentinel.py
   ```

2. **Access the dashboard**
   Open your browser and navigate to:
   ```
   http://127.0.0.1:8080
   ```

### What the System Does

Once running, CyberSentinel actively:

1. **Monitors and Analyzes**:
   - **System Logs**: Scans auth.log, syslog, and application logs for suspicious patterns
   - **Network Connections**: Tracks all incoming/outgoing connections and flags unusual activity
   - **Running Processes**: Identifies suspicious processes like netcat, nmap, or unknown services
   - **File System**: Monitors critical system files for unauthorized modifications

2. **Detects Threats**:
   - Uses pattern matching to identify known attack signatures
   - Applies behavioral analysis to detect abnormal system usage
   - Compares current activity against vulnerability database
   - Identifies potential zero-day exploits through heuristic analysis

3. **Responds to Incidents**:
   - Generates alerts with detailed attack information
   - Categorizes threats by severity (critical, high, medium, low)
   - Can automatically block malicious IPs (when configured)
   - Can terminate suspicious processes (when configured)
   - Maintains detailed logs for forensic analysis

### Reviewing Security Information

- **Dashboard**: Provides real-time security status, charts, and visualizations
- **Alerts Table**: Shows detailed information about detected threats
- **System Metrics**: Displays CPU, memory, and network usage to identify resource abuse
- **Logs**: Maintains detailed logs in `cybersentinel.log` for forensic analysis

## 🛠️ Customization

This project is designed to be extended and customized. Here are some ways you can adapt it to your needs:

### Adding Custom Attack Signatures

Edit the `signatures/attack_signatures.json` file to add your own regex patterns for detecting specific attacks:

```json
{
  "custom_attack": {
    "pattern": "your_regex_pattern_here",
    "description": "Description of the attack",
    "severity": "high"
  }
}
```

### Monitoring Additional Log Files

Modify the `config.json` file to add more log files to monitor:

```json
"monitor": {
  "log_files": [
    "/path/to/your/log/file.log",
    "/another/log/file.log"
  ]
}
```

### Implementing Custom Response Actions

Extend the `AlertManager` class in `cybersentinel.py` to implement custom responses to detected threats.

### Enhancing the Dashboard

Modify the HTML, CSS, and JavaScript files in the `templates` and `static` directories to add more visualization features or customize the appearance.

## 🔗 Real-World Use Cases

### 1. Small Business Security
Small businesses without dedicated security teams can deploy CyberSentinel to get immediate alerts about potential security breaches and unauthorized access attempts.

### 2. Home Network Protection
Protect your personal devices and home network by monitoring for suspicious activity that might indicate your systems have been compromised.

### 3. Server Monitoring
Deploy CyberSentinel on servers to detect potential intrusions, privilege escalation attempts, and unauthorized access to sensitive files.

### 4. Educational Environments
Universities and cybersecurity training programs can use CyberSentinel as a practical tool to demonstrate how intrusion detection systems work.

### 5. Security Research
Security researchers can extend CyberSentinel's capabilities to develop and test new intrusion detection methodologies and attack signatures.

## 👥 About the Developer

CyberSentinel was created by **Lord-Jexo**, a Pakistani security researcher and ethical hacker passionate about developing open-source security tools that empower organizations and individuals to protect their digital assets.

Lord-Jexo has worked extensively in the cybersecurity field and developed CyberSentinel as a modular, extensible framework that can be customized to address various security challenges facing modern systems.

## 📜 License

This project is released under the MIT License. You are free to:
- Use this project commercially
- Distribute
- Modify
- Use privately
- Sell the software
- Customize it to your needs

## 💖 Credit

Created by **JEXO (PAKISTANI HACKER)**

## ⚠️ Disclaimer

This tool is provided for educational and legitimate security purposes only. The creators are not responsible for any misuse or damage caused by this program. Always ensure you have proper authorization before monitoring any system.

---

```
     _____ ________   ________ 
    |_   _|_   ___ \ |_   __  |
      | |   | |   ) |  | |_ \_|
      | |   | |   | |  |  _| _ 
     _| |  _| |   ) | _| |__/ |
    |___| |___| |___||________|
                               
 (Long Life PAKISTAN)
```
