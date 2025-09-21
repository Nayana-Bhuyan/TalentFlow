TalentFLOW – A Mini Hiring Platform

A Walkthrough Video Link of the project for easy understanding:
https://drive.google.com/file/d/1OEsiiRJGJHspTNKkc-8yVXMtsZzxHTUV/view?usp=sharing




Usage & Login Credentials
Once the application is running, navigate to the login page. You can use the following mock credentials to access the dashboard:
Email: abc@talentflow.com
Password: password123

In order to log out, click on the profile picture on the right top corner.
Delpoy link of the project : http://51.68.136.60:3002/





TalentFLOW is a front-end React application designed as a mini hiring platform. It provides HR teams with a comprehensive interface to manage job postings, track candidates through the hiring pipeline, and build custom job-specific assessments.

This project was built as a technical assignment to demonstrate core front-end development skills, including state management, API mocking, and building a responsive, feature-rich user interface.





Features

Job Management:
    Full CRUD (Create, Read, Update, Delete) functionality for job postings.
    Interactive drag-and-drop interface to reorder job listings.
    Advanced filtering and server-like pagination for efficient browsing.
    Optimistic UI updates for a seamless and responsive user experience.

Candidate Tracking:
    A virtualized list capable of efficiently rendering and searching through 1,000+ candidates.
    An interactive Kanban board to visually manage and move candidates through different hiring stages (Applied, Screening, Interview, etc.).
    Detailed candidate profile pages with timelines of their status changes.

Dynamic Assessments:
    An assessment builder to create custom, job-specific quizzes and forms.
    Support for multiple question types, including single-choice, multi-choice, text inputs, and file uploads.
    A live preview pane to see how the assessment will appear to candidates.
    Conditional logic to show or hide questions based on previous answers.





Tech Stack

Front-End: React, Vite, Tailwind CSS
API Mocking: Mock Service Worker (MSW)
Local Persistence:** Browser localStorage to simulate a database and persist state across sessions.
Routing: React Router
UI Components: Radix UI for accessible, unstyled primitives.





Setup and Installation

To run this project locally, follow these steps:

1.  Clone the repository:
    bash
    git clone [https://github.com/Nayana-Bhuyan/TalentFLOW.git](https://github.com/Nayana-Bhuyan/TalentFLOW.git)
    
2.  Navigate to the project directory:
    bash
    cd TalentFLOW
    
3.  Install dependencies:
    bash
    npm install
    
4.  Start the development server:
    bash
    npm run dev





Architecture

The application is structured as a modern, component-based React application.

API Simulation: To operate without a true back-end, the project uses *Mock Service Worker (MSW)*. MSW intercepts network requests and returns mock data, simulating a fully functional REST API. This allows for realistic data fetching, latency, and even error handling.
Data Persistence: All application data (jobs, candidates, assessments) is persisted in the browser's **localStorage**. This ensures that the application state is maintained across page refreshes, providing a robust user experience.
Component Structure: The UI is built with a clear separation of concerns, with reusable components located in the src/components directory. Shared UI primitives and utility functions are organized for maintainability.





Technical Decisions

Vite for Build Tooling: Vite was chosen for its fast development server and optimized build process, providing an excellent developer experience.
Tailwind CSS for Styling: Tailwind CSS was used for its utility-first approach, enabling rapid and consistent UI development without writing custom CSS.
MSW over other mocking libraries: MSW was selected because it operates at the network level, meaning the application code doesn't need to know it's interacting with a mock API. This makes the transition to a real API seamless.
Local Storage for Simplicity: While IndexedDB is a more powerful solution, localStorage was used for this project to simplify state persistence while still meeting the core requirement of maintaining data across sessions.





Known Issues & Trade-offs

As this is a front-end-only application, there is no real user authentication or database. All data is stored locally in the browser.
The virtualized list for candidates is implemented to handle a large dataset, but performance may vary depending on the browser and machine.
