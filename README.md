# -HCM-KS26-CNTT1-_-Thi-t-k-giao-di-n-Web-_Session01_R-so-t-prompt-C.R.A.F.T-v-b-n-nh-p-c-a-AI

Bước 1: Rà soát phát hiện lỗi


1. Đánh giá khung Prompt C.R.A.F.T (P1, P2, P3)


Prompt	Thành phần thiếu hoặc yếu	Chi tiết lỗi
P1	Thiếu Context, Role, Format, Tone; Action quá chung chung	Chỉ nêu hành động viết thông báo lỗi cho app đặt đồ ăn. Không xác định ngữ cảnh lỗi cụ thể (quán đóng cửa), vai trò người viết, giới hạn 60 ký tự và giọng điệu thân thiện.
P2	Yếu ở Context và Format	Context thiếu mục đích hành động (đặt món và thanh toán). Format chỉ ghi "Ngắn gọn" thay vì quy định con số cụ thể (≤ 20 ký tự).
P3	Thiếu Role; thiếu dữ liệu đầu vào ở Context	Không định danh vai trò (UX Writer). Context nêu mốc ưu đãi 100.000đ nhưng thiếu giá trị tiền món hiện tại (64.000đ) nên AI tự suy diễn và tính sai.


2. Đánh giá 3 bản nháp của AI (D1, D2, D3)


Bản nháp	Loại lỗi mắc phải	Phân tích chi tiết
D1 (Nhắc ưu đãi)	Sai lệch toán học & Tràn ký tự	Tính sai số tiền món cần mua thêm là 26.000đ (đúng phải là 100.000đ - 64.000đ = 36.000đ). Ngoài ra, câu dài 64 ký tự, vượt quy định tối đa 60 ký tự.
D2 (Nút CTA)	Tràn số lượng ký tự thiết kế	Chuỗi "Xác nhận đặt món và thanh toán 80.000đ ngay" dài 43 ký tự, vượt 23 ký tự so với giới hạn tối đa 20 ký tự của nút bấm.
D3 (Báo quán đóng cửa)	Vi phạm Usability Heuristics (Giúp người dùng nhận biết, chẩn đoán và khắc phục lỗi)	Đổ lỗi người dùng ("vì bạn đặt quá muộn"), dùng mã lỗi kỹ thuật vô nghĩa ("Lỗi 503"), và thiếu lối ra/giải pháp (không gợi ý hướng xử lý tiếp theo).


Bước 2: Chuẩn hóa Prompt và Viết lại 3 nội dung


1. Chuẩn hóa P1 theo cấu trúc C.R.A.F.T hoàn chỉnh

• Context (Bối cảnh): Khách hàng đang ở màn hình Giỏ hàng trên ứng dụng ShopeeFood nhưng quán ăn vừa ngừng nhận đơn/đóng cửa.
• Role (Vai trò): Bạn là một UX Copywriter chuyên nghiệp cho ứng dụng giao đồ ăn.
• Action (Hành động): Viết một câu thông báo quán đã đóng cửa và gợi ý khách hàng tìm các quán tương tự khác.
• Format (Định dạng): 1 câu duy nhất, độ dài tối đa 60 ký tự (tính cả dấu cách và dấu câu).
• Tone (Giọng điệu): Lịch sự, thân thiện, ngôn ngữ tự nhiên, tuyệt đối không đổ lỗi cho người dùng và không dùng mã lỗi kỹ thuật.

2. Viết lại 3 nội dung đạt chuẩn UI/UX

• Sửa lại D1 (Nhắc ưu đãi):Mua thêm 36.000đ tiền món để giảm 15.000đ phí ship
(Độ dài thực tế: 50 ký tự — đạt chuẩn ≤ 60 ký tự)
• Sửa lại D2 (Nút CTA):Đặt đơn • 80.000đ
(Độ dài thực tế: 17 ký tự — đạt chuẩn ≤ 20 ký tự. Phương án thay thế: "Thanh toán 80.000đ" - 18 ký tự)
• Sửa lại D3 (Thông báo quán đóng cửa):Quán đã đóng cửa. Mời bạn xem các quán tương tự nhé!
(Độ dài thực tế: 52 ký tự — đạt chuẩn ≤ 60 ký tự)
