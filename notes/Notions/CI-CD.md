# Continuous Integration - Continuous Delivery
CI/CD is a method to frequently deliver apps to customers by introducing automation into the stages of app development.

CI/CD is a solution to the problems integrating new code can cause for development and operations teams (AKA "integration hell").

Specifically, CI/CD introduces ongoing automation and continuous monitoring throughout the lifecycle of apps, from integration and testing phases to delivery and deployment.

Taken together, these connected practices are often referred to as a "CI/CD pipeline"

## Continuous Integration
Means new code changes to an app are regularly built, tested, and merged to a shared repository.

It’s a solution to the problem of having too many branches of an app in development at once that might conflict with each other.

## Continuous Delivery / Continuous Deployment
Both are about automating further stages of the pipeline, but they’re sometimes used separately to illustrate just how much automation is happening.

### Continuous Delivery

usually means a developer’s changes to an application are automatically bug tested and uploaded to a repository (like GitHub or a container registry), where they can then be deployed to a live production environment by the operations team.

It’s an answer to the problem of poor visibility and communication between dev and business teams. To that end, the purpose of continuous delivery is to ensure that it takes minimal effort to deploy new code.

### Continuous deployment (the other possible "CD")
can refer to automatically releasing a developer’s changes from the repository to production, where it is usable by customers.

It addresses the problem of overloading operations teams with manual processes that slow down app delivery.

It builds on the benefits of continuous delivery by automating the next stage in the pipeline.

![CI/CD Flow](https://www.redhat.com/cms/managed-files/styles/wysiwyg_full_width/s3/ci-cd-flow-desktop.png?itok=2EX0MpQZ "CI/CD Flow")