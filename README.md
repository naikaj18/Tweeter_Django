
# Django Tweeter

Django Tweeter is a dynamic web application that allows users to manage tweets with full CRUD functionality (Create, Read, Update, Delete). Built using the Django framework, it emphasizes user authentication and authorization to ensure a secure and personalized experience.

## About the Project

This project is designed to mimic a basic version of a tweet management system. Users can register, log in, and interact with tweets in a secure environment. Key features include:

- **Registration**: Users can create accounts to join the platform.
- **Login/Logout**: Secure authentication for accessing the application.
- **Tweet Management**:
  - Create tweets with an optional media upload.
  - Edit existing tweets while ensuring only the original author can make changes.
  - Delete tweets after confirmation, restricted to the owner.

The application dynamically lists all tweets on the homepage, sorted by their creation time (newest first).

## Features

### General Features

1. **Authentication**:
   - User registration.
   - User login/logout.
   - Password security using Django's built-in authentication mechanisms.

2. **Authorization**:
   - Only logged-in users can create, edit, or delete tweets.
   - Users cannot edit or delete tweets authored by others.

3. **CRUD for Tweets**:
   - **Create**: Users can create tweets via a form.
   - **Read**: All tweets are displayed in a reverse chronological order on the homepage.
   - **Update**: Users can edit their own tweets with pre-filled forms.
   - **Delete**: Users can delete their tweets after a confirmation step.

### Implementation Highlights

- **Registration View**: 
  - Users can register by providing necessary details through a form.
  - Automatic login for new users upon successful registration.
  
- **Tweet Views**:
  - **`tweet_list`**: Displays all tweets sorted by creation time.
  - **`tweet_create`**: Enables authenticated users to post new tweets.
  - **`tweet_edit`**: Allows users to edit their tweets.
  - **`tweet_delete`**: Provides tweet deletion functionality with a confirmation page.

## Installation and Setup

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd django-tweeter
   ```

2. Create a virtual environment and activate it:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Apply migrations to set up the database:

   ```bash
   python manage.py migrate
   ```

5. Create a superuser to manage the application:

   ```bash
   python manage.py createsuperuser
   ```

6. Start the development server:

   ```bash
   python manage.py runserver
   ```

7. Open the browser and visit `http://127.0.0.1:8000` to access the application.

## How to Use

1. **Registration**:
   - Navigate to the registration page and create a new account.
   - Upon successful registration, you will be logged in automatically.

2. **Tweet Management**:
   - **Creating Tweets**: Log in and post tweets using the "Create Tweet" form.
   - **Editing Tweets**: Click the "Edit" button next to a tweet to update it.
   - **Deleting Tweets**: Click "Delete" to remove a tweet after confirmation.

3. **Viewing Tweets**:
   - The homepage displays all tweets in reverse chronological order.

## Technologies Used

- **Backend**: Django framework
- **Frontend**: Django templates, HTML, CSS
- **Database**: SQLite (default; can be replaced with PostgreSQL or MySQL)
- **Authentication**: Django’s built-in user authentication system
