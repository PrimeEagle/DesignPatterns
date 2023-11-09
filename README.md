# Design Patterns



## Creational Patterns
These patterns are designed to handle object creation mechanisms, increasing the flexibility and efficiency of object creation.

### [Singleton Pattern](https://refactoring.guru/design-patterns/singleton)
Ensures a class has only one instance and provides a global point of access to it. It's often used for central management of resources, like configurations or thread pools.

### [Factory Method Pattern](https://refactoring.guru/design-patterns/factory-method)
Defines an interface for creating an object, but lets subclasses alter the type of objects that will be created. This is used when a class can't anticipate the class of objects it must create.

### [Abstract Factory Pattern](https://refactoring.guru/design-patterns/abstract-factory)
Offers an interface for creating families of related or dependent objects without specifying their concrete classes. Useful when you need to ensure that multiple objects you're creating are compatible with each other.

### [Builder Pattern](https://refactoring.guru/design-patterns/builder)
Separates the construction of a complex object from its representation, allowing the same construction process to create various representations. This is beneficial when you need to construct complex objects step by step.

### [Prototype Pattern](https://refactoring.guru/design-patterns/prototype)
Allows copying of existing objects without making the code dependent on their classes. This pattern is useful when creating many identical objects quickly.



## Structural Patterns

### [Adapter Pattern](https://refactoring.guru/design-patterns/adapter)
Allows objects with incompatible interfaces to collaborate. It's used when you want an existing class to work with others without modifying its source code.

### [Bridge Pattern](https://refactoring.guru/design-patterns/bridge)
Splits a large class or a set of closely related classes into two separate hierarchies—abstraction and implementation—which can be developed independently. This is ideal when you want to decouple an abstraction from its implementation so that the two can vary independently.

### [Composite Pattern](https://refactoring.guru/design-patterns/composite)
Lets you compose objects into tree structures and then work with these structures as if they were individual objects. Use this pattern when you want clients to treat both individual objects and compositions uniformly.

### [Decorator Pattern](https://refactoring.guru/design-patterns/decorator)
Allows adding new behaviors to objects by placing them inside special wrapper objects. This pattern helps to add behavior to individual objects without affecting the behavior of other objects from the same class.

### [Facade Pattern](https://refactoring.guru/design-patterns/facade)
Provides a simplified interface to a library, a framework, or any other complex set of classes. Use this when you want to hide complex subsystems behind a simple interface.

### [Flyweight Pattern](https://refactoring.guru/design-patterns/flyweight)
Lets you fit more objects into the available RAM by sharing common parts of the state between multiple objects, instead of keeping all of the data in each object. This is ideal for supporting large numbers of similar objects efficiently.

### [Proxy Pattern](https://refactoring.guru/design-patterns/proxy)
Provides a surrogate or placeholder for another object to control access to it. This is used when you need a more versatile or sophisticated reference to an object than a simple pointer.


## Behavioral Patterns

### [Strategy Pattern](https://refactoring.guru/design-patterns/strategy)
Defines a family of algorithms, encapsulates each one, and makes them interchangeable. It's used when you have multiple algorithms for specific tasks and want the client to choose the algorithm.

### [Observer Pattern](https://refactoring.guru/design-patterns/observer)
Defines a subscription mechanism to notify multiple objects about any events that happen to the object they're observing. This is common in GUI systems or event monitoring systems.

### [Command Pattern](https://refactoring.guru/design-patterns/command)
Turns a request into a stand-alone object that contains all information about the request. This pattern is used to parameterize clients with queues, requests, or operations.

### [State Pattern](https://refactoring.guru/design-patterns/state)
Allows an object to alter its behavior when its internal state changes. This pattern is used when an object's behavior depends on its state and must change its behavior at runtime depending on that state.

### [Chain of Responsibility Pattern](https://refactoring.guru/design-patterns/chain-of-responsibility)
Passes requests along a chain of handlers. Upon receiving a request, each handler decides either to process the request or to pass it to the next handler in the chain. It's used to reduce coupling where a request from the client should be processed by multiple objects without the client knowing which object ultimately processes it.

### [Memento Pattern](https://refactoring.guru/design-patterns/memento)
Lets you save and restore the previous state of an object without revealing the details of its implementation. This is used when you need to capture and store an object's internal state at a specific moment without exposing its encapsulation.

### [Visitor Pattern](https://refactoring.guru/design-patterns/visitor)
Lets you define a new operation without changing the classes of the objects on which it operates. This is ideal when you need to perform an operation across a complex object structure with different kinds of objects.

