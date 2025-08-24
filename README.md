# Basic PHP CRUD App with Authentication (MySQL)

## What this includes
- User registration & login (password hashing with `password_hash`)
- Create, Read, Update, Delete posts
- Session-based auth (only logged-in users can create/edit/delete)
- PDO + prepared statements
- Minimal Bootstrap for quick styling

## Prerequisites
- PHP 8+ with PDO MySQL extension
- MySQL 5.7+/MariaDB 10+
- A web server (Apache, Nginx) or PHP built-in server

## Setup
1. Create the database and tables:
   ```sql
   SOURCE db.sql;
   ```

2. Update DB credentials in `config.php`:
   ```php
   $DB_HOST = "127.0.0.1";
   $DB_NAME = "blog";
   $DB_USER = "root";
   $DB_PASS = "";
   ```

3. Start a server:
   - Built-in PHP server (from project root):  
     ```bash
     php -S localhost:8000
     ```
   - Or configure Apache/Nginx to point to this folder.

4. Open in your browser:
   - `http://localhost:8000/`

## Default pages
- `/` — Posts list
- `/register.php` — Register
- `/login.php` — Login
- `/logout.php` — Logout
- `/create.php` — New post (requires login)
- `/edit.php?id=...` — Edit post (requires login)
- `/delete.php` — Delete post (requires login; POST only)

## Notes
- This is a teaching/demo project. For production, add CSRF tokens, stronger validation, and stricter error handling.
