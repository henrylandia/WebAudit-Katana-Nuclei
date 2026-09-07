<div align="center">

# 🛡️ Web Audit
### Katana + Nuclei

```text
██╗    ██╗███████╗██████╗      █████╗ ██╗   ██╗██████╗ ██╗████████╗
██║    ██║██╔════╝██╔══██╗    ██╔══██╗██║   ██║██╔══██╗██║╚══██╔══╝
██║ █╗ ██║█████╗  ██████╔╝    ███████║██║   ██║██║  ██║██║   ██║
██║███╗██║██╔══╝  ██╔══██╗    ██╔══██║██║   ██║██║  ██║██║   ██║
╚███╔███╔╝███████╗██████╔╝    ██╔══██║╚██████╔╝██████╔╝██║   ██║
 ╚══╝╚══╝ ╚══════╝╚═════╝     ╚═╝  ╚═╝ ╚═════╝ ╚═════╝ ╚═╝   ╚═╝

              ╔══════════════════════════════════╗
              ║      K A T A N A  +  N U C L E I ║
              ╚══════════════════════════════════╝
Automated Web Security Auditing










<br>

Reconnaissance → Crawling → Endpoint Discovery → Template Scanning → Results

<br>

🚀 Installation •
📖 Usage •
🔎 Features •
📂 Results •
⚠️ Legal

</div>
🛡️ About

Web Audit — Katana + Nuclei is a Bash automation framework created by Henry Molina for performing initial web security assessments in authorized environments.

The project combines tools from the ProjectDiscovery ecosystem to create a simple workflow:

                         ┌──────────────────────┐
                         │    AUTHORIZED TARGET │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │       KATANA         │
                         │                      │
                         │  Web Crawling        │
                         │  JavaScript           │
                         │  Forms                │
                         │  Endpoints           │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │     DISCOVERED URLS  │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │       NUCLEI         │
                         │                      │
                         │  XSS                 │
                         │  SQLi                │
                         │  SSTI                │
                         │  LFI                 │
                         │  SSRF                │
                         │  CORS                │
                         │  CVEs                │
                         │  Misconfigurations   │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │       RESULTS        │
                         │                      │
                         │  URLs                │
                         │  Findings            │
                         │  Logs                │
                         │  Summary             │
                         └──────────────────────┘

The goal is not to replace a complete penetration test.

Instead, Web Audit provides a convenient starting point for reconnaissance and automated vulnerability detection.

✨ Features
Feature	Description
🕷️ Katana Crawling	Discovers URLs and endpoints
🎯 Domain Scope	Keeps crawling within root domain + subdomains
📜 JavaScript Crawling	Parses JavaScript resources
📝 Form Extraction	Extracts forms and input fields
🧪 Nuclei Scanning	Runs template-based security checks
🎯 Modular Scans	Select individual vulnerability categories
📁 Automatic Reports	Organizes results by target and timestamp
📊 Summary	Generates a simple audit summary
🔧 Auto Installer	Installs required tools
🔄 Auto Updates	Updates ProjectDiscovery tools/templates
🖥️ Interactive CLI	Simple terminal menu
🔎 What Does It Scan?

The current version provides modules for:

┌──────────────────────────────────────────────┐
│               NUCLEI MODULES                 │
├──────────────────────────────────────────────┤
│                                              │
│   01  XSS                 Cross-Site Script │
│   02  SQLi                SQL Injection      │
│   03  SSTI                Template Injection │
│   04  LFI                 Local File Include │
│   05  SSRF                Server-Side Req.   │
│   06  CORS                CORS checks        │
│   07  Headers             HTTP headers       │
│   08  Exposure            Exposure checks    │
│   09  CVE                 Known CVEs         │
│   10  Misconfiguration    Misconfigurations  │
│   11  General             General templates  │
│                                              │
└──────────────────────────────────────────────┘
🎯 Scope Management

One of the important parts of the project is controlling the crawling scope.

Katana is executed using:

-fs rdn

This means the crawler is intended to stay within the root domain and its subdomains.

For example:

example.com
│
├── www.example.com
├── app.example.com
├── api.example.com
├── dev.example.com
├── staging.example.com
└── admin.example.com

External domains referenced by the application are not intended to become part of the crawling scope.

Examples:

google.com
microsoft.com
w3.org
cloudflare.com

This is especially useful for applications that load resources from multiple third-party services.

🧰 Technologies

Web Audit uses:

🕷️ Katana

High-speed web crawler from ProjectDiscovery.

Used for:

Endpoint discovery
URL crawling
JavaScript crawling
Form extraction
Web application reconnaissance
🧪 Nuclei

Template-based vulnerability scanner from ProjectDiscovery.

Used for:

Known vulnerabilities
Misconfigurations
Security checks
Exposure detection
Technology-specific templates
🌐 HTTPX

ProjectDiscovery HTTP toolkit used as an auxiliary component and planned for further integration.

🐚 Bash

The entire automation layer is written in Bash.

💻 Requirements
Operating System

The project is primarily designed for Linux environments.

Recommended:

Kali Linux

Also intended to support:

Debian
Ubuntu
Linux Mint
Pop!_OS
Fedora
RHEL
CentOS
Rocky Linux
AlmaLinux
Arch Linux
Manjaro
Dependencies

The project requires:

Bash
Git
Go
Curl
Wget
Ca-certificates
Build tools
Internet connection

The script can automatically install the main dependencies on supported distributions.

🚀 Installation
1. Clone the repository
git clone https://github.com/henrylandia/WebAudit-Katana-Nuclei.git

Enter the directory:

cd WebAudit-Katana-Nuclei
2. Give execution permission
chmod +x web-audit.sh
3. Validate the script

Before executing it, check the Bash syntax:

bash -n web-audit.sh

If there is no output, the syntax check passed.

4. Start Web Audit
./web-audit.sh

Or:

bash web-audit.sh
🛠️ First-Time Setup

When running Web Audit on a new machine, select:

2) Instalar todas las dependencias

The installer attempts to configure:

┌─────────────────────────────┐
│       INSTALLATION          │
├─────────────────────────────┤
│                             │
│  ✓ System dependencies      │
│  ✓ Go                       │
│  ✓ Katana                   │
│  ✓ Nuclei                   │
│  ✓ HTTPX                    │
│  ✓ Nuclei Templates         │
│                             │
└─────────────────────────────┘

The Go binaries are installed under:

$HOME/go/bin

and the script configures the user's PATH.

📋 Main Menu

After launching the script:

============================================================
                 WEB AUDIT - KATANA + NUCLEI
============================================================

Directorio de auditorías:
  /home/user/web-audits

1) Nueva auditoría web
2) Instalar todas las dependencias
3) Comprobar herramientas
4) Actualizar herramientas y templates
5) Ver auditorías anteriores
0) Salir
🔍 Usage
Step 1 — Start a new audit

Select:

1) Nueva auditoría web

The script asks for the target:

URL objetivo:

Example:

https://app.example.com

If you enter:

app.example.com

the script automatically normalizes it to:

https://app.example.com
⚙️ Step 2 — Choose Crawling Depth

The default crawling depth is:

5

Example:

Profundidad de Katana [5]:

You can adjust this depending on the size and complexity of the application.

Deeper crawling can generate significantly more requests and URLs.

🕷️ Step 3 — Katana

The crawling phase uses:

katana \
    -u TARGET \
    -fs rdn \
    -d DEPTH \
    -jc \
    -fx
Parameters
Parameter	Purpose
-u	Target URL
-fs rdn	Root domain + subdomains
-d	Crawl depth
-jc	JavaScript crawling
-fx	Form extraction
🔗 Step 4 — URL Collection

Katana produces the raw crawl output:

urls-raw.txt

The script then generates:

urls.txt

containing the processed and unique URLs.

The number of discovered URLs is stored in:

url-count.txt
🧪 Step 5 — Nuclei

After crawling, Web Audit asks which Nuclei module should be executed:

1) XSS
2) SQLi
3) SSTI
4) LFI
5) SSRF
6) CORS
7) Headers
8) Exposure
9) CVE
10) Misconfiguration
11) General
12) TODOS
0) Omitir Nuclei

You can run a single module or all configured modules.

📂 Results

Every audit is stored separately.

Default location:

~/web-audits/

Example:

web-audits/
└── app.example.com_20260907_153000/
    │
    ├── TARGET.txt
    ├── urls-raw.txt
    ├── urls.txt
    ├── url-count.txt
    ├── katana.log
    ├── SUMMARY.txt
    │
    └── nuclei/
        ├── xss.txt
        ├── xss.log
        ├── sqli.txt
        ├── sqli.log
        ├── ssti.txt
        ├── ssti.log
        ├── lfi.txt
        ├── lfi.log
        ├── ssrf.txt
        ├── ssrf.log
        ├── cors.txt
        ├── cors.log
        ├── headers.txt
        ├── headers.log
        ├── exposure.txt
        ├── exposure.log
        ├── cve.txt
        ├── cve.log
        ├── misconfig.txt
        ├── misconfig.log
        ├── general.txt
        └── general.log
📊 SUMMARY.txt

At the end of the audit, Web Audit generates:

SUMMARY.txt

The summary contains information such as:

Target
Hostname
Date
Number of URLs
Nuclei results
Output directory

This makes it easier to review an assessment without opening every individual log.

🔄 Updating Tools

From the main menu select:

4) Actualizar herramientas y templates

This updates the installed ProjectDiscovery tools and Nuclei templates.

You can also update Nuclei templates manually:

nuclei -update-templates
🔧 Troubleshooting
Permission denied

Run:

chmod +x web-audit.sh
Bash syntax error

Run:

bash -n web-audit.sh
Katana not found

Check:

ls -la "$HOME/go/bin/katana"

Then:

export PATH="$HOME/go/bin:$PATH"
Nuclei not found

Check:

ls -la "$HOME/go/bin/nuclei"

Then:

export PATH="$HOME/go/bin:$PATH"
Check installed tools
katana -version
nuclei -version
httpx -version
🧪 Recommended Workflow

For a normal authorized assessment:

       ┌──────────────────────┐
       │   Authorized Target  │
       └──────────┬───────────┘
                  │
                  ▼
       ┌──────────────────────┐
       │       KATANA         │
       │      Crawling        │
       └──────────┬───────────┘
                  │
          ┌───────┴────────┐
          │                │
          ▼                ▼
       URLs             Forms
          │                │
          └───────┬────────┘
                  │
                  ▼
       ┌──────────────────────┐
       │       NUCLEI         │
       │  Template Scanning   │
       └──────────┬───────────┘
                  │
                  ▼
       ┌──────────────────────┐
       │       RESULTS        │
       │                      │
       │  Findings            │
       │  Logs                │
       │  URLs                │
       │  Summary             │
       └──────────────────────┘
⚠️ Limitations

Web Audit is designed for initial automated assessment.

It does not replace a manual penetration test or a complete application security assessment.

Automated crawling and template-based scanning can miss vulnerabilities involving:

Authentication
Authorization
Business logic
Complex workflows
Multi-step transactions
JSON APIs
GraphQL
WebSockets
Session-dependent functionality
Client-side vulnerabilities
Custom application logic
Vulnerabilities without an existing Nuclei template

A clean scan does not mean that an application is secure.

🔐 Legal Disclaimer
Authorized Use Only

This software is intended exclusively for:

Your own applications.
Authorized penetration testing.
Security laboratories.
CTF environments.
Development environments.
Staging environments.
Systems for which you have explicit permission.

Do not scan third-party infrastructure without authorization.

The author, Henry Molina, is not responsible for any misuse of this software or for damage caused by unauthorized testing.

By using this project, you accept responsibility for ensuring that your activities comply with applicable laws, regulations, contracts and authorization boundaries.

🚧 Roadmap

Future improvements may include:

 HTTPX live-host verification
 Multi-target support
 Subdomain enumeration
 Improved URL filtering
 HTML reports
 JSON reports
 CSV export
 Vulnerability statistics
 Authentication support
 Custom Nuclei templates
 Configuration file
 Custom output directory
 Improved logging
 Parallel scanning options
 Additional ProjectDiscovery integrations
 Web-based dashboard
🤝 Contributing

Contributions, bug reports and suggestions are welcome.

Fork the project
git clone https://github.com/henrylandia/WebAudit-Katana-Nuclei.git
cd WebAudit-Katana-Nuclei

Create a branch:

git checkout -b feature/my-feature

Make your changes and test them:

bash -n web-audit.sh

Then commit:

git add .
git commit -m "Add my feature"
git push origin feature/my-feature

Open a Pull Request on GitHub.

⭐ Support the Project

If you find Web Audit — Katana + Nuclei useful:

⭐ Star the repository
🐛 Report bugs
💡 Suggest improvements
🔧 Submit Pull Requests

Repository:

https://github.com/henrylandia/WebAudit-Katana-Nuclei

👨‍💻 Author
<div align="center">
Henry Molina

Security Researcher / Developer

GitHub:

@henrylandia

Project:

WebAudit-Katana-Nuclei

</div>
📜 License

This project is released under the MIT License.

See:

LICENSE

for the complete license text.

<div align="center">
╔══════════════════════════════════════════════════════════╗
║                                                          ║
║             WEB AUDIT — KATANA + NUCLEI                 ║
║                                                          ║
║       Authorized Security Testing & Research             ║
║                                                          ║
╚══════════════════════════════════════════════════════════╝
Built with ❤️ and Bash by Henry Molina

⭐ Star the repo if you find it useful!

</div> ```
