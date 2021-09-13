
# Lab 4: RDS and Elastic Cache

Phần này sẽ dùng cho sau khi học xong Section 9

#### 1. Tạo EC2 Instance

- Tạo một Security Group cho EC2
- Sử dụng ngôn ngữ mình thành thạo để cài đặt api server trên EC2

#### 2. Tạo 1 Elastic Cache

- Tạo một Security Group cho Elastic Cache

  - Chỉ cho phép Security Group của EC2 có thể access

- Tạo Elastic Cache với 1 node, sử dụng Security Group đã tạo

#### 3. Tạo 1 RDS MySQL

- Tạo một Security Group cho RDS

  - Chỉ cho phép Security Group của EC2 có thể access

- Tạo RDS MySQL

  - Gán security group đã tạo vào RDS

  - Disable public

#### 4. Deploy source code lên EC2 kết nối với RDS and Elastic Cache
