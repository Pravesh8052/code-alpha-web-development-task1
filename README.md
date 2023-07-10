# code-alpha-web-development-task1
june batch
##landingpage.html

<!DOCTYPE html>
<html>
<head>
  <title>My Landing Page</title>
  <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
   
  <section id="home">
    <h1>Welcome to My Landing Page</h1>
    <p>This is a landing page.</p>
  </section>

  <section id="about">
    <h2>About</h2>
    <p>Some information about the company or product.</p>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <form action="contact.php" method="POST">
      <input type="text" name="name" placeholder="Your Name" required>
      <input type="email" name="email" placeholder="Your Email" required>
      <textarea name="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2023 My Landing Page. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>


###style.css


/* CSS styles for the landing page */

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header {
  background-color: #f1f1f1;
  padding: 10px;
}

nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

nav ul li {
  display: inline-block;
  margin-right: 10px;
}

nav ul li a {
  text-decoration: none;
  color: #333;
}

section {
  padding: 50px;
}

footer {
  background-color: #f1f1f1;
  padding: 10px;
  text-align: center;
}



#####contact.php

<?php
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
  $name = $_POST['name'];
  $email = $_POST['email'];
  $message = $_POST['message'];

  // Process the form data, e.g., send an email, store in a database, etc.

  // Redirect back to the landing page or show a success message
  header('Location: index.html');
  exit;
}
?>
