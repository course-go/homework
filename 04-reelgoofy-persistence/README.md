# ReelGoofy: Containarization & Persistence

ReelGoofy is movie recommendation service.

## Assignment

ReelGoofy's API was implemented in the previous homework. We will continue with this project throughout this and the following assignment. We will first containerize the application and then implement the persistence layer.

As with the router technology in previous assignment, the choice of the "persistence" library is again up to you. Here are the technologies that were presented in lectures:
- [databases/sql](https://pkg.go.dev/database/sql)
- [sqlx](https://github.com/jmoiron/sqlx)
- [sqlc](https://github.com/sqlc-dev/sqlc)
- [GORM](https://github.com/go-gorm/gorm)

Whatever your choice will be, document it in the `REASONING.md` file. Describe why you chose the library, what did you like about it, what additional features it offers compared to the standard library etc.

### Specification

#### Containerization

Create a Dockerfile for building a container image for the API. Follow it up with the creation of Docker Compose file.

#### Persistence

Replace the in-memory storage previously implemented with persistence layer. You can choose whatever RDBMS you would like, but [PostgreSQL](https://hub.docker.com/_/postgres) is recommended. Add its respective image to the compose file. If you choose to use a different database system then PostgreSQL, provide a reasoning the the markdown file.

## Requirements

The application is runnable by executing `docker compose up` command and it persists its data using the database system and library of choice.

## Motivation

The main goal of this homework is to practice implementing a persistence layer using the Go ecosystem and its libraries.
