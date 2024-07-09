# Django User Authentication System
This project is a comprehensive user authentication system built with Django. It supports registration, login, and user-specific dashboards for two types of users: Patients and Doctors. The system includes features like user profile pictures, address details, and basic form validation.

# Features

-User Registration: Allows new users to sign up with their personal details, including a profile picture and address.
-User Authentication: Secure login functionality using Django's built-in authentication system.
-User Types: Supports two types of users - Patients and Doctors.
-User Dashboard: Redirects authenticated users to their respective dashboards displaying their information.
-Form Validation: Ensures passwords match during registration and validates all required fields.
-Profile Pictures: Supports uploading and displaying user profile pictures.

# Project Structure
-user_auth_app/: Main project directory.
     -settings.py: Contains project settings, including the custom user model and installed apps.
     -urls.py: Defines the URL patterns for the project.
-accounts/: App directory.
     - models.py: Defines the custom user model.
     - forms.py: Contains the signup form.
     - views.py: Contains the views for signup and dashboard.
     - urls.py: Defines the URL patterns for the accounts app.

-templates/: Directory for HTML templates.
    -signup.html: Template for the signup form.
    -dashboard.html: Template for the user dashboard.

# Installation
1. Set Up the Project
    -Create a new Django project:
         -django-admin startproject user_auth_app
         -cd user_auth_app
    Create a new Django app:
         -python manage.py startapp accounts
    Add the new app to INSTALLED_APPS in user_auth_app/settings.py:
2. Create Models
   - accounts/models.py
3. Update Settings
   - Add the custom user model to user_auth_app/settings.py:
4. Create Forms
   -Create a signup form in accounts/forms.py:
5. Create Views
    - Add views for signup and dashboard in accounts/views.py:
6. Create URLs
    - Define URL patterns for the app in accounts/urls.py:
    - Include the app URLs in the main project URLs in user_auth_app/urls.py:
7.Create Templates
    - Create a signup template templates/signup.html:
    - Create a dashboard template templates/dashboard.html:
8. Run Migrations and Start the Server
    - Make migrations and migrate:
         - python manage.py makemigrations
         - python manage.py migrate
    - Create a superuser (to access the admin panel):
          - python manage.py createsuperuser
    - Run the server:
           - python manage.py runserver
    - Access the application:
           Open your browser and navigate to http://localhost:8000/accounts/signup to sign up.
           After signing up, you will be redirected to the dashboard.







