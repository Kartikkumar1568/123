<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Portfolio</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #6a11cb, #2575fc);
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      min-height: 100vh;
    }

    nav {
      width: 100%;
      background: rgba(0, 0, 0, 0.5);
      padding: 10px 0;
      display: flex;
      justify-content: center;
      gap: 15px;
    }

    nav button {
      background: #fff;
      color: #000;
      border: none;
      padding: 10px 20px;
      font-size: 1rem;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s ease-in-out;
    }

    nav button:hover {
      background: #2575fc;
      color: #fff;
    }

    .section {
      display: none;
      text-align: center;
      padding: 20px;
      animation: fadeIn 1s ease-in-out;
    }

    .section.active {
      display: block;
    }

    h1 {
      margin-bottom: 20px;
    }

    .social-media {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }

    .social-media a {
      width: 50px;
      height: 50px;
      display: inline-block;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .social-media img {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      object-fit: cover;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
      transition: box-shadow 0.3s ease;
    }

    .social-media a:hover img {
      transform: scale(1.1);
      box-shadow: 0 6px 10px rgba(0, 0, 0, 0.4);
    }

    .link-container a {
      display: inline-block;
      padding: 10px 20px;
      margin: 10px;
      font-size: 1.2rem;
      color: #fff;
      background: rgba(0, 0, 0, 0.3);
      border: 2px solid #fff;
      border-radius: 5px;
      text-decoration: none;
      transition: all 0.3s ease-in-out;
      position: relative;
      overflow: hidden;
    }

    .link-container a::before {
      content: "";
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: rgba(255, 255, 255, 0.2);
      transform: skewX(-45deg);
      transition: all 0.3s ease-in-out;
    }

    .link-container a:hover::before {
      left: 100%;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
      }
      to {
        opacity: 1;
      }
    }
  </style>
</head>
<body>
  <nav>
    <button onclick="showSection('home')">Home</button>
    <button onclick="showSection('about')">About</button>
    <button onclick="showSection('projects')">Projects</button>
  </nav>

  <div id="home" class="section active">
    <h1>Welcome to My Portfolio</h1>
    <img src="https://i.ibb.co/PFjYYLn/Whats-App-Image-2024-10-24-at-17-47-24-7f75fe44.jpg" alt="My Photo" style="border-radius: 50%; width: 150px; margin-bottom: 20px;">
    <div class="social-media">
      <a href="https://facebook.com" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/51/Facebook_f_logo_%282019%29.svg" alt="Facebook">
      </a>
      <a href="https://www.instagram.com/frostfable/profilecard/?igsh=MWpwaWtvOHRmY2Rw" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram">
      </a>
      <a href="https://www.youtube.com/@Life-with-a-Twist" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/4/42/YouTube_icon_%282013-2017%29.png" alt="YouTube">
      </a>
      <a href="https://chat.whatsapp.com/GP4FjNKpTAa6OrmuYeevjD" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
      </a>
    </div>
  </div>

  <div id="about" class="section">
    <h1>About Me</h1>
    <p>
      Hi, I'm kartik kumar, a passionate developer exploring the world of web and app development. 
      I love solving problems, creating innovative solutions, and learning new technologies.
    </p>
  </div>

  <div id="projects" class="section">
    <h1>My Projects</h1>
    <div class="link-container">
      <a href="https://globalcard.netlify.app/" target="_blank">Project 1</a>
      <a href="https://project2.com" target="_blank">Project 2</a>
      <a href="https://project3.com" target="_blank">Project 3</a>
    </div>
  </div>

  <script>
    function showSection(sectionId) {
      const sections = document.querySelectorAll('.section');
      sections.forEach(section => {
        if (section.id === sectionId) {
          section.classList.add('active');
        } else {
          section.classList.remove('active');
        }
      });
    }
  </script>
</body>
</html>
