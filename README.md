# Tasks Backend

A Spring Boot REST API for managing task lists and tasks. This project has been instructed by [Devtiro](https://www.youtube.com/@devtiro).

## Features

- CRUD for Task Lists and Tasks
- Task priorities and statuses
- Progress calculation per list
- Error handling with meaningful responses

## Technologies

- Java 21+
- Spring Boot
- PostgreSQL (via Docker)
- Maven

## Getting Started

### Prerequisites

- Java 21 or newer
- Maven
- Docker (for PostgreSQL)

### Setup

1. **Start PostgreSQL:**
   ```sh
   docker-compose up -d
   ```
2. **Build and Run:**
   ```sh
   ./mvnw clean install
   ./mvnw spring-boot:run
   ```

### API Overview

#### Task Lists

- `GET /api/task-lists` — List all
- `POST /api/task-lists` — Create
- `GET /api/task-lists/{id}` — Retrieve
- `PUT /api/task-lists/{id}` — Update
- `DELETE /api/task-lists/{id}` — Delete

#### Tasks

- `GET /api/task-lists/{listId}/tasks` — List tasks
- `POST /api/task-lists/{listId}/tasks` — Create task
- `GET /api/task-lists/{listId}/tasks/{taskId}` — Retrieve task
- `PUT /api/task-lists/{listId}/tasks/{taskId}` — Update task
- `DELETE /api/task-lists/{listId}/tasks/{taskId}` — Delete task