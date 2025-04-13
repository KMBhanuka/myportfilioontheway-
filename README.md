<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Tailwind Portfolio</title>

  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Google Font: Poppins -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  
  <!-- AOS (Animate On Scroll) CSS -->
  <link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">

  <style>
    body {
      font-family: 'Poppins', sans-serif;
    }
  </style>
</head>
<body class="bg-gray-100 text-gray-800">

  <!-- Header -->
  <header class="bg-gray-900 text-white shadow">
    <div class="max-w-6xl mx-auto px-4 py-5 flex flex-col md:flex-row items-center justify-between">
      <h1 class="text-2xl font-bold">My Portfolio</h1>
      <nav class="mt-4 md:mt-0">
        <ul class="flex gap-6 text-sm md:text-base">
          <li><a href="#about" class="hover:text-teal-400">About</a></li>
          <li><a href="#projects" class="hover:text-teal-400">Projects</a></li>
          <li><a href="#contact" class="hover:text-teal-400">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- About Section -->
  <section id="about" class="py-16 bg-white text-center">
    <div class="max-w-xl mx-auto px-4" data-aos="fade-up" data-aos-duration="1000">
      <h2 class="text-3xl font-semibold mb-4">About Me</h2>
      <p class="text-lg text-gray-600">
        Hello! I'm a web developer passionate about creating clean, responsive, and user-friendly websites for all devices.
      </p>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects" class="py-16 bg-gray-100">
    <div class="max-w-6xl mx-auto px-4 text-center">
      <h2 class="text-3xl font-semibold mb-8" data-aos="fade-up" data-aos-duration="800">My Projects</h2>
      <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
        <div class="bg-white p-6 rounded-xl shadow hover:shadow-lg transition" data-aos="fade-right" data-aos-delay="100">
          <h3 class="text-xl font-semibold mb-2">Project 1</h3>
          <p class="text-gray-600">Short description of the first project.</p>
        </div>
        <div class="bg-white p-6 rounded-xl shadow hover:shadow-lg transition" data-aos="fade-up" data-aos-delay="200">
          <h3 class="text-xl font-semibold mb-2">Project 2</h3>
          <p class="text-gray-600">Short description of the second project.</p>
        </div>
        <div class="bg-white p-6 rounded-xl shadow hover:shadow-lg transition" data-aos="fade-left" data-aos-delay="300">
          <h3 class="text-xl font-semibold mb-2">Project 3</h3>
          <p class="text-gray-600">Short description of the third project.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-16 bg-white">
    <div class="max-w-md mx-auto px-4 text-center" data-aos="fade-up" data-aos-duration="1000">
      <h2 class="text-3xl font-semibold mb-6">Contact Me</h2>
      <form id="contactForm" class="flex flex-col gap-4">
        <input type="text" placeholder="Your Name" required class="p-3 border rounded-md" />
        <input type="email" placeholder="Your Email" required class="p-3 border rounded-md" />
        <textarea placeholder="Your Message" required class="p-3 border rounded-md"></textarea>
        <button type="submit" class="bg-gray-900 text-white py-2 px-4 rounded-md hover:bg-teal-500 transition">Send Message</button>
      </form>
      <p id="formResponse" class="mt-4 text-teal-600 font-semibold"></p>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-900 text-white text-center py-4">
    <p>© 2025 My Portfolio. All rights reserved.</p>
  </footer>

  <!-- AOS JS -->
  <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init();
  </script>

  <!-- JavaScript -->
  <script>
    // Smooth scrolling
    document.querySelectorAll('a[href^="#"]').forEach(link => {
      link.addEventListener("click", function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute("href"));
        if (target) {
          target.scrollIntoView({ behavior: "smooth" });
        }
      });
    });

    // Simple contact form feedback
    document.getElementById("contactForm").addEventListener("submit", function (e) {
      e.preventDefault();
      document.getElementById("formResponse").textContent = "Thanks! Your message has been sent.";
      this.reset();
    });
  </script>
</body>
</html>
