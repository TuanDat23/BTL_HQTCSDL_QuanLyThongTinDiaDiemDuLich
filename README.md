# QUẢN LÝ HỆ THỐNG THÔNG TIN ĐỊA ĐIỂM DU LỊCH
- Tác giả: Vi Tuấn Đạt
- MSSV: K215480106088
- Lớp: K57KMT
## Chức Năng Cơ Bản
### 1. Quản lý
1.1.Quản Lý Địa Điểm Du Lịch
- Thêm địa điểm du lịch: Cho phép thêm mới một địa điểm du lịch vào cơ sở dữ liệu
- Sửa thông tin địa điểm du lịch: Cho phép chỉnh sửa thông tin của một địa điểm du lịch đã tồn tại
- Xóa địa điểm du lịch: Cho phép xóa một địa điểm du lịch khỏi cơ sở dữ liệu
- Xem danh sách địa điểm du lịch: Hiển thị danh sách tất cả các địa điểm du lịch

1.2. Quản Lý Khách Sạn 
- Thêm khách sạn: Cho phép thêm mới một khách sạn vào cơ sở dữ liệu
- Sửa thông tin khách sạn: Cho phép chỉnh sửa thông tin của một khách sạn đã tồn tại
- Xóa khách sạn: Cho phép xóa một khách sạn khỏi cơ sở dữ liệu
- Xem danh sách khách sạn: Hiển thị danh sách tất cả các khách sạn

1.3. Quản Lý Nhà Hàng
- Thêm nhà hàng: Cho phép thêm mới một nhà hàng vào cơ sở dữ liệu
- Sửa thông tin nhà hàng: Cho phép chỉnh sửa thông tin của một nhà hàng đã tồn tại
- Xóa nhà hàng: Cho phép xóa một nhà hàng khỏi cơ sở dữ liệu
- Xem danh sách nhà hàng: Hiển thị danh sách tất cả các nhà hàng

1.4. Quản Lý Đánh Giá
- Thêm đánh giá: Cho phép thêm mới một đánh giá từ khách hàng về địa điểm du lịch
- Sửa thông tin đánh giá: Cho phép chỉnh sửa thông tin của một đánh giá đã tồn tại
- Xóa đánh giá: Cho phép xóa một đánh giá khỏi cơ sở dữ liệu
- Xem danh sách đánh giá: Hiển thị danh sách tất cả các đánh giá

1.5. Quản Lý Khách Hàng
- Thêm khách hàng: Cho phép thêm mới một khách hàng vào cơ sở dữ liệu
- Sửa thông tin khách hàng: Cho phép chỉnh sửa thông tin của một khách hàng đã tồn tại
- Xóa khách hàng: Cho phép xóa một khách hàng khỏi cơ sở dữ liệu.
- Xem danh sách khách hàng: Hiển thị danh sách tất cả các khách hàng

### 2. Chức Năng Truy Vấn
- Tìm kiếm địa điểm du lịch theo tên hoặc loại hình du lịch
- Tìm kiếm khách sạn hoặc nhà hàng theo địa điểm du lịch
- Xem chi tiết đánh giá của một địa điểm du lịch cụ thể
- Xem chi tiết thông tin khách hàng
### 3. Chức Năng Nâng Cao
3.1. Trigger
- Cập nhật tổng số sao và số lượng đánh giá: Tự động cập nhật tổng số sao và số lượng đánh giá của một địa điểm du lịch khi có đánh giá mới được thêm vào hoặc khi một đánh giá bị xóa hoặc chỉnh sửa.

3.2. Cursor
- Duyệt qua các địa điểm du lịch: Tạo thủ tục lưu trữ để duyệt qua các địa điểm du lịch và thực hiện các tính toán tổng hợp như số lượng khách sạn hoặc nhà hàng tại mỗi địa điểm.

3.3. Báo Cáo và Thống Kê
- Báo cáo địa điểm du lịch phổ biến: Tạo báo cáo hiển thị các địa điểm du lịch phổ biến dựa trên số lượng đánh giá và điểm số trung bình.
## Thiết kế chương trình trong SQL
### 1. Tạo các bảng
Bảng KhachHang (Phải tạo đầu tiên để các bảng khác tham chiếu tới)
- ID🔑: Khóa chính được sử dụng để xác định mỗi khách hàng một cách duy nhất, tự tăng.
- TenKhachHang: Tên khách hàng.
- Email: Email của khách hàng.
- SoDienThoai: Số điện thoại của khách hàng.

  
