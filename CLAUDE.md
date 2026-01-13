# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Django student management system** built for learning Django web development fundamentals. The project uses Django 6.0.1 with Python 3.12+ and uv for package management.

## Development Commands

### Essential Commands

```bash
# Activate virtual environment (required for all commands)
source .venv/bin/activate

# Run development server (default: http://127.0.0.1:8000)
python manage.py runserver

# Create a new Django app
python manage.py startapp <app_name>

# Create migrations after model changes
python manage.py makemigrations

# Apply migrations to database
python manage.py migrate

# Create admin superuser
python manage.py createsuperuser

# Open Django shell for testing
python manage.py shell
```

### Package Management with uv

```bash
# Add a new dependency
uv add <package_name>

# Sync dependencies
uv sync
```

## Architecture

### Project Structure

- **config/** - Django project configuration directory (not a typical Django app)
  - `settings.py` - Main Django settings (INSTALLED_APPS, database, templates, etc.)
  - `urls.py` - Root URL configuration, currently only includes admin URLs
  - `wsgi.py` / `asgi.py` - Deployment gateways

### Current State

- Database: SQLite3 (`db.sqlite3`), currently empty with no migrations applied
- No custom Django apps exist yet
- Only Django's built-in apps are configured (admin, auth, sessions, etc.)
- Project is ready for app creation and model definition

### MTV Architecture Pattern

This project follows Django's Model-Template-View pattern:

- **Models** - Database schema definition in `models.py`
- **Views** - Business logic in `views.py`
- **Templates** - HTML presentation in `templates/` directories
- **URLs** - Routing in `urls.py`

### Adding New Features

When creating new functionality:
1. Create app: `python manage.py startapp <app_name>`
2. Add app to `INSTALLED_APPS` in `config/settings.py`
3. Define models in `<app>/models.py`
4. Create and apply migrations
5. Create views in `<app>/views.py`
6. Create URL configuration in `<app>/urls.py` and include in `config/urls.py`
7. Create templates in `<app>/templates/<app>/`
8. Register models with admin in `<app>/admin.py` for automatic admin interface

### Database

- Uses SQLite3 for development (configured in settings.py)
- Database file: `db.sqlite3` in project root
- No migrations applied yet - ready for initial model creation

## Learning Context

This is a learning project with goals including:
- Understanding Django project and app structures
- Git multi-branch development workflows
- Django ORM, URL routing, and template handling
- Form processing and admin interface
- uv package management workflow
