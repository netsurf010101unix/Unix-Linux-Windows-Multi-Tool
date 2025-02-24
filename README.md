```bash
chmod +x vulnerability_scanner.sh
```

Run the script (Linux):

```bash
sudo ./vulnerability_scanner.sh
```

For **PowerShell** (Windows):

```powershell
powershell -ExecutionPolicy Bypass -File vulnerability_scanner.ps1
```

For **Windows Command Line (CMD):**

```cmd
vulnerability_scanner.bat
```

## Permission Management

To set **read-only** access:

```bash
chmod 444 vulnerability_scanner.sh
```

To allow **read & write** access:

```bash
chmod 644 vulnerability_scanner.sh
```

To allow **full execution permissions**:

```bash
chmod 755 vulnerability_scanner.sh
```

## Automated Execution

To schedule automatic execution, the script sets up a **cron job** (Linux) or **Task Scheduler job** (Windows):

```bash
crontab -l   # Linux
```

```powershell
Get-ScheduledTask   # Windows
```

## Log Encryption & Storage

Logs are encrypted using **AES-256** and stored securely:

```bash
/var/log/security_audit_secure/security_log.enc   # Linux
C:\Security_Audit\security_log.enc   # Windows
```

To decrypt logs:

```bash
openssl enc -aes-256-cbc -d -in /var/log/security_audit_secure/security_log.enc -out decrypted_log.txt -pass file:/etc/security_audit_key
```

```powershell
openssl enc -aes-256-cbc -d -in C:\Security_Audit\security_log.enc -out C:\Security_Audit\decrypted_log.txt -pass file:C:\Security_Audit\security_audit_key
```

## Contribution

This project is open-source! Contributions are welcome via **pull requests**.

**GitHub Repository:** [GitHub Link](https://github.com/your-username/Linux-Vulnerability-Scanner)
