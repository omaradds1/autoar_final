<<<<<<< HEAD
<<<<<<< HEAD
# AutoAR (Automated Attack and Reconnaissance Tool)

AutoAR is a comprehensive web-based security scanning and vulnerability management platform that automates the process of reconnaissance and vulnerability assessment across multiple domains.

## Features

### Core Functionality
- Automated security scanning and reconnaissance
- Multi-domain support
- Comprehensive vulnerability assessment
- Real-time scan monitoring
- Configurable scanning options

### Web Interface Components
1. **Dashboard**
   - Vulnerability statistics
   - Scan overview
   - Recent scan tracking

2. **Vulnerabilities Page**
   - Detailed vulnerability listing
   - Filtering by severity and status
   - Comprehensive vulnerability details

3. **Attack Surface Page**
   - Endpoint discovery
   - Subdomain tracking
   - Technology stack identification

4. **Settings Page**
   - Tool configuration management
   - Notification settings
   - Scan default preferences

5. **Best Practices Page**
   - Security recommendations
   - Categorized best practices
   - Severity-based guidance

## Technology Stack

### Backend
- Flask (Python)
- Flask-CORS
- Virtual Environment

### Frontend
- Next.js
- TypeScript
- Tailwind CSS
- React

## Project Structure
```
autoAR-web/
├── backend/
│   ├── app.py
│   └── venv/
├── frontend/
│   ├── components/
│   ├── pages/
│   ├── styles/
│   └── public/
└── README.md
```

## Setup and Installation

### Backend Setup
1. Create and activate virtual environment:
   ```bash
   cd backend
   python3 -m venv venv
   source venv/bin/activate  # On Unix/macOS
   ```

2. Install dependencies:
   ```bash
   pip install flask flask-cors
   ```

3. Start the Flask server:
   ```bash
   python app.py
   ```
   The backend will run on http://localhost:5000

### Frontend Setup
1. Install dependencies:
   ```bash
   cd frontend
   npm install
   ```

2. Start the development server:
   ```bash
   npm run dev
   ```
   The frontend will run on http://localhost:3000

## Features in Development
- Backend API integration for real data
- Persistent configuration storage
- Advanced error handling
- Authentication mechanism
- Comprehensive result parsing
- Machine learning-based vulnerability prediction
- Advanced reporting capabilities
- Integration with external security platforms
- Containerization support
- CI/CD pipeline integration

## Security Considerations
- Input validation
- Secure header implementation
- Rate limiting
- Webhook notification security
- Configurable tool options

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
=======
# ReconRaptor
ReconRaptor automates reconnaissance for pentesters and bug hunters. It gathers and analyzes subdomains, URLs, and potential vulnerabilities, streamlining the process to efficiently identify security weaknesses. With automated workflows and built-in checks for common tools, ReconRaptor ensures thorough and systematic recon operations.
>>>>>>> d90b200 (Initial commit)
=======
## Overview

This tool is designed to automate various web security testing tasks such as subdomain enumeration, URL fetching, subdomain takeover scanning, JS exposure scanning, live host filtering, port scanning, nuclei scans, reflection scanning, GF pattern scans, Dalfox scans, fuzzing, and SQL injection scanning. It uses various popular security tools and organizes the results into a structured directory.

## Requirements

Before running this script, ensure that the following tools are installed on your system:

- `subfinder`
- `httpx`
- `gau`
- `subov88r`
- `nuclei`
- `naabu`
- `kxss`
- `qsreplace`
- `gf`
- `dalfox`
- `ffuf`
- `interlace`
- `urldedupe`
- `sqlmap`

Additionally, ensure the following directories are available or clone the respective repositories:

- `nuclei_templates` from [h0tak88r/nuclei_templates](https://github.com/h0tak88r/nuclei_templates.git)
- `nuclei-templates` from [projectdiscovery/nuclei-templates](https://github.com/projectdiscovery/nuclei-templates.git)
- `Wordlists` from [h0tak88r/Wordlists](https://github.com/h0tak88r/Wordlists.git)
- `~/.gf` for GF patterns from [1ndianl33t/Gf-Patterns](https://github.com/1ndianl33t/Gf-Patterns.git)

## Usage

```bash
./reconraptor.sh <target_domain|subdomain_list> [-s single_subdomain]
```

### Arguments

- `target_domain|subdomain_list`: The target domain or a file containing a list of subdomains to scan.
- `-s single_subdomain`: (Optional) Specify a single subdomain to focus the scan on.

## Features

1. **Subdomain Enumeration**
    - Uses `subfinder` to find subdomains of the target domain.

2. **URL Fetching**
    - Uses `gau` to fetch URLs associated with the target domain or subdomains.

3. **Subdomain Takeover Scanning**
    - Uses `subov88r` and `nuclei` to check for potential subdomain takeovers.

4. **JS Exposure Scanning**
    - Identifies and analyzes exposed JavaScript files.

5. **Live Host Filtering**
    - Uses `httpx` to filter live hosts.

6. **Port Scanning**
    - Uses `naabu` for port scanning on live hosts.

7. **Exposed Panels Scanning**
    - Uses `nuclei` to identify exposed administrative panels.

8. **Nuclei Scanning**
    - Runs `nuclei` scans using various templates.

9. **Reflection Scanning**
    - Uses `kxss` to find reflected XSS vulnerabilities.

10. **GF Pattern Scans**
    - Uses `gf` to search for specific vulnerability patterns in URLs.

11. **Dalfox Scanning**
    - Uses `dalfox` to scan for XSS vulnerabilities.

12. **Fuzzing with ffuf**
    - Uses `ffuf` to fuzz endpoints for potential vulnerabilities.

13. **SQL Injection Scanning**
    - Uses `sqlmap` to scan for SQL injection vulnerabilities.

## Setup

### Clone Necessary Repositories

Ensure the necessary repositories are cloned:

```bash
git clone https://github.com/h0tak88r/nuclei_templates.git
git clone https://github.com/projectdiscovery/nuclei-templates.git
git clone https://github.com/h0tak88r/Wordlists.git
git clone https://github.com/1ndianl33t/Gf-Patterns.git
mkdir -p ~/.gf
cp Gf-Patterns/*.json ~/.gf
echo 'source $GOPATH/src/github.com/tomnomnom/gf/gf-completion.bash' >> ~/.bashrc
source ~/.bashrc
```

### Install Required Tools

Install the required tools using your preferred package manager or by following their respective installation guides.

## Running the Script

To run the script, provide a target domain or a file containing a list of subdomains. Optionally, you can specify a single subdomain with the `-s` flag.

Example:

```bash
./reconraptor.sh example.com
./reconraptor.sh subdomains.txt -s sub.example.com
```

The script will create a `results` directory where all the output files will be stored.

## Output

The script organizes the results in the `results` directory with files for subdomains, URLs, live hosts, port scans, exposed panels, nuclei scan results, reflection scan results, GF pattern results, Dalfox scan results, fuzzing results, and SQL injection scan results.

## Conclusion

This tool automates the process of web security testing by integrating several popular security tools. Ensure all required tools are installed and repositories are cloned before running the script. Adjust the script and tools as necessary to fit your specific needs.
>>>>>>> a3d66be2 (Update README.md)
