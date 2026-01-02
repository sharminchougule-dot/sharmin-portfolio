# Security Notice

## Important: Sensitive Information

This repository is **public** for GitHub Pages hosting. Please note:

### ✅ Safe to be Public (Client-Side)
- EmailJS Public Key - This is meant to be public (client-side JavaScript)
- EmailJS Service ID - Public identifier
- EmailJS Template ID - Public identifier
- Email addresses - Public contact information

### ⚠️ Never Commit These
- Gmail App Passwords
- API Secret Keys
- Private Keys
- Database Credentials
- Any passwords or tokens

### 🔒 Protected Files
The following files are excluded from the repository (via `.gitignore`):
- `.env` files
- `app.py` (Flask app with sensitive config)
- `requirements.txt` (Flask dependencies)
- `Procfile` (Flask deployment config)
- `render.yaml` (Flask deployment config)

### 📝 For Static GitHub Pages
This repository uses **static HTML/CSS/JS** for GitHub Pages. The Flask application files (`app.py`, etc.) are excluded and not needed for the live site.

### 🔐 EmailJS Security
EmailJS credentials in `index.html` are **public keys** designed for client-side use. They are safe to be public. The actual email sending happens server-side through EmailJS's secure infrastructure.

---

**Note**: If you need to use the Flask version, deploy it separately on Render or another platform with environment variables for sensitive credentials.

