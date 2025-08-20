
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
  <div id="bab2" class="section"><h2>Bab 2</h2><p>Dua hari setelah kejadian rumit itu, Chandra masih belum bisa lepas dari pertanyaan yang terus menghantui pikirannya. Sejak dirinya membangkitkan kekuatan esper, ia memilih untuk diam dan merahasiakannya. Jika kekuatan itu sampai tersebar ke mana-mana, ia yakin masalah akan semakin rumit dan sulit dikendalikan. Oleh karena itu, Chandra berusaha menjalani hidupnya seperti biasa-bersekolah, mengerjakan tugas, membantu membersihkan rumah, dan melakukan aktivitas normal lainnya.

Namun, pada hari ketiga setelah kebangkitannya, Chandra kembali ke sekolah seperti biasa. Ia duduk menyendiri di kelas, berbicara hanya jika diperlukan. Hari itu, pelajaran berlangsung normal tanpa ada kejadian aneh sedikit pun. Para siswa fokus mengerjakan tugas yang diberikan oleh pak guru yang berlarut dalam keheningan. 

Tiba-tiba, suara ketukan terdengar dari pintu kelas yang memecahkan suasana keheningan di dalam ruang kelas.

Tok tok tok

"Silakan masuk," ujar pak guru dengan tenang.

Saat pintu mulai terbuka, terlihat jari-jari seseorang yang perlahan mendorongnya, seolah ragu atau takut untuk masuk ke dalam kelas. Ketika pintu terbuka lebar, tampak seorang anak laki-laki berdiri di ambang pintu. Ia mengenakan seragam sekolah, tetapi seragamnya sedikit berbeda dari milik Chandra dan teman-temannya.

Chandra langsung menebak dalam hati, "Pasti dia murid baru yang akan melengkapi kelas ini. Apalagi, bangku di sampingku masih kosong," gumamnya dalam hati.

Dengan rasa penasaran, Chandra memperhatikan anak itu dengan saksama. Namun, sebelum ia bisa menebak lebih jauh, suara guru tiba-tiba terdengar, memecah keheningan.

"Hei, Nak, mau sampai kapan kau berdiri di depan pintu? Masuklah dan perkenalkan dirimu di depan kelas," ujar sang guru.

Anak itu mulai melangkah perlahan menuju ke depan kelas, raut wajahnya menunjukkan rasa malu dan gugup. Dengan hati-hati, ia menghampiri sang guru, lalu menjabat tangannya dengan sopan.

Pak guru menundukkan sedikit kepalanya dan berbisik lembut, "Oke, sekarang perkenalkan dirimu kepada mereka. Mereka akan menjadi rumah dan teman barumu."

Tanpa ragu, tiba-tiba anak itu berbicara dengan nada lantang, menarik perhatian seluruh kelas.

"Perhatian semuanya! Perkenalkan, namaku Zenki, biasa dipanggil Zen. Aku adalah siswa pindahan dari SMA Kisomu. Aku harap kalian semua bisa menjadi temanku dan menerima kehadiranku di sini. Terima kasih!"

Seisi kelas langsung terdiam, beberapa murid saling berpandangan, terkejut dengan cara Zenki memperkenalkan dirinya yang begitu percaya diri.

Saat semua mata siswa tertuju pada Zenki, Chandra justru tidak terlalu memperdulikan hal tersebut. Ia kembali fokus pada buku dan penanya, melanjutkan tugas yang belum ia selesaikan dari Pak Guru.

Pak Guru yang melihat cara Zenki memperkenalkan diri tertawa terbahak-bahak sambil menepuk pundaknya.

"Hahaha! Kamu ini lucu sekali, Nak. Sekarang, coba pilih, kamu ingin duduk di mana?"

Zenki melirik ke sekeliling kelas, tetapi hanya tersisa satu bangku kosong-di samping Chandra. Dengan nada sedikit gugup, ia menjawab,

"Pak, saya ingin duduk di sudut belakang, di samping anak itu. Lagi pula, hanya bangku itu yang masih kosong."

Lalu, Pak Guru mengangkat tangannya dan menunjuk ke arah Chandra. Dengan suara keras dan lantang, beliau berkata, "Hei, Ndra! Anak baru ini ingin duduk di sebelahmu. Bapak harap kamu tidak mencuekinya seperti teman-teman yang lain."

Mendengar hal itu, seisi kelas langsung tertawa terbahak-bahak. "Hahaha!" Namun, seperti biasa, Chandra tidak menghiraukan gurauan mereka. Baginya, semua itu hanyalah angin lalu-sesuatu yang sudah menjadi bagian dari kehidupannya sehari-hari.

Zenki kemudian menghampiri dan duduk perlahan di sebelah Chandra awal nya Chandra merasa canggung untuk berbincang bincang dengan Zen, dirinya sedikit merasa risih karena dirinya sendiri sudah terbiasa duduk sendirian dan nyaman dengan kesendirian nya.

