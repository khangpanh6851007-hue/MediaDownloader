# 🚀 Media Downloader 5.0 (GitHub 2026 Edition)

Trang web tải video và âm thanh đa năng (YouTube, TikTok, Facebook) được thiết kế hiện đại, tối ưu hóa giao diện hoàn hảo cho thiết bị di động và các trình soạn thảo mã nguồn trực tuyến như **Acode** hoặc **Trebedit**.

---

## 🌟 Tính Năng Nổi Bật

*   **Giao diện 5.0 Hiện đại:** Thiết kế dạng kính mờ (Glassmorphism), hiệu ứng chuyển động mượt mà với tông màu tối sang trọng.
*   **Đồng hồ & Lịch tự động:** Widget hiển thị thời gian thực và ngày/tháng/năm theo giờ Việt Nam được cập nhật từng giây.
*   **Hướng dẫn sử dụng trực quan:** Tích hợp Modal hướng dẫn nhanh giúp người dùng thao tác dễ dàng ngay từ lần đầu truy cập.
*   **Hỗ trợ đa nền tảng:** Tổng hợp các liên kết trích xuất định dạng chất lượng cao cho YouTube, Facebook và TikTok không logo.

---

## 🛠️ Danh Sách Công Cụ Tích Hợp

| Nền tảng | Chức năng | Liên kết dịch vụ |
| :--- | :--- | :--- |
| **YouTube** | Tải MP3 | [Y2mate (Vi4)](https://vww-y2mate.com/vi4/) |
| **YouTube** | Tải MP4 | [SaveMP3](https://vi.savemp3.net/jbdel/youtube-video-to-mp3/) |
| **Facebook** | Tải Video | [FSave](https://fsave.net/vi) |
| **Facebook** | Tải Không Logo | [SnapSave](https://snapsave.vn/facebook) |
| **Facebook** | Tải MP3 | [FDown](https://fdown.vn/) |
| **TikTok** | Tải Không Logo | [SnapTik](https://snaptik.vn/) |
| **TikTok** | Tải dự phòng | [Odex SnapTik](https://odex.vn/tien-ich/tai-video-tiktok/) |
| **TikTok** | Tải Video Tobi | [Tobi](https://tobi.ie/) |

---

## 📱 Hướng Dẫn Cài Đặt Trên Acode / Trebedit

1. Mở ứng dụng **Acode** hoặc **Trebedit** trên điện thoại của bạn.
2. Tạo một tệp mới có tên: `index.html`.
3. Sao chép toàn bộ mã nguồn phía dưới dán vào tệp `index.html`.
4. Lưu tệp lại và chọn **Preview** để xem thành quả!

---

## 💻 Mã Nguồn Hoàn Chỉnh (`index.html`)

```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trình Tải Video & Âm Thanh Đa Năng</title>
    <!-- Font Awesome cho icon -->
    <link rel="stylesheet" href="[https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css)">
    <!-- Google Fonts -->
    <link href="[https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap](https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap)" rel="stylesheet">
    
    <style>
        :root {
            --bg-gradient: linear-gradient(135deg, #0f172a 0%, #1e1b4b 100%);
            --card-bg: rgba(255, 255, 255, 0.05);
            --card-border: rgba(255, 255, 255, 0.1);
            --text-color: #f8fafc;
            --text-muted: #94a3b8;
            --accent-glow: 0 0 20px rgba(99, 102, 241, 0.3);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: var(--bg-gradient);
            color: var(--text-color);
            min-height: 100vh;
            padding: 20px 15px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .container {
            width: 100%;
            max-width: 480px;
        }

        /* Widget Đồng hồ & Lịch */
        .datetime-widget {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            backdrop-filter: blur(12px);
            border-radius: 14px;
            padding: 12px 15px;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }

        .datetime-widget .date-box {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        .datetime-widget .date-box i {
            color: #60a5fa;
        }

        .datetime-widget .clock-box {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.95rem;
            font-weight: 600;
            color: #c084fc;
        }

        .datetime-widget .clock-box i {
            color: #c084fc;
        }

        /* Header Style */
        header {
            text-align: center;
            margin-bottom: 20px;
        }

        header h1 {
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(to right, #60a5fa, #c084fc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 6px;
        }

        header p {
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* Nút Hướng Dẫn Sử Dụng */
        .guide-btn-wrapper {
            margin-bottom: 20px;
            text-align: center;
        }

        .guide-btn {
            background: linear-gradient(135deg, #3b82f6 0%, #6366f1 100%);
            color: white;
            border: none;
            outline: none;
            padding: 12px 20px;
            border-radius: 12px;
            font-weight: 600;
            font-size: 0.9rem;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 4px 12px rgba(99, 102, 241, 0.4);
            transition: all 0.3s ease;
            width: 100%;
            justify-content: center;
        }

        .guide-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(99, 102, 241, 0.6);
        }

        /* Modal Hướng Dẫn */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(5px);
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .modal-content {
            background: #1e1b4b;
            border: 1px solid rgba(255, 255, 255, 0.15);
            width: 100%;
            max-width: 440px;
            border-radius: 16px;
            padding: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
            animation: fadeIn 0.3s ease;
            max-height: 80vh;
            overflow-y: auto;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.95); }
            to { opacity: 1; transform: scale(1); }
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding-bottom: 10px;
        }

        .modal-header h3 {
            font-size: 1.1rem;
            color: #60a5fa;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .close-btn {
            background: transparent;
            border: none;
            color: var(--text-muted);
            font-size: 1.2rem;
            cursor: pointer;
            transition: color 0.2s;
        }

        .close-btn:hover {
            color: #fff;
        }

        .modal-body {
            font-size: 0.9rem;
            color: var(--text-muted);
            line-height: 1.6;
        }

        .modal-body ol {
            padding-left: 20px;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .modal-body li strong {
            color: var(--text-color);
        }

        /* Search / Input Box simulation */
        .search-box {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            backdrop-filter: blur(12px);
            border-radius: 14px;
            padding: 15px;
            margin-bottom: 20px;
            box-shadow: var(--accent-glow);
        }

        .search-box input {
            width: 100%;
            background: transparent;
            border: none;
            outline: none;
            color: var(--text-color);
            font-size: 0.95rem;
        }

        .search-box input::placeholder {
            color: var(--text-muted);
        }

        /* Links Section */
        .section-title {
            font-size: 0.95rem;
            font-weight: 600;
            color: var(--text-muted);
            margin-bottom: 12px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .link-grid {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-bottom: 25px;
        }

        .link-btn {
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            backdrop-filter: blur(10px);
            padding: 14px 18px;
            border-radius: 12px;
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .link-btn:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-2px);
            border-color: rgba(255, 255, 255, 0.25);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
        }

        .link-btn .left-info {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .link-btn i.fa-youtube { color: #ef4444; }
        .link-btn i.fa-facebook { color: #3b82f6; }
        .link-btn i.fa-tiktok { color: #06b6d4; }
        .link-btn i.fa-download { color: #10b981; }

        .link-btn .fa-chevron-right {
            font-size: 0.8rem;
            color: var(--text-muted);
            transition: transform 0.2s;
        }

        .link-btn:hover .fa-chevron-right {
            transform: translateX(3px);
            color: var(--text-color);
        }

        /* Footer */
        footer {
            text-align: center;
            color: var(--text-muted);
            font-size: 0.8rem;
            margin-top: auto;
            padding-top: 15px;
            border-top: 1px solid var(--card-border);
            width: 100%;
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Widget Hiển Thị Đồng Hồ & Lịch Tự Động -->
        <div class="datetime-widget">
            <div class="date-box">
                <i class="fa-regular fa-calendar-days"></i>
                <span id="current-date">--/--/----</span>
            </div>
            <div class="clock-box">
                <i class="fa-regular fa-clock"></i>
                <span id="current-time">--:--:--</span>
            </div>
        </div>

        <!-- Header -->
        <header>
            <h1>Media Downloader 5.0</h1>
            <p>Hỗ trợ tải video & MP3 tốc độ cao</p>
        </header>

        <!-- Nút Hướng Dẫn Sử Dụng -->
        <div class="guide-btn-wrapper">
            <button class="guide-btn" onclick="openModal()">
                <i class="fa-solid fa-circle-question"></i> Hướng Dẫn Sử Dụng Website
            </button>
        </div>

        <!-- Khung nhập link minh họa -->
        <div class="search-box">
            <input type="text" placeholder="Dán link Video YouTube, TikTok, Facebook vào đây..." readonly>
        </div>

        <!-- Danh sách các nút liên kết -->
        <div class="section-title">Danh sách công cụ tải</div>
        
        <div class="link-grid">
            <!-- 1 -->
            <a href="[https://vww-y2mate.com/vi4/](https://vww-y2mate.com/vi4/)" target="_blank" class="link-btn">
                <div class="left-info">
                    <i class="fa-brands fa-youtube fa-lg"></i>
                    <span>YouTube Thành Mp3</span>
                </div>
                <i class="fa-solid fa-chevron-right"></i>
            </a>

            <!-- 2 -->
            <a href="[https://vi.savemp3.net/jbdel/youtube-video-to-mp3/](https://vi.savemp3.net/jbdel/youtube-video-to-mp3/)" target="_blank" class="link-btn">
                <div class="left-info">
                    <i class="fa-brands fa-youtube fa-lg"></i>
                    <span>YouTube Thành Mp4</span>
                </div>
                <i class="fa-solid fa-chevron-right"></i>
            </a>

            <!-- 3 -->
            <a href="[https://fsave.net/vi](https://fsave.net/vi)" target="_blank" class="link-btn">
                <div class="left-info">
                    <i class="fa-brands fa-facebook fa-lg"></i>
                    <span>Tải Video Facebook</span>
                </div>
                <i class="fa-solid fa-chevron-right"></i>
            </a>

            <!-- 4 -->
            <a href="[https://snapsave.vn/facebook](https://snapsave.vn/facebook)" target="_blank" class="link-btn">
                <div class="left-info">
                    <i class="fa-brands fa-facebook fa-lg"></i>
                    <span>Download Facebook Không Logo</span>
                </div>
                <i class="fa-solid fa-chevron-right"></i>
            </a>

            <!-- 5 -->
            <a href="[https://fdown.vn/](https://fdown.vn/)" target="_blank" class="link-btn">
                <div class="left-info">
                    <i class="fa-brands fa-facebook fa-lg"></i>
                    <span>Download Facebook Thành Mp3</span>
                </div>
                <i class="fa-solid fa-chevron-right"></i>
            </a>

            <!-- 6 -->
            <a href="[https://snaptik.vn/](https://snaptik.vn/)" target="_blank" class="link-btn">
                <div class="left-info">
                    <i class="fa-brands fa-tiktok fa-lg"></i>
                    <span>Download TikTok Không Logo</span>
                </div>
                <i class="fa-solid fa-chevron-right"></i>
            </a>

            <!-- 7 -->
            <a href="[https://odex.vn/tien-ich/tai-video-tiktok/](https://odex.vn/tien-ich/tai-video-tiktok/)" target="_blank" class="link-btn">
                <div class="left-info">
                    <i class="fa-brands fa-tiktok fa-lg"></i>
                    <span>SnapTik (TikTok Download)</span>
                </div>
                <i class="fa-solid fa-chevron-right"></i>
            </a>

            <!-- 8 -->
            <a href="[https://tobi.ie/](https://tobi.ie/)" target="_blank" class="link-btn">
                <div class="left-info">
                    <i class="fa-solid fa-download fa-lg"></i>
                    <span>Tải Video TikTok (Tobi)</span>
                </div>
                <i class="fa-solid fa-chevron-right"></i>
            </a>
        </div>

        <!-- Footer -->
        <footer>
            <p>&copy; 2026 - Designed for Acode & Trebedit</p>
        </footer>
    </div>

    <!-- Modal Hướng Dẫn -->
    <div id="guideModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3><i class="fa-solid fa-book-open"></i> Hướng Dẫn Sử Dụng</h3>
                <button class="close-btn" onclick="closeModal()"><i class="fa-solid fa-xmark"></i></button>
            </div>
            <div class="modal-body">
                <ol>
                    <li><strong>Bước 1:</strong> Chọn và sao chép (Copy) đường link video hoặc bài hát cần tải từ ứng dụng gốc (YouTube, TikTok, Facebook).</li>
                    <li><strong>Bước 2:</strong> Chọn đúng nút công cụ tương ứng với nền tảng bạn muốn tải ở danh sách bên dưới (ví dụ: Tải TikTok không logo, YouTube thành MP3...).</li>
                    <li><strong>Bước 3:</strong> Trình duyệt sẽ mở trang web hỗ trợ tương ứng trong tab mới. Tại đó, bạn dán (Paste) link vừa sao chép vào ô trống.</li>
                    <li><strong>Bước 4:</strong> Nhấn nút tải xuống và chờ hệ thống xử lý để lưu file về máy điện thoại của bạn.</li>
                </ol>
            </div>
        </div>
    </div>

    <!-- Script tự động cập nhật Lịch, Đồng hồ và tính năng mở/đóng Modal -->
    <script>
        function updateDateTime() {
            const now = new Date();

            // Định dạng ngày tháng năm
            const options = { weekday: 'long', year: 'numeric', month: '2-digit', day: '2-digit' };
            let dateString = now.toLocaleDateString('vi-VN', options);
            dateString = dateString.charAt(0).toUpperCase() + dateString.slice(1);
            document.getElementById('current-date').innerText = dateString;

            // Định dạng đồng hồ
            const hours = String(now.getHours()).padStart(2, '0');
            const minutes = String(now.getMinutes()).padStart(2, '0');
            const seconds = String(now.getSeconds()).padStart(2, '0');
            
            document.getElementById('current-time').innerText = `${hours}:${minutes}:${seconds}`;
        }

        updateDateTime();
        setInterval(updateDateTime, 1000);

        // Điều khiển Modal Hướng dẫn
        const modal = document.getElementById('guideModal');

        function openModal() {
            modal.style.display = 'flex';
        }

        function closeModal() {
            modal.style.display = 'none';
        }

        // Đóng modal khi bấm ra ngoài vùng nội dung
        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = 'none';
            }
        }
    </script>

</body>
</html>
