
<p align="center">
<img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeDNjMHd5cHNnYnNwZjc2eDRxeHY1ZHpkNmVldG96ZXYzcmN5MDJlcSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/7AHLANoFz7zm1VLEM4/giphy.gif", width="400", height="400">
</p>

<h1 align="center">PWN2PDF</h1>
<h4 align="center">A utility that transforms complex Python-based malware into compact one-liner commands</h4>

### DESCRIPTION
**PWN2PDF** is a Linux red team tool designed for authorized security assessments. It generates a malicious desktop launcher that is disguised as a standard PDF file using a zero-width space character in the filename. When an unsuspecting victim double-clicks the file, their system interprets it as a `.desktop` application rather than a genuine PDF. The launcher then performs two actions simultaneously: it downloads and opens a legitimate PDF document to maintain the illusion of normal behavior, while silently fetching and executing an attacker-supplied payload in the background. This allows the payload to run without disrupting the victim's experience, as the real PDF captures their attention. The tool is intended for use only in controlled environments with explicit written permission.


### Key Features:

- **Multiple Payload Support**: Seamlessly handles both Python and Bash payloads with automatic execution detection
- **Built-in Payload Hosting**: Integrated Supabase file upload system — no external hosting service required
- **Self-Destruct Mechanism**: Time-based payload auto-removal (e.g., 1 hour) from Supabase for complete trace eradication
- **Zero-Width Filename Trick**: Disguises malicious .desktop launchers as legitimate PDF files using invisible Unicode characters
- **One-Line Generation**: Produces a single executable script — ready to deploy without additional setup
- **Zero-Dependency Architecture**: Pure Python implementation with no external libraries required beyond standard modules

### Use Cases:
- Security research and malware analysis
- Penetration testing and red team operations
- Evasion technique development
- Educational purposes in cybersecurity

### INSTALLATION
    git clone https://github.com/0xbitx/DEDSEC_PWN2PDF.git
    cd DEDSEC_PWN2PDF
    chmod +x dedsec-pwn2pdf
    sudo ./dedsec-pwn2pdf
    
### TESTED ON FOLLOWING
* Kali Linux 
* Parrot OS 
  
## Legal Disclaimer

This tool is intended for educational and security research purposes only. Unauthorized usage may be illegal in your jurisdiction. The author is not responsible for any misuse of this tool.
