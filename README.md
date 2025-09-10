<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SAHARAT's Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    /* Reset */
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Poppins', sans-serif; }
    body {
      background: linear-gradient(135deg, #0f172a, #1e293b);
      color: #fff;
      line-height: 1.6;
    }

    /* Navbar */
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 50px;
      background: rgba(15,23,42,0.9);
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 4px 6px rgba(0,0,0,0.3);
      flex-wrap: wrap;
    }
    header h1 {
      color: #38bdf8;
      font-weight: 700;
      letter-spacing: 1px;
    }
    nav a {
      margin: 0 15px;
      color: #fff;
      text-decoration: none;
      font-weight: 500;
      transition: 0.3s;
    }
    nav a:hover {
      color: #34d399;
      transform: scale(1.05);
    }

    /* Hero Section */
    .hero {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 120px 20px;
      text-align: center;
      background: linear-gradient(180deg, rgba(15,23,42,0.95), rgba(15,23,42,0.85));
    }
    .hero h2 {
      font-size: 3rem;
      background: linear-gradient(90deg, #38bdf8, #f43f5e, #34d399);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: animateGradient 5s linear infinite;
      margin-bottom: 10px;
    }
    .hero h3 {
      font-size: 1.8rem;
      color: #34d399;
      margin-bottom: 20px;
    }
    .hero p {
      font-size: 1.2rem;
      max-width: 700px;
      margin-bottom: 30px;
    }
    .btn {
      padding: 12px 30px;
      background: #38bdf8;
      color: #0f172a;
      font-weight: 600;
      border-radius: 50px;
      text-decoration: none;
      transition: 0.3s;
    }
    .btn:hover {
      background: #0ea5e9;
      transform: scale(1.05);
    }

    @keyframes animateGradient {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Section Styles */
    section {
      padding: 80px 20px;
      max-width: 900px;
      margin: 40px auto;
      background: rgba(15,23,42,0.85);
      border-radius: 20px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.4);
    }
    section h2 {
      text-align: center;
      font-size: 2.5rem;
      background: linear-gradient(90deg, #38bdf8, #f43f5e, #34d399);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 40px;
      animation: animateGradient 5s linear infinite;
    }

    /* Profile Image */
    .profile-wrapper {
      display: flex;
      justify-content: center;
      margin-bottom: 30px;
    }
    .profile-wrapper img {
      border-radius: 50%;
      width: 250px;
      height: 250px;
      object-fit: cover;
      border: 6px solid transparent;
      background: linear-gradient(45deg, #38bdf8, #f43f5e, #34d399, #38bdf8);
      background-clip: padding-box, border-box;
      animation: gradientBorder 5s linear infinite;
    }
    @keyframes gradientBorder {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Skills Cards */
    .skills-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 20px;
    }
    .skill-card {
      flex: 1 1 45%;
      background: #1e293b;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 6px 15px rgba(0,0,0,0.3);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .skill-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.5);
    }
    .skill-card h3 { color: #38bdf8; margin-bottom: 10px; }
    .bar {
      width: 100%;
      height: 12px;
      background: #0f172a;
      border-radius: 8px;
      overflow: hidden;
    }
    .bar-fill {
      height: 100%;
      background: #34d399;
    }

    /* Contact Form */
    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    form input, form textarea {
      padding: 12px;
      border-radius: 10px;
      border: none;
      font-size: 16px;
    }
    form button {
      padding: 12px;
      border-radius: 50px;
      border: none;
      font-weight: 600;
      background: #38bdf8;
      color: #0f172a;
      cursor: pointer;
      transition: 0.3s;
    }
    form button:hover {
      background: #0ea5e9;
      transform: scale(1.05);
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      background: rgba(15,23,42,0.9);
      margin-top: 50px;
      border-radius: 15px 15px 0 0;
    }

    /* Responsive */
    @media(max-width:768px){
      header { flex-direction: column; text-align: center; }
      nav a { margin: 10px 0; }
      .skills-container { flex-direction: column; }
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <h1>SAHARAT</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#journey">Journey</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Hero -->
  <section class="hero" id="home">
    <h2>Hi, I'm SAHARAT TRAKULSUNTHONCHAI</h2>
    <h3>Newby Developer</h3>
    <p>มีความสามารถในการออกแบบกราฟิก การปั้นโมเดล 3D และเขียนโค้ดเบื้องต้น พร้อมที่จะเรียนรู้และสร้างสรรค์สิ่งใหม่ๆ</p>
    <a href="#contact" class="btn">Contact Me</a>
  </section>

  <!-- About -->
  <section id="about">
    <h2>About Me</h2>
    <div class="profile-wrapper">
      <img src="https://i.postimg.cc/KzJD8KVv/image.png" alt="Profile">
    </div>
    <p style="text-align:center; max-width:700px; margin:auto;">ชื่นชอบในการออกแบบสร้างสิ่งต่างๆที่ชอบและชอบในการสร้างเว็บไซต์ต่างๆ เช่น เว็บไซต์ให้ข้อมูลเกม แหล่งรวมรูปภาพ และชอบในการเรียนรู้สิ่งใหม่ๆ ฝึกในสิ่งที่อยากทำเพื่อพัฒนาตัวเองและความสามารถในหลายด้าน เพราะเชื่อว่ามนุษย์เรียนรู้ได้ไม่มีที่สิ้นสุด</p>
  </section>

  <!-- Journey -->
  <section id="journey">
    <h2>My Journey</h2>
    <h3>Education</h3>
    <p>2018 - 2021: Secondary Education - Muangmai School</p>
    <p>2021 - 2024: Vocational Certificate - Lopburi Technical College</p>
    <h3>Experience</h3>
    <img src="https://i.postimg.cc/wM57G8CY/34-1.png" alt="Experience" style="width:100%; border-radius:15px; box-shadow:0 6px 15px rgba(0,0,0,0.3);">
  </section>

  <!-- Skills -->
  <section id="skills">
    <h2>My Skills</h2>
    <div class="skills-container">
      <div class="skill-card">
        <h3>HTML</h3>
        <div class="bar"><div class="bar-fill" style="width:90%"></div></div>
      </div>
      <div class="skill-card">
        <h3>CSS</h3>
        <div class="bar"><div class="bar-fill" style="width:80%"></div></div>
      </div>
      <div class="skill-card">
        <h3>JavaScript</h3>
        <div class="bar"><div class="bar-fill" style="width:50%"></div></div>
      </div>
      <div class="skill-card">
        <h3>Python</h3>
        <div class="bar"><div class="bar-fill" style="width:5%"></div></div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form>
      <input type="text" placeholder="Full Name" required>
      <input type="email" placeholder="Email" required>
      <input type="tel" placeholder="Mobile Number">
      <textarea rows="5" placeholder="Your Message"></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>© 2025 SAHARAT. All Rights Reserved.</p>
  </footer>

</body>
</html>
