# iitm-wiki
[![Join the chat at https://gitter.im/The-WebOps-Club/iitm-wiki](https://badges.gitter.im/The-WebOps-Club/iitm-wiki.svg)](https://gitter.im/The-WebOps-Club/iitm-wiki?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Installation process of MediaWiki in ubuntu 16.04

1. Installation of Apachae2 web server : Execute the following commands -

            sudo apt-get update
            sudo apt-get install apache2
            
    Execute the following command to restart Apache2 serever whenever required.
    
            sudo systemctl restart apache2
           
2. Installation of MySQL : Execute the following commands -

            sudo apt-get update
            sudo apt-get install mysql-server
            
   You can configure your MySql database by executing following command :
   
            sudo mysql secure installation
            
   You will be asked to set the the root user name and password.
   
3. Installation of php and its extensions :

            sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql
            
   The above command will install the php without error. Execute the following commands to install the mbstring and xml   
   extensions which are required to run MediaWiki
   
            sudo apt-get install php7.0-mbstring
            sudo apt-get install php7.0-xml
            
   Restart your apache2 server.
   
 4. Installation of MediaWiki :
    Download the MedaWiki zipped file from https://www.mediawiki.org/wiki/Download
    Extract the zipped file and move it to the following directory -
    
            /var/www/html
            
 5. Creating new user and database in mysql for storing  MediaWiki data :
            
     login your mysql as root user by executing following command-
     
            mysql -u root -p
            
      create new user as following -
      
            CREATE USER 'wikiuser'@'localhost' IDENTIFIED BY 'pass-w0rd';
            GRANT ALL PRIVILEGES ON * . * TO 'wikiuser'@'localhost';
            flush privileges;
            quit;
            
  6. Completing the installation process :
  
     Feed the following address to your web browser : localhost/mediawiki
     Move forward as per the instruction displayed and download the LocalSettings.php file
     Move the LocalSettings.php file to the following directory /var/www/html/mediawiki

         
        























A wiki for IIT Madras.
The following is the process for installing mediaWiki on the local system:

    -Go to the website https://www.apachefriends.org/index.html and install Xampp as per your system 
    i.e if it is Windows or Mac or Linux
    Xampp is a free PHP based development environment which also contains Apache server and MySQL.
    
    - Further, after downloading Xampp install it as per the displayed instructions.
    
    - After installation is completed, a Xampp control panel window pops-up, click on the start
    buttons of Apache and MySql.
    
    - click on Admin button of MySQL in the control panel of Xampp, a webpage will be opened, go to databases
    tab and create new database by name say "my_wiki".
    
    - Go to the MediaWiki website https://www.mediawiki.org/wiki/MediaWiki and download the stable version of it.
    
    - Extract the downloaded zipped file to the location C:\xampp\htdocs and rename it as mediawiki.
    
    - In your Web Browser feed address " localhost/mediawiki".
    
    - In the webpage displayed click on the "set up wiki" and go further as per the instructions.
    
    - At the and after you have gone through the process of setting up wiki ,
    a php file "LocalSetting.php" will be downloaded.
    
    - Move that file to the directory "C:\xampp\htdocs\mediawiki".

Now your wiki is installed, feed the address "localhost/mediawiki" in your web browser to open the wiki. 
You can go through the following link for any details : https://www.youtube.com/watch?v=FkSfC1GLOc0 . 
    
    
