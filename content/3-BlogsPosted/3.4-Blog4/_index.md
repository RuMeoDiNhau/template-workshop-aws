---
title: "Blog 4: Getting Started with AWS: A Beginner's Perspective"
date: 2026-07-31
weight: 4
chapter: false
pre: " <b> 3.4. </b> "
---

# Getting Started with AWS: A Beginner's Perspective

> *Article published on the [AWS Study Group VN](https://www.facebook.com/groups/awsstudygroupfcj) community.*

AWS is a vast cloud ecosystem with a wide variety of services. When first starting out, I was quite confused about where to begin and which concepts were most important to understand first.

After spending time reading documentation, watching workshops, and exploring basic AWS services, I've compiled some knowledge that I think will be useful for others who are also getting started with AWS.

This article is not an in-depth technical guide, but rather what I have learned and understood so far. If there's anything I've misunderstood or missed, I would greatly appreciate feedback from everyone so we can learn together.

---

### AWS IS MORE THAN JUST "RENTING A SERVER"

Before learning about AWS, I used to think cloud was simply about putting an application on an Internet server instead of running it on a personal computer.

However, after digging deeper, I realized cloud is much more than that. AWS provides many services to help build, deploy, and operate systems without having to manage all the underlying hardware yourself.

Some fundamental services include:

- **Amazon EC2**: provides virtual servers to run applications.
- **Amazon S3**: stores object-based data such as images, videos, files, etc.
- **Amazon RDS**: provides AWS-managed databases.
- **AWS Lambda**: runs code without needing to manage servers.
- **IAM**: manages users and access permissions to AWS resources.

What I find interesting is that these services don't work in isolation — they typically integrate with each other to form a complete system.

---

### FOUNDATIONAL CONCEPTS WHEN STARTING WITH AWS

#### Region and Availability Zone

These are two concepts I encountered frequently when reading about AWS.

A Region can be simply understood as a geographic area where AWS places its infrastructure. When deploying an application, choosing the right Region can affect latency, cost, and data requirements.

Within a Region, there are usually multiple Availability Zones (AZs). Each AZ is an independent infrastructure area, helping systems maintain stability when issues occur in a specific zone.

Previously, I thought choosing a server location was simply about picking a spot close to users. But after learning more, I understood that designing systems on the cloud also involves scalability and high availability.

---

### IAM - SOMETHING BEGINNERS SHOULDN'T SKIP

When first learning AWS, I tended to focus more on services with immediately visible results like EC2 or S3.

However, the more I learned, the more I realized IAM is a crucial component.

IAM (Identity and Access Management) helps manage users, access permissions, and how AWS services interact with each other.

Some basic concepts:

- **User**: represents an individual user.
- **Group**: a collection of users sharing the same permissions.
- **Role**: permissions granted to a user or service for a specific use case.
- **Policy**: a set of rules defining what is allowed or denied.

The most important principle I found in IAM is **Least Privilege** — only grant the exact permissions that are needed.

For example, if an application only needs to read data from S3, it shouldn't have permission to delete all data in the bucket.

Through learning about IAM, I began to realize that security is not something to address last — it needs attention from the very beginning of system design.

---

### AWS SERVICES ARE INTERCONNECTED

One thing I find quite interesting when learning AWS is that the more you explore one service, the more you encounter other services.

For example:

- **EC2** relates to VPC and Security Groups.
- **S3** relates to IAM and access control.
- **Database on RDS** relates to networking and security.

At first, I felt overwhelmed by how much there is to learn on AWS, but later I understood that this is exactly how AWS is built. Each service solves a specific problem, and when combined, they form a complete system.

---

### REFLECTIONS AFTER STARTING WITH AWS

Currently, I am still a beginner in my AWS learning journey, and there is certainly much more to explore.

However, what I've realized after my initial time with AWS is that you shouldn't try to learn every service at once. What's more important is understanding what problem each service was created to solve and how they work together.

For me, starting with foundational concepts like Cloud Computing, Region, Availability Zone, IAM, and popular services like EC2 and S3 made approaching AWS much easier.

Thank you for taking the time to read this article. If you have additional perspectives, experiences, or suggestions, I would love to discuss further in the comments section.

---

### 📚 REFERENCES

- AWS Study Group: [https://www.youtube.com/@AWSStudyGroup](https://www.youtube.com/@AWSStudyGroup)
