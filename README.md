# 🔨 Real-time Online Auction System (ROAS)
> **Subject:** Software Architecture and Design (SWD392)  
> **Methodology:** Research-Based Learning (RBL)  
> **Academic Year:** 2026

---

## 📝 1. GIỚI THIỆU DỰ ÁN (PROJECT OVERVIEW)

### 🔹 Bối cảnh thực tế
Đấu giá trực tuyến truyền thống thường gặp phải các vấn đề nghiêm trọng về trải nghiệm người dùng như: giật lag do tải trang liên tục, giá hiển thị không đồng bộ, và đặc biệt là hệ thống bị nghẽn mạng (sập server) vào những giây cuối cùng của phiên đấu giá - thời điểm quyết định người chiến thắng.

### 🔹 Giải pháp của dự án (ROAS)
**Real-time Online Auction System (ROAS)** là một nền tảng đấu giá trực tuyến thế hệ mới, cho phép người dùng tham gia đấu giá các tài sản giá trị cao (đồ sưu tầm, thẻ hiếm, đồ điện tử...) với trải nghiệm **thời gian thực tuyệt đối**. Hệ thống được thiết kế để xử lý kịch bản hàng vạn người cùng nhảy vào "bắn giá" (sniping) ở 5 giây cuối cùng một cách mượt mà và chính xác.

### 🔹 Các tính năng cốt lõi (Key Features)
* **Live Auction Rooms:** Phòng đấu giá ảo tương tác thời gian thực, giá tiền nhảy liên tục không cần load lại trang.
* **Auto-Bid Agent:** Hệ thống robot tự động ra giá hộ người dùng dựa trên mức giá tối đa được cài đặt trước.
* **Anti-Snipe Protection:** Tự động gia hạn thêm 30 giây nếu có lượt ra giá ở những giây cuối cùng, đảm bảo tính công bằng.
* **Instant Notification:** Thông báo ngay lập tức qua WebSocket/Push Notification khi người dùng bị vượt giá (Outbid).

---

## 👥 2. THÀNH VIÊN NHÓM & PHÂN CÔNG NHIỆM VỤ

| Họ và Tên | MSSV |
| :--- | :--- |
| **Lê Hoàng** | DE190435 |
| **Trần Thanh Hưng** | DE190481 |
| **Nguyễn Tiến Quân** | DE190728 |
| **Châu Viết Doãn** | DE190484 |
| **Nguyễn Hữu Tài** | DE190484 |

---

## 🎯 3. ĐỊNH HƯỚNG NGHIÊN CỨU (RBL FOCUS)

Dự án tập trung nghiên cứu bài toán kỹ thuật nâng cao: **Xử lý lượng lớn lượt ra giá đồng thời (High-Concurrency Bidding) với độ trễ thời gian thực (Real-time Latency) mà không gây sai lệch dữ liệu (Race Conditions).**

* **Kiến trúc dự kiến:** Kết hợp Kiến trúc hướng sự kiện (Event-Driven Architecture) với Message Broker (Kafka/RabbitMQ) và Redis Distributed Lock.
* **Design Patterns dự kiến:** State Pattern (quản lý vòng đời phiên), Observer Pattern (cập nhật giá real-time), Command Pattern (đóng gói lệnh bid).

📚 **Danh mục tài liệu nghiên cứu (Research Papers):** `[⏳ ĐANG CẬP NHẬT]`  
*(Danh sách 10-50 bài báo khoa học chất lượng cao từ IEEE/Springer phục vụ định hướng RBL sẽ được nhóm tổng hợp và upload vào thư mục `/research-papers` ở các Sprint tiếp theo).*

---

## 🔗 4. LIÊN KẾT QUẢN LÝ DỰ ÁN (JIRA)

📌 **Jira Board:** [https://quansieunhoc.atlassian.net/jira/software/projects/KAN/boards/2](https://quansieunhoc.atlassian.net/jira/software/projects/KAN/boards/2)

---

## 📄 5. TÀI LIỆU ĐẶC TẢ THIẾT KẾ (RDS)

Tài liệu **Requirement Design Specification (RDS)** chứa toàn bộ bản thiết kế chi tiết (Use Case, Class Diagram, Sequence Diagram, ERD...) nhằm hiện thực hóa lý thuyết môn SWD392 vào dự án.

📁 **Đường dẫn tài liệu:** `[⏳ ĐANG CẬP NHẬT]`  
*(Tài liệu chi tiết sẽ được hoàn thiện dần theo tiến độ môn học tại thư mục `./docs/RDS_Specification.md`).*

---

## � 6. QUẢN LÝ DỰ ÁN (PROJECT MANAGEMENT)

**Jira Project:** [Real-time Online Auction System (ROAS)](https://hungthanh18122005.atlassian.net/?continue=https%3A%2F%2Fhungthanh18122005.atlassian.net%2Fwelcome%2Fsoftware%3FprojectId%3D10000&atlOrigin=eyJpIjoiNGZlNDY4Y2YxMGFhNDRhMTgyNTUzYzMzNWQwY2M1YWQiLCJwIjoiamlyYS1zb2Z0d2FyZSJ9)

Sử dụng Jira để quản lý Sprint, Task, Bug, và tiến độ dự án.

---

## 💻 7. HƯỚNG DẪN KHỞI CHẠY KHỞI ĐẦU (GETTING STARTED)

```bash
# 1. Clone repository về máy cá nhân
git clone [https://github.com/your-group/swd392-realtime-auction.git](https://github.com/your-group/swd392-realtime-auction.git)

# 2. Di chuyển vào thư mục dự án
cd swd392-realtime-auction