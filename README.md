# The-Last-Chapter



# UX
This application was built to allow users create and share recipes, as well as updating and deleting them as necessary. The application provides a registration page for new users to register on the site, and a log in page to sign in after they have registered. Any visitor can browse the recipes created on the site but logged in users, aside from adding, editing and deleting recipes, can upvote recipes using the "like" button system.
## Project Goals
A full stack CRUD application that allows users to register and log in to create, edit, update and delete recipes.

This application uses Python on the back-end with the Flask web framework, and uses MongoDB for the database. It also uses the Materialize framework on the front-end.

Built for Milestone Project no.4 in the Full Stack Software Development bootcamp at Code Institute, in the Data Centric Development module.

# User stories 
## First Time Visitor Goals
* register as a user on the site
*  log in to the site once registered
*  edit recipes I create on the site (when logged in)
* delete any recipes I created on the site (when logged in)
* view a list of recipes stored on the site
* search the list of recipes by a recipe name
* click on a recipe to see information about the recipe
* see the ingredients for a selected recipe
This site was built on the basis of ideas from initial wireframes created in Adobe XD and exported image files for these can be seen below. These image files as well as the XD project file can be found in the main project folder:


## Design 

### Colour Scheme
* The main colors used are Black , Dark green , Aquamarine , blanchedalmond

### Typography
* The Montserrat font is the main font used throughout the whole website with Sans Serif as the fallback font in case for any reason the font isn't being imported into the site correctly. Montserrat is a clean font used frequently in programming, so it is both attractive and appropriate.

### Imagery
The Imagery is a gif of a portal form the tv series and I got it from google it's important because it's 
the background of the card and once you click on it you get the image of the characthers that are also important
images.

