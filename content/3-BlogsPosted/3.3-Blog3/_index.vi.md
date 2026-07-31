---
title: "Blog 3: Bắt đầu với AWS: Làm quen với Amazon S3"
date: 2026-07-31
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Bắt đầu với AWS: Làm quen với Amazon S3

> *Bài viết được chia sẻ bởi tác giả trên cộng đồng [AWS Study Group VN](https://www.facebook.com/groups/awsstudygroupfcj).*

Khi mới tìm hiểu AWS, một trong những dịch vụ đầu tiên mình gặp là Amazon S3. Ban đầu mình chỉ hiểu đơn giản S3 là nơi để lưu file trên Cloud. Tuy nhiên, sau khi tìm hiểu thêm, mình nhận ra S3 không chỉ là một nơi lưu trữ dữ liệu, mà còn là một phần quan trọng trong nhiều hệ thống được xây dựng trên AWS.

Trong bài viết này, mình chia sẻ những gì mình tìm hiểu được về Amazon S3 dưới góc nhìn của một người mới bắt đầu làm quen với AWS. Nếu có nội dung nào mình hiểu chưa đúng hoặc còn thiếu sót, mình rất mong nhận được góp ý từ mọi người.

---

### AMAZON S3 LÀ GÌ?

Amazon S3 (Simple Storage Service) là một dịch vụ lưu trữ dữ liệu dạng object trên AWS.

Nếu như trong máy tính cá nhân, mình thường lưu file trong các thư mục thì S3 có một cách tổ chức khác. Dữ liệu được lưu dưới dạng object và được quản lý trong các bucket.

Có thể hình dung:

- **Bucket** giống như một nơi chứa dữ liệu.
- **Object** là các file được lưu bên trong bucket.

Ví dụ, một website bán hàng có thể sử dụng S3 để lưu:

- Hình ảnh sản phẩm.
- Video.
- File tài liệu.
- File người dùng tải lên.

Điểm khác biệt là thay vì phải tự quản lý ổ cứng hoặc server lưu trữ, AWS sẽ đảm nhiệm phần hạ tầng phía dưới.

---

### VÌ SAO KHÔNG LƯU TẤT CẢ DỮ LIỆU TRÊN SERVER?

Trước khi tìm hiểu Cloud, mình thường nghĩ rằng một website có thể lưu mọi thứ trên cùng một server:

- Code chạy trên server.
- Database trên server.
- Hình ảnh cũng lưu trên server.

Tuy nhiên, khi tìm hiểu cách các hệ thống thực tế được xây dựng, mình nhận ra việc tách riêng từng phần sẽ có nhiều lợi ích hơn.

Ví dụ:

- **Backend** tập trung xử lý logic.
- **Database** tập trung lưu dữ liệu có cấu trúc.
- **S3** đảm nhiệm việc lưu trữ file.

Cách tiếp cận này giúp hệ thống dễ quản lý hơn và phù hợp khi cần mở rộng.

---

### MỘT VÀI KHÁI NIỆM CƠ BẢN TRONG S3

#### Bucket

Bucket là nơi chứa các object trên S3.

Khi sử dụng S3, bước đầu tiên thường là tạo một bucket để lưu trữ dữ liệu.

Một bucket có thể chứa nhiều loại dữ liệu khác nhau, nhưng trong thực tế người dùng thường tổ chức bucket theo mục đích.

Ví dụ:

- Bucket lưu ảnh website.
- Bucket lưu file backup.
- Bucket lưu dữ liệu phục vụ ứng dụng.

#### Object

Object là đơn vị dữ liệu được lưu trong S3.

Một object bao gồm:

- Nội dung file.
- Metadata mô tả thông tin của file.
