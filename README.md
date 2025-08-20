
<html lang="id">                            <!-- Splash Screen Awal -->
<div id="splashScreen">
  <div id="splashContent">
    <h1>Welcome to the World of Espers</h1>
    <button onclick="enterWorld()">Jelajahi Dunia Esper</button>
  </div>
</div>

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Esper World</title>
  <style>
    body {    /* Splash Screen */
#splashScreen {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(270deg, #000428, #004e92);
  background-size: 400% 400%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  color: cyan;
  z-index: 2000;
  animation: gradientBG 15s ease infinite;
}

#splashScreen h1 {
  font-size: 3rem;
  text-shadow: 0 0 15px cyan;
  margin-bottom: 2rem;
}

#splashScreen button {
  background: transparent;
  border: 2px solid cyan;
  color: cyan;
  padding: 1rem 2rem;
  border-radius: 12px;
  font-size: 1.2rem;
  cursor: pointer;
  transition: all 0.3s;
}

#splashScreen button:hover {
  background: cyan;
  color: black;
  box-shadow: 0 0 15px cyan;
}
                
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      background: linear-gradient(270deg, #000428, #004e92);
      background-size: 400% 400%;
      color: #fff;
      overflow-x: hidden;
      animation: gradientBG 15s ease infinite;
    }

    @keyframes gradientBG {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }

    header {
      text-align: center;
      padding: 2rem;
      font-size: 2rem;
      letter-spacing: 2px;
      color: cyan;
      text-shadow: 0 0 15px cyan;
      position: relative;
      overflow: hidden;
    }

    header::before, header::after {
      content: "🌌 Esper World Interface 🌌";
      position: absolute;
      left: 0;
      right: 0;
      color: cyan;
      overflow: hidden;
      clip: rect(0, 900px, 0, 0);
    }
    header::before {
      animation: glitchTop 2s infinite linear alternate-reverse;
      color: #ff00c1;
    }
    header::after {
      animation: glitchBot 3s infinite linear alternate-reverse;
      color: #00fff9;
    }
    @keyframes glitchTop {
      0% { clip: rect(0, 9999px, 0, 0); }
      20% { clip: rect(0, 9999px, 10px, 0); transform: translate(-5px, -2px);}
      40% { clip: rect(0, 9999px, 5px, 0); transform: translate(3px, 2px);}
      60% { clip: rect(0, 9999px, 8px, 0); transform: translate(-2px, 0);}
      80% { clip: rect(0, 9999px, 3px, 0); transform: translate(1px, -1px);}
      100% { clip: rect(0, 9999px, 0, 0);}
    }
    @keyframes glitchBot {
      0% { clip: rect(0, 9999px, 0, 0);}
      20% { clip: rect(15px, 9999px, 25px, 0); transform: translate(5px,2px);}
      40% { clip: rect(10px, 9999px, 20px, 0); transform: translate(-3px, -1px);}
      60% { clip: rect(5px, 9999px, 15px, 0); transform: translate(2px,1px);}
      80% { clip: rect(20px, 9999px, 30px, 0); transform: translate(-1px,0);}
      100% { clip: rect(0, 9999px, 0, 0);}
    }

    nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
      margin-bottom: 2rem;
      backdrop-filter: blur(8px);
      background: rgba(0, 0, 0, 0.3);
      padding: 1rem;
      border-radius: 15px;
    }

    nav button {
      background: transparent;
      border: 1px solid cyan;
      color: cyan;
      padding: 0.7rem 1.5rem;
      border-radius: 10px;
      cursor: pointer;
      transition: all 0.3s ease, transform 0.2s;
      font-size: 1rem;
      text-shadow: 0 0 8px cyan;
    }

    nav button:hover {
      background: cyan;
      color: black;
      box-shadow: 0 0 15px cyan;
      transform: scale(1.1);
    }

    .section {
      display: none;
      padding: 2rem;
      text-align: center;
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }
    .active {
      display: block;
      opacity: 1 !important;
      transform: translateY(0) !important;
    }

    .hologram {
      position: relative;
      color: cyan;
      font-size: 1.5rem;
      text-shadow: 0 0 10px cyan, 0 0 20px blue;
      animation: flicker 2s infinite;
    }

    @keyframes flicker {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.6; }
    }

    .particles {
      position: relative;
      width: 100%;
      height: 200px;
      margin-top: 20px;
      overflow: hidden;
    }

    .particle {
      position: absolute;
      width: 6px;
      height: 6px;
      background: cyan;
      border-radius: 50%;
      animation: float 5s infinite;
    }

    @keyframes float {
      from { transform: translateY(200px) scale(0.5); opacity: 0; }
      to { transform: translateY(-200px) scale(1.5); opacity: 1; }
    }

    .card {
      background: rgba(0, 0, 0, 0.3);
      border: 1px solid cyan;
      border-radius: 15px;
      padding: 1rem;
      margin: 1rem auto;
      width: 250px;
      transition: transform 0.3s, box-shadow 0.3s;
      text-align: center;
      transform-style: preserve-3d;
    }

    .card:hover {
      transform: rotateY(10deg) rotateX(5deg) scale(1.05);
      box-shadow: 0 0 20px cyan;
    }

    .toggle-dark {
      position: fixed;
      top: 10px;
      right: 10px;
      background: rgba(0,0,0,0.5);
      border: 1px solid cyan;
      padding: 0.5rem 1rem;
      border-radius: 10px;
      color: cyan;
      cursor: pointer;
    }

    .dark-mode {
      background: #000 !important;
    }

    .stars {
      position: fixed;
      width: 100%;
      height: 100%;
      z-index: -1;
      top: 0;
      left: 0;
      overflow: hidden;
    }

    .star {
      position: absolute;
      width: 2px;
      height: 2px;
      background: white;
      animation: twinkle 3s infinite;
    }

    @keyframes twinkle {
      0%, 100% { opacity: 0.2; }
      50% { opacity: 1; }
    }

    .esper-controls {
      margin: 1rem;
    }
    .esper-btn {
      background: transparent;
      border: 1px solid magenta;
      color: magenta;
      padding: 0.5rem 1rem;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }
    .esper-btn:hover {
      background: magenta;
      color: black;
    }

    /* Portal spiral teleportasi */
    #portal {
      position: fixed;
      top: 50%;
      left: 50%;
      width: 250px;
      height: 250px;
      border-radius: 50%;
      transform: translate(-50%, -50%) scale(0);
      opacity: 0.9;
      z-index: 999;
      pointer-events: none;
      overflow: visible;
      transition: transform 0.8s ease, opacity 0.8s ease;
      background: radial-gradient(circle, rgba(0,255,255,0.7) 0%, rgba(0,0,0,0) 70%);
      box-shadow: 0 0 50px cyan, 0 0 100px blue inset;
    }

    .portal-particle {
      position: absolute;
      width: 5px;
      height: 5px;
      background: cyan;
      border-radius: 50%;
    }

    /* ===== Modal Tambahan ===== */
    #novelModal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.8);
      justify-content: center;
      align-items: center;
    }

    #novelModalContent {
      background: rgba(0,0,0,0.9);
      border: 1px solid cyan;
      padding: 2rem;
      border-radius: 15px;
      text-align: center;
      max-width: 400px;
      width: 90%;
    }

    #novelModalContent h3 {
      margin-bottom: 1rem;
      color: cyan;
    }

    .modal-btn {
      display: block;
      width: 80%;
      margin: 0.5rem auto;
      padding: 0.5rem;
      border: 1px solid cyan;
      border-radius: 8px;
      background: transparent;
      color: cyan;
      cursor: pointer;
      transition: 0.3s;
    }

    .modal-btn:hover {
      background: cyan;
      color: black;
    }
  </style>
