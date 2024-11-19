# DEPLOY-A-SIMPLE-WEB-APPLICATION1


    <h1>Simple Calendar Web Application</h1>

    <p>This project is a basic calendar web application built using PHP. It allows users to view a calendar interface on a web browser. The application is deployed on a public server to make it accessible to everyone.</p>

    <h2>Table of Contents</h2>
    <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#deployment">Deployment</a></li>
        <li><a href="#accessing-the-application">Accessing the Application</a></li>
        <li><a href="#license">License</a></li>
    </ul>

    <h2 id="prerequisites">Prerequisites</h2>
    <p>Before deploying the application, make sure you have the following:</p>
    <ul>
        <li>A cloud account on AWS, Google Cloud, Azure, or DigitalOcean (for hosting the app on a public server).</li>
        <li>Basic knowledge of using PHP, file transfers, and terminal commands.</li>
        <li>An SSH key for secure access to the server (optional but recommended).</li>
    </ul>

    <h2 id="installation">Installation</h2>

    <h3>Step 1: Download the Project Files</h3>
    <ol>
        <li>Go to the GitHub page for the calendar project: <a href="https://github.com/wftutorials/php-mini-projects/tree/main/calendar">PHP Calendar Project on GitHub</a>.</li>
        <li>Download the <code>calendar</code> folder as a ZIP file.</li>
        <li>Extract the ZIP file to a folder on your local machine.</li>
    </ol>

    <h3>Step 2: Set Up a Local PHP Environment</h3>
    <ol>
        <li>Make sure PHP is installed:</li>
        <pre><code>php -v</code></pre>
        <li>Navigate to the <code>calendar</code> folder:</li>
        <pre><code>cd path/to/calendar</code></pre>
        <li>Start a PHP local server:</li>
        <pre><code>php -S localhost:8000</code></pre>
        <li>Visit <a href="http://localhost:8000" target="_blank">http://localhost:8000</a> in your browser to view the calendar app.</li>
    </ol>

    <h2 id="deployment">Deployment</h2>

    <h3>Step 1: Set Up a Cloud Instance</h3>
    <ol>
        <li>Create an account with a cloud provider of your choice (AWS, Google Cloud, Azure, or DigitalOcean).</li>
        <li>Create a new instance (Ubuntu is recommended) using the provider’s free tier options.</li>
        <li>Connect to the instance using SSH:</li>
        <pre><code>ssh username@your-instance-ip</code></pre>
    </ol>

    <h3>Step 2: Install Apache and PHP on the Server</h3>
    <p>Run the following commands to install Apache and PHP on your server:</p>
    <pre><code>
sudo apt update
sudo apt install apache2 -y
sudo apt install php libapache2-mod-php -y
    </code></pre>

    <h3>Step 3: Transfer the Project Files</h3>
    <p>Transfer the files from your local machine to the server’s Apache root directory using <code>scp</code>:</p>
    <pre><code>scp -r /path/to/local/calendar/* username@your-instance-ip:/var/www/html/</code></pre>

    <h3>Step 4: Set Permissions</h3>
    <p>Ensure that the Apache user has permissions to access the files:</p>
    <pre><code>sudo chown -R www-data:www-data /var/www/html/</code></pre>

    <h3>Step 5: Restart Apache</h3>
    <p>After uploading the files, restart Apache to load the application:</p>
    <pre><code>sudo systemctl restart apache2</code></pre>

    <h2 id="accessing-the-application">Accessing the Application</h2>
    <p>Once deployed, you can access the application via your server’s public IP address:</p>
    <pre><code>http://your-instance-ip/</code></pre>
    <p>Replace <code>your-instance-ip</code> with the actual IP address of your server.</p>

    <h2 id="license">License</h2>
    <p>This project is open-source and licensed under the MIT License.</p>


