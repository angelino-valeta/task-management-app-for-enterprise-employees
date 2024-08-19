# task-management-app-for-enterprise-employees
A task management system developed with Angular for the frontend and Adonis 5 for the 
backend, following hexagonal architecture principles.

## Overview

The Task Management System allows employees of a company to assign and move tasks between each other. Key features include:


- Task assignment between employees
- Email notification when an employee receives a task
- Email notification when a task is moved to another employee
- Responsive web interface built with Angular
- RESTful backend API built Adonis 5
- Implementation of hexagonal architecture for better separation of concerns


## Technologies Used

- Frontend: Angular 14+
- Backend: Adonis 5
- Database: Mysql
- Architecture: Hexagonal (Ports and Adapters)

## Project Structure

### Backend (Adonis 5)


src/
  application/
    ports/
      driver/
        TaskManagementPort.ts
      driven/
        TaskPersistencePort.ts
        NotificationPort.ts
    services/
      TaskManagementService.ts
  domain/
    Task.ts
    User.ts
  infrastructure/
    adapters/
      persistence/
        MySQLTaskRepository.ts
        InMemoryTaskRepository.ts
      notification/
        EmailNotificationAdapter.ts
        MockNotificationAdapter.ts
    web/
      controllers/
        TaskController.ts
      routes/
        tasks.ts
  tests/
    integration/
      TaskManagement.spec.ts

### Frontend (Angular)

src/
  app/
    core/
      models/
        task.model.ts
      services/
        task.service.ts
    features/
      task-list/
        task-list.component.ts
        task-list.component.html
      task-create/
        task-create.component.ts
        task-create.component.html
      task-detail/
        task-detail.component.ts
        task-detail.component.html
    shared/
      components/
        header/
          header.component.ts
          header.component.html
    app.module.ts
    app.component.ts
    app.component.html



## Setup and Installation

#### Prerequisites

- Node.js (v14+)
- npm or yarn
- Mysql

#### Backend (Adonis 5)

1. Navigate to backend folder.

cd backend

2. Install dependencies:

npm install

3. Set up environment variables by copying the `.env.example` file to `.env` and adjusting the settings:

cp .env.example .env

4. Run database migrations:

5. Start the development server:

node ace server --watch


### Frontend (Angular)

1. Navigate to the frontend folder

cd frontend

2. Install dependencies:
npm install

3. Start the development server:
ng serve

4. Access the application at `http://localhost:4200`

After starting both the backend and frontend, you can:

1. Create a new task
2. View the list of tasks
3. Assign tasks to other users
4. Move tasks between users

Email notification will be sent automatically when tasks are assigned or moved.

## Testing

### Backend

Run tests using:
node ace test

### Frontend
Run tests using

ng test



## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add dome AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the Apache License - see the [LICENSE.md] file for details.

## Contact

Angelino Valeta - angelinovaleta@gmail.com

Project Link: https://github.com/angelino-valeta/task-management-app-for-enterprise-employees

