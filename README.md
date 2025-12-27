<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>D Konsult Blog Carousel</title>

  <!-- Tailwind -->
  <script src="https://cdn.tailwindcss.com"></script>

  <style>
    /* Floating Button */
    .floating-btn {
      position: fixed;
      top: 20px;
      right: 20px;
      z-index: 50;
      background-color: #16a34a;
      color: white;
      padding: 12px 22px;
      border-radius: 9999px;
      font-weight: bold;
      box-shadow: 0 10px 15px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease, opacity 0.3s ease;
    }

    /* Hidden state */
    .floating-btn.hide {
      transform: translateY(-80px);
      opacity: 0;
      pointer-events: none;
    }
  </style>
</head>

<body class="bg-gray-50 font-sans">

  <!-- CONTENT -->
  <section class="p-4 max-w-5xl mx-auto">
    <h1 class="text-3xl font-bold text-center text-gray-800 mb-6">
      Explore D Konsult Highlights
    </h1>

    <p class="text-center text-gray-600 mb-10">
      D Konsult offers resources tailored for both beginners and seasoned professionals.
      Whether you're looking to enhance productivity, delve into AI applications, or
      kickstart your online business journey, D Konsult serves as your trusted companion
      in the evolving digital landscape.
    </p>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">

      <!-- CARD 1 -->
      <div class="bg-white rounded-xl overflow-hidden shadow-md">
        <img
          src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/12/imagine_15462143230908918843052169799993526.jpg"
          class="w-full h-48 object-cover"
        >
        <div class="p-4">
          <h2 class="font-semibold text-lg mb-2">What’s New</h2>
          <p class="text-sm text-gray-600 mb-4">
            Unlock your digital potential with AI-powered guides and tools.
          </p>
          <a
            href="https://beatzde4.blogspot.com/p/advertise-online-for-free.html"
            target="_blank"
            class="text-green-600 font-bold"
          >
            Home →
          </a>
        </div>
      </div>

      <!-- Add more cards here (2–10) -->

    </div>
  </section>

  <!-- FLOATING BUTTON -->
  <a
    id="floatingBtn"
    class="floating-btn"
    href="https://beatzde4.blogspot.com/p/advertise-online-for-free.html"
    target="_blank"
  >
    All Resources
  </a>

  <!-- AUTO-HIDE ON SCROLL SCRIPT -->
  <script>
    let lastScrollY = window.scrollY;
    const btn = document.getElementById("floatingBtn");

    window.addEventListener("scroll", () => {
      if (window.scrollY > lastScrollY) {
        // scrolling down → hide
        btn.classList.add("hide");
      } else {
        // scrolling up → show
        btn.classList.remove("hide");
      }
      lastScrollY = window.scrollY;
    });
  </script>

</body>
</html>