Selama pelajaran berlangsung, Chandra enggan berbicara sedikit pun kepada Zenki. Sebagai murid baru, Zenki merasa tidak enak karena sejak tadi ia dan Chandra hanya terdiam tanpa berbincang sama sekali.

---

Saat jam istirahat tiba, Zenki berusaha menarik perhatian Chandra. Ia mencoba membuka percakapan dengan topik yang berkaitan dengan psikologi. Dengan santai, ia menatap Chandra dan mulai berbicara,

"Hei, namamu Chandra, kan? Salam kenal, aku Zenki."

Chandra yang mendengar Zenki tiba-tiba menyapanya, menoleh sebentar dan menjawab singkat, "Oh, ya. Namaku Chandra. Salam kenal juga."

Zenki merasa jengkel dengan respon singkat itu. Dalam hati, ia menggerutu, "Apa-apaan sih dia ini? Orang mau ngobrol malah diabaikan. Sok dingin banget."

Namun, Zenki tidak menyerah. Ia mencoba membuka topik baru, kali ini dengan nada yang lebih sopan dan halus.

"Oh iya, Chandra. Aku dengar kamu cukup pendiam di kelas ini. Kenapa, sih? Ada alasan tertentu?" tanyanya dengan penasaran.

Chandra, yang jarang diajak bicara lebih dulu oleh orang lain, akhirnya menoleh dan menatap Zenki dengan serius.

"Aku diam begini ada alasannya. Nanti kamu juga bakal tahu sendiri," jawabnya dengan nada sedikit kesal.

Melihat Chandra mulai tertarik dengan pembicaraan, Zenki pun tersenyum iseng dan mencoba memancing reaksinya.

"Heh, aku tahu kok. Sebenarnya kamu ingin diajak ngobrol, tapi gengsi, ya?" katanya dengan nada menggoda dan senyum mengejek.

Chandra yang mendengar itu langsung mengangkat satu alisnya, ekspresinya berubah sedikit jengkel.

"Hei, maksudmu apa? Ngajak ribut?" tanyanya dengan nada menantang.

Dalam hati, Zenki tertawa puas. "Hahaha, akhirnya dia terpancing juga."

Namun, bukannya menjawab, ia justru terkekeh pelan. Melihat reaksi itu, Chandra semakin kesal. Ia yang tadinya duduk santai, kini menegakkan bahunya dan kembali bertanya,

"Hei, aku tanya sekali lagi. Kau ngajak berantem, ya?" ucapnya dengan senyum kesal.

Zenki, yang sejak tadi hanya menggoda, akhirnya tertawa lepas dan menjawab dengan nada santai,

"Hahaha! Kamu ini lucu juga, ya? Dari luar kelihatan sok dingin dan misterius, tapi ternyata asyik diajak ngobrol. Aku rasa kita bisa jadi teman baik!"

Chandra yang mendengar itu hanya mendengus, tapi sudut bibirnya sedikit terangkat, seolah menahan senyum.

Zenki pun mengulang pertanyaannya, kali ini dengan nada yang sedikit lebih lembut dan meyakinkan, "Jadi, kita bisa jadi teman baik, kan?"

Chandra, yang selama ini tidak terlalu mengenal arti pertemanan, merasakan sesuatu yang hangat di hatinya. Baru pertama kali ada seseorang yang benar-benar ingin berteman dengannya. Matanya sedikit bersinar, dan tanpa sadar, air mata tipis hampir terbentuk di sudutnya.

Ia tersenyum, lalu menjawab tanpa ragu, "Hahaha, kamu memang pandai, ya, membuatku tersentuh sekaligus tertawa. Tentu saja, kenapa tidak? Kita pasti bisa menjadi teman yang baik!"

Zenki yang mendengar jawaban Chandra seperti itu senyum nya pun melebar dan matanya berbinar binar "makasih banget, gimana kalau nanti kita pulang barengan?" Kebetulan aku cuma tinggal sendiri dan gapunya kedua orang tua."

Chandra yang mendengar pernyataan Zenki bahwa ia tidak memiliki kedua orang tua merasa semakin iba dan tersentuh.

"Oh, baiklah. Aku nggak keberatan sama sekali, kok," jawabnya dengan tulus.

Melihat Zenki tampak senang, Chandra pun menambahkan, "Kalau mau menginap di rumahku juga nggak apa-apa. Lagipula, aku hanya tinggal berdua dengan ibuku."

Setelah sedikit ragu, ia akhirnya bertanya dengan wajah penuh kebingungan, "Oh iya, kalau boleh tahu, ke mana kedua orang tuamu, Zen?"

Mendengar pertanyaan itu, Zenki terdiam sejenak. Ia tidak ingin langsung membahasnya, jadi ia berusaha menghindar dengan jawaban ringan,

