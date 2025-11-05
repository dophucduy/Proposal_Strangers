---
title: "Đề xuất Strangers"
date: 2024-01-01T00:00:00Z
draft: false
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@400;700&display=swap');
body, html {
  font-family: 'Noto Sans', Arial, Helvetica, sans-serif;
}
</style>


## 🐦 Đề xuất: Flyora – Nền tảng Thương mại Điện tử cho Người yêu Chim

### 1. Tóm tắt Điều hành
Flyora là một ứng dụng web chuyên biệt được thiết kế để phục vụ những người đam mê chim cảnh trên khắp Việt Nam. Nền tảng cung cấp các sản phẩm được tuyển chọn như thức ăn chim, đồ chơi, lồng và phụ kiện trang trí phù hợp với các loài như Chào Mào, Vẹt, Yến Phụng và Chích Chòe. Được xây dựng với công nghệ web hiện đại và lưu trữ trên AWS, Flyora đảm bảo khả năng mở rộng, hiệu suất và truy cập an toàn. Nền tảng hướng tới trở thành điểm đến hàng đầu cho việc chăm sóc và trang trí chim, kết hợp thương mại điện tử với cá nhân hóa và tương tác cộng đồng.

---

### 2. Phát biểu Vấn đề
**Thách thức Hiện tại**:
- Không có nền tảng tập trung cho các sản phẩm chuyên biệt về chim
- Các cửa hàng thú cưng chung thiếu khuyến nghị theo từng loài
- Giao diện người dùng lỗi thời và khả năng đáp ứng di động kém
- Khả năng mở rộng backend và tìm kiếm hạn chế

**Giải pháp Đề xuất**:
Flyora mang đến trải nghiệm mua sắm theo danh mục đáp ứng với xác thực người dùng an toàn, lọc sản phẩm thời gian thực và backend có thể mở rộng. Hỗ trợ cả người dùng desktop và di động, với kế hoạch tương lai cho khuyến nghị được hỗ trợ AI và chatbot.

---

### 3. Kiến trúc Giải pháp
#### 📄 Sơ đồ Kiến trúc Hệ thống
![Sơ đồ Kiến trúc Hệ thống](/images/SystemArch.drawio.png)

#### 🧩 Frontend (Tầng Web)
* **Amazon S3**: Lưu trữ web tĩnh cho tài sản frontend
* **CloudFront**: CDN cho phân phối nội dung toàn cầu
* **Thiết kế đáp ứng**: Giao diện thân thiện với di động

#### 🔐 Xác thực & Bảo mật
* **Amazon Cognito**: Xác thực và ủy quyền người dùng
* **IAM**: Quản lý danh tính và truy cập
* **CloudWatch**: Giám sát và lớp bảo mật

#### 🔄 Dịch vụ Backend (Tầng Ứng dụng)
* **Amazon API Gateway**: Quản lý API RESTful
* **AWS Lambda Functions**: 
  - Xử lý chatbot
  - Xử lý API
  - Tự động hóa nhập
* **Amazon Bedrock**: Mô hình nhúng và LLM cho các tính năng AI

#### 📦 Dữ liệu & Lưu trữ (Tầng Dữ liệu)
* **Amazon RDS for PostgreSQL**: Cơ sở dữ liệu quan hệ
* **DynamoDB**: Cơ sở dữ liệu NoSQL
* **Amazon S3**: Lưu trữ dữ liệu

#### 🔧 CI/CD & Phát triển
* **GitLab**: Kiểm soát phiên bản và kích hoạt pipeline CI/CD
* **AWS CodeBuild**: Quy trình xây dựng tự động
* **AWS CodePipeline**: Tích hợp và triển khai liên tục

---

### 4. Triển khai Kỹ thuật

#### Các Giai đoạn:
1. **Học AWS & Thiết lập** – Thành thạo các dịch vụ AWS và thiết kế kiến trúc
2. **Phát triển & Tích hợp** – Xây dựng frontend và kết nối backend AWS
3. **Kiểm thử & Triển khai** – Hoàn thành kiểm thử và phát hành sản xuất

