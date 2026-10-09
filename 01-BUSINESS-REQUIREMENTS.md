# Tài Liệu Phân Tích Nghiệp Vụ (Business Requirements Document - BRD)
**Dự án:** Hệ thống đặt và giao đồ ăn trực tuyến (Food Delivery System)

---

## 1. Giới thiệu tổng quan
Hệ thống kết nối 3 đối tượng chính: **Khách hàng** (đặt đồ ăn), **Nhà hàng/Đối tác** (quản lý món & đơn), và **Quản trị viên/Admin** (điều hành toàn bộ hệ thống & phân phối đơn hàng cho tài xế).

---

## 2. Các phân hệ và Luồng nghiệp vụ chính

### 2.1. Khách hàng (Customer)
* **Đăng ký / Đăng nhập:** Email/SĐT + OTP, Google OAuth.
* **Tìm kiếm & Duyệt món:** 
  * Tìm kiếm theo tên món, nhà hàng, danh mục.
  * Lọc theo vị trí (bán kính gần nhất), đánh giá, giá tiền, khuyến mãi.
* **Giỏ hàng & Đặt hàng:**
  * Chọn món, tùy chọn topping/ghi chú (ít đường, không hành...).
  * Chọn địa chỉ giao hàng trên bản đồ.
  * Áp dụng Mã giảm giá (Voucher).
* **Thanh toán:**
  * Tiền mặt khi nhận hàng (COD).
  * Ví điện tử / Cổng thanh toán (MoMo, ZaloPay, VNPay, QR Banking).
* **Theo dõi đơn hàng (Order Tracking):**
  * Trạng thái đơn: *Chờ xác nhận -> Đang chế biến -> Đang giao -> Hoàn thành / Hủy*.

### 2.2. Nhà hàng / Đối tác (Merchant)
* **Quản lý Thực đơn (Menu Management):** Tạo/sửa/xóa món, nhóm món, topping, ẩn món khi hết hàng.
* **Quản lý Đơn hàng:** Nhận thông báo đơn mới, chấp nhận/từ chối đơn, cập nhật trạng thái "Đang chế biến" -> "Sẵn sàng giao".
* **Báo cáo doanh thu:** Thống kê doanh số theo ngày/tần/tháng, đối soát chiết khấu.

### 2.3. Admin & Điều phối
* **Quản lý người dùng & Đối tác:** Duyệt nhà hàng mới, khóa/mở tài khoản khách hàng, tài xế.
* **Quản lý Khuyến mãi:** Tạo mã giảm giá toàn hệ thống hoặc theo nhà hàng.
* **Điều phối & Quản lý Đơn hàng:** Theo dõi tất cả đơn hàng real-time, xử lý khiếu nại, hoàn tiền.
* **Thống kê & Analytics:** Tổng doanh thu hệ thống, hoa hồng thu từ nhà hàng, số lượng đơn hoàn thành/hủy.