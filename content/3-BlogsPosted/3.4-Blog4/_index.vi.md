---
title: "Blog 4: Amazon S3 - Quyền truy cập, ứng dụng thực tế và những điều nhận ra"
date: 2026-07-31
weight: 4
chapter: false
pre: " <b> 3.4. </b> "
---

# Amazon S3 - Quyền truy cập, ứng dụng thực tế và những điều nhận ra

> *Bài viết được chia sẻ bởi tác giả trên cộng đồng [AWS Study Group VN](https://www.facebook.com/groups/awsstudygroupfcj).*

- **Key** dùng để xác định vị trí của object trong bucket.

Ví dụ, một hình ảnh có thể được lưu với đường dẫn:

```
images/product01.png
```

S3 sẽ sử dụng key này để quản lý object thay vì cấu trúc thư mục vật lý như trên máy tính.

---

### S3 VÀ VẤN ĐỀ QUYỀN TRUY CẬP

Một phần mình thấy quan trọng khi tìm hiểu S3 là vấn đề bảo mật.

Ban đầu mình nghĩ việc lưu file lên Cloud chỉ cần quan tâm đến dung lượng và tốc độ. Nhưng thực tế, việc kiểm soát ai có thể truy cập dữ liệu cũng rất quan trọng.

AWS cung cấp các cơ chế như:

- **IAM** để quản lý quyền của người dùng và service.
- **Bucket Policy** để kiểm soát quyền truy cập vào bucket.
- **Access Control** để quản lý quyền đối với object.

Ví dụ:

Một website có thể cho phép mọi người xem hình ảnh sản phẩm, nhưng không nên để file dữ liệu cá nhân của người dùng bị truy cập công khai.

Qua việc tìm hiểu S3, mình nhận ra việc lưu trữ dữ liệu luôn đi kèm với việc quản lý quyền truy cập.

---

### S3 KHÔNG CHỈ DÙNG ĐỂ LƯU FILE

Lúc đầu mình nghĩ S3 chỉ phù hợp để lưu hình ảnh hoặc tài liệu.

Nhưng khi tìm hiểu thêm, mình nhận ra S3 còn được sử dụng trong nhiều trường hợp khác:

- Lưu trữ dữ liệu backup.
- Lưu log của hệ thống.
- Lưu dữ liệu phục vụ phân tích.
- Lưu file cho các ứng dụng web/mobile.

Một điểm mình thấy hay là S3 có thể kết hợp với nhiều dịch vụ khác trong AWS.

Ví dụ:

- Ứng dụng sử dụng **S3** để lưu file.
- **Lambda** xử lý dữ liệu khi có file mới được tải lên.
- **CloudFront** phân phối nội dung nhanh hơn đến người dùng.

---

### MỘT VÀI ĐIỀU MÌNH NHẬN RA KHI TÌM HIỂU S3

Điều mình thấy thú vị nhất ở S3 là AWS không chỉ cung cấp một nơi để lưu dữ liệu, mà còn cung cấp cách để quản lý dữ liệu đó một cách linh hoạt.

Ban đầu mình tiếp cận S3 như một "ổ cứng trên Cloud". Nhưng sau khi tìm hiểu thêm, mình hiểu rằng S3 là một thành phần có thể đóng vai trò quan trọng trong kiến trúc của nhiều ứng dụng.

Với người mới bắt đầu tìm hiểu AWS, mình nghĩ S3 là một service khá phù hợp để làm quen vì nó giúp hiểu được một trong những ý tưởng quan trọng của Cloud: **tách việc lưu trữ dữ liệu khỏi việc xử lý ứng dụng**.

---

### KẾT LẠI

Hiện tại mình vẫn đang trong quá trình tìm hiểu AWS và Amazon S3 chỉ là một trong những dịch vụ đầu tiên mình tiếp cận.
