# Blog Application

## Installation and Run 

**Click on 'BlogCorner.war' file above, then click on download option which is there right side, then 'BlogCorner.war' file will be downloaded**

**Create a database `blog` in MySQL**
**And Create these two tables in that database**

**CREATE TABLE User (
    UserId INT AUTO_INCREMENT PRIMARY KEY,
    UserName VARCHAR(100) NOT NULL,
    Password VARCHAR(50) NOT NULL,
    Email VARCHAR(100) NOT NULL,
    Address VARCHAR(100) NOT NULL,
    Role ENUM('Admin', 'Viewer') NOT NULL
);**


**CREATE TABLE Blog (
    BlogId INT AUTO_INCREMENT PRIMARY KEY,
    UserId INT,
    BlogName VARCHAR(100) NOT NULL,
    IsEdited TINYINT(1) NOT NULL DEFAULT 0,
    Title VARCHAR(255) NOT NULL,
    Content TEXT NOT NULL,
    PostedDate DATETIME DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (UserId) REFERENCES User(UserId)
);**


## Download and import the above BlogCorner.war file in Eclipse
## Make Sure that Apache Tomcat 9 Server should there in Eclipse
## Right click on the project, then click on Run As > Run on Server > Select Tomcat Server > Next > In Congifure 'BlogCorner' project should be there > Then Click on Finish 

Noote: After importing, it may show Descripter not loaded or some errors in jsp import statements, Don't worry this doesn't give any errors while running the project on Web Browser. 
