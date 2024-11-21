<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>For you only</title>
    <!-- Google Fonts -->
    <link
      href="https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;600&family=Open+Sans:wght@300;400;600&display=swap"
      rel="stylesheet"
    />
    <style>
      body {
        font-family: "Open Sans", sans-serif;
        margin: 0;
        padding: 0;
        background: #f7e1f2;
        color: #333;
        text-align: center;
        line-height: 1.6;
      }

      header {
        background: #dc4c94;
        color: white;
        padding: 10px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      }

      header h1 {
        font-size: clamp(2rem, 5vw, 3rem);
        margin: 0;
        font-family: "Raleway", sans-serif;
      }
      .hero-section {
        position: relative;
        height: 100vh;
        overflow: hidden;
      }

      .background-video {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        height: 100%;
        object-fit: cover;
        z-index: 1;
      }

      .hero-section .overlay {
        position: relative;
        z-index: 2;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100%;
        color: white;
        text-shadow: 0 2px 10px rgba(0, 0, 0, 0.7);
        background: rgba(
          0,
          0,
          0,
          0.3
        ); /* Optional: Add a semi-transparent overlay */
      }

      .hero-section h2 {
        font-size: 3rem;
        margin-bottom: 20px;
        animation: fadeInDown 1.2s ease;
      }

      .hero-section p {
        font-size: 1.25rem;
        max-width: 800px;
        margin: 0 auto;
        animation: fadeInUp 1.2s ease;
      }

      @keyframes fadeInDown {
        from {
          opacity: 0;
          transform: translateY(-20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      @keyframes fadeInUp {
        from {
          opacity: 0;
          transform: translateY(20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      .content {
        padding: 50px 20px;
        background: #ffffff;
        box-shadow: 0 -4px 10px rgba(0, 0, 0, 0.1);
        margin-top: -30px;
      }
      ß .content h1 {
        font-size: 3rem;
        color: #a2939a;
        margin-bottom: 20px;
      }

      .content p {
        font-size: 1.2rem;
        max-width: 800px;
        margin: 20px auto;
      }

      .button {
        background: linear-gradient(135deg, #ff66b2, #ff99cc);
        color: white;
        padding: 15px 40px;
        font-size: 1.0rem;
        font-weight: bold;
        text-transform: uppercase;
        border: none;
        border-radius: 30px;
        transition: all 0.4s ease;
        box-shadow: 0 8px 20px rgba(255, 102, 178, 0.4);
        cursor: pointer;
        position: relative;
        overflow: hidden;
      }

      .button::before {
        content: "";
        position: absolute;
        top: 0;
        left: -100%;
        width: 300%;
        height: 100%;
        background: rgba(255, 255, 255, 0.2);
        transform: skewX(-45deg);
        transition: left 0.4s ease;
      }

      .button:hover {
        background: linear-gradient(135deg, #ff85c2, #ffcce0);
        box-shadow: 0 12px 25px rgba(255, 102, 178, 0.6);
        transform: translateY(-2px);
      }

      .button:hover::before {
        left: -50%;
      }

      /* Modal (Love Letter) */
      .modal {
        display: none;
        position: fixed;
        z-index: 1;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        overflow: auto;
        background-color: rgba(0, 0, 0, 0.6);
        transition: all 0.3s ease;
      }

      .modal-content {
        background-color: #fff;
        margin: 10% auto;
        padding: 40px;
        border-radius: 12px;
        width: 80%;
        max-width: 600px;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
      }

      .close {
        color: #aaa;
        font-size: 28px;
        font-weight: bold;
        float: right;
        cursor: pointer;
      }

      .close:hover,
      .close:focus {
        color: black;
      }

      footer {
        background: #c84084;
        color: white;
        padding: 5px;
        text-align: center;
        font-size: 1rem;
        margin-top: 50px;
      }

      /* Image Gallery Section */

      .gallery img {
        width: 250px; /* Fixed width */
        height: 300px; /* Fixed height */
        object-fit: fill; /* Ensures the image covers the box, maintaining aspect ratio */
        border-radius: 10px;
        box-shadow: 0 4px 10px rgba(169, 52, 52, 0.1);
        transition: transform 0.3s ease, opacity 0.3s ease;
        margin-left: 10px;
        margin-bottom: 10px;
      }

      .gallery img:hover {
        transform: scale(1.05);
        opacity: 0.8;
        cursor: pointer;
      }

      /* Image Navigation */
      .image-navigation button {
        background: rgba(0, 0, 0, 0.7);
        color: white;
        border: none;
        font-size: 2rem;
        padding: 10px 20px;
        cursor: pointer;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
      }

      .image-navigation #prevImage {
        left: 10px;
      }
      .image-navigation #nextImage {
        right: 10px;
      }
    </style>
  </head>
  <body>
    <header>
      <h1>Happy 1st Monthsary, My Love!</h1>
    </header>

    <div class="hero-section">
      <video autoplay loop muted playsinline class="background-video">
        <source src="your-video-path.mp4" type="video/mp4" />
        Your browser does not support the video tag.
      </video>
      <div class="overlay">
        <h2>To The Love Of My Life</h2>
        <p>Every moment with you is a treasure.</p>
      </div>
    </div>

    <div class="content">
      <h1>Just for you.</h1>
      <p>
        This is just my way to express my love for you. Every day with you is
        filled with joy, laughter, and love. I'm so grateful that you came into
        my life in an unexpected way.
      </p>
      <button class="button" id="showModal">Read My Love Letter</button>

      <div class="modal" id="myModal">
        <div class="modal-content">
          <span class="close" id="closeModal">&times;</span>
          <h2>My Love Letter</h2>
          <p>My Love,</p>
          <p>
            From the moment we met, I knew that you were something special.
            These past few weeks have been a hell of a ride, and I can’t wait
            for all the beautiful moments we will continue to share. Even though
            we’ve had a few misunderstandings, we still continue to fight for
            our love and work things out as one. Every smile, every hug, and
            every glance make my heart skip a beat. You are my everything, and I
            love you so much, I can’t even explain how much I love you.
          </p>
          <p>
            Happy 1st monthsary, my love. Here's to many more months of
            happiness together.
          </p>
          <p>Forever yours,</p>
          <p><em>Kaarl Sanchez</em></p>
        </div>
      </div>
    </div>

    <!-- Image Gallery Section -->
    <div class="gallery">
      <img
        src="moment1.jpeg"
        alt="Moment 1"
        loading="lazy"
        onclick="openImageModal('moment1.jpeg')"
      />
      <img
        src="moment2.jpeg"
        alt="Moment 2"
        loading="lazy"
        onclick="openImageModal('moment2.jpeg')"
      />
      <img
        src="moment3.jpeg"
        alt="Moment 3"
        loading="lazy"
        onclick="openImageModal('moment3.jpeg')"
      />
      <img
        src="moment4.jpeg"
        alt="Moment 4"
        loading="lazy"
        onclick="openImageModal('moment4.jpeg')"
      />
      <img
        src="moment5.jpeg"
        alt="Moment 5"
        loading="lazy"
        onclick="openImageModal('moment5.jpeg')"
      />
      <img
        src="moment6.jpeg"
        alt="Moment 6"
        loading="lazy"
        onclick="openImageModal('moment6.jpeg')"
      />
      <img
        src="moment7.jpeg"
        alt="Moment 7"
        loading="lazy"
        onclick="openImageModal('moment7.jpeg')"
      />
      <img
        src="moment8.jpg"
        alt="Moment 8"
        loading="lazy"
        onclick="openImageModal('moment8.jpeg')"
      />
      <img
        src="moment9.jpeg"
        alt="Moment 9"
        loading="lazy"
        onclick="openImageModal('moment9.jpeg')"
      />
      <img
        src="moment10.jpeg"
        alt="Moment 10"
        loading="lazy"
        onclick="openImageModal('moment10.jpeg')"
      />
    </div>

    <!-- Image Modal -->
    <div id="imageModal" class="modal">
      <div class="modal-content">
        <span class="close" onclick="closeImageModal()">&times;</span>
        <img
          id="modalImage"
          src=""
          alt="Image Modal"
          style="width: 100%; border-radius: 10px"
        />
      </div>
    </div>

    <footer>
      <p>Made with love 💖</p>
    </footer>

    <script>
      // Confetti effect
      const confettiScript = document.createElement("script");
      confettiScript.src =
        "https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js";
      document.head.appendChild(confettiScript);

      // Modal functionality
      const modal = document.getElementById("myModal");
      const closeModal = document.getElementById("closeModal");
      const showModalButton = document.getElementById("showModal");

      showModalButton.onclick = function () {
        modal.style.display = "block";
        confetti({
          particleCount: 100,
          spread: 70,
          origin: { y: 0.6 },
          colors: ["#ff66b2", "#ff85c2", "#ffaad4"]
        });
      };

      closeModal.onclick = function () {
        modal.style.display = "none";
      };

      // Close modal when clicking outside of it
      window.onclick = function (event) {
        if (event.target === modal) {
          modal.style.display = "none";
        }
      };

      // Image modal functionality
      const imageModal = document.getEleßmentById("imageModal");
      const modalImage = document.getElementById("modalImage");

      function openImageModal(imageSrc) {
        modalImage.src = imageSrc;
        imageModal.style.display = "block";
      }

      function closeImageModal() {
        imageModal.style.display = "none";
      }

      document.addEventListener("keydown", function (event) {
        if (event.key === "Escape" && modal.style.display === "block") {
          modal.style.display = "none";
        }
      });
    </script>
  </body>
</html>
