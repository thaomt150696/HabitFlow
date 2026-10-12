# Đưa bản dùng thử lên mạng để cài vào điện thoại

> Dành cho Thảo. Thư mục này là một web app (PWA): để cài vào điện thoại thì **phải đưa lên một địa chỉ https** (không cài được từ file trên máy tính). Tui không đăng lên mạng thay chế; chế tự làm theo một trong các cách dưới đây. Các trang web này có thể đổi giao diện, nếu khác thì làm theo ý tương tự.

## Các file trong thư mục (phải đưa lên đủ, cùng một thư mục)
| File | Làm gì |
|---|---|
| `index.html` | Toàn bộ app |
| `manifest.webmanifest` | Tên, màu, biểu tượng để cài vào màn hình chính |
| `sw.js` | Giúp app mở được khi không có mạng |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | Biểu tượng app (**tạm**, chỉ là dấu tích trong vòng tròn) |
| `fonts/` (không bắt buộc) | Nếu chế muốn đúng font Be Vietnam Pro: tải font từ Google Fonts, đổi tên các file `BeVietnamPro-Regular.woff2` và `BeVietnamPro-SemiBold.woff2`, đặt vào thư mục `fonts/`. Không có thì app dùng font của điện thoại, không lỗi. |

**Không** đưa lên các file khác trong thư mục `Starbit` (tài liệu, wireframe...). Chỉ đưa thư mục `ban-dung-thu`.

## Cách 1 (dễ nhất): Netlify Drop
1. Mở trình duyệt, vào trang kéo-thả của Netlify (tìm "Netlify Drop").
2. Kéo cả thư mục `ban-dung-thu` thả vào ô trên trang.
3. Chờ vài giây, nhận một địa chỉ dạng `https://tên-ngẫu-nhiên.netlify.app`. Gửi địa chỉ này cho người dùng thử.
4. Nếu địa chỉ có hạn, tạo tài khoản miễn phí để giữ lâu hơn (tuỳ trang tại thời điểm chế làm).

## Cách 2: GitHub Pages (miễn phí, địa chỉ ổn định)
1. Tạo tài khoản GitHub, tạo một kho (repository) mới, đặt tên bất kỳ.
2. Tải toàn bộ **nội dung** thư mục `ban-dung-thu` lên kho (nút "Add file" → "Upload files").
3. Vào Settings → Pages, chọn nhánh `main`, thư mục gốc, lưu. Chờ 1–2 phút.
4. Địa chỉ có dạng `https://tên-của-bạn.github.io/tên-kho/`.

## Cách 3: Cloudflare Pages (tải thư mục trực tiếp)
Tạo tài khoản Cloudflare, vào Pages, chọn tải thư mục lên trực tiếp (Direct Upload), chọn thư mục `ban-dung-thu`.

**Lưu ý chung:**
- Ai có địa chỉ đều mở được app. App **không chứa dữ liệu của ai**; dữ liệu của mỗi người nằm trên điện thoại của họ. Vẫn nên chỉ gửi địa chỉ cho người dùng thử.
- Kiểm tra trước khi gửi: mở địa chỉ trên điện thoại của chính chế, cài vào màn hình chính, thêm một thói quen, tắt mạng rồi mở lại: vẫn dùng được.

## Cài vào điện thoại (người dùng thử làm theo)
- **iPhone (dùng Safari, không dùng Chrome):** mở địa chỉ → nút Chia sẻ (hình vuông mũi tên lên) → **"Thêm vào Màn hình chính"** → Thêm. Từ nay **chỉ mở app bằng biểu tượng trên màn hình chính**.
- **Android (Chrome):** mở địa chỉ → nút ⋮ → **"Cài đặt ứng dụng"** (hoặc "Thêm vào màn hình chính").

**Quan trọng:** trên iPhone, app mở từ màn hình chính thường có **vùng lưu dữ liệu riêng** khác với khi mở bằng Safari. Hãy cài vào màn hình chính **trước**, rồi mới bắt đầu dùng, để dữ liệu không bị tách đôi. (Nếu đã dùng ở Safari trước thì dữ liệu đó không tự sang.)

## Khi chế sửa app và muốn người dùng nhận bản mới
1. Sửa file, đổi dòng `const VERSION='hf-test-1'` trong `sw.js` (ví dụ `hf-test-2`).
2. Tải lại các file lên cùng chỗ cũ (thay thế).
3. Người dùng mở app khi có mạng là nhận bản mới (có thể phải tắt hẳn app rồi mở lại một lần).
4. Dữ liệu của họ **không bị mất** khi cập nhật.

## Giới hạn của bản dùng thử (nói với người dùng thử trước)
- **Chưa có nhắc giờ, widget, thông báo.** Hãy đặt báo thức điện thoại cho thói quen cần nhắc.
- **Không đăng nhập, không sao lưu tự động.** Nếu họ xóa dữ liệu trình duyệt, gỡ app, hoặc (trên iPhone) lâu không dùng, dữ liệu có thể mất. Vì vậy cuối mỗi tuần nên **Xuất dữ liệu** (Cài đặt → Xuất dữ liệu).
- Biểu tượng và hình minh họa là tạm.
- Đây là bản **thử để học**, không phải sản phẩm hoàn chỉnh.
