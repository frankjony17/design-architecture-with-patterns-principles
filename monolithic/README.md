# Monolithic Architecture ([medium](https://medium.com/design-microservices-architecture-with-patterns/monolithic-architecture-is-still-worth-at-2021-98bfc112dc24))

![monolithic-architecture](/monolithic/images/monolithic-architecture.png)

When it comes to legacy applications, we can say that most of legacy applications are mainly implemented as a monolithic architecture. 
If all the functionalities of a project exists in a single codebase, then that application is known as monolithic application.

In the monolith pattern, everything from user interface, business codes and database calls is included in the same codebase. All application concerns are contained in a single big deployment. Even the monolithic applications can design in different layers like presentation, business and data layer and then deploy that codebase as single jar/war file.

<img src="/monolithic/images/intro.png" alt="monolithic-architecture" width="350"/>

There are several advantages to the monolith approach that we will discuss them in the upcoming captions. But let me say some main advantages and disadvantages here.

Since it is a single code base, its easy to pull and get started to project. Since project structure in 1 project and easy to debug business interactions across different modules.

Unfortunately, the monolith architecture has lots of disadvantages, we can say that; It becomes too large in code size with time that's why its really difficult to manage. Difficult to work in parallel in the same code base. Hard to implement new features on legacy big monolithic applications. Any change, requires deploying a new version of the entire application.

As you can see that we understand Monolithic Architecture.

---

### When to use Monolithic Architecture
Even monolithic architecture has lots of disadvantages, if you are building small application, still monolithic architecture is one of the best architecture that you can apply for your projects.

Because, In many ways, monolithic apps are straightforward.

They’re **straightforward** to:

- Build
- Test
- Deploy
- Troubleshoot
- Scale vertically (scale up)

is very easy and fast.

It is simple to develop relative to microservices where skilled developers are required in order to identify and develop the services. 
It is easier to deploy as only a single jar/war file is deployed.

---

### Request per Second and Acceptable Latency
And if you don't need to expect hundreds of request, you can scale it vertically which is scaling up, that means upgrading existing server. 
By this way you can avoid the problems of network latency and security are relatively less if we compare with the microservices architecture.

![request-per-second](/monolithic/images/request_per_second.png)

As you can see in the table, we will start a small e-commerce application that get only 2K concurrent user and gets 500 request per second.
So if you don’t expect any growth of your customer base, so we should pick the Monolithic architecture.

Even we expect growth of our users to 500K or millions of users, its good to start simple and evolve step by step.

---

### Benefits of Monolithic Architecture
As we said before the monolithic architecture is considered to be a traditional way of building applications. A monolithic application is built as a single big code base that means it has one large code base. If developers want to update or change something, they access the same code base. So, they make changes in the whole stack at once.

So What is the Strengths — Benefits — Advantages of the Monolithic Architecture ?

- **Simple to develop**:<br>
  As long as the monolithic approach is a standard way of building applications, any engineering team has the right knowledge and capabilities to develop a monolithic application. That means it is relatively easier and simple to develop in comparison to microservices architecture.
- **Easier debugging and testing:**<br>
  In contrast to the microservices architecture, monolithic applications are much easier to debug and test. Since a monolithic app is a single big code base, you can run end-to-end testing much faster.
- **Simple to deploy**:<br>
  Another advantage associated with the simplicity of monolithic apps is easier deployment. When it comes to monolithic applications, you do not have to handle many deployments — just one file or directory. Easier to deploy as only a single jar/war file is deployed. The problems of network latency and security are relatively less in comparison to microservices architecture.

So if you are building small application, still monolithic architecture is one of the best architecture that you can apply for your projects.

---

### Challenges of Monolithic Architecture
- **Understanding**:<br>
  It becomes too large in size with time and that’s why its difficult to manage.
  When a monolithic application scales up, it becomes too complicated to understand. So that means, the monolith application has become so complicated that no single person understands it.

- **Making New changes:**<br>
  It is harder to implement new changes in such a large and complex application with highly tight coupling. Any code change affects the whole system. This makes You fear when making new changes. And these changes brings costly side effects. And also this makes the overall development process much longer. It will develop New features become time-consuming and expensive to implement.