</head>
<body>                                        <script>
  // ===== Script Splash Screen =====
  function enterWorld() {
    const splash = document.getElementById("splashScreen");
    splash.style.transition = "opacity 0.8s";
    splash.style.opacity = 0;
    setTimeout(() => {
      splash.style.display = "none";
      showSection('sinopsis'); // langsung masuk menu awal
    }, 800);
  }
</script>

  <header>🌌 Esper World Interface 🌌</header>

  <button class="toggle-dark" onclick="toggleDarkMode()">🌙</button>
  <audio id="bg-music" autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-10.mp3" type="audio/mpeg">
  </audio>
  <button class="toggle-dark" style="top: 60px;" onclick="toggleMusic()">🔊</button>

  <nav>
    <button onclick="showSection('sinopsis')">Sinopsis</button>
    <button onclick="showSection('latar')">Latar Belakang</button>
    <button onclick="showSection('profil')">Profil Karakter</button>
    <button onclick="showSection('esper')">Esper Interface</button>
 
    <!-- Tombol Modal Baru -->
    <button onclick="openModal()">📖 Baca Novel</button>
  </nav>

  <div id="sinopsis" class="section active">
    <h2>Sinopsis</h2>
    <p>"Ada enam kekuatan esper yang tertidur dalam jiwa-jiwa terpilih-dan kini, dunia mulai terbangun."

