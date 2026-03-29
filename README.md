# 🌿 Edenthought

Edenthought is a Django-based web application for personal journaling. Users can register, log in, create and manage journal entries (thoughts), and maintain a profile with a profile picture. The project emphasizes user authentication, clean UI with Bootstrap 5, and email notifications for new users.

---

## 🚀 Features

- 📝 Create, update, and delete journal thoughts  
- 👤 User registration, login, and logout  
- 🖼️ Profile management with profile picture uploads  
- 📩 Email notification on registration  
- 💻 Password reset functionality  
- 🎨 Styled forms using **Crispy Forms** and **Bootstrap 5**  
- 🔐 Authentication-protected dashboards and actions  

---

## 🛠️ Tech Stack

- **Backend:** Django 4.2.6  
- **Frontend Styling:** Bootstrap 5 via `crispy-bootstrap5`  
- **Forms:** `django-crispy-forms`  
- **Email:** Django `send_mail` functionality  
- **Server:** Gunicorn  
- **Database:** SQLite (`db.sqlite3`)  
- **Media Handling:** Pillow for image uploads  
- **Environment Management:** `django-environ`  

---

## 📁 Project Structure

```text
Edenthought/
│
├── manage.py
├── requirements.txt
├── db.sqlite3                  # SQLite database
├── README.md                   # This file
├── media/                      # Uploaded media files
│   └── Default.png             # Default profile picture
├── static/                     # Static files
│   ├── css/style.css           # Custom CSS
│   └── js/app.js               # Custom JS
├── edenthought/                # Main Django project
│   ├── __pycache__/            # Compiled Python files
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── journal/                    # Core journal app
│   ├── __pycache__/
│   ├── migrations/             # DB migrations
│   ├── templates/              # HTML templates
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   ├── views.py
│   └── tests.py

```

---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/nathanlopes45/Edenthought.git
cd Edenthought
```
### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate      # macOS/Linux
venv\Scripts\activate         # Windows
```
### 3. Install dependencies
```bash
pip install -r requirements.txt
```
### 4. Setup environment variables
Create a **`.env`** file in the root directory:
```bash
DEBUG=True
SECRET_KEY=your-secret-key
ALLOWED_HOSTS=127.0.0.1,localhost
DEFAULT_FROM_EMAIL=your-email@example.com
EMAIL_HOST=smtp.example.com
EMAIL_PORT=587
EMAIL_HOST_USER=your-email@example.com
EMAIL_HOST_PASSWORD=your-email-password
EMAIL_USE_TLS=True
```
Adjust email settings to enable registration notifications.

---

## 🗄️ Database Setup
Run migrations
```bash
python manage.py migrate
```
Create a superuser
```bash
python manage.py createsuperuser
```
---

## ▶️ Running the Development Server
```bash
python manage.py runserver
```
Visit: http://127.0.0.1:8000/

---

## 📌 Key URLs / Routes

| URL                    | Description                     |
| ---------------------- | ------------------------------- |
| `/`                    | Homepage                        |
| `/register`            | User registration               |
| `/my-login`            | Login                           |
| `/dashboard`           | User dashboard (requires login) |
| `/create-thought`      | Create a new journal thought    |
| `/my-thoughts`         | View all your thoughts          |
| `/update-thought/<pk>` | Update a thought                |
| `/delete-thought/<pk>` | Delete a thought                |
| `/profile-management`  | Update profile and user info    |
| `/delete-account`      | Delete account                  |
| `/reset_password`      | Password reset flow             |

---

## 📂 Static, Media & Templates

### Static files
**Location:** `/static/`  
- `css/style.css` — Form styling  
- `js/app.js` — Auto-hide messages after 5 seconds  

### Media files
**Location:** `/media/`  
- Profile pictures and uploaded images  
- Default profile picture: `Default.png`  

### Templates
**Location:** `/journal/templates/`  
- HTML templates for all pages (registration, login, dashboard, thought management, profile, etc.)

---

## 🚀 Deployment

This project can be deployed with Gunicorn and NGINX:
```bash
gunicorn edenthought.wsgi:application
```

Production tips:
- Set `DEBUG=False`
- Configure `ALLOWED_HOSTS`
- Use PostgreSQL or MySQL in production
- Serve static files via NGINX

---
## 📌 Future Improvements
- Rich text editor for thoughts
- Tagging or categories for entries
- REST API endpoints with Django REST Framework
- Notifications / reminders
---
## 🤝 Contributing
- Fork the repository
- Create a branch (`git checkout -b feature-name`)
- Commit your changes (`git commit -m "Description"`)
- Push to the branch (`git push origin feature-name`)
- Open a pull request

---

## 📄 License
MIT License

---

## 👤 Author
Nathan Lopes









