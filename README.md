# Course homework

This repository maps the course homework assignments.

To learn more about the schedule of the these assignments, visit the [course repository](https://github.com/course-go/course).

## Homework assignments

1. EGG [[assignment](https://github.com/course-go/egg)]
    - Implement a grep-based CLI tool
2. Barbershop [[assignment](https://github.com/course-go/barbershop)]
    - Implement the Sleeping barber problem
3. ReelGoofy: REST API & Testing [[assignment](https://github.com/course-go/reelgoofy)]
    - Implement and test REST API for a recommendation service
4. ReelGoofy: Containerization & Persistence [[assignment](https://github.com/course-go/homework/blob/master/04-reelgoofy-persistence/README.md)]
    - Containerize the service using Docker
    - Implement persistence
5. ReelGoofy: CI/CD & Telemetry [[assignment](https://github.com/course-go/homework/blob/master/05-reelgoofy-observability/README.md)]
    - Create pipeline using GitHub Actions
    - Set-up basic monitoring using Prometheus and Grafana

## Evalution

The following table summarizes how many points can be received
for each assignment.

| Assignment            | Points |
| :---------------------| :----: |
| EGG                   | 7      |
| Barbershop            | 7      |
| ReelGoofy REST API    | 12     |
| ReelGoofy Persistence | 12     |
| ReelGoofy Telemetry   | 12     |

## General guidelines and submission workflow

### Workflow

The submission flow slightly differs based on the homework type.
Some have dedicated templates and some build upon the previous assignment.

- For assignments with dedicated templates, create a new **private** repository
using the template. Then add your tutors to the repository so they can later
provide your with a review. Switch to your submit branch and implement your solution
there. When you are finished, create a pull request from this submit branch to your
main branch and assign it to you tutors.

- For assignments based on a previous assignment, continue with the same repository
using a different git branch.

One problem, you might stumble upon, is when you have two consecutive assignments
and the first one is not yet merged to the main branch (e.g. you are waiting
for a review for the first assignment and you already want to start
working on the second one). In that case, the suggested way to work is that
you create a git branch for the second assignment from the
first, not yet merged, assignment branch. After your first assignment
gets approved, merge it and rebase the second assignment branch.

### Guidelines

- Do not merge your pull requests until you are instructed to do so.
- All solutions must comply with the Go formatter.
- If the homework skeleton contains a continuous integration pipeline it
must successfully pass.
- If the assignment contains tests they also have to pass.
- If any of your solutions become public, you will be issued a penalty.
