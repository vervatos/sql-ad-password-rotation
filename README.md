# sql-ad-password-rotation
PowerShell script to automate monthly password changes for SQL Server logins and Active Directory service accounts, with logging and email notifications
# SQL & AD Password Rotation Script

## Overview
This PowerShell script automates monthly password changes for:
- SQL Server logins
- Active Directory (AD) service accounts

### Features:
✅ Generates secure random passwords  
✅ Updates SQL Server login passwords via `ALTER LOGIN`  
✅ Updates AD service account passwords via `Set-ADAccountPassword`  
✅ Logs all changes for audit purposes  
✅ Sends an email notification with a summary  

## Usage
### 1️⃣ Prerequisites:
- Ensure you have `Invoke-Sqlcmd` and the **Active Directory module** installed.
- Run the script with an account having **SQL sysadmin & AD admin** rights.
- Update the **SMTP settings** for email notifications.

### 2️⃣ Running the Script:
```powershell
powershell -ExecutionPolicy Bypass -File ChangePasswords.ps1
