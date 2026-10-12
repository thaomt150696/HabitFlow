# Thử bản dùng thử trên điện thoại của Thảo (khoảng 20 phút)

> Làm **trước khi** gửi cho người khác. Mục tiêu: biết app có cài được, lưu được dữ liệu, mở được khi không có mạng và xuất được tệp hay không. Tui (Claude) **chưa thử các việc này trên điện thoại thật**, nên chế báo lỗi nào gặp, tui sửa.

## Bước 1. Đưa lên mạng (5 phút)
Làm theo `HUONG-DAN-DANG-LEN-MANG.md`. Cách nhanh nhất là Netlify Drop: kéo cả thư mục `ban-dung-thu` vào trang, nhận địa chỉ `https://….netlify.app`. Gửi địa chỉ này sang điện thoại của chế (tin nhắn tự gửi, Zalo, email).

**Kiểm tra trước:** địa chỉ phải bắt đầu bằng **https**. Mở trên máy tính trước, thấy màn "Giữ thói quen bằng những việc nhỏ" là đã lên đúng.

## Bước 2. Cài vào màn hình chính (2 phút)
- **iPhone:** mở địa chỉ bằng **Safari** (không dùng Chrome) → nút Chia sẻ (ô vuông mũi tên lên) → **Thêm vào Màn hình chính** → Thêm.
- **Android:** mở bằng **Chrome** → nút ⋮ → **Cài đặt ứng dụng** (hoặc Thêm vào màn hình chính).
- Sau khi cài, **đóng tab trình duyệt và chỉ mở bằng biểu tượng mới** trên màn hình chính.

**Ghi lại:** biểu tượng có hiện không? Mở lên có **toàn màn hình** (không thấy thanh địa chỉ) không?

## Bước 3. Thử nhanh 10 điểm (10 phút)
Đánh dấu từng dòng: chạy đúng / có lỗi (ghi lỗi gì).

| # | Làm | Kỳ vọng |
|---|---|---|
| 1 | Mở app lần đầu, bấm Bắt đầu, chọn "Đọc sách", Tạo thói quen | Vào màn Hôm nay có "Đọc sách" |
| 2 | Chạm ⊕, tạo "Tập thể dục" với 2 việc nhỏ, lặp lại "Chọn các thứ" | Thẻ hiện "Kế tiếp: …" |
| 3 | Chạm ô tick cạnh "Kế tiếp" | Vòng đổi thành 1/2; máy rung nhẹ (Android) |
| 4 | Chạm vào tên thói quen → xem chuỗi, chạm "Sửa" → thêm 1 việc nhỏ → Xong | Không lỗi |
| 5 | Chạm "Hôm nay mình mệt" → chọn Nghỉ một thói quen → OK → bấm Hoàn tác | Thẻ nghỉ rồi trở lại |
| 6 | Mở Tuần và Tháng | Hiện, không lỗi (còn ít dữ liệu nên đơn giản) |
| 7 | **Đóng hẳn app** (vuốt bỏ khỏi danh sách ứng dụng), mở lại | **Dữ liệu còn nguyên** |
| 8 | Bật **chế độ máy bay**, đóng hẳn app, mở lại | **Vẫn mở được** và còn dữ liệu |
| 9 | Cài đặt → "Xuất dữ liệu…" → Sao chép → dán vào ghi chú | Có nội dung CSV; thử cả "Chia sẻ tệp" |
| 10 | Cài đặt → Chế độ → Tối | Đổi màu đúng, chữ đọc được |

**Hai điểm quan trọng nhất:** #7 và #8. Nếu một trong hai lỗi thì chưa gửi cho ai được.

## Bước 4. Xem Tuần, Tháng khi có dữ liệu (không cần đợi 2 tuần)
Cài đặt → **Hướng dẫn và thông tin** → **Nạp dữ liệu mẫu để xem thử** (có hộp xác nhận). App sẽ có 40 ngày dữ liệu mẫu để xem Tuần, Tháng, lịch tháng, chuỗi. **Việc này thay toàn bộ dữ liệu**, nên chỉ làm ở bản thử của chế. Xong thì chọn **Xóa toàn bộ dữ liệu** để về trạng thái trống trước khi dùng thật.

**Xem màn "Chào mừng quay lại":** dùng 2 ngày liên tiếp không mở rồi mở lại, hoặc nhờ tui chỉ cách giả ngày trên máy tính.

## Bước 5. Thử cập nhật (3 phút, nên làm một lần)
Sửa một chữ nhỏ trong `index.html`, đổi `VERSION` trong `sw.js` (ví dụ `hf-test-2`), tải lên lại, rồi mở app trên điện thoại (có mạng). Có thể phải tắt hẳn rồi mở lại một lần để thấy chữ mới. **Dữ liệu cũ phải còn nguyên.**

## Khi gặp lỗi, ghi lại giúp tui
1. Điện thoại và hệ điều hành (ví dụ iPhone 13, iOS 17.4; Samsung A54, Android 14).
2. Mở bằng Safari/Chrome hay biểu tượng màn hình chính.
3. Bước nào (số ở bảng trên) và chuyện gì xảy ra.
4. Ảnh chụp màn hình nếu được.

## Nếu không cài được hoặc dữ liệu mất
| Dấu hiệu | Thường do | Thử |
|---|---|---|
| iPhone không thấy "Thêm vào Màn hình chính" | Đang dùng Chrome, hoặc địa chỉ không phải https | Dùng Safari; kiểm tra https |
| Android không thấy "Cài đặt ứng dụng" | Chưa tải đủ file, hoặc không phải https | Kiểm tra đủ file; dùng "Thêm vào màn hình chính" |
| Mở lại thấy trống | Mở nhầm bằng Safari/Chrome thay vì biểu tượng; hoặc dữ liệu đã nhập ở chỗ khác | Mở bằng biểu tượng; xem Cài đặt → "Dữ liệu của bạn đang ở đâu?" |
| Mất mạng không mở được | Chưa mở app ít nhất một lần khi có mạng sau khi cài | Mở khi có mạng một lần rồi thử lại |
| Chữ không phải Be Vietnam Pro | Bình thường (chưa thêm file font) | Xem mục font trong `HUONG-DAN-DANG-LEN-MANG.md` |

Báo kết quả #1–#10 cho tui (chạy đúng hay lỗi), tui sửa các lỗi trước khi chế gửi cho 6–8 người.
