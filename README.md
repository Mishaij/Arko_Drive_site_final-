# Arko Drive

## Armenian Driving School Platform

Arko Drive is a web platform developed for an Armenian driving school. The platform provides students with access to theory materials, practice tests, road-sign information, and course packages. Website content can be managed through the Django Admin panel without changing the source code.

## Features

### Student Features

- Armenian-language responsive interface
- Information about the driving school
- Theory lessons organized by categories
- Practice tests with questions and answer choices
- Randomized question practice
- Session-based progress tracking
- Road-sign catalogue grouped by categories
- Theory, practical, and combined course packages
- Responsive mobile navigation
- Educational image support

### Admin Features

- Manage tests, questions, and answers
- Add and edit theory lessons
- Manage road-sign groups and road signs
- Manage course packages and package features
- Upload images for questions and road signs
- Manage vehicles, company values, and history
- Update website content through Django Admin

## Technologies

- Python
- Django 5.2
- MySQL
- Pillow
- HTML5
- CSS3
- JavaScript
- Django Templates
- Django Admin

## Application Routes

| Route | Description |
|---|---|
| `/` | Homepage |
| `/theory/` | Theory groups |
| `/theory/<id>/` | Questions for a theory group |
| `/tests/` | Practice tests |
| `/tests/<id>/` | Questions for a selected test |
| `/random-question/` | Randomized question practice |
| `/trafficsigns/` | Road-sign catalogue |
| `/packages/` | Course packages |
| `/about/` | About the driving school |
| `/admin/` | Django Admin panel |

## Project Structure

```text
Arko_Drive_site_final/
├── core/
│   ├── core/                 # Django project settings and URLs
│   ├── main/                 # Models, views, templates, and admin
│   ├── media/                # Uploaded images and educational materials
│   ├── manage.py             # Django management script
│   └── requirements.txt      # Project dependencies
└── README.md
```

## Installation

### Windows PowerShell

```powershell
cd core
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

### macOS / Linux

```bash
cd core
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

After starting the development server, open:

```text
http://127.0.0.1:8000/
```

The Django Admin panel is available at:

```text
http://127.0.0.1:8000/admin/
```

## Database Configuration

The project uses MySQL. Configure the database using the following environment variables:

```bash
DJANGO_SECRET_KEY="your-secret-key"
DJANGO_DEBUG="True"
DJANGO_ALLOWED_HOSTS="127.0.0.1,localhost"

MYSQL_DATABASE="arko_drive_autoschool"
MYSQL_USER="root"
MYSQL_PASSWORD="your-password"
MYSQL_HOST="localhost"
MYSQL_PORT="3306"
```

Do not commit real passwords, secret keys, or database credentials to GitHub.

## Database Models

The application includes relational Django models for:

- Tests
- Questions and answers
- Theory groups and lessons
- Road-sign groups and road signs
- Course packages and package features
- Vehicles
- Company values
- Company history

This structure allows administrators to update website content through the Django Admin panel while keeping the frontend dynamic and database-driven.

## Project Status

The project is currently being prepared for production deployment.

## Security

Never upload the following files to GitHub:

- Database passwords
- Secret keys
- `.env` files
- Local databases
- Virtual environments
- Python cache files

These files should be excluded through `.gitignore`.
