
# Helpdesk Lab 2026 – Active Directory & System Administration

Hands-on virtual lab focused on core Helpdesk / IT Support skills using Windows Server 2022 and Windows 11.

## Lab Overview

This lab covers the full process of building and managing a small Active Directory environment, including user management, Group Policy, file shares, security, and patch management with Action1.

### Key Skills Demonstrated

- Active Directory Domain Services installation & configuration
- Windows 11 domain join
- User account creation and management
- Group Policy (password policy, account lockout, logon hours, desktop restrictions, wallpaper)
- Security Groups + NTFS & Share permissions
- Home folder / drive mapping
- Account lockout, expiration and unlock procedures
- Action1 for endpoint inventory and patch management

---

## Screenshots

### 1. Active Directory & Domain Setup

| Screenshot | Description |
|------------|-------------|
| ![AD DS Installed](.) | Active Directory Domain Services installed on Windows Server 2022 |
| ![Domain Controller](./02-Domain-Controller-SystemInfo.png) | Server confirmed as Primary Domain Controller (`axellab.test`) |
| ![AD Users](./03-AD-Users-Created.png) | Custom user accounts created in Active Directory |
| ![Win11 Domain Joined](./04-Windows11-Domain-Joined.png) | Windows 11 client successfully joined to the domain |
| ![Domain User Login](./05-Domain-User-Login.png) | Domain user logged in (`whoami`) |
| ![Computer Object](./06-Computer-Object-in-AD.png) | Windows 11 computer object visible in Active Directory |

### 2. Account Management & Security

| Screenshot | Description |
|------------|-------------|
| ![Logon Hours](./07-Logon-Hours-Configured.png) | Logon hours restricted via Active Directory |
| ![Time Restriction](./08-Time-Restriction-Error.png) | Login blocked due to logon hour restrictions |
| ![Account Expiration](./09-Account-Expiration-Set.png) | Account expiration date configured |
| ![Expired Error](./10-Account-Expired-Error.png) | Login blocked because the account has expired |
| ![Lockout Policy](./11-Account-Lockout-Policy.png) | Account lockout threshold and duration configured via GPO |
| ![Locked Out](./12-Account-Locked-Error.png) | Account locked after too many failed attempts |
| ![Account Unlocked](./13-Account-Unlocked.png) | Locked account successfully unlocked |
| ![Protect OU](./14-Protect-From-Accidental-Deletion.png) | Organizational Unit protected from accidental deletion |

### 3. Group Policy – Desktop Restrictions

| Screenshot | Description |
|------------|-------------|
| ![GPO Restrictions](./15-GPO-Remove-TaskManager-Logoff.png) | Group Policy configured to remove Task Manager, Change Password and Logoff |
| ![Restricted Ctrl+Alt+Del](./16-Ctrl-Alt-Del-Restricted.png) | Result: Only Lock and Switch user available |

### 4. File Shares, Permissions & Drive Mapping

| Screenshot | Description |
|------------|-------------|
| ![Home Folder Mapping](./17-Home-Folder-Mapping.png) | Home folder mapped to network path |
| ![Mapped Drive](./18-Mapped-Drive-on-Client.png) | Network drive successfully mapped on Windows 11 |
| ![Security Group](./19-Security-Group-Tech.png) | Security Group “Tech” created and Domain User added as member |
| ![NTFS Permissions](./20-NTFS-Permissions.png) | NTFS permissions configured on the Tech folder |
| ![Share Permissions](./21-Share-Permissions.png) | Share-level permissions granted to the Tech security group |

### 5. Group Policy – Wallpaper

| Screenshot | Description |
|------------|-------------|
| ![Wallpaper GPO](./22-Wallpaper-GPO-Configured.png) | Desktop wallpaper deployed via Group Policy |
| ![Wallpaper Applied](./23-Wallpaper-Applied.png) | Custom wallpaper successfully applied on client |

### 6. Action1 Patch Management

| Screenshot | Description |
|------------|-------------|
| ![Action1 Endpoints](./24-Action1-Endpoints.png) | Both Windows 11 and Windows Server 2022 managed in Action1 |
| ![Patch Deployment](./25-Action1-Patch-Deployment.png) | Critical updates successfully deployed via Action1 |

---

## Environment

- **Domain Controller**: Windows Server 2022
- **Client**: Windows 11
- **Domain**: `axellab.test`
- **Tools used**: Active Directory Users and Computers, Group Policy Management, Action1, File Shares

---

*Lab completed as part of Helpdesk Lab 2025 series.*
