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

## AWS SAM - AWS Serverless Application Model

AWS Serverless Application Model (AWS SAM) is an open-source framework that helps developers build and run serverless applications on AWS. It uses infrastructure as code (IaC) to define resources like databases, APIs, and event source mappings. 

### Features

- Shorthand syntax: Uses a shorthand syntax to declare resources in YAML 
- Templates: Includes pre-built application templates for common use cases 
- Command-line interface: Includes a command-line interface (CLI) tool for building, packaging, and testing applications 
- CI/CD integration: Integrates with popular CI/CD tools for production-ready deployments 
- Local and cloud testing: Allows developers to test applications locally or use SAM Accelerate for cloud testing 


### template.yml

- Create new application.
- Build.
- Invoke locally.
- Debug.
- Deploy.
- View remote log files.


### Installing AWS Serverless Application Model - SAM (macOS)

```terminal
> which sam
/usr/local/bin/sam

> sam --version
SAM CLI, version 1.135.0
```

Reference to install: [docs.aws.amazon.com]([Installing](https://docs.aws.amazon.com/es_es/serverless-application-model/latest/developerguide/install-sam-cli.html))

## AWS CLI

```terminal
> which aws
/usr/local/bin/aws

> aws --version
aws-cli/2.24.26 Python/3.12.9 Darwin/24.3.0 exe/x86_64
```

### AWS Configure CLI

```terminal
carlosandresmartinez@Carloss-Mac-mini AWS-Serverless-for-Java-Developers % aws configure
AWS Access Key ID [None]: Paste AWS Access Key ID
AWS Secret Access Key [None]: Paste AWS Secret Access Key
Default region name [None]: us-east-1
Default output format [None]: Default is JSON, press enter
```

[AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html)

### Create new project with SAM

```terminal
> sam init

SAM CLI now collects telemetry to better understand customer needs.

You can OPT OUT and disable telemetry collection by setting the
environment variable SAM_CLI_TELEMETRY=0 in your shell.
Thanks for your help!

Learn More: https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-telemetry.html


You can preselect a particular runtime or package type when using the `sam init` experience.
Call `sam init --help` to learn more.

Which template source would you like to use?
	1 - AWS Quick Start Templates
	2 - Custom Template Location
Choice: 1

Choose an AWS Quick Start application template
	1 - Hello World Example
	2 - Data processing
	3 - Hello World Example with Powertools for AWS Lambda
	4 - Multi-step workflow
	5 - Scheduled task
	6 - Standalone function
	7 - Serverless API
	8 - Infrastructure event management
	9 - Lambda Response Streaming
	10 - GraphQLApi Hello World Example
	11 - Full Stack
	12 - Lambda EFS example
	13 - Serverless Connector Hello World Example
	14 - Multi-step workflow with Connectors
	15 - DynamoDB Example
	16 - Machine Learning
Template: 1

Use the most popular runtime and package type? (python3.13 and zip) [y/N]: N

Which runtime would you like to use?
	1 - dotnet8
	2 - dotnet6
	3 - go (provided.al2)
	4 - go (provided.al2023)
	5 - graalvm.java11 (provided.al2)
	6 - graalvm.java17 (provided.al2)
	7 - java21
	8 - java17
	9 - java11
	10 - java8.al2
	11 - nodejs22.x
	12 - nodejs20.x
	13 - nodejs18.x
	14 - python3.9
	15 - python3.13
	16 - python3.12
	17 - python3.11
	18 - python3.10
	19 - ruby3.3
	20 - ruby3.2
	21 - rust (provided.al2)
	22 - rust (provided.al2023)
Runtime: 7

What package type would you like to use?
	1 - Zip
	2 - Image
Package type: 1

Which dependency manager would you like to use?
	1 - gradle
	2 - maven
Dependency manager: 2

Would you like to enable X-Ray tracing on the function(s) in your application?  [y/N]: N

Would you like to enable monitoring using CloudWatch Application Insights?
For more info, please view https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch-application-insights.html [y/N]: y
AppInsights monitoring may incur additional cost. View https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/appinsights-what-is.html#appinsights-pricing for more details

Would you like to set Structured Logging in JSON format on your Lambda functions?  [y/N]: y
Structured Logging in JSON format might incur an additional cost. View https://docs.aws.amazon.com/lambda/latest/dg/monitoring-cloudwatchlogs.html#monitoring-cloudwatchlogs-pricing for more details

Project name [sam-app]: photo-app-users-rest-api-sam

Cloning from https://github.com/aws/aws-sam-cli-app-templates (process may take a moment)

    -----------------------
    Generating application:
    -----------------------
    Name: photo-app-users-rest-api-sam
    Runtime: java21
    Architectures: x86_64
    Dependency Manager: maven
    Application Template: hello-world
    Output Directory: .
    Configuration file: photo-app-users-rest-api-sam/samconfig.toml

    Next steps can be found in the README file at photo-app-users-rest-api-sam/README.md


Commands you can use next
=========================
[*] Create pipeline: cd photo-app-users-rest-api-sam && sam pipeline init --bootstrap
[*] Validate SAM template: cd photo-app-users-rest-api-sam && sam validate
[*] Test Function in the Cloud: cd photo-app-users-rest-api-sam && sam sync --stack-name {stack-name} --watch
```

## IAM - AWS Identity and Access Management

AWS Identity and Access Management (IAM) is a web service that controls who can access AWS resources. It also manages permissions for those resources. 
What IAM does Controls who can sign in to AWS, Controls who has permission to use AWS resources, Manages workload and workforce access, and Keeps data safe. 
How IAM works 
Users are individuals or applications that need access to AWS resources
Groups are collections of users
Roles are entities that can be assumed by anyone who needs them
Benefits of IAM Prevents unauthorized access to AWS resources, Prevents unauthorized changes to AWS configurations, Prevents unauthorized deletion of AWS resources, and Prevents unauthorized access to sensitive data. 
IAM features 
Password policy
Multifactor authentication (MFA)
Auto-administration of MFA
Updating credentials
Viewing the last access information to the service of Organizations for a policy
Applying limited managed policies