"Oh, orang tuaku ya? Nanti aja deh, Ndra. Aku ceritain di perjalanan pulang," katanya sambil tersenyum kecil, mencoba mengalihkan suasana.

Selama jam pelajaran berlangsung Chandra dan Zen terlihat akur dan saling bantu membantu ketika salah satu dari mereka tidak paham tentang pelajaran yang di pelajari.

Saat senja mulai menyelimuti kota tepatnya jam lima sore bel sekolah pun berbunyi menandakan kegiatan belajar mengajar telah usai dan murid di perbolehkan untuk pulang.
Zenki dan Chandra bergegas menyandang tas mereka dan menuju ke gerbang keluar sekolah. 

Selama di perjalanan pulang mereka jalan berdampingan dan saling berirama sore itu udara terasa sedikit dingin dan terasa hening serta sepi, Zen memiliki perasaan yang kurang enak terhadap apa yang sedang terjadi namun berusaha tak menghiraukan nya agar Chandra tidak ikut khawatir, namun di saat itu

Chandra, yang masih penasaran dengan latar belakang Zenki, akhirnya bertanya lagi, "Jadi, sekarang kamu bisa cerita tentang orang tuamu, Zen?"

Zenki menghela napas pelan. "Ya... sebenarnya, mereka sudah lama tiada. Aku tumbuh di panti asuhan sebelum akhirnya tinggal sendiri."

Chandra terdiam, merasa bersalah karena telah menanyakannya. Namun sebelum ia sempat merespons, tiba-tiba mereka merasakan hawa aneh di sekitar mereka. Udara mendadak terasa lebih berat, dan lampu-lampu jalanan mulai berkedip-kedip seakan ada gangguan listrik.

Zenki dan Chandra saling bertatapan, merasakan ada sesuatu yang tidak beres.

"Zen, kau merasakan ini juga?" tanya Chandra dengan suara pelan namun waspada.

Zenki mengangguk. "Ya... ini bukan sesuatu yang biasa."

Tiba-tiba, dari kejauhan, terdengar suara langkah kaki menyeret di atas aspal. Suara itu terdengar tidak wajar-seperti sesuatu yang berat sedang bergerak.

Mereka berdua menoleh ke arah suara itu, dan di ujung jalan yang remang-remang, terlihat sesosok bayangan tinggi berdiri diam. Sosok itu samar, tubuhnya seperti diselimuti kabut gelap.

Jantung Chandra mulai berdegup lebih cepat. Ia merasa merinding tanpa alasan yang jelas. "Zen... apa itu?" bisiknya.

Zenki menatap sosok tersebut dengan mata tajam, lalu berbisik, "Aku nggak tahu... tapi sepertinya dia bukan manusia biasa."

Tiba-tiba, sosok itu bergerak cepat ke arah mereka, membuat angin berhembus kencang. Zenki dengan refleks menarik tangan Chandra dan berteriak, "LARI!"

Mereka berdua berlari sekencang mungkin, namun entah mengapa, bayangan itu terus mendekat tanpa mengeluarkan suara. Sesuatu yang gelap sedang mengincar mereka-dan mereka harus segera mencari cara untuk melarikan diri atau melawan.

Sejauh apa pun mereka berlari, rasanya seperti hanya berputar-putar kembali ke tempat semula. Jalanan yang mereka lewati selalu sama-pohon yang sama, lampu jalan yang sama, bahkan suara gemerisik daun yang tak berubah.

Chandra mulai merasakan sesuatu yang aneh. Dengan cepat, ia menyentak tangan Zenki dan menggenggamnya erat. Dengan nada serius, ia berkata, "Hei, Zen! Aku nggak tahu kenapa, tapi rasanya sejak tadi kita cuma berputar-putar di tempat yang sama. Sepertinya kita sudah terjebak di dunia yang berbeda!"

Zenki terdiam, napasnya memburu. Ia menoleh ke sekeliling, mencoba memahami situasi. Namun sebelum ia sempat berpikir lebih jauh, Chandra melanjutkan dengan tegas, "Nggak ada pilihan lain! Mau nggak mau, kita harus menghadapi makhluk itu!"

Mata Zenki melebar, terkejut dengan keberanian Chandra. Dengan nada panik, ia berbisik, "Menghadapi? Tapi... gimana caranya?! Yang punya kekuatan di sini cuma aku-"

Zenki langsung terhenti, menyadari bahwa ia keceplosan. Wajahnya menegang, sementara Chandra menatapnya dengan ekspresi penuh keterkejutan.

"Tunggu... apa maksudmu barusan, Zen?" tanya Chandra, matanya menyipit curiga.

Zenki menggigit bibirnya. Ia baru saja membocorkan rahasia besarnya-bahwa dirinya bukan orang biasa.

