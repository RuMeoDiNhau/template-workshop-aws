---
title: "Blog 5: Một ứng dụng web được xây dựng trên Cloud như thế nào?"
date: 2026-07-31
weight: 5
chapter: false
pre: " <b> 3.5. </b> "
---

# Một ứng dụng web được xây dựng trên Cloud như thế nào?

> *Bài viết được chia sẻ bởi tác giả trên cộng đồng [AWS Study Group VN](https://www.facebook.com/groups/awsstudygroupfcj).*

Khi mới tìm hiểu AWS, mình từng nghĩ việc đưa một ứng dụng lên Cloud chỉ đơn giản là đưa source code lên một máy chủ rồi chạy. Nhưng sau khi tìm hiểu thêm, mình nhận ra để một ứng dụng web hoạt động ổn định trên Cloud thì phía sau còn có nhiều thành phần khác nhau cùng phối hợp.

Trong bài viết này, mình thử tìm hiểu cách một ứng dụng web cơ bản có thể được xây dựng trên AWS dưới góc nhìn của một người mới bắt đầu. Đây là những kiến thức mình tổng hợp được trong quá trình tìm hiểu, nếu có phần nào chưa chính xác hoặc còn thiếu sót, mình rất mong nhận được góp ý từ mọi người.

---

### MỘT ỨNG DỤNG WEB CẦN NHỮNG GÌ ĐỂ HOẠT ĐỘNG?

Khi truy cập một website, người dùng thường chỉ nhìn thấy phần giao diện bên ngoài. Tuy nhiên, để website có thể hoạt động, phía sau thường sẽ gồm nhiều thành phần khác nhau.

Ví dụ với một website bán hàng đơn giản:

- Người dùng cần một giao diện để xem sản phẩm.
- Hệ thống cần nơi xử lý đăng nhập, đặt hàng.
- Dữ liệu sản phẩm và người dùng cần được lưu trữ.
- Các file như hình ảnh sản phẩm cần có nơi lưu giữ.
- Hệ thống cần được bảo vệ và theo dõi trong quá trình hoạt động.

Khi tìm hiểu AWS, mình nhận ra Cloud không chỉ cung cấp một nơi để chạy ứng dụng, mà còn cung cấp các dịch vụ riêng cho từng nhu cầu trong hệ thống.

---

### TỪ MỘT REQUEST CỦA NGƯỜI DÙNG ĐẾN HỆ THỐNG PHÍA SAU

Giả sử người dùng truy cập vào một website.

Đầu tiên, request từ người dùng cần được gửi đến hệ thống xử lý. AWS cung cấp nhiều cách để triển khai phần này, ví dụ như sử dụng **Amazon EC2** để chạy backend trên một máy chủ ảo hoặc sử dụng **AWS Lambda** để thực thi code theo nhu cầu.

Sau khi nhận được request, backend có thể cần truy xuất dữ liệu từ database.

Ví dụ:

- Kiểm tra thông tin tài khoản.
- Lấy danh sách sản phẩm.
- Lưu thông tin đơn hàng.

Đối với phần dữ liệu, AWS cung cấp các dịch vụ như **Amazon RDS** giúp triển khai và quản lý database dễ dàng hơn.

---

### DỮ LIỆU ĐƯỢC LƯU TRỮ NHƯ THẾ NÀO TRÊN CLOUD?

Một điều mình thấy thú vị khi tìm hiểu Cloud là dữ liệu không nhất thiết phải nằm chung một nơi.

Ví dụ trong một website bán hàng:

- Thông tin sản phẩm, tài khoản người dùng có thể lưu trong database.
- Hình ảnh sản phẩm có thể lưu trên **Amazon S3**.

Việc tách riêng phần lưu trữ giúp hệ thống dễ quản lý hơn và phù hợp với từng loại dữ liệu.

Qua phần này, mình hiểu thêm rằng khi thiết kế hệ thống, việc lựa chọn nơi lưu trữ dữ liệu cũng là một quyết định quan trọng chứ không chỉ đơn giản là "lưu ở đâu cũng được".

---

### NGOÀI VIỆC CHẠY ĐƯỢC, HỆ THỐNG CÒN CẦN ĐƯỢC QUẢN LÝ

Ban đầu khi tìm hiểu AWS, mình thường tập trung vào câu hỏi:

*"Làm sao để ứng dụng chạy được?"*

Nhưng sau đó mình nhận ra còn nhiều vấn đề khác cần quan tâm:

- Ai có quyền truy cập vào tài nguyên?
- Làm sao giới hạn những truy cập không cần thiết?
- Làm sao theo dõi khi hệ thống gặp vấn đề?

AWS có các dịch vụ hỗ trợ những vấn đề này, ví dụ:

- **IAM** giúp quản lý quyền truy cập.
- **VPC** giúp tổ chức môi trường mạng.
- **CloudWatch** hỗ trợ theo dõi trạng thái hoạt động của hệ thống.

Điều này giúp mình hiểu rằng xây dựng ứng dụng trên Cloud không chỉ là triển khai code, mà còn liên quan đến bảo mật và vận hành.

---

### ĐIỀU MÌNH NHẬN RA KHI TÌM HIỂU CÁCH MỘT ỨNG DỤNG CHẠY TRÊN AWS

Điều khó nhất khi mới học AWS có lẽ là số lượng service khá lớn. Ban đầu mình thấy mỗi service như một phần riêng biệt và khá khó hình dung chúng liên quan với nhau như thế nào.

Nhưng khi đặt AWS vào một bài toán cụ thể như xây dựng một website, mình bắt đầu hiểu được vai trò của từng thành phần:

- **Compute** để chạy ứng dụng.
- **Database** để lưu trữ dữ liệu.
- **Storage** để quản lý file.
- **Security** để bảo vệ hệ thống.
- **Monitoring** để theo dõi hoạt động.

Từ đó, mình thấy việc học AWS không nên bắt đầu bằng việc cố nhớ thật nhiều service, mà nên bắt đầu từ cách một hệ thống hoạt động và những vấn đề nó cần giải quyết.

---

### KẾT LẠI

Hiện tại mình vẫn đang trong quá trình tìm hiểu AWS và còn nhiều kiến thức cần học thêm. Tuy nhiên, việc nhìn AWS thông qua một ứng dụng cụ thể giúp mình dễ tiếp cận hơn rất nhiều.

Thay vì xem AWS là một tập hợp rất nhiều dịch vụ rời rạc, mình bắt đầu hiểu nó như một bộ công cụ giúp xây dựng, triển khai và vận hành một hệ thống hoàn chỉnh trên Cloud.

Đây là những gì mình tìm hiểu được ở thời điểm hiện tại. Nếu có phần nào chưa chính xác hoặc có cách tiếp cận khác, mình rất mong nhận được góp ý từ mọi người.

---

### 📚 NGUỒN THAM KHẢO

- AWS Architecture Center: [https://aws.amazon.com/architecture/](https://aws.amazon.com/architecture/)
- AWS Documentation: [https://docs.aws.amazon.com/](https://docs.aws.amazon.com/)
