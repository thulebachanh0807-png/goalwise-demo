# GoalWise AI — yofi

Prototype cuộc thi độc lập, lấy cảm hứng từ MoMo. Không phải tính năng chính thức.

## Chạy demo
Tải `index.html` và mở bằng Chrome hoặc Edge. Không cần cài đặt, server, API key hay mạng. Có thể dùng GitHub Pages: Settings → Pages → Deploy from a branch → main / root → Save (cần chủ repo bật).

## Kịch bản trình diễn
1. Lập kế hoạch cùng AI, xác nhận quyền dùng dữ liệu mô phỏng.
2. Xem dòng tiền 3 tháng; tạo mục tiêu laptop 18 triệu, đã có 2 triệu, 8 tháng.
3. Xác nhận ngưỡng chi linh hoạt; tạo đề xuất. Chi tiêu giảm từ 7,8 triệu xuống 6,7 triệu; tiền dành mục tiêu tăng từ 900.000 lên 2 triệu/tháng.
4. Áp dụng kế hoạch và bật quyền theo dõi. Trong Chế độ Demo thêm 200.000 vào mua sắm. Với ngân sách 600.000 và chi trước đó 550.000, cảnh báo vượt 150.000.
5. Sang Tiết kiệm: so sánh danh mục giả định hoặc dữ liệu ngân hàng lưu sẵn; thay đổi kỳ hạn và mô phỏng rút trước hạn.

## Kiến trúc
Ứng dụng HTML/CSS/JavaScript tự chứa. Dữ liệu giao dịch mô phỏng → tổng hợp dòng tiền → tối ưu theo ràng buộc → duyệt kế hoạch → theo dõi và dự báo → lọc kỳ hạn và tính lãi. LocalStorage lưu trạng thái trên thiết bị. `data/evidence.json` là bản trích database nhúng, để team phát triển backend; chỉnh JSON riêng không tự cập nhật HTML.

## Giới hạn
- Không có API MoMo, AWS, LLM hay giao dịch thật. Giải thích sinh từ mẫu quy tắc, không phải mô hình AI trực tuyến.
- Lãi suất lưu từ prototype trước, chưa xác minh lại; lãi không kỳ hạn 0,1% là giả định mô phỏng. Không tuyên bố quan hệ đối tác.
- Benchmark địa lý chỉ để tham chiếu. Dự báo giữ phần ngân sách chưa chi; không phải dự báo hành vi theo thời gian. Điều chuyển cần xác nhận và chỉ trong phần chi linh hoạt còn khả năng giảm.
- MVP một mục tiêu, không có hệ thống tài khoản hoặc dữ liệu server, chưa kiểm thử trên trình duyệt thật. Để tích hợp production cần xác nhận API, dữ liệu, quyền truy cập, bảo mật và compliance.

## Kiểm thử tự động trong JS isolate
- entry: PASS
- consent: PASS
- snapshot: PASS
- goal: PASS
- context: PASS
- expense: PASS
- capacity: PASS
- required: PASS
- shortfall: PASS
- optimized: PASS
- shopping: PASS
- protected: PASS
- plan: PASS
- infeasible: PASS
- approved: PASS
- alert: PASS
- bank: PASS
- withdraw: PASS
- minDeposit: PASS
- term: PASS
- demo: PASS

Kiểm thử sử dụng DOM giả lập và bộ nhớ giả lập; không thay cho browser E2E hoặc kiểm thử accessibility.
