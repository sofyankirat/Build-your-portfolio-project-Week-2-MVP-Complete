hurchConnect - Church Member Management and Community Platform
ChurchConnect is a web application built using Laravel and MySQL, designed to enhance communication and interaction among church members. It provides church administrators with tools to manage member accounts, publish blog posts, schedule events, and facilitate community engagement through ministry pages and real-time group chats.

Table of Contents
Project Overview
Features
Technology Stack
Installation
Configuration
Usage
API Documentation
Data Model
Contributing
License
Project Overview
ChurchConnect is designed to be a comprehensive platform for church administration and member interaction. The platform allows church admins to create and manage member accounts, share updates via blogs and event pages, and facilitate discussions through comments and group chats. The platform also supports mass emailing, making it easier for church leaders to keep in touch with their congregation.

Features
Admin Account Creation: Church admins can create and manage accounts for new members.
Ministry Pages: Dedicated pages for each ministry, with options for members to view updates and leave comments.
Blog Posts: Admins can create and publish blog posts, and members can comment on these posts.
Event Management: Schedule events that members can view and discuss.
Real-Time Group Chat: A chat feature allowing members to communicate in real-time within the platform.
Bulk Emailing: Admins can send emails to all registered members.
Technology Stack
Frontend: HTML, CSS, JavaScript, Bootstrap
Backend: Laravel (PHP Framework)
Database: MySQL
Real-Time Communication: WebSockets with Laravel Echo and Ajax
Email Service: Laravel Mail with Mailgun
Installation
Prerequisites
PHP 8.0 or higher
Composer
MySQL
Node.js & npm
jQuery and Ajax for real-time chat
SMTP Mail.com account for email service
Steps
Clone the repository:

git clone https://github.com/EliezerSunny/ChurchConnect.git
cd ChurchConnect
Install dependencies:

composer install
npm install
Set up environment variables:

Copy the .env.example file to .env and update the necessary fields:

cp .env.example .env
Generate the application key:

php artisan key:generate
Set up the database:

Update the .env file with your database credentials and run the following commands:

php artisan migrate
php artisan db:seed
Install front-end dependencies:

npm install
npm run dev
Start the development server:

php artisan serve
Configuration
jQuery/Ajax: Adding jquery and ajax in the code.
SMTPMail: Set up a Mail account and configure the Mail settings in the .env file.
Usage
Access the platform by navigating to http://localhost:8000 in your web browser.
Log in as an admin to create new member accounts, manage blogs, events, and ministries.
Registered members can log in to comment on blogs, interact in ministry pages, and participate in group chats.
API Documentation
ChurchConnect includes a set of APIs for managing users, posts, events, and chats. These APIs allow for integration with other services or apps.

Example Routes
User Management

POST /divine_help/add_member: Register a new user Add Member

POST /signin: Log in a user Login page

Blog Management

GET /blogs: Fetch all blogs Blog post

POST /divine_help/add_post: Create a new blog post (Admin only) Add Post

Event Management

GET /events: Fetch all events Event Post
POST /divine_help/add_post: Create a new event (Admin only) Add Post
Chat

GET /divine_help/chat: Get chat messages Group Chat
POST /divine_help/chat: Send a new chat message Send Message
Data Model
The data model consists of tables for users, blogs, comments, ministries, events, and chat messages. Each table is related through keys that define the interactions within the platform. Data Model

Contributing
Contributions are welcome! Please fork this repository and submit a pull request with your changes. Make sure to follow the coding standards used throughout the project.