Tepat sebelum Chandra sempat merespons, tiba-tiba makhluk misterius itu menyerang. Dengan kekuatan mengerikan, ia melemparkan beberapa bongkahan batu besar yang berserakan di sekitar mereka. Menyadari bahaya yang mengancam, Chandra refleks mengulurkan tangannya, menggunakan kekuatannya untuk menghentikan batu-batu itu di udara sebelum menghantam mereka.

Zenki terpaku, jantungnya berdebar kencang. Ia baru saja melihat sesuatu yang tak pernah ia duga-Chandra juga memiliki kekuatan.

"Ka-kau..." Zenki masih sulit berkata-kata. "Kau juga seorang esper?"

Chandra menoleh cepat, ekspresinya waspada. "Kita bicarakan nanti!" katanya tegas. Ia mengayunkan tangannya, dan batu-batu besar yang sebelumnya melayang di udara kini melesat kembali ke arah makhluk misterius itu.

Makhluk itu menggeram marah. Tubuhnya yang hitam pekat seolah berdenyut, lalu dari dalam tubuhnya muncul gelombang energi yang menghancurkan batu-batu tersebut menjadi serpihan kecil. Zenki bisa merasakan tekanan luar biasa dari kekuatan lawan mereka.

"Kita harus bekerja sama!" Chandra berseru. "Kalau tidak, kita tidak akan selamat dari ini!"

Zenki menelan ludah. Ia tahu Chandra benar-tak ada lagi gunanya menyembunyikan kekuatannya. Dengan nada serius, ia akhirnya menjawab, "Ya, kita harus bekerja sama."

Lalu, dengan tatapan tegas, Zenki melanjutkan, "Chandra, tolong alihkan perhatian makhluk ini. Aku akan memasuki dunia spiritual. Singkatnya, tubuh asliku tidak akan sadar untuk sementara. Aku akan melawannya di alam bawah sadar. Bisa dibilang, kemampuanku ini disebut Nethermind."

Chandra, yang masih dalam kondisi panik, hanya bisa mendengarkan perkataan Zenki dan mempercayakan semuanya kepadanya. Dengan cepat, ia berusaha mengalihkan perhatian monster tersebut. "Woi, monster jelek! Aku di sini!" Chandra berteriak lantang sambil menggunakan kekuatannya untuk menahan tubuh makhluk itu.

"Zen, apakah masih lama kau memasuki dunia spiritual? Aku nggak bisa menahannya lebih lama lagi!" serunya dengan napas tersengal.

Saat itu juga, Chandra melihat sesuatu keluar dari tubuh Zenki-seperti roh yang berterbangan di udara. Namun, tidak seperti roh pada umumnya yang berwarna putih, aura yang menyelimutinya justru bersinar dalam cahaya ungu misterius.

Wushhh! Roh itu melesat dengan kecepatan tinggi ke arah makhluk tersebut, menciptakan ledakan dahsyat. Boom! Asap tebal menyebar ke segala arah.

Chandra segera membentengi dirinya, berusaha menahan dampak ledakan agar tidak mengenainya. Namun, penglihatannya terhalang oleh kepulan asap yang memenuhi udara.

"A-apa-apaan dengan kekuatan itu?! Hanya satu serangan, tapi dampaknya sebesar ini!"

Saat gumpalan asap mulai menghilang, Chandra menatap ke depan. Ia terkejut bukan kepalang melihat makhluk misterius itu telah tewas dengan kepala remuk dan tubuh hancur. Ia mengedarkan pandangan ke sekeliling, memastikan bahwa roh tersebut benar-benar lenyap. Namun, ketika ia menoleh ke belakang, matanya membelalak melihat tubuh Zenki yang tumbang.

Jantungnya berdegup kencang saat ia bergegas memeriksa denyut nadi Zenki. "Syukurlah, dia hanya pingsan," desahnya lega, meski napasnya masih tersengal.

Dengan enggan, Chandra bersiap menggendong Zenki. "Mau tak mau, aku harus membawanya pulang," gumamnya.

Namun, dalam benaknya, sebuah kesadaran baru mulai tumbuh-ternyata, bukan hanya dirinya yang memiliki kemampuan spesial. Dan ini hanya akan membuat segalanya semakin rumit.

</p></div>
  <div id="bab3" class="section"><h2>Bab 3</h2><p>Setelah kejadian kemarin sore menjelang malam, Chandra masih diliputi kegelisahan. Meskipun ia berhasil bertarung dan selamat, perasaan tak berdaya terus menghantuinya. Nyatanya, jika bukan karena Zenki, mereka mungkin sudah tidak ada di dunia ini. Fakta bahwa Zenki sampai harus mengerahkan seluruh kekuatannya hingga pingsan membuat Chandra sadar-mereka masih terlalu lemah. Jika ancaman lain muncul, apakah mereka benar-benar bisa bertahan?

