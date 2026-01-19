# Microsoft-Entra-PIM-MFA-enforcement-SAML-integration-and-IAM-auditing.
Microsoft Entra PIM, MFA enforcement, SAML integration, and IAM auditing.

# Lab Objective
- Just-in-Time (JIT) privilege elevation
- Role-based access control (RBAC)
- Secure authentication practices
- Auditing and monitoring access

# Tasks

- Task 1: Enable Privileged Identity Management (PIM) 
- Task 2: Configure PIM Role Activation & Approval Flow 
- Task 3: Integrate Enterprise App with Entra ID via SAML 
- Task 4: Automate Access Reviews in PIM
- Task 5: Audit and Monitor IAM Activities in Entra ID
- Task 6: Setup Bitwarden Password Collection
- Task 7: Enforce MFA for Bitwarden Access

# Task 1: Enable Privileged Identity Management (PIM)

## 🎯 Objective

Enable Just-in-Time (JIT) elevation in **Microsoft Entra PIM** for the following roles:

| Role Name              | Purpose                           |
|------------------------|-----------------------------------|
| Exchange Administrator | Manage Exchange Online settings   |
| Teams Administrator    | Manage Microsoft Teams services   |
| Security Administrator | Manage security-related features  |

This minimizes standing admin privileges and reduces risk of privilege abuse 

## Steps Taken

1. Logged in to Microsoft Entra Admin Center  
2. Navigated to **Privileged Identity Management** → **Microsoft Entra roles**  
3. Enabled **PIM** for the selected roles  
4. Assigned user as **Eligible** (not Active) with a **Permanent assignment**

## Key Concepts
- JIT Access - Grant roles onnly when needed
- Eligble - Requires users to request access
- PIM - Provides access control, auditability, and time limits

<img width="1703" height="899" alt="MS Entra" src="https://github.com/user-attachments/assets/db021a7c-3590-4f6e-a230-67a8c7c29f94" />

**![PIM Role Enabled]**
<img width="1508" height="906" alt="Screenshot 2026-01-19 090310" src="https://github.com/user-attachments/assets/f70af4f2-f966-41ce-a737-d743f0aed155" />

## Task 2 Configure PIM Role Activation & Approval Flow 
## 🎯 Objective
Strenghten access control by requiring **aproval**, **MFA**, and **justification** before activating privileged role (JIT Model). 

##Steps Taken
1. **Navigated to each role in:**
   
 ○ Microsoft Entra Admin Center > Privileged Identity Management > Microsoft Entra roles
   
2. **Selected Roles:**
   
  ○ Exchange Administrator  
  ○ Teams Administrator  
  ○ Security Administrator  

 3. **Role Settings Configuration:**
   
  ○ Opened **Role Settings** for each selected role   
  ○ Enabled **MFA required to activate**  
  ○ Enabled **Justification required**    
  ○ Enabled **Approval required**  
  ○ Selected a **test user/admin** as the approver  
  ○ Set **Activation duration** to **1 hour**  
##

 ## <img width="728" height="894" alt="MS Entra 3" src="https://github.com/user-attachments/assets/efebf052-f85f-4641-9f9f-158f0673cbda" />

## Key Concepts ##
- Aproval workflow ensures that elevated access isn't automatic. 
- MFA & justification add layered verification and traceability. 
- Time-bound access limits security exposure.
## ## 
![ Role Activation Settings]
  <img width="1273" height="899" alt="MS Entra 4" src="https://github.com/user-attachments/assets/93f0cf9d-be1b-4da2-8287-b43b52cb1544" />

## Integrate Salesforce App with Entra ID via SAML 
# Objective ## 
Enable Single Sign On (SSO) for **Salesforce** using SAML 2.0 protcol with Entra ID as the identity Provider (IdP). ## 

**Steps Taken**
1. Navigated to: Microsoft Entra ID Admin Center > Enterprise Applications
2. Clicked " + **New Applications**," then searched and selected:
     o Salesforce
3. After app created, selected: **Single Sign On > SAML**
4. On SAML config page: Confirm Identity (Entity ID): https://saml.salesforce.com   && Reply URL (ACS):  https://<your-domain>.my.salesforce.com


<img width="1599" height="810" alt="image" src="https://github.com/user-attachments/assets/21b09644-1569-42b2-a77a-ab682818db89" />


   
