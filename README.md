# The spring Framework

### Spring

```
    A java framework that provides a convinient way of disparate components into a working,
    enterprise-grade application
```

```
    Relies heavily on "inversion of control"(control of object or portions of a program is
    transfered to a container or framework  within which the program runs) to achieve this
```

### Visualization of what spring offers

```
    at the core - The spring Container(plain old java follows inversion of control)
    Business objects(plain old java objects) - can be configured using configuration metadata
    Configuration Metadata
```

### Spring Beans

```
Objects that form the backbone of your spring applicaton and are managed by spring

A bean is an object that is the basic building block of the Spring framework, which Spring
manages at runtime

Spring is responsible for creating and destroying beans and providing dependencies for the beans.
```

### Inversion Control

```
A process by which objects define their dependencies and an external container injects those
dependencies into the object

An object only has to declare what it is dependent on but is not responsible for creating those
dependent objects or figuring out where they come from
```

### The Principle of Inversion Control

```
This means the burden of managing dependencies is passed on to the spring container rather that the
developer handling it themselves

Spring relies on dependency injection to achieve inversion of control

The use of dependecy injection completely frees the developer of figuring out how to
manage the dependencies of any component within their larger application
```

### Dependency Injection and the IoC(Inversion of Control)

```
    Bean - object that depends on behaviour of another object
    Service - Object that client bean depends on
    Injector - code that tells the client bean which service to use (part of spring boot code)
    Injection -  process of telling client bean which service to use

Service becomes part of state of client bean
Client bean can NOT choose, find, or build a service
Client bean delegates this responsibility to injector
Client bean DOES neet to know interface of service

```

### Different Paths to Ioc

```
    Dependency Injection - Spring achieves Ioc using this approach
    Service Locator pattern - Beans find their own service objects
    Factory pattern - Puts onus on implementor of bean; hard to use of pojos
```

### IoC in Spring

```
Client beans are created via factory(or some via constructor)
BeanFactory interdace and ApplicationContext sub-interface

Responsible for instantiating, configuring, and assembling beans.
Several implementations available out of the box with spring

Once bean objects are constructed, dependencies are injected

IoC container: Spring framework to instantiate beans and inject dependencies
```

### Mechanics of dependency Injection

```
    Constructor arguments(if object created via constructor)
    Arguments passed to (static or instance) factory method
    Properties set on objects after instantiations
    Spring supports XML-based declarative instantiation
```

### IoC Container

```
The core component of the Spring framework responsible for the entire lifecycle of
Spring beans
```

### Spring Modules

```
    Data Access/ Integration - JDBC, OXM, ORM, JMS, Transactions
    AOP
    Aspect
    Web - WebSocket, Web, Servlet, Portlet
    Instrumentation
    Messaging
    Core Container - Beans, Core, Context, SpEl
    Test
```

### Core Container - Beans, Core, Context, SpEl

```

Spring core- Takes care of IoC and dependency Injection

ApplicationContext within container is responsible for eliminating simngletons and decouple components

spring context  - For access to objects in JNDI(Java Naming Directory Interface) registry style

spring expression - For working with object graph at runtime
```

### Data Access/ Integration - JDBC, OXM, ORM, JMS, Transactions

```

Spring-jdbc- Abstacts away vendor-specific error codes and handling

spring-orm- For working with JPA, Hibernate, and other ORM APIs

spring-jms  - spring-messaging for message processing

spring-tx - for working with POJOs declaratively
```

### Messaging

```

Spring-messaging module

Message, MessageChannel, and MessageHandler

Annotations for mapping messages to methods

Similiar to spring MVC annotation-based programming
```

### Web

```

Spring-web, spring-webmvc, and spring-websocket modules

spring-web for basic web features, e.g. servlet listeners, HTTP

spring-webmvc for web applicatoin programming using MVS paradigm

sprinf-websocket as thing, lightweight layer above TCP
```

### Aspect-oriented programming

```

Programming paradigm that adds new "aspects" to behavior of existing code using "pointcuts"
(external specifications)
```

### Test

```
Unit-testing as well as integration-testing
Junit or TestNG
Loading and caching ApplicationContext objects
Mock objects to test code in isolation
```

### Dependency Management

```
The process of getting all the required jar files into correct locations (and into the classpath)
so that spring works correctly

Spring publishes artifacts to maven central

Also publishes to specific public Maven repi

Either use Maven, Grable or Ivy

Or download them manually(more error prone)

```

### Spring MVC

```
The framework, within spring, that supports the use of MVC(Model-View-Controller) paradigm
for building web apps

```

### The Model in the MVC Paradigm

```
Encapsulates application state(but not application logic)

Can be queried to obtain state

Notified by controller when state needs to change

Notifies controller once state has been changed

```

### The Controller in the MVC Paradigm

```
Defines the application logic(not application state)

Maps user actions to state changes

Updates the application state via model(not directly)

Updates views once application state is changed

```

### The View in the MVC Paradigm

```
Presents application state to users via appropriate interfaces

Allows users to interact with state, modify state

Do not store application data(except caching)

Built using reusable and configurable elements

```

### The MVC Paradigm

```
Model, view, controller linked by observer design pattern

Synchronous methods vs. asynchronous events

Decouples logic and UI

Extremely powerful and popular approach

```

### Spring MVC Tech technologies

```
Spring MVC heavily relies on three underlying technologies - servlets, JSP, and JSTL

Servlets
refer to java code that runs on a web server, or the application server
Used to build dynamic web pages in java
Run on java enabled web or app server
Handle incoming HTTP request

JSP - akin to PHP, used to create dynamic web pages
JSP compiler is needed to compute JSP scriptlet and servlet
This JSP Compiler runs on Java-enabled web or app server
Servlet code runs inside JVM on web server
JSP allows Java code and HTML to be interleaved

JSTL - Collection of useful JSP tags for common tasks
Scriplet tags are basic building blocks of JSP
JSTL is a standard library of JSP tags
Taglibs contain core functionality of JSTL
Taglibs ship with every servlet and JSP framework
```

### Spring MVC, a.k.a Spring Web MVC

```
MVC architecture for web apps

DispatcherServlets as front contoller to recieve browser requests

Dispatched to appropriate controller via handler mappings

Result returned to users via ViewResolver classes
```

### Typical Spring MVC App

```
Model - POJO(Plain Old Java Object)

Views - JSP templates written with JSTL

Controller - Dispatcher Servlet

Useful for classis 3-tier architecture
```

### Role of dispatcher Servlet

```
a.k.a Spring contoller is a front controller

Every web request first comes to this controller

Request handler controllers, view resolvers, annotations then play a role

Request is then passed onto the actual handler
```
