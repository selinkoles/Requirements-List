# UI Interface for User Management
___Product Name:___ XYZ Management System  
___Date:___ 29 November, 2022  
___By:___ Selin Koles  

1. ## Introduction
	1. ### Product Value:
		Our client asked to add a new web page to XYZ Management System. The page intends to help the manager to manage the users. On this page a user manager can add a new user and visualize the users added to the database.
	2. ### Intended audience:
		This web page will be used by the manager who manages the users in XYZ Management System.
	3. ### Intended use:
		This web page performs two functions, visualizing the users and adding new users. On the web page, manager can add a new user using a form. There is a database too showing the ID, User Name, Email, and Enabled status of current users. The manager can also filter the users to hide the disabled user.
2. ## Functional requirements
	This web page has two sections; one section consists of a database table and the other one is a form. There is a navigation bar that adds functionalities to the page to add a new user, save the form, and filter the database based on the status of the user and whether it is enabled or not.
The database table shown on the page contains four columns, the ID, User Name, Email, and Enabled status of the user. The table also has sorting options for each column.  
The form to add a new user has imput fields to give the Username, Display Name, Phone, Email, User Roles options, and Enabled status.
3. ## External interface requirements
	1. ### User interface requirements:
		As mentioned in the functional requirements, the navigation bar should have two buttons, one to add New User and the other one to Save User. Also, there should be a radio button "Hide Disabled Users" that can check if we are filtering the user on basis of their Enabled status. The color for the buttons and radio check option should be #2596be, but button Save User should have #56a7cf color in inactive state (when input fields are empty) and the background color for the navigation bar should be #f5f5f5.  
The page should be divided into two sections having two columns division for the database table and form each.  
The database table must have four columns, named the ID, User Name, Email, and Enabled fields. The content in cells should be aligned to the left of each cell, only the cells containing ID numbers should be aligned to the right. The column headers should also have a sort button displayed on the right side of the cell. The table design should be as follows: the color for the column headers should be #007cba and the border with #64a8ca color, and then the cells should have a coloring sequence of #ffffff and #b9d9e8 alternatively and border color as #f0f0f0.  
The form should start with the heading New User with the background color #f5f5f5 and a font size of 16pt. Each input field should fill the whole row. The labels for each input field should be aligned to the left of the page and input fields should start and end at the same point filling the whole row. The input field User Role should be a dropdown with three options, Guest, Admin, and SuperAdmin and the input field Enabled should be a radio button with a rounded corner square check box.  
The font family should be "Calibri, sans-serif" and font size of the whole layout should be 12pt.
	2. ### Hardware interface requirements:
		The form should create a POST request when we press the Save User button. But before submitting the POST request we should validate the form if it is completed correctly.  
Alongside the database table should GET the required data of user from PostgreSQL Database Server to display on the table after submitting each POST request in the form end.  
	3. ### Software interface requirements:
		The frontend of the web page should be developed using React framework and it should be responsive. The backend should be built by using NodeJS as per the requirements of our client and to store the database we should use PostgreSQL. The web page should be deployed on Amazon Web Services.
4. ## Non-functional requirements
	For this web page, we should check the User authentication and User role when accessing this page, in case it doesn't match we should display the proper Error page. We will deploy this new web page on Amazon S3 storage service where we already have deployed XYZ Management System. This page should be reliable and easily maintainable.
