# FlowTrack – The Ultimate Productivity Prank 🎭

**FlowTrack** is a Flask web application that looks and feels like a real productivity suite. Users can sign up, log in, and are greeted with a beautiful dashboard—until they realize it's an **April Fools' Day prank**. After login, the app reveals a playful jumpscare message: **"There's nothing in this app you fool – April FOOL!"**

> ⚠️ **Note:** This is a harmless joke. No user data is collected beyond what’s necessary for the login flow (usernames and hashed passwords are stored locally in an SQLite database). The prank is purely visual and resets on logout.

---

## 🚀 Features

- **Beautiful, responsive UI** – Works on desktop, tablet, and mobile.
- **User registration & login** – Secure password hashing with Werkzeug.
- **Realistic productivity theme** – Cards, icons, and gradients that mimic a modern SaaS tool.
- **The prank** – After a successful login, users are redirected to a page that delivers the joke with dramatic animations, a skull icon, and a "Logout & Run Away" button.
- **Harmless** – No tracking, no external data collection. The joke is confined to the dashboard.

---

## 📁 Project Structure

```
flask-april-fools/
├── app.py               # Main Flask application
├── models.py            # Database model (User)
├── forms.py             # WTForms for login/signup
├── requirements.txt     # Python dependencies
├── .gitignore           # (optional) Ignore venv, __pycache__, etc.
└── templates/
    ├── base.html        # Base template with Tailwind CSS
    ├── login.html       # Login page
    ├── signup.html      # Signup page
    └── dashboard.html   # The prank page (shown after login)
```

---

## 🛠️ Setup & Run

1. **Clone the repository** (or copy the files into a new directory).

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip3 install -r requirements.txt    # On Windows : pip install -r requirements.txt
   ```

4. **Run the application**:
   ```bash
   python3 app.py    # On Windows : python app.py
   ```

5. **Open your browser** and go to `http://127.0.0.1:5000`.

6. **Share the fun!** Give your friends the URL (forward the port or have them clone the repo) and watch their reaction when they log in.

---

## 🧪 How the Prank Works

- The app uses **Flask-Login** to manage sessions and **SQLAlchemy** to store user credentials.
- After a user signs up and logs in, they are redirected to `/dashboard`.
- The dashboard template (`dashboard.html`) contains a completely different design: a red‑themed card with a skull icon and the prank message.
- The prank is immediate—there's no "real" dashboard content. The logout button returns to the login page.

---

## 🔧 Customization

- **Change the prank message** – Edit the text in `templates/dashboard.html`.
- **Modify the design** – The UI uses Tailwind CSS (loaded via CDN). You can adjust colors, fonts, or animations.
- **Set a custom secret key** – Replace `'your-secret-key-change-in-production'` in `app.py` with a strong key if you plan to deploy publicly (though this is meant for fun, not production).

---

## 🎉 Happy April Fools' Day!

Remember: This is a lighthearted joke. Use it responsibly and with friends who appreciate harmless fun.

**Enjoy fooling your friends!** 😈

---

Made with ❤️ by [jakegithub24](https://github.com/jakegithub24)
