<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    /* รีเซ็ต */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: Arial, sans-serif;
      background: url("https://i.postimg.cc/tRLGqYHz/ae7cd05d9438e3a42f955718affa1c9b.gif") no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      line-height: 1.6;
      position: relative;
    }

    /* Navbar */
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 50px;
      background: rgba(15, 23, 42, 0.85);
      flex-wrap: wrap;
    }
    header h1 { 
      color: #38bdf8; 
    }
    nav a {
      margin: 0 15px;
      color: #fff;
      text-decoration: none;
    }
    nav a:hover { color: #38bdf8; }

    /* Hero */
    .hero {
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 100px 50px;
      flex-wrap: wrap;
      text-align: center;
    }
    .hero-text h2 {
      font-size: 3rem;
    }
    .hero-text h3 {
      font-size: 2rem; 
      color: #38bdf8;
      margin: 10px 0;
    }
    .hero-text p {
      font-size: 1.2rem;
    }
    .btn {
      display: inline-block;
      margin-top: 20px;
      padding: 10px 25px;
      background: #38bdf8;
      color: #0b1120;
      border-radius: 5px;
      text-decoration: none;
      font-weight: bold;
    }
    .btn:hover { background: #0ea5e9; }

    /* Section */
    section {
      padding: 60px 50px;
      background: rgba(15, 23, 42, 0.85);
      margin: 20px auto;
      border-radius: 15px;
      max-width: 900px;
    }

    /* หัวข้อ h2 gradient วิ่งเต็มตัว */
    section h2 {
      position: relative;
      margin-bottom: 20px;
      text-align: center;
      font-size: 2.2rem;

      background: linear-gradient(90deg, #38bdf8, #f43f5e, #fff, #34d399, #38bdf8);
      background-size: 300% 100%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;

      animation: animateGradient 5s linear infinite;
      text-shadow: none;
    }

    @keyframes animateGradient {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* เส้น gradient เฉียง */
    section h2::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -8px;
      width: 100%;
      height: 8px;
      background: linear-gradient(120deg, #38bdf8, #f43f5e, #fff, #34d399, #38bdf8);
      transform: skewX(-20deg);
      border-radius: 4px;
      z-index: -1;
      background-size: 300% 100%;
      animation: animateGradient 5s linear infinite;
    }

    /* Profile รูปสมัยใหม่ */
    .profile-wrapper {
      position: relative;
      display: inline-block;
      border-radius: 50%;
      padding: 5px;
      background: linear-gradient(90deg, #38bdf8, #f43f5e, #34d399, #38bdf8);
      background-size: 300% 300%;
      animation: gradientBorder 5s linear infinite;
      box-shadow: 0 10px 20px rgba(56,189,248,0.4), 0 0 30px rgba(52,211,153,0.3);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      margin: 20px 0;
    }
    .profile-wrapper img {
      border-radius: 50%;
      display: block;
      width: 350px;
      height: 400px;
      object-fit: cover;
      transition: transform 0.3s ease;
    }
    .profile-wrapper:hover {
      transform: scale(1.05);
      box-shadow: 0 15px 25px rgba(56,189,248,0.6), 0 0 40px rgba(52,211,153,0.5);
    }

    @keyframes gradientBorder {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Skills Bar */
    .skill { margin: 15px 0; }
    .bar {
      width: 100%;
      background: #1e293b;
      border-radius: 5px;
      overflow: hidden;
    }
    .bar-fill {
      height: 14px;
      background: #38bdf8;
    }

    /* Contact Form */
    form input, form textarea {
      width: 100%;
      margin: 10px 0;
      padding: 12px;
      border: none;
      border-radius: 5px;
    }
    form button {
      padding: 12px 25px;
      background: #38bdf8;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
      margin-top: 10px;
    }
    form button:hover { background: #0ea5e9; }

    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      background: rgba(15, 23, 42, 0.85);
    }

    /* Responsive */
    @media (max-width: 768px) {
      header { flex-direction: column; text-align: center; padding: 15px; }
      nav { margin-top: 10px; }
      nav a { display: block; margin: 8px 0; }
      .hero-text h2 { font-size: 2rem; }
      .hero-text h3 { font-size: 1.4rem; }
      .hero-text p { font-size: 1rem; }
      section { padding: 30px 20px; }
      .profile-wrapper img { width: 200px; height: 200px; }
    }

    .big-form {
      font-size: 18px;
      padding: 20px;
    }
  </style>
</head>
<body>
  <!-- Navbar -->
  <header>
    <h1>MyPortfolio.</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#journey">Education</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Hero -->
  <section class="hero" id="home">
    <div class="hero-text">
      <h2>Hi, I'm SAHARAT TRAKULSUNTHONCHAI</h2>
      <h3 style="font-size:2rem; color:#38bdf8; margin:10px 0;">Newby Developer</h3>
      <p>มีความสามารถในการออกแบบกราฟิก การปั้นโมเดล 3D และเขียนโค้ดเบื้องต้น</p>
      <a href="#contact" class="btn">Contact Me</a>
    </div>
  </section>

  <!-- About -->
  <section id="about">
    <h2>About Me</h2>
    <div style="text-align:center;">
      <div class="profile-wrapper">
        <img src="https://i.postimg.cc/KzJD8KVv/image.png" alt="Profile">
      </div>
    </div>
    <p style="text-align:center; max-width:700px; margin:auto;"> ชื่นชอบในการออกแบบสร้างสิ่งต่างๆที่ชอบและชอบในการสร้างเว็บไซต์ต่างๆ อย่างเช่นเว็บไซต์ ให้ข้อมูลเกม แหล่งรวมรูปภาพ ชอบในการเรียนรู้สิ่งไหม่ๆฝึกในสิ่งที่อยากทำเพราะอยากมีความรู้ความสามารถในหลายๆทางเพราะความเชื่อที่ว่ามนุษย์เรียนรู้ได้ไม่มีที่สิ้นสุด</p>
  </section>

  <!-- Journey -->
  <section id="journey">
    <h2>My Journey</h2>
    <h3>Education</h3>
    <p>2018 - 2021: secondary education - Muangmai School.</p>
    <p>2021 - 2024: Vocational Certificate -  Lopburi Technical College </p>
    <h3>Experience</h3>
    
    <img src="https://i.postimg.cc/wM57G8CY/34-1.png" 
     alt="Example" 
     style="width:800px; height:auto; border:2px solid #38bdf8;">
  </section>

  <!-- Skills -->
  <section id="skills">
    <h2>My Skills</h2>
    <div class="skill">
      <p>HTML</p>
      <div class="bar"><div class="bar-fill" style="width:90%"></div></div>
    </div>
    <div class="skill">
      <p>CSS</p>
      <div class="bar"><div class="bar-fill" style="width:80%"></div></div>
    </div>
    <div class="skill">
      <p>JavaScript</p>
      <div class="bar"><div class="bar-fill" style="width:50%"></div></div>
    </div>
    <div class="skill">
      <p>Python</p>
      <div class="bar"><div class="bar-fill" style="width:5%"></div></div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form class="big-form">
      <input type="text" placeholder="Full Name" required>
      <input type="email" placeholder="Email" required>
      <input type="tel" placeholder="Mobile Number">
      <textarea rows="5" placeholder="Your Message"></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>© 2025 MyPortfolio. All Rights Reserved.</p>
  </footer>
</body>
</html>
