<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Undangan Niko & Auliya</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
  <style>
    body {
      background: url('attached_assets/Untitled39_20250523070856.png') no-repeat center center fixed;
      background-size: cover;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    .rain {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      background-image: url('https://i.imgur.com/NM3hE4L.png');
      animation: rain 0.5s linear infinite;
    }
    @keyframes rain {
      0% {background-position: 0 0;}
      100% {background-position: 0 100%;}
    }
  </style>
</head>
<body class="relative text-white">
  <div class="rain"></div>
  <div class="min-h-screen flex flex-col justify-center items-center text-center px-4">
    <h1 class="text-4xl font-bold mb-4" data-aos="fade-down">Niko Rahmadi Wiharto & Nur Auliya Widjaja</h1>
    <p class="mb-4 italic" data-aos="fade-up">
      “As twilight falls and rain softly graces the earth, may love and imān bloom in our hearts—bathed in the quiet mercy of the Most Loving.”
    </p>
    <p class="text-sm" data-aos="fade-up">
      اللهم اجعل بيوتنا رياضًا من رياض الجنة، واسقها بماء الرحمة والسكينة والبركة
    </p>
    <div id="countdown" class="text-2xl font-mono my-6 animate-pulse" data-aos="zoom-in"></div>
    <a href="#location" class="bg-indigo-400 hover:bg-indigo-500 px-6 py-2 rounded-lg text-white font-bold transition duration-300 mb-4" data-aos="zoom-in-up">Lihat Lokasi</a>
    <button onclick="scrollToForm()" class="bg-amber-400 hover:bg-amber-500 px-6 py-2 rounded-lg text-gray-900 font-bold transition duration-300" data-aos="zoom-in-up">Isi RSVP</button>
  </div>

  <div id="location" class="bg-white text-black py-12 px-4">
    <h2 class="text-2xl font-bold text-center mb-6" data-aos="fade-up">Lokasi Acara</h2>
    <div class="max-w-xl mx-auto" data-aos="zoom-in">
      <iframe src="https://www.google.com/maps?q=-7.578814,110.829775&hl=id&z=17&output=embed" width="100%" height="400" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
      <p class="text-center mt-2"><a href="https://g.co/kgs/Z65rGa9" target="_blank" class="text-blue-600 underline">Buka di Google Maps</a></p>
    </div>
  </div>

  <div id="form" class="bg-white text-black py-12 px-4 mt-12">
    <h2 class="text-2xl font-bold text-center mb-6" data-aos="fade-up">Form Konfirmasi Kehadiran</h2>
    <form class="max-w-md mx-auto" name="rsvp-form" action="https://formspree.io/f/xqkrvnod" method="POST">
      <input type="text" name="nama" placeholder="Nama Anda" class="w-full mb-4 p-2 border rounded" required>
      <input type="email" name="email" placeholder="Email (opsional)" class="w-full mb-4 p-2 border rounded">
      <select name="kehadiran" class="w-full mb-4 p-2 border rounded">
        <option value="Hadir">Hadir, insyaAllah</option>
        <option value="Berhalangan">Berhalangan hadir</option>
      </select>
      <button type="submit" class="bg-green-500 hover:bg-green-600 w-full py-2 rounded text-white transition duration-300">Kirim</button>
    </form>
  </div>

  <div id="kesan-pesan" class="bg-gray-100 text-black py-12 px-4">
    <h2 class="text-2xl font-bold text-center mb-6" data-aos="fade-up">Kesan & Pesan untuk Mempelai</h2>
    <form class="max-w-xl mx-auto" name="kesan-pesan-form" action="https://formspree.io/f/mleqvpor" method="POST">
      <input type="text" name="nama" placeholder="Nama Anda" class="w-full mb-4 p-2 border rounded" required>
      <textarea name="pesan" rows="4" placeholder="Tulis kesan atau doa untuk mempelai..." class="w-full mb-4 p-2 border rounded" required></textarea>
      <button type="submit" class="bg-purple-600 hover:bg-purple-700 w-full py-2 rounded text-white transition duration-300">Kirim Pesan</button>
    </form>
  </div>

  <footer class="text-center text-xs text-white bg-black bg-opacity-40 py-4">
    <p>© 2025 Invitation. Design by Niko & Auliya. All rights reserved.</p>
    <p class="mt-2">Contact: <a href="https://wa.me/6281234567890" class="underline text-green-300">WhatsApp Admin</a></p>
    <p class="mt-2">Musik: <a href="https://soundcloud.com/relaxing-white-noise/rain-in-the-woods-sleep-sound-5-hours" target="_blank" class="underline text-blue-300">Rain</a></p>
  </footer>

  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script>
    AOS.init();

    // Countdown Timer
    const eventDate = new Date("2025-08-01T00:00:00").getTime();
    const countdown = document.getElementById("countdown");
    setInterval(() => {
      const now = new Date().getTime();
      const distance = eventDate - now;

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      countdown.innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;
    }, 1000);

    // Scroll to form
    function scrollToForm() {
      document.getElementById("form").scrollIntoView({ behavior: "smooth" });
    }
  </script>
</body>
</html>
