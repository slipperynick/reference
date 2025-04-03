# Microsoft Graph CLI (`mgc`) Commands

---

## 📂 **Resources**
- [Samples](https://github.com/microsoftgraph/msgraph-cli/tree/main/samples) – Example usage of `mgc`
- [Releases](https://github.com/microsoftgraph/msgraph-cli/releases) – Latest CLI updates

---

## 🔑 **Authentication Commands**
- `mgc --help` – Show the help menu
- `mgc login` – Log in to Microsoft Graph
- `mgc logout` – Log out of the current session
- `mgc login --scopes user.read.all` – Log in with specific permission scopes
- `mgc login --strategy InteractiveBrowser --client-id [id] --tenant-id [tenant] --scopes Directory.AccessAsUser.All` – Log in using **Interactive Browser Authentication**

---

## 👥 **User Management**
- `mgc users list --output table` – List all users in a table format
- `mgc users list --query` – List users with a specific query
- `mgc me get --output table` – Get details of the currently logged-in user
- `mgc organization list --output table` – Get organization details
- `mgc users list --select "id, displayName, OfficeLocation, BusinessPhones"` – Retrieve specific user details

---

## 💻 **Device Management**
- `mgc device-management managed-devices list` – List all managed devices

---