Chandra, seorang remaja biasa dengan masa lalu penuh amarah, tidak pernah menyangka bahwa kekuatan telekinesis dalam dirinya hanyalah awal dari sesuatu yang jauh lebih besar. Pertemuannya dengan Zenki-pemuda pendiam yang menyimpan kekuatan spiritual bernama Nethermind-membawanya ke jalan berbahaya yang menyingkap misteri warisan esper, simbol kuno, dan makhluk-makhluk bayangan dari dimensi lain.

Di tengah dunia modern yang tidak menyadari ancaman yang mengintai, mereka menemukan bahwa ada enam kekuatan esper utama, masing-masing terikat pada batu warisan kuno yang tersebar dan terlupakan. Dengan bantuan Kael, seorang mantan anggota Aetherion yang menyimpan rahasia masa lalu, mereka mulai mengungkap kebenaran yang menghubungkan kekuatan mereka dengan sejarah dunia yang hampir terhapus.

Namun semakin dalam mereka menggali, semakin jelas bahwa kekuatan bukanlah anugerah semata-melainkan ujian terhadap jiwa dan pilihan. Dalam pertarungan antara terang dan bayangan, mereka harus belajar memahami kekuatan bukan hanya dengan kekuatan otot, tetapi juga dengan kedewasaan batin.

Sebuah kisah fantasi spiritual tentang pertumbuhan, persahabatan, dan takdir, dalam dunia yang berdetak di antara realita dan yang tak terlihat.</p>
  </div>

  <div id="latar" class="section">
    <h2>Latar Belakang</h2>
    <p>Latar Belakang Novel – Esper World

Di dunia modern yang terlihat biasa, tersembunyi dimensi lain yang hanya bisa disentuh oleh mereka yang memiliki kekuatan esper. Kekuatan ini lahir dari kedalaman jiwa manusia, dipicu oleh emosi, trauma, dan tekad untuk melindungi diri maupun orang yang dicintai.

Para Esper tidak hanya manusia biasa; mereka adalah penjaga keseimbangan antara dunia nyata dan bayangan. Di balik kehidupan sehari-hari, ada organisasi rahasia, entitas gelap, dan simbol kuno yang terus mengintai, menunggu saat yang tepat untuk muncul.

Chandra, Zenki, dan Kael adalah tiga pilar awal yang tak disadari perannya oleh dunia. Chandra, dengan kekuatan telekinesis, memiliki kendali atas benda dan energi di sekitarnya. Zenki, pemilik Nethermind, mampu memasuki dunia spiritual dan membaca pikiran terdalam manusia. Sedangkan Kael, misterius dan terasing, menyatu dengan bayangan melalui Duskform, menghilang dari pandangan sekalipun.

Kehadiran mereka dipaksa ketika sebuah ancaman baru muncul: makhluk bayangan yang menelan jiwa, simbol misterius yang terukir di tempat-tempat suci, dan rahasia Aetherion, organisasi yang pernah Kael tinggalkan, yang kini kembali mengatur gerakannya dari balik bayangan.

