## **Part 1 — Introduction to System Design**

Start here

### **1. System Design Basics**

- What is System Design?
    
- Why is System Design required?
    
- Software development vs System Design
    
- Functional requirements
    
- Non-functional requirements
    
- System constraints
    
- Design trade-offs
    
- Scalability, reliability, maintainability
    
- Monolithic vs distributed systems
    

### **2. Client-Server Architecture**

- What is a client?
    
- What is a server?
    
- Client-server communication
    
- Request-response cycle
    
- Frontend, backend, and database interaction
    
- 2-tier architecture
    
- 3-tier architecture
    
- N-tier architecture
    
- Presentation layer
    
- Business logic layer
    
- Data access layer
    

**Interview question:** Explain the architecture of a web application you have developed.

## **Part 2 — Networking Fundamentals**

### **3. Internet and Network Basics**

- How the internet works
    
- IP address
    
- Public IP vs private IP
    
- Port numbers
    
- DNS
    
- Domain names
    
- URL structure
    
- TCP vs UDP
    
- HTTP vs HTTPS
    
- Request and response headers
    
- HTTP status codes
    
- TLS/SSL basics
    

### **4. HTTP and API Communication**

- HTTP request methods
    
    - GET
        
    - POST
        
    - PUT
        
    - PATCH
        
    - DELETE
        
    
- REST API fundamentals
    
- Request body, headers, query parameters, route parameters
    
- JSON serialization and deserialization
    
- Stateless communication
    
- API versioning
    
- Authentication vs authorization
    

**Practical connection:** Understand how your React frontend sends an HTTP request to an ASP.NET Core Web API.

## **Part 3 — API Design Fundamentals**

### **5. REST API Design**

- What is an API?
    
- What is REST?
    
- REST architectural principles
    
- Resource-based API design
    
- Naming API endpoints
    
- CRUD operations
    
- Proper HTTP status codes
    
- Pagination
    
- Filtering and sorting
    
- API validation
    
- Error handling
    
- API documentation using Swagger / OpenAPI
    

### **6. API Performance and Reliability**

- Rate limiting
    
- Throttling
    
- Request timeout
    
- Retry mechanism
    
- Idempotency
    
- API caching
    
- API gateway — introductory understanding
    
- Load balancing — introductory understanding
    

**Example:** Design APIs for a fitness application:

```
GET    /api/workouts
GET    /api/workouts/{id}
POST   /api/workouts
PUT    /api/workouts/{id}
DELETE /api/workouts/{id}
```

## **Part 4 — Database Design**

### **7. Database Fundamentals**

- What is a database?
    
- Relational vs non-relational databases
    
- SQL vs NoSQL
    
- Tables, rows, columns
    
- Primary key
    
- Foreign key
    
- Constraints
    
- Relationships
    
    - One-to-one
        
    - One-to-many
        
    - Many-to-many
        
    
- ER diagrams
    
- Schema design
    

### **8. Database Normalization**

- Why normalization is required
    
- 1NF
    
- 2NF
    
- 3NF
    
- Denormalization
    
- Data redundancy
    
- Data consistency
    

### **9. Database Performance**

- Indexing
    
- Clustered vs non-clustered index — basic concept
    
- Composite indexes
    
- Query optimization
    
- Execution plans — basic understanding
    
- Joins
    
- Database connection pooling
    
- N+1 query problem
    
- Database transactions
    

### **10. Advanced Database Concepts — Basic Interview Level**

- ACID properties
    
- Isolation levels
    
- SQL transactions
    
- Deadlocks
    
- Replication
    
- Sharding
    
- Read replicas
    
- Horizontal vs vertical partitioning
    

## **Part 5 — Core System Design Concepts**

Very important

### **11. Scalability**

- What is scalability?
    
- Vertical scaling
    
- Horizontal scaling
    
- Advantages and disadvantages
    
- Bottlenecks
    
- Stateless vs stateful services
    

### **12. Load Balancing**

- What is a load balancer?
    
- Why is load balancing required?
    
- How load balancing works
    
- Round Robin
    
- Least Connections
    
- Health checks
    
- Reverse proxy
    
- Load balancer vs reverse proxy
    

### **13. Caching**

- What is caching?
    
- Why caching improves performance
    
- Browser cache
    
- Server-side cache
    
- Database cache
    
- Redis fundamentals
    
- Cache-aside pattern
    
- Write-through caching
    
- Write-back caching
    
- Cache invalidation
    
