# Nishant-Sonkamble.github.io

portifolio/
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Portfolio</title>

  <style>
    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      background-color: #f4f4f4;
      color: #333;
    }

    header {
      background-color: #1f2937;
      color: white;
      text-align: center;
      padding: 2.5rem 1rem;
      animation: fadeInDown 1s ease;
    }

    header h1 {
      margin: 0;
      font-size: 2.5rem;
      transition: transform 0.3s;
    }

    header h1:hover {
      transform: scale(1.05);
    }

    section {
      max-width: 800px;
      margin: 2rem auto;
      background: white;
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.05);
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      color: #007acc;
    }

    ul {
      list-style: none;
      padding-left: 0;
    }

    ul li {
      padding: 0.3rem 0;
    }

    a {
      color: #007acc;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    .button {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      background-color: #007acc;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: all 0.3s;
    }

    .button:hover {
      background-color: #005f99;
      transform: scale(1.05);
    }

    .button:active {
      transform: scale(0.98);
    }

    footer {
      text-align: center;
      padding: 1rem;
      background-color: #e0e0e0;
      margin-top: 2rem;
    }

    @keyframes fadeInDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <header>
    <h1 onmouseover="highlightHeader(this)" onmouseout="unhighlightHeader(this)">Nishant Sonkamble </h1>
    <p>1st Year CS Student | Learning Web Development</p>
  </header>

  <section id="about">
    <h2>About Me</h2>
    <img src="my picture.png" width="100px"
         style="float:right;margin-left:16px;border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.2);" />

    <p>
      "I'm a first-year Computer Science student currently learning HTML, CSS, and JavaScript. While there's still much to learn, I'm committed to improving through hands-on experience and embracing challenges. I enjoy exploring new technologies and expanding my skill set.I'm currently interested in web development and have started building simple websites to apply my learning."    </p>
    <div style="clear: both;"></div>
  </section>

  <section id="projects">
  <h2>Projects</h2>

  <div class="project">
    <h3>Simple Calculator</h3>

    <img src="calculator.png.png" alt="Calculator Screenshot" width="300"
         style="border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.2);" />

    <p>A basic calculator using HTML, CSS, and JavaScript.</p>

       <a href="calci for internship.html">Live Demo</a> |
    <a href="https://github.com/Nishant-Sonkamble/calculator-for-internship/tree/main">GitHub Code</a>
  </div>
</section>

  <section id="skills">
    <h2>Skills</h2>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript (Basic)</li>
    </ul>
  </section>

  <section id="learning">
    <h2>Currently Learning</h2>
    <p>Focused on learning JavaScript and building interactive web pages. Planning to learn about coding language such as python,c++,etc.</p>
  </section>

<section id="Resume">
    <h2>My resume</h2>
    <p>To see my resume<a href="documents/Nishnat resume(1).pdf"> Click here</a></p>
  </section>

  <section id="contact">
  <h2>Contact</h2>

  <p>
    Email:
    <a href="mailto:sonkamblenishant4@gmail.com">sonkamblenishant4@gmail.com</a>
  </p>

  <p>
    LinkedIn:
    <a href="https://www.linkedin.com/in/nishant-sonkamble-632ba6334?trk=contact-info" target="_blank">
      linkedin.com/in/nishant-sonkamble
    </a>
  </p>

  <button class="button" onclick="sayHello()">Click Me</button>
</section>

  <footer>
    <p>© 2025 Nishant Sonkamble</p>
  </footer>

  <script>
    
    function sayHello() {
      alert("Thank you for visiting my portfolio!");
    }

    
    function highlightHeader(elem) {
      elem.style.color = "#00ffff";
    }

    function unhighlightHeader(elem) {
      elem.style.color = "white";
    }

    
    const sections = document.querySelectorAll('section');

    function revealOnScroll() {
      const triggerBottom = window.innerHeight * 0.9;
      sections.forEach(section => {
        const top = section.getBoundingClientRect().top;
        if (top < triggerBottom) {
          section.classList.add('visible');
        }
      });
    }

    window.addEventListener('scroll', revealOnScroll);
    window.addEventListener('load', revealOnScroll);
  </script>

</body>
</html>
