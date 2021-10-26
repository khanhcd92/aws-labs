
# Final Mock

Phần này sẽ để kiểm tra lại toàn bộ khoá học mà mọi người đã tham giá trên Udemy

## Nội dung

- Đề bài
- Yêu cầu
- Output

### Đề bài

Khách hàng đang có 1 hệ thống Jira đang chạy trên on-premise. Bây giờ khách muốn migrate nó lên cloud để giảm tải chi phí vận hành và cho các bên vendor khác có thể access vào được. Khách hàng có vài yêu cầu về non function như bên dưới cần được đảm bảo khi migrate hệ thống:

- Hệ thống phải đáp ứng được High Available và Fault Tolerant
- Họ có trace được log khi hệ thống xảy ra vấn đề
- Dữ liệu phải được backup 1 ngày 1 lần vào 12:30 đêm và lưu trữ tới 30 ngày sau đó
- Hệ thống cho phép downtime khi migrate dữ liệu từ on-premise lên cloud
- Hệ thống có thể đáp ứng 100 người cùng thời điểm

### Yều cầu

1. Dựa vào đề bài vẽ architecture của việc migrate hệ thống jira lên cloud
2. Dùng CloudFormation để triển khai Infrastructure

   - Template triển khai VPC
   - Template triển khai Jira

### Output

1. File draw.io cho việc vẽ architecture
2. File template CloudFormation
