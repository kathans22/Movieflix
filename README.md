# MovieFlix - Netflix Clone

MovieFlix is a Netflix clone built using PHP, MySQL, and integrated with PayPal for payment processing. This README will guide you through setting up the project on your local machine.

## Table of Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [Step 1: Install XAMPP](#step-1-install-xampp)
  - [Step 2: Clone the Repository](#step-2-clone-the-repository)
  - [Step 3: Set Up the Database](#step-3-set-up-the-database)
  - [Step 4: Configure the Environment](#step-4-configure-the-environment)
  - [Step 5: Start the Application](#step-5-start-the-application)
- [Usage](#usage)
- [Payment Integration](#payment-integration)

## Features
- User authentication (Sign up, Login, Logout)
- Movie and TV show browsing
- Payment processing using PayPal
- Secure user management and subscriptions

## Prerequisites
Before you begin, ensure you have the following installed:
- [XAMPP](https://www.apachefriends.org/index.html) (Apache, MySQL, PHP)
- Git (optional, for cloning the repository)

## Installation

### Step 1: Install XAMPP
1. Download and install XAMPP from the [official website](https://www.apachefriends.org/download.html).
2. During installation, ensure you select Apache and MySQL.
3. Once installed, start the Apache and MySQL services from the XAMPP Control Panel.

### Step 2: Clone the Repository
1. Open a terminal or command prompt.
2. Navigate to the `htdocs` directory of your XAMPP installation:
    ```bash
    cd C:/xampp/htdocs
    ```
3. Clone the repository:
    ```bash
    git clone https://github.com/your-username/reeceflix.git
    ```

### Step 3: Set Up the Database
1. Open [phpMyAdmin](http://localhost/phpmyadmin) in your web browser.
2. Create a new database named `reeceflix`.
3. Import the `reeceflix.sql` file located in the `database` directory of the cloned repository:
    1. Select the `reeceflix` database.
    2. Click on the "Import" tab.
    3. Choose the `reeceflix.sql` file and click "Go" to import the database schema and data.

### Step 4: Configure the Environment
1. Open the cloned repository directory:
    ```bash
    cd C:/xampp/htdocs/reeceflix
    ```
2. Open the `config.php` file in a text editor.
3. Update the database connection settings:
    ```php
    $host = 'localhost';
    $db_name = 'reeceflix';
    $username = 'root';
    $password = '';  // Default password for XAMPP is empty
    ```
4. (Optional) Configure PayPal settings in `config.php`:
    ```php
    $paypalClientID = 'your-paypal-client-id';
    $paypalSecret = 'your-paypal-secret';
    ```

### Step 5: Start the Application
1. Ensure Apache and MySQL are running from the XAMPP Control Panel.
2. Open your web browser and go to [http://localhost/reeceflix](http://localhost/reeceflix).
3. You should now see the ReeceFlix homepage.

## Usage
- **Sign Up:** Create a new account to start using ReeceFlix.
- **Login:** Access your account to browse movies and TV shows.
- **Payment:** Subscribe to a plan using PayPal to unlock premium content.

## Payment Integration
ReeceFlix uses PayPal for handling payments. Ensure you have a PayPal developer account set up to test the payment functionality. The PayPal integration is configured in `config.php`.

---

Enjoy your movie experience with MovieFlix!
