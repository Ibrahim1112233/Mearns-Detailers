<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mearns Detailers</title>
    <link rel="stylesheet" href="style.css">
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
            margin: 0 25px; /* Increased margin around links */
        }

        nav ul li a {
            text-decoration: none;
            color: white;
            font-weight: bold;
            padding: 15px 25px; /* Increased padding around links */
            transition: 0.3s;
        }

        nav ul li a:hover {
            background-color: #38B6FF;
            border-radius: 5px;
        }

        /* Button Styles */
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
            background-color: #38B6FF;
        }

        /* Widget Banner */
        .widget-banner {
            background-color: #38B6FF;
            padding: 20px;
            text-align: center;
            margin-top: 80px; /* Adjusted to account for fixed header */
        }

        .widget-banner h2 {
            margin: 0;
            font-size: 24px;
            color: white;
        }

        /* Widget Container */
        .widget-container {
            background-color: #F4F8FB;
            padding: 20px;
            margin: 20px auto;
            max-width: 800px;
            border-radius: 15px;
            box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.1);
        }

        .widget-container h1 {
            color: #333;
            font-size: 28px;
            margin-bottom: 20px;
        }

        .widget-container label {
            font-weight: 600;
            display: block;
            margin-top: 15px;
            color: #555;
        }

        .widget-container select, .widget-container button, .widget-container input {
            width: 100%;
            padding: 12px;
            margin-top: 8px;
            border: 2px solid #38B6FF;
            border-radius: 8px;
            font-size: 16px;
            background: white;
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
        }

        .widget-container select:focus, .widget-container input:focus {
            border-color: #2B92E4;
            box-shadow: 0px 0px 8px rgba(43, 146, 228, 0.5);
            outline: none;
        }

        .widget-container button {
            background-color: #38B6FF;
            color: white;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }

        .widget-container button:hover {
            background-color: #2B92E4;
            transform: scale(1.05);
        }

        .widget-container .dropdown {
            position: relative;
            width: 100%;
            margin: 10px 0;
        }

        .widget-container .dropdown-content {
            display: none;
            position: absolute;
            background-color: white;
            border: 2px solid #38B6FF;
            width: 100%;
            text-align: left;
            max-height: 300px;
            overflow-y: auto;
            border-radius: 8px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            z-index: 1;
            transition: opacity 0.3s ease, transform 0.3s ease;
            opacity: 0;
            transform: translateY(-10px);
        }

        .widget-container .dropdown-content.show {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }

        .widget-container .dropdown-content div {
            padding: 12px;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .widget-container .dropdown-content div:hover {
            background-color: #E6F4FF;
        }

        .widget-container .selected {
            font-weight: bold;
            color: #38B6FF;
            background-color: #E6F4FF;
        }

        .widget-container #quote-result {
            font-size: 28px;
            font-weight: bold;
            margin-top: 20px;
            color: #38B6FF;
            padding: 15px;
            background-color: #E6F4FF;
            border-radius: 12px;
            transition: opacity 0.3s ease-in-out, transform 0.3s ease-in-out;
            border: 2px solid black;
            box-shadow: 0px 0px 15px rgba(56, 182, 255, 0.6), 
                        0px 0px 40px rgba(56, 182, 255, 0.3);
        }

        .widget-container #quote-result:hover {
            transform: scale(1.05);
            box-shadow: 0px 0px 20px rgba(56, 182, 255, 0.9), 
                        0px 0px 50px rgba(56, 182, 255, 0.5);
        }

        .widget-container .input-group {
            padding: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .widget-container .input-group label {
            flex: 1;
            text-align: left;
            color: #555;
        }

        .widget-container .input-group input {
            flex: 0.5;
            text-align: center;
        }

        .widget-container .highlight {
            color: #000;
            font-weight: bold;
            background-color: #FFD700;
            padding: 5px 10px;
            border-radius: 5px;
        }

        .widget-container .image-container {
            display: none;
            justify-content: space-between;
            margin-top: 20px;
        }

        .widget-container .image-container img {
            width: 48%;
            border-radius: 8px;
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
    
    <!-- Widget Banner -->
    <div class="widget-banner">
        <h2>Get Your Free Quote Now!</h2>
    </div>

    <!-- Widget Container -->
    <div class="widget-container">
        <h1>Get Your Free Quote!</h1>

        <label for="service">Choose a Service <span class="required">*</span>:</label>
        <select id="service">
            <option value="">-- Select a Service --</option>
            <option value="exterior">Exterior Detail</option>
            <option value="interior">Interior Detail</option>
            <option value="mini_valet">Mini Valet</option>
            <option value="full_detail">Full Detail</option>
            <option value="maintenance">Maintenance Package (Only available after a Mini Valet or Full Detail)</option>
            <option value="ceramic_1">Ceramic Coating (1 Year)</option>
            <option value="ceramic_2">Ceramic Coating (2 Year)</option>
            <option value="ceramic_3">Ceramic Coating (3 Year)</option>
            <option value="gloss_enhancement">Gloss Enhancement Polish</option>
            <option value="paint_correction_1">1-Step Paint Correction (Estimate)</option>
            <option value="paint_correction_2">2-Step Paint Correction (Estimate)</option>
        </select>

        <label for="brand">Choose a Car Brand <span class="required">*</span>:</label>
        <select id="brand" onchange="updateModels()">
            <option value="">-- Select a Brand --</option>
        </select>

        <label for="model">Choose a Car Model <span class="required">*</span>:</label>
        <select id="model">
            <option value="">-- Select a Model --</option>
        </select>

        <label>Choose Additional Services (Optional):</label>
        <div class="dropdown">
            <button type="button" onclick="toggleDropdown()">Select Additional Services</button>
            <div class="dropdown-content" id="additional-services">
                <div class="input-group">
                    <label>Seats for Stain Removal (£10 per seat):</label>
                    <input type="number" id="seat_count" min="0" value="0">
                </div>
                <div class="input-group">
                    <label>Footwells for Stain Removal (£10 per footwell):</label>
                    <input type="number" id="footwell_count" min="0" value="0">
                </div>
                <div onclick="toggleService(this, 'clay_bar')">Chemical Decontamination and Clay Bar Treatment (£25)</div>
                <div onclick="toggleService(this, 'wax_coating')">Wax Coating (£10)</div>
                <div onclick="toggleService(this, 'ceramic_sealant')">Ceramic Sealant (£20)</div>
                <div onclick="toggleService(this, 'leather_conditioning')">Leather Conditioning (£10)</div>
                <div onclick="toggleService(this, 'odour_removal')">Odour Removal (£10)</div>
                <div onclick="toggleService(this, 'premium_scent')">Premium Car Scent (£5)</div>
            </div>
        </div>

        <button onclick="getQuote()">Get Quote</button>

        <div id="quote-result"></div>
        
        <!-- Before-and-after images for exterior detailing -->
        <div class="image-container" id="exterior-images">
            <img src="https://i.imgur.com/oREYw5e.jpeg" alt="Before Exterior Detailing" style="height: 250px">
            <img src="https://i.imgur.com/HBXm0cp.jpeg" alt="After Exterior Detailing" style="height: 250px">
        </div>

        <!-- Before-and-after images for interior detailing -->
        <div class="image-container" id="interior-images">
            <img src="https://i.imgur.com/fNfHupM.jpeg" alt="Before Interior Detailing" style="height: 250px">
            <img src="https://i.imgur.com/8eCngD8.jpeg" alt="After Interior Detailing" style="height: 250px">
        </div>

        <!-- Images for mini valet -->
        <div class="image-container" id="mini-valet-images">
            <img src="https://i.imgur.com/RAyB52U.jpeg" alt="Mini Valet Before" style="height: 200px">
            <img src="https://images.pexels.com/photos/6873123/pexels-photo-6873123.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" alt="Mini Valet After" style="height: 200px">
        </div>

        <!-- Images for full detail -->
        <div class="image-container" id="full-detail-images">
            <img src="https://cavallistables.com/wp-content/uploads/2020/09/professional-car-detailing-1200x675.jpg" alt="Full Detail Before" style="height: 200px">
            <img src="https://www.mycarcleaning.co.uk/cdn/shop/articles/Copy_of__P7A1812.jpg?v=1731945751&width=1000" alt="Full Detail After" style="height: 200px">
        </div>

        <!-- Images for maintenance package -->
        <div class="image-container" id="maintenance-images">
            <img src="https://i.ytimg.com/vi/fpjtukJpOy4/hq720.jpg?sqp=-oaymwEhCK4FEIIDSFryq4qpAxMIARUAAAAAGAElAADIQj0AgKJD&rs=AOn4CLDCRknNlMN8jBrg4s6IDcMkqmsVBA" alt="Maintenance Package" style="height: 180px">
            <img src="https://cdn.shopify.com/s/files/1/0797/2968/8869/files/spJnSTldAQfhvwo5aE4VYCw060rUDmfTb5Ngx5vI.jpg?v=1737641076&width=1620&height=1080" alt="Maintenance Package" style="height: 180px">
        </div>

        <!-- Images for ceramic coating (1 year) -->
        <div class="image-container" id="ceramic-1-images">
            <img src="https://carspecialistcustoms.co.uk/wp-content/uploads/2023/11/shutterstock_2271145909.jpg" alt="Ceramic Coating 1 Year" style="height: 200px">
            <img src="https://cdn.prod.website-files.com/5ce681ae5375caf5729444b1/5d2f2c8a46b3c512285e9312_5ceaa3de7a0da80ba6649221_58375556_2276839995706795_2425296452126244864_o-1.jpg" alt="Ceramic Coating 1 Year" style="height: 200px">
        </div>

        <!-- Images for ceramic coating (2 year) -->
        <div class="image-container" id="ceramic-2-images">
            <img src="https://www.huntsmiths.co.uk/wp-content/uploads/Gyeon-Beading.jpeg" alt="Ceramic Coating 2 Year" style="height: 200px">
            <img src="https://media.istockphoto.com/id/1434542471/photo/process-of-applying-ceramic-protective-coat-on-body-car-using-sponge-in-detailing-auto.jpg?s=612x612&w=0&k=20&c=csC-5vvQDqAzjGLvEcrR-yShuGwb-9J9uCGfEGjvfM4=" alt="Ceramic Coating 2 Year" style="height: 200px">
        </div>

        <!-- Images for ceramic coating (3 year) -->
        <div class="image-container" id="ceramic-3-images">
            <img src="https://i.imgur.com/4XZJQ9H.jpeg" alt="Ceramic Coating 3 Year" style="height: 250px">
        </div>

        <!-- Images for gloss enhancement polish -->
        <div class="image-container" id="gloss-enhancement-images">
            <img src="https://i.imgur.com/5XZJQ9I.jpeg" alt="Gloss Enhancement Polish" style="height: 250px">
        </div>

        <!-- Images for 1-step paint correction -->
        <div class="image-container" id="paint-correction-1-images">
            <img src="https://i.imgur.com/6XZJQ9J.jpeg" alt="1-Step Paint Correction" style="height: 250px">
        </div>

        <!-- Images for 2-step paint correction -->
        <div class="image-container" id="paint-correction-2-images">
            <img src="https://i.imgur.com/7XZJQ9K.jpeg" alt="2-Step Paint Correction" style="height: 250px">
        </div>
    </div>

    <footer>
        <div class="container">
            <p>&copy; 2025 Mearns Detailers. All Rights Reserved.</p>
        </div>
    </footer>
    
    <script>
        const carBrands = {
            "Alfa Romeo": { "Giulia": "medium", "Stelvio": "large", "Tonale": "medium" },
            "Aston Martin": { "DB11": "large", "DBS": "large", "Vantage": "medium", "DBX": "large-7" },
            "Audi": { "A1": "small", "A3": "medium", "A4": "medium", "A6": "large", "A8": "large", "Q2": "small", "Q3": "medium", "Q5": "large", "Q7": "large-7", "Q8": "large-7", "R8": "large", "RS3": "medium", "RS6": "large" },
            "Bentley": { "Bentayga": "large-7", "Continental GT": "large", "Flying Spur": "large", "Mulsanne": "large" },
            "BMW": { "1 Series": "small", "2 Series": "medium", "3 Series": "medium", "4 Series": "medium", "5 Series": "large", "7 Series": "large", "X1": "small", "X3": "medium", "X5": "large", "X7": "large-7", "i3": "small", "i4": "medium", "iX3": "medium", "iX": "large" },
            "Bugatti": { "Chiron": "large", "Divo": "large", "Veyron": "large" },
            "Chevrolet": { "Camaro": "large", "Corvette": "large", "Spark": "small", "Malibu": "medium" },
            "Citroen": { "C1": "small", "C3": "small", "C4": "medium", "C5 Aircross": "large", "Berlingo": "large-7", "Grand C4 SpaceTourer": "large-7" },
            "Dacia": { "Duster": "large", "Jogger": "large-7", "Logan": "medium", "Sandero": "small" },
            "Ferrari": { "296 GTB": "large", "488 Pista": "large", "812 Superfast": "large", "F8 Tributo": "large", "LaFerrari": "large", "SF90 Stradale": "large" },
            "Fiat": { "500": "small", "500L": "medium", "500X": "medium", "Doblo": "large-7", "Panda": "small", "Tipo": "medium" },
            "Ford": { "Edge": "large", "Fiesta": "small", "Focus": "medium", "Galaxy": "large-7", "Ka+": "small", "Kuga": "large", "Mondeo": "large", "Mustang": "large", "S-Max": "large-7" },
            "Honda": { "Accord": "large", "Civic": "medium", "CR-V": "large", "HR-V": "medium", "Jazz": "small", "Pilot": "large-7" },
            "Hyundai": { "i10": "small", "i20": "small", "i30": "medium", "i40": "large", "Kona": "medium", "Palisade": "large-7", "Santa Fe": "large-7", "Tucson": "large" },
            "Jaguar": { "F-Pace": "large", "F-Type": "large", "I-Pace": "large", "XE": "medium", "XF": "large", "XJ": "large-7" },
            "Kia": { "Ceed": "medium", "Niro": "medium", "Optima": "large", "Picanto": "small", "Rio": "small", "Sorento": "large-7", "Sportage": "large", "Stonic": "medium" },
            "Lamborghini": { "Aventador": "large", "Huracán": "large", "Revuelto": "large", "Sian FKP 37": "large", "Centenario": "large", "Veneno": "large", "Reventón": "large", "Murciélago": "large", "Diablo": "large", "Gallardo": "medium", "Urus": "large-7", "SC20": "large", "SC18 Alston": "large", "Essenza SCV12": "large", "Lanzador": "large", "Terzo Millennio": "large" },
            "Land Rover": { "Defender 110": "large-7", "Defender 90": "large", "Discovery": "large-7", "Discovery Sport": "large", "Range Rover": "large-7", "Range Rover Evoque": "medium", "Range Rover Sport": "large" },
            "Mazda": { "CX-30": "medium", "CX-5": "large", "CX-9": "large-7", "Mazda2": "small", "Mazda3": "medium", "Mazda6": "large" },
            "McLaren": { "570S": "large", "600LT": "large", "720S": "large", "Artura": "large", "P1": "large" },
            "Mercedes": { "A-Class": "small", "B-Class": "medium", "C-Class": "medium", "E-Class": "large", "GLA": "small", "GLB": "medium", "GLC": "medium", "GLE": "large", "GLS": "large-7", "V-Class": "large-7" },
            "Nissan": { "Ariya": "large", "GT-R": "large", "Juke": "medium", "Leaf": "medium", "Micra": "small", "Qashqai": "medium", "X-Trail": "large-7" },
            "Peugeot": { "108": "small", "208": "small", "2008": "medium", "308": "medium", "3008": "large", "508": "large", "5008": "large-7" },
            "Porsche": { "911": "large", "Cayenne": "large-7", "Macan": "large", "Panamera": "large", "Taycan": "large" },
            "Renault": { "Captur": "medium", "Clio": "small", "Espace": "large-7", "Kadjar": "large", "Koleos": "large", "Megane": "medium", "Talisman": "large", "Twingo": "small" },
            "Tesla": { "Model 3": "medium", "Model S": "large", "Model X": "large-7", "Model Y": "large" },
            "Toyota": { "Aygo": "small", "C-HR": "medium", "Camry": "large", "Corolla": "medium", "Highlander": "large-7", "Land Cruiser": "large-7", "RAV4": "large", "Yaris": "small" },
            "Vauxhall": { "Astra": "medium", "Corsa": "small", "Grandland": "large", "Insignia": "large", "Mokka": "medium", "Vivaro": "large-7", "Zafira": "large-7" },
            "Volkswagen": { "Golf": "medium", "ID.3": "medium", "ID.4": "large", "Polo": "small", "T-Roc": "medium", "Tiguan": "large", "Touareg": "large-7", "Up!": "small" },
            "Volvo": { "S60": "medium", "S90": "large", "V60": "medium", "V90": "large", "XC40": "medium", "XC60": "large", "XC90": "large-7" }
        };

        const servicePrices = {
            "exterior": { small: 45, medium: 50, large: 55, "large-7": 55 },
            "interior": { small: 55, medium: 60, large: 65, "large-7": 70 },
            "mini_valet": { small: 65, medium: 70, large: 75, "large-7": 80 },
            "full_detail": { small: 100, medium: 110, large: 120, "large-7": 130 },
            "maintenance": { small: 40, medium: 50, large: 60, "large-7": 65 },
            "ceramic_1": { small: 100, medium: 110, large: 120, "large-7": 120 },
            "ceramic_2": { small: 140, medium: 150, large: 160, "large-7": 160 },
            "ceramic_3": { small: 180, medium: 190, large: 200, "large-7": 200 },
            "gloss_enhancement": { small: 120, medium: 140, large: 150, "large-7": 150 },
            "paint_correction_1": { small: 250, medium: 270, large: 300, "large-7": 300 },
            "paint_correction_2": { small: 400, medium: 430, large: 450, "large-7": 450 }
        };

        const additionalServicePrices = {
            "clay_bar": 25,
            "wax_coating": 15,
            "ceramic_sealant": 15,
            "leather_conditioning": 10,
            "odour_removal": 10,
            "premium_scent": 5
        };

        let selectedAdditionalServices = new Set();

        function populateBrands() {
            const brandSelect = document.getElementById("brand");
            Object.keys(carBrands).forEach(brand => {
                brandSelect.innerHTML += `<option value="${brand}">${brand}</option>`;
            });
        }

        function updateModels() {
            const brand = document.getElementById("brand").value;
            const modelSelect = document.getElementById("model");
            modelSelect.innerHTML = '<option value="">-- Select a Model --</option>';
            if (brand && carBrands[brand]) {
                Object.keys(carBrands[brand]).forEach(model => {
                    modelSelect.innerHTML += `<option value="${model}">${model}</option>`;
                });
            }
        }

        function toggleDropdown() {
            const dropdown = document.getElementById("additional-services");
            dropdown.classList.toggle("show");
        }

        function toggleService(element, serviceId) {
            element.classList.toggle("selected");
            if (selectedAdditionalServices.has(serviceId)) {
                selectedAdditionalServices.delete(serviceId);
            } else {
                selectedAdditionalServices.add(serviceId);
            }
        }

        function getQuote() {
            const service = document.getElementById("service").value;
            const brand = document.getElementById("brand").value;
            const model = document.getElementById("model").value;

            if (!service || !brand || !model) {
                alert("Please select a service, brand, and model.");
                return;
            }

            const carSize = carBrands[brand][model];
            const basePrice = servicePrices[service][carSize];

            let additionalPrice = 0;
            selectedAdditionalServices.forEach(serviceId => {
                additionalPrice += additionalServicePrices[serviceId];
            });

            const seatCount = parseInt(document.getElementById("seat_count").value) || 0;
            const footwellCount = parseInt(document.getElementById("footwell_count").value) || 0;
            additionalPrice += (seatCount * 10) + (footwellCount * 10);

            const totalPrice = basePrice + additionalPrice;
            document.getElementById("quote-result").innerHTML = `Your Quote: <span class="total-price">£${totalPrice}</span>`;

            // Hide all image containers
            const imageContainers = document.querySelectorAll(".image-container");
            imageContainers.forEach(container => {
                container.style.display = "none";
            });

            // Show the relevant image container based on the selected service
            const serviceImages = document.getElementById(`${service.replace(/_/g, "-")}-images`);
            if (serviceImages) {
                serviceImages.style.display = "flex";
            }
        }

        populateBrands();
    </script>
</body>
</html>
