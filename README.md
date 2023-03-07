# FLOW OF EXECUTION
1. Đăng ký tên miền (ở đây sử dụng Godaddy để đăng ký tên miền tamnguyen.cloud).
2. Đăng nhập vào AWS Account đã tạo.
3. Đăng ký AWS Certificate Manager (ACM) và trỏ đến tên miền tamnguyen.cloud.
4. Tạo Key Pairs.
###myKey.pem
chmod 400 myKey.pem
5. Tạo Security Groups.
- 
6. Khởi tạo các Instances dành cho TomCat Server, RDS MySQL Server, Elastic Cache Server, Amazon MQ Server.
7. Tạo Private Domain trong Route53 và gán các Private IP các Servers: RDS MySQL Server, Elastic Cache Server, Amazon MQ Server để chúng giao tiếp với nhau.
8. Triển khai App dựa trên Source Code.
9. Tạo S3 Bucket để lưu Artifact.
10. Download Artifact từ S3 Bucket ở trên về máy TomCat Server và khởi động lại dịch vụ TomCat.
11. Cài đặt Elastic Load Balancer với giao thức HTTPS (sử dụng Certificate từ ACM ở trên).
12. Ánh xạ ELB Endpoint đến tên Website qua phần cấu hình DNS trên Godaddy.
13. Xác thực ứng dụng đã hoạt động.
14. Cài đặt Auto Scaling Group cho ứng dụng.

-Tam Nguyen-
