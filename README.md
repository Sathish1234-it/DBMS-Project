📘 E-Diary Web Application

A simple and user-friendly digital diary built using Flask and MySQL, where users can securely register, log in, write personal diary entries, edit them, and delete them.

🚀 Features

✔ User Registration & Login
✔ Secure session-based authentication
✔ Add diary entries
✔ View all personal entries
✔ Edit existing entries
✔ Delete entries
✔ Logout
✔ MySQL database integration
✔ Clean, simple UI (HTML + Bootstrap)

🛠 Tech Stack
Component	Technology
Backend	Python Flask
Database	MySQL
Frontend	HTML, CSS (Bootstrap)
Authentication	Flask Sessions
📂 Project Structure
/e-diary
│
├── app.py
├── requirements.txt
├── /templates
│     ├── login.html
│     ├── register.html
│     ├── view_entries.html
│     ├── add_entry.html
│     └── edit_entry.html
└── /static (optional for CSS/JS)

🗄️ Database Setup

Run this SQL in your MySQL:

CREATE DATABASE ediary;

USE ediary;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) UNIQUE,
    password VARCHAR(255)
);

CREATE TABLE entries (
    entry_id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT,
    title VARCHAR(255),
    content TEXT,
    entry_date DATE,
    FOREIGN KEY (user_id) REFERENCES users(id)
);

⚙️ Install Dependencies
pip install flask mysql-connector-python werkzeug

▶️ How to Run the Project

Open terminal in project folder

Run:

python app.py


Open the browser and go to:

http://127.0.0.1:5000

🔐 Security Notes

Use password hashing (generate_password_hash)

Never store plain-text passwords

Avoid hardcoding the database password

📌 Future Improvements (Optional)

Add profile page

Add image/file uploads

Add search option for entries

Dark/Light mode toggle

Export diary as PDF

Add category tags

🤝 Contributing

Feel free to fork this project and improve it!

📜 License

This project is free to use.
