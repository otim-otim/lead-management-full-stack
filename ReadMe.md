## LEAD MANAGEMENT SYSTEM

This system uses react.js to serve the application frontend which is serviced by a laravel backend for API.

### BACKEND SET UP

## **Prerequisites**

Ensure the following tools are installed:

- PHP (version >= 8.1)
- Composer (latest version)
- Node.js and npm (optional, if frontend assets need compilation)
- A database (MySQL, PostgreSQL, or SQLite)


---

## **Setup Instructions**

1. **Clone the Repository**  
   Clone the repository to your local machine:  
   ```bash
   git clone https://github.com/otim-otim/lead-management-full-stack.git
   cd lead-be
2.  **Install Dependencies**
    ```bash
    composer install
3.  **Environment Configuration**
    Copy the example environment file and configure it:
    ```bash
    cp .env.example .env

4.  **Run Migrations**
    Copy the example environment file and configure it:
    ```bash
    php artisan migrate

4.  **Install Frontend Dependencies**
    ```bash
    npm install
    npm run dev

## **Starting the Backend Application**

1.  **Reverb Server**
    ```bash
    php artisan reverb:start
2.  **Queue Worker**
    ```bash
    php artisan queue:work
3.  **Development Server**
    ```bash
    php artisan serve

## **Initial Application Data**

Atleast one user is required to operate the application. use tinker to create a user(s).

    ```bash
    php artisan tinker

    User::factory()->create([
        "name": "your names",
        "email": "your email",
        "password": "your preferred password", //default is password
        "role": "your prefered role" //['admin', 'sales_manager', 'sales_rep']
        ])



### FRONTEND SET UP

## **Prerequisites**

Ensure the following tools are installed:

- Node 21

## **Setup Instructions**

1.  **Install Frontend Dependencies**
    ```bash
    npm install
    npm run dev

2.  **Environment Configuration**
    Copy the following lines to your env:
    ```bash
    VITE_BACKEND_URL=http://localhost:8000