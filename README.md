<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SAHARAT Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
<style>
/* Reset */
* { margin:0; padding:0; box-sizing:border-box; font-family:'Poppins',sans-serif; }
body { overflow-x:hidden; background:#0f172a; color:#fff; }
canvas { position:fixed; top:0; left:0; z-index:-1; }

/* Navbar */
header{
  display:flex; justify-content:space-between; align-items:center;
  padding:20px 50px; background:rgba(15,23,42,0.9); position:sticky; top:0; z-index:10;
  box-shadow:0 4px 10px rgba(0,0,0,0.5); flex-wrap:wrap;
}
header h1 { color:#0ff; font-weight:700; font-size:1.8rem; }
nav a { margin:0 15px; color:#fff; text-decoration:none; font-weight:500; transition:.3s; }
nav a:hover { color:#ff3f7d; transform:scale(1.05); }

/* Hero Section */
.hero{
  display:flex; flex-wrap:wrap; align-items:center; justify-content:center;
  padding:100px 20px; min-height:100vh; gap:40px;
}
.hero-text{ flex:1 1 400px; }
.hero-text h2{
  font-size:3rem; color:#0ff; text-shadow:0 0 10px #0ff,0 0 20px #0ff;
  margin-bottom:15px;
}
.hero-text h3{
  font-size:1.8rem; color:#ff3f7d; margin-bottom:20px;
}
.hero-text p{ font-size:1.1rem; margin-bottom:30px; line-height:1.5; color:#ccc; }
.btn{
  display:inline-block; padding:12px 30px; border-radius:50px; font-weight:600;
  text-decoration:none; color:#0f172a; background:#0ff; transition:.3s;
}
.btn:hover{ background:#ff3f7d; transform:scale(1.05); box-shadow:0 0 10px #ff3f7d,0 0 20px #ff3f7d; }

/* Hero Image */
.hero-image{
  flex:1 1 300px; display:flex; justify-content:center; perspective:1000px;
}
.hero-image img{
  width:300px; border-radius:20px;
  box-shadow:0 0 30px #0ff,0 0 60px #ff3f7d;
  transform:rotateY(0deg) rotateX(0deg);
  transition:transform .5s, box-shadow .5s;
}
.hero-image img:hover{ transform:rotateY(15deg) rotateX(5deg); }

/* Sections */
section{
  max-width:900px; margin:40px auto; padding:60px 30px;
  background:rgba(15,23,42,0.85); border-radius:20px; box-shadow:0 10px 20px rgba(0,0,0,0.5);
}
section h2{
  text-align:center; font-size:2.5rem;
  background:linear-gradient(90deg,#0ff,#ff3f7d,#0f0); -webkit-background-clip:text; -webkit-text-fill-color:transparent;
  margin-bottom:40px; animation:gradientAnim 5s linear infinite;
}
@keyframes gradientAnim{
  0%{background-position:0% 50%;}
  50%{background-position:100% 50%;}
  100%{background-position:0% 50%;}
}

/* Profile */
.profile-wrapper{ display:flex; justify-content:center; margin-bottom:30px; }
.profile-wrapper img{ width:250px; height:250px; border-radius:50%; border:5px solid #0ff; box-shadow:0 0 20px #0ff,0 0 40px #ff3f7d; }

/* Skills Cards */
.skills-container{ display:flex; flex-wrap:wrap; justify-content:space-between; gap:20px; }
.skill-card{
  flex:1 1 45%; padding:20px; border-radius:15px; background:#1e293b; box-shadow:0 6px 15px rgba(0,0,0,0.5);
  transition:.3s;
}
.skill-card:hover{ transform:translateY(-5px); box-shadow:0 10px 25px rgba(0,0,0,0.7); }
.skill-card h3{ color:#0ff; margin-bottom:10px; }
.bar{ width:100%; height:12px; background:#0f172a; border-radius:8px; overflow:hidden; }
.bar-fill{ height:100%; background:#ff3f7d; }

/* Contact Form */
form{ display:flex; flex-direction:column; gap:15px; }
form input,form textarea{ padding:12px; border-radius:10px; border:none; font-size:16px; }
form button{
  padding:12px; border-radius:50px; border:none; font-weight:600; background:#0ff; color:#0f172a; cursor:pointer; transition:.3s;
}
form button:hover{ background:#ff3f7d; transform:scale(1.05); box-shadow:0 0 10px #ff3f7d,0 0 20px #ff3f7d; }

/* Footer */
footer{ text-align:center; padding:20px; background:rgba(15,23,42,0.9); margin-top:50px; border-radius:15px 15px 0 0; }

/* Responsive */
@media(max-width:768px){
  .hero{ flex-direction:column; text-align:center; }
  .hero-image img{ width:200px; }
  .skills-container{ flex-direction:column; }
}

/* Particles Animation */
.particle{ position:absolute; border-radius:50%; background:rgba(255,255,255,0.7); pointer-events:none; }
</style>
</head>
<body>

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
  <div class="hero-text">
    <h2>Hi, I'm SAHARAT TRAKULSUNTHONCHAI</h2>
    <h3>Newby Developer</h3>
    <p>ออกแบบกราฟิก 3D และเขียนโค้ดเบื้องต้น พร้อมสร้างสิ่งใหม่ ๆ และพัฒนาอย่างต่อเนื่อง</p>
    <a href="#contact" class="btn">Contact Me</a>
  </div>
  <div class="hero-image">
    <img src="https://i.postimg.cc/KzJD8KVv/image.png" alt="Profile">
  </div>
</section>

<!-- About -->
<section id="about">
  <h2>About Me</h2>
  <div class="profile-wrapper">
    <img src="https://i.postimg.cc/KzJD8KVv/image.png" alt="Profile">
  </div>
  <p style="text-align:center;">ชื่นชอบในการออกแบบสร้างสิ่งต่างๆที่ชอบและชอบในการสร้างเว็บไซต์ ฝึกสิ่งใหม่ ๆ เพื่อพัฒนาความสามารถและความรู้ที่ไม่สิ้นสุด</p>
</section>

<!-- Journey -->
<section id="journey">
  <h2>My Journey</h2>
  <h3>Education</h3>
  <p>2018 - 2021: Secondary Education - Muangmai School</p>
  <p>2021 - 2024: Vocational Certificate - Lopburi Technical College</p>
  <h3>Experience</h3>
  <img src="https://i.postimg.cc/wM57G8CY/34-1.png" alt="Experience" style="width:100%; border-radius:15px; box-shadow:0 6px 15px rgba(0,0,0,0.5);">
</section>

<!-- Skills -->
<section id="skills">
  <h2>My Skills</h2>
  <div class="skills-container">
    <div class="skill-card"><h3>HTML</h3><div class="bar"><div class="bar-fill" style="width:90%"></div></div></div>
    <div class="skill-card"><h3>CSS</h3><div class="bar"><div class="bar-fill" style="width:80%"></div></div></div>
    <div class="skill-card"><h3>JavaScript</h3><div class="bar"><div class="bar-fill" style="width:50%"></div></div></div>
    <div class="skill-card"><h3>Python</h3><div class="bar"><div class="bar-fill" style="width:5%"></div></div></div>
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

<script>
// Particles JS
const numParticles=100;
for(let i=0;i<numParticles;i++){
  const p=document.createElement('div');
  p.classList.add('particle');
  p.style.width=p.style.height=Math.random()*4+2+'px';
  p.style.top=Math.random()*window.innerHeight+'px';
  p.style.left=Math.random()*window.innerWidth+'px';
  document.body.appendChild(p);
}

const particles=document.querySelectorAll('.particle');
function animateParticles(){
  particles.forEach(p=>{
    let x=parseFloat(p.style.left);
    let y=parseFloat(p.style.top);
    y-=0.3+Math.random()*0.3;
    if(y<0){ y=window.innerHeight; x=Math.random()*window.innerWidth; }
    p.style.top=y+'px'; p.style.left=x+'px';
  });
  requestAnimationFrame(animateParticles);
}
animateParticles();
</script>

</body>
</html>
