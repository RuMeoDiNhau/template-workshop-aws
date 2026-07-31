---
title: "Blog 4: Amazon S3 - Access Control, Real-World Use Cases and Insights"
date: 2026-07-31
weight: 4
chapter: false
pre: " <b> 3.4. </b> "
---

# Amazon S3 - Access Control, Real-World Use Cases and Insights

> *Article published on the [AWS Study Group VN](https://www.facebook.com/groups/awsstudygroupfcj) community.*

- A **Key** is used to identify the location of an object within a bucket.

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