Di dalam kamar Chandra, Zenki perlahan membuka mata. Rasa sakit menjalar di seluruh tubuhnya, seolah setiap otot menolak untuk bergerak. Nethermind memang kuat, tapi efek sampingnya terlalu besar. Ia harus memahami batas kemampuannya-bagaimana menggunakannya dengan lebih efisien tanpa mengorbankan tubuhnya sendiri.

Zenki mencoba bangkit, namun tubuhnya masih lemah. Saat ia berusaha berdiri, pandangannya berputar, dan lututnya hampir menyerah. Sempoyongan, ia bertumpu pada dinding, mengatur napas yang terasa berat. Keringat dingin mengalir di pelipisnya. Ini bukan sekadar kelelahan-ini adalah peringatan bahwa ia belum siap menghadapi pertarungan yang lebih besar.

Chandra masih merasa khawatir dengan keadaan Zenki. Ia membawa sepiring nasi dengan lauk ayam dan berjalan menuju kamar temannya. Saat pintu terbuka, Chandra terkejut melihat Zenki yang berusaha bangkit dari tempat tidur.

Dengan sigap, ia segera menghampiri Zenki dan menopang tubuhnya agar kembali berbaring. "Hei, jangan memaksakan diri. Kau belum sepenuhnya pulih," tegurnya dengan nada khawatir.

Zenki menunduk sedikit sebelum menjawab pelan, "Aku hanya tidak ingin merepotkanmu."

Chandra menghela napas dalam-dalam, lalu menatapnya dengan ekspresi yang sulit dijelaskan. "Kau tahu nggak, kalau kemarin kau nggak menggunakan kekuatanmu sepenuhnya, mungkin nyawa kita sudah melayang. Kita bahkan nggak akan ada di sini sekarang," ucapnya, suaranya terdengar lebih tegas dari yang ia maksudkan. Namun, wajahnya sedikit memerah karena malu.

Sejenak, keheningan menyelimuti mereka. Lalu, dengan suara lebih pelan, Chandra melanjutkan, "Dan... aku juga minta maaf. Kemarin, aku nggak bisa berbuat banyak. Seandainya aku bisa melakukan sesuatu lebih dari itu, mungkin kondisimu nggak akan seburuk ini. Maafkan aku, Zenki."

Tatapannya merunduk, rasa bersalah mengendap di dadanya. Zenki menghela napas sejenak sebelum berkata dengan nada pelan, berusaha menenangkan perasaan Chandra, "Soal itu jangan dipikirkan. Lagipula, apa yang kau lakukan sudah sangat baik. Coba bayangkan jika kau tidak menahan makhluk itu, mungkin aku tak akan punya cukup waktu untuk memasuki dunia Nethermind."

Mendengar ucapan Zenki, Chandra perlahan mengangkat kepalanya kembali. Senyum tipis terukir di wajahnya.

"Oh iya, aku bawa makanan untukmu. Jangan sungkan, silakan dimakan," tutur Chandra pelan.

Zenki menerima piring itu dan mulai makan perlahan, suapan demi suapan. Rasa hangat dari makanan itu sedikit mengurangi kelelahan dalam tubuhnya.

"Ini enak. Siapa yang memasak ayamnya?" tanya Zenki heran.

"Oh, itu aku yang memasaknya sendiri," jawab Chandra sambil memainkan selembar kertas dengan kemampuannya. "Kebetulan ibuku sedang berada di luar kota selama satu bulan ke depan. Dia dapat panggilan kerja mendadak."

Zenki mengangguk kecil, mencerna informasi tersebut. "Jadi ibumu sedang di luar kota, ya... satu bulan..." Ia terdiam sejenak, pikirannya berputar, mencari ide tentang apa yang bisa mereka lakukan dalam waktu tersebut.

Tiba-tiba, matanya berbinar penuh semangat. "Aku rasa kita bisa latihan!" serunya antusias.

"T-tunggu, maksudnya apa? Latihan?" tanya Chandra dengan kaget dan heran. "Aku sih setuju saja kalau kau menyarankan untuk melatih kemampuan kita ini, tapi kau tidak memikirkan sekolah? Bagaimana dengan nilai kita?" celetuknya dengan nada sedikit kesal.

Sebenarnya, Chandra setuju dengan saran Zenki, tetapi ia juga sadar bahwa dirinya tetaplah manusia biasa yang harus menyelesaikan pendidikannya. Tidak mungkin dalam waktu sebulan ia malah bolos sekolah, karena itu akan berdampak buruk pada nilainya.

