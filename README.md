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
| ![AD Installed](./1.%20AD%20installed%20on%20win2022%20server.png) | Active Directory Domain Services installed on Windows Server 2022 |
| ![System Info](./2.%20sysinfo%20win2022%20server.png) | Server confirmed as Primary Domain Controller (`axellab.test`) |
| ![AD Users](./3.%20AD%20user%20created.png) | Custom user accounts created in Active Directory |
| ![Win11 Domain Joined](./4.win11vm%20joined%20to%20domain.png) | Windows 11 client successfully joined to the domain |
| ![Domain User Login](./5.%20win11%20whoami%20showing%20testuser%20joined%20to%20domain.png) | Domain user logged in (`whoami`) |
| ![Computer Object](./6.win11%20machine%20joined%20to%20AD%20domain.png) | Windows 11 computer object visible in Active Directory |

### 2. Account Management & Security

| Screenshot | Description |
|------------|-------------|
| ![Logon Hours](./11.setting%20logon%20hours%20deniying%20login.png) | Logon hours restricted via Active Directory |
| ![Time Restriction](./12.showing%20time%20restriction%20login%20message%20after%20setting%20the%20logon%20hours.png) | Login blocked due to logon hour restrictions |
| ![Account Expiration](./13.%20setting%20account%20expiration%20date.png) | Account expiration date configured |
| ![Expired Error](./14.%20the%20users%20account%20has%20expired%20login%20error.png) | Login blocked because the account has expired |
| ![Lockout Policy](./17.changed%20account%20lockout%20duration%20and%20threshold%20under%20domain%20policy.png) | Account lockout threshold and duration configured via GPO |
| ![Locked Out](./18.%20account%20locked%20out%20after%20too%20many%20attempts.png) | Account locked after too many failed attempts |
| ![Account Unlocked](./unlocking%20the%20testusers%20account%20.png) | Locked account successfully unlocked |
| ![Protect OU](./accessed%20object%20protection%20setting.png) | Organizational Unit protected from accidental deletion |
| ![Account Disabled](./10.testuser%20profile%20acount%20disabled%20login%20error.png) | Account disabled login error |

### 3. Group Policy – Desktop Restrictions

| Screenshot | Description |
|------------|-------------|
| ![GPO Restrictions](./change%20password%20task%20manager%20remove%20logoff%20group%20policy%20setting.png) | Group Policy configured to remove Task Manager, Change Password and Logoff |
| ![Restricted Screen](./removed%20task%20manager%20change%20password%20and%20signout%20in%20group%20policy.png) | Result: Only Lock and Switch user available |

### 4. File Shares, Permissions & Drive Mapping

| Screenshot | Description |
|------------|-------------|
| ![Home Folder Mapping](./mapping%20domain%20user%20profile%20to%20P%20networkpath%20and%20shared%20personal%20folder.png) | Home folder mapped to network path |
| ![Mapped Drive P](./personal%20network%20path%20on%20win11%20VM.png) | Personal network drive visible on Windows 11 |
| ![Mapped Drive Tech](./mapped%20network%20drive%20tech%20Z%20on%20win11vm.png) | Tech network drive mapped on Windows 11 |
| ![Security Group](./Security%20Group%20“Tech”%20with%20Domain%20User%20as%20member.png) | Security Group “Tech” created and Domain User added as member |
| ![NTFS Permissions](./NTFS%20permissions%20on%20tech%20folder.png) | NTFS permissions configured on the Tech folder |
| ![Share Permissions](./read%20write%20share%20folder%20permissions%20to%20tech%20security%20group.png) | Share-level permissions granted to the Tech security group |

### 5. Group Policy – Wallpaper

| Screenshot | Description |
|------------|-------------|
| ![Wallpaper GPO](./set%20desktop%20wallpaper%20in%20group%20policy%20after%20sharing%20wallpaper%20in%20shared%20folder.png) | Desktop wallpaper deployed via Group Policy |
| ![Wallpaper Applied](./domainuser%20on%20win11vm%20having%20the%20shared%20wallpaper%20from%20the%20policy%20and%20shared%20folder.png) | Custom wallpaper successfully applied on client |
| ![Wallpaper File](./showing%20the%20open%20shared%20folder%20with%20the%20wallpaper%20and%20it%20being%20set%20sucessfully%20.png) | Wallpaper file accessible from shared folder |

### 6. Action1 Patch Management

| Screenshot | Description |
|------------|-------------|
| ![Action1 Endpoints](./win11vm%20and%20win2022%20server%20seen%20as%20connected%20in%20action1.png) | Both Windows 11 and Windows Server 2022 managed in Action1 |
| ![Patch Deployment](./basicly%20patch%20deployment%20status%20for%20the%20win2022vm%20in%20action1.png) | Critical updates successfully deployed via Action1 |

---

## Environment

- **Domain Controller**: Windows Server 2022
- **Client**: Windows 11
- **Domain**: `axellab.test`
- **Tools used**: Active Directory Users and Computers, Group Policy Management, Action1, File Shares

---

