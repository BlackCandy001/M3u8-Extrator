# Stream Downloader Companion

**Stream Downloader Companion** là một tiện ích mở rộng (extension) cho trình duyệt (Chrome, Edge, Firefox) giúp tự động phát hiện và thu thập các liên kết truyền tải video (HLS/m3u8, DASH/mpd, YouTube) từ các trang web và gửi chúng trực tiếp đến ứng dụng desktop **Stream Downloader**.

## ✨ Tính năng chính

- 🔍 **Tự động phát hiện**: Tự động tìm kiếm các liên kết `.m3u8`, `.mpd`, và video YouTube thông qua network requests, thẻ video, và nội dung script.
- 📺 **Hỗ trợ YouTube**: Tự động nhận diện video YouTube, hiển thị thumbnail chất lượng cao ngay trong sidebar.
- 📱 **Sidebar tiện lợi**: Giao diện sidebar giúp quản lý danh sách các luồng đã phát hiện mà không làm gián đoạn trải nghiệm duyệt web.
- ⚡ **Thao tác nhanh**:
  - **Send All**: Gửi tất cả các stream đã phát hiện đến ứng dụng desktop chỉ với một click.
  - **Clear All**: Xóa nhanh danh sách để bắt đầu phiên làm việc mới.
- 🔔 **Thông báo & Tự động**:
  - **Auto-send**: Tùy chọn tự động gửi liên kết đến ứng dụng desktop ngay khi phát hiện.
  - **Real-time Notifications**: Nhận thông báo (tùy chỉnh) khi tìm thấy stream mới.
- 🌐 **Hỗ trợ SPA**: Hoạt động mượt mà trên các trang web Single Page Application (như YouTube, Facebook) nhờ cơ chế theo dõi thay đổi route.
- 🛠️ **Tùy chỉnh máy chủ**: Linh hoạt thay đổi địa chỉ server của ứng dụng desktop và kiểm tra kết nối thời gian thực.

## 🚀 Cài đặt

### Cho trình duyệt dựa trên Chromium (Chrome, Edge, Brave...)

1. Tải mã nguồn của extension về máy.
2. Truy cập `chrome://extensions/`.
3. Bật **Developer mode** (Chế độ nhà phát triển) ở góc trên bên phải.
4. Chọn **Load unpacked** (Tải tiện ích đã giải nén) và trỏ đến thư mục chứa dự án này.

### Cho Firefox

1. Truy cập `about:debugging#/runtime/this-firefox`.
2. Chọn **Load Temporary Add-on...** (Tải tiện ích tạm thời).
3. Chọn file `manifest.json` trong thư mục dự án.

## 📖 Hướng dẫn sử dụng

1. **Mở Sidebar**: Click vào biểu tượng extension. Trên Firefox, sidebar sẽ tự động mở nếu được cấu hình.
2. **Duyệt Web**: Truy cập các trang chứa video. Số lượng stream sẽ hiển thị ngay trên icon extension.
3. **Quản lý Stream**:
   - **Tìm kiếm & Lọc**: Lọc theo tiêu đề, URL hoặc định dạng (HLS, DASH, YouTube).
   - **Gửi/Sao chép**: Click **Send** để gửi đến desktop app, **Copy** để lưu URL, hoặc **Mở** để xem trực tiếp.
   - **Thao tác hàng loạt**: Sử dụng **Send All** hoặc **Clear All** ở cuối Sidebar.
4. **Cấu hình**:
   - Click icon ⚙️ để mở phần cài đặt.
   - Nhập Server URL (mặc định: `127.0.0.1:34567`).
   - Bật/tắt **Auto-send** hoặc **Notifications**.
   - Kiểm tra trạng thái kết nối qua chấm đèn (Xanh: OK, Đỏ: Mất kết nối).

## 📂 Cấu trúc dự án

- `icons/`: Chứa các biểu tượng của extension.
- `src/background/`: Logic xử lý ngầm, quản lý dữ liệu và giao tiếp server.
- `src/content/`: Script detect link từ network, DOM và injected script.
- `src/sidebar/`: Giao diện người dùng hiện đại và logic điều khiển.
- `manifest.json`: Cấu hình quyền hạn và thành phần extension.

---

Phát triển bởi **Stream Kẹo Đen**. Dự án này hỗ trợ tốt nhất cho hệ sinh thái [N_m3u8DL-RE](https://github.com/nilaoda/N_m3u8DL-RE).
