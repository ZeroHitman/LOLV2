![LOLV2](logo.png)

LOLV2 — Recon & Detection Toolkit
================================

🔍 **LOLV2** is a CLI-based reconnaissance and detection toolkit designed to identify  
misconfigurations, sensitive endpoints, and exposed web services **at scale**.

LOLV2 focuses on **visibility and discovery**, not exploitation.

------------------------------------------------------------

🎯 FOCUS
--------

✔ Recon & Detection  
✖ No exploitation  
✖ No brute-force  
✖ No auto-dump  
✖ No privilege escalation  

Designed for:
- Security reconnaissance
- Exposure assessment
- Pre-exploitation validation
- Blue team & defensive audits

------------------------------------------------------------

⚙️ INSTALLATION
---------------

📥 Download binary:

```bash
wget https://raw.githubusercontent.com/ZeroHitman/LOLV2/refs/heads/main/lolv2 -O lolv2
chmod +x lolv2
```

▶ Run:

```bash
./lolv2 -h
```

📌 Optional (system-wide):

```bash
sudo mv lolv2 /usr/local/bin/lolv2
```

------------------------------------------------------------

🚀 USAGE
--------

📂 Scan list of targets:

```bash
lolv2 -l targets.txt
```

🌐 Scan single URL:

```bash
lolv2 -u https://example.com
```

🧩 Verbose mode:

```bash
lolv2 -l targets.txt -v
```

🔄 Update internal httpx engine:

```bash
lolv2 --updateHttpx
```

------------------------------------------------------------

📁 OUTPUT STRUCTURE
------------------

Results are stored **per target list**, following the executing user:

```text
~/result_lolv2/targets.txt/
├── phpinfo.txt
├── phpmyadmin.txt
├── laravel_env.txt
├── jenkins.txt
└── ...
```

Rules:
- 1 menu = 1 output file
- Full URL + metadata preserved
- No alive check performed
- Errors do not interrupt scan flow

------------------------------------------------------------

🧠 DETECTION MODULES
-------------------

• Laravel Ignition Execute  
• Laravel .env exposure  
• Laravel Logout (Whoops)  
• Laravel Log (MySQL)  
• Laravel Log (PostgreSQL)  
• phpMyAdmin  
• phpPgAdmin  
• phpinfo  
• .git directory exposure  
• .svn directory exposure  
• .hg directory exposure  
• CMS configuration backups  
• sftp.json exposure  
• Jenkins Groovy Script Console  
• react2shell (RSC detection)  

Each module:
- Uses signature-based detection
- Executes all rules in one run
- Produces a single output file

------------------------------------------------------------

🖼 SCREENSHOTS
--------------

![LOLV2](lolv2.png)

------------------------------------------------------------

⚠️ DISCLAIMER
-------------

This tool is intended solely for legitimate security testing and educational purposes.  
It is **100% free**. Anyone selling this tool is a fool.

Any misuse, unauthorized scanning, or illegal activity using this tool  
is **the sole responsibility of the user**.

------------------------------------------------------------

👤 AUTHOR
--------

HITMAN  
Recon & Detection Toolkit  
https://github.com/ZeroHitman

------------------------------------------------------------

🛡 Philosophy
-------------

"Visibility first. Exploitation is optional."