#### Tháng 1 - Tập trung Học AWS:
- **Tuần 1-2**: Cơ bản AWS (S3, Lambda, API Gateway, DynamoDB)
- **Tuần 3**: Dịch vụ nâng cao (Cognito, Bedrock, OpenSearch)
- **Tuần 4**: Thiết kế kiến trúc và mô hình hóa cơ sở dữ liệu với MySQL Workbench

#### Yêu cầu Kỹ thuật:
- Thành thạo dịch vụ AWS cho kiến trúc serverless
- Phát triển frontend với lưu trữ tĩnh S3
- DynamoDB cho quản lý dữ liệu NoSQL
- GitHub cho kiểm soát phiên bản và tích hợp CI/CD

---

### 5. Lịch trình & Cột mốc

| Giai đoạn                | Thời gian  | Cột mốc Chính                               |
|--------------------------|------------|---------------------------------------------|
| **Tháng 1: Học AWS**    | 4 tuần     | • Thành thạo cơ bản AWS<br>• Thiết kế kiến trúc<br>• Tạo lược đồ cơ sở dữ liệu |
| **Tháng 2: Phát triển** | 4 tuần     | • Hoàn thành UI frontend<br>• Xây dựng hàm Lambda<br>• Cấu hình API Gateway |
| **Tháng 3: Tích hợp**   | 4 tuần     | • Tích hợp hệ thống đầy đủ<br>• Hoàn thành kiểm thử<br>• Triển khai sản xuất |

---

### 6. Ước tính Ngân sách

| Mục                              | Chi phí Hàng tháng | Chi phí Hàng năm |
|-----------------------------------|-------------------|------------------|
| Amazon S3 + CloudFront            | $0.20             | $2.40            |
| AWS Lambda                       | $0.00             | $0.00            |
| Amazon API Gateway                | $0.01             | $0.12            |
| DynamoDB                          | $0.25             | $3.00            |
| Amazon Cognito                    | $0.08             | $0.96            |
| CloudWatch & Logs                 | $0.05             | $0.60            |
| Amazon Bedrock (Nhúng/LLM)        | $0.10             | $1.20            |
| Amazon RDS for PostgreSQL         | $0.20             | $2.40            |
| CodePipeline/CodeBuild            | $0.05             | $0.60            |
| **Tổng Ước tính**                 | **$0.94**         | **$11.28**       |

Chi phí phần cứng không áp dụng vì Flyora là nền tảng chỉ web.

---

### 7. Đánh giá Rủi ro

| Rủi ro                      | Tác động   | Xác suất   | Chiến lược Giảm thiểu                        |
|-----------------------------|------------|------------|----------------------------------------------|
| Lambda cold starts          | Trung bình | Trung bình | Đồng thời được cung cấp cho các hàm quan trọng |
| DynamoDB throttling         | Trung bình | Thấp       | Tự động mở rộng và thiết kế khóa phân vùng phù hợp |
| RDS downtime                | Trung bình | Thấp       | Triển khai Multi-AZ, sao lưu tự động          |
| Vượt chi phí                | Thấp       | Thấp       | Giám sát với AWS Budgets và cảnh báo CloudWatch |
| Giới hạn API Bedrock        | Trung bình | Thấp       | Giám sát sử dụng, dự phòng kết quả cache      |

---

### 8. Kết quả Mong đợi

#### Cải tiến Kỹ thuật:
- Giao diện người dùng đáp ứng, thân thiện với di động
- Xác thực người dùng an toàn và quản lý vai trò (Cognito, IAM)
- Backend có thể mở rộng với Lambda/API Gateway
- Lọc sản phẩm thời gian thực và hỗ trợ chatbot
- Tính năng AI qua Bedrock (Nhúng/LLM)
- Lưu trữ dữ liệu mạnh mẽ với RDS, DynamoDB, S3

#### Giá trị Kinh doanh:
- Nền tảng tập trung cho người yêu chim ở Việt Nam
- Giảm phụ thuộc vào các cửa hàng thú cưng chung
- Nền tảng cho các tính năng AI và mở rộng cộng đồng tương lai
- Tiềm năng cho ứng dụng di động và tích hợp chatbot