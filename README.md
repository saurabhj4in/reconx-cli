# reconx
---

# 🔍 reconx-cli

**`reconx-cli`** is a lightweight command-line reconnaissance tool designed to help security analysts and DevSecOps teams quickly gather information about subdomains. It resolves IP addresses, performs reverse DNS lookups, and extracts hosting and organizational metadata using WHOIS records.

---

## 🧩 Features

* Resolve subdomains to IP addresses
* Perform reverse DNS lookups (PTR records)
* Extract hosting provider info via WHOIS:

  * `OrgName`
  * `Organization`
  * `NetName`
* Outputs structured, human-readable and color-coded terminal results

---

## 🚀 Getting Started

### Prerequisites

Ensure the following are installed on your system:

* Python 3.x (for `reconx-cli.py`)
* `whois`
* `host`
* `awk`, `grep`, `sed` (for the Bash version)
* `termcolor` (for Python version: install via `pip install termcolor`)

### Installation

Clone the repository or copy the scripts directly.

```bash
git clone https://github.com/your-org/reconx-cli.git
cd reconx-cli
```

### Usage

Prepare a file with one subdomain per line (e.g., `subdomains.txt`):

```txt
dev.example.com
api.example.net
login.example.org
```

Run the tool:

#### Python version:

```bash
python3 reconx-cli.py subdomains.txt
```

---

## 🖥️ Example Output

```
Subdomain        | IP Address     | Domain Pointer       | OrgName        | Organization
-----------------|----------------|----------------------|----------------|------------------
dev.example.com  | 192.0.2.5      | example-host.com     | Cloudflare     | Cloudflare, Inc.
```

---

## 🛡 Use Cases

* Initial reconnaissance during infrastructure VAPT
* Subdomain inventory and cleanup planning
* Detecting unmanaged or shadow IT infrastructure

---

## 📁 File Structure

```
reconx-cli/
├── reconx-cli.py        # Python version
├── subdomains.txt       # Sample input file
└── README.md
```

---
