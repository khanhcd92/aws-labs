
# Lab 2: EC2

Phần này sẽ dùng cho sau khi học xong Section 5 -> 7

#### 1. Tạo EC2 Instance thông thường

Sử dụng ngôn ngữ mình thành thạo để cài đặt 1 web hoặc api server trên EC2.

- Size: t2.micro

- Region: N.Virginia

- VPC: default

- Security group: open port 80, 22

- Test lại web của mình trên trình duyệt

#### 2. Tạo EC2 với việc sử dụng Userdata

Sử dụng ngôn ngữ mình thành thạo để cài đặt 1 web hoặc api server trên EC2.

- Size: t2.micro

- Region: N.Virginia

- VPC: default

- Security group: open port 80, 22

- Cái phần cài đặt web server sẽ được cài đặt trong Userdata

- Tạo ra EIP rồi gán vào EC2 đã tạo

- Test lại web của mình trên trình duyệt

#### 3. Backup EC2, EBS

- Sử dụng AMI tạo backuo cho EC2

- Tạo backup cho EBS

#### 4. Thêm dung lượng, chia sẻ file với EBS và EFS

**Thêm dung lượng**

- Tạo EBS với dung lượng 10GB

- Attach EBS đã tạo vào EC2 đã tạo ở phần 2

- Kiểm tra lại dung lượng trên EC2 đã tăng lên chưa

**Chia sẻ file với EFS**

- Tạo EFS

- Tạo EFS mount point

- Mount EFS với EC2 đã tạo từ phần 2

- Tạo thử 1 file trên dường dẫn đã mount vào EC2 xem có tạo được file không

#### 5. Optional

- Tạo 1 con Jenkins trên EC2

- Lưu source code 1 web đơn giản trên Github

- Tạo 1 con web server đơn giản trên EC2 với source code lưu trên Github

- Config 1 job trên Jenkins để deploy source code lên EC2 => Keyword liên quan sẽ là deploy by ssh

- Tạo 1 trigger mỗi khi commit code lên Github sẽ gọi sang Jenkins job đã tạo chạy deploy
