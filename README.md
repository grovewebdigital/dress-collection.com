# 🧵 JamaKapor.com — Django Admin Panel

A modern Django admin panel for **JamaKapor.com**, styled with **Jazzmin**, powered by **PostgreSQL (Neon DB)**, and configured with `.env` environment variables, static/media file handling, and clean UI tweaks.

---

## 🚀 Features

- Jazzmin admin interface with custom theme
- PostgreSQL database integration via Neon
- Static and media file support
- Environment variable support via `.env`
- Django 4.x or 5.x compatible

---

## 📦 Requirements

- Python 3.10+
- pip
- PostgreSQL (Neon or local)
- virtualenv (recommended)

---

## ⚙️ Installation

```bash
# Clone the repo
git clone https://github.com/yourusername/jamakapor.com.git
cd jamakapor.com

# Create a virtual environment
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```dotenv
DEBUG=True
SECRET_KEY=your-secret-key

DB_NAME=neondb
DB_USER=neondb_owner
DB_PASSWORD=npg_8txS4PivNqsV
DB_HOST=ep-polished-forest-a1wbf4db-pooler.ap-southeast-1.aws.neon.tech
DB_PORT=5432
```

---

## 🛠 Settings Summary

### Static & Media
```python
STATIC_URL = '/static/'
STATICFILES_DIRS = [BASE_DIR / 'static']
STATIC_ROOT = BASE_DIR / 'staticfiles'

MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'
```

### Jazzmin Theme
```python
JAZZMIN_UI_TWEAKS = {
    "theme": "flatly",
    "dark_mode_theme": "solar",
    "navbar": "navbar-light bg-light",
    "accent": "accent-info",
    "button_classes": {
        "primary": "btn btn-outline-primary",
        "secondary": "btn btn-outline-secondary"
    },
    "actions_sticky_top": True,
}
```

---

## 🧪 Run Locally

```bash
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Open in browser: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

---

## 📁 Project Structure

```
jamakapor.com/
│
├── manage.py
├── .env
├── static/
├── media/
├── your_app/
│   ├── admin.py
│   └── ...
└── your_project/
    ├── settings.py
    └── urls.py
```

---

## ✅ Production Tips

- Use `DEBUG=False` in production
- Run `python manage.py collectstatic`
- Serve static/media via Nginx or WhiteNoise
- Use Gunicorn or uWSGI as the WSGI server

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## ✨ Credits

Made with ❤️ by Grove Web Digital
Powered by Django & Jazzmin

