# Employee-mgt.-system
# Employee Management System (PyQt5)



A comprehensive desktop application for managing employee records with a modern UI and secure database integration.


## Features

- **CRUD Operations**:
  - Add new employees with validation
  - Update existing records
  - Delete employees with confirmation
  - View detailed profiles
- **Employee Directory**:
  - Search/filter by name, email, or designation
  - Sortable columns
  - Action buttons for quick operations
- **Database Management**:
  - Automatic database setup
  - Sample data generation
  - Secure MySQL connection
- **Modern UI**:
  - Welcome dashboard with feature highlights
  - Responsive layout
  - Themed interface with dark/light modes
- **Help System**:
  - About application
  - Developer information
  - Database connection details

## Tech Stack

- **Frontend**: PyQt5
- **Backend**: Python 3.8+
- **Database**: MySQL
- **Dependencies**: 
  - `mysql-connector-python`
  - `PyQt5`

## Installation

### Prerequisites
- Python 3.8+
- MySQL Server
- Git

### Setup Steps:
```bash
# Clone repository
git clone https://github.com/yourusername/employee-management-system.git
cd employee-management-system

# Install dependencies
pip install -r requirements.txt

# Configure MySQL:
# 1. Create a user with privileges:
#    CREATE USER 'emp_user'@'localhost' IDENTIFIED BY 'securepassword';
# 2. Grant privileges:
#    GRANT ALL PRIVILEGES ON employee.* TO 'emp_user'@'localhost';

# Run application
python main.py

Database Configuration
The application automatically:

Creates employee database

Generates emp table structure

Seeds sample data if empty

Edit connection parameters in the MainWindow class if needed:
conn = mysql.connector.connect(
    host='localhost',
    user='emp_user',
    password='securepassword',
    database='employee'
)

Usage
Main Menu:

Navigate through sections using toolbar icons

Access help documentation from menu bar

Employee Management:

Add: Complete all required fields

Update: Search by ID first

Delete: Confirmation dialog appears

Directory Features:

Click column headers to sort

Use search bar for filtering

Action buttons per row for quick operations

**Project Structure**
├── main.py             # Application entry point
├── database_setup.py   # DB initialization script
├── requirements.txt    # Dependencies
├── modules/
│   ├── ui_welcome.py   # Welcome screen
│   ├── ui_add.py       # Add employee UI
│   ├── ui_update.py    # Update employee UI
│   ├── ui_view.py      # Profile viewer
│   └── ui_list.py      # Employee directory
└── icons/              # Toolbar icons

PyQt5==5.15.7
mysql-connector-python==8.0.28