### [Mediator Pattern](https://refactoring.guru/design-patterns/mediator)
Reduces chaotic dependencies between objects by making them communicate indirectly, through a specially created mediator object. This pattern is used to bring order to systems with multiple objects that all need to interact with each other.

### [Interpreter Pattern](https://www.geeksforgeeks.org/interpreter-design-pattern/#)
Provides a way to evaluate language grammar or expression for a language which clients are likely to understand. This pattern is used in compilers or calculators, where you can extend the language easily.


## Concurrency Patterns

### [Active Object](https://www.state-machine.com/active-object)
Decouples method execution from method invocation that reside in their own thread of control. The goal is to introduce concurrency, by using asynchronous method invocation and a scheduler for handling requests.

### [Monitor Object](https://www.topcoder.com/thrive/articles/Concurrency%20Patterns%20-%20Active%20Object%20and%20Monitor%20Object)
An object whose methods are subject to mutual exclusion, thus preventing multiple objects from erroneously trying to use it at the same time.

### [Lock](https://www.studocu.com/en-us/document/the-university-of-texas-at-arlington/software-design-patterns/understanding-the-concurrency-pattern-lock/52444388)
Provides a mechanism for controlling access (by multiple threads) to a shared resource.

### [Thread Pool](https://medium.com/@dholnessii/the-thread-pool-pattern-7227eb9ec2b6)
Creates a number of threads at startup, placing them into a pool where they await work. These threads are then reused rather than creating a new one every time.

### [Thread-Specific Storage](https://www.slideserve.com/romo/thread-specific-storage-tss-powerpoint-ppt-presentation)
Static or "global" memory local to a thread.


## Enterprise Application Patterns

### [Repository Pattern](https://medium.com/@pererikbergman/repository-design-pattern-e28c0f3e4a30)
The Repository pattern is used to separate the logic that retrieves data from a database (or any other data source) from the business logic of your application. Instead of having the domain logic communicate directly with the database, it interacts with a repository instead, which handles the connection, commands, and transactions.
This pattern is commonly used in scenarios where you want to simplify data access by separating it from the complex business rules and processing.

### [Unit of Work Pattern](https://mono.software/2017/01/13/unit-of-work-a-design-pattern/)
This pattern maintains a list of objects affected by a business transaction and coordinates the writing out of changes. Essentially, it keeps track of everything you do during a business transaction that can affect the database and isolates this work from other transactions.
You'd use this pattern to ensure that all operations within a transaction are committed or rolled back as one single unit.

### [Service Layer Pattern](https://docs.oracle.com/cd/E93130_01/service_layer/service%20layer%20API/Content/Service%20Layer%20Architecture/Service%20Layer%20Architecture.htm)
The Service Layer is a design pattern that aims to organize the services that your application offers and provides a set of high-level APIs. These APIs coordinate responses in a complex system (e.g., retrieving data from repositories, processing, and then returning a response).
This pattern is useful when you want a unified, orchestrated set of operations available to your system, especially if these operations involve interactions between different back-end systems or require specific sets of rules and logic.

### [Data Transfer Object (DTO) Pattern](https://medium.com/@orcunyilmazoy/the-dto-pattern-data-transfer-objects-8146b262636e)
DTOs are simple objects that should not contain any business logic but may contain serialization and deserialization mechanisms for transferring data over the network.
It's beneficial when you need to exchange data between subsystems or across the network, and you don't want to share complex domain objects.

### [n-Tier Architecture Pattern](https://medium.com/geekculture/n-tier-architecture-explained-5d2e0246c354)
A multi-tier architecture that separates presentation, business logic, data access, and data storage.

### [Onion Architecture Pattern](https://medium.com/@alessandro.traversi/understanding-onion-architecture-an-example-folder-structure-9c62208cc97d#:~:text=Onion%20Architecture%20is%20a%20software,easier%20to%20evolve%20over%20time.)
A loosely coupled architectural design focused on separation of concerns, which uses different layers to manage the flow of data.


## Domain-Driven Design Patterns

### [Domain Service](https://alok-mishra.com/2021/04/08/domain-service-architecture-the-good-bad-and-ugly/)
When an operation does not conceptually belong to any object and yet pertains to the domain layer, it could be implemented using the Domain Service pattern. These services hold domain logic that doesn't naturally fit within a domain object.
You would use a Domain Service when the action you're considering transcends a single entity or entity aggregate.

