# 🔐 Django OTP + JWT Auth System with Chat (WIP)

A Django-based web app with OTP authentication, JWT-secured sessions, and real-time chat integration (WebSocket in progress).

This project uses Django's arcitecture, but in myapp is an inactive arcitecture (MVC + Clean Code) for big projects. If you need to use, myapp/Controller contains all files that handle rendering pages, and myapp/Models contains all Models and queries, and myapp/Services files are for logic of the application and they are imported and used in Model or Controller files, there is a myapop/Helper folder which is used to make many actions easier: like rendering pages without .html or using for payment gateways and etc.

The complete MVC application is in test1 in address: https://github.com/alih982/Django-application-with-JWT-Authentication
---

## 📦 Apps Included

### `myapp`
- Secure `/panel/` view
- JWT validation via `access_token` cookie
- Auto-user creation using `username=phone`
- Custom user model (`db_table = 'User'`)

### `otpauth`
- OTP generation and verification
- Sets JWT token in HTTP-only cookie
- Handles new user registration if not found

### `chatapp`
- Real-time messaging via WebSocket (WIP)
- Designed to support channels/rooms
- Frontend integrated, backend handler in progress

---

## 🗂 Structure

.
├── myproject/
│ ├── settings.py
│ ├── urls.py
│ └── ...
├── myapp/
│ ├── views.py
│ ├── templates/panel.html
│ └── ...
├── otpauth/
│ ├── views.py
│ ├── otp logic (JWT/Phone-based)
├── chatapp/
│ ├── consumers.py # WebSocket logic (incomplete)
│ ├── templates/chat.html
├── templates/
│ └── otp.html
├── static/
├── requirements.txt
└── README.md


---

## ⚙️ Features

- 🔑 OTP login by phone number
- 🧾 JWT (access token) stored in cookies
- 🧍 Custom `User` model (username only)
- 📥 Auto-create user on login if needed
- 🧪 Protected panel access via JWT
- 💬 Real-time chat with WebSocket (planned)
- 🔁 JWT refresh planned (not implemented)

---

## 🚀 Quick Start

### 1. Clone the repo

```bash
git clone https://github.com/yourname/otp-chat-auth.git
cd otp-chat-auth

Indtalling requirements:

pip install -r requirements.txt

or if using python 3:
pip3 install -r requirements.txt

Run project:

python manage.py runserver

or python 3:

python3 manage.py runserver
