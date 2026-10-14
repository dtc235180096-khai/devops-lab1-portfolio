# devops-lab1-portfolio
Lab 1 — DevOps Course: My First CI/CD Pipeline
Họ tên: Dương Quang Khải   masv:dtc23510096

# BƯỚC 4: So sánh DevOps vs Truyền thống (15 phút)

## 4.1 Bảng So sánh

Dựa trên trải nghiệm lab, dưới đây là bảng so sánh chi tiết giữa quy trình triển khai thủ công truyền thống và quy trình tự động hóa với DevOps (CI/CD Pipeline):

| Tiêu chí | Cách THỦ CÔNG (Traditional) | Cách DEVOPS (CI/CD Pipeline) |
| :--- | :--- | :--- |
| **Làm sao để deploy?** | Mở phần mềm FTP/SSH, upload từng file thủ công, chạy các lệnh build/deploy trực tiếp trên server bằng tay | Push code lên GitHub → pipeline tự chạy |
| **Mất bao lâu?** | Vài phút đến vài giờ (tùy thuộc vào độ phức tạp và khả năng xảy ra lỗi do con người) | ~10 giây |
| **Ai làm deploy?** | Developer hoặc System Administrator (con người thực hiện) | GitHub Actions (máy tự làm) |
| **Có bị sai sót không?** | Dễ sai sót (quên copy file, nhầm môi trường, thiếu lệnh cấu hình) | Không — pipeline nhất quán 100% |
| **Rollback nếu lỗi?** | Phải tìm bản backup cũ, copy đè thủ công lại file lỗi hoặc chạy lại lệnh cài đặt từ đầu, mất nhiều thời gian | `git revert` + `push` → tự động rollback |
| **Làm sao biết deploy thành công?** | Tự F5 trang web, kiểm tra log server thủ công để xem có lỗi hay không | GitHub Actions gửi notification ✅/❌ |

---

## 4.2 Nhận xét & Đánh giá tóm tắt

1. **Tốc độ & Hiệu suất:** Quy trình CI/CD giúp giảm thời gian triển khai từ hàng chục phút xuống còn tính bằng giây (~10 giây).
2. **Độ tin cậy:** Loại bỏ yếu tố sai sót do con người (human error), đảm bảo quy trình chạy đồng nhất trên mọi môi trường.
3. **Khả năng phục hồi:** Cho phép hoàn tác (rollback) sự cố cực kỳ nhanh chóng và an toàn thông qua Git.