### [Value Object](https://codeburst.io/value-objects-and-how-to-appreciate-them-19711c74e3cb)
An object that contains attributes but has no conceptual identity. They should be treated as immutable.
They are often useful when you want to group several pieces of information into a single compound value (e.g., a color, money amount, or a range of dates).

### [Entity](https://badia-kharroubi.gitbooks.io/microservices-architecture/content/patterns/tactical-patterns/domain-entity-pattern.html)
Objects that are not defined by their attributes, but rather by a thread of continuity and identity.
Entities are used when you have a distinct object based on identity, often coming with its own lifecycle.

### [Aggregate](https://badia-kharroubi.gitbooks.io/microservices-architecture/content/patterns/tactical-patterns/aggregate-pattern.html)
A collection of objects that are bound together by a root entity, otherwise known as an aggregate root. Any references from outside the aggregate should only go to the aggregate root.
This pattern is used to enforce business rules and invariants within the aggregate boundary and to simplify interaction with a complex graph of domain objects.

### [Factory](https://culttt.com/2014/12/24/factories-domain-driven-design)
In the context of DDD, a factory abstracts the process of creating complex objects or aggregates. It's responsible for providing whole, consistent objects and aggregates.
This is crucial when the process of creating the domain object is complex or requires additional validation.


## Dependency Injection Patterns

### [Constructor Injection]
This form of dependency injection involves providing the dependencies of a class through its constructor when creating the instance. This pattern ensures that objects are fully initialized with all of their dependencies before they're used.
Use this when you want to ensure an instance’s dependencies are provided before it is used and avoid changing the dependencies after the instance is created.

### [Property Injection (Setter Injection)]
Instead of providing the dependencies through the constructor, they are set through the class’s public properties. This pattern is useful when you need to set dependencies after an object is constructed, especially on objects created through a default constructor or objects instantiated by a framework.
Employ this pattern if you have optional dependencies or need to change dependencies during the lifetime of an object.

### [Method Injection]
The dependencies are provided through methods. These methods can be called at any time, which means that the instance can start in an uninitialized state.
This is helpful when an object requires different instances of the same dependency at various times during its lifetime or if it only requires a dependency under specific circumstances (not for every method call).

### [Service Locator]
Though considered an anti-pattern by some, the Service Locator is a common pattern used to find services (dependencies) in a global point in the application (usually a singleton), rather than injecting them. This often involves a registry that is aware of all the components in the system and is responsible for providing them when asked.


## Architectural Patterns
These are high-level strategies that concern large-scale components, the global properties and mechanisms of a system.

### [Model-View-Controller (MVC)]
Separates an application into three interconnected components
the model (data), the view (user interface), and the controller (processes that handle input).
This pattern is used for designing the layout of code to decouple data access and business logic from data presentation and user interaction, simplifying future development and maintenance.

### [MVVM (Model-View-ViewModel)]
A software architectural pattern used primarily for developing user interfaces, where it separates data representation and interaction logic from the visual elements. This pattern facilitates efficient code reusability and independent development of components, making it ideal for applications requiring a robust and dynamic UI that changes in response to data modifications or user interactions.

### [Microservices Architecture]
Breaks down a traditional monolithic application into smaller, self-contained services, which are easier to build and maintain and can be developed independently.
This approach is suitable for complex, scalable, and high-demand applications, especially those needing frequent updates or with functionality that spans multiple platforms.

### [Layered Architecture (n-tier architecture)]
Organizes the application infrastructure into layers (UI, business logic, data access), each one with its own responsibilities.
This is beneficial for traditional web applications or enterprise applications that require standardization, maintainability, and scalability but don't require high levels of scalability.

### [Event-Driven Architecture]
Focuses on producing, detecting, consuming, and reacting to events. This pattern is highly scalable and provides high throughput for data processing.
Use this for applications that need real-time updates, asynchronous processing, or need to handle a high volume of requests spread across multiple services.

### [Serverless Architecture]
Allows developers to build and run applications without managing server infrastructure, delegating these responsibilities to cloud providers.
This is ideal for applications that can benefit from auto-scaling, want to reduce overhead of server maintenance, or have unpredictable workloads.


## Integration Patterns

### [Gateway]
Encapsulates the internal system's architecture and provides an API to clients. It might include mechanisms like load balancing, caching, access control, API composition, and security.
This is used when building applications that expose APIs over disparate underlying systems or services.

### [Pipeline]
Uses a series of processing elements arranged so that the output of one element is the input of the next one. It's commonly used for tasks such as data processing or task scheduling.
Implement this pattern when you need a series of processing steps, potentially with varying sequence, to be executed in order.

