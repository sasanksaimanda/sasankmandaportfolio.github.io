<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portfolio</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" />
  <style>
    /* Your CSS styles here */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Poppins", sans-serif;
    }

    header {
      background-color: #dc8914;
      height: 100vh;
    }

    .container {
      max-width: 1200px;
      width: 90%;
      margin: auto;
    }

    /* Navbar */
    .navbar {
      position: fixed;
      width: 100%;
      z-index: 500;
    }

    .navbar-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 64px;
    }

    .menu-items {
      display: flex;
    }

    .menu-items li {
      list-style: none;
      padding: 1rem;
    }

    .menu-items a {
      text-decoration: none;
      color: #f0f0e6;
      font-size: 1.2rem;
      padding: 0.3rem;
    }

    .menu-items a:hover {
      border-bottom: 2px solid #f0f0e6;
    }

    .navbar .logo {
      order: 1;
      color: #f0f0e6;
      font-size: 2rem;
    }

    /* Home Content */
    .home-content .name {
      position: absolute;
      top: 47%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: #3a21a0;
      width: 100%;
      text-align: center;
    }

    .home-content .name h1 {
      font-size: 2.2rem;
      text-align: center;
    }

    .home-content .name p {
      color: #f0f0e6;
      font-size: 1.5rem;
    }

    .angle-down-icon {
      position: absolute;
      bottom: 10%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 2rem;
      border: 3px solid #07374a;
      border-radius: 50%;
    }

    .angle-down-icon a {
      text-decoration: none;
      color: #07374a;
      padding: 1rem;
    }

    /* About Me */
    .about-me {
      background-color: #ad1db5;
      padding: 6rem 0;
    }

    .about-me .about-heading {
      color: #25b79f;
      font-size: 2rem;
      font-weight: 600;
      text-align: center;
    }

    .about-content img {
      height: 200px;
      width: 150px;
      object-fit: cover;
      border-radius: 50%;
    }

    .about-content p {
      font-size: 1.2rem;
      color: #f0f0e6;
      padding: 0 2.3rem;
      text-align: center;
    }

    .skills .skills-heading {
      font-size: 2rem;
      font-weight: 600;
      color: #658c85;
      text-align: center;
    }

    .about-me .about-content {
      display: flex;
      flex-wrap: wrap;
    }

    .about-content .left-content {
      flex-basis: 45%;
      text-align: center;
    }

    .about-content .right-content {
      flex-basis: 45%;
    }

    /* Skill Bar */
    .skills-bar {
      padding: 25px 30px;
    }

    .skills-bar .bar {
      margin: 25px 0;
    }

    .skills-bar .bar .info span {
      font-size: 1rem;
      font-weight: 500;
    }

    .skills-bar .bar .info {
      margin-bottom: 8px;
      color: #f0f0e6;
    }

    .skills-bar .bar .progress-line {
      position: relative;
      height: 10px;
      width: 550px;
      background: #f0f0f0;
      border-radius: 10px;
      transform: scaleX(0);
      transform-origin: left;
      animation: animate 1s cubic-bezier(1, 0, 0.5, 1) forwards;
    }

    .bar .progress-line span {
      position: absolute;
      background: #3021b0;
      height: 100%;
      border-radius: 10px;
      transform: scaleX(0);
      transform-origin: left;
      animation: animate 1s 1s cubic-bezier(1, 0, 0.5, 1) forwards;
    }

    @keyframes animate {
      100% {
        transform: scaleX(1);
      }
    }

    .progress-line .html {
      width: 90%;
    }

    .progress-line .css {
      width: 70%;
    }

    .progress-line .JAVA {
      width: 80%;
    }

    .progress-line .SQL {
      width: 70%;
    }

    .progress-line .cybersecurity {
      width: 80%;
    }

    .bar .progress-line span::before {
      position: absolute;
      content: "";
      height: 0;
      right: 0;
      top: -12px;
      width: 0;
      border: 7px solid transparent;
      border-bottom-width: 0px;
      border-right-width: 0px;
      border-top-style: #f0f0f0;
      border-top-color: #f0f0f0;
    }

    .bar .progress-line span::after {
      position: absolute;
      right: 0;
      top: -28px;
      color: #07374a;
      font-size: 12px;
      font-weight: 700;
      background: #f0f0f0;
      padding: 1px 8px;
      border-radius: 3px;
    }

    .progress-line .html::after {
      content: "80%";
    }

    .progress-line .css::after {
      content: "70%";
    }

    .progress-line .java::after {
      content: "70%";
    }

    .progress-line .sql::after {
      content: "70%";
    }

    .progress-line .cybersecurity::after {
      content: "80%";
    }

    .navbar.solid {
      background-color: #07374a;
      transition: background-color 1s ease 0s;
      box-shadow: 0 0 4px rgb(7 55 74 / 20%);
      z-index: 500;
    }

    .navbar.solid .navbar-brand {
      display: inline-block;
      color: #f0f0e6;
      transition: color 1s ease 0s;
    }

    .navbar-brand {
      display: none;
      color: #f0f0e6;
      font-weight: 400;
    }

    .work-arrow {
      margin: 2rem 0;
    }

    .work-arrow a {
      font-size: 1rem;
      text-decoration: none;
      color: #25b79f;
    }

    .work-arrow-2 {
      margin: 2rem 0;
    }

    .work-arrow-2 a {
      font-size: 1rem;
      text-decoration: none;
      color: #25b79f;
      display: none;
    }

    /* Portfolio */
    .portfolio {
      background: #f52727;
      padding: 6rem 0;
    }

    .proj-heading h1 {
      text-align: center;
      color: #07374a;
      font-size: 2.3rem;
      font-weight: 700;
      margin: 3rem 0;
    }

    .proj-1 {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .proj-1 img {
      height: 330px;
      width: 380px;
      object-fit: cover;
      border-radius: 50%;
      box-shadow: 0 20px 10px -10px rgb(37 41 52 / 31%);
      margin-right: 1.7rem;
    }

    .proj-1 .proj1-details {
      width: 32rem;
    }

    .proj-1 .proj1-details i {
      font-size: 1.5rem;
      color: #085f26;
    }

    .proj-1 .proj1-details h2 {
      font-size: 2rem;
      color: #07374a;
    }

    .proj-1 .proj1-details p {
      font-size: 1.3rem;
      color: #07374a;
      font-weight: 600;
    }

    .proj-1 .proj1-details button {
      background: #f0f0e6;
      padding: 0.5rem;
      margin-top: 0.5rem;
      width: 150px;
      border: none;
      border-bottom: 2px solid #07374a;
    }

    .proj-1 .proj1-details button a {
      text-decoration: none;
      color: #07374a;
      font-size: 1.1rem;
      transition: 0.2s ease-in-out;
      text-align: center;
      transition: 0.3s ease-in-out;
    }

    .proj-1 .proj1-details button .fas {
      font-size: 0.7rem;
      padding: 0.3rem;
      transition: 0.2s ease-in-out;
    }

    .proj-1 .proj1-details button:hover {
      background: #07374a;
    }

    .proj-1 .proj1-details button:hover a,
    .proj-1 .proj1-details button:hover .fas {
      color: #f0f0e6;
    }

    /* proj2 */
    .proj-2 {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-top: 3rem;
    }

    .proj-2 img {
      height: 330px;
      width: 380px;
      object-fit: cover;
      border-radius: 50%;
      box-shadow: 0 20px 10px -10px rgb(37 41 52 / 31%);
      margin-right: 1.7rem;
    }

    .proj-2 .proj2-details {
      width: 32rem;
    }

    .proj-2 .proj2-details i {
      font-size: 1.5rem;
      color: #184a07;
    }

    .proj-2 .proj2-details h2 {
      font-size: 2rem;
      color: #0b621b;
    }

    .proj-2 .proj2-details p {
      font-size: 1.3rem;
      color: #0d7709;
      font-weight: 600;
    }

    .proj-2 .proj2-details button {
      background: #d65809;
      padding: 0.5rem;
      margin-top: 0.5rem;
      width: 150px;
      border: none;
      border-bottom: 2px solid #6daac3;
    }

    .proj-2 .proj2-details button a {
      text-decoration: none;
      color: #07374a;
      font-size: 1.1rem;
      transition: 0.2s ease-in-out;
      text-align: center;
      transition: 0.3s ease-in-out;
    }

    .proj-2 .proj2-details button .fas {
      font-size: 0.7rem;
      padding: 0.3rem;
      transition: 0.2s ease-in-out;
    }

    .proj-2 .proj2-details button:hover {
      background: #03364a;
    }

    .proj-2 .proj2-details button:hover a,
    .proj-2 .proj2-details button:hover .fas {
      color: #f0f0e6;
    }

    .more-work {
      text-align: center;
      margin: 3rem 0 1rem 0;
    }

    .more-work p {
      font-size: 1.6rem;
      color: #07374a;
      font-weight: 500;
    }

    .more-work a {
      text-decoration: none;
      color: #f0f0e6;
      font-size: 1.3rem;
    }

    .more-work a:hover {
      border-bottom: 2px solid #f0f0e6;
    }

    /* Contact */
    .contact {
      background: #cbc812;
      position: relative;
      height: 92vh;
    }

    .contact-content {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
    }

    .contact-content h2 {
      font-size: 2.5rem;
      font-weight: 400;
      color: #1758d2;
      padding-bottom: 0.5rem;
    }

    .contact-content .mail {
      color: #1758d2;
      padding-bottom: 0.2rem;
      font-size: 1rem;
    }

    .contact-content .links {
      color: #1758d2;
      padding: 0.5rem;
      padding-bottom: 1.8rem;
      font-size: 1rem;
    }

    .contact-content a {
      text-decoration: none;
      color: #1758d2;
      padding: 0.5rem;
      transition: 0.3s ease-in-out;
    }

    .contact-content a:hover {
      color: #f0f0e6;
    }

    /* Media Queries */
    @media (max-width: 500px) {
      html {
        font-size: 60%;
      }

      .about-content .left-content {
        flex-basis: 100%;
        text-align: center;
      }

      .about-content .right-content {
        flex-basis: 100%;
      }

      .skills {
        width: 100%;
      }

      .skills-bar .bar .progress-line {
        width: 100%;
      }

      .work-arrow {
        display: none;
      }

      .right-content h1 {
        margin-top: 3.2rem;
      }

      .proj-1 {
        display: flex;
        justify-content: center;
        flex-direction: column;
      }

      .proj-1 img {
        height: 230px;
        width: 290px;
        margin-bottom: 0.5rem;
      }

      .proj-2 {
        display: flex;
        justify-content: center;
        flex-direction: column;
      }

      .proj-2 img {
        height: 250px;
        width: 290px;
        margin-bottom: 0.5rem;
      }

      .work-arrow-2 a {
        font-size: 1.3rem;
        text-decoration: none;
        color: #25b79f;
        display: block;
        text-align: center;
      }

      .contact-content {
        width: 100%;
      }
    }

    @media (min-width: 501px) and (max-width: 768px) {
      html {
        font-size: 65%;
      }

      .about-content .left-content {
        flex-basis: 100%;
        text-align: center;
      }

      .about-content .right-content {
        flex-basis: 100%;
      }

      .skills {
        width: 100%;
      }

      .skills-bar .bar .progress-line {
        width: 100%;
      }

      .work-arrow {
        display: none;
      }

      .right-content h1 {
        margin-top: 3.2rem;
      }

      .proj-1 {
        display: flex;
        justify-content: center;
        flex-direction: column;
      }

      .proj-1 img {
        height: 240px;
        width: 290px;
        margin-bottom: 0.5rem;
      }

      .proj-2 {
        display: flex;
        justify-content: center;
        flex-direction: column;
      }

      .proj-2 img {
        height: 240px;
        width: 290px;
        margin-bottom: 0.5rem;
      }

      .work-arrow-2 a {
        font-size: 1.3rem;
        text-decoration: none;
        color: #25b79f;
        display: block;
        text-align: center;
      }

      .contact-content {
        width: 100%;
      }
    }

    @media (min-width: 769px) and (max-width: 1200px) {
      html {
        font-size: 70%;
      }

      .about-content .left-content {
        flex-basis: 100%;
        text-align: center;
      }

      .about-content .right-content {
        flex-basis: 100%;
      }

      .skills {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
      }

      .work-arrow {
        display: none;
      }

      .left-content h1 {
        margin-top: 3.2rem;
        text-align: center;
      }

      .right-content h1 {
        margin-top: 3.2rem;
        text-align: center;
      }

      .work-arrow-2 a {
        font-size: 1.3rem;
        text-decoration: none;
        color: #25b79f;
        display: block;
        text-align: center;
      }

      .contact-content {
        width: 100%;
      }
    }

    @media (orientation: landscape) and (max-height: 500px) {
      .header {
        height: 90vmax;
      }
    }
  </style>
</head>
<body>
  <header class="header">
    <nav class="navbar">
      <div class="navbar-container container">
        <div>
          <h1 class="navbar-brand">Sasank Manda</h1>
        </div>
        <ul class="menu-items">
          <li><a href="#about">About</a></li>
          <li><a href="#my-works">Portfolio</a></li>
          <li><a href="#contact-me">Contact</a></li>
        </ul>
      </div>
    </nav>
    <div class="home-content" id="home-page">
      <div class="name">
        <h1>Hi, I'm Sasank</h1>
        <p>working on web development and cyber security .</p>
      </div>
      <div class="angle-down-icon">
        <a href="#about"><i class="fas fa-angle-down"></i></a>
      </div>
    </div>
  </header>
  <section class="about-me" id="about">
    <div class="container">
      <div class="about-content">
        <div class="left-content">
          <div>
            <h1 class="about-heading">About Me</h1>
          </div>
          <img src="images/me.png" alt="image" />
          <p>
            I am 19 year old, Btech student at VIT-AP pursuing computer science I really enjoy solving problems as well
            as making things pretty and easy to use. I can't stop learning new things; the more, the better.
          </p>
          <div class="work-arrow">
            <p><a href="#my-works">Check out my work <i class="fas fa-arrow-down"></i></a></p>
          </div>
        </div>
        <div class="skills">
          <div class="right-content">
            <div>
              <h1 class="skills-heading">My Skills</h1>
            </div>
            <div class="skills-bar">
              <div class="bar">
                <div class="info">
                  <span>HTML</span>
                </div>
                <div class="progress-line HTML">
                  <span></span>
                </div>
              </div>
              <div class="bar">
                <div class="info">
                  <span>CSS</span>
                </div>
                <div class="progress-line CSS">
                  <span></span>
                </div>
              </div>
              <div class="bar">
                <div class="info">
                  <span>Java</span>
                </div>
                <div class="progress-line Java">
                  <span></span>
                </div>
              </div>
              <div class="bar">
                <div class="info">
                  <span>SQL</span>
                </div>
                <div class="progress-line SQL">
                  <span></span>
                </div>
              </div>
              <div class="bar">
                <div class="info">
                  <span>Cybersecurity</span>
                </div>
                <div class="progress-line Cybersecurity">
                  <span></span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="portfolio" id="my-works">
    <div class="container">
      <div class="proj-heading">
        <h1>My Portfolio</h1>
      </div>
      <div class="proj-1">
        <img src="images/proj1.png" alt="project 1" />
        <div class="proj1-details">
          <i class="fas fa-tasks"></i>
          <h2>Project 1</h2>
          <p>Automated indoor gardener using RaspberryPI.</p>
          <button><a href="https://github.com/sasanksaimanda/Autonomous.rescue.robot">View Details <i class="fas fa-arrow-right"></i></a></button>
        </div>
      </div>
      <div class="proj-2">
        <img src="images/proj2.jpg" alt="project 2" />
        <div class="proj2-details">
          <i class="fas fa-tasks"></i>
          <h2>Project 2</h2>
          <p>Autonomous rescue robot using Arduino.</p>
          <button><a href="https://github.com/sasanksaimanda/Autonomous.rescue.robot">View Details <i class="fas fa-arrow-right"></i></a></button>
        </div>
      </div>
      <div class="work-arrow-2">
        <p><a href="#contact-me">Get in touch <i class="fas fa-arrow-down"></i></a></p>
      </div>
    </div>
  </section>
  <section class="contact" id="contact-me">
    <div class="contact-content">
      <h2>Get In Touch</h2>
      <p class="mail">Email: sasankmanda8@gmail.com</p>
      <p class="links">Find me on social media:</p>
      <div class="social-links">
        <a href="https://www.linkedin.com/in/sasank-sai-manda-4a3383227/"><i class="fab fa-linkedin"></i></a>
        <a href="https://github.com/sasanksaimanda"><i class="fab fa-github"></i></a>
        <a href="https://www.instagram.com/sasankkkk/"><i class="fab fa-instagram"></i></a>
      </div>
    </div>
  </section>
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <script>
    window.addEventListener("scroll", function () {
      var header = document.querySelector("header");
      header.classList.toggle("solid", window.scrollY > 0);
    });
  </script>
</body>
</html>