- **New technology barriers:**<br>
  It is extremely problematic to apply a new technology in a monolithic application because then the entire application has to be re development. We can say this condition as the Fear Cycle. If you’ve developing same monolithic application for a long time, It’s stressful to change your full code base with newest technology. Instead of building new or innovative solutions, most of your time is spent maintaining legacy apps. So we can say that Adding new technologies and frameworks aren’t an option.

- **Scalability:**<br>
  You cannot scale components independently, the only option is the scaling the whole application. Maybe one of your module get more request according to other modules but you have to scale for all modules in your application. You can’t separate modules and scale independently.

---

### Reference architectures of Monolithic Architecture
You can imagine that we are building an e-commerce application that takes orders from customers, add to basket and checkout the order and so on.

Lets see example Reference Monolithic Architectures.

**Reference Monolithic Architecture 1**

![architecture-1](/monolithic/images/architecture_1.png)

The application can include several components like GUI and business logics and database persistence layers. The application is deployed as a single monolithic application. For example, a Java web application consists of a single WAR file that runs on a web container such as Tomcat. You can run multiple instances of the application behind a load balancer in order to scale and improve availability.

As a result this solution has a number of benefits:

- Simple to develop — you develop in single code base.
- Simple to deploy — you simply need to deploy only the WAR file.
- Simple to scale — you can scale the application by running multiple copies of the application behind a load balancer.
---
### Reference Monolithic Architecture 2
Here is we can see different illustrations, again e-commerce application.

![architecture-2](/monolithic/images/architecture_2.png)
---
### Evolve Reference Monolithic Architectures
And the last one shows how to evolve monolithic architecture.

![architecture-3](/monolithic/images/architecture_3.png)

You can see in this picture, the evolution of monolithic architecture. So its start with standalone 1 application server and database. After that we can split Client application, after that split the business logic and data access and last we split services components in monolithic application.

So as you can see that we will also follow these example reference monolithic architectures and principles and design our own e-commerce application.

---

### Design principles of Monolithic Architecture — KISS, YAGNI, DRY
In software industry, we can get projects from the easiest to the most complex projects and solutions from our clients. However, it is often that we fall into the trap of **designing more complex systems** than necessary required systems.

So before we start to design, its good to check our design principles that we can apply on every design.

These principles are:
- DRY
- KISS
- YAGNI
Let’s see details.

### DRY Principle
DRY is stands for "**Don’t Repeat Yourself**".

In the book of 'The Pragmatic Programmer'’', we can see this definition for DRY;

><cite>-- Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.</cite>

This means that, you must try to maintain the behavior of a functionality of the system in a single piece of code, it should not have duplicated code or design item. Since we are looking these principles for system design, we will follow same concepts with software development. It’s easier to maintain a code or system that is only in one place, because if you need to change something in the code or system, you just need to change in one place.

---

### KISS Principle
KISS is stands for "**Keep It Simple, Stupid**".

This principle says about to make your code or system simple. You should avoid unnecessary complexity. A simple code it’s easier to maintain and easier to understand. You can apply this principle in the design and in the implementation of the code. You should eliminate duplicated code, should remove unnecessary features, use names for apis and methods that makes sense and matches their responsibilities.

You also should separate the responsibilities of your applications and the responsibilities from the layers of the systems. Most systems work best if they are kept simple rather than making them complex designs; therefore, simplicity should be a key goal in design and unnecessary complexity should be avoided.

---

### YAGNI Principle
YAGNI is stands for "**You Ain’t Gonna Need It**".

Sometimes, we try to think way ahead, into the future of the project, adding some extra features “just in case we need them”. This is Wrong! we don’t need it and in most of the case we can say YAGNI = “You Aren’t Gonna Need It”.
This principle is similar to the KISS principle, both of them aim for a simpler solution. The difference between them is that YAGNI focus on removing unnecessary functionality and logic and KISS focus on the complexity.

So **with following these principles**, we will start to design our **e-commerce application architecture**. Remember that a clean system, it’s easier to main, easier to understand and for sure it will save your time when you need to change or implement something.

