# Inventory Management System (Desktop Application)

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Tkinter](https://img.shields.io/badge/GUI-Tkinter-green)](https://docs.python.org/3/library/tkinter.html)
[![Database](https://img.shields.io/badge/Database-SQLite-lightgrey)](https://www.sqlite.org/index.html)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-informational)]()

A secure, role-based **Inventory & Asset Management System** built using Python, Tkinter, and SQLite. Designed for industrial and enterprise use, this application features a clean desktop interface, complete audit logging, and expiry tracking, making it suitable for deployment as a standalone Windows EXE.

---

🚀 Features

 🔐 Authentication & Roles
* **Secure Login:** SHA-256 hashed password system.
* **Setup Wizard:** Automatic "First-run" Admin setup.
* **Role-Based Access Control (RBAC):**
    * **Admin:** Full control (Manage users, inventory, view logs).
    * **User:** Operational access (Add/Edit inventory, restricted delete).

### 📦 Inventory Management
* Add, Edit, and Delete (Admin only) asset records.
* **Track Key Metrics:**
    * Item Name & Serial/Reference Number.
    * Category, Department, and Location.
    * Supplier/Vendor details.
    * Expiry Dates.

### ⏰ Expiry Monitoring
* Centralized dashboard for inventory health.
* dedicated view for expired items.
* **Alert System:** View items expiring within the next 30 days.

### 👥 User Management (Admin)
* Create and remove user accounts.
* Assign roles (Admin/User).
* Reset credentials.
* Full traceability of user actions.

### 🧾 Audit & Logs
* **Immutable Logging:** Every action is timestamped and stored.
* **Tracked Events:** Login/Logout, Inventory changes (Add/Edit/Delete), User creation/updates.

### 🖥️ Desktop UI
* Clean, sidebar-based navigation.
* Optimized for Windows desktop environments.
* **Offline First:** No internet dependency required.

---

## 🛠️ Technology Stack

* **Language:** Python 3.10+
* **GUI Framework:** Tkinter (Native Python UI)
* **Database:** SQLite (Embedded, serverless)
* **Security:** SHA-256 Password Hashing
* **Architecture:** Modular (Separation of Concerns: UI, Auth, DB, Logic)

## 📁 Project Structure

```text
ims/
│
├── main.py                # Application entry point
├── database.py            # Database initialization & helpers
├── auth.py                # Authentication & user management
├── logs.py                # Audit logging
│
├── ui/
│   ├── login.py           # Login screen
│   ├── setup_admin.py     # First-run admin setup
│   ├── dashboard.py       # Main dashboard
│   ├── inventory.py       # Inventory views
│   ├── add_item.py        # Add inventory form
│   ├── users.py           # User management (admin)
│   └── activity_logs.py   # Logs viewer
│
└── assets.db              # SQLite database (auto-generated)

```

▶️ How to Run (Development)
Prerequisites
Python 3.10 or later.

Tkinter (Usually bundled with standard Python installations on Windows/macOS).

Steps
Clone the repository or download the source code.

Navigate to the project directory.

Run the application:

Bash

```python main.py```

or


```python3 main.py```


Note: On the very first launch, the application will detect a fresh install and prompt you to create the Master Admin Account.


> **Note:** On the very first launch, the application will detect a fresh install and prompt you to create the **Master Admin Account**.

---

## 📦 Building for Windows (Production)

This application is optimized to be packaged as a standalone `.exe` using PyInstaller.

1. **Install PyInstaller:**
```bash
pip install pyinstaller

```


2. **Build the Executable:**
```bash
pyinstaller --onefile --windowed --name="InventorySystem" main.py

```


3. **Locate the File:**
The resulting `.exe` will be found in the `dist/` folder. This file is portable and can be distributed to client machines.

---

## 🔐 Security Notes

* **Password Safety:** Passwords are salted and hashed using SHA-256; they are never stored in plain text.
* **Data Privacy:** The SQLite database is stored locally (`assets.db`), ensuring data remains offline and within the organization's network.
* **Network:** No external network calls or cloud dependencies.

---

## 📈 Use Cases

* **Manufacturing:** Raw material and spare parts tracking.
* **Industrial:** Asset compliance and machinery maintenance logs.
* **Enterprise:** Internal IT asset management.
* **Retail/Pharma:** Expiry date monitoring for perishable goods.

---

## 🔧 Roadmap & Future Enhancements

* [ ] **Data Export:** Generate CSV/PDF reports for audits.
* [ ] **Backup System:** Integrated database backup and restore tools.
* [ ] **Licensing:** License key enforcement and activation system.
* [ ] **Installer:** Create a standard Windows Setup Wizard (MSI/Inno Setup).
* [ ] **UI Customization:** Dark Mode support.

---

## 👨‍💻 Credits

**Designed and Developed by Harsh**



### Next Steps for you

The README mentions "Future Enhancements" that you are considering. Would you like me to help you implement the **Export to CSV/PDF** feature next, or should we work on the **License Key/Activation system** to make it commercial-ready?
