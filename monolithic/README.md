# Monolithic Architecture ([medium](https://medium.com/design-microservices-architecture-with-patterns/monolithic-architecture-is-still-worth-at-2021-98bfc112dc24))

![monolithic-architecture](/monolithic/images/monolithic-architecture.png)

When it comes to legacy applications, we can say that most of legacy applications are mainly implemented as a monolithic architecture. 
If all the functionalities of a project exists in a single codebase, then that application is known as monolithic application.

In the monolith pattern, everything from user interface, business codes and database calls is included in the same codebase. All application concerns are contained in a single big deployment. Even the monolithic applications can design in different layers like presentation, business and data layer and then deploy that codebase as single jar/war file.

![monolithic-architecture](/monolithic/images/intro.png)

There are several advantages to the monolith approach that we will discuss them in the upcoming captions. But let me say some main advantages and disadvantages here.

Since it is a single code base, its easy to pull and get started to project. Since project structure in 1 project and easy to debug business interactions across different modules.

Unfortunately, the monolith architecture has lots of disadvantages, we can say that; It becomes too large in code size with time that's why its really difficult to manage. Difficult to work in parallel in the same code base. Hard to implement new features on legacy big monolithic applications. Any change, requires deploying a new version of the entire application.

As you can see that we understand Monolithic Architecture.


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

### Request per Second and Acceptable Latency
And if you don't need to expect hundreds of request, you can scale it vertically which is scaling up, that means upgrading existing server. 
By this way you can avoid the problems of network latency and security are relatively less if we compare with the microservices architecture.

![request-per-second](/monolithic/images/request_per_second.png)

As you can see in the table, we will start a small e-commerce application that get only 2K concurrent user and gets 500 request per second.
So if you don’t expect any growth of your customer base, so we should pick the Monolithic architecture.

Even we expect growth of our users to 500K or millions of users, its good to start simple and evolve step by step.

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

