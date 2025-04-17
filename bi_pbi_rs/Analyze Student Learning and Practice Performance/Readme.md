# Phân tích hiệu suất học tập và thực hành của học viên bằng Power BI

## Tổng quan

Dự án Power BI này nhằm mục đích phân tích dữ liệu hiệu suất của học viên và đưa ra thông tin chi tiết để cải thiện kết quả giáo dục. Bộ dữ liệu bao gồm thông tin như giới tính, chủng tộc/dân tộc, trình độ học vấn của cha mẹ, loại bữa trưa, hoàn thành khóa học chuẩn bị kiểm tra và điểm số môn toán, đọc và viết. README này cung cấp tổng quan về các thông tin chi tiết chính, các biện pháp DAX và các đề xuất trực quan hóa có được từ phân tích.

## Thông tin chi tiết chính và các biện pháp DAX

1. **Hiệu suất chung:**
- Biện pháp DAX: `Hiệu suất chung = AVERAGE('Bảng thống kê'[math_score] + 'Bảng thống kê'[reading_score] + 'Bảng thống kê'[writing_score])`
- Mô tả: Đánh giá hiệu suất học tập chung của học viên trên tất cả các môn học.

2. **Khoảng cách hiệu suất:**
- Đo lường DAX: `Khoảng cách hiệu suất = ABS(AVERAGE('Bảng thống kê'[math_score]) - AVERAGE('Bảng thống kê'[reading_score]))`
- Mô tả: Xác định khoảng cách hiệu suất giữa các môn học khác nhau.

3. **Tác động của việc chuẩn bị kiểm tra:**
- Đo lường DAX: `Tác động của việc chuẩn bị kiểm tra = IF(ISBLANK(AVERAGE('Bảng nghiên cứu tình huống'[test_preparation_course])), "Không có khóa học", "Khóa học đã hoàn thành")`
- Mô tả: Đo lường tác động của việc hoàn thành khóa học chuẩn bị kiểm tra đối với hiệu suất chung.

4. **Chênh lệch hiệu suất theo giới tính:**
- Đo lường DAX: `Chênh lệch hiệu suất theo giới tính = ABS(AVERAGE('Bảng thống kê'[math_score]) - AVERAGE('Bảng thống kê'[reading_score]))`
- Mô tả: Đánh giá xem có sự khác biệt đáng kể nào về hiệu suất giữa các giới tính hay không?

5. **Ảnh hưởng của trình độ học vấn của cha mẹ:**
- Đo lường DAX: `Ảnh hưởng từ trình độ học vấn của cha mẹ = IF(AVERAGE('Bảng nghiên thống kê'[parental_level_of_education]) = "Bằng cử nhân", "Bằng cử nhân", IF(AVERAGE('Bảng thống kê'[parental_level_of_education]) = "Bằng thạc sĩ", "Bằng thạc sĩ", "Khác"))`
- Mô tả: Xác định xem trình độ học vấn của cha mẹ có tương quan với thành tích của học viên hay không?

## Gợi ý trực quan hóa

1. **Hiệu suất chung:**
- Trực quan hóa: Biểu đồ thanh ngang hoặc biểu đồ dấu đầu dòng.

2. **Khoảng cách hiệu suất:**
- Trực quan hóa: Biểu đồ thanh xếp chồng hoặc biểu đồ thác nước.

3. **Tác động đến việc chuẩn bị kiểm tra:**
- Trực quan hóa: Biểu đồ hình tròn hoặc biểu đồ cột xếp chồng.

4. **Chênh lệch hiệu suất theo giới tính:**
- Trực quan hóa: Biểu đồ thanh nhóm hoặc biểu đồ hộp.

5. **Ảnh hưởng của giáo dục phụ huynh:**
- Hình ảnh hóa: Biểu đồ cột nhóm hoặc biểu đồ thanh xếp chồng.

Những gợi ý hình ảnh hóa này nhằm mục đích truyền đạt hiệu quả những hiểu biết có được từ các biện pháp DAX và tạo điều kiện cho việc ra quyết định dựa trên dữ liệu trong bối cảnh giáo dục.

## Sử dụng

1. Nhập tập dữ liệu hiệu suất của học viên vào Power BI.
2. Tạo các biện pháp DAX cho từng hiểu biết chính bằng cách sử dụng các biểu thức được cung cấp.
3. Sử dụng các biện pháp DAX và gợi ý hình ảnh hóa để phân tích và hình ảnh hóa dữ liệu hiệu suất của học viên một cách hiệu quả.