---

### Design the Monolithic Architecture — E-Commerce App — KISS & YAGNI
In this part we are going to design our **e-commerce application** with the monolithic architecture step by step. We will iterate the architecture design one by one as per requirements.

In every case, before we design the architecture, We should always start with writing down **FRs** and **NFRs**. So lets write down FRs.

### Functional Requirements
- List products
- Filter products as per brand and categories
- Put products into the shopping cart
- Apply coupon for discounts and see the total cost all for all of the items in shopping cart
- Checkout the shopping cart and create an order
- List my old orders and order items history

### Non-Functional Requirements
- Availability
- Scalability

Its good to add principles in our picture in order to remember them always.

### Principles
- DRY
- KISS
- YAGNI

We are going to consider these principles when design our architecture.

Now we can consider to Database and Components of e-commerce application.

### Database
- Database will be single relational database — RDBMS.

### Components of E-Commerce
- Shop UI
- Catalog Service
- SC Service
- Discount Service
- Order Service

With following all these considerations, we can design our E-Commerce Monolithic Architecture with applying tech stack as below image;

![monolithic-architecture](/monolithic/images/monolithic-architecture.png)

As you can see that all modules of this traditional web application, such as Shop Front UI, Catalog Service, SC Service, Discount Service and Order Service, are single artifacts in the container.

This monolithic application has a massive codebase that includes all modules. If you introduce new modules to this application, you have to make changes to the existing code and then deploy the artifact with a different code to the Tomcat server. We can develop Java application and output to single WAR Artifact. We can use Oracle or PostgreSQL for our e-commerce monolithic database.

---

### Communication of Components — E-Commerce App — Monolithic Application — Inter-Process Communication
As you know that, monolithic application sitting in the same server with all modules. So we don’t need to make any network call. So it is very easy and fast to communicate between modules of our E -Commerce Monolithic Application.

The communication will be INTER-PROCESS COMMUNICATION.

![inter-process-communication](/monolithic/images/inter_process_communication.png)

**Inter-process communication** is the mechanism provided by the operating system that **allows processes to communicate with each other**. So that means communication performs by method calls into the code.

This communication could involve a **process letting another process know** that some event has occurred or **transferring of data** from one process to another. As you can see that we only use method calls for communication in monolithic architectures.

---

### Transaction Management in Monolithic Architectures
Transaction management in Monolith architecture is quite easy compared to Microservice Architecture. Many frameworks or languages contains some mechanism for transaction management. For example orm tools with applying unit of work patterns.

These mechanism have a **single database** of the whole application. They are developed for scenarios where all transactions are running on a single context. In other words, we can **simply commit** and **rollback operations** with these mechanism in monolith architectures.
Lets think about our e-commerce domain, We have transactional use case when placing order.

Lets see pseudo code fore **place_order** method

```c#
function place_order()
   do_payment
   decrease_stock
   send_shipment
   generate_bill
   update_order
```

As you can see that we can handle all operations into one method and surround operation in a **transactional scope**.

By this way, Transactions operated in the transaction scope are kept in memory **without writing to the database** until they are **committed**, and if a Rollback is made at any time, all transactions that have been processed so far in the scope are deleted from memory and the transaction is canceled. **Without rollback**, when **Commit** is written to the **database**, the transaction is completed successfully.

---

### Deployments for Monolithic Architecture
We have design the architecture and think about that how we can deploy this architecture ? As we already said before, since this is **single code base**, It is **harder to implement new changes** in such a large and complex application with highly tight coupling. Any code change affects the whole system.

Even the **smallest change requires full deployment** of the entire application — it is **expensive** and **risky**. It is **not reliable** that a single bug in any module can bring down the whole monolithic application.

![deployments-monolithic-architecture](/monolithic/images/deployments_monolithic_architecture.png)

**See the image**. The large developer **team commits** their changes to a **single source code repository**. The path from **code commit** to production is long and hard to manage and requires manual testing. So that comes with the application is large, complex, unreliable, and difficult to maintain. In order to solve these problems we should **evolve** our **architecture** to **Microservices** Architecture.