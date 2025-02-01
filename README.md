# Book Search Engine
Description
The Book Search Engine is an app that allows users to search for books, save their favorite books, and view them later. Originally built with a RESTful API, this app has been refactored to utilize a GraphQL API using Apollo Server. It is built with the MERN stack: MongoDB, Express.js, React, and Node.js. The app also supports user authentication, allowing users to sign up, log in, and save their book searches to their account.

User Story
As an avid reader,
I want to search for new books to read
So that I can keep a list of books to purchase.

Acceptance Criteria
Search Interface: When loading the search engine, users are presented with options to "Search for Books" and "Login/Signup," along with an input field for book search.
Book Search: Users can search for books and view results with titles, authors, descriptions, images, and links to Google Books.
Authentication: Users can sign up with a username, email, and password, or log in with their credentials.
Save Books: Logged-in users can save books to their account, viewing them on a separate page.
Saved Books: Users can remove saved books from their list and log out.
Key Features
GraphQL API: The backend uses Apollo Server to serve GraphQL queries and mutations for interacting with the database and Google Books API.
Authentication: User authentication allows for secure account creation, login, and saved books management.
Save and Remove Books: Users can save books to their account and remove them as needed.
Mock-Up
The app features a search input where users can type a book name. Upon clicking the "Search for Books" button, the app fetches results showing a book's title, author, description, image, and a link to its Google Books page. Users can click "Save This Book!" to save the book to their account, with a button that changes to "Book Already Saved" once saved. Users can view their saved books on a separate page.

Getting Started
Prerequisites
Node.js and npm installed
MongoDB Atlas account for database hosting
Apollo Server and MongoDB libraries
Installation
Clone the repository:

bash
Copy
Edit
git clone <repository-url>
cd <project-directory>
Install dependencies:

Back end:

bash
Copy
Edit
cd backend
npm install
Front end:

bash
Copy
Edit
cd frontend
npm install
Set up MongoDB Atlas:

Create a MongoDB Atlas cluster.
Get the connection string and add it to .env files on both front and back ends.
Run the app locally:

Start the backend server:
bash
Copy
Edit
cd backend
npm start
Start the frontend development server:
bash
Copy
Edit
cd frontend
npm start
Deploy to Render:

Follow the Render deployment guide to deploy your app.
Use MongoDB Atlas for database hosting.
Back-End Modifications
auth.ts: Update the authentication middleware to integrate with GraphQL.
server.ts: Set up Apollo Server and integrate it with Express.
Schemas Directory:
Define types (Query, Mutation, User, Book, Auth).
Implement resolvers to handle queries like me, mutations like login, addUser, saveBook, and removeBook.
Front-End Modifications
queries.ts: Define GraphQL queries like GET_ME for fetching the logged-in user.
mutations.ts: Define mutations like LOGIN_USER, ADD_USER, SAVE_BOOK, REMOVE_BOOK.
App.tsx: Set up Apollo Provider to communicate with Apollo Server.
SearchBooks.tsx: Use Apollo's useMutation hook to save books and display results.
SavedBooks.tsx: Use Apollo's useQuery hook to fetch saved books and useMutation to remove them.
SignupForm.tsx: Use Apollo's ADD_USER mutation for signup.
LoginForm.tsx: Use Apollo's LOGIN_USER mutation for login.
Technologies Used
MongoDB: NoSQL database for storing user information and saved books.
Apollo Server: For GraphQL API.
React: Front-end user interface.
Express.js: Web server.
Node.js: JavaScript runtime.
Future Enhancements
Add search filters (e.g., by genre, year, etc.).
Improve the UI with more interactivity and animations.
Add support for multiple user accounts and profiles.
Contributing
Fork the repository
Create a feature branch (git checkout -b feature/feature-name)
Commit your changes (git commit -m 'Add feature')
Push to the branch (git push origin feature/feature-name)
Open a pull request
License
This project is licensed under the MIT License - see the LICENSE file for details.