Novel ini bukan hanya tentang pertarungan fisik. Ia adalah perjalanan spiritual, pengembangan diri, dan pertemuan dengan sisi gelap manusia. Setiap Esper harus menghadapi konflik batin, misteri masa lalu, dan pilihan yang bisa mengubah nasib dunia. Di dunia Esper, setiap kekuatan datang dengan harga, dan setiap keputusan bisa membuka jalan menuju cahaya… atau kehancuran.</p>
  </div>

  <div id="profil" class="section">
    <h2>Profil Karakter</h2>
    <div class="card"><b>Chandra</b><br>Esper Telekinesis, seorang mc yang awalnya mengalami kebangkitan</div>
    <div class="card"><b>Zenki</b><br>Esper Nethermind</div>
    <div class="card"><b>Kael</b><br>Esper Duskform</div>
  </div>

  <div id="esper" class="section">
    <h2 class="hologram" id="esper-title">Esper Interface - Telekinesis</h2>
    <p id="esper-desc">Kekuatan untuk mengendalikan benda dengan pikiran, seakan memiliki tangan tak kasat mata.</p>
    
    <div class="esper-controls">
      <button class="esper-btn" onclick="switchEsper('telekinesis')">Telekinesis</button>
      <button class="esper-btn" onclick="switchEsper('nethermind')">Nethermind</button>
      <button class="esper-btn" onclick="switchEsper('duskform')">Duskform</button>
    </div>

    <div class="particles" id="particles"></div>
  </div>

  <!-- Section Bab 1 - 11 -->
  <div id="bab1" class="section"><h2>Bab 1</h2><p>Namanya adalah Chandra dirinya hanyalah seorang manusia biasa. Ia adalah seorang laki-laki yang tinggal berdua bersama ibunya, dari kecil Chandra hanya dirawat oleh Ibunya dengan penuh kasih sayang yang hangat. Ayah Chandra sudah pergi meninggalkan Chandra di saat dirinya masih berumur lima tahun. Ibu dan Ayahnya bercerai, sehingga Ibu Chandra lah yang memilih untuk merawat Chandra dengan penuh kasih sayang. Saat ini, Chandra sedang menempuh pendidikan di sebuah SMAN di kota Kyoku kelas delapan.

Di sekolahnya, Chandra dikenal sebagai anak yang aneh karena lebih memilih untuk menyendiri. Teman-temannya menganggap Chandra sebagai seorang introvert, sebab setiap kali masuk kelas, ia hampir tidak pernah berbicara dengan siapa pun. Namun, mereka juga tidak terlalu peduli dengan kebiasaannya itu.

Di balik sifat pendiam dan misteriusnya, Chandra sebenarnya telah lama mendalami ilmu spiritual. Sejak kecil, tepatnya sejak usia sepuluh tahun, ia sudah tertarik dengan hal-hal yang berkaitan dengan kekuatan psikis dan spiritual. Ia selalu membaca buku-buku yang ia koleksi. Buku tersebut adalah koleksi lama Ayahnya yang sudah berdebu seperti tak dibuka selama berabad-abad. Isi buku-buku tersebut membahas ilmu seperti psikis dan spiritual esper. Selama membaca buku tersebut, dirinya semakin terobsesi akan dunia dengan kekuatan spiritual ataupun esper. Tak jarang juga dia selalu berandai-andai dirinya memiliki kekuatan tersebut.

Dalam buku tersebut berisi berbagai metode untuk membangkitkan kekuatan esper, salah satunya yaitu telekinesis. Beragam cara telah ia coba, seperti bermeditasi, mengamati lingkungan sekitar, dan bereksperimen dengan telekinesis-kemampuan untuk menggerakkan benda dengan kekuatan pikiran. Ia mencoba mengendalikan kertas kosong, berharap suatu hari bisa menguasai teknik ini sepenuhnya. Dalam teori yang ia pelajari, telekinesis merupakan kemampuan seorang esper untuk mengendalikan benda mati pada tahap awal, dan pada tingkat yang lebih tinggi, seseorang dapat mengendalikan serta merasakan aura makhluk hidup di sekitarnya.

Namun, meskipun sudah berlatih selama lima tahun, Chandra belum juga berhasil membangkitkan kekuatannya. Satu-satunya perubahan yang ia rasakan hanyalah peningkatan fokus dan ketenangan mental. Sifat penyendirinya pun tetap bertahan hingga kini.

