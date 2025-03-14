# Ex02 Commercial Website
## Date:14-03-2025

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
*/
DEVELOPED BY : NARRA RAMYA

REG NO : 212223040128
*/
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Codenvy</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
    }
    .splash-screen {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: lightskyblue;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      animation: fadeOut 3s forwards; 
    }

    .splash-screen img {
      max-width: 200px; 
      animation: zoomIn 3s ease-in-out; 
    }

    @keyframes zoomIn {
      0% {
        transform: scale(0.5);
        opacity: 0;
      }
      100% {
        transform: scale(1);
        opacity: 1;
      }
    }

    @keyframes fadeOut {
      0% {
        opacity: 1;
      }
      100% {
        opacity: 0;
        visibility: hidden; 
      }
    }
    .main-content {
      display: none; 
    }
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      background-color: powderblue;
      color: black;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header .logo {
      font-size: 1.5rem;
      font-weight: bold;
    }

    header nav ul {
      display: flex;
      list-style: none;
    }

    header nav ul li {
      margin-left: 1.5rem;
    }

    header nav ul li a {
      color: black;
      text-decoration: none;
      transition: color 0.3s;
    }

    header nav ul li a:hover {
      color:black;
      text-decoration: underline;
    }
    .hero {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 400px;
      background-color: white; 
      color: black; 
      text-align: center;
      padding: 2rem;
    }

    .hero h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }

    .hero .cta-button {
      padding: 0.75rem 1.5rem;
      background-color: white;
      color: black;
      text-decoration: none;
      border-radius: 5px;
      transition: background-color 0.3s;
    }

    .hero .cta-button:hover {
      background-color: powderblue;
    }

    .about {
      padding: 2rem;
      text-align: center;
      background-color: white;
    }

    .about h2 {
      margin-bottom: 1.5rem;
    }

    .about p {
      max-width: 800px;
      margin: 0 auto;
      line-height: 1.8;
    }

    .services {
      padding: 2rem;
      text-align: center;
      background-color: white;
    }

    .services h2 {
      margin-bottom: 1.5rem;
    }

    .service-container {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }

    .service {
      flex: 1 1 30%;
      margin: 1rem;
      padding: 1.5rem;
      background-color: white;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 10px;
    }

    .section {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 50vh;
    text-align: center;
    background: #f4f4f4;
    margin: 10px;
    padding: 20px;
    border-radius: 10px;
    background-color:WHITE;
}
    footer {
      text-align: center;
      padding: 1rem;
      background-color:powderblue;
      color: black;
    }
    @media (max-width: 768px) {
      header {
        flex-direction: column;
        text-align: center;
      }

      header nav ul {
        flex-direction: column;
        margin-top: 1rem;
      }

      header nav ul li {
        margin: 0.5rem 0;
      }

      .service-container {
        flex-direction: column;
      }

      .service {
        flex: 1 1 100%;
      }
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <div class="splash-screen">
    <img src="codenvy logo.jpg" alt="CodeXel Logo"> 
  </div>

  <!-- Main Content -->
  <div class="main-content">
    <header>
      <div class="logo">Codenvy</div>
      <nav>
        <ul>
          <li><a href="#home" onclick="showSection('home')">Home</a></li>
          <li><a href="#about" onclick="showSection('about')">About</a></li>
          <li><a href="#services" onclick="showSection('services')">Services</a></li>
          <li><a href="#contact" onclick="showSection('contact')">Contact</a></li>
        </ul>
      </nav>
    </header>

    <!-- Home Section -->
    <section id="home" class="hero">
      <h1>Welcome to Codenvy</h1>
      <p>Code, debug, and deploy applications in the cloud.</p>
      <a href="#services" onclick="showSection('services')" class="cta-button">Sign Up for Free</a>
    </section>

    <!-- About Section -->
    <section id="about" class="about hidden">
      <h2>About Us</h2>
      <p>
        At Codenvy, our mission is to empower developers to create, innovate, and succeed in the cloud. 
        We believe that cloud-based development should be accessible, collaborative, and fun. 
        Our platform is designed to help developers work more efficiently, effectively, and enjoyably.
.
      </p>
    </section>

    <!-- Services Section -->
    <section id="services" class="services hidden">
      <h2>Our Services</h2>
      <div class="service-container">
        <div class="service">
          <h3> Workspace Management</h3>
          <p>Codenvy allows developers to create and manage multiple workspaces, each with its own set of projects, files, and settings.</p>
        </div>
        <div class="service">
          <h3> Debugging and Testing</h3>
          <p>Codenvy offers debugging and testing tools that allow developers to identify and fix errors in their code, including features like breakpoints, console output, and test runners.</p>
        </div>
        <div class="service">
          <h3>Support and Training</h3>
          <p>Codenvy offers support and training resources that help developers get started with the platform and resolve any issues they may encounter, including documentation, tutorials, and customer support.</p>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    </section>

    <section id="contact" class="section">
        <h2>Contact Us<p><sub>Email: codenvy123@gmail.com<p><sub>Phone NO: 4124-65432-7865<p><sub>Address: KV Colony,Anna Nagar,Chennai<p><sub>Pincode: 602571</sub></p></h2>
        
    </section><br><br><br><br><br><br><br><br><br>
    <footer>
      <p>&copy; 2025 Codenvy. All rights reserved.</p>
    </footer>
  </div>

  <script>
    // Function to show the selected section and hide others
    function showSection(sectionId) {
      // Hide all sections
      document.querySelectorAll('section').forEach(section => {
        section.classList.add('hidden');
      });

      // Show the selected section
      document.getElementById(sectionId).classList.remove('hidden');
    }

    // Wait for the splash screen to finish, then show the main content
    setTimeout(() => {
      document.querySelector('.splash-screen').style.display = 'none';
      document.querySelector('.main-content').style.display = 'block';
      showSection('home'); // Show the Home section by default
    }, 3000); // 3 seconds delay
  </script>
</body>
</html>
```

## OUTPUT
## HOME
![image](https://github.com/user-attachments/assets/799fcef9-a11b-4c01-a976-b28b19158e84)
## ABOUT US
![WhatsApp Image 2025-03-14 at 18 42 39_3f45d3ed](https://github.com/user-attachments/assets/987ae23c-14e9-45a6-bc98-a5a9047dd8b6)
## SERVICES
![WhatsApp Image 2025-03-14 at 18 43 15_18fb076c](https://github.com/user-attachments/assets/4a48236a-0e31-4243-965d-2b7139ded17a)
## CONTACT 
![image](https://github.com/user-attachments/assets/f2107c7c-2d72-467a-ab36-20a678997699)



## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
