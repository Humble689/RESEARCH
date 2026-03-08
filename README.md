# Microservices Research

## What Are Microservices?

Microservices are a software architecture style in which an application is built as a collection of small, independent services. Each service is responsible for a specific business function and communicates with other services through lightweight APIs or messaging.

Instead of putting all functionality into one large monolithic application, microservices split the system into smaller parts that can be developed, deployed, scaled, and maintained separately.

### Main characteristics of microservices

- Each service focuses on one business capability.
- Services can be deployed independently.
- Different services can scale independently.
- Teams can work on separate services at the same time.
- A failure in one service does not always bring down the entire system.

## 1. How Netflix Uses Microservices

Netflix uses microservices as a collection of small, independently deployable services instead of one large monolithic application. Each service is responsible for a specific business capability, such as user accounts, recommendations, content metadata, playback-related features, or operational platform functions.

### How Netflix applies microservices

- Services are independently deployable, so one team can update a service without redeploying the entire platform.
- Services can scale independently, which is critical because some workloads, such as streaming support, recommendations, or metadata access, may require far more resources than others.
- Netflix uses a cloud-first operating model on AWS, which helps it provision infrastructure quickly and support global scale.
- The company is known for resilience patterns such as circuit breakers, fault isolation, and chaos engineering.
- Netflix popularized failure-testing tools such as Chaos Monkey and the broader Simian Army approach to make sure systems can survive service or infrastructure failures.
- Teams follow a build-it/run-it model, meaning the same teams that develop services are also responsible for operating them in production.
- Netflix relies heavily on automation for deployment, monitoring, and recovery because managing many distributed services manually would be too slow and error-prone.

### Why Netflix adopted microservices

Netflix moved toward microservices to solve problems of scale, speed, and reliability.

- A monolithic system would make frequent releases harder and riskier.
- A failure in one part of a large system could have a bigger blast radius.
- Different parts of the platform need different scaling behavior.
- Many engineering teams need to work in parallel without blocking one another.
- Global streaming demand requires strong fault tolerance and automated operations.

### Main benefits Netflix gets

- Faster feature delivery
- Better fault isolation
- Independent scaling
- Greater team autonomy
- Stronger resilience in distributed cloud environments

## 2. Two Other Companies That Used Microservices

## Uber

Uber adopted microservices after outgrowing its early monolithic systems.

### Why Uber changed

According to Uber Engineering, the company experienced several problems with its monolithic architecture as it grew:

- Availability risks: a single regression could affect the whole system.
- Risky and expensive deployments: releases were painful and rollbacks were common.
- Poor separation of concerns: a very large codebase made boundaries unclear.
- Reduced team autonomy: as engineering teams multiplied, the monolith tied teams together.

### What changed after the move

Uber says microservices improved:

- System reliability
- Clear ownership of services
- Autonomous execution by teams
- Developer velocity
- Independent deployment and scaling

As Uber later grew to thousands of microservices, complexity became a new challenge. To address that, Uber evolved its architecture further into Domain-Oriented Microservice Architecture (DOMA), which groups related services into domains and adds gateways to reduce dependency sprawl.

## LinkedIn

LinkedIn also moved away from a monolithic architecture as traffic, features, and engineering complexity increased.

### Why LinkedIn changed

LinkedIn originally ran a monolithic application called Leo. As the platform grew, LinkedIn found that:

- The monolith was becoming too complex.
- Production outages were harder to troubleshoot and recover from.
- Releasing new code became difficult.
- Core systems, especially databases, were under increasing load.
- Some functions needed to scale independently from the main application.

### What changed after the move

LinkedIn began extracting specialized services such as the member graph and search, then expanded this into a broad service-oriented architecture with many small stateless services.

This gave LinkedIn:

- Independent scaling of critical functions
- Better availability
- Easier recovery from failures
- More manageable releases
- Better support for rapid growth across products and teams

## 3. Comparison Summary

Netflix, Uber, and LinkedIn all adopted microservices for similar high-level reasons, but their triggers were slightly different.

- Netflix changed mainly for global scale, resilience, and rapid delivery.
- Uber changed because monoliths were slowing team execution and increasing operational risk.
- LinkedIn changed because its monolith became unstable, hard to release, and difficult to scale.

In all three cases, microservices helped by separating systems into smaller services that could be deployed, scaled, and operated more independently.

## 4. Sources

1. Martin Fowler and James Lewis, "Microservices"
   - https://martinfowler.com/articles/microservices.html
2. AWS Customer Story, "Netflix on AWS"
   - https://aws.amazon.com/solutions/case-studies/netflix/
3. Uber Engineering, "Introducing Domain-Oriented Microservice Architecture"
   - https://www.uber.com/blog/microservice-architecture/
4. LinkedIn Engineering, "A Brief History of Scaling LinkedIn"
   - https://engineering.linkedin.com/architecture/brief-history-scaling-linkedin
