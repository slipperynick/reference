# 📜 GAM (Google Apps Manager) Command Reference


---

## 🔍 User & Domain Information

- `gam info user <email>` – Get detailed information about a specific user  
- `gam user <email> check serviceaccount` – Check service account permissions for a user  
- `gam version` – Display the installed version of GAM  
- `gam info domain` – Retrieve domain information  
- `gam whatis` – Get information about an email, group, or domain  

---

## 👤 User Management

- `gam create user <email>` – Create a new user  
- `gam update user <email>` – Update user details  
- `gam update user <email> suspended on` – Suspend a user  
- `gam update user <email> suspended off` – Unsuspend a user  
- `gam update user <email> password "<new_password>"` – Reset a user's password  
- `gam update user <email> changepassword on` – Force user to change password on next login  
- `gam update user <email> firstname <first> lastname <last>` – Change a user’s name  
- `gam delete user <email>` – Delete a user account  

---

## 📩 Email & Forwarding

- `gam all users print` – Print all users  
- `gam all users print >> allusers.txt` – Save all users to a text file  
- `gam user <email> show forwardingaddresses` – Show email forwarding settings  
- `gam user <email> add forwardingaddress <forwarding_email>` – Add a forwarding address  
- `gam user <email> delete forwardingaddresses <forwarding_email>` – Remove a forwarding address  
- `gam user <email> forward off` – Disable email forwarding  

---

## 📬 Gmail & Labels

- `gam user <email> filter subject "<subject>" label "<label>" archive` – Automatically label and archive emails based on subject  
- `gam user <email> print filters` – List all Gmail filters for a user  
- `gam user <email> delete filter <filter_id>` – Delete a Gmail filter  
- `gam all users print forwardingaddresses` – Print all users’ forwarding addresses  

---

## 📂 Google Drive Management

- `gam user <email> show drivefilelist` – List all files in a user’s Google Drive  
- `gam user <email> delete drivefile <file_id>` – Delete a file from Google Drive  
- `gam user <email> transfer drive <new_owner>` – Transfer Google Drive ownership  

---

## 🏢 Google Groups & Aliases

- `gam create group <group_email>` – Create a new Google Group  
- `gam info group <group_email>` – Get details about a Google Group  
- `gam update group <group_email> name "<New Group Name>"` – Update a group name  
- `gam delete group <group_email>` – Delete a Google Group  
- `gam print groups` – Print all Google Groups in the domain  
- `gam user <email> show aliases` – Show all aliases for a user  
- `gam user <email> add alias <alias_email>` – Add an alias to a user  
- `gam user <email> delete alias <alias_email>` – Remove an alias from a user  

---

## 📊 Reporting & Logs

- `gam report users` – Get user activity reports  
- `gam report admin` – Retrieve admin activity logs  
- `gam report drive` – Get Google Drive usage reports  
- `gam report usage parameters` – Show available reporting parameters  

---

## 🔧 Google Workspace Settings

- `gam print orgs` – List all organizational units (OUs)  
- `gam create org <org_unit_path>` – Create a new organizational unit  
- `gam update org <org_unit_path> name "<New Name>"` – Rename an organizational unit  
- `gam update org <org_unit_path> parent <parent_org_unit>` – Move an OU under a different parent  

---

## ❌ Uninstalling GAM

- `gam OAuth revoke` - revoke Oauth Access

## Additional commands

- `gam print licenses` – Print all Google Workspace licenses
- `gam update license` <license_id> user <email> – Assign a license to a user
- `gam update group` <group_email> add member <email> – Add a member to a group
- `gam update group` <group_email> remove member <email> – Remove a user from a group
- `gam print mobile` – Print a list of mobile devices in the domain
- `gam delete mobile` <device_id> – Remove a mobile device from Google Workspace


## Useful one liners

- `gam all users print > users.csv` - List all users and save to CSV
- `gam print users 2sv enrolled | grep 'no'` - Find users with 2-Step Verification disabled
- `gam all users update imap off` - Disable IMAP for all users