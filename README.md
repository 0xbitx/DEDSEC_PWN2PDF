
<p align="center">
<img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExNWMybWZkc3B4dzBwYzFxM2JtY213aG14Nml2cXAwYXNpeWY0ODh3eiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/sMiP6YqCIyPCfshhyU/giphy.gif", width="400", height="400">
</p>

<h1 align="center">PWN2PDF</h1>
<h4 align="center">A Linux based tool that Disguises your payload as a PDF to silently execute on a linux system.
</h4>

### DESCRIPTION

PWN2PDF is a Linux-based red team tool. It generates a malicious desktop launcher that is disguised as a standard PDF file. When an unsuspecting victim double-clicks the file, their system interprets it as a .desktop application rather than a genuine PDF. The launcher then performs two actions simultaneously: it downloads and opens a legitimate PDF document to maintain the illusion of normal behavior, while silently fetching and executing an attacker-supplied payload in the background. This allows the payload to run without disrupting the victim's experience, as the real PDF captures their attention. The tool is intended for use only in controlled environments with explicit written permission.


### Key Features:

- **Multiple Payload Support**: Supports binary, bash, python, reverse shell, and Metasploit payloads
- **Controlled Payload Hosting**: Integrated Supabase file upload system for controlled database
- **Zero-Dependency Architecture**: Pure Python implementation with no external libraries required beyond standard modules

## SETUP SUPABASE

   * Go to: https://supabase.com/dashboard/new

<img width="714" height="492" alt="Screenshot_20260505_093635" src="https://github.com/user-attachments/assets/d2a58e19-63bf-4210-adf5-ba09a8a2aca6" />
    
   * Create organization (org, personal)

<img width="722" height="896" alt="Screenshot_20260505_093758" src="https://github.com/user-attachments/assets/eb83c347-bb2f-49d3-94f8-2d08b286faa4" />

   * enable (Enable Data API) and (Automatically expose new tables)

<img width="926" height="540" alt="Screenshot_20260505_093835" src="https://github.com/user-attachments/assets/24b60cfe-da7d-44c9-82b4-b49edcf983f1" />

   * Copy Product URL and Publishable Key

<img width="980" height="617" alt="Screenshot_20260505_093921" src="https://github.com/user-attachments/assets/06c1cec9-f365-4140-b78a-2606f5cb9bf1" />

   * Go to Project Settings
     
<img width="714" height="625" alt="Screenshot_20260505_093948" src="https://github.com/user-attachments/assets/f77b1040-866c-4fa3-8133-e67f882b8199" />
   
   * select API Keys

<img width="1201" height="573" alt="Screenshot_20260505_094048" src="https://github.com/user-attachments/assets/3db41af1-f001-4afb-bcc4-fc7f947e8eac" />

   * Copy Service role secret
     
<img width="675" height="622" alt="Screenshot_20260505_094138" src="https://github.com/user-attachments/assets/57899895-0d1a-4f33-bcbd-6f6c552e9cd3" />

   * Go to Storage
     
<img width="1152" height="486" alt="Screenshot_20260505_094209" src="https://github.com/user-attachments/assets/5a5ea812-2d0f-44f0-954d-b874ace983e4" />
   
   * click New bucket

<img width="571" height="633" alt="Screenshot_20260505_094346" src="https://github.com/user-attachments/assets/4abf1a4f-7537-4dcd-8c45-3458aa398cbf" />

   * Put "data" as the bucket name, enable public bucket, and click Create.

and update your config.json file with your 
Project URL, Publishable key, service role secret

### Example:
```json
{
    "SUPABASE_URL": "https://gqbdetbewhevkksclbfu.supabase.co",
    "SUPABASE_KEY": "sb_publishable_TvQ2jFqzrPfsKC-krVrwqA_g_xjy9GM",
    "SUPABASE_SERVICE_KEY": "eyJHbgcrOeJIUsI2NiIsInR3cCI6IkpXcCJ9.eyJpc311OilzeXBhymFrZSIsInJlZiI6ImdxYmR5dGJld2hpdmtrZWNsYmd14iwicm9sZSI6InNlcnZpY2Vfcm9sZSIs3mlhdCI2MTc3NzkyMDk4OCwiZXhwIjoyMDkzNDk2OTg4fQ.L4wdbD3QgDv2NHlP6ZU53wpI2jlLZ0TQXfq6vy7VB_A"
}
```

### INSTALLATION
    git clone https://github.com/0xbitx/DEDSEC_PWN2PDF.git
    cd DEDSEC_PWN2PDF
    chmod +x dedsec-pwn2pdf
    ./dedsec-pwn2pdf
    
### TESTED ON FOLLOWING
* Kali Linux 
* Parrot OS 
  
## Legal Disclaimer

This tool is intended for educational and security research purposes only. Unauthorized usage may be illegal in your jurisdiction. The author is not responsible for any misuse of this tool.
