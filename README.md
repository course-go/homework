# Course homework

This repository maps the course homework assignments.

To learn more about the schedule of the these assignments, visit the [course repository](https://github.com/course-go/course).

## Homework assignments

All assignments are grouped by their domain or topic they exercise.
The suggested approach, if you want to follow the course design, is to
pick a single assignment from each topic.

Be aware that some of the assignments are linked to each other. I.e. they
build upon the solution of the previous assignment.

1. CLI tools
    - EGG [[assignment](https://github.com/course-go/egg)]
        - Implement a grep-based CLI tool
2. Concurrency & Parallelism
    - EGG Currency [[assignment](https://github.com/course-go/homework/blob/master/02-egg-currency/README.md)]
        - Implement concurrent file processing for EGG
    - Barbershop [[assignment](https://github.com/course-go/barbershop)]
        - Implement the Sleeping barber problem
3. REST API & Testing
    - ReelGoofy: REST API & Testing [[assignment](https://github.com/course-go/reelgoofy)]
        - Implement and test REST API for a recommendation service
4. Containerization & Persistence
    - ReelGoofy: Containerization & Persistence [[assignment](https://github.com/course-go/homework/blob/master/04-reelgoofy-persistence/README.md)]
        - Containerize the service using Docker
        - Implement persistence
5. CI/CD & Telemetry
    - ReelGoofy: CI/CD & Telemetry [[assignment](https://github.com/course-go/homework/blob/master/05-reelgoofy-observability/README.md)]
        - Create pipeline using GitHub Actions
        - Set-up basic monitoring using Prometheus and Grafana

## Evaluation

Any combination of assignments by their respective topics, as described
in the previous paragraph, should make up 50 points in total. Some assignments
provide bonus tasks. For these bonus tasks
you can acquire bonus points that are equivalent to the standard points.

The following table summarizes how many points can be received
for each assignment:

| Assignment            | Points | Bonus points |
| :---------------------| :----: | :----------: |
| EGG                   | 7      |      0       |
| EGG Currency          | 7      |      3       |
| Barbershop            | 7      |      2       |
| ReelGoofy REST API    | 12     |      5       |
| ReelGoofy Persistence | 12     |      0       |
| ReelGoofy Telemetry   | 12     |      0       |

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

- Do not merge your pull requests until your reviewer approves it or
you are explicitly instructed to do so.
- All solutions must comply with the standard Go formatter.
- If the homework skeleton contains a continuous integration pipeline it
must successfully pass.
- If the assignment contains tests they also have to pass.
- If any of your solutions become public, you will be issued a penalty.
