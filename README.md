# **Hacking Tools Collection (Golang) 🚀**

A collection of powerful hacking tools written in **Golang**, designed to enhance penetration testing, reconnaissance and exploitation workflows. This repository includes tools for **DNS enumeration, HTTP attack vectors, metadata extraction, and Metasploit integration**.

⚠️ **Disclaimer:** These tools are strictly for ethical hacking, security research and educational purposes. Unauthorized use of these tools against systems you don’t own or have explicit permission to test is illegal.

---
## **Tools Overview**

This repository features a variety of offensive security tools, divided into different categories:

### **🔎 Bing Search Scraper**

A tool for extracting search results from **Bing** to assist in OSINT (Open-Source Intelligence) gathering.

 Features:
- Automates queries to **Bing**
- Extracts **URLs, titles, and descriptions**
- Supports **pagination for deeper searches**
- Output results in **JSON, CSV, or plaintext**

 **Example Usage:**
`bing_scraper -query "site:example.com" -pages 5 -output results.json`

---
### **🌐 DNS Tools**

#### **DNS Server**

A lightweight **DNS server** written in Golang, useful for handling and logging DNS queries.

Features:
- Handles **A, AAAA, CNAME, and TXT records**
- Supports **custom domain resolution**
- Logs **incoming queries** for analysis

**Example Usage:**
`dns_server -port 53 -config dns_config.json`

#### **DNS Proxy**

A **transparent DNS proxy** that can modify or redirect queries for security analysis and MITM attacks.

Features:
- Forward queries to **upstream DNS servers**
- Modify **responses on-the-fly**
- Supports **logging and debugging**

**Example Usage:**
`dns_proxy -upstream 8.8.8.8 -log dns.log`

#### **Subdomain Fuzzer**

A tool to **brute-force subdomains** using a wordlist.

Features:
- Supports **multithreading** for faster enumeration
- Can resolve **IP addresses** of found subdomains
- Export results in **CSV or JSON**

**Example Usage:**
`subfuzzer -domain example.com -wordlist subdomains.txt -threads 10`

---
### **HTTP Tools**

#### **1️⃣ Credential Harvesting Server**

A **fake login page generator** to capture credentials during phishing engagements.

Features:
- Create a **custom phishing login page**
- Logs **entered credentials**
- Supports **TLS for secure-looking phishing pages**

**Example Usage:**
`cred_harvester -port 8080 -template login.html -output creds.log`

#### **2️⃣ Keylogger (HTTP-Based)**

A **JavaScript-based keylogger** that captures keystrokes and sends data to a remote server.

Features:

- **Injectable script** for capturing keystrokes
- Sends keystrokes to an **HTTP endpoint**
- Lightweight and stealthy

**Example Usage:**
`keylogger_server -port 9000 -log keys.log`

#### **3️⃣ HTTP Client Wrapper**

A **custom HTTP client** with enhanced capabilities for penetration testing.

 Features:
- **Bypass WAF and security headers**
- Supports **proxy chaining**
- Auto-retry failed requests

**Example Usage:**
`http_client -url "https://target.com" -proxy "http://127.0.0.1:8080"`

#### **4️⃣ Reverse Proxy**

A **man-in-the-middle reverse proxy** that intercepts HTTP traffic.

 Features:
- Modify **requests and responses**
- Capture and log **credentials, headers, and tokens**
- Supports **TLS decryption**

**Example Usage:**
`reverse_proxy -listen 8081 -target https://example.com`

#### **5️⃣ Middleware Toolkit**

Custom **middleware components** for logging, modifying, and injecting HTTP requests.

 Features:
- Can be **integrated with other tools**
- Supports **header manipulation, cookie injection**
- Useful for **automating attacks on web applications**

**Example Usage:**
`middleware.AddHeader("User-Agent", "Mozilla/5.0")`

---
### **📄 Metadata Extractor**

A tool to **analyze and extract metadata** from files like PDFs, DOCX, and images.

 Features:
- Extract **EXIF data, document properties, and timestamps**
- Supports **PDF, DOCX, PNG, JPG, and MP4**
- Can be used for **OSINT investigations**

**Example Usage:**
`metadata_extractor -file document.pdf`

---
### **💀 Metasploit RPC API Wrapper (WIP)**

A **Golang-based wrapper** to interact with Metasploit’s **RPC API** for automation.

 Features (Work in Progress):
- Launch and **control Metasploit modules**
- Retrieve **session details and exploit outputs**
- Automate **Metasploit actions from Golang scripts**

**Example Usage:**
`msf := MetasploitClient{Host: "127.0.0.1", Port: 55553, Token: "your_token"} msf.RunModule("exploit/windows/smb/ms17_010")`

---
## **⚙️ Installation & Setup**

To install and run these tools, ensure you have **Golang installed**.
### **Install Golang**

If not installed, download and install Golang from: [https://golang.org/dl/](https://golang.org/dl/)

### **Clone the Repository**
`git clone https://github.com/ssam246/GoPwn`

### **Build & Run a Tool**

Example for the **Subdomain Fuzzer**:
`cd subdomain_fuzzer go build -o subfuzzer main.go ./subfuzzer -domain example.com -wordlist subdomains.txt`

---
## **Contributing**

💡 Contributions are welcome! If you’d like to improve an existing tool or add a new one:

1. Fork the repo
2. Create a new branch (`git checkout -b feature-xyz`)
3. Commit changes and push (`git push origin feature-xyz`)
4. Submit a Pull Request (PR)

---
## **⚠️ Legal Disclaimer**

This software is intended for **educational and security research** purposes **only**.  
**Do not use** these tools against systems **without explicit authorization**.  
Misuse of these tools may violate **cybersecurity laws** and could result in **legal consequences**.

Use responsibly and **stay ethical**! 🛡️

---
## **Author**

Developed with ❤️ and ☕ by **Stephen**
