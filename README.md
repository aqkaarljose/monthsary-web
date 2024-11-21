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
    <link rel="stylesheet" href="styles.css">

   
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
