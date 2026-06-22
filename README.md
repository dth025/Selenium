## 1. Môi trường và Công cụ phát triển
* **Ngôn ngữ lập trình:** Python 3.14.6
* **Thư viện sử dụng:** Selenium WebDriver 4.45.0
* **Trình duyệt thử nghiệm:** Google Chrome (kết hợp ChromeDriver tự động quản lý bởi Selenium 4).
* **Đối tượng kiểm thử:** Xây dựng các ca kiểm thử tự động cho hệ thống Website thương mại điện tử mẫu `https://www.saucedemo.com/`.

---

## 2. Danh sách các Kịch bản kiểm thử (03 Test Cases)

| STT | Tên Test Case | Các bước thực hiện (Steps) | Kết quả mong đợi (Expected Result) | Trạng thái (Status) |
| :--- | :--- | :--- | :--- | :--- |
| **01** | Kiểm thử Đăng nhập (Login Test) | 1. Điều hướng đến trang `saucedemo.com`.<br>2. Định vị ô tài khoản và mật khẩu bằng thuộc tính `ID`.<br>3. Nhập tài khoản `standard_user` và mật khẩu `secret_sauce`.<br>4. Nhấn nút "Login". | Hệ thống đăng nhập thành công, chuyển hướng người dùng về trang danh sách sản phẩm (`inventory.html`). | **Passed** |
| **02** | Thêm vào giỏ hàng (Add to Cart) | 1. Định vị nút "Add to cart" của sản phẩm đầu tiên (Sauce Labs Backpack) bằng `ID`.<br>2. Click chọn nút thêm vào giỏ hàng.<br>3. Kiểm tra số lượng trên icon giỏ hàng. | Icon giỏ hàng trên Header cập nhật số lượng tăng lên 1, khẳng định sản phẩm đã nằm trong giỏ. | **Passed** |
| **03** | Kiểm thử Đăng xuất (Logout Test) | 1. Click vào nút Menu bên góc trái để mở thanh điều hướng.<br>2. Định vị và click vào nút "Logout". | Hệ thống đăng xuất thành công, xóa phiên làm việc và chuyển hướng an toàn về lại trang đăng nhập ban đầu. | **Passed** |

---

## 3. Hình ảnh minh họa kết quả thực hiện

* **Đoạn mã nguồn viết mã kịch bản Selenium trong IDLE Python:**
    *Mô tả: Hình ảnh cấu trúc code thiết lập WebDriver, xử lý kiểm tra các phần tử Element bằng ID/Class Name.*
    ![Mã nguồn Selenium](images/04_selenium_code.png)

* **Quá trình trình duyệt tự động thực hiện thao tác:**
    *Mô tả: Trình duyệt Google Chrome được điều khiển tự động bởi Selenium thực hiện các hành động trên trang giao diện web.*
    ![Trình duyệt chạy tự động](images/05_selenium_browser.png)

* **Log kết quả chạy thành công hiển thị trên IDLE Shell:**
    *Mô tả: Cửa sổ thông báo đầu ra xác nhận toàn bộ 3 Test Cases đều vượt qua bài kiểm tra (Assertion passed) không lỗi.*
    ![Kết quả Console](images/06_selenium_console.png)

---

## 4. Kết luận bài tập
* Kịch bản kiểm thử tự động UI hoạt động chính xác theo đúng quy trình logic của các Use Case hệ thống.
* Việc áp dụng các câu lệnh khẳng định `assert` giúp tự động hóa khâu kiểm tra kết quả mà không cần con người nhìn và đối chiếu thủ công, tối ưu hóa quá trình kiểm thử hồi quy (Regression Testing).
