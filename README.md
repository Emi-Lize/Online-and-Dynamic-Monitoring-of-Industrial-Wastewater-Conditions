# Web App to Provide Online and Dynamic Monitoring of Industrial Wastewater Conditions to Enhance Overall Water Treatment System
>This project was a group project done during my second year at university for a module which spanned two semesters.

The aim of this project is to provide an online and dynamic capture system that is both cost-effective and accessible (without the use of professional equipment) for performing water quality checks. A web application, as well as a computer system, are employed to do this. The computer system works by analysing the water quality using photographs of water. Some modest apparatus (e.g., beaker, food dye, soil and webcam) must be prepared to accomplish this. The data will be kept in a database after the water has been analysed, and then uploaded onto the web application. The data will be shown on the web application, and the off-site operator will be notified of any additional measures that can be performed if the water quality changes.

### Water Analysis Software
The water analysis software was developed using Python. To initialise the software, the user is required to position the camera to take a picture of the beaker of water and the user will need to crop the image to the water region. The camera will then periodically take a picture of the beaker and crop the image following the coordinates chosen by the user. The image is pre-processed to remove any noise, glare or background before performing thresholding and comparing the HSV colour histograms of the initial image and the current image. 

### Web Application
The web application was done as a PWA and MySQL was used for the database to store the images. The user would be able to view all the images taken by the camera and be alerted if there is any change to the water colour in the beaker.

## Pre-requisites

Both the GUI and the Web-app needs Python, and needs to be connected to a localhost server. Below are the steps to get your localhost server running for each OS: 
  - Windows
      - Make sure Python is installed on your machine: https://www.python.org/downloads/
      - Download XAMPP from: https://www.apachefriends.org/index.html
      - Open the XAMPP Application and run Apache and MySQL
      - Open your browser and type `localhost"` in your address search bar
      - Click on "phpMyAdmin" in the top right corner of the page 
      - Import `hfyql1ju_csv_db_7.sql` and `hfyql1ju_segp.sql` into your server using the export button
  - macOS
      - Make sure Python is installed on your machine: https://www.python.org/downloads/macos/
      - Install phpMyAdmin for macOS: https://www.javatpoint.com/how-to-install-phpmyadmin-on-mac
      - Click on "phpMyAdmin" in the top right corner of the page 
      - Import `hfyql1ju_csv_db_7.sql` and `hfyql1ju_segp.sql` into your server using the export button
  - Linux:
      - Make sure Python is installed on your machine: https://opensource.com/article/20/4/install-python-linux
      - Install phpMyAdmin for Linux: https://www.linuxtechi.com/install-phpmyadmin-linux/
      - Click on "phpMyAdmin" in the top right corner of the page 
      - Import `hfyql1ju_csv_db_7.sql` and `hfyql1ju_segp.sql` into your server using the export button

## To run the web app

To deploy the web app locally, the following steps have to be done. 
Here are the steps required to run the web app on each OS:
  - Windows:
      - Extract the file `WebApp` and store it in the `htdocs` folder in the `xampp` folder
      - the `xampp` folder is usually stored in the `C:/Users/Username/xampp/htdocs`
      - Run the XAMPP software and activate the localhost server, with the databases stored
      - Go to the browser, and type `"localhost/webapp/index.php"` in the address bar
      - The web app should pop-up and prompt you to login
      - You may use the pre-set credentials: `username:ivan` , `password:qwerty`
  - macOS:
      - Make sure to run the XAMPP software and activate the localhost server, with the databases stored
      - Extract the file `WebApp` and store this in the localhost server
      - The location of this server can be seen in `"locations/[ip address]"` where the `[ip address]` will take the form of `000.000.000.000` where the `0` can be any number, this is the IP Address of your machine
      - After selecting the IP address, store the folder in `lampp/htdocs`
      - Open your browser and type in the address bar `"localhost:8080/webapp/index.php"`
      - Here is a video tutorial for a visual guide: https://www.youtube.com/watch?v=GwgWlkDxRPs
  - Linux:
      - Open XAMPP in the terminal with this command `cd /opt/lampp`
      - Then type `sudo ./manager-linux-x64.run` 
      - In the XAMPP window, go to `"Manage Servers"` and make sure all the options are running
      - You may import the databases (refer to pre-requisites)
      - Extract the file `WebApp` and store it in `/opt/lampp/htdocs`
      - Open your browser and type in the address bar `"127.0.0.1/webapp/index.php"`

## To run the software

The steps are the same across all platforms, just make sure the pre-requisites are met: 

  - Navigate to `__main__.py`
  - Run localhost server
  - Make sure database is set-up with the database files imported
  - Run `__main__.py`: 
     - Open any IDE of your choice 
     - Or Open your command prompt to the project directory and type `python __main__.py` and click enter