Namun pada suatu sore ada suatu kejadian yang merubah perjalanan hidup Chandra sepenuhnya. Saat itu Chandra pulang sekolah dengan berjalan kaki seperti biasa. Sekolahnya memang tidak terlalu jauh dari rumah, dan keluarganya juga memiliki keterbatasan dalam hal kendaraan. Namun, hari itu berbeda dari biasanya.

"Ini semua karena kelas tambahan! Aku juga belum menyelesaikan pekerjaan rumah. Terpaksa aku harus pulang selarut ini," gumamnya kesal.

Langit sudah mulai gelap. Chandra memutuskan untuk mengambil jalan pintas agar bisa cepat sampai di rumah. Kebetulan, jalan pintas tersebut melewati sebuah bangunan kantor yang sudah terbengkalai selama lima belas tahun.

Saat melewati jalan setapak menuju bangunan itu, Chandra teringat peringatan ibunya. Jangan pernah melewati daerah itu sendirian. Banyak preman dan berandalan yang sering memalak orang di sana.

Namun, sudah terlambat untuk berpikir ulang.

"Aduh, kenapa baru ingat sekarang?" keluhnya sambil mempercepat langkah.

Tiba-tiba-

BRAKK!

Sebuah tendangan keras menghantam punggungnya dari belakang. Chandra terjerembap ke tanah, tubuhnya terasa nyeri.

"Woe, kawan-kawan! Lihat siapa yang kita temukan di sini!"

Lima orang preman berdiri mengelilinginya. Salah satu dari mereka, yang tampak seperti pemimpin, menatap Chandra dengan sinis.

"Woi, bocah! Berani sekali kau melewati daerah kami! Apa kau tidak tahu ini wilayah kekuasaan kami?" bentaknya dengan nada mengancam.

Chandra mengusap punggungnya yang masih sakit. Ia menatap tajam ke arah mereka dan berkata dengan sinis, "Tch, orang-orang sampah seperti kalian, yang hanya berani mengeroyok anak SMA sepertiku, tidak lebih baik dari kotoran hewan. Lemah!"

Perkataan Chandra sukses memancing emosi mereka. Namun, sebelum mereka menyerangnya secara bersamaan, Chandra segera menyela,

"Heh! Kalau kalian benar-benar jantan, ayo satu lawan satu denganku. Jika aku menang, aku boleh lewat. Jika aku kalah, ambil saja barang berhargaku. Bagaimana? Cukup adil, bukan?"

Preman-preman itu terdiam sejenak, lalu salah satu dari mereka maju. Pria bertubuh besar namun sedikit gemuk itu menyeringai licik.

"Hei, bocah! Kau tahu? Hari sial itu tidak pernah ada di kalender!" katanya sambil mengepalkan tinju.

Chandra hanya tersenyum santai. "Kalau begitu, ayo maju! Mau berapa lama lagi kita tatap-tatapan seperti ini?"

Pada saat itu, Chandra merasakan sesuatu yang aneh. Ada energi asing yang muncul dari dalam tubuhnya, membuat adrenalinnya meningkat drastis.

Pria besar itu akhirnya bergerak. Ia berlari ke arah Chandra dan mengayunkan tinjunya dengan kekuatan penuh.

Namun-

DUMP!

Sebelum pukulan itu mengenai wajahnya, Chandra menghempaskan tangannya ke tanah. Seketika, sebuah penghalang tak terlihat terbentuk di sekelilingnya. Tubuh preman itu terpental jauh begitu mengenai penghalang tersebut.

"Ugh! Uhuk... Apa-apaan ini?! Ada sesuatu yang melindunginya!"

Preman itu terbatuk-batuk, wajahnya penuh dengan keterkejutan.

Di mata mereka, Chandra hanya menggerakkan tangannya sedikit. Tapi di mata Chandra sendiri, ia melihat sebuah dinding pelindung bercahaya biru yang mengelilinginya.

"Jadi... begini rasanya telekinesis? Semua latihan ini akhirnya membuahkan hasil!" pikirnya penuh kegirangan.

Ketakutan, para preman itu perlahan mundur.

"Semuanya, lari! Anak ini dirasuki setan!" teriak salah satu dari mereka.

Chandra terkekeh pelan. "Seharusnya aku berterima kasih kepada mereka. Gara-gara mereka, aku bisa membangkitkan kekuatanku!"

