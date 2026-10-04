---
marp: true
theme: default
paginate: true
style: |
  @import "default";
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
    background-size: 20px 20px;
    background-image:
      linear-gradient(#3f32af18 1px, transparent 1px),
      linear-gradient(to right, #ccc89536 1px, #d8d8e62d 1px);
    color: var(--text-color);
    padding: 35px 50px;
  }

  /* --- TITLES --- */
  h1, h2, h3, h4, h5, h6 {
    color: var(--text-color);
    font-weight: 800;
  }

  h1 {
    font-size: 1.85rem;
    margin-top: 4px;
    margin-bottom: 16px;
    border-bottom: 2px solid var(--main-color);
    padding-bottom: 6px;
  }

  /* --- TEXT & MARP KEYWORDS --- */
  blockquote {
    background: #ffffff;
    border-left: 8px solid var(--main-color);
    margin: 12px 0 0 0;
    padding: 10px 16px;
    border-radius: 0 6px 6px 0;
    font-size: 0.82rem;
    font-weight: 600;
    color: #1e1b4b;
    box-shadow: 2px 2px 0px rgba(0, 0, 0, 0.05);
  }

  mark {
    background-color: var(--mark-background);
    padding: 1px 4px;
    font-weight: 600;
    border-radius: 2px;
  }

  /* --- TAG & CARD LAYOUT --- */
  .tag {
    font-size: 0.75rem;
    font-weight: 800;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: #4338ca;
  }

  .grid-3 {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
  }

  .card {
    background-color: #ffffff;
    border: 1px solid #c7c7d9;
    border-radius: 6px;
    padding: 14px 14px;
    display: flex;
    flex-direction: column;
    box-shadow: 2px 3px 0px rgba(4, 0, 20, 0.08);
  }

  .card-header {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 8px;
    padding-bottom: 6px;
    border-bottom: 1px dashed #c7c7d9;
  }

  .badge-num {
    background-color: var(--main-color);
    color: #ffffff;
    width: 24px;
    height: 24px;
    min-width: 24px;
    border-radius: 4px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 0.8rem;
  }

  .card-title {
    color: var(--text-color);
    font-size: 0.92rem;
    font-weight: 700;
    line-height: 1.25;
  }

  .card-body {
    font-size: 0.8rem;
    line-height: 1.45;
    color: #262626;
  }

  .card-body p {
    margin: 0 0 6px 0;
  }

  /* --- PAGINATION --- */
  section::after {
    font-size: 0.75em;
    content: attr(data-marpit-pagination) " / " attr(data-marpit-pagination-total);
    color: var(--text-color);
  }

  /* --- LỚP BỔ TRỢ ĐỒNG BỘ LAYOUT --- */
  .grid-3-cards {
    display: grid !important;
    grid-template-columns: repeat(3, 1fr) !important;
    gap: 16px !important;
    margin-top: 24px !important;
  }

  .card-box {
    background: #ffffff !important;
    border: 1px solid #c7c7d9 !important;
    border-radius: 8px !important;
    height: 250px !important;
    display: flex !important;
    flex-direction: column !important;
    justify-content: center !important;
    align-items: center !important;
    text-align: center !important;
    box-shadow: 2px 3px 0px rgba(4, 0, 20, 0.08) !important;
    box-sizing: border-box !important;
    padding: 16px !important;
  }

  .circle-icon {
    width: 72px !important;
    height: 72px !important;
    border-radius: 50% !important;
    color: #ffffff !important;
    display: flex !important;
    align-items: center !important;
    justify-content: center !important;
    font-size: 2rem !important;
    margin-bottom: 16px !important;
  }

  .card-label {
    font-size: 1.6rem !important;
    font-weight: 800 !important;
    line-height: 1.2 !important;
    letter-spacing: -0.5px !important;
    margin: 0 !important;
  }

  .two-col {
    display: grid !important;
    grid-template-columns: 1.05fr 1.35fr !important;
    gap: 32px !important;
    align-items: center !important;
    margin-top: 8px !important;
  }
  .three-col {
    display: grid !important;
    grid-template-columns: repeat(3, 1fr) !important;
    gap: 20px !important;
    align-items: stretch !important;
    margin-top: 8px !important;
  }

  .left-lead {
    font-size: 1.25rem;
    font-weight: 600;
    color: #1e293b;
    margin-bottom: 20px;
    line-height: 1.5;
  }

  .left-note-box {
    margin-top: 20px;
    background-color: #ffedd5;
    border-radius: 6px;
    padding: 12px 16px;
    font-size: 0.88rem;
    color: #9a3412;
    font-weight: 600;
    line-height: 1.45;
  }

  .loop-grid {
    display: grid !important;
    grid-template-columns: 1fr auto 1fr !important;
    grid-template-rows: auto auto auto !important;
    gap: 10px !important;
    align-items: center !important;
    justify-items: center !important;
  }

  .node-box {
    background-color: #1e3a5f;
    color: #ffffff;
    font-weight: 700;
    font-size: 0.9rem;
    text-align: center;
    padding: 14px 10px;
    border-radius: 6px;
    width: 100%;
    box-shadow: 2px 3px 0 rgba(4, 0, 20, 0.12);
    box-sizing: border-box;
  }

  .node-orange {
    background-color: #ea580c !important;
  }

  .feature-card {
    background-color: #ffffff;
    border: 1px solid #c7c7d9;
    border-radius: 8px;
    padding: 20px 24px;
    box-shadow: 2px 3px 0px rgba(4, 0, 20, 0.08);
    font-size: 0.95rem;
    line-height: 1.6;
  }

  .feature-card b {
    color: #0f2d59;
  }

---
<!-- Slide 2: 3 Vấn đề chính -->
# Ba vấn đề chính

<div class="grid-3-cards">
  <div class="card-box">
    <div class="card-label" style="color: #ea580c;">Core loop</div>
  </div>
  <div class="card-box">
   <div class="card-label" style="color: #0d828a;">Cái "đã" nhất?</div>   
  </div>
  <div class="card-box">
   <div class="card-label" style="color: #c2410c;">Cái Bực nhất?</div>
  </div>
</div>
  


  ---
  
<!-- Slide 1: Bìa Hit Perfect 3D -->

<h1 style="font-size: 3.8rem; font-weight: 800; color: #ffffff; border-bottom: none; margin: 0; padding: 0; line-height: 1.2;">
  Hit Perfect 3D
</h1>
<p style="font-size: 1.45rem; font-weight: 400; color: #8fa0b5; margin: 24px 0 0 0; padding: 0;">
  Hyper-casual
</p>

---

<!-- Slide 3: Core loop Hit Perfect 3D -->
# Core loop 

<div class="">
  

  <div class="loop-grid">
    <div class="node-box">Nhìn vị trí địch</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">➔</div>
    <div class="node-box">Vuốt để bắn</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬆</div>
     <div style="font-style: italic; color: #64748b; font-size: 0.85rem; font-weight: 600;">lặp lại</div>
   <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬇</div>
    
<div class="node-box node-orange">Mở khóa màn & vũ khí mới</div>
     <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬅</div>
    <div class="node-box">Địch văng đi & chết </div>
   
  </div>
</div>

---

<!-- Slide 4: "Đã" nhất Hit Perfect 3D -->
# Khoảnh khắc "đã" nhất?

<div >
  <div class="feature-card">
    <p style="margin: 0 0 8px 0;">• <b>Âm thanh:</b> Tiếng súng nổ, dao cắm đanh và vang giòn tai đầy uy lực.</p>
    <p style="margin: 0 0 8px 0;">• <b>Thị giác:</b> Kẻ địch đổi biểu cảm tức thì, tái mét mặt và hoảng loạn trước khi ngã.</p>
    <p style="margin: 0;">• <b>Vật lý Ragdoll:</b> Thân thể kẻ địch trúng lực văng bổng tự do, rơi lảo đảo khỏi tòa nhà cực đã mắt.</p>
    <p style="margin: 0;">• <b>Thưởng tức thì:</b> Hiệu ứng pháo giấy nổ ăn mừng khi về đích. Mở khóa vũ khí / Skin hài hước</p>

  </div>
</div>

---

<!-- Slide 5: Bực nhất Hit Perfect 3D -->
# Chỗ nào bắt đầu bực?

<div >
  <div class="feature-card">
    <p style="margin: 0 0 8px 0;">• <b>Điểm bực:</b> Quảng cái bị spam liên tục</p>
    <p style="margin: 0 0 8px 0;">• <b>Vì sao:</b> Game quá dễ; AI kẻ địch di chuyển lặp lại => Không thỏa mãn được người chơi thích tư duy chiến thuật sâu.</p>
    <p style="margin: 0;">• <b>Nếu sửa 1 điều:</b> Giảm/Cắt bỏ quảng cáo xen ngang khi đang chơi. Tập trung nâng cấp AI để nâng tính chiến thuật. Thêm chế độ Time Attack ép nhịp bắn liên tục .</p>
  </div>
</div>

---

<!-- Slide 6: Điểm cốt lõi Hit Perfect 3D -->
# Điểm cốt lõi

<div >
  <div>
    <div class="left-lead">
      Với cơ chế 1-chạm tối giản, Feedback hay Juice chính là linh hồn giữ chân người chơi.
    </div>
  
  </div>
  <div class="feature-card" style="border-left: 6px solid #ea580c;">
    <p style="font-size: 1.15rem; font-weight: 700; color: #0f2d59; margin: 0 0 10px 0;">
      💡 Audio + Ragdoll = Thỏa mãn tức thì
    </p>
    <p style="margin: 0; color: #334155;">
    <b> Điểm yếu của Hyper Casual nói chung:</b>
    luật chơi quá đơn giản, nếu phản hồi âm thanh và hiệu ứng vật lý không đem lại cảm giác sướng tay ngay lập tức, người chơi sẽ xóa game trong 30 giây đầu tiên.
    </p>
  </div>
</div>

---

<!-- Slide 7: Bìa Smash Hit -->


<h1 style="font-size: 3.8rem; font-weight: 800; color: #ffffff; border-bottom: none; margin: 0; padding: 0; line-height: 1.2;">
  Smash Hit
</h1>
<p style="font-size: 1.45rem; font-weight: 400; color: #8fa0b5; margin: 24px 0 0 0; padding: 0;">
  Casual Arcade
</p>

---

<!-- Slide 9: Core loop Smash Hit -->
# Core loop 

<div >
  

  <div class="loop-grid">
    <div class="node-box">Tự động lao về phía trước theo góc nhìn thứ nhất</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">➔</div>
    <div class="node-box">Bắn bi phá kính &pha lê</div>
<div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬆</div>
    <div style="font-style: italic; color: #64748b; font-size: 0.85rem; font-weight: 600;">lặp lại</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬇</div>
<div class="node-box node-orange">Vượt Checkpoint</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬅</div>
    <div class="node-box">Tích combo nhân bi</div>
  </div>
</div>

---

<!-- Slide 10: "Đã" nhất Smash Hit -->
# Khoảnh khắc "đã" nhất?

<div >
 

  <div class="feature-card">
    <p style="margin: 0 0 8px 0;">• <b>Âm thanh:</b> Tiếng kính vỡ vụn "xoảng" cực kỳ trong trẻo, sắc gọn và vang vọng rất thật.</p>
    <p style="margin: 0 0 8px 0;">• <b>Khoảnh khắc:</b> Bắn vỡ tan cánh cửa kính lớn hoặc trục xoay khổng lồ ngay sát trước mắt ở cự ly chỉ vài cm.</p>
    <p style="margin: 0;">• <b>Vật lý 3D:</b> Mảnh kính văng tung tóe theo va đập chân thực, ăn khớp hoàn hảo với nhịp rung bass.</p>
  </div>
</div>

---

<!-- Slide 11: Bực nhất Smash Hit -->
# Chỗ nào bắt đầu bực?

<div >

  <div class="feature-card">
    <p style="margin: 0 0 8px 0;">• <b>Điểm bực:</b> Ở bản miễn phí, khi hết bi người chơi bị trả về tận Checkpoint phòng số 1.</p>
    <p style="margin: 0 0 8px 0;">• <b>Vì sao:</b> Phải mua Premium để lưu Checkpoin. Việc phải bay lại các căn phòng đầu tiên ở tốc độ chậm khi kỹ năng đã thuần thục gây cảm giác lãng phí thời gian và chán nản.</p>
    <p style="margin: 0;">• <b>Nếu sửa 1 điều:</b> Cho phép xem video quảng cáo (Rewarded Ad) để lưu checkpoint tạm thời tại phòng vừa thua.</p>
  </div>
</div>

---

<!-- Slide 12: Điểm cốt lõi Smash Hit -->

# Điểm cốt lõi

<div >
  <div>
    <div class="left-lead">
      Một kiệt tác về mặt Audiovisual Feedback, nhưng bị hạn chế bởi mô hình kinh doanh cũ.
    </div>
    <div class="left-note-box">
      Bài toán giữ chân nằm ở việc cân bằng giữa thử thách sinh tồn và cảm giác thoải mái khi tiến bộ.
    </div>
  </div>

  
  </div>
</div>

---
<!-- Slide 13: Bìa Subway Surfers -->


<h1 style="font-size: 3.8rem; font-weight: 800; color: #ffffff; border-bottom: none; margin: 0; padding: 0; line-height: 1.2;">
  Subway Surfers
</h1>
<p style="font-size: 1.45rem; font-weight: 400; color: #8fa0b5; margin: 24px 0 0 0; padding: 0;">
  Endless Runner
</p>

---

<!-- Slide 15: Core loop Subway Surfers -->
# Core loop 

  <div class="loop-grid">
    <div class="node-box">Chạy né chướng ngại vật</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">➔</div>
    <div class="node-box">Nhặt xu & Power-up</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬆</div>
    <div style="font-style: italic; color: #64748b; font-size: 0.85rem; font-weight: 600;">lặp lại</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬇</div>
    <div class="node-box node-orange">Tốc độ / độ khó tăng dần</div>
    <div style="color: #64748b; font-size: 1.3rem; font-weight: bold;">⬅</div>
    <div class="node-box">Va chạm & Kết thúc</div>
  </div>
</div>

---

<!-- Slide 16: "Đã" nhất Subway Surfers -->
# Khoảnh khắc "đã" nhất?
  <div class="feature-card">
    <p style="margin: 0 0 8px 0;">• <b>Khoảnh khắc:</b> Nhặt Jetpack bay vút lên bầu trời, tự do hút sạch dải xu vàng an toàn.</p>
    <p style="margin: 0 0 8px 0;">• <b>Thị giác</b> Game có nhiều loại skin từ ván trượt đến nhân vật.</p>
    <p style="margin: 0;">• <b>Thoát hiểm:</b> Hiệu ứng quẹt sườn tàu, chui qua khe hẹp trong tích tắc tạo cảm giác thỏa mãn về phản xạ nhanh nhạy.</p>
  </div>
</div>

---

<!-- Slide 17: Bực nhất Subway Surfers -->

# Chỗ nào bắt đầu bực?

<div class=>
  <div class="feature-card">
    <p style="margin: 0 0 8px 0;">• <b>Điểm bực:</b> Va chạm chết oan vào mép nóc toa tàu ngay thời điểm tiếp đất sau cú nhảy cao.</p>
    <p style="margin: 0 0 8px 0;">• <b>Vì sao:</b> Camera 3D từ phía sau che khuất vật cản ngay điểm mù dưới chân.</p>
    <p style="margin: 0;">• <b>Nếu sửa 1 điều:</b> Thêm 1 khoảng IFrame ngay thời điểm vừa chạm đất.</p>
  </div>
</div>

---

<!-- Slide 18: Điểm cốt lõi Subway Surfers -->

# Điểm cốt lõi

<div >
  <div>
    <div class="left-lead">
      Chu kỳ nâng cấp dài hạn biến những lượt chơi lặp lại thành hành trình tích lũy.
    </div>
    <div >
      Game giữ chân tốt khi kết thúc một phiên mà người chơi vẫn còn một mục tiêu đang dang dở.
    </div>
  </div>
  </div>
</div>

---

<!-- Slide 19: Bìa Tổng kết -->

<h1 style="font-size: 3.8rem; font-weight: 800; color: #ffffff; border-bottom: none; margin: 0; padding: 0; line-height: 1.2;">
  Tổng kết & So sánh
</h1>
<p style="font-size: 1.45rem; font-weight: 400; color: #8fa0b5; margin: 24px 0 0 0; padding: 0;">
  Điểm chung & Điểm mạnh / yếu của từng dòng game
</p>

---

<!-- Slide 20: 3 Dòng game ngang chuẩn -->
# Ba dòng game — Ba triết lý thiết kế

<div class="grid-3-cards">
  <div class="card-box">
    <div class="card-label" style="color: #ea580c; font-size: 1.45rem !important;">Hyper-casual</div>
    <div style="color: #64748b; font-size: 0.85rem; font-weight: 600; margin-top: 8px;">Hit Perfect 3D</div>
  </div>

  <div class="card-box">
    <div class="card-label" style="color: #0d828a; font-size: 1.45rem !important;">Casual Arcade</div>
    <div style="color: #64748b; font-size: 0.85rem; font-weight: 600; margin-top: 8px;">Smash Hit</div>
  </div>

  <div class="card-box">
    <div class="card-label" style="color: #c2410c; font-size: 1.45rem !important;">Endless Runner</div>
    <div style="color: #64748b; font-size: 0.85rem; font-weight: 600; margin-top: 8px;">Subway Surfers</div>
  </div>
</div>

---

<!-- Slide 21: Mạnh & Yếu -->
# Ba dòng game — Ba triết lý thiết kế

<div >
  <div>
    <div class="left-lead">
      Mỗi phân khúc giải quyết một nhu cầu tâm lý khác nhau của người chơi trên di động.
    </div>
    <div class="left-note-box">
      Không có thể loại nào hoàn hảo — sự đánh đổi nằm giữa độ dễ tiếp cận và khả năng giữ chân lâu dài.
    </div>
  </div>

--- 
# Mạnh & Yếu của từng dòng game
  <div class ="three-col" style="font-size: 0.85rem; line-height: 1.5; padding: 16px 20px;">
    <p style="margin: 0 0 8px 0;">
      • <b style="color: #ea580c;">Hyper-casual (Hit Perfect 3D):</b><br>
      <b>+ Mạnh:</b> Nhìn vào hiểu ngay, Juice tức thì, thỏa mãn nhanh.<br>
      <b>- Yếu:</b> Thiếu chiều sâu nâng cấp, vòng đời ngắn, dễ ức chế vì quảng cáo.
    </p>
    <p style="margin: 0 0 8px 0;">
      • <b style="color: #0d828a;">Casual Arcade (Smash Hit):</b><br>
      <b>+ Mạnh:</b> Đồ họa & Audio Juice đỉnh cao, tạo trải nghiệm Flow nhập tâm.<br>
      <b>- Yếu:</b> Dễ cụt hứng vì rào cản của Premium, ít tính năng xã hội.
    </p>
    <p style="margin: 0;">
      • <b style="color: #c2410c;">Endless Runner (Subway Surfers):</b><br>
      <b>+ Mạnh:</b> Meta Loop dài hạn rất mạnh, giữ chân người chơi nhiều năm.<br>
      <b>- Yếu:</b> Đoạn đầu chạy chậm gây chán khi đã thuần thục. Items dễ bị bão hòa
  </div>
</div>

---

<!-- Slide 22: Điểm chung cốt lõi -->

# Điểm chung: Điều gì làm game đáng chơi?

<div >
  <div>
    <div class="left-lead">
      Cả 3 tựa game đều xoay quanh một trục bất biến: <b>Phản hồi rõ ràng</b> và <b>Mục tiêu tiếp theo</b>.
    </div>
    <div class="left-note-box">
      Code chạy đúng là điều kiện tối thiểu — tạo ra cảm giác muốn chơi thêm một lượt nữa mới là đích đến.
    </div>
  </div>

---
# 💡 3 Nguyên lý giữ chân người chơi
  <div class="feature-card" style="border-left: 6px solid #ea580c;">
    <p style="font-size: 1.15rem; font-weight: 700; color: #0f2d59; margin: 0 0 10px 0;">
    </p>
    <p style="margin: 0 0 6px 0; color: #334155;">
      1. <b>Core loop rõ ràng:</b> Bấm là phải có kết quả nhìn thấy/nghe thấy ngay lập tức.
    </p>
    <p style="margin: 0 0 6px 0; color: #334155;">
      2. <b>Độ khó vừa sức:</b> Không bao giờ làm người chơi cảm thấy thua do lỗi game thiếu công bằng.
    </p>
    <p style="margin: 0; color: #334155;">
      3. <b>Mục tiêu dang dở:</b> Người chơi tắt app nhưng trong đầu vẫn nghĩ tới món đồ sắp nâng cấp được.
    </p>
  </div>
</div>