- Cache expiration / TTL
    

### **14. Message Queues and Asynchronous Processing**

- Synchronous vs asynchronous processing
    
- What is a message queue?
    
- Why queues are used
    
- Producer and consumer
    
- Background jobs
    
- Event-driven architecture
    
- RabbitMQ / Kafka — introductory concepts
    
- Retry and dead-letter queues
    

**Example:** Sending an email after a user registers should not necessarily delay the registration API response.

### **15. Reliability and Availability**

- What is reliability?
    
- What is availability?
    
- Fault tolerance
    
- Single point of failure
    
- Redundancy
    
- Failover
    
- Health checks
    
- Graceful degradation
    
- Disaster recovery — basic understanding
    

## **Part 6 — Distributed System Fundamentals**

### **16. Distributed Systems**

- What is a distributed system?
    
- Why distributed systems are used
    
- Advantages and disadvantages
    
- Communication between services
    
- Network failures
    
- Partial failures
    
- Latency
    
- Consistency
    
- Availability
    

### **17. CAP Theorem**

- Consistency
    
- Availability
    
- Partition tolerance
    
- CAP theorem
    
- What happens during a network partition?
    
- Strong consistency vs eventual consistency
    

### **18. Microservices Architecture**

- Monolith vs microservices
    
- What are microservices?
    
- Advantages and disadvantages
    
- Service boundaries
    
- Inter-service communication
    
- REST communication
    
- Messaging communication
    
- Service discovery — basic concept
    
- API gateway
    
- Distributed transactions — basic concept
    

**Fresher expectation:** You should be able to explain the difference between a monolithic ASP.NET Core application and a microservices-based application. You do not need to implement a complete microservices platform.

## **Part 7 — Low-Level System Design (LLD)**

This is especially useful for fresher interviews involving OOP, Java/C#, and backend development.

### **19. Object-Oriented Design**

- Classes and objects
    
- Encapsulation
    
- Abstraction
    
- Inheritance
    
- Polymorphism
    
- Interfaces
    
- Composition vs inheritance
    
- SOLID principles
    
- Dependency Injection
    
- Separation of concerns
    

### **20. UML and Design Diagrams**

- Class diagram
    
- Use case diagram
    
- Sequence diagram
    
- Activity diagram
    
- Entity relationship diagram
    
- Component diagram
    

### **21. Design Patterns — Basic Interview Level**

- Singleton
    
- Factory
    
- Strategy
    
- Observer
    
- Repository
    
- Dependency Injection
    
- Adapter
    
- Decorator
    

Understand **what problem each pattern solves**, when to use it, and a simple C# example.

### **22. Common LLD Practice Problems**

- Design a parking lot
    
- Design a library management system
    
- Design a food ordering system
    
- Design a notification system
    
- Design an elevator system
    
- Design a meeting room booking system
    
- Design a simple ATM
    

## **Part 8 — High-Level System Design (HLD)**

You only need introductory HLD for fresher interviews, but understand the architecture of common applications.

### **23. HLD Fundamentals**

- What is High-Level Design?
    
- HLD vs LLD
    
- Architecture diagrams
    
- Components and their responsibilities
    
- Data flow
    
- API flow
    
- Database selection
    
- Capacity estimation — basic
    
- Trade-offs
    

### **24. Basic Capacity Estimation**

- Requests per second (RPS)
    
- Daily active users (DAU)
    
- Storage estimation
    
- Bandwidth estimation
    
- Read-to-write ratio
    
- Peak traffic
    
- Basic estimation using simple calculations
    

### **25. Common HLD Practice Problems**

- URL shortener
    
- Chat application
    
- File upload and storage system
    
- Notification system
    
- Social media feed
    
- Video streaming platform — basic architecture
    
- E-commerce application
    
- Fitness tracking application
    

# **Part 9 — Cloud and Deployment Fundamentals**

### **26. Cloud Basics**

- What is cloud computing?
    
- IaaS, PaaS, SaaS
    
- Public, private, hybrid cloud
    
- Virtual machines
    
- Containers — basic understanding
    
- Docker fundamentals
    
- Cloud deployment
    
- CDN
    
- Object storage
    
- Cloud databases
    

### **27. Deployment Architecture**

- Development vs production environment
    
- CI/CD basics
    
- Environment variables
    
- Secrets management
    
- Logging
    
- Monitoring
    
- Application health monitoring
    
- Azure App Service — basic understanding
    
- Database deployment and backups