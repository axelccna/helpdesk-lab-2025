# Helpdesk Lab 2026 – Active Directory & System Administration

Hands-on virtual lab focused on core Helpdesk / IT Support skills using Windows Server 2022 and Windows 11.

## Lab Overview

This lab covers building and managing an Active Directory environment, including user management, Group Policy, file shares, security settings, and patch management with Action1.

### Key Skills Demonstrated

- Active Directory installation and management
- Windows 11 domain join
- User account creation and management
- Group Policy (account lockout, logon hours, desktop restrictions)
- Security Groups + NTFS & Share permissions
- Home folder / drive mapping
- Account lockout and unlock procedures
- Action1 endpoint management and patch deployment

---

## Screenshots

### 1. Active Directory & Domain Setup

| Screenshot | Description |
|------------|-------------|
| ![AD Installed](./screenshots/1.%20AD%20installed%20on%20win2022%20server.png) | Active Directory Domain Services installed on Windows Server 2022 |
| ![System Info](./screenshots/2.%20sysinfo%20win2022%20server.png) | Server configured as Primary Domain Controller |
| ![AD Users](./screenshots/3.%20AD%20user%20created.png) | Custom user accounts created in Active Directory |
| ![Win11 Domain Joined](./screenshots/4.win11vm%20joined%20to%20domain.png) | Windows 11 client successfully joined to the domain |
| ![Domain User Login](./screenshots/5.%20win11%20whoami%20showing%20testuser%20joined%20to%20domain.png) | Domain user logged in |

### 2. Account Management & Security

| Screenshot | Description |
|------------|-------------|
| ![Logon Hours](./screenshots/11.setting%20logon%20hours%20deniying%20login.png) | Logon hours restricted |
| ![Time Restriction](./screenshots/12.showing%20time%20restriction%20login%20message%20after%20setting%20the%20logon%20hours.png) | Login blocked due to time restrictions |
| ![Lockout Policy](./screenshots/17.changed%20account%20lockout%20duration%20and%20threshold%20under%20domain%20policy.png) | Account lockout policy configured via GPO |
| ![Locked Out](./screenshots/18.%20account%20locked%20out%20after%20too%20many%20attempts.png) | Account locked after failed login attempts |
| ![Account Unlocked](./screenshots/unlocking%20the%20testusers%20account%20.png) | Locked account successfully unlocked |

### 3. Group Policy – Desktop Restrictions

| Screenshot | Description |
|------------|-------------|
| ![GPO Restrictions](./screenshots/change%20password%20task%20manager%20remove%20logoff%20group%20policy%20setting.png) | Group Policy used to remove Task Manager, Change Password and Logoff |
| ![Restricted Screen](./screenshots/removed%20task%20manager%20change%20password%20and%20signout%20in%20group%20policy.png) | Result after applying the GPO |

### 4. File Shares & Permissions

| Screenshot | Description |
|------------|-------------|
| ![Security Group](./screenshots/Security%20Group%20“Tech”%20with%20Domain%20User%20as%20member.png) | Security Group created and user added |
| ![NTFS Permissions](./screenshots/NTFS%20permissions%20on%20tech%20folder.png) | NTFS permissions configured |
| ![Mapped Drive](./screenshots/mapped%20network%20drive%20tech%20Z%20on%20win11vm.png) | Network drive successfully mapped on Windows 11 |

### 5. Action1 Patch Management

| Screenshot | Description |
|------------|-------------|
| ![Action1 Endpoints](./screenshots/win11vm%20and%20win2022%20server%20seen%20as%20connected%20in%20action1.png) | Endpoints managed in Action1 |
| ![Patch Deployment](./screenshots/basicly%20patch%20deployment%20status%20for%20the%20win2022vm%20in%20action1.png) | Updates successfully deployed via Action1 |

---

## Environment

- **Domain Controller**: Windows Server 2022  
- **Client**: Windows 11  
- **Domain**: `axellab.test`  
- **Tools**: Active Directory, Group Policy Management, Action1

---


