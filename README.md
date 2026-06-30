# 2048 AI Solver 🤖🎮

Một dự án trò chơi 2048 tích hợp Trí tuệ nhân tạo (AI), được phát triển bằng ngôn ngữ Python và thư viện Pygame. Dự án này minh họa cách áp dụng các thuật toán tìm kiếm đối kháng kinh điển để giúp máy tính tự động đưa ra các quyết định tối ưu và giành điểm số cao trong trò chơi 2048.

## 🌟 Tính năng nổi bật

- **Engine Game Hoàn Chỉnh:** Giả lập chính xác logic của trò chơi 2048 gốc (di chuyển, gộp số, sinh số ngẫu nhiên 2 và 4).
- **Giao Diện Đồ Họa (GUI) Tùy Chỉnh:** Xây dựng bằng Pygame với thiết kế bo góc, bảng màu chuẩn nguyên bản, hỗ trợ thay đổi kích thước cửa sổ linh hoạt (Resizable).
- **3 Thuật Toán AI Cốt Lõi:**
  - `Minimax`: Thuật toán đối kháng cơ bản, giả định máy tính (người thả số) luôn chọn vị trí tệ nhất cho người chơi.
  - `Alpha-Beta Pruning`: Phiên bản tối ưu của Minimax, sử dụng kỹ thuật cắt tỉa nhánh để tăng tốc độ tính toán mà không làm thay đổi kết quả.
  - `Expectimax`: Thuật toán phù hợp nhất với bản chất ngẫu nhiên của 2048, dựa trên tính toán xác suất kỳ vọng (90% sinh số 2, 10% sinh số 4) để tối ưu hóa quyết định.
- **Bảng Theo Dõi Trạng Thái (AI Log Panel):** Hiển thị trực tiếp (Real-time) số lượng Node (trạng thái bàn cờ) mà AI đã duyệt, điểm số kỳ vọng của từng nhánh di chuyển (Left, Right, Up, Down) và nước đi được chọn.
- **Điều Khiển Tốc Độ:** Cho phép tùy chỉnh tốc độ đánh của AI (100ms, 300ms, 500ms, 1000ms) để tiện lợi cho việc quan sát và báo cáo đồ án.

## 🧠 Kiến trúc Hàm Heuristic (Đánh giá thế cờ)

AI không thể tự hiểu số nào lớn, số nào nhỏ. Để AI chơi giỏi, dự án sử dụng một **Ma trận trọng số (Weight Matrix)** kết hợp với **Điểm thưởng ô trống (Empty Cell Bonus)**:

1. **Ma trận trọng số:** Khuyến khích AI dồn các con số lớn nhất vào góc trên cùng bên trái và sắp xếp theo hình zíc-zắc giảm dần.
2. **Điểm thưởng sinh tồn:** Mỗi ô trống trên bàn cờ được cộng 10.000 điểm. AI sẽ luôn ưu tiên các nước đi giải phóng mặt bằng để tránh việc bàn cờ bị lấp đầy (Game Over).

## ⚙️ Hướng dẫn cài đặt và chạy dự án

### 1. Yêu cầu hệ thống
- Máy tính cài đặt sẵn Python (phiên bản 3.x).
- Thư viện `pygame`.

### 2. Cài đặt
Mở terminal/command prompt và chạy lệnh sau để cài đặt thư viện cần thiết:
    
    pip install pygame

### 3. Chạy trò chơi
Di chuyển vào thư mục chứa dự án và thực thi file chính:
    
    python main.py

## 🎮 Cách sử dụng

1. Khi giao diện mở lên, sử dụng khu vực Menu bên phải để tương tác.
2. Nhấn chọn một trong 3 thuật toán: **Minimax**, **Alpha-Beta**, hoặc **Expectimax** để AI bắt đầu chơi.
3. Nhấn **Speed** để luân phiên thay đổi thời gian nghỉ giữa các nước đi của AI.
4. Nhấn **Details: ON/OFF** để bật/tắt bảng theo dõi log chi tiết thuật toán.
5. Nhấn **Reset / Stop** để dừng quá trình AI đang chạy và tạo ván mới.

## 👨‍💻 Tác giả
- **Sinh viên thực hiện:** Võ Cao Quốc Khánh
- **MSSV:** 24110252
