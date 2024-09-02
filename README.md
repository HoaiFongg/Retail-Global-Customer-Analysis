# 📊 Retail-Global-Customer-Analysis

## 🗂️ Dữ liệu

Dự án **Retail-Global-Customer-Analysis** sử dụng tập dữ liệu với 3 sheet chính, mỗi sheet đại diện cho một tập thông tin quan trọng:

### 1. **Order** 📝
Chứa thông tin chi tiết về các đơn hàng. Các cột dữ liệu bao gồm:
- **Row ID**: Mã định danh cho mỗi dòng dữ liệu.
- **Order ID**: Mã đơn hàng duy nhất.
- **Order Date**: Ngày đặt hàng.
- **Ship Date**: Ngày giao hàng.
- **Ship Mode**: Phương thức giao hàng (Standard, First Class, Second Class, Same Day).
- **Customer ID**: Mã khách hàng duy nhất.
- **Customer Name**: Tên khách hàng.
- **Segment**: Phân khúc khách hàng (Consumer, Corporate, Home Office).
- **Postal Code**: Mã bưu điện khách hàng.
- **City**, **State**, **Country**, **Region**: Thông tin địa lý của khách hàng.
- **Market**: Thị trường địa lý.
- **Product ID**: Mã sản phẩm duy nhất.
- **Category**, **Sub-Category**: Danh mục và phân loại sản phẩm.
- **Product Name**: Tên sản phẩm.
- **Sales**: Doanh thu từ đơn hàng.
- **Quantity**: Số lượng sản phẩm bán.
- **Discount**: Mức giảm giá của đơn hàng.
- **Profit**: Lợi nhuận từ đơn hàng.
- **Shipping Cost**: Chi phí vận chuyển.
- **Order Priority**: Mức độ ưu tiên đơn hàng.

### 2. **Return** 🔄
Chứa thông tin về các đơn hàng bị hoàn trả, bao gồm:
- **Returned**: Trạng thái hoàn trả (Yes/No).
- **Order ID**: Mã đơn hàng bị hoàn trả.
- **Region**: Khu vực địa lý của đơn hàng hoàn trả.

### 3. **People** 👥
Chứa thông tin về người quản lý các khu vực:
- **Person**: Tên người quản lý.
- **Region**: Khu vực do người quản lý phụ trách.

---

## 🔄 Quá trình thực hiện trong Power BI

### 1. ETL (Extract, Transform, Load)

#### 1.1 **Extract**
- Dữ liệu từ các sheet **Order**, **Return**, và **People** trong Excel đã được nhập vào Power BI để chuẩn bị cho các bước phân tích.

#### 1.2 **Transform**
- **Làm sạch dữ liệu**: Sử dụng **Power Query Editor** để:
  - Loại bỏ giá trị **null** và đảm bảo không còn dữ liệu bị thiếu.
  - Định dạng lại các cột ngày tháng để đảm bảo tính nhất quán.
  - Kiểm tra và chuẩn hóa **kiểu dữ liệu** cho các cột: ngày tháng, số liệu (doanh thu, chi phí, lợi nhuận), và định danh.

#### 1.3 **Load**
- **Tạo bảng DateDimension**: Một bảng thời gian đã được tạo thêm để hỗ trợ cho việc phân tích dữ liệu liên quan đến thời gian.

---

## 📈 Tạo Dashboard

Sau khi hoàn tất quá trình ETL, dữ liệu đã sẵn sàng cho các phân tích và trực quan hóa dưới dạng dashboard với 3 phần chính:

### 1. **Revenue and Profits** 💰
Phân tích doanh thu và lợi nhuận:
- **Doanh thu theo khách hàng**: Phân tích doanh thu theo từng **Customer ID** và **Customer Name** để tìm ra khách hàng tiềm năng.
- **Lợi nhuận theo sản phẩm**: Sử dụng **Product ID** và **Product Name** để xác định sản phẩm mang lại lợi nhuận cao nhất.
- **Tổng quan doanh thu & lợi nhuận**: Biểu đồ xu hướng doanh thu và lợi nhuận theo thời gian, thị trường, và phân khúc khách hàng.

### 2. **Analyze Shipping Costs** 🚚
Phân tích chi phí và hiệu quả vận chuyển:
- **Thời gian giao hàng**: Dùng **Order Date** và **Ship Date** để tính toán thời gian vận chuyển, phân tích hiệu quả giao hàng.
- **Chi phí vận chuyển**: So sánh chi phí vận chuyển từ cột **Shipping Cost** với lợi nhuận của từng đơn hàng.
- **Phương thức vận chuyển**: Biểu đồ so sánh các phương thức vận chuyển như **Standard Class**, **First Class**, **Same Day**.

### 3. **Customer Segmentation** 👥
Phân tích phân khúc khách hàng:
- **Phân khúc khách hàng**: Dựa vào **Segment** để đánh giá doanh thu và lợi nhuận từ các nhóm khách hàng khác nhau (Consumer, Corporate, Home Office).
- **Phân phối khách hàng theo khu vực**: Phân tích địa lý dựa trên các cột **Region**, **Country**.
- **Top khách hàng**: Danh sách các khách hàng có đóng góp doanh thu và lợi nhuận cao nhất.
