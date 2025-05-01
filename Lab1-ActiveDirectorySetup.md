# 🧪 Home Lab #1 – Active Directory Setup (Attempt)

## 🖥️ What I Tried
- Installed Windows Server 2016 in VirtualBox
- Installed the “Active Directory Domain Services” role
- Attempted to promote the server to a domain controller using PowerShell

## ⚠️ What Went Wrong
- Got repeated errors in PowerShell:
  - `Verification of prerequisites for Domain Controller promotion failed`
  - `'InstallDNS' was not recognized`
- Realized some issues were:
  - Misspelled parameters
  - Forgot to add a dot in the domain name
  - PowerShell is case-sensitive

## ✅ What I Learned
- Installing AD DS is step 1 — promoting it is step 2
- The domain name needs to be something like `homelab.local`
- Commands must be typed **exactly right** in PowerShell

## 📸 Screenshots (coming soon)
*I will upload images showing my PowerShell errors and setup progress*

## 🧠 Next Steps
- Fix the domain setup using the correct syntax:
Install-ADDSForest -DomainName homelab.local -InstallDNS:$true -Force:$true
- After reboot, create users in Active Directory
