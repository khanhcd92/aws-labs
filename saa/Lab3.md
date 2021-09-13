
# Lab 3: Load Balancer and AutoScaling

Phần này sẽ dùng cho sau khi học xong Section 8

#### 1. Tạo EC2 Instance A

Sử dụng ngôn ngữ mình thành thạo để cài đặt 1 static web với Hello A

- Size: t2.micro

- Region: N.Virginia

- VPC: default

- Security group: open port 80, 22

#### 2. Tạo EC2 Instance B

Sử dụng ngôn ngữ mình thành thạo để cài đặt 1 static web với Hello B

- Size: t2.micro

- Region: N.Virginia

- VPC: default

- Security group: open port 80, 22

#### 3. Tạo Application Load Balancer

- Tạo Target group, rồi assign IP của 2 server từ bước 1 và 2 vào

- Tạo Application Load Balancer với listen rule là port 80 rồi chuyển tiếp tới target group đã tạo

- Lấy DNS của Application Load Balancer để access trên browser để kiểm tra nội dung hiển thị trên web

=> Chỗ này mọi nguời thấy được nội dụng được thay đổi Hello A sang Hello B khi load lại trình duyệt thì đã cấu hình thành công

#### 4. Cấu hình Autoscale Group

- Tạo 1 EC2 với web tĩnh

- Tạo AMI từ EC2 đã tạo

- Tạo Application Load Balancing với target group nhưng không chưa add server vào

- Tạo Launch Config
  - Dùng tới bản AMI đã tạo phía trên

- Tạo Autoscaling Group
  - Dùng Launch Config đã tạo phía trên
  - Dùng Application Load Balancer đã tạo phía
  - Desired insance: 2, Min instance: 2, Max instance: 4
  - Cấu hình autoscaling policy theo CPU
    - CPU > 50 thì thêm 1 instance
    - CPU < 50 thì xoá 1 instance

=> Sau khi tạo xong bạn sẽ thấy server sẽ được tạo ra là 2 và được gắn vào autoscaling group và load balancing.