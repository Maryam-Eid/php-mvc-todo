# PHP MVC Todo

A small to-do list built with a custom PHP MVC structure.

## Pages

- `/` lists tasks from the database. A completed task is shown with a strikethrough
- `/about` shows the About page
- `/contact` shows the Contact page

## How it is organized

- `routes.php` maps each URL to a controller action
- `controllers/pagesController.php` loads the page data
- `core/router.php` and `core/request.php` match the request to a route
- `core/database` connects with PDO and runs `SELECT *` queries
- `views` are plain PHP templates

## Tech Stack

- PHP
- Composer (classmap autoload)
- MySQL (PDO)

## Requirements

- PHP with the PDO MySQL extension
- Composer
- MySQL

## Database

Connection settings are in `config.php`:

| Setting | Value |
| --- | --- |
| Host | `localhost` |
| Database | `todos` |
| Username | `root` |
| Password | empty |

Create a `todos` table with at least these columns:

- `description`
- `completed`

## Run

```bash
composer install
php -S localhost:8000
```

Then open `http://localhost:8000`.
