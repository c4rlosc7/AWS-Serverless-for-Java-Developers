# AWS-Serverless-for-Java-Developers
AWS Serverless for Java Developers

# REST API

REST API, or Representational State Transfer API, is a type of application programming interface (API) that uses a software architecture to manage communication between applications. REST APIs are often used for mobile app development and the Internet of Things (IoT). 

### How does REST API work?
REST APIs use standard HTTP methods to access resources using URLs. 
REST APIs are stateless, meaning each request needs to include all the information needed to process it. 
REST APIs are client-server, meaning the sender and receiver are independent of each other. 
REST APIs use a uniform interface, meaning all requests for the same resource look the same. 
REST APIs are cacheable, meaning API responses can be cached on the client or server side. 

### Benefits of REST APIs 

REST APIs are easier to use than other protocols like SOAP.
REST APIs are faster and more lightweight.
REST APIs are highly scalable.
REST APIs are cross-platform portable.
REST APIs are easy to implement and modify.tr


## HTTP verbs

The most commonly used HTTP verbs are POST, GET, PUT, PATCH, and DELETE. These verbs are also known as HTTP methods. They correspond to the operations of create, read, update, and delete (CRUD). 

### Explanation

- POST: Used to request that a web server accept data from a request message. This is often used to upload a file or submit a web form. 
- GET: Used to read data. 
- PUT: Used to update data. 
- PATCH: Used to update data. 
- DELETE: Used to delete data. 
- OPTIONS: Used to find out which HTTP methods are allowed for a resource. The server responds with a list of supported methods. 


## REST API discovery

REST API discovery is the process of identifying all REST APIs in a system. It's the first step in managing and securing APIs. 

### How it works

Discovery tools catalog all APIs, including public and internal APIs 
Discovery tools search for APIs that can perform specific functions 
Discovery tools provide information about APIs, including what they do, what data they access, and how to access them 

### Discovery tools

Google API Discovery Service
Provides discovery documents for most APIs, including API descriptions, resource schemas, and authentication scopes 
SoapUI
Captures REST traffic, which can be filtered and converted into services for use in projects 
AWS Application Discovery Service
Allows users to specify filters and consult elements of configuration for server assets 

### Benefits of discovery

Discovery helps developers understand the APIs used by an organization, which can help them identify and better use those APIs. 

## Amazon API Gateway

Amazon API Gateway is a service that helps developers create, manage, and secure APIs. It acts as an entry point for applications to access data and functionality from backend services. 

### Features 

API creation: Create RESTful and WebSocket APIs
API management: Manage APIs, including traffic management, authorization, and monitoring
API security: Secure APIs with authentication and authorization controls
API scaling: Run multiple versions of an API simultaneously
API support: Support containerized and serverless workloads, as well as web applications

### Benefits

Developers can focus on building application logic instead of worrying about infrastructure 
APIs can serve traffic over the internet or can be accessible only within your VPC 
APIs can be used to connect non-AWS applications to AWS back-end resources 