"Bagaimana kalau kita membagi waktu?" ujar Zenki dengan penuh percaya diri. "Kita bisa menjalani aktivitas normal dari pagi hingga sore, lalu setelah pulang sekolah, kita berlatih mengembangkan kemampuan kita. Lagi pula, kalau tidak salah, bulan ini sekolah akan banyak libur karena adanya ujian penilaian sekolah," tambahnya berusaha meyakinkan Chandra sepenuh hati.

"Aku rasa usulmu tidak buruk, aku setuju," jawab Chandra, lalu menyipitkan mata penuh curiga. "Tapi... dari mana kau tahu kalau kita akan banyak libur karena ujian sekolah?" tanyanya heran.

Zenki terkekeh sambil melirik Chandra dengan ekspresi mengejek. "Aduh, kau ini benar-benar tidak peka dengan kemampuan temanmu sendiri, ya?" godanya dengan senyum sinis.

Sebelum Chandra sempat membalas, Zenki melanjutkan dengan nada serius. "Nethermind adalah kemampuan yang memungkinkan seseorang memiliki dua kesadaran-satu berada di dunia nyata, satu lagi di dunia spiritual. Di dunia nyata, aku bisa membaca pikiran seseorang dan merasakan aura emosi mereka, entah itu bahagia, sedih, marah, atau lainnya. Sedangkan di dunia spiritual, aku dapat merasakan keberadaan makhluk tak kasat mata dan menggunakan kekuatan penuhkku. Namun, aku masih belum mahir mengendalikannya. Setiap kali menggunakan Nethermind sepenuhnya, tubuhku terasa seperti ingin hancur," jelasnya dengan sorot mata tajam ke arah Chandra.

Chandra, yang sejak tadi menyimak, mengangguk pelan. "Oh, jadi itu dasar kekuatanmu... Tapi aku masih belum sepenuhnya mengerti," katanya ragu. "Terutama karena aku sendiri juga belum memahami cara kerja kemampuanku sepenuhnya. Kadang-kadang aku hanya bisa menggerakkan kertas atau benda kecil seperti ini, tapi saat dalam keadaan terdesak, aku mampu mengendalikan dan menggenggam benda-benda seolah memiliki tangan yang lebih panjang. Aku tidak benar-benar mengerti bagaimana mekanismenya. Yang kutahu, kemampuanku disebut telekinesis," jelasnya dengan nada bimbang.

Zenki terdiam sejenak, mencerna penjelasan Chandra. Ada sesuatu yang terasa janggal baginya. Setelah berpikir sejenak, sebuah pertanyaan terlintas di benaknya.

"Oh, soal itu... kau mendapatkan kemampuan ini dari mana?" tanya Zenki dengan nada serius, matanya menatap Chandra tajam.

"Aku mendapatkannya melalui latihan," jawab Chandra santai.

Zenki semakin bingung. Ia hendak menanggapi, tetapi sebelum sempat berbicara, Chandra memotongnya, "Tunggu di sini, aku akan mengambil sesuatu dulu."

Tanpa menunggu jawaban, Chandra berjalan menuju lemari bukunya. Zenki hanya bisa menatapnya dengan penuh kebingungan. Beberapa saat kemudian, Chandra kembali dengan sebuah buku tua yang tampak usang dan sudah lama berdebu.

"Ini... buku yang membuatku memiliki kemampuan esper," ungkap Chandra sambil menyerahkan buku itu kepada Zenki.

Zenki membuka buku tersebut, membalik halaman demi halaman, membaca beberapa bagian dengan penuh perhatian. Raut wajahnya semakin serius. Setelah membaca beberapa lembar, ia mengangkat kepalanya dan menatap Chandra dengan kebingungan.

"Darimana kau mendapatkan buku ini?" tanyanya heran.

Chandra mengambil kembali buku itu dari tangan Zenki, lalu menunjuk ke arah sebuah meja di sudut ruangan. "Buku ini kutemukan di dalam laci meja itu. Bentuknya sudah usang... dan setahuku, buku ini milik ayahku," jelasnya dengan nada sedikit muram.

Zenki menatap meja itu dalam diam, pikirannya dipenuhi berbagai pertanyaan yang belum terjawab. Namun, untuk saat ini, ia lebih ingin fokus pada latihan mereka.

"Oh, begitu... Lalu bagaimana dengan pembahasan tadi? Kau setuju, kan, kita tetap berlatih?" tanya Zenki, mengharapkan kepastian.

"Hmm, kurasa aku bisa. Lagipula, kau boleh menginap di sini agar rumah ini terasa lebih ramai," jawab Chandra dengan senyum.

Zenki menyeringai. "Kau ingin rumah ini terasa lebih ramai, atau sebenarnya kau hanya takut makhluk seperti tadi menyerang lagi?" godanya dengan tawa keras.

"Hah, aku tidak selemah itu," sahut Chandra, mendengus. "Lebih baik kau istirahat sekarang. Aku juga ingin tidur. Lagi pula, besok kita libur, tidak ada sekolah."

