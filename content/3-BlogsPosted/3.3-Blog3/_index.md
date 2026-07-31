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
- A **Key** used to identify the location of an object within a bucket.

For example, an image could be stored with the path:

```
images/product01.png
```

S3 uses this key to manage objects instead of a physical folder structure like on a computer.

---

### S3 AND ACCESS CONTROL

One aspect I found important when learning about S3 is security.

Initially, I thought storing files on the Cloud only required attention to storage capacity and speed. However, in reality, controlling who can access data is equally important.

AWS provides mechanisms such as:

- **IAM** to manage user and service permissions.
- **Bucket Policy** to control access to buckets.
- **Access Control** to manage permissions for objects.

For example:

A website may allow everyone to view product images, but should not let personal user data be publicly accessible.

Through learning about S3, I realized that data storage always goes hand-in-hand with access control management.

---

### S3 IS NOT JUST FOR STORING FILES

At first, I thought S3 was only suitable for storing images or documents.

But upon further research, I realized S3 is also used in many other scenarios:

- Storing backup data.
- Storing system logs.
- Storing data for analytics.
- Storing files for web/mobile applications.

An interesting point is that S3 can integrate with many other AWS services.

For example:

- Applications use **S3** to store files.
- **Lambda** processes data when new files are uploaded.
- **CloudFront** distributes content faster to users.

---

### INSIGHTS FROM LEARNING ABOUT S3

What I find most interesting about S3 is that AWS doesn't just provide a place to store data — it also provides ways to manage that data flexibly.

Initially, I approached S3 as a "hard drive on the Cloud." But after learning more, I understood that S3 is a component that can play a critical role in the architecture of many applications.

For beginners learning AWS, I think S3 is a very suitable service to start with because it helps understand one of the key ideas of Cloud computing: **separating data storage from application processing**.

---

### CONCLUSION

Currently, I am still in the process of learning AWS, and Amazon S3 is just one of the first services I have explored.

Through learning about S3, I gained not only knowledge about a storage service, but also a deeper understanding of how Cloud systems are designed: each component has its own responsibility and can be combined to form a complete system.

This is what I have learned about Amazon S3 so far. If there is anything inaccurate or if you have practical experience to share, I would greatly appreciate your feedback.

---

### 📚 REFERENCES

- Amazon S3 Documentation: [https://docs.aws.amazon.com/s3/](https://docs.aws.amazon.com/s3/)
- Amazon S3 Overview: [https://aws.amazon.com/s3/](https://aws.amazon.com/s3/)
