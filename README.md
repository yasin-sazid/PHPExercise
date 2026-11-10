# PHP Account and Session Exercise

A small PHP web application implementing registration, sign-in, sign-out, and a session-aware home page. Developed as a practical web-programming exercise, it connects HTML forms to database records and server-side session state.

## User workflow

```text
Sign up → Store account in MySQL → Establish session → Home page
Sign in → Match account details → Establish session → Home page
Sign out → Clear session
```

## Project map

| File | Responsibility |
| --- | --- |
| `phpClassWork1/signUp.php` | Registration form, password-confirmation interaction, and account insertion |
| `phpClassWork1/signIn.php` | Sign-in form, account matching, and sign-out handling |
| `phpClassWork1/homePage.php` | Session-aware page navigation |
| `phpClassWork1/mydb.sql` | Database schema and supplied SQL content |
| `phpClassWork1/readme.txt` | Original local database setup details |

The implementation uses PHP's `mysqli` extension for database access and PHP sessions for signed-in state. Browser-side JavaScript checks the registration form's password confirmation.

## Local setup

Use PHP with `mysqli` enabled and a local MySQL-compatible server. Create the `myDB` database and import `phpClassWork1/mydb.sql`. The PHP connection settings and original setup notes specify the local database account expected by the exercise.

Serve the application directory:

```bash
php -S 127.0.0.1:8000 -t phpClassWork1
```

Open `http://127.0.0.1:8000/signUp.php` to register, or `http://127.0.0.1:8000/signIn.php` to use the sign-in workflow.

## Technical focus

The project illustrates request handling, form submission, SQL-backed account storage, session lifecycle management, and redirects across a multi-page application using core PHP facilities.