Dengan senyum puas, Chandra melanjutkan perjalanannya pulang.

Sesampainya di rumah, Chandra langsung masuk ke kamar tanpa memberi tahu ibunya tentang kejadian tadi.

Ia masih teringat bagaimana energi itu muncul dari tubuhnya. Dalam situasi terpojok, nalurinya secara otomatis mengaktifkan kekuatan telekinesis.

Untuk memastikan kekuatannya benar-benar bangkit, ia mengambil selembar kertas kosong, meletakkannya di meja belajar, lalu duduk di depannya.

Ia menenangkan pikirannya dan mencoba menggerakkan kertas itu.

Perlahan... kertas itu mulai melayang dengan mudah.

Namun, ada satu hal yang membuatnya heran. Kali ini, ia tidak melihat aura biru seperti saat bertarung tadi sore.

"Hmm... Kenapa ya? Aku tetap bisa mengendalikan benda ini dengan mudah, tapi kenapa aku tidak bisa melihat atau memunculkan aura biru seperti tadi?" gumamnya bingung.

Namun, ia tidak terlalu memikirkannya. Yang terpenting, impiannya selama lima tahun ini akhirnya menjadi kenyataan.

Lelah setelah melalui hari yang panjang, Chandra tanpa sadar tertidur di kursi di depan meja belajarnya.

Keesokan paginya, Chandra terbangun dengan kepala sedikit pusing. Ia masih duduk di kursinya, dengan tangan yang tergeletak di atas meja.

"Aku tertidur?" gumamnya sembari mengusap wajahnya.

Ia menatap kertas yang semalam berhasil ia gerakkan dengan telekinesis. Perasaan aneh masih menggelayut di benaknya. Mengapa saat melawan preman, ia bisa melihat aura biru, tapi saat berlatih sendiri, hal itu tidak muncul?

Chandra mencoba lagi. Ia menatap kertas itu dengan penuh konsentrasi. Kertas itu melayang, tetapi tetap tidak ada aura biru yang muncul.

"Apa mungkin ini hanya terjadi saat emosiku memuncak?" pikirnya.

Tiba-tiba, terdengar suara ketukan di pintu.

Tok... tok... tok...

"Chandra, ayo sarapan dulu," suara ibunya terdengar dari luar kamar.

Chandra menghela napas panjang. "Iya, Bu. Aku segera keluar."

