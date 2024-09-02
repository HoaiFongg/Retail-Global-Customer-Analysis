# Retail-Global-Customer-Analysis
## Dữ liệu

Dự án **Retail-Global-Customer-Analysis** sử dụng tập dữ liệu bao gồm 3 sheet chính:

### 1. **Order**
Chứa thông tin chi tiết về các đơn hàng bao gồm:
- **Row ID**: Mã định danh duy nhất cho mỗi dòng dữ liệu.
- **Order ID**: Mã đơn hàng duy nhất.
- **Order Date**: Ngày đặt hàng.
- **Ship Date**: Ngày giao hàng.
- **Ship Mode**: Phương thức giao hàng (ví dụ: Standard Class, First Class, Second Class, Same Day).
- **Customer ID**: Mã khách hàng duy nhất.
- **Customer Name**: Tên khách hàng.
- **Segment**: Phân khúc khách hàng (ví dụ: Consumer, Corporate, Home Office).
- **Postal Code**: Mã bưu điện của khách hàng.
- **City**: Thành phố của khách hàng.
- **State**: Bang của khách hàng.
- **Country**: Quốc gia của khách hàng.
- **Region**: Khu vực địa lý của khách hàng.
- **Market**: Thị trường của khách hàng.
- **Product ID**: Mã sản phẩm duy nhất.
- **Category**: Danh mục sản phẩm (ví dụ: Furniture, Office Supplies, Technology).
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
- **Order ID**: Mã đơn hàng đã bị hoàn trả.
- **Region**: Khu vực địa lý của đơn hàng hoàn trả.

### 3. **People**
Chứa thông tin về người quản lý các khu vực:
- **Person**: Tên người quản lý.
- **Region**: Khu vực địa lý do người đó quản lý.

