# IUTLib

> Library Management System

## Installation

### 1. Clone GitHub repo for this project locally

If the project is hosted on github, we can use git on your local computer to clone it from github onto your local computer.

```
git clone https://github.com/KhasanovR/IUTLib.git
```

Once this runs, you will have a copy of the project on your computer.

### 2. cd into the project

```cd IUTLib```

### 3. Install Composer Dependencies

Whenever you clone a new Laravel project you must now install all of the project dependencies. This is what actually installs Laravel itself, among other necessary packages to get started.

When we run composer, it checks the `composer.json` file which is submitted to the github repo and lists all of the composer (PHP) packages that your repo requires. Because these packages are constantly changing, the source code is generally not submitted to github, but instead we let composer handle these updates. So to install all this source code we run composer with the following command.

```
composer install
```

### 4. Install NPM Dependencies

Just like how we must install composer packages to move forward, we must also install necessary NPM packages to move forward. 

```
npm install
```

or if you prefer yarn (as i do)

```
yarn
```

### 6. Create a copy of your .env file

`.env` files are not generally committed to source control for security reasons. But there is a `.env.example` which is a template of the `.env` file that the project expects us to have. So we will make a copy of the `.env.example` file and create a `.env` file that we can start to fill out to do things like database configuration in the next few steps.

```
cp .env.example .env
```

This will create a copy of the `.env.example` file in your project and name the copy simply `.env`.

### 7. Generate an app encryption key

Laravel requires you to have an app encryption key which is generally randomly generated and stored in your `.env` file. The app will use this encryption key to encode various elements of your application from cookies to password hashes and more.

Laravel’s command line tools thankfully make it super easy to generate this. In the terminal we can run this command to generate that key. (Make sure that you have already installed Laravel via composer and created an .env file before doing this, of which we have done both).

```
php artisan key:generate
```

If you check the `.env` file again, you will see that it now has a long random string of characters in the `APP_KEY` field. We now have a valid app encryption key.

### 8. Create an empty database for our application

