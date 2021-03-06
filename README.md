# test-blog
Blog app built with Flask. Features include - users, register, authentication, posts, edit.



This is a RESTful app. Scripted in Python3. Built using Flask, Bootstrap, Jinja,
SQLite/Postgres, SQLalchemy, CKEditor, WTForms, and several other libraries.
Hosted with gunicorn and heroku. Users can register, then create a user name and password.
Relationships are formed between the classes and their properties. 
Then they are stored in the database. Passwords are encrypted, hashed and salted.
Once authenticated, users can then add and edit their own post entries, comment on posts, and login and out.

Now, let's talk about REST and what makes this project REST-ful. This abbreviation stands for representational state transfer.
The definition can be conveyed with simpler words: data presentation for a client in the format that is convenient for it. 
There is one of the main points that you need to understand and remember: 
REST is not a standard or protocol, this is an approach to or architectural style fro writing API. 
It gives authenticated users access to the state of the sites contents that is appropritae to their user.

Server is built with flask for veiwing site through localhost in developement stage. 
Configure app connection to the database. Configure your Flask.app so its on your local server.
Bootstrap template design.

General rundown:

#forms.py Forms classes are defined to construct your actual form boxes for users to register,
login, post, comment, etc. #main.py Configure your tables classes for the forms to be established in the database.
Also established in these classes are your authtication validation requirements.
Once that is run and the tables are made, comment out the line of code "db.create_all()".
Define your functions for the behavior of your classes and your app. 
HTML pages must all be stored in a "templates" folder to let the flask server know where to look for them so they can be rendered.
CSS JS and a few other folders must be stored in "static" for the same reason.
Make your routes in main.py to connect these functions and objects into your HTML pages. 
Do the same on your HTML pages leading them to their correct objects and functions, using JINJA. 
JINGA allows python code lines to be written and executed in your HTML pages with FLASK. 
Form relationships between objects for database. They are made in the params of the class attributes.
Deploying, I used Heroku to host the app. You must switch to a WSGI server to run a python application. 
This app used gunicorn for the WSGI server.
Normal web servers can't run Python applications, 
so this will standardize language protocols between the application and the host server.
Also when in Heroku switch from sqlite to postgres database to prevent losing any stored data from your app.
