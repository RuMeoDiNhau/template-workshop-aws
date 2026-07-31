---
title: "Blog 3: Getting Started with AWS: Introduction to Amazon S3"
date: 2026-07-31
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Getting Started with AWS: Introduction to Amazon S3

> *Article published on the [AWS Study Group VN](https://www.facebook.com/groups/awsstudygroupfcj) community.*

When first exploring AWS, one of the earliest services I encountered was Amazon S3. Initially, I simply understood S3 as a place to store files on the Cloud. However, after further research, I realized that S3 is not just a data storage service, but also a critical component in many systems built on AWS.

In this article, I share what I've learned about Amazon S3 from the perspective of a beginner getting started with AWS. If there's anything I've misunderstood or missed, I would greatly appreciate feedback from everyone.

---

### WHAT IS AMAZON S3?

Amazon S3 (Simple Storage Service) is an object storage service on AWS.

On a personal computer, we typically save files in folders, but S3 organizes data differently. Data is stored as objects and managed within buckets.

Think of it this way:

- A **Bucket** is like a container for data.
- An **Object** is a file stored inside a bucket.

For example, an e-commerce website might use S3 to store:

- Product images.
- Videos.
- Documents.
- User-uploaded files.

The key difference is that instead of managing hard drives or storage servers yourself, AWS handles the underlying infrastructure.

---

### WHY NOT STORE EVERYTHING ON THE SERVER?

Before learning about Cloud, I used to think a website could store everything on a single server:

- Code running on the server.
- Database on the server.
- Images also stored on the server.

However, when studying how real-world systems are built, I realized that separating each component provides many more benefits.

For example:

- **Backend** focuses on processing logic.
- **Database** focuses on storing structured data.
- **S3** handles file storage.

This approach makes the system easier to manage and suitable for scaling.

---

### BASIC CONCEPTS IN S3

#### Bucket

A Bucket is where objects are stored in S3.

When using S3, the first step is usually to create a bucket for storing data.

A bucket can contain many different types of data, but in practice, users typically organize buckets by purpose.

For example:

- Bucket for website images.
- Bucket for backup files.
- Bucket for application data.

#### Object

An Object is the unit of data stored in S3.

An object consists of:

- File content.
- Metadata describing information about the file.