Dengan itu, Zenki dan Chandra memutuskan untuk beristirahat, membiarkan malam berlalu dalam ketenangan setelah peristiwa yang mereka alami.
•
•
•

Pagi itu, sinar matahari menerobos melalui celah jendela kamar Chandra, membanjiri ruangan dengan cahaya keemasan. Zenki mengerjap pelan, merasakan tubuhnya yang masih terasa berat setelah pertarungan kemarin. Di seberang ruangan, Chandra sudah terjaga, duduk di lantai sambil membuka-buka buku tua yang semalam mereka bicarakan.

"Pagi," ujar Zenki dengan suara serak.

Chandra menoleh, lalu tersenyum kecil. "Pagi. Gimana perasaanmu sekarang?"

Zenki menggerakkan bahunya sedikit, merasakan nyeri yang masih tersisa. "Lebih baik, meskipun masih agak pegal."

"Baguslah. Aku sudah membaca beberapa bagian dari buku ini lagi. Sepertinya ini bukan sekadar buku biasa. Ada beberapa simbol aneh yang aku belum mengerti," kata Chandra sambil menunjuk halaman yang penuh dengan tulisan dan diagram yang terlihat kuno.

Zenki bangkit perlahan dan menghampiri Chandra. Ia memperhatikan halaman yang ditunjukkan. Mata ungunya menyipit, mencoba memahami simbol-simbol tersebut. "Aku pernah melihat sesuatu yang mirip ini dalam penglihatanku saat menggunakan Nethermind... Tapi aku tidak yakin."

Chandra menghela napas. "Sepertinya kita harus menemukan seseorang yang bisa membaca ini. Mungkin ini bisa membantu kita memahami kekuatan kita dengan lebih baik."

Zenki mengangguk setuju. "Tapi untuk saat ini, mari kita mulai latihan. Kau sudah setuju, kan?"

Chandra tersenyum tipis. "Baiklah, tapi jangan memaksakan diri. Kita mulai dari yang ringan dulu."

Mereka berdua melangkah keluar rumah menuju halaman belakang, yang cukup luas untuk latihan. Udara pagi masih segar, embun masih menggantung di dedaunan. Zenki berdiri di tengah halaman, mencoba merasakan energi Nethermind dalam dirinya, sementara Chandra mulai mengangkat beberapa benda kecil dengan telekinesisnya.

"Baiklah, mari kita mulai dengan dasar-dasarnya. Aku ingin mencoba mengendalikan Nethermind tanpa efek samping berlebihan," kata Zenki sambil menutup mata.

Chandra mengangguk dan mulai menggerakkan kertas-kertas yang ia siapkan, mencoba mengasah kendali halusnya terhadap telekinesis.

Selama beberapa waktu, mereka berlatih dengan tenang. Zenki mencoba mengatur aliran energinya, membatasi keluarnya agar tidak langsung menguras tubuhnya. Chandra, di sisi lain, fokus pada meningkatkan presisi kendali telekinesisnya, berusaha menggerakkan objek lebih berat secara perlahan dan terkontrol.

Di tengah latihan, Chandra tiba-tiba berhenti dan menatap Zenki dengan ragu. "Aku penasaran... Sebenarnya bagaimana kau bisa mendapatkan kekuatan Nethermind ini? Apakah kau juga menemukannya seperti aku menemukan buku ini?"

Zenki membuka matanya dan menatap Chandra sejenak sebelum mengalihkan pandangannya ke langit. "Aku sendiri tidak sepenuhnya mengerti... Tapi aku tahu satu hal, ini bukan sesuatu yang kudapatkan secara kebetulan. Ada sesuatu di masa laluku yang memicu kekuatan ini bangkit, tapi aku belum bisa mengingat semuanya dengan jelas."

Chandra mengangguk pelan, memahami bahwa Zenki mungkin menyimpan sesuatu yang lebih dalam tentang kekuatannya. "Kalau begitu, mungkin kita bisa mencari tahu bersama. Kita tidak hanya berlatih meningkatkan kekuatan, tapi juga memahami asal-usulnya."

Zenki tersenyum tipis. "Itu ide yang bagus. Kalau kita bisa memahami asal mula kekuatan kita, mungkin kita bisa mengendalikannya dengan lebih baik."

Chandra tersenyum dan kembali berkonsentrasi pada latihannya. Hari itu, mereka terus berlatih dengan serius, tanpa sadar bahwa perjalanan mereka baru saja dimulai.

Saat latihan mereka semakin intens, Chandra dan Zenki mulai merasakan peningkatan dalam pengendalian kekuatan masing-masing. Chandra berhasil menggerakkan benda lebih besar dengan lebih presisi, sementara Zenki mulai menemukan cara untuk mengurangi efek samping dari Nethermind.

Namun, ketenangan itu tidak berlangsung lama.

