# To-Do List Management App

## Overview
The **To-Do List Management App** is a feature-rich application designed to help users manage their daily tasks efficiently. It combines a modern, professional UI with a robust back-end architecture, offering functionalities like secure user authentication, task creation, editing, deletion, and real-time updates. The application is built with industry best practices and technologies to deliver a responsive and seamless user experience.

---

## Features

### User Authentication
- Secure login and registration functionality using **JWT (JSON Web Tokens)**.
- Passwords are securely hashed for added security.

### Task Management
- **Create Tasks**: Users can add new tasks with attributes such as title, description, status, priority, and due date.
- **Edit Tasks**: Modify task details in real-time with an intuitive form-based interface.
- **Delete Tasks**: Remove tasks permanently.

### Empty State Handling
- A visually engaging empty state is displayed when there are no tasks, including a relaxing animation and a friendly message: *"You're all caught up!"*.

### Task List Display
- Tasks are displayed in a clean grid format with hover animations and visually distinct action buttons.
- Task cards include details like title, description, status, priority, and due date.

### Professional and Responsive Design
- The application uses a **consistent color scheme** across all pages, creating a cohesive and polished look.
- Fully responsive layout that adapts to various screen sizes, ensuring usability on desktops, tablets, and mobile devices.

---

## Best Practices Followed

### Front-End
- **React.js with Modular Components**: Code is split into reusable and testable components.
- **CSS Optimization**: Consistent styling with SCSS and Bootstrap to ensure scalability and maintainability.
- **State Management**: Tasks and user authentication are managed efficiently using React hooks and context.

### Back-End
- **Separation of Concerns**: API endpoints for authentication and task management are logically organized.
- **Error Handling**: Comprehensive error responses to guide the user when operations fail.
- **Secure Communication**: Usage of HTTP-only cookies for session management and environment variables for sensitive data.

### UI/UX
- **Interactive Design**: Hover effects and animations for buttons and cards to enhance interactivity.
- **Accessibility**: Components and forms are designed to be user-friendly and accessible.

---

## Technologies Used

### Front-End
- **React.js**: For building the user interface.
- **Bootstrap**: For responsive and modern UI components.
- **SCSS**: For customized and scalable styling.

### Back-End
- **Node.js with Express**: For building API endpoints.
- **SQLite**: Lightweight and efficient database management.
- **JWT**: For secure authentication.

### Additional Tools
- **Axios**: For making API requests.
- **Regex**: For input validation in the front-end and back-end.
- **Nodemon**: For back-end live reloading during development.



---

## Project Structure

```
project-root/
│
├── backend/
│   ├── controllers/
│   ├── db/
│   ├── middleware/
│   ├── routes/
│   ├── server.js
│   ├── .env
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── styles/
│   │   └── App.js
│   ├── public/
│   └── package.json
│
├── README.md
└── .gitignore
```

## Getting Started

### Prerequisites
Ensure you have the following installed:
- **Node.js** (v16+ recommended)
- **npm** or **yarn**
- **SQLite** (configured as part of the backend)

### Installation

1. Clone the repository:
```
git clone https://github.com/kusumanth7329/Task-it-management-app.git
```

2. Navigate to the project folder:
```
cd Task-it-management-app
```

3. Install dependencies for both the front-end and back-end:
```
# Back-end
#unzip the backend file
unzip backend.zip -d backend
#navigate to the zip file and install
cd backend
npm install

# Front-end
#unzip the backend file
unzip frontend.zip -d frontend
cd ../frontend
npm install
```

## Running the Application

1. start the back-end server:
```
cd backend
npm start
```

3. In a separate terminal, start the front-end application:
```
cd frontend
npm start
```

## Development

### Front-End
- **Location:** /frontend
- **Entry Point:** src/index.js
- **Important Scripts:**
  - npm start: Runs the app in the development mode.
  - npm test: Launches the test runner.
  - npm run build: Builds the app for production to the build folder.

### Back-End
- **Location:** /backend
- **Entry Point:** server.js
- **Important Scripts:**
  - npm start: Starts the Node server.
  - npm run dev: Starts the server with nodemon for live reloading.

