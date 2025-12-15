<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Madja-as Park Guide App</title>
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: "Poppins", Arial, sans-serif;
      color: white;
      text-align: center;
      overflow-y: auto;
      overflow-x: hidden;
      background-color: black;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(1.02); }
      to { opacity: 1; transform: scale(1); }
    }

    section {
      position: absolute;
      top: 0;
      left: 0;
      min-height: 100vh;
      width: 100%;
      background-size: cover;
      background-position: center;
      display: none;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 40px 20px;
      opacity: 0;
      transition: opacity 0.6s ease-in-out;
    }

    section.active {
      display: flex;
      z-index: 1;
      animation: fadeIn 0.8s ease forwards;
      opacity: 1;
    }

    h1 {
      font-size: 36px;
      font-weight: 700;
      text-shadow: 3px 3px 8px rgba(0, 0, 0, 0.8);
      margin-bottom: 25px;
    }

    h2 {
      font-size: 28px;
      font-weight: 700;
      margin-bottom: 15px;
      text-shadow: 3px 3px 8px rgba(0, 0, 0, 0.9);
    }

    p {
      font-size: 18px;
      line-height: 1.7;
      text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.8);
      max-width: 700px;
      margin-bottom: 20px;
    }

    button, a {
      display: block;
      width: 220px;
      margin: 10px auto;
      padding: 14px;
      font-size: 17px;
      font-weight: bold;
      border: none;
      border-radius: 30px;
      background-color: rgba(0, 102, 255, 0.9);
      color: white;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
      text-decoration: none;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
    }

    button:hover, a:hover {
      background-color: rgba(0, 102, 255, 1);
      transform: scale(1.05);
    }

    iframe {
      width: 90%;
      height: 60%;
      border: none;
      border-radius: 15px;
      margin-top: 20px;
      box-shadow: none;
      background: none;
    }

    input, textarea {
      width: 250px;
      margin: 10px;
      padding: 10px;
      border-radius: 10px;
      border: none;
      font-size: 15px;
      text-align: center;
    }

    form {
      background: rgba(0, 0, 0, 0.5);
      padding: 25px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.7);
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .gallery-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin-top: 20px;
    }

    .gallery-container img {
      width: 150px;
      height: 150px;
      border-radius: 10px;
      object-fit: cover;
      box-shadow: 0 0 10px rgba(0,0,0,0.7);
      transition: transform 0.3s;
    }

    .gallery-container img:hover {
      transform: scale(1.1);
    }

    /* ✅ Portrait video */
    video {
      width: 220px;
      height: 360px;
      margin-top: 20px;
      border-radius: 15px;
      box-shadow: 0 0 10px rgba(0,0,0,0.7);
    }

  </style>
</head>
<body>

  <section id="home" class="active" style="background-image: url(/Gemini_Generated_Image_b7a5n2b7a5n2b7a5.png);">
    <div>
      <h1>MADJA-AS PARK GUIDE APP</h1>
      <button onclick="showScreen('about')">About</button>
      <button onclick="showScreen('gallery')">Gallery</button>
      <button onclick="showScreen('location')">Location</button>
      <button onclick="showScreen('contact')">Contact Us</button>
    </div>
  </section>

  <section id="about" style="background-image: url(/1760607171804.jpg);">
    <div>
      <h2>About Madja-as Park</h2>
      <p>Madja-as Park is a scenic eco-tourism destination located in Culasi, Antique. 
         It is known for its refreshing mountain breeze, peaceful surroundings, 
         and relaxing ambiance perfect for family outings and nature lovers.</p>
      <p>The park features beautiful landscapes, walking trails, and local art 
         installations that reflect the rich culture and heritage of Antique. 
         Visitors can enjoy picnics, sightseeing, and photography amidst nature’s beauty.</p>
      <p>Madja-as Park serves as a reminder to preserve and appreciate the 
         environment while providing a space for recreation and learning for all ages.</p>
      <button onclick="showScreen('home')">Back to Home</button>
    </div>
  </section>

  <section id="gallery" style="background-image: url(/1760605620547.jpg);">
    <div>
      <h2>Gallery</h2>
      <p>Take a look at some of the best attractions inside Madja-as Park!</p>

      <div class="gallery-container">
        <img src="/IMG_20250405_174322.jpg" alt="Madja-as Entrance">
        <img src="/IMG_20250405_165415_491@-1148081188.jpg" alt="View Tower">
        <img src="/1760607698423.jpg" alt="Flower Garden">
        <img src="/IMG_20250405_160530.jpg" alt="Hanging Bridge">
        <img src="/1760607717529.jpg" alt="Sunset Point">
        <img src="/IMG_20250405_170136.jpg" alt="Picnic Area">
        <img src="/IMG_20250405_171425.jpg" alt="Art Zone">
        <img src="/IMG_20250405_165414.jpg" alt="Walk Trail">
      </div>

      <video controls>
        <source src="/Messenger_creation_9844127F-9FD5-4676-B454-B3A55A145C2C.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>

      <button onclick="showScreen('home')">Back to Home</button>
    </div>
  </section>

  <section id="location" style="background-image: url('/IMG_20251012_152248.jpg');">
    <div>
      <h2>Madja-as Park Location</h2>
      <p>Find us easily using Google Maps! Madja-as Park is located in a scenic area surrounded by mountains and nature.</p>
      <iframe 
        src=""
        allowfullscreen="" loading="lazy">
      </iframe>
      <p>📍 Google Map:
      https://maps.app.goo.gl/Ddbh3XryzVPgmAUW6</p>
      <p>🕒 Open Hours: 7:00 AM - 6:00 PM (Daily)</p>
      <button onclick="showScreen('home')">Back to Home</button>
    </div>
  </section>

  <section id="contact" style="background-image: url('/IMG_20251012_155035.jpg');">
    <form>
      <h2>Contact Information</h2>
      <p>If you have questions, feedback, or inquiries, please reach out to us below.</p>
      <input type="text" placeholder="Your Name" required /><br />
      <input type="email" placeholder="Your Email" required /><br />
      <textarea placeholder="Your Message" rows="4"></textarea><br />
      <button type="submit">Send</button><br />
      <p>📞 Phone: +63 912 345 6789</p>
      <p>📧 Email: info@madjaaspark.com</p>
      <p>📍 Address: Madja-as Eco Park, Culasi, Antique</p>
      <button type="button" onclick="showScreen('home')">Back to Home</button>
    </form>
  </section>

  <script>
    function showScreen(screenId) {
      document.querySelectorAll('section').forEach(sec => {
        sec.classList.remove('active');
        sec.style.opacity = 0;
      });
      const activeSec = document.getElementById(screenId);
      if (activeSec) {
        activeSec.classList.add('active');
        window.scrollTo({ top: 0, behavior: "smooth" });
      } else {
        console.error("Section not found:", screenId);
      }
    }
  </script>

</body>
</html>
