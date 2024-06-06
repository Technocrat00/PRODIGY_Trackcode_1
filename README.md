# PRODIGY_Trackcode_1
//index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="navbar">
        <ul class="nav-menu">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    <div class="content">
        <section id="home"><h1>Home Section</h1></section>
        <section id="about"><h1>About Section</h1></section>
        <section id="services"><h1>Services Section</h1></section>
        <section id="contact"><h1>Contact Section</h1></section>
    </div>
    <script src="script.js"></script>
</body>
</html>

//style.css
body, html {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}

.navbar {
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    background-color: #333;
    color: white;
    padding: 1rem;
    transition: background-color 0.3s;
}

.nav-menu {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-around;
}

.nav-menu li {
    display: inline;
}

.nav-menu a {
    text-decoration: none;
    color: white;
    padding: 0.5rem 1rem;
    transition: background-color 0.3s, color 0.3s;
}

.nav-menu a:hover {
    background-color: #555;
    color: #fff;
}

.navbar.scrolled {
    background-color: #222;
}

.content {
    padding-top: 5rem;
}

section {
    height: 100vh;
    padding: 2rem;
}

//script.js
// Change navbar style on scroll
window.addEventListener('scroll', function() {
    var navbar = document.querySelector('.navbar');
    if (window.scrollY > 0) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});

// Add hover effect for menu items
var navLinks = document.querySelectorAll('.nav-menu a');
navLinks.forEach(function(link) {
    link.addEventListener('mouseenter', function() {
        this.style.backgroundColor = '#555';
        this.style.color = '#fff';
    });
    link.addEventListener('mouseleave', function() {
        this.style.backgroundColor = '';
        this.style.color = '';
    });
});