## Key Pages
### Login Page
- Features an off-white background with a gradient and a professional card-based form.
- Includes a footer with links to the designer's email and LinkedIn profile.
### Register Page
- Similar design to the Login Page with fields for user registration.
### Tasks Page
- Split layout: Task creation form on the left and task list on the right.
- Responsive grid layout for tasks with hover effects.
- Empty state with a relaxing animation when no tasks are present.


## Explanation of Design and Trade-Offs

### Design Philosophy
The design of the To-Do List Management App was driven by three primary goals:

1. **User-Centric Design**: Ensuring the application is intuitive, responsive, and visually appealing to provide a seamless user experience.
2. **Scalability and Maintainability**: Following modular architecture and clean coding practices to support future enhancements and ensure long-term maintainability.
3. **Performance and Security**: Optimizing performance by minimizing render cycles, reducing API calls, and incorporating secure authentication mechanisms.

---

### Front-End Design Decisions

1. **UI/UX Consistency**:
   - A consistent **color scheme** (shades of green and off-white) was chosen across all pages to provide a professional and unified look.
   - Components such as headers, footers, and task cards were styled similarly to maintain a cohesive user experience.
   - The responsive design ensures usability across devices without sacrificing aesthetics.

2. **Form Validation**:
   - **Regex patterns** were implemented for email and password validation on the front-end to prevent invalid submissions and improve user experience.
   - This reduces unnecessary API calls by catching errors early.

3. **Empty States**:
   - When no tasks are available, a visually engaging empty state is displayed with an animation and a friendly message. This avoids leaving the page visually "empty" and improves engagement.

4. **Grid Layout for Tasks**:
   - Tasks are displayed in a **grid layout** to utilize screen space effectively, especially on larger devices.
   - The cards are designed with hover effects and animations to improve interactivity and aesthetic appeal.

---

### Back-End Design Decisions

1. **Separation of Concerns**:
   - APIs for authentication and task management were logically separated into different controllers and routes.
   - Middleware was used for common functionalities like error handling and authentication.

2. **SQLite Database**:
   - SQLite was chosen as the database for its simplicity and lightweight nature, making it suitable for a small-scale project. 
   - However, this could be upgraded to a more robust database like PostgreSQL or MongoDB for scalability in a production environment.

3. **JWT Authentication**:
   - Secure, stateless authentication was implemented using JSON Web Tokens (JWT). While this ensures secure session management, trade-offs include requiring token storage on the client-side, which must be managed securely (e.g., HTTP-only cookies).

---

### Trade-Offs

1. **Front-End Framework**:
   - **React.js** was chosen for its component-based architecture and ability to manage state effectively. While React is heavier than simpler frameworks, it provides greater flexibility and scalability for this application.

2. **Styling Approach**:
   - The app uses a combination of **CSS**, **SCSS**, and **Bootstrap** for styling. While SCSS adds complexity compared to plain CSS, it ensures scalability and allows for easier management of styling variables and nested selectors.

3. **Database Selection**:
   - **SQLite** was used for simplicity, but it lacks support for high concurrency and advanced scaling, which would be necessary in a production environment with many users.

4. **No Real-Time Updates**:
   - The app does not include real-time task updates (e.g., using WebSockets or polling). While this simplifies the architecture and reduces server load, it sacrifices real-time collaboration features.

5. **Error Handling**:
   - The app handles most common errors, but it could be extended to provide more detailed feedback for edge cases (e.g., server timeouts or network interruptions).

---

### Future Improvements

1. **Real-Time Updates**:
   - Incorporate WebSockets for real-time task updates and notifications.
2. **Enhanced Filters**:
   - Add advanced filtering and search capabilities (e.g., by priority, due date range).
3. **Accessibility**:
   - Ensure WCAG compliance by enhancing accessibility features such as keyboard navigation and screen-reader compatibility.
4. **Scalability**:
   - Transition to a more scalable database (e.g., PostgreSQL) and a cloud-based deployment strategy (e.g., AWS or Azure).
5. **Internationalization**:
   - Add support for multiple languages to cater to a global audience.

This design achieves a balance between simplicity, functionality, and professional aesthetics, while remaining flexible enough to accommodate future enhancements.
