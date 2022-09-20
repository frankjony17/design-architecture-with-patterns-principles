# Monolithic Architecture ([medium](https://medium.com/design-microservices-architecture-with-patterns/monolithic-architecture-is-still-worth-at-2021-98bfc112dc24))

![monolithic-architecture](/monolithic/images/monolithic-architecture.png)

When it comes to legacy applications, we can say that most of legacy applications are mainly implemented as a monolithic architecture. 
If all the functionalities of a project exists in a single codebase, then that application is known as monolithic application.

### When to use Monolithic Architecture
Even monolithic architecture has lots of disadvantages, if you are building small application, still monolithic architecture is one of the best architecture that you can apply for your projects.

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


### Benefits of Monolithic Architecture
- Simple to develop.
- Easier debugging and testing.
- Simple to deploy.

### Challenges of Monolithic Architecture
- **Understanding**:
It becomes too large in size with time and that’s why its difficult to manage.
When a monolithic application scales up, it becomes too complicated to understand. So that means, the monolith application has become so complicated that no single person understands it.

- **Making New changes:**
  It is harder to implement new changes in such a large and complex application with highly tight coupling. Any code change affects the whole system. This makes You fear when making new changes. And these changes brings costly side effects. And also this makes the overall development process much longer. It will develop New features become time-consuming and expensive to implement.

- **New technology barriers:**
  It is extremely problematic to apply a new technology in a monolithic application because then the entire application has to be re development. We can say this condition as the Fear Cycle. If you’ve developing same monolithic application for a long time, It’s stressful to change your full code base with newest technology. Instead of building new or innovative solutions, most of your time is spent maintaining legacy apps. So we can say that Adding new technologies and frameworks aren’t an option.

- **Scalability:**
  You cannot scale components independently, the only option is the scaling the whole application. Maybe one of your module get more request according to other modules but you have to scale for all modules in your application. You can’t separate modules and scale independently.

---
### Principles
- **DRY**
  DRY is stands for “Don’t Repeat Yourself”
- **KISS**
  KISS is stands for “Keep It Simple, Stupid”
- YAGNI
  YAGNI is stands for “You Ain’t Gonna Need It”.


### Functional Requirements
Example of Functional Requirements:
- List products
- Filter products as per brand and categories
- Put products into the shopping cart
- Apply coupon for discounts and see the total cost all for all of the items in shopping cart
- Checkout the shopping cart and create an order
- List my old orders and order items history

### Non-Functional Requirements
- Availability
- Scalability

**We are going to consider these principles when design our architecture.**

Now we can consider to Database and Components of e-commerce application.

### **Database**
- Database will be single relational database — RDBMS.

### Components of E-Commerce
- Shop UI
- Catalog Service
- SC Service
- Discount Service
- Order Service

With following all these considerations, we can design our E-Commerce Monolithic Architecture with applying tech stack as below image.


---

### Non-Funcional Requirements
## - ilities
- Scalability  - Escalabilidad
- Availability - Disponibilidad
- Reliability  - Fiabilidad
- Maintability - Mantenibilidad
- Usability    - Usabilidad
- Eficiency    - Eficiencia
  
