# Retail-Global-Customer-Analysis

## Dữ liệu
Dự án **Retail-Global-Customer-Analysis** sử dụng tập dữ liệu bao gồm 3 sheet chính:

### 1. **Order**
Chứa thông tin chi tiết về các đơn hàng:
- **Row ID**: Mã định danh duy nhất cho mỗi dòng dữ liệu.
- **Order ID**: Mã đơn hàng duy nhất.
- **Order Date**: Ngày đặt hàng.
- **Ship Date**: Ngày giao hàng.
- **Ship Mode**: Phương thức giao hàng (Standard Class, First Class, Second Class, Same Day).
- **Customer ID**: Mã khách hàng duy nhất.
- **Customer Name**: Tên khách hàng.
- **Segment**: Phân khúc khách hàng (Consumer, Corporate, Home Office).
- **Postal Code**: Mã bưu điện của khách hàng.
- **City**: Thành phố của khách hàng.
- **State**: Bang của khách hàng.
- **Country**: Quốc gia của khách hàng.
- **Region**: Khu vực địa lý của khách hàng.
- **Market**: Thị trường của khách hàng.
- **Product ID**: Mã sản phẩm duy nhất.
- **Category**: Danh mục sản phẩm (Furniture, Office Supplies, Technology).
- **Sub-Category**: Danh mục con của sản phẩm.
- **Product Name**: Tên sản phẩm.
- **Sales**: Doanh thu từ đơn hàng.
- **Quantity**: Số lượng sản phẩm đã bán.
- **Discount**: Mức giảm giá áp dụng cho đơn hàng.
- **Profit**: Lợi nhuận từ đơn hàng.
- **Shipping Cost**: Chi phí vận chuyển.
- **Order Priority**: Mức độ ưu tiên của đơn hàng.

### 2. **Return**
Chứa thông tin về các đơn hàng bị hoàn trả:
- **Returned**: Trạng thái hoàn trả (Yes/No).
- **Order ID**: Mã đơn hàng bị hoàn trả.
- **Region**: Khu vực địa lý của đơn hàng hoàn trả.

### 3. **People**
Chứa thông tin về người quản lý các khu vực:
- **Person**: Tên người quản lý.
- **Region**: Khu vực địa lý do người quản lý phụ trách.

## Quá trình thực hiện trong Power BI

### 1. ETL (Extract, Transform, Load)
Quá trình ETL được thực hiện qua các bước sau:

#### 1.1 Extract
- **Extract dữ liệu**: Nhập dữ liệu từ các sheet **Order**, **Return**, và **People** trong file Excel vào Power BI.

#### 1.2 Transform
- **Làm sạch dữ liệu**: Sử dụng **Power Query Editor** để làm sạch dữ liệu:
  - Loại bỏ các giá trị **null** và đảm bảo không còn dữ liệu bị thiếu.
  - Định dạng lại các cột ngày tháng để đảm bảo tính nhất quán.
  - Kiểm tra và xác nhận đúng **kiểu dữ liệu** cho tất cả các cột, ví dụ: cột ngày phải là định dạng ngày tháng, cột doanh thu và chi phí phải là định dạng số.

#### 1.3 Load
- **Tạo bảng bổ sung**: Tạo bảng **DateDimension** để phục vụ cho việc trực quan hóa dữ liệu liên quan đến thời gian trong các phân tích sau này.
