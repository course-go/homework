# ReelGoofy: Containerization & Persistence

ReelGoofy is movie recommendation service.

## Assignment

ReelGoofy's API was implemented in [the previous homework](https://github.com/course-go/homework/tree/master/03-reelgoofy-api).
This homework follows up on the on it.
You goal will be to containerize the application, add database
using Docker compose and implement the persistence layer.

As with the router technology in previous assignment, the choice
of the "persistence" library is again up to you.
Here are the technologies that were presented in lectures:

- [databases/sql](https://pkg.go.dev/database/sql) with a driver of your choice
- [sqlx](https://github.com/jmoiron/sqlx)
- [sqlc](https://github.com/sqlc-dev/sqlc)
- [GORM](https://github.com/go-gorm/gorm)

Whatever your choice will be, document it in the `REASONING.md` file.
Describe why you chose the library, what did you like about it, what
additional features it offers compared to the standard library etc.

### Specification

#### Containerization

##### Container image for API

Create a [Dockerfile](https://docs.docker.com/reference/dockerfile/) for
building the container image for the API.

The Dockerfile should be multistage to decrease the image size, that is:

- it should only contain the final binary
- it shouldn't contain any source code or Go tooling such as the compiler etc.

##### Compose for running the application

Create a [Docker Compose](https://docs.docker.com/compose/) for
running the application with all of its dependencies.

The compose should contain two service definitions:

- one service for the API built using the Dockerfile created earlier and
- one service for the database.

Note that you will need to mount a volume for the database to persist its data.

#### Persistence

Replace the previously implemented in-memory storage with persistent one.
For this, you can choose whatever relational database system
you like, but [PostgreSQL](https://hub.docker.com/_/postgres) is recommended.
As previously mentioned, the library used is also up to you.

If you choose to use a different database system
than PostgreSQL, provide a reasoning in the `REASONING.md` file.

### Bonus

Reuse your in-memory storage created in the previous assignment as a local cache
for all of the database data. For example, you can preload all of your data at
the start of the application and only query the database when altering records.

Please note, that while this approach will save you trips to the database, it isn't
really scalable. If you would like to scale the API with such cache, you will
have to deal with some kind of cache data synchronization or invalidation.
However, as this is rather complex issue, you can safely ignore it in this assignment.
Same goes for any "memory size issues", i.e. you can expect that the stored data
is reasonably big.

You can earn up to **4 points** for implementing this bonus.

## Requirements

The application is runnable by executing `docker compose up` command
and it persists its data using the database system and the library of your choice.

## Motivation

The goal of this homework is to practice
implementing a persistence layer using the Go ecosystem and its libraries
and to containerize and setup a basic compose file for the application and its dependencies.
