# Vanshart Website

This repository contains the codebase for the Vanshart website. You can explore the website here: [vanshartandexport.com](https://vanshartandexport.com/) 

For security reasons, several sensitive files have been excluded from this repository. If you are cloning or pulling this repository to set it up locally, you will need to recreate these missing files.

## 🔒 Ignored & Sensitive Files

The following files are not included in this repository:
- The SQL database file (`vanshart.sql`)
- Database connection files (`dbconnection.php`)
- Dependencies (`node_modules`)

---

## 🛠️ How to Recreate the Missing Files

### 1. Database Connection Credentials

You need to manually create the database connection files. Create a file named `dbconnection.php` in the following locations:
- `admin/includes/dbconnection.php`
- `agms/admin/includes/dbconnection.php`
- `agms/includes/dbconnection.php`

**Content for `dbconnection.php`:**
```php
<?php
// Replace "localhost", "root", "", "vanshart" with your actual database host, username, password, and database name.
$con = mysqli_connect("localhost", "root", "", "vanshart");

if(mysqli_connect_errno()){
    echo "Connection Fail: " . mysqli_connect_error();
}
?>
```

### 2. Database Setup

The original `vanshart.sql` file was ignored as it contains the live data.
- To run this locally, you must create a MySQL database (e.g., named `vanshart`).
- If you need the tables, you will need to export a safe/development copy of the SQL schema from your original server or local setup and import it into your newly created database.

### 3. Node Modules (If applicable)

If you are working with the frontend/backend assets that use npm, simply run:
```bash
npm install
```