Sebelum beranjak, ia melirik kertas itu sekali lagi. Ada banyak pertanyaan yang belum terjawab, dan ia tahu bahwa ini barulah permulaan dari sesuatu yang lebih besar.</p></div>
  <div id="bab2" class="section"><h2>Bab 2</h2><p>Isi Bab 2 di sini...</p></div>
  <div id="bab3" class="section"><h2>Bab 3</h2><p>Isi Bab 3 di sini...</p></div>
  <div id="bab4" class="section"><h2>Bab 4</h2><p>Isi Bab 4 di sini...</p></div>
  <div id="bab5" class="section"><h2>Bab 5</h2><p>Isi Bab 5 di sini...</p></div>
  <div id="bab6" class="section"><h2>Bab 6</h2><p>Isi Bab 6 di sini...</p></div>
  <div id="bab7" class="section"><h2>Bab 7</h2><p>Isi Bab 7 di sini...</p></div>
  <div id="bab8" class="section"><h2>Bab 8</h2><p>Isi Bab 8 di sini...</p></div>
  <div id="bab9" class="section"><h2>Bab 9</h2><p>Isi Bab 9 di sini...</p></div>
  <div id="bab10" class="section"><h2>Bab 10</h2><p>Isi Bab 10 di sini...</p></div>
  <div id="bab11" class="section"><h2>Bab 11</h2><p>Isi Bab 11 di sini...</p></div>

  <div class="stars" id="stars"></div>
  <div id="portal"></div>

  <!-- Modal Baca Novel -->
  <div id="novelModal">
    <div id="novelModalContent">
      <h3>Pilih Bab</h3>
      <button class="modal-btn" onclick="selectBab('bab1')">Bab 1</button>
      <button class="modal-btn" onclick="selectBab('bab2')">Bab 2</button>
      <button class="modal-btn" onclick="selectBab('bab3')">Bab 3</button>
      <button class="modal-btn" onclick="selectBab('bab4')">Bab 4</button>
      <button class="modal-btn" onclick="selectBab('bab5')">Bab 5</button>
      <button class="modal-btn" onclick="selectBab('bab6')">Bab 6</button>
      <button class="modal-btn" onclick="selectBab('bab7')">Bab 7</button>
      <button class="modal-btn" onclick="selectBab('bab8')">Bab 8</button>
      <button class="modal-btn" onclick="selectBab('bab9')">Bab 9</button>
      <button class="modal-btn" onclick="selectBab('bab10')">Bab 10</button>
      <button class="modal-btn" onclick="selectBab('bab11')">Bab 11</button>
      <button class="modal-btn" onclick="closeModal()">Tutup</button>
    </div>
  </div>

  <script>
    const portal = document.getElementById("portal");

    function showSection(id) {
      portal.style.transform = "translate(-50%, -50%) scale(1)";
      createPortalSpiral();

      setTimeout(() => {
        document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
        document.getElementById(id).classList.add('active');
        portal.style.transform = "translate(-50%, -50%) scale(0)";
        document.querySelectorAll(".portal-particle").forEach(p => p.remove());
        if (id === 'esper') generateParticles();
      }, 900);
    }

    function generateParticles(color="cyan") {
      const container = document.getElementById("particles");
      container.innerHTML = "";
      for (let i = 0; i < 20; i++) {
        let p = document.createElement("div");
        p.className = "particle";
        p.style.background = color;
        p.style.left = Math.random() * 100 + "%";
        p.style.animationDuration = (3 + Math.random() * 3) + "s";
        container.appendChild(p);
      }
    }

    function createPortalSpiral() {
      const count = 60;
      const center = 125; // tengah portal
      for (let i = 0; i < count; i++) {
        let p = document.createElement("div");
        p.className = "portal-particle";
        let angle = i * 12;
        let radius = 5 + i * 2;
        let rad = angle * Math.PI/180;
        let x = center + radius * Math.cos(rad);
        let y = center + radius * Math.sin(rad);
        p.style.left = x + "px";
        p.style.top = y + "px";
        p.style.background = `hsl(${i*6}, 100%, 50%)`;
        portal.appendChild(p);
      }
    }

    function toggleDarkMode() { document.body.classList.toggle("dark-mode"); }
    function toggleMusic() {
      let music = document.getElementById("bg-music");
      if (music.paused) music.play(); else music.pause();
    }

    function generateStars() {
      const container = document.getElementById("stars");
      for (let i = 0; i < 100; i++) {
        let s = document.createElement("div");
        s.className = "star";
        s.style.top = Math.random() * 100 + "%";
        s.style.left = Math.random() * 100 + "%";
        s.style.animationDuration = (2 + Math.random() * 3) + "s";
        container.appendChild(s);
      }
    }

    function switchEsper(type) {
      let title = document.getElementById("esper-title");
      let desc = document.getElementById("esper-desc");
      if (type === "telekinesis") {
        title.textContent = "Esper Interface - Telekinesis";
        desc.textContent = "Kekuatan untuk mengendalikan benda dengan pikiran, seakan memiliki tangan tak kasat mata.";
        generateParticles("cyan");
      } else if (type === "nethermind") {
        title.textContent = "Esper Interface - Nethermind";
        desc.textContent = "Menyelam ke kedalaman jiwa dan kesadaran, mengungkap misteri batin manusia.";
        generateParticles("purple");
      } else if (type === "duskform") {
        title.textContent = "Esper Interface - Duskform";
        desc.textContent = "Menyatu dengan bayangan, menghilang dari pandangan dunia nyata.";
        generateParticles("black");
      }
    }

    generateStars();

    // ===== Script Modal =====
    const novelModal = document.getElementById("novelModal");

    function openModal() { novelModal.style.display = "flex"; }
    function closeModal() { novelModal.style.display = "none"; }

    function selectBab(babId) {
      closeModal();
      showSection(babId);
    }
  </script>
</body>
</html> masih dalam pengembangan 2025/dst
