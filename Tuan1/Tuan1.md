---
marp: true
theme: default
paginate: true
style: |
  @import url("https://fonts.googleapis.com/css2?family=Work+Sans:wght@400;600;700;800&display=swap");

  :root {
    font-family: "Work Sans", Arial, sans-serif;
    --main-color: #040014;
    --text-color: #121114;
    --bg-color-alt: #dadada;
    --mark-background: #98d6ff;
  }

  /* --- BACKGROUND GRAPH PAPER --- */
  section {
    background-color: #e3e3f1;
    background-size: 24px 24px;
    background-image:
      linear-gradient(#3f32af18 1px, transparent 1px),
      linear-gradient(to right, #ccc89536 1px, #d8d8e62d 1px);
    color: var(--text-color);
    padding: 36px 52px;
    font-size: 26px;
    line-height: 1.5;
  }

  /* --- TITLES --- */
  h1, h2, h3, h4, h5, h6 {
    color: var(--text-color);
    font-weight: 800;
  }

  h1 {
    font-size: 2.25rem;
    margin-top: 4px;
    margin-bottom: 20px;
    border-bottom: 3px solid var(--main-color);
    padding-bottom: 8px;
  }

  blockquote {
    background: #ffffff;
    border-left: 8px solid var(--main-color);
    margin: 16px 0 0 0;
    padding: 12px 18px;
    border-radius: 0 6px 6px 0;
    font-size: 1.05rem;
    font-weight: 600;
    color: #1e1b4b;
    box-shadow: 2px 2px 0px rgba(0, 0, 0, 0.05);
  }

  mark {
    background-color: var(--mark-background);
    padding: 2px 6px;
    font-weight: 700;
    border-radius: 3px;
  }

  .tag {
    font-size: 0.95rem;
    font-weight: 800;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: #4338ca;
  }

  .grid-3 {
    display: grid !important;
    grid-template-columns: repeat(3, 1fr) !important;
    gap: 18px !important;
  }

  .two-col {
    display: grid !important;
    grid-template-columns: 1.15fr 0.85fr !important;
    gap: 24px !important;
    align-items: center !important;
  }

  .feature-card {
    background-color: #ffffff;
    border: 1px solid #c7c7d9;
    border-radius: 8px;
    padding: 20px 24px;
    box-shadow: 2px 3px 0px rgba(4, 0, 20, 0.08);
    font-size: 1.05rem;
    line-height: 1.6;
  }

  /* CLASS HIỂN THỊ HÌNH ẢNH BO GÓC */
  .img-frame {
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #ffffff;
    border: 1px solid #c7c7d9;
    border-radius: 8px;
    padding: 10px;
    box-shadow: 2px 3px 0px rgba(4, 0, 20, 0.08);
  }

  .img-frame img {
    width: 100%;
    height: 320px;
    object-fit: cover;
    border-radius: 6px;
  }

  .img-caption {
    font-size: 0.85rem;
    font-weight: 700;
    color: #475569;
    margin-top: 8px;
    text-align: center;
  }

  /* --- COVER SLIDE --- */
  .title-slide {
    display: flex !important;
    flex-direction: column !important;
    justify-content: center !important;
    height: 100% !important;
  }

  .title-tag-box {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 14px;
  }

  .badge-num {
    background-color: var(--main-color);
    color: #ffffff;
    width: 30px;
    height: 30px;
    min-width: 30px;
    border-radius: 6px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 800;
    font-size: 0.95rem;
  }

  .title-h1 {
    font-size: 2.85rem !important;
    line-height: 1.2 !important;
    border-bottom: none !important;
    padding-bottom: 0 !important;
    margin-bottom: 12px !important;
  }

  .title-sub {
    font-size: 1.35rem;
    color: #334155;
    font-weight: 600;
    margin-bottom: 28px;
  }

  .title-meta {
    display: flex;
    gap: 32px;
    border-top: 2px solid var(--main-color);
    padding-top: 18px;
    margin-top: 14px;
    font-size: 1.05rem;
    font-weight: 600;
    color: #475569;
  }

  .title-meta span b {
    color: var(--text-color);
  }

  section::after {
    font-size: 0.85em;
    content: attr(data-marpit-pagination) " / " attr(data-marpit-pagination-total);
    color: var(--text-color);
    font-weight: 600;
  }
---

<!-- Slide 0: Bìa -->

<div class="title-slide">
  <div class="title-tag-box">
    <span class="tag">Side Quest • Lịch sử ngành Game</span>
    <span class="badge-num">01</span>
  </div>

  <h1 class="title-h1">Bình minh ngành Game</h1>
  <div class="title-sub">Thập niên 1970: Game đầu tiên, <mark>Pong</mark> & Kỷ nguyên Arcade</div>

  <div class="title-meta">
    <span>Trình bày: <b>Trần Minh Đăng</b></span>
  </div>
</div>

---

<!-- Slide 1: Khởi nguồn & Computer Space -->
<span class="tag">01. Khởi nguồn</span>
<h1>Từ phòng Lab ra thương trường</h1>

<div class="two-col">
  <div class="feature-card" style="border-left: 6px solid #ea580c;">
    <p style="margin: 0 0 10px 0; font-size: 1.15rem;"><b>1971: Computer Space (Arcade đầu tiên)</b></p>
    <p style="margin: 0 0 8px 0;">• Cỗ máy thương mại bỏ xu (coin-op) đầu tiên trên thế giới.</p>
    <p style="margin: 0 0 8px 0;">• Thùng máy vỏ nhựa sợi thủy tinh (fiberglass) uốn lượn phong cách tương lai.</p>
    <p style="margin: 0 0 8px 0;">• <b>Thực tế:</b> Thất bại doanh thu (~1.500 máy).</p>
    <p style="margin: 0; color: #9a3412; font-weight: 600;">👉 Rào cản: Bảng điều khiển quá nhiều nút bấm, khó chơi.</p>
  </div>

  <div class="img-frame">
    <img src="/Users/tranminhdang/Desktop/GameDev/Lihuhu/Marp/Tuan1/Screenshot 2026-10-09 at 00.37.06.png" alt="Máy Pong Arcade nguyên bản" />
    <div class="img-caption">Thùng máy Computer Space (1971)</div>
  </div>
</div>

---
<div class ="two-col">
<div >
    <img src="/Users/tranminhdang/Desktop/GameDev/Lihuhu/Marp/Tuan1/Screenshot 2026-10-09 at 01.17.51.png" alt="Máy Pong Arcade nguyên bản" />
    <div class="img-caption">Máy tính nghiên cứu PDP-1</div>
  </div>

  <div >
    <img src="/Users/tranminhdang/Desktop/GameDev/Lihuhu/Marp/Tuan1/Screenshot 2026-10-09 at 01.23.21.png" alt="Máy Pong Arcade nguyên bản" />
    <div class="img-caption">Game Spacewar (1962)</div>
  </div>
</div>

</div>

---

<!-- Slide 2: Pong & Atari -->
<span class="tag">02. Bước ngoặt</span>
<h1>Pong (1972) — Đơn giản là vua</h1>

<div class="two-col">
  <div class="feature-card" style="border-left: 6px solid #0d828a;">
    <p style="margin: 0 0 10px 0; font-size: 1.15rem;"><b>Triết lý thiết kế tối giản</b></p>
    <p style="margin: 0 0 8px 0;">• <b>Phần cứng:</b> Chạy bằng mạch logic TTL, không có CPU hay code.</p>
    <p style="margin: 0 0 8px 0;">• <b>Điều khiển:</b> Chỉ 1 núm xoay (paddle) đỡ bóng.</p>
    <p style="margin: 0 0 8px 0;">• <b>Onboarding:</b> Hiểu luật trong 3 giây <i>(Easy to learn, hard to master)</i>.</p>
    <p style="margin: 0; color: #0f2d59; font-weight: 600;">🔥 Cột mốc: Thùng thử nghiệm kẹt cứng vì nhét quá nhiều tiền xu.</p>
  </div>

  <div class="img-frame">
   <img src="/Users/tranminhdang/Desktop/GameDev/Lihuhu/Marp/Tuan1/Screenshot 2026-10-09 at 01.15.17.png" alt="Thùng máy Space Invaders Arcade cổ điển" />
    <div class="img-caption">Thùng máy Pong (1972) của Atari</div>
  </div>
</div>

---

<!-- Slide 3: Space Invaders -->
<span class="tag">03. Bùng nổ</span>
<h1>Space Invaders (1978) — Kỷ nguyên vàng</h1>

<div class="two-col">
  <div class="feature-card" style="border-left: 6px solid #4338ca;">
    <p style="margin: 0 0 10px 0; font-size: 1.15rem;"><b>Bước nhảy Vi xử lý (Intel 8080)</b></p>
    <p style="margin: 0 0 8px 0;">• Cơn sốt toàn cầu: Doanh thu hơn 3,8 tỷ USD.</p>
    <p style="margin: 0 0 8px 0;">• <b>Dynamic Difficulty:</b> Bắn bớt quái => CPU nhẹ tải => Quái bay nhanh dần (từ bug thành feature kinh điển).</p>
    <p style="margin: 0; font-weight: 600;">• <b>High Score:</b> Bảng kỷ lục điểm số kích thích ganh đua nhét thêm xu.</p>
  </div>

  <div class="img-frame">
    <img src="https://encrypted-tbn3.gstatic.com/licensed-image?q=tbn:ANd9GcSXJG0lB-Z-LH3fS44XTYmaDQk-81Gh9lFPEkhZfQoeuu3R9axvVv7Q5Vj88KHTOAITcx967n_pXvs9Hck" alt="Space Invaders Arcade Gameplay" />
    <div class="img-caption">Giao diện kinh điển Space Invaders</div>
  </div>
</div>

---

<div class ="two-col">
   <img src="/Users/tranminhdang/Desktop/GameDev/Lihuhu/Marp/Tuan1/Screenshot 2026-10-09 at 01.44.54.png" alt="Thùng máy Space Invaders Arcade cổ điển" />
    <div class="img-caption">Máy tính Apple II</div>
  </div>
</div>

---

<!-- Slide 4: Bài học -->
<span class="tag">04. Đúc kết</span>
<h1>Bài học cho Dev ngày nay</h1>

<div class="feature-card" style="border-left: 6px solid #ea580c; margin-bottom: 16px;">
  <b>1. Core loop gọn + Feedback tức thì (Pong)</b><br>
  Giảm tối đa friction lúc onboarding; âm thanh và va chạm trực quan phải thỏa mãn ngay từ cú chạm đầu.
</div>

<div class="feature-card" style="border-left: 6px solid #0d828a; margin-bottom: 16px;">
  <b>2. Giới hạn phần cứng = Cơ hội thiết kế</b><br>
  Tận dụng đặc tính kỹ thuật để làm chất liệu đẩy nhịp độ thay vì than vãn cấu hình.
</div>

<div class="feature-card" style="border-left: 6px solid #4338ca;">
  <b>3. Động lực điểm số & Lặp lại </b><br>
  Tâm lý "chơi thêm ván nữa để phá kỷ lục" là cội nguồn của bảng xếp hạng (Leaderboard) và Meta loop hiện đại.
</div>

---

<!-- Slide 5: Chuyển giao & Q&A -->
<span class="tag">05. Chuyển giao</span>
<h1>Cơn sốt Arcade & Mầm mống khủng hoảng</h1>

<div class="two-col" style="grid-template-columns: 1fr 1fr !important;">
  <div class="feature-card">
    <p style="margin: 0 0 10px 0;">• Thập niên 70 chứng minh: Game là ngành công nghiệp triệu đô.</p>
    <p style="margin: 0 0 10px 0;">• Chuyển dịch: Từ thùng máy công cộng về phòng khách gia đình (Console).</p>
    <p style="margin: 0; color: #b91c1c; font-weight: 600;">• Mầm mống: Tăng trưởng nóng => Làm game ẩu, thiếu kiểm soát.</p>
  </div>

  <div class="feature-card" style="border-left: 6px solid #ea580c;">
    <p style="font-weight: 700; color: #ea580c; font-size: 1.15rem; margin: 0 0 8px 0;"></p>
    <p style="margin: 0; font-style: italic; line-height: 1.6;">
      "Thị trường sụp đổ ra sao khi niềm tin chạm đáy vào 1983, và Nintendo đã giải cứu ngành game như thế nào?
    </p>
  </div>
</div>

---

<!-- Slide 6: Nguồn -->
<span class="tag">06. Kiểm chứng</span>
<h1>Tài liệu tham khảo độc lập</h1>

<div class="grid-3" style="font-size: 0.95rem; line-height: 1.55;">
  <div class="feature-card">
    <b style="font-size: 1.05rem;">Youtube:</b><br><br>
    <i>ATARI - Kẻ Tiên Phong Vĩ Đại | LỊCH SỬ NGÀNH GAME</i> <br><br>
  </div>

  <div class="feature-card">
    <b style="font-size: 1.05rem;">Chuyên khảo ngành:</b><br><br>
    <i>Replay: The History of Video Games</i> (Tristan Donovan)<br><br>
  </div>

  <div class="feature-card">
    <b style="font-size: 1.05rem;">Bảo tàng Game:</b><br><br>
    <i>The Strong National Museum of Play</i><br><br>
  </div>
</div>