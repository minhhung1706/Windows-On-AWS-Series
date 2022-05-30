---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Session Manager** là một chức năng nằm trong dịch vụ System Manager của AWS, Session Manager cung cấp khả năng quản lý các máy chủ một cách an toàn mà **không cần mở port SSH, không cần Bastion Host hoặc quản lý SSH key**. 
Session Manager cũng giúp dễ dàng tuân thủ các chính sách của công ty yêu cầu quyền truy cập có kiểm soát, đảm bảo việc bảo mật nghiêm ngặt và ghi log truy việc truy cập trong khi vẫn cung cấp cho người dùng cuối quyền truy cập đa nền tảng.

Với việc sử dụng Session Manager, bạn sẽ có được những ưu điểm sau:

- Không cần phải mở cổng 22 cho giao thức SSH.
- Có thể cấu hình để kết nối không cần đi ra ngoài internet.
- Không cần quản lý private key của server để kết nối SSH.
- Quản lý tập trung được user bằng việc sử dụng AWS IAM.
- Truy cập tới server một cách dễ dàng và đơn giản bằng một cú click chuột.
- Thời gian truy cập nhanh chóng hơn các phương thức truyền thống như SSH.
- Hỗ trợ nhiều hệ điều hành khác nhau như Linux, Windows, MacOS.
- Log lại được các phiên kết nối và các câu lệnh đã thực thi trong lúc kết nối tới server.

Với những ưu điểm trên, bạn có thể sử dụng Session Manager thay vì sử dụng kỹ thuật Bastion host giúp chúng ta tiết kiệm được thời gian và chi phí khi quản lý server Bastion.