### Wireframes
* Home Page Wireframe - [View](https://balsamiq.cloud/sbfz8q4/pk8qq3n)
* Mobile Wireframe -  [View](https://balsamiq.cloud/sbfz8q4/pk8qq3n)



### Features
* Feature 1 - The User Registration and User Login feature hashes user passwords so user's passwords are not stored in the application database as simple text strings as they are entered by the user when registering. This means that even by viewing the database documents you will not be able to see a user's password. The Registration form and Login forms use a lot of HTML validation including Regex pattern detection to ensure that usernames and password etc are all entered in the correct format. These forms also provide dynamic helper text to let a user know if there are any problems with anything they have entered in one of the fields, or if everything is ok. Usernames also have to be unique and the application will check through the database to ensure usernames aren't already taken before a new user can be registered.


* Feature 2 - User Authorisation built within the application ensures that visitors to the site cannot access URL routes for adding, updating or deleting recipes and will be redirected to the Login page if any of these URLs are entered in the browser address bar. Also, once a user is logged in they will only be able to Edit/Update or Delete recipes only created by them alone. They will not be able to do the same to recipes created by other users. The option to log out of the site is available to users who are logged into an active session.

* Feature 3 - The feature for Adding Recipes will be available for users who are logged in and is accessed by the 'Add' button in the bottom right-hand corner of the UI. This will take the user to a full page form that will allow them to submit detailed information about a new recipe as well as adding an image (a remotely hosted image, added by URL) dynamically adding and removing ingredients and steps in the recipe method. Again, this form provides helper text assistance to users to let them know if there are problems with entries in form fields or whether everything is ok.
# Technologies Used
## Languages Used
* HTML5
 *  This project uses HTML to structure the content of the website.


* CSS3
  * The project uses CSS to add additional styling to the site and refine responsive beahviour using media queries.

* JavaScript
  * The project uses JavaScript to add and remove content dynamically and to initialise Materialize components.

* Materialize
  * This project uses Materialize to provide the front-end grid framework and support responsive behaviour.


* jQuery 
  * This project uses jQuery to assist in making asynchronous requests for and also to simplify DOM node selection and manipulation.


* Python
  * This project uses Python as the server-side programming language to provide back-end logic and serve dynamic web pages to the browser.


* Flask
  * This project uses Flask as the back-end framework to simplify configuration of the application and routing, to render HTML templates, work with client requests and to assist with user session management.

* Flask-PyMongo
  * This project uses Flask-PyMongo to connect the application to MongoDB and for retrieving, inserting, updating and deleting data to and from the database.


* MongoDB 
  * This project uses MongoDB, and more specifically MongoDB Atlas, as it's database system used to store data about users and recipes.



# Frameworks, Libraries & Programs Used
* Bootstrap 4.4.1:
* Bootstrap was used to assist with the responsiveness and styling of the website.
* Hover.css:
* Javascript 
* jQuery

## Font Awesome:
* Font Awesome was used on all pages throughout the website to add icons for aesthetic and UX purposes.

## Git :
* Git was used for version control by utilizing the Gitpod terminal to commit to Git and Push to GitHub.

## GitHub:
* GitHub is used to store the projects code after being pushed from Git.
## Photoshop:
* Photoshop was used to create the logo, resizing images and editing photos for the website.
## Balsamiq:
* Balsamiq was used to create the wireframes during the design process.
# Testing
This project was developed incrementally with continuous use of console.log statement in JavaScript and the print() function in Python to repeatedly check the changes made in the application and to ensure all changes to source code were providing the desired outcome in the browser. The site was build using Google Chrome browser (version 74) and then later tested in other browsers; FireFox (version 66) and Edge (version 42).

This project was tested for responsiveness using the Chrome Developer Tools mobile device simulator. It was also viewed on physical Samsung Galaxy A5 (2017) mobile device to ensure good responsive behaviour. The site was also tested in Mozilla Firefox (version 66) and Microsoft Edge (version 42) browsers to ensure appearance and functionality of the site was as expected across all 3 of these browsers.

All of the following routes were checked using the W3C Validation Tool [here](https://validator.w3.org/), and both HTML and CSS files passed without error:

* /
* /login
* /add_recipe
* /edit_recipe/<recipe_id>/
* /recipe/<recipe_id>/
* /signup

* W3C Markup Validator Html - [View](https://dujeb9m.sharing.bublup.com/ui/landing_page?item_id=001-i-8a9e545d-8d33-4d47-ae86-7d30d88d9675)


* W3C CSS Validator -  [View](https://dujeb9m.sharing.bublup.com/ui/landing_page?item_id=001-i-6c4ceb7d-c555-4bc8-ad2a-0aa2b26e4b54)

* JavaScript Validator -  [View](https://dujeb9m.sharing.bublup.com/ui/landing_page?item_id=001-i-6203c21d-482f-4be1-85ea-360e42c3d9e9)
* Python Validator -  [View](https://dujeb9m.sharing.bublup.com/ui/landing_page?item_id=001-i-8a3d0d32-c983-409a-adbc-3af8745d42e1)

There are a number of forms used on this application to accept user input including the login form, signup form, search and filter forms on the recipe list page and on the add and edit recipe pages. Various forms and levels of HTML validation has been used on form inputs to verify inputs to each form field. These forms were tested while being developed to ensure that the validation was having the desired effect and providing the desired outcome.

The site was also audited with Chrome Dev Tools' Lighthouse, with no throttling, and the results were good and were as follows on the audit report: 

                 Performance | Accessibility | Best Practices | SEO
--- | --- | ---
99 | 92 | 100 |89

The application is hosted on Heroku and I understand SSL certificates are only provided for on paid dynos, whereas this application is currently being hosted on a free dyno.

All the JavaScript code written in this application does not explicitly return any values as such and for the most part simply completes operations for manipulating the DOM or providing UI effect and features. This is primarily done using functions provided by the jQuery library as well as some functions provided with the Materialize framework, and on that basis I have not written unit tests to test any functions in the application as they are predominantly provided by external libraries which I trust have already been thoroughly tested by the developers and maintainers of those libraries.


## Further Testing
* The Website was tested on Google Chrome, Internet Explorer, Microsoft Edge and Safari browsers.
* The website was viewed on a variety of devices such as Desktop, Laptop, iPhone11 & iPhoneX.
* A large amount of testing was done to ensure that all pages were linking correctly.
* Friends and family members were asked to review the site and documentation to point out any bugs and/or user experience issues.
## Known Bugs
Some known bugs are that the search and reset button overlap in some certain web apps and don't do it mostly but it does.
Also some of the name on the page don't match the code but still figure out how to make it work and pages works fine.
Had trouble with the mongodb but managed to make it work so the pages looks nice and well.



## Deployment
GitHub was used for version control throught the development of the application and to host the code by pushing all code to the repo on GitHub.

This project was then deployed to Heroku to host the live application, following the steps below:
1. Log in to [Herkou]()and create a new app called 'last-chapter-project'

2. Log in to Heroku in the CLI
3. Add the remote Heroku repo
4. Create the requirements.txt file by running pip3 freeze --local > requirements.txt in the CLI
5. Create a Procfile by running echo web: python run.py > Procfile in the CLI
6. Start a web process on Heroku by running heroku ps:scale web=1 in the CLI
7. Set environment variables in Heroku for IP, PORT and MONGO_URI
8. Restart all dynos on Heroku
## Forking the GitHub Repository
By forking the GitHub Repository we make a copy of the original repository on our GitHub account to view and/or make changes without affecting the original repository by using the following steps...

* Log in to GitHub and locate the GitHub Repository
* At the top of the Repository (not top of page) just above the "Settings" Button on the menu, locate the "Fork" Button.
* You should now have a copy of the original repository in your GitHub account.



## Credits
### Code
* Bootstrap4: Bootstrap Library used throughout the project mainly to make site responsive using the Bootstrap Grid System.
* The concept for this cook book came mostly from the mini project on code institute thanks to them and their task manger i was able to built my own search functionality and make it my own, also kes2401 was a big help his own cookbook gave me ideas for mine.




## Content
* All content was written by me Freddy Garcia.


## Media
* All Images were found on Google.
* Some images were photo shopped to better fit my needs 
## Acknowledgements
My Mentor, for continuous helpful feedback.

Tutor support at Code Institute for their support.







