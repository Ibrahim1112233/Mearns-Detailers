<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mearns Detailers</title>
    <style>
        /* General Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #111;
            color: white;
        }

        /* Header & Navigation */
        header {
            background-color: #222;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }

        .container {
            width: 80%;
            margin: auto;
            text-align: center;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav ul li a {
            text-decoration: none;
            color: white;
            font-weight: bold;
            padding: 10px 15px;
            transition: 0.3s;
        }

        nav ul li a:hover {
            background-color: #ff4500;
            border-radius: 5px;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: url('https://source.unsplash.com/1600x900/?car,detailing') no-repeat center center/cover;
        }

        .hero h2 {
            font-size: 3em;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.7);
        }

        button {
            background-color: #ff4500;
            color: white;
            border: none;
            padding: 12px 20px;
            font-size: 18px;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover {
            background-color: #e63900;
        }

        /* Sections */
        section {
            padding: 80px 20px;
            text-align: center;
        }

        #services ul {
            list-style: none;
            padding: 0;
        }

        #services ul li {
            background: #222;
            margin: 10px;
            padding: 15px;
            border-radius: 5px;
            display: inline-block;
            width: 30%;
        }

        /* Footer */
        footer {
            background-color: #222;
            text-align: center;
            padding: 20px;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Mearns Detailers</h1>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <section id="home" class="hero">
        <div class="container">
            <h2>Luxury Car Detailing & Protection</h2>
            <p>Expert detailing services to keep your car in pristine condition.</p>
            <button onclick="learnMore()">Learn More</button>
        </div>
    </section>
    
    <section id="services">
        <div class="container">
            <h2>Our Services</h2>
            <ul>
                <li>Paint Protection Film (PPF)</li>
                <li>Window Tinting</li>
                <li>Unit Detailing</li>
                <li>Mobile Valeting</li>
            </ul>
        </div>
    </section>
    
    <section id="about">
        <div class="container">
            <h2>About Us</h2>
            <p>At Mearns Detailers, we provide top-tier car detailing services to enhance and protect your vehicle's appearance.</p>
        </div>
    </section>
    
    <section id="contact">
        <div class="container">
            <h2>Contact Us</h2>
            <p>Email: info@mearnsdetailers.com</p>
            <p>Phone: +44 123 456 789</p>
            <p>Location: Mearns, Scotland</p>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <p>&copy; 2025 Mearns Detailers. All Rights Reserved.</p>
        </div>
    </footer>
    
    <script>
        // Smooth Scroll for Navigation
        document.querySelectorAll('nav ul li a').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({ behavior: 'smooth' });
            });
        });

        // Button Click Effect
        function learnMore() {
            alert("Welcome to Mearns Detailers! Contact us to book an appointment.");
        }
    </script>
</body>
</html>
