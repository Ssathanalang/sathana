<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Sathana S — Portfolio</title>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;900&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#05070f;
      --card:#121a2f;
      --text:#f5f7ff;
      --muted:#a5afc9;
      --brand:#7b61ff;
      --accent:#00d9ff;
      --highlight:#5fff9f;
      --shadow:0 12px 28px rgba(0,0,0,.35);
      --radius:20px;
    }
    *{box-sizing:border-box;}
    body{
      margin:0; font-family:'Inter',sans-serif; background:var(--bg); color:var(--text); line-height:1.6; overflow-x:hidden;
    }
    header{position:sticky;top:0;background:rgba(8,13,24,.92);backdrop-filter:blur(10px);border-bottom:1px solid rgba(255,255,255,.08);z-index:10;}
    nav{max-width:1100px;margin:0 auto;padding:14px 18px;display:flex;justify-content:space-between;align-items:center;}
    .logo{display:flex;align-items:center;gap:10px;font-weight:900;font-size:18px;}
    .logo-mark{width:34px;height:34px;border-radius:10px;background:linear-gradient(135deg,var(--brand),var(--accent));box-shadow:0 0 0 5px rgba(123,97,255,.25),var(--shadow)}
    .nav-links a{margin-left:18px;color:var(--muted);font-weight:600;text-decoration:none;transition:.3s;cursor:pointer;}
    .nav-links a.active{color:var(--text);}
    .container{max-width:1100px;margin:0 auto;padding:32px 18px 80px;}
    .section{display:none;opacity:0;transform:translateY(20px);transition:all .6s ease;}
    .section.active{display:block;opacity:1;transform:translateY(0);}
    .hero{display:grid;grid-template-columns:1.1fr .9fr;gap:30px;align-items:center;margin-top:40px;}
    .badge{display:inline-flex;align-items:center;gap:10px;padding:8px 12px;border-radius:999px;background:rgba(123,97,255,.15);border:1px solid rgba(123,97,255,.4);font-size:12px;font-weight:700;text-transform:uppercase;letter-spacing:1px;}
    .title{font-size:clamp(34px,5vw,64px);font-weight:900;line-height:1.1;margin:16px 0 10px;}
    .subtitle{font-size:clamp(15px,1.6vw,20px);color:var(--muted);margin-bottom:22px;}
    .cta-row{display:flex;gap:16px;flex-wrap:wrap;}
    .btn{padding:12px 18px;border-radius:14px;border:1px solid rgba(255,255,255,.1);background:linear-gradient(180deg,rgba(255,255,255,.05),rgba(255,255,255,.02));color:var(--text);text-decoration:none;font-weight:700;box-shadow:var(--shadow);transition:.3s;}
    .btn.primary{background:linear-gradient(135deg,var(--brand),var(--accent));border:0;color:#fff;}
    .btn:hover{transform:translateY(-3px);}
    .card{background:linear-gradient(180deg,rgba(255,255,255,.04),rgba(255,255,255,.01));border:1px solid rgba(255,255,255,.08);border-radius:var(--radius);padding:24px;box-shadow:var(--shadow)}
    .kv{display:grid;grid-template-columns:120px 1fr;row-gap:10px;column-gap:18px;align-items:center;}
    .kv .k{color:var(--muted)}
    .kv .v{font-weight:700}
    .skills{display:flex;flex-wrap:wrap;gap:12px;padding:0;margin:0;list-style:none;}
    .skills li{background:rgba(123,97,255,.15);border:1px solid rgba(123,97,255,.3);padding:8px 14px;border-radius:12px;font-weight:700;transition:.3s;}
    .skills li:hover{background:var(--accent);color:#000;}
    .timeline{position:relative;margin-left:20px;padding-left:20px;border-left:3px solid var(--brand);}
    .timeline .event{margin-bottom:20px;}
    .timeline .event h3{margin:0;font-size:18px;color:var(--highlight)}
    .timeline .event span{font-size:14px;color:var(--muted)}
    .certificates-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:20px;margin-top:20px;}
    .certificates-grid img{width:100%;border-radius:12px;box-shadow:var(--shadow);transition:.3s;}
    .certificates-grid img:hover{transform:scale(1.05);}
    .profile-pic{
      width:100%;
      max-width:320px;
      border-radius:20px;
      border:6px solid var(--accent);
      box-shadow:0 8px 24px rgba(0,0,0,0.4);
      transition:.3s;
    }
    .profile-pic:hover{
      transform:scale(1.05) rotate(-1.5deg);
      border-color:var(--highlight);
    }
    footer{margin-top:50px;color:var(--muted);text-align:center}
    @media(max-width:900px){.hero{grid-template-columns:1fr;}}
  </style>
</head>
<body>
  <header>
    <nav>
      <div class="logo">
        <div class="logo-mark"></div>
        <span>Sathana S · Portfolio</span>
      </div>
      <div class="nav-links">
        <a data-target="home" class="active">Home</a>
        <a data-target="about">About</a>
        <a data-target="education">Education</a>
        <a data-target="skills">Skills</a>
        <a data-target="certificates">Certificates</a>
        <a data-target="contact">Contact</a>
      </div>
    </nav>
  </header>

  <main class="container">
    <section id="home" class="section active">
      <div class="hero">
        <div>
          <span class="badge">Aspiring Professional</span>
          <h1 class="title">Hello, I’m <span style="background:linear-gradient(135deg,var(--accent),var(--highlight));-webkit-background-clip:text;background-clip:text;color:transparent">Sathana S</span></h1>
          <p class="subtitle">A passionate <strong>BCA student</strong> who thrives on building impactful digital experiences and growing through collaboration, creativity, and leadership.</p>
          <div class="cta-row">
            <a class="btn primary" data-target="contact">Hire Me</a>
          </div>
          <div class="card" style="margin-top:20px;">
            <div class="kv">
              <div class="k">Name</div><div class="v">Sathana S</div>
              <div class="k">Age</div><div class="v">19</div>
              <div class="k">DOB</div><div class="v">28/03/2006</div>
              <div class="k">Gender</div><div class="v">Female</div>
              <div class="k">Phone</div><div class="v"><a href="tel:+919043585389" style="color:inherit">+91 90435 85389</a></div>
              <div class="k">Email</div><div class="v"><a href="mailto:13653bca2024@princescience.in" style="color:inherit">13653bca2024@princescience.in</a></div>
              <div class="k">Location</div><div class="v">Chennai, India</div>
            </div>
          </div>
        </div>
        <!-- Profile Picture -->
        <div>
          <img src="myphoto.jpg" alt="Sathana S" class="profile-pic">
        </div>
      </div>
    </section>

    <section id="about" class="section card">
      <h2>About Me</h2>
      <p>I am currently pursuing a <strong>Bachelor of Computer Applications (BCA)</strong> at Prince Shri Venkateswara Arts & Science College, Gowrivakkam. I enjoy solving problems, creating user-friendly designs, and continuously improving my technical and leadership skills.</p>
    </section>

    <section id="education" class="section card">
      <h2>Education</h2>
      <div class="timeline">
        <div class="event">
          <h3>Bachelor of Computer Applications</h3>
          <span>Prince Shri Venkateswara Arts & Science College, Gowrivakkam · 2024 — Present</span>
        </div>
        <div class="event">
          <h3>Higher Secondary</h3>
          <span>Completed in 2023 with strong focus on Computer Science and Mathematics</span>
        </div>
      </div>
    </section>

    <section id="skills" class="section card">
      <h2>Skills</h2>
      <ul class="skills">
        <li>Strong coding fundamentals</li>
        <li>Leadership and teamwork</li>
        <li>Effective communication</li>
        <li>Problem-solving</li>
        <li>Time management</li>
        <li>Creative thinking</li>
      </ul>
    </section>

    <!-- Certificates Section -->
    <section id="certificates" class="section card">
      <h2>Certificates</h2>
      <div class="certificates-grid">
        <img src="certificate1.jpg" alt="Certificate 1">
        <img src="certificate2.jpg" alt="Certificate 2">
      </div>
    </section>

    <section id="contact" class="section card">
      <h2>Contact Me</h2>
      <p>If you are looking for a motivated and enthusiastic student to join your team, feel free to get in touch with me.</p>
      <div class="cta-row">
        <a class="btn primary" href="tel:+919043585389">Call</a>
        <a class="btn" href="mailto:13653bca2024@princescience.in">Email</a>
        <a class="btn" href="https://wa.me/919043585389" target="_blank" rel="noopener">WhatsApp</a>
      </div>
    </section>

    <footer>
      <p>© <span id="year"></span> Sathana S · Professional Portfolio</p>
    </footer>
  </main>

  <script>
    document.getElementById('year').textContent=new Date().getFullYear();

    const navLinks=document.querySelectorAll('.nav-links a, .btn[data-target]');
    const sections=document.querySelectorAll('.section');

    navLinks.forEach(link=>{
      link.addEventListener('click',()=>{
        const target=link.getAttribute('data-target');
        if(!target) return;

        sections.forEach(sec=>{
          sec.classList.remove('active');
        });
        navLinks.forEach(l=>l.classList.remove('active'));

        document.getElementById(target).classList.add('active');
        link.classList.add('active');
      });
    });
  </script>
</body>
</html>
