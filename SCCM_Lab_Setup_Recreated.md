# SCCM Lab Setup Documentation

## Lab Overview
This lab was built using a personal server equipped with a **Xeon processor** and **128GB RAM**.  
VMware vSphere was used to host the virtual machines.

---

## Virtual Machines and IP Addresses

| VM Name            | IP Address     | Role                             |
|--------------------|----------------|----------------------------------|
| SCCM Server        | 192.168.81.133  | Primary Site Server             |
| Domain Controller  | 192.168.81.30   | Active Directory + DNS Server   |
| Distribution Point | 192.168.81.60   | Distribution Point and Management Point |
| Windows 11 Client  | 192.168.81.50   | Client PC                        |

---

## Major Setup Steps
1. Installed Windows Server 2022 and Windows 11 on VMs.
2. Promoted Domain Controller (LAB-DC01) and configured DNS.
3. Installed SQL Server and SCCM on Lab-CM01.
4. Configured Distribution Point (Lab-GW01).
5. Installed SCCM Client on Windows 11 Client (WINCL01).
6. Integrated on-prem Active Directory with Azure Active Directory using Microsoft Entra Connect.
7. Set up Co-Management between SCCM and Intune.
8. Captured screenshots and documented troubleshooting steps.

---

## Key Troubleshooting
- **WMI and firewall issues** during client push — resolved by enabling WinRM and firewall ports.
- **DNS misconfigurations** corrected — domain join and SCCM communication established.
- **Azure AD Connect** permissions issue — resolved by adding user to **Enterprise Admins** group.
- **Client push installation failures** — resolved through administrative shares, firewall exceptions, and DNS checks.

---

## GitHub Instructions
If you want to import this file into GitHub:

1. Create a new repository on [GitHub](https://github.com/).
2. Name it something like `SCCM-Lab-With-Azure-Integration`.
3. Click **"Add file"** → **"Create new file"** → name the file `README.md`.
4. Paste this content into the editor.
5. Commit the new file to `main` branch.

GitHub will automatically format it beautifully.

---
