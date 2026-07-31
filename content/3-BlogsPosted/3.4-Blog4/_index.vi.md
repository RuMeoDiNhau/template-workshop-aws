---
title: "Blog 4: Bắt đầu với AWS: Góc nhìn người mới"
date: 2026-07-31
weight: 4
chapter: false
pre: " <b> 3.4. </b> "
---

# Bắt đầu với AWS: Góc nhìn người mới

> *Bài viết được chia sẻ bởi tác giả trên cộng đồng [AWS Study Group VN](https://www.facebook.com/groups/awsstudygroupfcj).*

AWS là một hệ sinh thái cloud khá rộng với rất nhiều dịch vụ khác nhau. Khi mới bắt đầu tìm hiểu, mình từng khá bối rối vì không biết nên bắt đầu từ đâu, cũng như những khái niệm nào là quan trọng cần nắm trước.

Sau một thời gian đọc tài liệu, xem workshop và tìm hiểu các dịch vụ cơ bản trên AWS, mình tổng hợp lại một số kiến thức mà mình nghĩ sẽ hữu ích cho những bạn cũng đang bắt đầu làm quen với AWS.

Bài viết này không phải là một bài hướng dẫn chuyên sâu, mà là những gì mình tìm hiểu và hiểu được ở thời điểm hiện tại. Nếu có nội dung nào mình hiểu chưa đúng hoặc còn thiếu sót, mình rất mong nhận được góp ý từ mọi người để cùng học hỏi thêm.

---

### AWS KHÔNG CHỈ ĐƠN GIẢN LÀ "THUÊ MỘT CÁI SERVER"

Trước khi tìm hiểu AWS, mình từng nghĩ cloud chỉ là việc đưa ứng dụng lên một máy chủ trên Internet thay vì chạy trên máy cá nhân.

Tuy nhiên, sau khi tìm hiểu sâu hơn, mình nhận ra cloud còn nhiều hơn thế. AWS cung cấp rất nhiều dịch vụ giúp xây dựng, triển khai và vận hành một hệ thống mà không cần tự quản lý toàn bộ phần cứng phía dưới.

Một số dịch vụ cơ bản có thể kể đến:

- **Amazon EC2**: cung cấp máy chủ ảo để chạy ứng dụng.
- **Amazon S3**: lưu trữ dữ liệu dạng object như hình ảnh, video, file,...
- **Amazon RDS**: cung cấp database được AWS quản lý.
- **AWS Lambda**: chạy code mà không cần tự quản lý server.
- **IAM**: quản lý người dùng và quyền truy cập vào tài nguyên AWS.

Điều mình thấy thú vị là các dịch vụ này không hoạt động riêng lẻ, mà thường kết hợp với nhau để tạo thành một hệ thống hoàn chỉnh.

---

### MỘT VÀI KHÁI NIỆM NỀN TẢNG KHI BẮT ĐẦU TÌM HIỂU AWS

#### Region và Availability Zone

Đây là hai khái niệm mình gặp khá nhiều khi đọc về AWS.

Region có thể hiểu đơn giản là một khu vực địa lý nơi AWS đặt hạ tầng của mình. Khi triển khai một ứng dụng, việc lựa chọn Region phù hợp có thể ảnh hưởng đến độ trễ, chi phí cũng như yêu cầu về dữ liệu.

Bên trong một Region thường có nhiều Availability Zone (AZ). Mỗi AZ là một khu vực hạ tầng độc lập, giúp hệ thống có khả năng hoạt động ổn định hơn khi xảy ra sự cố ở một khu vực cụ thể.

Trước đây mình chỉ nghĩ việc chọn nơi đặt server đơn giản là chọn vị trí gần người dùng. Nhưng khi tìm hiểu thêm, mình mới hiểu rằng thiết kế hệ thống trên cloud còn liên quan đến khả năng mở rộng và tính sẵn sàng.

---

### IAM - PHẦN MÌNH NGHĨ NGƯỜI MỚI KHÔNG NÊN BỎ QUA

Ban đầu khi mới tìm hiểu AWS, mình thường chú ý nhiều hơn đến những service có thể nhìn thấy kết quả ngay như EC2 hoặc S3.

Tuy nhiên, càng tìm hiểu mình càng nhận ra IAM là một phần rất quan trọng.

IAM (Identity and Access Management) giúp quản lý người dùng, quyền truy cập và cách các dịch vụ AWS tương tác với nhau.

Một số khái niệm cơ bản:

- **User**: đại diện cho một người dùng.
- **Group**: nhóm các user có chung quyền.
- **Role**: quyền được cấp cho user hoặc service trong một trường hợp cụ thể.
- **Policy**: tập hợp các quy tắc xác định quyền được phép hoặc bị từ chối.

Điều mình thấy quan trọng nhất ở IAM là nguyên tắc **Least Privilege** - chỉ cấp đúng những quyền cần thiết.

Ví dụ, nếu một ứng dụng chỉ cần đọc dữ liệu từ S3 thì không nhất thiết phải có quyền xóa toàn bộ dữ liệu trong bucket.

Qua việc tìm hiểu IAM, mình bắt đầu nhận ra bảo mật không phải là phần làm sau cùng, mà cần được quan tâm ngay từ khi thiết kế hệ thống.

---

### CÁC SERVICE TRÊN AWS CÓ SỰ LIÊN KẾT VỚI NHAU

Một điều mình thấy khá thú vị khi học AWS là càng tìm hiểu một service thì lại gặp thêm những service khác.

Ví dụ:

- **EC2** liên quan đến VPC, Security Group.
- **S3** liên quan đến IAM và quyền truy cập.
- **Database trên RDS** liên quan đến network và security.

Lúc đầu mình hơi cảm thấy AWS có quá nhiều thứ cần học, nhưng sau đó mình hiểu rằng đây cũng chính là cách AWS được xây dựng. Mỗi service giải quyết một vấn đề riêng, và khi kết hợp lại sẽ tạo thành một hệ thống hoàn chỉnh.

---

### MỘT VÀI SUY NGHĨ SAU KHI BẮT ĐẦU TÌM HIỂU AWS

Hiện tại mình vẫn còn là người mới trong quá trình học AWS và chắc chắn còn rất nhiều điều cần tìm hiểu thêm.

Tuy nhiên, điều mình nhận ra sau khoảng thời gian đầu làm quen với AWS là không nên cố gắng học tất cả dịch vụ cùng một lúc. Quan trọng hơn là hiểu được từng service được tạo ra để giải quyết vấn đề gì và cách chúng kết hợp với nhau.

Với mình, việc bắt đầu từ những khái niệm nền tảng như Cloud Computing, Region, Availability Zone, IAM hay các service phổ biến như EC2, S3 giúp việc tiếp cận AWS dễ dàng hơn rất nhiều.

Cảm ơn mọi người đã dành thời gian đọc bài viết. Nếu mọi người có thêm góc nhìn, kinh nghiệm hoặc góp ý, mình rất mong được trao đổi thêm ở phần bình luận.

---

### 📚 NGUỒN THAM KHẢO

- AWS Study Group: [https://www.youtube.com/@AWSStudyGroup](https://www.youtube.com/@AWSStudyGroup)
