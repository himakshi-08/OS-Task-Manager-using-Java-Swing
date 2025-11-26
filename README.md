# Advanced Task Manager (Java Desktop Application)

This project is a simple desktop-based **Task Manager tool** created using **Java Swing**.  
It allows users to view running processes, check CPU and memory usage, search for specific processes, refresh the list, and terminate processes directly from the interface.

---

## 🚀 Features

### ✔ View Running Processes
Displays:
- **PID**
- **Process Name**
- **CPU Usage (%)**
- **Memory Usage (MB)**

### 🔍 Search Function
- Search using **process name** or **PID**.
- Filters the table to show only matching processes.

### ❌ Kill Process
- Select any process in the table and click **Kill Process** to terminate it.
- Uses the `taskkill` command internally.

### 🔄 Refresh
- Reloads the complete list of running processes.

### 🧹 Clear Search
- Clears the search box.
- Reloads the full process list automatically.

---

## 🛠 Technologies Used

- **Java (JDK 8 or above)**
- **Java Swing** (GUI)
- **PowerShell Commands** (for fetching process details)
- **JTable + DefaultTableModel** (for displaying data)

---

## 📥 How It Works

The application internally runs the following PowerShell command:
Get-Process | Select-Object Name,Id,CPU,WorkingSet

It extracts:
- `Name` → Process Name  
- `Id` → PID  
- `CPU` → CPU usage  
- `WorkingSet` → Memory usage (converted from bytes → MB)

These values are formatted and displayed in a table.

---

## ▶ How to Run the Application

1. Install **Java 8+** on your system.
2. Save the project file:


3. Open a terminal in the same directory and run:

```sh
javac TaskManager.java
java TaskManager