### [Broker]
Acts as a mediator between the communication of two components, providing a low-coupling, scalable, and simple-to-extend architecture.
This pattern is useful for messaging, task processing, or handling requests where the components don't need to know about each other.

### [Reactive Patterns]
These deal with software systems that maintain a consistent response time despite varying workload, typically implemented with event-driven architecture, non-blocking I/O, and other asynchronous programming techniques.

### [Back Pressure]
Provides control over resource consumption and handling in systems with asynchronous processing by propagating pressure from the resource consumer to the producer.
Use this when you need to prevent the system from crashing or becoming unresponsive due to resource overconsumption under high demand.

### [Circuit Breaker]
Monitors the status of external services and prevents continuous failure that can result from calling a service that is down.
Implement this pattern in distributed systems where you want to maintain system integrity and avoid cascading failures in a microservice environment.


## Cloud Design Patterns

### [Strangler Pattern]
Incrementally migrates a legacy system by gradually replacing specific pieces of functionality with new applications and services.
This is used when migrating an old legacy system piece by piece, rather than doing a full replacement at once.

### [Sidecar Pattern]
Deploys an additional service alongside the main application service, offering an isolated environment to execute or process specific tasks or features.
Use this for tasks like monitoring, logging, configuration, networking, and security protocols separate from the main application logic.

### [CQRS (Command Query Responsibility Segregation)]
Separates read and update operations for a data store, optimizing performance, simplifying code, and providing more robust security.
This pattern is useful in complex business systems where you want to achieve scalability, security, and separation of concerns by handling read and write operations differently.


## Game Development Patterns

### [Game Loop]
The Game Loop is the central heartbeat of most games, handling the cyclic processes of user input, game updates (logic), and rendering within a continuous loop.
This pattern ensures smooth gameplay by maintaining a consistent flow of game updates and rendering, often aiming for a specific number of frames per second.

### [Update Method]
The Update Method involves having a method that is automatically called at every frame update or tick, often used within the Game Loop, and it's where the logic for AI, character movement, physics, and more is placed.
This keeps game elements in sync with the game world's real-time nature and helps organize how game entities are updated.

### [omponent Pattern (also known as Entity-Component-System (ECS))]
Instead of representing game objects in a deep class hierarchy, this pattern breaks down game entities into components that add functionality and allows you to treat entities as bags of interchangeable parts.
This pattern is used for flexibility in defining game entities and better performance in updating them, especially in systems with a large number of objects (useful for both rendering and AI efficiency).

### [State Pattern]
In gaming, this pattern allows an object to alter its behavior when its internal state changes, making it seem like the object's class has changed.
This is particularly useful in game AI to manage character behaviors, where characters can have various states like patrolling, chasing, attacking, fleeing, etc.

### [Singleton Pattern]
This ensures a class has only one instance and provides a global point of access to that instance.
Often used for managers in games, such as a game manager, audio manager, or input manager, which should be unique and accessible from everywhere.

### [Behavior Trees]
This hierarchical model is used to build complex, context-sensitive behavior for game agents based on simple, reusable components called nodes. The tree structure allows for the addition of decision-making processes in the game entities.
This pattern is used for creating intelligent and scalable AI with clear logic, especially for non-player characters (NPCs) in games.

### [Finite State Machine (FSM)]
A simple machine that mimics the logical states an entity can take on with clearly defined transitions between those states.
This is perfect for simpler AI logic, where characters or elements have a limited number of states and behaviors.

### [Navigation Mesh]
This is a data structure used in AI calculations for pathfinding, allowing an agent to navigate around a complex 3D environment by breaking down the world space into traversable polygons.
It's used in situations where game entities need to navigate through game areas avoiding obstacles, especially in 3D games.

### [Blackboard]
A shared knowledge base for communication between different AI systems (such as NPCs) that allows for both centralized and decentralized AI decision-making.
This pattern is used when multiple AI agents need to share data and make decisions based on shared world knowledge, coordinating behavior between different agents.

### [Utility System]
Instead of traditional rule or priority-based decisions, actions are evaluated based on a utility score, considering multiple variables to decide the best action to take.
Useful for more nuanced AI decisions, where actions aren't just based on priority or triggers but involve multiple influencing factors.

### [Memento Pattern]
Allows for a way to store and restore the game or an entity's state, useful for "undo" operations, checkpoints, or managing game saves.
This is crucial for allowing players to save their game state and return to it later without losing progress.
