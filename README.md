# 🔍 Security Log Analyzer — SSH Brute Force Detection Tool

A Python-based cybersecurity tool that analyzes Linux SSH authentication logs, detects suspicious login activities, identifies potential brute-force attacks, and generates structured security reports.

Built to demonstrate practical cybersecurity concepts, log analysis, threat detection, and Python automation.

## 🚀 Features

- **SSH Log Parsing:** Reads and processes Linux authentication log files (`auth.log`).
- **Brute Force Detection:** Identifies suspicious IP addresses based on repeated failed login attempts.
- **IP-Based Analysis:** Groups failed login attempts and highlights potentially malicious sources.
- **Targeted Username Detection:** Identifies usernames frequently targeted during login attempts.
- **Terminal Reporting:** Displays security analysis results in a structured terminal interface.
- **Report Generation:** Exports analysis results into CSV, HTML, and JSON formats.
- **Custom Threshold:** Allows users to configure the number of failed attempts required to flag suspicious activity.
- **Efficient Processing:** Processes log files line by line for better memory efficiency.

## 📁 Project Structure

```text
Security-Log-Analyzer/
│
├── analyzers/
│   ├── __init__.py
│   └── brute_force.py
│
├── parsers/
│   ├── __init__.py
│   └── ssh_parser.py
│
├── reporters/
│   ├── __init__.py
│   ├── report.py
│   └── export.py
│
├── sample_logs/
│   └── auth.log
│
├── reports/
│
├── .gitignore
├── main.py
├── generate_test_logs.py
├── requirements.txt
└── README.md
```

## ⚙️ Installation

**1. Clone the repository**

```bash
git clone https://github.com/rajputsidhu/Security-Log-Analyzer.git
cd Security-Log-Analyzer
```

**2. Create a virtual environment**

```bash
python3 -m venv venv
```

**3. Activate the virtual environment**

macOS / Linux:

```bash
source venv/bin/activate
```

Windows:

```bash
venv\Scripts\activate
```

**4. Install dependencies**

```bash
pip install -r requirements.txt
```

## 🖥️ Usage

**Basic log analysis**

```bash
python main.py --log sample_logs/auth.log --threshold 5
```

**Analyze logs with a custom threshold**

```bash
python main.py --log sample_logs/auth.log --threshold 10
```

**Generate reports**

```bash
python main.py --log sample_logs/auth.log --threshold 5 --export
```

**Generate sample test logs**

```bash
python generate_test_logs.py
```

Then analyze the generated logs:

```bash
python main.py --log sample_logs/auth.log --threshold 5 --export
```

**View available command-line options**

```bash
python main.py --help
```

## 🔧 Command-Line Arguments

| Argument | Description |
|---|---|
| `--log` | Path to the SSH authentication log file |
| `--threshold` | Minimum failed login attempts required to flag an IP address |
| `--export` | Enables report export |

## 📊 Report Formats

The tool supports multiple report formats for security analysis:

| Format | Output | Purpose |
|---|---|---|
| Terminal | Console output | Quick security analysis |
| CSV | Reports directory | Data analysis and investigation |
| HTML | Reports directory | Browser-based report viewing |
| JSON | `report.json` | Structured security data |

## ⚙️ How It Works

**1. Log Parsing**

The parser reads SSH authentication logs and extracts relevant information such as timestamps, usernames, IP addresses, and login activity.

**2. Security Analysis**

The analyzer groups failed login attempts by IP address, identifies suspicious activity based on the configured threshold, and determines frequently targeted usernames.

**3. Threat Detection**

IP addresses exceeding the configured failed-login threshold are flagged for further investigation.

**4. Report Generation**

The reporting module displays analysis results and generates structured CSV, HTML, and JSON reports.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core development |
| Regular Expressions | Log parsing |
| Pandas | Data analysis and aggregation |
| Rich | Terminal reporting |
| CSV | Structured report export |
| HTML | Browser-based reports |
| JSON | Structured data export |
| Git & GitHub | Version control |

## 🔐 Cybersecurity Concepts Demonstrated

- Linux system log analysis
- SSH authentication monitoring
- Brute-force attack detection
- Failed login investigation
- IP address-based threat identification
- Security event analysis
- Automated security reporting

## 👨‍💻 Author

**Sidhu Kumar Singh**

B.Tech Computer Science Engineering  
Cybersecurity Enthusiast | Python Developer

- GitHub: https://github.com/rajputsidhu
- LinkedIn: https://linkedin.com/in/sidhusingh

## 📄 License

This project is licensed under the MIT License.

---

⭐ If you find this project useful, consider giving it a star!
