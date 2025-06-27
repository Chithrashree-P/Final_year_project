# Final_year_project
  
               ###  MILK QUALITY ANALYSIS  
====================================================  

Welcome to the Milk Quality Analysis project! This project uses multiple sensors to collect data about milk quality and stores it in a local XAMPP server. The data is then displayed on a web page to analyze and visualize milk quality parameters in real time.  

----------------------------------------------------  
PROJECT OVERVIEW:  
----------------------------------------------------  
This project integrates the following components:  
1. *Sensors Used*:  
   - *pH Sensor*: Measures the acidity or alkalinity of the milk.  
   - *Colour Sensor*: Detects changes in milk color, indicating spoilage or quality.  
   - *Temperature Sensor*: Records milk temperature to ensure optimal storage conditions.  
   - *Gas Sensor*: Identifies gases like ammonia, indicating spoilage.  
   - *Ultrasonic Sensor*: Measures milk volume.  

2. *Data Storage*:  
   - The collected data is stored in a *MySQL database* using *XAMPP local server*.  

3. *Web Page Display*:  
   - The stored data is surfaced on a web page using PHP and HTML.  
   - Real-time updates provide insights into milk quality parameters.  

4. *Milk Quality Analysis*:  
   - The webpage evaluates and displays whether the milk is safe for consumption based on thresholds for the measured parameters.  

----------------------------------------------------  
CONTENTS OF THIS CD:  
----------------------------------------------------  
1. *Source Code*:  
   - sensors_code/: Contains Arduino/ESP8266 code for sensor integration.  
   - web_code/: Contains PHP, HTML, and CSS files for the web interface.  

2. *Database*:  
   - database/: SQL file to set up the MySQL database (milk_quality_db.sql).  

3. *Documentation*:  
   - README.txt (This file).  
   - Setup_Guide.pdf: Detailed instructions on project setup.  

4. *Dependencies*:  
   - requirements/: Libraries and software needed for this project.  

----------------------------------------------------  
SYSTEM REQUIREMENTS:  
----------------------------------------------------  
- *Hardware*:  
  - pH Sensor, Colour Sensor, Temperature Sensor, Gas Sensor, Ultrasonic Sensor.  
  - Microcontroller: ESP32

- *Software*:  
  - XAMPP (PHP, Apache, and MySQL).  
  - Arduino IDE for uploading sensor code.  

- *Browser*: Any modern web browser (e.g., Chrome, Firefox).  

----------------------------------------------------  
SETUP INSTRUCTIONS:  
----------------------------------------------------  

### Step 1: Install XAMPP  
1. Download XAMPP from [https://www.apachefriends.org/](https://www.apachefriends.org/).  
2. Install and start Apache and MySQL from the XAMPP control panel.  

### Step 2: Set Up the Database  
1. Open phpMyAdmin by visiting http://localhost/phpmyadmin in your browser.  
2. Create a new database named milk_quality_db.  
3. Import the provided milk_quality_db.sql file located in the database/ folder.  

### Step 3: Upload Sensor Code  
1. Connect the sensors to the microcontroller.  
2. Open the Arduino IDE and upload the code from sensors_code/sensors.ino.  
3. Ensure the microcontroller sends data to the XAMPP server via HTTP requests.  

### Step 4: Deploy Web Interface  
1. Copy the contents of the web_code/ folder to the htdocs/ directory in your XAMPP installation.  
2. Open your browser and go to http://localhost/ to access the web interface.  

### Step 5: Start Collecting Data  
1. Power on the sensors and microcontroller.  
2. Real-time data will be sent to the MySQL database and displayed on the web page.  

----------------------------------------------------  
HOW IT WORKS:  
----------------------------------------------------  
1. *Data Collection*:  
   - Sensors continuously monitor milk parameters.  
   - Data is sent to the MySQL database via the microcontroller.  

2. *Data Storage*:  
   - The XAMPP server stores data in the milk_quality table.  

3. *Web Interface*:  
   - The web page retrieves and displays data using PHP and MySQL queries.  
   - Milk quality is evaluated based on preset thresholds (e.g., pH < 6.5 indicates spoilage).  

----------------------------------------------------  
TROUBLESHOOTING:  
----------------------------------------------------  
1. *XAMPP Not Running*:  
   - Ensure Apache and MySQL are started from the XAMPP control panel.  

2. *Database Connection Errors*:  
   - Check the database credentials in web_code/config.php.  
   - Ensure the database name matches (milk_quality_db).  

3. *No Data on Web Page*:  
   - Verify that the microcontroller is sending data to the correct server address.  

----------------------------------------------------  
CONTACT INFORMATION:  
----------------------------------------------------  
For questions or support, please contact:  
- Email: pchitrashree@gmail.com

----------------------------------------------------  
DISCLAIMER:  
----------------------------------------------------  
This project is for educational and research purposes only. It is not intended for commercial use without validation and certification.  

====================================================  
THANK YOU FOR USING THIS PROJECT!  
====================================================
