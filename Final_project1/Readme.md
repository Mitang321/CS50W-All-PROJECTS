# Django Poll App

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Distinctiveness and Complexity](#distinctiveness-and-complexity)
- [File Structure](#file-structure)
- [Installation and Setup](#installation-and-setup)
- [How to Run](#how-to-run)


## Introduction
Django Poll App is a full-featured web application for creating and participating in polls. Users are required to register in order to view and vote in polls. The application ensures that each user can vote only once per poll. Additionally, only the owner of a poll has the authority to add, edit, update, or delete polls and choices. Once a poll is ended, voting is disabled and the final results are displayed.

## Features
- User Authentication: Register/Login to access polls.
- Create Poll: Only the owner can add a new poll.
- Edit, Update, Delete Poll: Poll owners have full control over their polls.
- Voting System: Users can vote once per poll.
- Search: Users can search for polls.
- Filters: Polls can be filtered by name, publish date, and the number of votes.
- Pagination: Easy navigation through pages, even with applied filters.

## Distinctiveness and Complexity

The Django Poll App brings a unique combination of features and utilities that make it both distinctive and complex in its scope. Below are some of the key aspects:

### User Authentication
One of the fundamental complexities is the robust user authentication system. It's not just about logging in; it's about maintaining a secure environment where each user's activities are isolated and personalized. This complexity extends to ensuring that each user can only vote once per poll, thereby making the voting process fair and transparent.

### CRUD Operations
The application provides full CRUD (Create, Read, Update, Delete) capabilities for polls but extends this basic feature set in a user-centric way. For instance, only the poll's creator can edit or delete it, adding a layer of authorization on top of the basic CRUD operations. This introduces complexity in the back-end logic to ensure that these rules are strictly adhered to.

### Advanced Search and Filtering
The application allows users to search and filter polls, not just on one criterion but multiple, such as name, publish date, and number of votes. Implementing this feature required a complex query mechanism that can handle multiple filters seamlessly, making the application distinctive in its capabilities.

### Voting Mechanism
The voting mechanism is not just a simple click-and-count operation. It involves validation to check whether the user has already voted, recording the vote securely, and then updating the poll statistics in real-time. This multi-step process adds complexity to the application.

### User Experience
On the front-end side, the application provides a clean, intuitive interface that dynamically updates based on user interactions. Implementing a seamless user experience like this involves a complex interplay of front-end and back-end technologies, making the application distinctive in its approach to UI/UX.

### Security Measures
Apart from user authentication, the application also implements various security measures such as data validation, session management, and secure handling of user passwords. Ensuring a secure user environment adds another layer of complexity to the project.

By integrating these features and mechanisms, the Django Poll App not only fulfills but exceeds the basic requirements of a web application, making it both distinctive and complex. It demonstrates a well-thought-out architecture, complex back-end logic, robust security measures, and a seamless user interface.


## File Structure
- `accounts/`: Manages user accounts and authentication.
- `pollme/`: Main project configuration and settings.
  - `__init__.py`: Initialization file for the package.
  - `settings.py`: Django settings file for the project.
  - `urls.py`: URL configurations for the project.
  - `views.py`: Generic views.
  - `wsgi.py`: WSGI configuration.
- `polls/`: Contains Django models, views, and templates specific to the polling functionality.
  - `migrations/`: Database migrations.
  - `templates/polls/`: HTML templates for polls.
  - `admin.py`: Admin interface customizations.
  - `apps.py`: Application configuration.
  - `forms.py`: Forms related to polls.
  - `models.py`: Data models.
  - `tests.py`: Test cases.
  - `urls.py`: URL configurations for polls.
  - `views.py`: Views for polls.
- `static/`: Static files.
  - `css/`: Stylesheets.
  - `img/`: Images.
- `templates/`: Global HTML templates.
  - `includes/`: Partial templates.
  - `base.html`: Base HTML template.
  - `home.html`: Home page template.
- `README.md`: This file, describing the project.
- `manage.py`: Django's command-line utility for administrative tasks.
- `requirements.txt`: List of project dependencies.
- `seeder.py`: Script for seeding the database with initial data.

## Installation and Setup
1. Install packages:
    ```bash
    pip install -r requirements.txt
    ```
2. Migrate:
    ```bash
    python manage.py migrate
    ```
3. Create superuser:
    ```bash
    python manage.py createsuperuser
    ```

## How to Run
1. Start the server:
    ```bash
    python manage.py runserver
    ```
2. Open `http://127.0.0.1:8000/` in your browser.




