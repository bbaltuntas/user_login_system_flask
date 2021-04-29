# user_login_system_flask

File Structure and Setup

After open the project in ide that I upload, if you are using PyCharm u can use the terminal at the bottom of the page to install the flask and mysqldb :
 
The static, templates and main.py files should be  copied and pasted to your new project directory. Like above.

 
If you are not, Open Command Prompt and navigate to your project directory. You can do this with the command cd c:\your_project_folder_destination on Windows.
	Install Python Flask with the command:         pip install flask
Install Flask-MySQLdb with the command:    pip install flask-mysqldb

Creating the Database and the setting-up Tables
Open MySQL Workbench and enter your account.
Open your connection.
Copy, past and execute the following SQL statements:


CREATE DATABASE IF NOT EXISTS `pythonlogin` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
USE `pythonlogin`;

CREATE TABLE IF NOT EXISTS `accounts` (
	`id` int(11) NOT NULL AUTO_INCREMENT,
  	`username` varchar(50) NOT NULL,
  	`password` varchar(255) NOT NULL,
  	`email` varchar(100) NOT NULL,
    `telephone` varchar(255) NOT NULL,
  	`address` varchar(100) NOT NULL,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

INSERT INTO `accounts` (`id`, `username`, `password`, `email`, `telephone`, `address`) VALUES (1, 'test', 'test', 'test@test.com','123','test');


Coding Explanation
1)

You should enter your own connection details in first part of the main.

2)
To run the code, you should run some several lines.
Again, go to your Command prompt and navigate to your project directory or go Ide’s terminal and run these lines:
set FLASK_APP=main.py 
set FLASK_DEBUG=1
flask run
Every time before u close the project u can use flask run method to run the project.

Website Information
To test before the registration u can use username = “test” and password = “test”.
Or you can navigate the register page and by filling out the forms you can register.
First page, Welcome Page you will see the information of the existing users.
On the top right on the screen, you can visit the profile page where u can see the current user’s data. And you can update the username, password, and email from the Update part. But unfortunately, after updating the information once you can not change it again until you logout and login. I could not fix the problem. But when you logout and login again u can update the user’s information again.

You can use the website: 
http://localhost:5000
