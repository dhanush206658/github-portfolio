# github-portfolio
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dhanush Ram | Portfolio</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: #f9f9f9;
      color: #333;
      line-height: 1.6;
    }

    header {
      background: #4b6cb7;
      color: white;
      padding: 1rem 0;
    }

    .container {
      width: 90%;
      max-width: 1200px;
      margin: auto;
    }

    header .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
    }

    .logo {
      font-size: 1.8rem;
      font-weight: bold;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 10px;
      font-weight: 500;
      padding: 0.5rem 1rem;
      border-radius: 25px;
      background: linear-gradient(145deg, #4b6cb7, #182848);
      transition: 0.3s;
      cursor: pointer;
    }

    nav a:hover, nav a.active {
      background: #ffd700;
      color: #000;
    }

    section {
      padding: 3rem 0;
      display: none;
    }

    section.active-tab {
      display: block;
    }

    .hero {
      background: linear-gradient(135deg, #667eea, #764ba2);
      color: white;
      padding: 4rem 0;
    }

    .hero .container {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 2rem;
      flex-wrap: wrap;
    }

    .hero-img img {
      width: 280px;
      border-radius: 50%;
      border: 5px solid white;
    }

    .hero-content h1 {
      font-size: 2.5rem;
    }

    .hero-content h3 span {
      color: #ffcc00;
    }

    .btn {
      display: inline-block;
      margin-top: 20px;
      padding: 0.8rem 1.5rem;
      background: #ffcc00;
      color: #000;
      border-radius: 25px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }

    .btn:hover {
      background: #e6b800;
    }

    section h2 {
      text-align: center;
      margin-bottom: 1.5rem;
      font-size: 2rem;
      color: #4b6cb7;
    }

    .card-section, .projects {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      flex-wrap: wrap;
    }

    .card, .project {
      background: white;
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      width: 260px;
      text-align: center;
      font-weight: 600;
    }

    .contact-info {
      text-align: center;
      font-size: 1.1rem;
      line-height: 1.8;
    }

    footer {
      background: #eee;
      padding: 1rem 0;
      text-align: center;
      font-size: 0.9rem;
      color: #555;
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="container">
      <div class="logo">Dhanush Ram</div>
      <nav>
        <a class="tab-link active" data-tab="home">Home</a>
        <a class="tab-link" data-tab="about">About</a>
        <a class="tab-link" data-tab="services">Services</a>
        <a class="tab-link" data-tab="projects">Projects</a>
        <a class="tab-link" data-tab="contact">Contact</a>
        <a href="c:\Users\Dhanush Ram\Desktop\myportpolio\lussu.pdf" class="btn" target="_blank">Download Resume</a>
      </nav>
    </div>
  </header>

  <!-- Hero Section (Main Home Page) -->
  <section id="home" class="hero active-tab">
    <div class="container">
      <div class="hero-img">
        <img src="c:\Users\Dhanush Ram\Desktop\myportpolio\1718555820111~2.jpg" alt="Dhanush Ram">
      </div>
      <div class="hero-content">
        <h1>Hello, I'm <span>Dhanush Ram</span></h1>
        <h3>I’m a <span>Web Developer & IT Student</span></h3>
        <a href="#contact" class="btn tab-link" data-tab="contact">Contact Me</a>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about">
    <div class="container">
      <h2>About Me</h2>
      <p>I am an IT student at PSNA College of Engineering and Technology. I enjoy building responsive websites and continuously learning new technologies in the field of development and design.</p>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services">
    <div class="container">
      <h2>Services</h2>
      <div class="card-section">
        <div class="card">Web Design</div>
        <div class="card">Frontend Development</div>
        <div class="card">UI/UX Prototyping</div>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects">
    <div class="container">
      <h2>Projects</h2>
      <div class="projects">
        <div class="project">Portfolio Website</div>
        <div class="project">Lab Booking System</div>
        <div class="project">E-learning Platform</div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <div class="container">
      <h2>Contact Information</h2>
      <div class="contact-info">
        <p><strong>Email:</strong> dhanushramj23it@psnacet.edu.in</p>
        <p><strong>Phone:</strong> +91 6380951594</p>
        <p><strong>Location:</strong> Dindigul, Tamil Nadu, India</p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      &copy; 2025 Dhanush Ram. All Rights Reserved.
    </div>
  </footer>

  <!-- Tab Script -->
  <script>
    const tabs = document.querySelectorAll('.tab-link');
    const sections = document.querySelectorAll('section');

    tabs.forEach(tab => {
      tab.addEventListener('click', function () {
        const target = tab.getAttribute('data-tab');
        sections.forEach(sec => sec.classList.remove('active-tab'));
        tabs.forEach(t => t.classList.remove('active'));
        document.getElementById(target).classList.add('active-tab');
        tab.classList.add('active');
      });
    });
  </script>

</body>
</html>