Create an empty database for your project using the database tools you prefer (My favorite is [SequelPro](https://www.sequelpro.com/) for mac). In our example we created a database called “test”. Just create an empty database here, the exact steps will depend on your system setup.

### 9. In the .env file, add database information to allow Laravel to connect to the database

We will want to allow Laravel to connect to the database that you just created in the previous step. To do this, we must add the connection credentials in the .env file and Laravel will handle the connection from there.

In the .env file fill in the `DB_HOST`, `DB_PORT`, `DB_DATABASE`, `DB_USERNAME`, and `DB_PASSWORD` options to match the credentials of the database you just created. This will allow us to run migrations and seed the database in the next step.

### 10. Migrate the database

Once your credentials are in the .env file, now you can migrate your database.

```
php artisan migrate
```

It’s not a bad idea to check your database to make sure everything migrated the way you expected.

------

Madina Kurbanova u1610127

Madinakhon Raufova u1610130

Rakhmatjon Khasanov u1610183

Sardor Allabergenov u1610202

Shokhsanam Shirinkulova u1610231

**GitHub repo:** [https://github.com/KhasanovR/IUTLIB](https://github.com/KhasanovR/IUTLIB) 

Our web site is designed for an electronic library management system, which enables you to familiarize and download electronic textbooks, books and manuals, and add or remove them to or from “IUTLib“ database
based on the type of user.

There are three types of users and they are student, teacher, librarian who can control all activities which is held and others.

Stundent can see all content, download them and reserve them online then take it from library. Also the teacher can do the same things.

Librarians as we said before, can control all system activities and changes. And they can add more type of books moreover, new librarian accounts. Only librarian can delete members and books from the database.

![](meta/iut_lms_report_html_28d8eaa0c36b3f32.jpg)

Firstly as you try to enter to our website, every page on it starts with “preloader” that was implemented by JavaScript and this loader will wait until whole page components are loaded.

Then, first page will be showed as following pictures:

![](meta/iut_lms_report_html_b49e45d41c4301b1.jpg)

![](meta/iut_lms_report_html_57faf7de2c9a214.jpg)

![](meta/iut_lms_report_html_767ff31463e8de04.jpg)

![](meta/iut_lms_report_html_e76d89838e3e1f6c.jpg)

As you see first index page includes “Most popular books” with animation owl-carousel. Every cover page of most popular books that is on carousel is taken from database, “books” table according to their ranks that
members was given.

Also, recently added books’ cover pages will be shown that followed brief information about IUT-LMS, after that Service, Entertainment, Audio books block give references to resources.

And lastly, every page includes navigation bar, which has page options Home, Catalogue, Textbooks, About and Login and additional options based on types of user logged in, and footer part which include all contact information and addresses with location that is implemented by API of the Google map.

![](meta/iut_lms_report_html_ecc5861aa95dba6.jpg)

When you try to login to our page by pressing “Login” button on the corner, you will see Authentication page, then you can enter by passing your UserID and Password that has already been given by Librarians. There you can see “Remember Me” checkbox, if you mark it, every time when you login to your account it saves your records.

![](meta/iut_lms_report_html_4c68ec3ae5eac632.jpg)

After you logged in to your account you will see default “Dashboard” page that illustrates current statistics of the system. Then you will have reference options (with dashboard) Personal Info, Change Password, and Log out.

![](meta/iut_lms_report_html_11cec52fe0e5585f.jpg)

Here you see, there is a personal information of the user

![](meta/iut_lms_report_html_48fe234e8ca71f38.jpg)

Changing password page. First user should enter current password and then new password after all he/she should confirm it

![](meta/iut_lms_report_html_63cf3346d570b532.jpg)

Here is a catalog page, and here user can see all books with some book information and search them

![](meta/iut_lms_report_html_561101c346fae876.jpg)

And as you see here at the end of the page it displays books with pagination and every page displays 10 book items per page

![](meta/iut_lms_report_html_f8f616fb79a07494.jpg)

Individual book description page and here you can download if user is singed

![](meta/iut_lms_report_html_591bfc2a683365e3.jpg)

Also in this page you can leave comment to this book

![](meta/iut_lms_report_html_5a0cfd08e8068eb7.jpg)

Here you can download the book item

![](meta/iut_lms_report_html_8ee5980a4988b47b.jpg)

Here is a text book page. In this page you can see all text books which is used in both first and second semesters in a year for 4 courses. As well as, we should inform that this page is currently not dynamic and not linked to database. For the future, we will finish this.

![](meta/iut_lms_report_html_6f6ac63a3a0f4ac5.jpg)

![](meta/iut_lms_report_html_2409e966a82e4c54.jpg)

This page informs you about iut library. Here you can see rules of iut library

![](meta/iut_lms_report_html_64237de8d53be2ce.jpg)

Validated login page checks the user ID and password and if it is not matched it will gives error message

![](meta/iut_lms_report_html_7b8c2c2d734c7fd5.jpg)

Here is personal page of the librarian and you can see some addition features at navigation bar .

![](meta/iut_lms_report_html_be87744347ed36f1.jpg)

![](meta/iut_lms_report_html_5e5d5cca4b92bbc4.jpg)

This is the table which is provides all list of books

![](meta/iut_lms_report_html_a9e715d8b3a4faae.jpg)

![](meta/iut_lms_report_html_a1228f80623eda0e.jpg)

This page is to add books as you can see

![](meta/iut_lms_report_html_7ebe851f776221c5.jpg)

Here is a page of all list of member who enrolled in iut library database

![](meta/iut_lms_report_html_91d703a48f4d344d.jpg)

This is a page to enroll new user of our website

![](meta/iut_lms_report_html_f112f9b8713d4ff.jpg)

At the bottom of our website you can get acquainted with contact information and location in the map which is used by API of the google services.

Database Schema:

Users Table

![](meta/iut_lms_report_html_630a92443ddd93bf.jpg)

Books Table

![](meta/iut_lms_report_html_f6caeafac62d4818.jpg)

Genre column should be provided in the case that bookType = ‘Literature’, Similarly, if bookType is equal to ’Textbook’, then semester should be provided. And This way we can use this current table for bookType = ‘Literature’ | ‘Science’ | ‘Textbook’ | ‘Others’

![](meta/iut_lms_report_html_f9317324f12d2118.jpg)

Exception and Routing of 404 not found page was done by Rakhmatjon Khasanov

Template of these given page was fully decorated and written by Sardor Allaberganov

Comments Table

![](meta/iut_lms_report_html_5b9ff8eba4e5eaf1.jpg)

Genres Table

![](meta/iut_lms_report_html_8bcbd2130c1e966.jpg)

Relation between Genres and Books

![](meta/iut_lms_report_html_ccc7f2bdc54a45c3.jpg)

With above given tables we can easily related books with genres and we can say that each book can have multiple genres.

**Contributions of members:**

1.  **Sardor Allabergenov**
    - made page design and dashboard pages, profile pages. Worked on appearance of the website and client – side part. Applied google map API in the footer. Constructs the page layouts with the javascript ,css and using the framework like jquery, bootstrap and some instruments like owl carousel.

2.  **Rakhmatjon Khasanov**
    - Login and Members, Books, Pages, and Comments Models and Controllers.
    - Relation with Books and Users and Comments.
    - Validation for the inputs and securing the from request like get, post, put, delete and other headers of http request.
    - Ensuring simple users, students and teachers, can’t access others files and personal info, except they can see each others’ comments.
    - Embedding Controllers, Routes and Views(‘blades’)
    - Migration that related to the ones I mentioned above

3. **Shokhsanam Shirinkulova**
   - Mostly, Embedding the blades, models and controllers
   - Migration of Genre and relation between books and genres and adding some the columns to tables which are clear from migrations folder.
   - Embedding Show page for book Details and so on.

4. **Madina Kurbanova**
   - made some inputs and pages catalog page with Sardor Allabergenov. Works with styling this page. Constructs the adding book page using bootstrap styles and own styles.

5. **Madinakhon Raufova**
   - made text Book page using the bootstrap styles and own styles. Works on hovering book name on this page and grid the of this page made by her. 

There are some limitations in our website because of time. We think more features and implement them just statically and some pages we cannot reach at all. But in future we trying to improve and complete them.

