---
title: "Blog 5: How is a Web Application Built on the Cloud?"
date: 2026-07-31
weight: 5
chapter: false
pre: " <b> 3.5. </b> "
---

# How is a Web Application Built on the Cloud?

> *Article published on the [AWS Study Group VN](https://www.facebook.com/groups/awsstudygroupfcj) community.*

When first learning about AWS, I used to think deploying an application to the Cloud was simply about uploading source code to a server and running it. But after further research, I realized that for a web application to run stably on the Cloud, there are many different components working together behind the scenes.

In this article, I explore how a basic web application can be built on AWS from a beginner's perspective. This is knowledge I've compiled during my learning process — if there's anything inaccurate or incomplete, I would greatly appreciate feedback from everyone.

---

### WHAT DOES A WEB APPLICATION NEED TO FUNCTION?

When visiting a website, users typically only see the external interface. However, for a website to function, there are usually many different components working behind the scenes.

For example, with a simple e-commerce website:

- Users need an interface to browse products.
- The system needs a place to handle login and ordering.
- Product and user data needs to be stored.
- Files like product images need a storage location.
- The system needs to be protected and monitored during operation.

When learning about AWS, I realized that Cloud doesn't just provide a place to run applications — it also provides dedicated services for each need within the system.

---

### FROM A USER REQUEST TO THE BACKEND SYSTEM

Suppose a user accesses a website.

First, the user's request needs to be sent to a processing system. AWS provides many ways to deploy this part, such as using **Amazon EC2** to run the backend on a virtual server or using **AWS Lambda** to execute code on demand.

After receiving the request, the backend may need to retrieve data from the database.

For example:

- Checking account information.
- Fetching product listings.
- Saving order information.

For the data layer, AWS provides services like **Amazon RDS** to deploy and manage databases more easily.

---

### HOW IS DATA STORED ON THE CLOUD?

One thing I found interesting when learning about Cloud is that data doesn't necessarily have to be in one place.

For example, in an e-commerce website:

- Product information and user accounts can be stored in a database.
- Product images can be stored on **Amazon S3**.

Separating storage makes the system easier to manage and better suited for each type of data.

From this, I learned that when designing a system, choosing where to store data is also an important decision — not simply "store it anywhere."

---

### BEYOND JUST RUNNING — SYSTEMS ALSO NEED MANAGEMENT

When first learning about AWS, I usually focused on the question:

*"How do I get the application running?"*

But later I realized there are many other concerns:

- Who has access to resources?
- How to limit unnecessary access?
- How to monitor when the system has issues?

AWS has services to address these concerns, for example:

- **IAM** helps manage access permissions.
- **VPC** helps organize the network environment.
- **CloudWatch** supports monitoring system operational status.

This helped me understand that building applications on the Cloud is not just about deploying code — it also involves security and operations.

---

### INSIGHTS FROM LEARNING HOW AN APPLICATION RUNS ON AWS

The hardest part of learning AWS as a beginner is probably the sheer number of services. At first, each service seemed like a separate piece, and it was quite difficult to visualize how they relate to each other.

But when placing AWS in the context of a specific problem like building a website, I began to understand each component's role:

- **Compute** to run the application.
- **Database** to store data.
- **Storage** to manage files.
- **Security** to protect the system.
- **Monitoring** to track operations.

From there, I realized that learning AWS shouldn't start with trying to memorize many services, but rather with understanding how a system works and what problems it needs to solve.

---

### CONCLUSION

Currently, I am still in the process of learning AWS and there is much more knowledge to acquire. However, looking at AWS through a specific application made it much more approachable.

Instead of viewing AWS as a collection of many disparate services, I began to understand it as a toolkit for building, deploying, and operating a complete system on the Cloud.

This is what I have learned so far. If there's anything inaccurate or if you have a different approach, I would greatly appreciate your feedback.

---

### 📚 REFERENCES

- AWS Architecture Center: [https://aws.amazon.com/architecture/](https://aws.amazon.com/architecture/)
- AWS Documentation: [https://docs.aws.amazon.com/](https://docs.aws.amazon.com/)
