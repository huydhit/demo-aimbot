# Nghiên cứu Phân tích Toán học không gian & Phát hiện Aimbot

> **Dự án Nghiên cứu & Giáo dục về Bảo mật Trò chơi & Phân tích Chống gian lận hành vi**

## ⚠️ Tuyên bố miễn trừ trách nhiệm về Giáo dục & Đạo đức

Dự án này được tạo ra hoàn toàn phục vụ **mục đích giáo dục, nghiên cứu an ninh mạng và phát triển giải pháp chống gian lận (anti-cheat)**.
- Dự án **KHÔNG** chứa mã khai thác (exploits), mã chèn bộ nhớ (memory injection) cho các trò chơi thương mại, hay cơ chế vượt qua các hệ thống chống gian lận hiện đại (như Vanguard, EAC, BattlEye).
- Mọi mô phỏng và kiểm thử đều được thực hiện trong môi trường sandbox cô lập sử dụng dữ liệu tổng hợp/giả lập (synthetic/mock data).
- Tác giả không cổ suyếu, khuyến khích hay hỗ trợ việc gian lận trong trò chơi dưới bất kỳ hình thức nào.

---

## 📌 Tổng quan Dự án

Mục tiêu của kho lưu trữ này là phân tích và nghiên cứu cách thức hoạt động toán học của các thuật toán hỗ trợ ngắm bắn/aimbot nhằm phát triển **các heuristic phát hiện hành vi bất thường**. Bằng cách thấu hiểu các phép tính véc-tơ không gian và các chuyển động giật tâm (snap movements), chúng ta có thể thiết kế các thuật toán phát hiện tốt hơn ở phía máy chủ (server-side) hoặc máy khách (client-side) để giảm thiểu nạn gian lận.

### Lĩnh vực trọng tâm:
- **Toán học Không gian:** Phép biến đổi ma trận Thế giới sang Màn hình (World-to-Screen - W2S) & tính toán quỹ đạo góc.
- **Phân tích Quỹ đạo:** Phát hiện gia tốc phi nhân loại, thao tác giật tâm tức thời và chuyển động chuột không có độ rung tự nhiên (zero-jitter).
- **Heuristics hành vi:** Xác định các điểm bất thường về mặt thống kê giữa đầu vào của con người so với đầu vào nhân tạo (synthetic input).

---

## 🏗️ Kiến trúc Dự án
