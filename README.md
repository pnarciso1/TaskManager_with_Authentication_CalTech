This project implements a Task Manager application with user authentication in Python, designed to run in a Jupyter Notebook environment. The system allows users to register, login, and manage their personal tasks with full CRUD (Create, Read, Update, Delete) capabilities.
Architectural Approach
I approached this project using domain-driven design principles, focusing first on modeling the core domain entities before implementing the technical details. This allowed me to build a clean, maintainable, and extensible codebase.
TypeScript-Inspired Design Pattern
Although this project is implemented in Python, I deliberately adopted a TypeScript-like approach,  The personal reason for taking this approach is because I am writing predominantly in TypeScript and wanted to maintain my personal style.  I also did it for several, more functional reasons:
1.	Type Safety and Documentation: I leveraged Python's type hints to create clear interfaces similar to TypeScript declarations, making the code self-documenting and easier to understand.
2.	Domain Modeling: I defined explicit typed structures for our domain models (User, Task) that clearly communicate the shape of our data.
3.	Interface-First Development: By defining TypedDict classes, I created contract-like interfaces between components similar to TypeScript interfaces.
4.	Modularity: The TypeScript approach encouraged me to think in terms of modules with clear responsibilities, resulting in better separation of concerns.
Repository Pattern
I implemented the repository pattern to abstract data persistence:
•	Each repository class encapsulates all data access logic
•	The application core remains decoupled from the storage mechanism
•	This approach simplifies potential future changes to storage (e.g., switching to a database)
Service Layer
The service layer implements business logic and acts as an intermediary between repositories and the UI:
•	AuthenticationService handles user registration, login, and session management
•	TaskService manages tasks for the authenticated user
•	This separation allows for clean unit testing and better maintainability
User-Centric Data Isolation
For security and data isolation:
•	Each user's tasks are stored in a separate file
•	Passwords are hashed using SHA-256
•	The application prevents unauthorized access to other users' tasks
Benefits of the Approach
1.	Maintainability: The code is structured into logical components with clear responsibilities
2.	Extensibility: New features can be added with minimal changes to existing code
3.	Testability: The separation of concerns makes unit testing straightforward
4.	Security: Proper password hashing and user data isolation protect user information
5.	Domain Focus: The implementation focuses on the core domain concepts rather than technical details
By combining domain-driven design with TypeScript-inspired patterns in Python, I created a robust Task Manager application that prioritizes code quality, security, and user experience. 

![image](https://github.com/user-attachments/assets/3deaf237-533f-43a8-accf-0bda1d8c42e8)
