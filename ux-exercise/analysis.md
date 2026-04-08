# UX exercise — Airline Chatbot NEO

## Sản phẩm: Trợ lý AI tra cứu chuyến bay

## 4 paths

### 1. AI đúng
- User nhập đúng thông tin chuyến bay
- AI trả về đúng mã chuyến, điểm đi, điểm đến, giờ khởi hành và dự kiến hạ cánh
- User có đủ thông tin để ra quyết định ngay, không cần thao tác thêm

### 2. AI không chắc
- User nhập thông tin chưa đủ rõ (ví dụ chỉ nhớ ngày hoặc giờ gần đúng)
- AI đưa ra danh sách chuyến/ngày gần khớp và hỏi user xác nhận
- Sau khi user xác nhận, AI mới kết luận tìm thấy hoặc không tìm thấy chuyến phù hợp

### 3. AI sai
- User đang ở giai đoạn pre-booking (tìm lịch bay)
- AI hiểu nhầm intent và chuyển sang post-booking, yêu cầu mã đặt chỗ
- User bị chặn luồng vì không có mã đặt chỗ dù nhu cầu chỉ là tra cứu thông tin chung

### 4. User mất niềm tin
- Khi AI nhiều lần hiểu sai, user cảm thấy không thể tiếp tục self-service
- Không có lối thoát rõ ràng như kết nối nhân viên hoặc quay lại menu chính
- Hệ thống tạo cảm giác bắt buộc user phải có mã đặt chỗ mới được hỗ trợ

## Path yếu nhất: Path 3 + 4
- Sai intent khiến user rơi vào sai giai đoạn hành trình
- Recovery flow kém: không có cách sửa nhanh hoặc chuyển đúng luồng
- Thiếu fallback và exit rõ ràng khi user mất niềm tin

## Gap marketing vs thực tế
- Marketing: AI hỗ trợ tra cứu chuyến bay nhanh, tiện, chính xác
- Thực tế: AI vẫn nhầm intent giữa pre-booking và post-booking ở các tình huống thiếu ngữ cảnh
- Gap lớn nhất: truyền thông nhấn mạnh trải nghiệm mượt, nhưng chưa thể hiện rõ cách hệ thống xử lý khi AI sai hoặc khi user cần thoát luồng