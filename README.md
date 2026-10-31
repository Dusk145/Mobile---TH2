# Student Study Schedule Management & Booking (Android, Kotlin, SQLite)

Ứng dụng quản lý và đặt lịch học cho sinh viên viết bằng ngôn ngữ **Kotlin**, sử dụng cơ sở dữ liệu cục bộ **SQLite**, hỗ trợ thông báo nhắc lịch học qua `Notification` & `AlarmManager`.

---

## 👥 Phân công nhiệm vụ

| TV | Vai trò | File phụ trách | Tên sinh viên | Mã sinh viên |
|:--:|:--------|:---------------|:--------------|:------------:|
| **1 (Leader)** | DB, Auth, Git | `Models.kt`, `Db.kt`, `Session.kt`, `LoginActivity.kt`, `build.gradle` | Đoàn Hoàng Nam | B23DCCE068 |
| **2** | Chức năng Admin | `Ui.kt` (CrudActivity), `AdminActivity.kt`, `StudentActivity.kt`, `SubjectActivity.kt` | Lưu Khánh Toàn | B23DCVT418 |
| **3** | Chức năng Student | `ScheduleActivity.kt`, `CalendarActivity.kt`, `Notifier.kt`, `StudentHomeActivity.kt` | Đỗ Ngọc Ngai | B23DCCE071 |

---

## 🚀 Hướng dẫn cài đặt và chạy ứng dụng

### 1. Yêu cầu môi trường
* **Android Studio:** Phiên bản Koala (2024.1+) hoặc mới hơn.
* **JDK:** Java 17 trở lên.
* **Thiết bị chạy:** 
  * Thiết bị thật hoặc Máy ảo Android (Emulator) chạy hệ điều hành **Android 8.0 (API 26)** trở lên.
  * *(Khuyến nghị Android 13 / API 33+ để trải nghiệm tính năng cấp quyền thông báo đẩy).*

### 2. Các bước chạy dự án
1. **Mở dự án:**
   * Mở Android Studio, chọn **File > Open** (hoặc chọn Open từ màn hình bắt đầu).
   * Điều hướng và chọn thư mục dự án `thuchanh`.
2. **Đồng bộ Gradle (Sync Gradle):**
   * Đợi Android Studio tự động tải các dependencies.
   * Nếu thấy thanh thông báo xuất hiện, nhấn **Sync Now** (hoặc bấm biểu tượng hình con voi: *Sync Project with Gradle Files*).
3. **Khởi chạy ứng dụng:**
   * Khởi động máy ảo Android (Emulator) hoặc cắm điện thoại Android (đã bật chế độ *USB Debugging*).
   * Nhấn nút **Run** (biểu tượng tam giác xanh ▶ trên thanh công cụ) hoặc bấm tổ hợp phím tắt **`Shift + F10`**.

### 3. Tài khoản đăng nhập mẫu
Dữ liệu mẫu đã được nạp sẵn vào cơ sở dữ liệu `study.db`:

1. **Tài khoản Admin:**
   * **Username:** `admin`
   * **Password:** `admin123`
   * *Chức năng:* Quản lý danh sách sinh viên, quản lý môn học, phân quyền tài khoản.

2. **Tài khoản Sinh viên:**
   * **Username:** `SV001`
   * **Password:** `123456`
   * *Chức năng:* Màn hình chính xem lịch học sắp tới, Đặt lịch học / Hủy lịch / Đổi trạng thái, Xem lịch theo Ngày - Tuần - Tháng, Nhận thông báo hẹn giờ nhắc học trước 15 phút.

> [!NOTE]
> Khi đăng nhập lần đầu bằng tài khoản sinh viên trên Android 13+, vui lòng chọn **Allow (Cho phép)** khi ứng dụng yêu cầu cấp quyền thông báo (`POST_NOTIFICATIONS`) để tính năng báo thức và nhắc giờ học hoạt động chính xác.

---

## 🌿 Git Flow
* **Nhánh chính:** `main` (bản phát hành ổn định) <- `develop` (nhánh phát triển chung).
* **Nhánh tính năng:** `feature/db-auth`, `feature/admin`, `feature/student`.
* **Quy ước:** Tạo commit nhỏ, tạo PR vào `develop` để Leader review và merge. Tiền tố commit: `feat:`, `fix:`, `docs:`.