Tiba-tiba, udara di sekitar mereka berubah. Angin bertiup lebih kencang, membawa serta aura yang tidak asing bagi Zenki. Ia merasakan tekanan yang sama seperti saat bertarung melawan makhluk misterius sebelumnya, namun kali ini, energinya terasa lebih terkendali-lebih manusiawi.

"Kau merasakannya?" tanya Chandra, suaranya tegang.

Zenki mengangguk. "Kita tidak sendirian."

Sebuah suara menggema dari arah pohon di belakang mereka. "Jadi, kalian berdua yang membuat kehebohan belakangan ini?"

Dari bayangan pepohonan, muncul sosok bertudung hitam. Tatapannya tajam, penuh dengan niat yang sulit diterka. Dalam sekejap, ia melesat ke arah mereka dengan kecepatan luar biasa.

Zenki dan Chandra langsung bersiap. Chandra mengangkat beberapa batu dengan telekinesisnya, sementara Zenki berusaha mengaktifkan Nethermind tanpa kehilangan kendali.

Tanpa basa-basi, sosok itu menyerang. Sebuah serangan energi meluncur ke arah mereka. Chandra buru-buru membentuk penghalang dengan menggerakkan beberapa papan kayu yang ada di sekitar, sementara Zenki melompat ke samping, menghindari serangan dengan susah payah.

"Kalian lamban," ucap sosok itu dengan nada meremehkan. "Jika ini batas kemampuan kalian, lebih baik menyerah sekarang."

Zenki menggeram, mengaktifkan Nethermind dalam skala kecil. Aura ungu mengelilingi tubuhnya, matanya bersinar tajam. "Siapa kau sebenarnya?" tanyanya dengan nada penuh kewaspadaan.

Sosok itu tidak langsung menjawab. Ia hanya tersenyum tipis, lalu tiba-tiba menghilang dari pandangan. Dalam sekejap, ia muncul tepat di depan Chandra dan mendorongnya mundur dengan sebuah serangan gelombang energi yang tak terlihat. Chandra terhempas ke belakang, mendarat dengan keras di tanah.

"Chandra!" teriak Zenki, mencoba berlari ke arahnya. Namun, sebelum ia bisa bergerak lebih jauh, sosok misterius itu sudah berdiri di hadapannya.

"Kita akan bertemu lagi," bisiknya pelan, sebelum tiba-tiba menghilang secepat ia datang.

Zenki dan Chandra terdiam, napas mereka terengah-engah. Serangan itu begitu cepat, begitu mendadak, hingga mereka bahkan tidak bisa membalas dengan baik.

Chandra bangkit perlahan, menahan nyeri di tubuhnya. "Siapa... orang itu?"

Zenki mengepalkan tangannya. "Aku tidak tahu... tapi yang jelas, dia tidak datang hanya untuk menguji kita. Dia punya tujuan."

Chandra berusaha untuk bangkit ia bertanya sambil terbatuk "aku tidak begitu mengerti mengapa dia dapat menhilang dan timbul dalam sekejap mata?." 

Zenki yang mendengar pertanyaan itu berusaha berpikir keras. Ia teringat tentang kemampuan kamuflase, tetapi masih belum bisa memastikan jenisnya.

"Aku rasa orang tadi memiliki kemampuan untuk menghilang dan muncul kembali dalam sekejap... kemungkinan besar itu sejenis kamuflase," ujar Zenki dengan nada serius. "Tapi aku belum tahu pasti bagaimana cara kerjanya. Bisa jadi dia memanipulasi cahaya, memasuki dimensi lain, atau mungkin sesuatu yang lebih kompleks dari itu, namun sekilas aku dapat merasakan suatu aura saat dia menghilang."

Chandra mengusap lengan yang masih terasa nyeri akibat serangan sebelumnya. "Kalau begitu, kita harus mencari tahu lebih banyak... karena jelas dia bukan musuh biasa."

Zenki mengangguk. "Ya... dan aku yakin ini bukan pertemuan terakhir kita dengannya."

Chandra mengepalkan tangannya, matanya menyala penuh tekad. "Kalau orang itu muncul lagi, kita harus siap. Kita tidak bisa terus-menerus bertahan tanpa benar-benar memahami kemampuan kita."

Zenki mengangguk, matanya menyipit tajam. "Setuju. Kita harus lebih kuat. Jika tidak, kita hanya akan menjadi mangsa berikutnya."

Angin berembus pelan, membawa keheningan yang terasa berat. Mereka berdua tahu-latihan mereka baru saja berubah menjadi sesuatu yang lebih serius.

Di kejauhan, sosok misterius itu berdiri di atas pohon, memperhatikan mereka dari bayang-bayang. Ia menyeringai tipis. "Sepertinya mereka masih bisa berkembang... Ini akan menarik."

</p></div>
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
