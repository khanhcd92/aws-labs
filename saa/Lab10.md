
# Lab 10: VPC

Phần này sẽ dùng cho sau khi học xong Section 25

## 1. Không sử dụng VPC Endpoint

- Tạo VPC có CIDR 10.0.0.0/16
- Tạo 1 public subnet A có CIDR: 10.0.1.0/24
- Tạo 1 public subnet B có CIDR: 10.0.2.0/24
- Tạo 1 private subnet A có CIDR: 10.0.3.0/24
- Tạo 1 private subnet B có CIDR: 10.0.4.0/24
- Tạo 1 routable public chứa 2 public subnet A và B
- Tạo 1 routable private chứa 2 private subnet A và B
- Tạo 1 NAT Gateway
- Tạo 1 RDS MySQl trong private subnet A hoặc B
- Tạo 1 S3 bucket
- Tạo 1 Instance profile có quyền upload file lên S3
- Tạo 1 EC2 api server trong private subnet A hoặc B có thể upload file lên S3 và liên kết tới instance profile đã tạo.
- Tạo 1 Application Load Balancer trong cả public subnet A và B rồi liên kết với server EC2
- Test API đã deploy của mình với việc sử dụng DNS của load balancer

## 2. Sử dụng VPC Endpoint

- Làm y hệt như các bước ở mục 1 nhưng thay vì tạo 1 NAT Gateway thì tạo VPC Endpoint cho S3
