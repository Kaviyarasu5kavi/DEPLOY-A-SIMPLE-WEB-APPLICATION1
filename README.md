# Simple Calendar Web Application

This project is a basic calendar web application built using PHP. It allows users to view a calendar interface on a web browser. The application is deployed on a public server to make it accessible to everyone.

---

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Deployment](#deployment)
- [Accessing the Application](#accessing-the-application)
- [License](#license)

---

## Prerequisites

Before deploying the application, make sure you have the following:

- A Google Cloud Platform (GCP) account (for hosting the app on a public server).
- Basic knowledge of PHP, file transfers, and terminal commands.
- An SSH key for secure access to the server (optional but recommended).

---

## Installation

### Step 1: Download the Project Files
1. Go to the GitHub page for the calendar project: [PHP Calendar Project on GitHub](https://github.com/wftutorials/php-mini-projects/tree/main/calendar).
2. Download the `calendar` folder as a ZIP file.
3. Extract the ZIP file to a folder on your local machine.

### Step 2: Set Up a Local PHP Environment
1. Make sure PHP is installed:
   ```bash
   php -v
2. Navigate to the calendar folder:
   ```bash
   cd path/to/calendar
3. Start a PHP local server:
   ```bash
   php -S localhost:8000
4. Visit http://localhost:8000 in your browser to view the calendar app.

## Deployment

### Step 1: Set Up a GCP VM Instance
1. Log in to your Google Cloud Console.
2. Navigate to the Compute Engine section and create a new VM instance:
   - Name: Choose a unique name for your instance.
   - Machine Type: Select a suitable machine type (e.g., e2-micro for free tier).
   - Image: Use Ubuntu as the operating system.
3. Allow HTTP and HTTPS traffic under the Firewall section.
4. Click Create to start the instance.

### Step 2: Connect to the GCP VM Instance
1. Use the SSH button in the Google Cloud Console to connect to the instance.
2. Alternatively, connect via terminal using the following command:
   ```bash
   gcloud compute ssh your-instance-name



### Step 3: Install Apache and PHP on the Server
1. Run the following commands to install Apache and PHP on your server:
   ```bash
   sudo apt update
   sudo apt install apache2 -y
   sudo apt install php libapache2-mod-php -y

### Step 4: Transfer the Project Files
1. Transfer the files from your local machine to the server’s Apache root directory using scp:
   ```bash
   scp -r /path/to/local/calendar/* username@your-instance-ip:/var/www/html/


### Step 5: Set Permissions
1. Ensure that the Apache user has permissions to access the files:
   ```bash
   sudo chown -R www-data:www-data /var/www/html/

### Step 6: Restart Apache
1. After uploading the files, restart Apache to load the application:
   ```bash
   sudo systemctl restart apache2.


## Accessing the Application
Once deployed, you can access the application via your server’s public IP address:
1. Replace your-instance-ip with the actual IP address of your server.
   ```bash
   http://your-instance-ip/












