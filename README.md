# SAFConnect
----
# Django Multi-Tenant Setup with PostgreSQL on Docker

This README outlines the steps for setting up a Django project with multi-tenancy using `django-tenants`, PostgreSQL in a Docker container, and creating a client app with tenant-specific models.

## Prerequisites

Before you begin, ensure you have the following:
- Python 3.x installed
- Docker installed and running
- Git installed
- Virtual environment (venv) enabled
- PostgreSQL running in Docker container

## Step 1: Clone the Django Project

Clone your Django project from GitHub:

```bash
git clone https://github.com/DEVHYDAR01/SAFConnect.git
```
###Navigate to the project directory:
```
cd your-django-project
```
###Create a virtual environment:
```
python3 -m venv venv
source venv/bin/activate
```
###Install Django version 5.2:
```
pip install django==5.2
```
###Pull the official PostgreSQL Docker image:
```
docker pull postgres
```
###Start the PostgreSQL container:
```
docker run --name Django-tenants-postgres-container -e POSTGRES_USER=youruser -e POSTGRES_PASSWORD=yourpassword -e POSTGRES_DB=yourdbname -p 5432:5432 -d postgres
docker ps
```
###Install the django-tenants package:
```
pip install django-tenants
```
###Create a new Django app called client:
```
python manage.py startapp client
```
**READ THE DJANGO TENANTS DOCUMENTATION BY:** [Thomas Turner & Bernardo Pires Carneiro Revision](https://django-tenants.readthedocs.io/en/latest/)
