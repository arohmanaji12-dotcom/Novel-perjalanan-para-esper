
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
  <div id="bab4" class="section"><h2>Bab 4</h2><p>Malam telah menelan langit sepenuhnya, menyisakan bintang-bintang yang menggantung seperti pengintai abadi. Di atas sebuah menara air tua, sosok bertudung hitam berdiri membisu. Angin malam menggoyangkan jubahnya, namun ia tidak bergeming. Matanya menatap lurus ke arah kota di kejauhan, di mana dua anak muda baru saja mulai memahami kekuatan mereka.

"Chandra dan Zenki," gumamnya pelan, seolah mengulang nama-nama yang baru ia pelajari. "Mereka belum siap... tapi mereka bisa menjadi aset-atau ancaman."

Tangannya membuka sebuah liontin kecil yang tergantung di lehernya. Di dalamnya, tergambar simbol kuno yang sama seperti yang ada di buku milik Chandra. Tatapannya menajam.

"Sudah lama sejak aku melihat simbol ini terakhir kali. Tidak kusangka, warisan itu muncul kembali."

Ia duduk di pinggir menara, memejamkan mata. Dalam pikirannya, suara-suara dari masa lalu kembali menggema-latihan yang brutal, pengkhianatan, dan sebuah organisasi yang menghilang tanpa jejak. Ia bukan sekadar pengamat. Ia pernah menjadi bagian dari semua itu.

"Ayahmu... Chandra. Apa kau benar-benar tahu siapa dia?" bisiknya, senyuman sinis menyungging di bibirnya.

Ia membuka matanya. Tatapan tajam dan dingin kembali terpancar. "Sudah saatnya aku mencari jawaban. Kalau buku itu memang warisan dari generasi sebelumnya, maka mereka tidak bisa dibiarkan berlatih tanpa pengawasan."

Ia melompat turun dari menara, mendarat dengan senyap di atap sebuah bangunan. Tubuhnya bergerak cepat, hampir tak terlihat di tengah bayang malam.

"Aku akan menguji mereka lagi. Tapi kali ini... bukan untuk mengalahkan."

Dia adalah Kael Varuna.

Dulu, ia adalah bagian dari organisasi rahasia bernama Aetherion, kelompok esper elit yang bertugas menjaga keseimbangan spiritual dunia-sampai satu peristiwa tragis menghancurkan segalanya. Pengkhianatan dari dalam membubarkan Aetherion, dan Kael adalah satu dari sedikit yang selamat.

Sejak itu, ia hidup dalam bayang-bayang, mengawasi kebangkitan kekuatan baru. Ia menyimpan dendam terhadap pengkhianat yang mengkhianati organisasinya, dan ia percaya semua yang berkaitan dengan simbol warisan harus diawasi-atau dimusnahkan.

Namun sesuatu dalam diri Chandra dan Zenki membuatnya ragu.

Mereka tidak seperti para esper yang dulu dia kenal.

---

---

Pagi itu, sekolah terasa ganjil. Langit memang cerah, tapi ada sesuatu di udara-getaran halus yang membuat kulit merinding. Chandra dan Zenki saling melirik saat memasuki kelas.

"Zenki, kau juga ngerasa?" bisik Chandra.

Zenki mengangguk. "Sejak bangun tadi. Aura itu... seperti ada yang mengawasi kita."

Hari berjalan lambat. Tapi perasaan ditekan itu tak juga menghilang. Di lorong kelas, di tangga belakang, bahkan di ruang guru yang biasanya aman-getaran aneh itu tetap ada. Tidak cukup kuat untuk mengganggu, tapi cukup untuk membuat jantung berdetak lebih cepat.

Saat bel pulang berbunyi, keduanya langsung berkemas.

"Kita ke kuil," kata Chandra pelan. "Kalau dia mau muncul, di sanalah tempatnya."

Zenki mengangguk. "Dan kita nggak sendiri. Aku yakin dia udah mengincar kita sejak pagi."

Langit mulai menguning saat mereka tiba di reruntuhan kuil. Tempat itu sunyi, tapi aura itu... semakin kuat, semakin dekat.

Lalu dia muncul.

Dari balik reruntuhan pilar, seorang remaja berdiri. Wajahnya teduh tapi tatapannya tajam, seolah bisa menembus kedalaman pikiran. Rambut hitamnya tergerai, dan di balik seragam sekolah yang dikenakan, ada aura pekat yang membuat Zenki refleks menaikkan pertahanannya.

"Jadi kalian yang selama ini membuat suara dunia ini bergetar," ucapnya pelan, hampir seperti gumaman.

Chandra melangkah maju. "Kau siapa?"

"Aku... Kael. Esper, seperti kalian. Tapi tak seperti kalian, aku tidak menunggu dunia meminta tolong."

"Artinya?" tanya Zenki.

Kael tersenyum tipis. "Artinya, aku sudah bosan menunggu. Dunia ini sakit, dan kadang... sesuatu harus dihancurkan sebelum bisa diperbaiki."

Aura spiritual Kael meledak. Tanah bergetar pelan, reruntuhan berderak, dan udara terasa semakin berat. Dari balik bayangan, semacam entitas hitam muncul di belakangnya-misterius dan berdenyut seperti kabut hidup.

Chandra merapat ke Zenki. "Kita nggak bisa ngomong baik-baik ya?"

Kael menatap mereka dengan pandangan dingin. "Buktikan dulu bahwa kalian layak bicara denganku."

Chandra dan Zenki berdiri di hadapan Kael, pemuda berambut hitam pendek dengan tatapan tenang namun tajam. Percakapan mereka baru saja mulai saat udara tiba-tiba menggetar pelan, seperti ada sesuatu yang bangun.

Suara gemuruh halus menggema dari dinding belakang kuil. Sebuah simbol retak memancarkan cahaya kehijauan yang merayap.

Zenki: "Apa itu...?"

Chandra mundur setengah langkah, bersiap memanggil energinya.

Kael tidak berkata apa-apa. Dalam sekejap, tubuhnya lenyap dalam bayangan, seolah tertelan senja. Suasana makin mencekam-langkah kaki tak terdengar, udara jadi dingin.

Tiba-tiba-CRACK!

Simbol pecah, dan energi negatif menyembur keluar, membentuk bayangan raksasa samar.

Namun sebelum makhluk itu sempat bergerak, sesosok bayangan muncul tepat di atasnya. Dalam gerakan cepat dan nyaris tak terlihat, Kael muncul kembali dari kegelapan, telapak tangannya menyentuh kepala makhluk itu.

Sebuah ledakan cahaya gelap menyelimuti makhluk itu... dan menghilang.

Chandra tertegun.
Zenki, dengan tatapan serius: "Apa barusan dia... menghilang?"

Kael melangkah keluar dari bayangan tiang kuil, seolah baru muncul dari tempat lain sepenuhnya.

Kael: "Tenang saja. Itu hanya segel tua yang lepas kendali. Tapi kuil ini tidak sepenuhnya mati, dan beberapa jebakan masih aktif. Jangan sentuh simbol sembarangan."

Chandra: (pelan) "Jadi ini kekuatanmu... kamuflase?"

Kael: "Kau bisa menyebutnya begitu. Aku menyebutnya Duskform."

----

Zenki melangkah mendekat, ekspresi wajahnya berubah menjadi lebih serius.
Zenki: "Teknik yang kau pakai tadi... bukan sembarangan. Itu bukan hanya kamuflase biasa."

Kael menoleh perlahan, tapi tak langsung menjawab.

Chandra: "Apa kau... pernah dilatih sebelumnya? Kau bukan anak biasa, bukan?"

Kael menghela napas pendek, lalu menyandarkan tubuhnya ke dinding batu kuil yang dingin. Matanya memandang jauh ke arah lubang cahaya di langit-langit yang memantulkan cahaya senja.

Kael: "Dulu, aku bagian dari sesuatu yang disebut Aetherion. Organisasi itu... sekarang sudah tak ada."

Keduanya saling bertatapan. Nama itu terasa asing, namun anehnya menggema dalam nurani mereka, seolah pernah terdengar dalam mimpi.

Zenki: "Aetherion? Itu... organisasi esper?"

Kael mengangguk pelan.
Kael: "Kami menjaga keseimbangan antara dunia manusia dan energi spiritual. Tapi waktu itu... sesuatu terjadi. Sesuatu yang membuat semuanya runtuh. Sejak saat itu, aku memilih diam."

Chandra: "Kenapa ada di sini sekarang?"

Kael: "Karena aku mencium bau yang sama... Energi yang dulu membuat Aetherion runtuh. Dan entah kenapa, kalian-"

Ia menatap Zenki dan Chandra dalam-dalam.

Kael: "-berada di pusatnya."

Suasana hening. Bayangan matahari sore mulai tertelan senja. Angin berdesir di antara celah kuil.

Zenki, pelan: "Kalau begitu... kita di jalan yang sama."

Kael: "Mungkin."

Chandra: "Dan kalau benar begitu... kau bersama kami sekarang?"

Kael tak menjawab langsung. Ia melangkah perlahan keluar dari naungan kuil, bayangannya seolah larut bersama senja.

Kael: "...Kita lihat saja nanti."

Kael menghilang ke balik reruntuhan, meninggalkan Chandra dan Zenki dalam keheningan. Tapi keheningan itu bukan kedamaian-melainkan awal dari sesuatu yang lebih besar.

Chandra menarik napas dalam. "Dia bukan musuh," ucapnya akhirnya. "Tapi bukan juga kawan."

Zenki mengangguk. "Tapi dia tahu lebih banyak dari kita... tentang Aetherion, tentang kekuatan ini."

Chandra dan Zenki masih berdiri di depan reruntuhan kuil yang kini terasa sunyi, seolah baru saja menyaksikan sesuatu yang tidak sepenuhnya bisa dimengerti. Cahaya matahari senja sudah hampir lenyap sepenuhnya, digantikan bayangan malam yang merambat pelan.

Zenki memegang lengan Chandra. "Kau yakin tentang dia?"

Chandra mengangguk perlahan, meski matanya masih menyisakan keraguan. "Aku nggak yakin bisa percaya dia... tapi aku tahu kita perlu dia."

Tiba-tiba, suara langkah terdengar dari sisi reruntuhan. Mereka refleks bersiap, namun yang muncul hanyalah siluet samar-Kael kembali, kali ini tanpa menyembunyikan kehadirannya.

"Aku akan bantu kalian," ucapnya datar. "Tapi bukan karena aku percaya pada misi kalian. Aku hanya ingin tahu... apakah kalian benar-benar pantas memegang warisan itu."

Zenki menyipitkan mata. "Warisan?"

Kael tak menjawab. Ia melemparkan sesuatu ke arah mereka-sebuah pecahan kristal berwarna hitam dengan jejak retakan ungu di dalamnya. Chandra menangkapnya dengan telekinesis secara refleks.

Chandra menggenggam pecahan kristal itu lebih erat, rasanya dingin dan berat-seperti membawa beban yang tidak terlihat. Zenki melirik ke arah pecahan tersebut, sorot matanya tak bisa menyembunyikan rasa penasaran.

"Apa maksudmu dengan 'dulu milik salah satu dari kalian'?" tanya Chandra, nada suaranya pelan tapi menuntut.

Kael menunduk, bayang-bayang senja menutupi setengah wajahnya. "Dia salah satu esper terkuat yang pernah kulihat. Tapi kekuatannya... terlalu besar untuk dunia ini. Dia percaya bisa menyatukan semua esper, tapi jalan yang dia pilih... berujung pada kehancuran."

Kael menatap langit yang mulai menggelap.

"Aku masih mengingat hari saat Aetherion runtuh. Api, suara-suara pengkhianatan, dan teriakan... teman-teman kami. Kami tak kalah oleh musuh. Kami dihancurkan oleh diri kami sendiri."

Chandra dan Zenki terdiam. Aura yang menyelimuti kuil menjadi lebih pekat, bukan karena kekuatan spiritual, tapi karena kenangan pahit yang mengendap di udara.

Chandra membuka mulut, tapi Kael lebih dulu bicara.

"Karena itulah aku menguji kalian. Aku perlu tahu... apakah kalian akan mengulangi kesalahan mereka."

Zenki menatap Kael lurus-lurus. "Dan setelah melihat kami... kau yakin?"

Kael tidak langsung menjawab. Ia mengangkat tangan, dan dari bayangan di belakangnya, sesosok entitas gelap perlahan muncul. Bentuknya kabur, berubah-ubah seperti asap, tapi di tengahnya bersinar sebuah kristal hitam-utuh, memancarkan aura senyap yang menelan cahaya di sekitarnya.

"Inilah kekuatanku yang sebenarnya-Duskform," ucap Kael. "Bayangan bukan sekadar tempatku bersembunyi. Aku adalah bayangan itu."

Entitas itu menyatu kembali ke tubuhnya, dan seketika angin berhembus kembali, seolah waktu baru saja bergerak lagi.

Zenki melangkah maju, wajahnya serius. "Kau menguji kami. Sekarang izinkan kami menguji balik."

Kael menaikkan satu alis. "Oh?"

Chandra tersenyum tipis. "Jika kau benar-benar bagian dari Aetherion... maka kau tahu pentingnya kepercayaan. Kau tahu seperti apa rasanya kehilangan rekan. Jangan jadikan kami musuh hanya karena bayang-bayang masa lalu."

Kael terdiam cukup lama. Angin malam meniup pelan helai rambutnya yang jatuh di dahi. Lalu ia berbalik, melangkah pergi-namun sebelum benar-benar menghilang ke dalam kegelapan, ia berhenti.

"Aku akan menghubungi kalian lagi. Tapi ingat... kepercayaan itu rapuh. Dan bayangan selalu mengawasi."

Lalu dia lenyap-seolah larut dalam udara malam.

Chandra dan Zenki saling pandang. Mereka tidak tahu apakah baru saja mendapatkan sekutu... atau musuh paling berbahaya.

---

Malam itu, di bawah cahaya bulan separuh, mereka berdiri di reruntuhan kuil yang kembali sunyi. Tapi kini, mereka tahu: mereka bukan lagi dua esper yang sendirian.

Mereka adalah bagian dari warisan yang lebih besar.

Dan bayangan dari masa lalu... perlahan mulai bangkit.

---

Malam turun sepenuhnya ketika Chandra dan Zenki berjalan pulang dari kuil. Langkah mereka lambat, tidak hanya karena tubuh yang lelah, tapi juga karena pikiran yang berat. Hening menyelimuti sepanjang perjalanan, hanya suara serangga malam yang menemani.

Setibanya di rumah, Chandra langsung mengunci pintu dan menjatuhkan tasnya di sofa.

"Ini gila," katanya pelan, menjatuhkan diri ke kursi. "Kael... Aetherion... semua ini makin rumit."

Zenki membuka kulkas, mengambil dua botol air dan melempar salah satunya ke arah Chandra. "Tapi itu juga berarti kita nggak salah jalan. Kita nggak berhalusinasi atau semacamnya. Semua ini nyata."

Chandra memandang ke arah meja, di mana buku tua pemberian ayahnya tergeletak. Simbol di sampulnya kini terasa lebih berat, seakan berdenyut dengan makna yang baru saja terbuka sebagian.

"Ayahku dulu bagian dari semua ini, ya?" gumamnya.

Zenki hanya diam, lalu duduk di sampingnya. "Mungkin kita nggak bakal dapet semua jawabannya sekarang. Tapi kita udah mulai jalan."

Setelah mandi dan berganti pakaian, keduanya duduk di lantai kamar, membentangkan kembali halaman-halaman buku yang lusuh itu. Ada banyak catatan, diagram, dan simbol. Tapi malam itu, satu halaman tampak berbeda.

Simbol kristal dengan enam warna-masing-masing mewakili kekuatan mereka-mulai bersinar samar. Cahaya biru di tengah berkedip pelan.

￼

Chandra menatapnya dengan dalam. "Kael bilang kita ada di pusat semuanya. Kalau benar begitu, maka ini bukan cuma tentang bertahan... tapi memilih ke mana arah kekuatan ini dibawa."

Zenki tersenyum tipis. "Dan sepertinya kita nggak punya pilihan selain maju."

Keesokan harinya...

Cahaya matahari pagi menerobos jendela kamar, membangunkan Chandra dari tidurnya. Ia menggeliat malas, lalu menoleh ke arah Zenki yang sudah duduk di meja, membuka halaman-halaman buku tebal itu.

"Lo nggak tidur?" tanya Chandra sambil mengucek mata.

"Sebentar aja," jawab Zenki. "Buku ini... ada satu halaman yang baru muncul waktu lo udah tidur."

Chandra menghampiri, melihat halaman yang dimaksud. Sebuah simbol baru terukir samar-bentuknya seperti topeng runcing dengan mata hitam kosong.

"Apa ini...?"

"Sesuatu yang nggak enak. Dan firasatku bilang, itu bakal muncul hari ini."

---

Di sekolah...

Hari berjalan seperti biasa-sampai mereka sampai di lorong dekat ruang musik. Udara mendadak jadi lembap, seperti habis hujan, padahal cuaca di luar terang. Beberapa siswa mengeluh merasa pusing, dan beberapa lainnya mendadak panik melihat bayangan aneh di cermin kelas.

Chandra dan Zenki saling pandang. Aura itu familiar-gelap dan menekan, tapi juga... kelaparan.

"Di ruang musik," bisik Zenki.

Mereka menyelinap ke sana saat bel istirahat. Ruangan kosong, tapi udara di dalamnya terasa seperti menggantung-tebal dan berat.

Lalu... terdengar suara.

"Kelaparan... jiwa... suara..."

Sebuah bayangan muncul di pojok ruangan, membentuk sosok menyerupai manusia, tapi wajahnya kosong seperti topeng. Mulutnya terus membuka, seolah-olah menyerap suara di sekitarnya.

Chandra menarik napas dalam. "Roh jahat."

Zenki mengangkat tangannya, aura ungu dari Nethermind mulai mengalir. "Kita tangkap ini cepat, sebelum ada yang lihat."

Roh itu mengaum-suara seperti serak angin dan logam. Ia melesat ke arah mereka dengan gerakan terputus-putus, seperti film rusak. Tapi Chandra mengangkat tangannya, dan benda-benda di sekeliling langsung beterbangan, membentuk penghalang. Meja piano melayang di udara, menghantam roh itu dari samping.

Zenki melompat, telapak tangannya menyentuh bayangan itu. Energi ungu menyerap masuk, mencoba menahan roh tersebut di dalam pikirannya.

Namun roh itu memberontak. Tiba-tiba, ia mengeluarkan teriakan melengking-frekuensi tinggi yang membuat kaca jendela bergetar hebat dan memecah.

Chandra berteriak. "Aku nggak bisa tahan lama!"

Telinga Chandra berdering akibat jeritan roh itu. Ia mengerjap-lalu menyadari sesuatu yang aneh.

Ruangan berubah.

Piano di pojok kini tampak usang dan berdebu, tirai jendela berkibar meski tak ada angin. Warna ruangan memudar, seperti lukisan yang dilunturkan air. Udara kental dengan gema bisikan, dan bayangan-bayangan samar bergerak di dinding.

"Dia tarik kita masuk ke... Dimensi Roh," desis Zenki, wajahnya pucat.

Lantai seperti berkabut, dan cermin-cermin di ruangan memantulkan sosok yang bukan milik mereka. Sosok lain-tak bernama, tanpa wajah.

Chandra mencengkeram lengan kursi piano yang melayang, lalu sadar benda itu tak benar-benar ada. Semuanya di sini adalah pantulan, tiruan. Dunia ini... meniru dunia nyata, tapi tanpa kehidupan.

Roh itu muncul lagi, kini lebih besar, tubuhnya menggumpal seperti awan tinta dalam air. Suaranya menggema tanpa arah. "Kelaparan... suara... suara kalian... kuat..."

Zenki berdiri, energi Nethermind menjalar di telapak tangannya.

"Kita harus selesaikan ini di sini. Kalau tidak, dia bisa tembus ke dunia nyata."

Chandra mengangguk, lalu melemparkan kesadarannya ke sekeliling. Di dunia ini, batas antara pikir dan benda jauh lebih tipis. Telekinesisnya tak hanya mengangkat-ia membentuk ulang. Ia mengumpulkan serpihan dari 'suara'-gema percakapan yang tersisa di dinding ruang musik bayangan itu-dan membentuknya menjadi penghalang berbentuk spiral.

Roh itu menghantam spiral suara itu, lalu menjerit saat tubuhnya retak oleh bentuk suara yang tak bisa ia kendalikan.

Zenki melompat masuk ke tengah spiral, mengukir simbol Nethermind dengan energi pikirannya. Rune ungu menyala, lalu memancar ke seluruh dimensi.

"Kunci suara... segel ilusi..." bisiknya.

Roh itu mencoba kabur, tapi ruangan mulai runtuh-bukan hancur, tapi "menguap", perlahan-lahan larut menjadi cahaya putih.

Chandra memejamkan mata.

Saat ia membukanya-

Mereka kembali di ruang musik.

Piano utuh. Cermin tak pecah. Meja dan kursi rapi seperti biasa.

Seakan tak pernah terjadi apa-apa.

Zenki berdiri perlahan, keringat dingin masih menetes di dahinya. "Kita keluar... tepat waktu."

Chandra menatap ke arah cermin. Di sana, tak ada apa pun-hanya bayangan dirinya sendiri.

---

Di atap sekolah, sore harinya...

Langit mulai memerah saat Kael berdiri membelakangi matahari, memandangi lapangan sekolah yang perlahan sepi. Ia menyaksikan dua sosok keluar dari gedung musik-Chandra dan Zenki, dengan langkah lelah tapi wajah waspada.

Kael menyipitkan mata. "Mereka bergerak cepat."

Suara-suara samar kembali bergema di kepalanya-kenangan masa lalu saat Aetherion pernah mengurung roh serupa di lokasi lain. Tapi roh tadi... bukan sembarangan.

Ia melangkah mundur dari tepian atap dan menyentuh liontin di lehernya.

"Segel tua yang rusak... dan simbol itu muncul lagi. Dunia spiritual mulai retak, dan mereka terjun ke dalamnya begitu saja."

Wajahnya datar, tapi ada kilatan rasa penasaran dan... keterlibatan.

---

Sementara itu, di lorong sekolah yang sepi...

Langkah Chandra dan Zenki terhenti.

Kael muncul dari ujung lorong, bersandar santai ke dinding dengan tangan di saku. Tatapannya tajam seperti biasa, tapi kali ini ada sedikit nada menguji.

Kael: "Kalian berdua... membuat gempar satu gedung dengan roh kelas-C. Menarik."

Chandra, heran: "Kau ngikutin kita?"

Kael mengangkat bahu. "Mengamati."

Zenki: "Itu bukan roh biasa. Dia... seperti mengincar sesuatu."

Kael: "Dia memang bukan roh biasa. Namanya Voidsong. Dulu, kami segel dia jauh di bawah kuil. Tapi tampaknya waktu sudah melemahkan segalanya." (diam sebentar) "Dan kini, segel itu-dan dunia ini-mulai retak lagi."

Chandra: "Lalu kenapa kau biarkan kami melawan sendirian?"

Kael menatap Chandra, tajam. "Karena kalian harus belajar. Aetherion tidak pernah berdiri dengan tangan gemetar."

Zenki menghela napas. "Apa kau mau kami mati?"

Kael: "Kalau kalian mati hari ini, kalian tidak pantas menyentuh warisan itu."

Hening. Suasana tegang. Tapi Kael kemudian berjalan mendekat dan menjatuhkan sesuatu-sepotong kristal hitam kecil, berbentuk belah ketupat.

Kael: "Itu milikku dulu. Simpan. Aku akan tahu jika sesuatu mendekat lagi."

Chandra mengambil kristal itu, menatapnya bingung.

Kael berjalan pergi, dan sebelum menghilang di balik bayangan, ia menoleh:

Kael: "Besok... kalian harus mulai mencari tahu apa yang sebenarnya kalian warisi. Sebelum segalanya terlambat."

---

Malam hari, rumah Chandra.

Lampu ruang tengah menyala lembut, memantulkan cahaya ke dinding yang dipenuhi rak buku dan foto keluarga. Di atas meja makan, dua cangkir teh masih mengepulkan uap. Chandra duduk menyandar di kursi, menatap langit-langit, sementara Zenki bersandar di dinding, tangan terlipat.

Chandra: "Hari ini... aneh banget."

Zenki mengangguk pelan. "Kita hampir dilahap roh kuno, Kael nongol lagi, dan sekarang... kita punya batu misterius ini."

Ia menaruh kristal hitam Kael di meja. Kristal itu berdenyut samar, seperti merespons udara malam.

Chandra: "Menurutmu Kael percaya kita bisa mengatasinya?"

Zenki: "Aku rasa... dia lebih percaya kalau kita akan mati dan menyaring siapa yang pantas lanjut."

Chandra tertawa hambar. "Klasik Kael."

Suasana hening sejenak. Di luar, suara jangkrik mulai terdengar. Angin malam masuk dari jendela yang terbuka, membawa aroma dedaunan basah.

Zenki: "Aku sempat lihat sesuatu di mata Voidsong tadi."

Chandra menoleh. "Apa?"

Zenki menunduk. "Seperti... rasa takut. Seolah dia melarikan diri dari sesuatu yang lebih besar."

Chandra mengerutkan alis. "Kau yakin?"

Zenki: "Aku tahu bagaimana takut itu terlihat. Dia... bukan datang untuk menyerang. Dia kabur."

Mereka saling tatap. Pemikiran itu membuat suasana jadi lebih berat.

Chandra: "Jadi kita belum lihat musuh sebenarnya."

Zenki: "Belum. Dan Kael tahu itu."

Chandra berdiri, menatap ke luar jendela. "Kalau begitu... kita harus lebih kuat. Besok, kita mulai pelajari apa pun yang bisa kita temukan soal Aetherion."

Zenki tersenyum tipis. "Kita?"

Chandra: (menoleh dan menyeringai) "Kau pikir aku bakal biarin kau jadi pahlawan sendirian?"

---

bergerak ke arah kristal hitam di meja.

Kilatan energi samar keluar darinya, menciptakan bayangan kecil di dinding... bayangan itu bukan milik siapa pun yang ada di ruangan.

Dan di tempat jauh... seorang sosok membuka matanya perlahan.

???: "...Warisan itu telah bangkit."

Chandra mematikan lampu ruang tengah, menyisakan cahaya dari kamar tidurnya yang terbuka sedikit. Ia berjalan ke dapur, mengambil segelas air, lalu menatap cermin kecil di lemari es.

Tatapannya kosong.

Chandra: (berbisik) "Ayah... Kau pernah tahu soal ini, kan?"

Ia membuka laci, mengeluarkan buku tua yang sebelumnya ditemukan-yang memicu semuanya. Ia membolak-balik halaman, lalu berhenti di satu bagian yang mulai lusuh karena sering dibaca: simbol Aetherion.

Jari-jarinya menyusuri garis lambang itu.

Chandra: (pelan) "Apa kau juga bagian dari ini...?"

Di luar rumah, tak jauh dari pagar depan, Kael berdiri diam di balik pohon besar. Tatapannya tertuju ke jendela kamar Chandra.

Kael: (berbisik) "Jadi kau memang anaknya..."

Ia menatap langit sebentar. Lalu berbalik, bayangannya menghilang seiring desiran angin malam.

---

</p></div>
  <div id="bab5" class="section"><h2>Bab 5</h2><p>Dua hari setelah kejadian
Malam telah menelan langit sepenuhnya, menyisakan bintang-bintang yang menggantung seperti pengintai abadi. Di atas sebuah menara air tua, sosok bertudung hitam berdiri membisu. Angin malam menggoyangkan jubahnya, namun ia tidak bergeming. Matanya menatap lurus ke arah kota di kejauhan, di mana dua anak muda baru saja mulai memahami kekuatan mereka.

"Chandra dan Zenki," gumamnya pelan, seolah mengulang nama-nama yang baru ia pelajari. "Mereka belum siap... tapi mereka bisa menjadi aset-atau ancaman."

Tangannya membuka sebuah liontin kecil yang tergantung di lehernya. Di dalamnya, tergambar simbol kuno yang sama seperti yang ada di buku milik Chandra. Tatapannya menajam.

"Sudah lama sejak aku melihat simbol ini terakhir kali. Tidak kusangka, warisan itu muncul kembali."

Ia duduk di pinggir menara, memejamkan mata. Dalam pikirannya, suara-suara dari masa lalu kembali menggema-latihan yang brutal, pengkhianatan, dan sebuah organisasi yang menghilang tanpa jejak. Ia bukan sekadar pengamat. Ia pernah menjadi bagian dari semua itu.

"Ayahmu... Chandra. Apa kau benar-benar tahu siapa dia?" bisiknya, senyuman sinis menyungging di bibirnya.

Ia membuka matanya. Tatapan tajam dan dingin kembali terpancar. "Sudah saatnya aku mencari jawaban. Kalau buku itu memang warisan dari generasi sebelumnya, maka mereka tidak bisa dibiarkan berlatih tanpa pengawasan."

Ia melompat turun dari menara, mendarat dengan senyap di atap sebuah bangunan. Tubuhnya bergerak cepat, hampir tak terlihat di tengah bayang malam.

"Aku akan menguji mereka lagi. Tapi kali ini... bukan untuk mengalahkan."

Dia adalah Kael Varuna.

Dulu, ia adalah bagian dari organisasi rahasia bernama Aetherion, kelompok esper elit yang bertugas menjaga keseimbangan spiritual dunia-sampai satu peristiwa tragis menghancurkan segalanya. Pengkhianatan dari dalam membubarkan Aetherion, dan Kael adalah satu dari sedikit yang selamat.

Sejak itu, ia hidup dalam bayang-bayang, mengawasi kebangkitan kekuatan baru. Ia menyimpan dendam terhadap pengkhianat yang mengkhianati organisasinya, dan ia percaya semua yang berkaitan dengan simbol warisan harus diawasi-atau dimusnahkan.

Namun sesuatu dalam diri Chandra dan Zenki membuatnya ragu.

Mereka tidak seperti para esper yang dulu dia kenal.

---

---

Pagi itu, sekolah terasa ganjil. Langit memang cerah, tapi ada sesuatu di udara-getaran halus yang membuat kulit merinding. Chandra dan Zenki saling melirik saat memasuki kelas.

"Zenki, kau juga ngerasa?" bisik Chandra.

Zenki mengangguk. "Sejak bangun tadi. Aura itu... seperti ada yang mengawasi kita."

Hari berjalan lambat. Tapi perasaan ditekan itu tak juga menghilang. Di lorong kelas, di tangga belakang, bahkan di ruang guru yang biasanya aman-getaran aneh itu tetap ada. Tidak cukup kuat untuk mengganggu, tapi cukup untuk membuat jantung berdetak lebih cepat.

Saat bel pulang berbunyi, keduanya langsung berkemas.

"Kita ke kuil," kata Chandra pelan. "Kalau dia mau muncul, di sanalah tempatnya."

Zenki mengangguk. "Dan kita nggak sendiri. Aku yakin dia udah mengincar kita sejak pagi."

Langit mulai menguning saat mereka tiba di reruntuhan kuil. Tempat itu sunyi, tapi aura itu... semakin kuat, semakin dekat.

Lalu dia muncul.

Dari balik reruntuhan pilar, seorang remaja berdiri. Wajahnya teduh tapi tatapannya tajam, seolah bisa menembus kedalaman pikiran. Rambut hitamnya tergerai, dan di balik seragam sekolah yang dikenakan, ada aura pekat yang membuat Zenki refleks menaikkan pertahanannya.

"Jadi kalian yang selama ini membuat suara dunia ini bergetar," ucapnya pelan, hampir seperti gumaman.

Chandra melangkah maju. "Kau siapa?"

"Aku... Kael. Esper, seperti kalian. Tapi tak seperti kalian, aku tidak menunggu dunia meminta tolong."

"Artinya?" tanya Zenki.

Kael tersenyum tipis. "Artinya, aku sudah bosan menunggu. Dunia ini sakit, dan kadang... sesuatu harus dihancurkan sebelum bisa diperbaiki."

Aura spiritual Kael meledak. Tanah bergetar pelan, reruntuhan berderak, dan udara terasa semakin berat. Dari balik bayangan, semacam entitas hitam muncul di belakangnya-misterius dan berdenyut seperti kabut hidup.

Chandra merapat ke Zenki. "Kita nggak bisa ngomong baik-baik ya?"

Kael menatap mereka dengan pandangan dingin. "Buktikan dulu bahwa kalian layak bicara denganku."

Chandra dan Zenki berdiri di hadapan Kael, pemuda berambut hitam pendek dengan tatapan tenang namun tajam. Percakapan mereka baru saja mulai saat udara tiba-tiba menggetar pelan, seperti ada sesuatu yang bangun.

Suara gemuruh halus menggema dari dinding belakang kuil. Sebuah simbol retak memancarkan cahaya kehijauan yang merayap.

Zenki: "Apa itu...?"

Chandra mundur setengah langkah, bersiap memanggil energinya.

Kael tidak berkata apa-apa. Dalam sekejap, tubuhnya lenyap dalam bayangan, seolah tertelan senja. Suasana makin mencekam-langkah kaki tak terdengar, udara jadi dingin.

Tiba-tiba-CRACK!

Simbol pecah, dan energi negatif menyembur keluar, membentuk bayangan raksasa samar.

Namun sebelum makhluk itu sempat bergerak, sesosok bayangan muncul tepat di atasnya. Dalam gerakan cepat dan nyaris tak terlihat, Kael muncul kembali dari kegelapan, telapak tangannya menyentuh kepala makhluk itu.

Sebuah ledakan cahaya gelap menyelimuti makhluk itu... dan menghilang.

Chandra tertegun.
Zenki, dengan tatapan serius: "Apa barusan dia... menghilang?"

Kael melangkah keluar dari bayangan tiang kuil, seolah baru muncul dari tempat lain sepenuhnya.

Kael: "Tenang saja. Itu hanya segel tua yang lepas kendali. Tapi kuil ini tidak sepenuhnya mati, dan beberapa jebakan masih aktif. Jangan sentuh simbol sembarangan."

Chandra: (pelan) "Jadi ini kekuatanmu... kamuflase?"

Kael: "Kau bisa menyebutnya begitu. Aku menyebutnya Duskform."

----

Zenki melangkah mendekat, ekspresi wajahnya berubah menjadi lebih serius.
Zenki: "Teknik yang kau pakai tadi... bukan sembarangan. Itu bukan hanya kamuflase biasa."

Kael menoleh perlahan, tapi tak langsung menjawab.

Chandra: "Apa kau... pernah dilatih sebelumnya? Kau bukan anak biasa, bukan?"

Kael menghela napas pendek, lalu menyandarkan tubuhnya ke dinding batu kuil yang dingin. Matanya memandang jauh ke arah lubang cahaya di langit-langit yang memantulkan cahaya senja.

Kael: "Dulu, aku bagian dari sesuatu yang disebut Aetherion. Organisasi itu... sekarang sudah tak ada."

Keduanya saling bertatapan. Nama itu terasa asing, namun anehnya menggema dalam nurani mereka, seolah pernah terdengar dalam mimpi.

Zenki: "Aetherion? Itu... organisasi esper?"

Kael mengangguk pelan.
Kael: "Kami menjaga keseimbangan antara dunia manusia dan energi spiritual. Tapi waktu itu... sesuatu terjadi. Sesuatu yang membuat semuanya runtuh. Sejak saat itu, aku memilih diam."

Chandra: "Kenapa ada di sini sekarang?"

Kael: "Karena aku mencium bau yang sama... Energi yang dulu membuat Aetherion runtuh. Dan entah kenapa, kalian-"

Ia menatap Zenki dan Chandra dalam-dalam.

Kael: "-berada di pusatnya."

Suasana hening. Bayangan matahari sore mulai tertelan senja. Angin berdesir di antara celah kuil.

Zenki, pelan: "Kalau begitu... kita di jalan yang sama."

Kael: "Mungkin."

Chandra: "Dan kalau benar begitu... kau bersama kami sekarang?"

Kael tak menjawab langsung. Ia melangkah perlahan keluar dari naungan kuil, bayangannya seolah larut bersama senja.

Kael: "...Kita lihat saja nanti."

Kael menghilang ke balik reruntuhan, meninggalkan Chandra dan Zenki dalam keheningan. Tapi keheningan itu bukan kedamaian-melainkan awal dari sesuatu yang lebih besar.

Chandra menarik napas dalam. "Dia bukan musuh," ucapnya akhirnya. "Tapi bukan juga kawan."

Zenki mengangguk. "Tapi dia tahu lebih banyak dari kita... tentang Aetherion, tentang kekuatan ini."

Chandra dan Zenki masih berdiri di depan reruntuhan kuil yang kini terasa sunyi, seolah baru saja menyaksikan sesuatu yang tidak sepenuhnya bisa dimengerti. Cahaya matahari senja sudah hampir lenyap sepenuhnya, digantikan bayangan malam yang merambat pelan.

Zenki memegang lengan Chandra. "Kau yakin tentang dia?"

Chandra mengangguk perlahan, meski matanya masih menyisakan keraguan. "Aku nggak yakin bisa percaya dia... tapi aku tahu kita perlu dia."

Tiba-tiba, suara langkah terdengar dari sisi reruntuhan. Mereka refleks bersiap, namun yang muncul hanyalah siluet samar-Kael kembali, kali ini tanpa menyembunyikan kehadirannya.

"Aku akan bantu kalian," ucapnya datar. "Tapi bukan karena aku percaya pada misi kalian. Aku hanya ingin tahu... apakah kalian benar-benar pantas memegang warisan itu."

Zenki menyipitkan mata. "Warisan?"

Kael tak menjawab. Ia melemparkan sesuatu ke arah mereka-sebuah pecahan kristal berwarna hitam dengan jejak retakan ungu di dalamnya. Chandra menangkapnya dengan telekinesis secara refleks.

Chandra menggenggam pecahan kristal itu lebih erat, rasanya dingin dan berat-seperti membawa beban yang tidak terlihat. Zenki melirik ke arah pecahan tersebut, sorot matanya tak bisa menyembunyikan rasa penasaran.

"Apa maksudmu dengan 'dulu milik salah satu dari kalian'?" tanya Chandra, nada suaranya pelan tapi menuntut.

Kael menunduk, bayang-bayang senja menutupi setengah wajahnya. "Dia salah satu esper terkuat yang pernah kulihat. Tapi kekuatannya... terlalu besar untuk dunia ini. Dia percaya bisa menyatukan semua esper, tapi jalan yang dia pilih... berujung pada kehancuran."

Kael menatap langit yang mulai menggelap.

"Aku masih mengingat hari saat Aetherion runtuh. Api, suara-suara pengkhianatan, dan teriakan... teman-teman kami. Kami tak kalah oleh musuh. Kami dihancurkan oleh diri kami sendiri."

Chandra dan Zenki terdiam. Aura yang menyelimuti kuil menjadi lebih pekat, bukan karena kekuatan spiritual, tapi karena kenangan pahit yang mengendap di udara.

Chandra membuka mulut, tapi Kael lebih dulu bicara.

"Karena itulah aku menguji kalian. Aku perlu tahu... apakah kalian akan mengulangi kesalahan mereka."

Zenki menatap Kael lurus-lurus. "Dan setelah melihat kami... kau yakin?"

Kael tidak langsung menjawab. Ia mengangkat tangan, dan dari bayangan di belakangnya, sesosok entitas gelap perlahan muncul. Bentuknya kabur, berubah-ubah seperti asap, tapi di tengahnya bersinar sebuah kristal hitam-utuh, memancarkan aura senyap yang menelan cahaya di sekitarnya.

"Inilah kekuatanku yang sebenarnya-Duskform," ucap Kael. "Bayangan bukan sekadar tempatku bersembunyi. Aku adalah bayangan itu."

Entitas itu menyatu kembali ke tubuhnya, dan seketika angin berhembus kembali, seolah waktu baru saja bergerak lagi.

Zenki melangkah maju, wajahnya serius. "Kau menguji kami. Sekarang izinkan kami menguji balik."

Kael menaikkan satu alis. "Oh?"

Chandra tersenyum tipis. "Jika kau benar-benar bagian dari Aetherion... maka kau tahu pentingnya kepercayaan. Kau tahu seperti apa rasanya kehilangan rekan. Jangan jadikan kami musuh hanya karena bayang-bayang masa lalu."

Kael terdiam cukup lama. Angin malam meniup pelan helai rambutnya yang jatuh di dahi. Lalu ia berbalik, melangkah pergi-namun sebelum benar-benar menghilang ke dalam kegelapan, ia berhenti.

"Aku akan menghubungi kalian lagi. Tapi ingat... kepercayaan itu rapuh. Dan bayangan selalu mengawasi."

Lalu dia lenyap-seolah larut dalam udara malam.

Chandra dan Zenki saling pandang. Mereka tidak tahu apakah baru saja mendapatkan sekutu... atau musuh paling berbahaya.

---

Malam itu, di bawah cahaya bulan separuh, mereka berdiri di reruntuhan kuil yang kembali sunyi. Tapi kini, mereka tahu: mereka bukan lagi dua esper yang sendirian.

Mereka adalah bagian dari warisan yang lebih besar.

Dan bayangan dari masa lalu... perlahan mulai bangkit.

---

Malam turun sepenuhnya ketika Chandra dan Zenki berjalan pulang dari kuil. Langkah mereka lambat, tidak hanya karena tubuh yang lelah, tapi juga karena pikiran yang berat. Hening menyelimuti sepanjang perjalanan, hanya suara serangga malam yang menemani.

Setibanya di rumah, Chandra langsung mengunci pintu dan menjatuhkan tasnya di sofa.

"Ini gila," katanya pelan, menjatuhkan diri ke kursi. "Kael... Aetherion... semua ini makin rumit."

Zenki membuka kulkas, mengambil dua botol air dan melempar salah satunya ke arah Chandra. "Tapi itu juga berarti kita nggak salah jalan. Kita nggak berhalusinasi atau semacamnya. Semua ini nyata."

Chandra memandang ke arah meja, di mana buku tua pemberian ayahnya tergeletak. Simbol di sampulnya kini terasa lebih berat, seakan berdenyut dengan makna yang baru saja terbuka sebagian.

"Ayahku dulu bagian dari semua ini, ya?" gumamnya.

Zenki hanya diam, lalu duduk di sampingnya. "Mungkin kita nggak bakal dapet semua jawabannya sekarang. Tapi kita udah mulai jalan."

Setelah mandi dan berganti pakaian, keduanya duduk di lantai kamar, membentangkan kembali halaman-halaman buku yang lusuh itu. Ada banyak catatan, diagram, dan simbol. Tapi malam itu, satu halaman tampak berbeda.

Simbol kristal dengan enam warna-masing-masing mewakili kekuatan mereka-mulai bersinar samar. Cahaya biru di tengah berkedip pelan.

Chandra menatapnya dengan dalam. "Kael bilang kita ada di pusat semuanya. Kalau benar begitu, maka ini bukan cuma tentang bertahan... tapi memilih ke mana arah kekuatan ini dibawa."

Zenki tersenyum tipis. "Dan sepertinya kita nggak punya pilihan selain maju."

Keesokan harinya...

Cahaya matahari pagi menerobos jendela kamar, membangunkan Chandra dari tidurnya. Ia menggeliat malas, lalu menoleh ke arah Zenki yang sudah duduk di meja, membuka halaman-halaman buku tebal itu.

"Lo nggak tidur?" tanya Chandra sambil mengucek mata.

"Sebentar aja," jawab Zenki. "Buku ini... ada satu halaman yang baru muncul waktu lo udah tidur."

Chandra menghampiri, melihat halaman yang dimaksud. Sebuah simbol baru terukir samar-bentuknya seperti topeng runcing dengan mata hitam kosong.

"Apa ini...?"

"Sesuatu yang nggak enak. Dan firasatku bilang, itu bakal muncul hari ini."

---

Di sekolah...

Hari berjalan seperti biasa-sampai mereka sampai di lorong dekat ruang musik. Udara mendadak jadi lembap, seperti habis hujan, padahal cuaca di luar terang. Beberapa siswa mengeluh merasa pusing, dan beberapa lainnya mendadak panik melihat bayangan aneh di cermin kelas.

Chandra dan Zenki saling pandang. Aura itu familiar-gelap dan menekan, tapi juga... kelaparan.

"Di ruang musik," bisik Zenki.

Mereka menyelinap ke sana saat bel istirahat. Ruangan kosong, tapi udara di dalamnya terasa seperti menggantung-tebal dan berat.

Lalu... terdengar suara.

"Kelaparan... jiwa... suara..."

Sebuah bayangan muncul di pojok ruangan, membentuk sosok menyerupai manusia, tapi wajahnya kosong seperti topeng. Mulutnya terus membuka, seolah-olah menyerap suara di sekitarnya.

Chandra menarik napas dalam. "Roh jahat."

Zenki mengangkat tangannya, aura ungu dari Nethermind mulai mengalir. "Kita tangkap ini cepat, sebelum ada yang lihat."

Roh itu mengaum-suara seperti serak angin dan logam. Ia melesat ke arah mereka dengan gerakan terputus-putus, seperti film rusak. Tapi Chandra mengangkat tangannya, dan benda-benda di sekeliling langsung beterbangan, membentuk penghalang. Meja piano melayang di udara, menghantam roh itu dari samping.

Zenki melompat, telapak tangannya menyentuh bayangan itu. Energi ungu menyerap masuk, mencoba menahan roh tersebut di dalam pikirannya.

Namun roh itu memberontak. Tiba-tiba, ia mengeluarkan teriakan melengking-frekuensi tinggi yang membuat kaca jendela bergetar hebat dan memecah.

Chandra berteriak. "Aku nggak bisa tahan lama!"

Telinga Chandra berdering akibat jeritan roh itu. Ia mengerjap-lalu menyadari sesuatu yang aneh.

Ruangan berubah.

Piano di pojok kini tampak usang dan berdebu, tirai jendela berkibar meski tak ada angin. Warna ruangan memudar, seperti lukisan yang dilunturkan air. Udara kental dengan gema bisikan, dan bayangan-bayangan samar bergerak di dinding.

"Dia tarik kita masuk ke... Dimensi Roh," desis Zenki, wajahnya pucat.

Lantai seperti berkabut, dan cermin-cermin di ruangan memantulkan sosok yang bukan milik mereka. Sosok lain-tak bernama, tanpa wajah.

Chandra mencengkeram lengan kursi piano yang melayang, lalu sadar benda itu tak benar-benar ada. Semuanya di sini adalah pantulan, tiruan. Dunia ini... meniru dunia nyata, tapi tanpa kehidupan.

Roh itu muncul lagi, kini lebih besar, tubuhnya menggumpal seperti awan tinta dalam air. Suaranya menggema tanpa arah. "Kelaparan... suara... suara kalian... kuat..."

Zenki berdiri, energi Nethermind menjalar di telapak tangannya.

"Kita harus selesaikan ini di sini. Kalau tidak, dia bisa tembus ke dunia nyata."

Chandra mengangguk, lalu melemparkan kesadarannya ke sekeliling. Di dunia ini, batas antara pikir dan benda jauh lebih tipis. Telekinesisnya tak hanya mengangkat-ia membentuk ulang. Ia mengumpulkan serpihan dari 'suara'-gema percakapan yang tersisa di dinding ruang musik bayangan itu-dan membentuknya menjadi penghalang berbentuk spiral.

Roh itu menghantam spiral suara itu, lalu menjerit saat tubuhnya retak oleh bentuk suara yang tak bisa ia kendalikan.

Zenki melompat masuk ke tengah spiral, mengukir simbol Nethermind dengan energi pikirannya. Rune ungu menyala, lalu memancar ke seluruh dimensi.

"Kunci suara... segel ilusi..." bisiknya.

Roh itu mencoba kabur, tapi ruangan mulai runtuh-bukan hancur, tapi "menguap", perlahan-lahan larut menjadi cahaya putih.

Chandra memejamkan mata.

Saat ia membukanya-

Mereka kembali di ruang musik.

Piano utuh. Cermin tak pecah. Meja dan kursi rapi seperti biasa.

Seakan tak pernah terjadi apa-apa.

Zenki berdiri perlahan, keringat dingin masih menetes di dahinya. "Kita keluar... tepat waktu."

Chandra menatap ke arah cermin. Di sana, tak ada apa pun-hanya bayangan dirinya sendiri.

---

Di atap sekolah, sore harinya...

Langit mulai memerah saat Kael berdiri membelakangi matahari, memandangi lapangan sekolah yang perlahan sepi. Ia menyaksikan dua sosok keluar dari gedung musik-Chandra dan Zenki, dengan langkah lelah tapi wajah waspada.

Kael menyipitkan mata. "Mereka bergerak cepat."

Suara-suara samar kembali bergema di kepalanya-kenangan masa lalu saat Aetherion pernah mengurung roh serupa di lokasi lain. Tapi roh tadi... bukan sembarangan.

Ia melangkah mundur dari tepian atap dan menyentuh liontin di lehernya.

"Segel tua yang rusak... dan simbol itu muncul lagi. Dunia spiritual mulai retak, dan mereka terjun ke dalamnya begitu saja."

Wajahnya datar, tapi ada kilatan rasa penasaran dan... keterlibatan.

---

Sementara itu, di lorong sekolah yang sepi...

Langkah Chandra dan Zenki terhenti.

Kael muncul dari ujung lorong, bersandar santai ke dinding dengan tangan di saku. Tatapannya tajam seperti biasa, tapi kali ini ada sedikit nada menguji.

Kael: "Kalian berdua... membuat gempar satu gedung dengan roh kelas-C. Menarik."

Chandra, heran: "Kau ngikutin kita?"

Kael mengangkat bahu. "Mengamati."

Zenki: "Itu bukan roh biasa. Dia... seperti mengincar sesuatu."

Kael: "Dia memang bukan roh biasa. Namanya Voidsong. Dulu, kami segel dia jauh di bawah kuil. Tapi tampaknya waktu sudah melemahkan segalanya." (diam sebentar) "Dan kini, segel itu-dan dunia ini-mulai retak lagi."

Chandra: "Lalu kenapa kau biarkan kami melawan sendirian?"

Kael menatap Chandra, tajam. "Karena kalian harus belajar. Aetherion tidak pernah berdiri dengan tangan gemetar."

Zenki menghela napas. "Apa kau mau kami mati?"

Kael: "Kalau kalian mati hari ini, kalian tidak pantas menyentuh warisan itu."

Hening. Suasana tegang. Tapi Kael kemudian berjalan mendekat dan menjatuhkan sesuatu-sepotong kristal hitam kecil, berbentuk belah ketupat.

Kael: "Itu milikku dulu. Simpan. Aku akan tahu jika sesuatu mendekat lagi."

Chandra mengambil kristal itu, menatapnya bingung.

Kael berjalan pergi, dan sebelum menghilang di balik bayangan, ia menoleh:

Kael: "Besok... kalian harus mulai mencari tahu apa yang sebenarnya kalian warisi. Sebelum segalanya terlambat."

---

Malam hari, rumah Chandra.

Lampu ruang tengah menyala lembut, memantulkan cahaya ke dinding yang dipenuhi rak buku dan foto keluarga. Di atas meja makan, dua cangkir teh masih mengepulkan uap. Chandra duduk menyandar di kursi, menatap langit-langit, sementara Zenki bersandar di dinding, tangan terlipat.

Chandra: "Hari ini... aneh banget."

Zenki mengangguk pelan. "Kita hampir dilahap roh kuno, Kael nongol lagi, dan sekarang... kita punya batu misterius ini."

Ia menaruh kristal hitam Kael di meja. Kristal itu berdenyut samar, seperti merespons udara malam.

Chandra: "Menurutmu Kael percaya kita bisa mengatasinya?"

Zenki: "Aku rasa... dia lebih percaya kalau kita akan mati dan menyaring siapa yang pantas lanjut."

Chandra tertawa hambar. "Klasik Kael."

Suasana hening sejenak. Di luar, suara jangkrik mulai terdengar. Angin malam masuk dari jendela yang terbuka, membawa aroma dedaunan basah.

Zenki: "Aku sempat lihat sesuatu di mata Voidsong tadi."

Chandra menoleh. "Apa?"

Zenki menunduk. "Seperti... rasa takut. Seolah dia melarikan diri dari sesuatu yang lebih besar."

Chandra mengerutkan alis. "Kau yakin?"

Zenki: "Aku tahu bagaimana takut itu terlihat. Dia... bukan datang untuk menyerang. Dia kabur."

Mereka saling tatap. Pemikiran itu membuat suasana jadi lebih berat.

Chandra: "Jadi kita belum lihat musuh sebenarnya."

Zenki: "Belum. Dan Kael tahu itu."

Chandra berdiri, menatap ke luar jendela. "Kalau begitu... kita harus lebih kuat. Besok, kita mulai pelajari apa pun yang bisa kita temukan soal Aetherion."

Zenki tersenyum tipis. "Kita?"

Chandra: (menoleh dan menyeringai) "Kau pikir aku bakal biarin kau jadi pahlawan sendirian?"

---

bergerak ke arah kristal hitam di meja.

Kilatan energi samar keluar darinya, menciptakan bayangan kecil di dinding... bayangan itu bukan milik siapa pun yang ada di ruangan.

Dan di tempat jauh... seorang sosok membuka matanya perlahan.

???: "...Warisan itu telah bangkit."

Chandra mematikan lampu ruang tengah, menyisakan cahaya dari kamar tidurnya yang terbuka sedikit. Ia berjalan ke dapur, mengambil segelas air, lalu menatap cermin kecil di lemari es.

Tatapannya kosong.

Chandra: (berbisik) "Ayah... Kau pernah tahu soal ini, kan?"

Ia membuka laci, mengeluarkan buku tua yang sebelumnya ditemukan-yang memicu semuanya. Ia membolak-balik halaman, lalu berhenti di satu bagian yang mulai lusuh karena sering dibaca: simbol Aetherion.

Jari-jarinya menyusuri garis lambang itu.

Chandra: (pelan) "Apa kau juga bagian dari ini...?"

Di luar rumah, tak jauh dari pagar depan, Kael berdiri diam di balik pohon besar. Tatapannya tertuju ke jendela kamar Chandra.

Kael: (berbisik) "Jadi kau memang anaknya..."

Ia menatap langit sebentar. Lalu berbalik, bayangannya menghilang seiring desiran angin malam.

---

Dalam bayang ingatan yang samar, Zenki berdiri di tengah reruntuhan kuil kuno yang tak pernah ia lihat sebelumnya. Di sekelilingnya, pilar-pilar retak menjulang seperti tulang-tulang purba, memancarkan cahaya ungu yang samar. Di tengah altar melayang sebuah batu kecil, berwarna ungu tua, berdenyut pelan seperti jantung yang tertidur.

Suara lirih, nyaris seperti bisikan dari dalam dirinya sendiri, menyebut satu nama: Nethermind.

Zenki terbangun dari mimpi itu dengan napas terengah. Keringat dingin membasahi dahinya. Ia duduk di tepi tempat tidur, tangannya mencengkeram kain seprai. Di luar, fajar baru menyingsing, tetapi ketenangan pagi tak sanggup menghapus gema mimpi tadi.

"Aku pernah melihat tempat itu..." gumamnya, lebih kepada dirinya sendiri.

Sejak pertemuan dengan makhluk bayangan di ruang musik, sesuatu dalam dirinya berubah. Nethermind, kekuatan yang selama ini ia pikir hanya sebatas membaca pikiran dan menjelajahi lapisan kesadaran, kini mulai menariknya lebih dalam. Ada ruang baru-gelap, dalam, dan seakan memanggil. Ia merasakannya setiap kali ia diam terlalu lama. Seolah ada sesuatu di balik batas pikirannya, menunggu untuk ditemukan.

Kael, yang sejak beberapa hari terakhir ikut tinggal sementara bersama mereka, memperhatikan perubahan itu. Suatu malam, ia bicara pelan saat mereka duduk di halaman belakang.

"Nethermind... bukan kekuatan biasa. Itu bukan cuma kunci untuk memasuki pikiran orang lain. Itu adalah pintu ke dimensi antara jiwa dan kehendak. Dan kalau kau sudah mulai melihat batu itu... berarti waktumu mendekat."

Zenki menatap Kael. "Batu itu memang nyata?"

Kael mengangguk, lalu membuka telapak tangannya. Batu hitam kecil yang selalu ia simpan berkilau samar di bawah cahaya bulan.

"Setiap esper yang melewati ambang tertentu... akan dipanggil oleh batu mereka. Kau belum memegangnya, tapi kau sudah dipanggil."

Zenki menggertakkan gigi. "Jadi... aku harus siap?"

"Tidak. Kau harus bertanya pada dirimu sendiri... apakah kau berani masuk lebih dalam."
----

Keesokan harinya, suasana sekolah tidak seperti biasa. Ada keheningan yang menekan, meskipun bel berbunyi dan siswa lalu-lalang seperti biasa. Zenki berjalan berdampingan dengan Chandra, tetapi pikirannya tak lepas dari mimpi, batu, dan ucapan Kael semalam.

"Ruang musik masih disegel," bisik Chandra. "Tapi aura itu... masih terasa."

Zenki hanya mengangguk. Ia bisa merasakannya juga. Seperti getaran di udara yang hanya dia yang peka. Tiap langkah mendekati gedung seni membuat dadanya terasa berat, seolah langkah-langkahnya menuju takdir yang sudah menunggu.

Di sela jam kosong, Kael menyusup lewat pintu samping dan membawa mereka ke ruang peralatan musik lama, yang terhubung dengan ruang utama melalui lorong tersembunyi. Debu, bau kayu tua, dan gemuruh samar seperti bisikan samar di telinga langsung menyergap mereka.

"Aura spiritual meningkat di sini," kata Kael, berdiri tenang seperti penjaga gerbang dunia lain.

Zenki melangkah ke tengah ruangan, tepat di mana simbol muncul sebelumnya. Tak ada tanda batu, tak ada pilar-namun dunia tak kasat mata di sekitarnya terasa bergerak, berputar pelan.

Chandra memperhatikan Zenki yang memejamkan mata. "Kau oke?"

"Diam." Kael mengangkat tangan pelan. "Dia akan masuk."

Dan saat itu terjadi.

Dunia di sekitar Zenki memudar. Suara menghilang. Ia terhuyung, jatuh ke lutut-tapi tak terasa. Ia membuka mata, dan dunia telah berubah.

Ia berdiri lagi di kuil itu.

Pilar-pilar ungu menjulang, langitnya kelam seperti malam tanpa bintang. Di hadapannya, altar dengan batu ungu yang kini menyala lebih terang.

Langkah kaki menggema di belakangnya.

Zenki berbalik, dan melihat sosok-bukan bayangan, bukan manusia. Sosok berjubah kelam dengan wajah tak terlihat, hanya dua mata bercahaya ungu yang menatapnya tanpa ekspresi.

"Selamat datang, pewaris Nethermind," suara itu bergema, seakan dari dalam pikirannya sendiri.

"Siapa kau?" tanya Zenki.

"Aku adalah penjaga antara kesadaran dan kehendak. Dan kau telah tiba di ambangmu."

Tiba-tiba, tanah retak. Pilar-pilar berguncang. Dari kegelapan muncul bentuk-bentuk kabur-kenangan buruk, trauma lama, ketakutan yang Zenki pikir telah ia kubur. Semua muncul dalam bentuk wujud bayangan, mengelilinginya.

"Inilah syaratnya," suara itu berkata lagi. "Hadapi bayangan jiwamu. Hanya mereka yang mampu menatap gelapnya pikiran mereka sendiri yang berhak menerima Batu Nethermind."

Zenki menelan ludah. Tubuhnya gemetar, tapi ia menggenggam kedua tangannya erat. Ia tahu-ini bukan pertarungan fisik. Ini adalah pertarungan batin. Dan kalau ia kalah... ia akan tersesat dalam dimensi Nethermind selamanya.

Di dunia nyata, Chandra melihat tubuh Zenki bergetar, peluh mengucur dari wajahnya. Kael berdiri di belakangnya, mata tajam seperti elang.

"Jangan ganggu dia," kata Kael. "Kalau dia bisa mengalahkan dirinya sendiri... kita akan melihat batu itu muncul."

Dan dalam dunia spiritual, Zenki pun maju selangkah.

Menuju bayangan jiwanya.

---

Zenki maju satu langkah, lalu dua. Bayangan-bayangan yang mengelilinginya tak bergerak. Mereka hanya menatap, dengan wajah-wajah yang aneh-sebagian menyerupai orang yang pernah ia kenal, sebagian lagi seperti cermin buram dari dirinya sendiri. Tapi di tengah semuanya, satu sosok muncul lebih jelas dari yang lain.

Dia berdiri tenang, mengenakan pakaian yang sama seperti Zenki, bahkan luka kecil di dagu pun sama. Namun matanya-mata itu-berkilau ungu sepenuhnya. Dingin. Kosong. Dan ketika ia bicara, suaranya identik dengan milik Zenki, tapi lebih datar.

"Akhirnya kau datang," kata sosok itu.

Zenki mematung. "Kau..."

"Aku adalah kau, tapi tanpa keraguan. Tanpa penyesalan. Tanpa rasa takut. Aku adalah bentuk murni dari kehendakmu, jika kau membuang semua kelemahan itu."

Zenki menggertakkan gigi. "Kau bukan aku."

Sosok itu menyeringai kecil. "Kalau begitu, buktikan."

Tanpa aba-aba, dunia di sekeliling mereka runtuh. Pilar-pilar ungu hancur menjadi serpihan cahaya. Dan dari reruntuhan itu, mereka berdua melesat saling serang.

Pikiran bentrok. Gambar-gambar masa lalu terpantul seperti cermin pecah-wajah ibunya yang meninggal terlalu dini, malam-malam sepi di rumah sakit, rasa tidak pernah cukup baik, ketakutan bahwa kekuatannya akan membuatnya kehilangan kendali.

Zenki terdorong ke belakang, napasnya berat. Dirinya yang lain muncul di hadapannya, membentuk tombak ungu dari energi murni Nethermind.

"Kau lemah karena terlalu banyak peduli," ucapnya, melemparkan tombak itu.

Zenki menghindar, tapi ujung tombak itu melukai lengannya. Luka itu tidak hanya fisik-tapi terasa seperti menyayat batinnya.

"Tapi justru karena aku peduli... aku kuat," gumam Zenki.

Ia memejamkan mata. Dalam keheningan itu, ia mendengar suara Chandra, samar tapi jelas. "Kau gak sendiri, Zenki..."

Ia membuka mata.

Dan kali ini, energi ungu di sekeliling tubuhnya berubah. Lebih tenang. Lebih stabil.

"Nethermind... bukan tentang menyingkirkan rasa takut," katanya sambil berdiri tegak. "Ini tentang memahami diriku, seluruhnya... bahkan sisi gelapku."

Tangan Zenki terangkat, dan sebuah simbol muncul di udara-pilar ungu yang sekarang bercahaya dari dalam. Sosok "Zenki bayangan" mulai retak, kilau tubuhnya meredup.

"Kalau kau benar-benar aku... maka kau tahu aku tidak akan lari dari diriku sendiri."

Cahaya pilar itu meledak, melingkupi keduanya.

Dan saat cahaya memudar...

Zenki berdiri sendirian di altar. Batu kecil berwarna ungu tua melayang perlahan ke arahnya, lalu jatuh tenang di telapak tangannya.

Nethermind telah mengakui dirinya.

Di dunia nyata, Zenki terbangun dengan tubuh gemetar. Ia duduk perlahan, dan saat membuka tangannya, Chandra terkejut.

Sebuah batu kecil berwarna ungu tua ada di sana, berdenyut pelan seperti jantung.

Kael tersenyum tipis. "Dia kembali."

Chandra berbisik, "Zenki..."

Dan Zenki, meski masih lemah, menatap mereka dengan mata baru-mata yang telah menatap ke dalam dirinya sendiri... dan kembali dengan kekuatan yang lebih dalam.

Kael membantunya berdiri. "Kau harus belajar mengendalikannya. Sekarang kau tak hanya punya akses ke pikiran orang lain... kau punya pintu ke kedalaman jiwa. Termasuk jiwamu sendiri."

Tiba-tiba, suara seperti gesekan geser terdengar dari balik dinding ruang musik. Aura gelap yang sebelumnya hanya samar kini terasa lebih jelas, lebih padat. Chandra dan Zenki saling berpandangan.

Zenki memejamkan mata, memegang batu Nethermind.

Dan saat ia membukanya kembali, matanya menyala ungu, pupilnya berubah bentuk seperti spiral.

"Ada yang bersembunyi di balik tembok itu," ucapnya pelan. "Tapi bukan manusia."

Ia melangkah maju, dan sesuatu terjadi-udara di sekelilingnya bergelombang. Sebuah lingkaran ungu terbentuk di bawah kakinya, dan sekejap kemudian, seluruh ruangan berubah. Chandra dan Kael melihat sekeliling mereka tiba-tiba diliputi kabut ungu, suara lenyap, dan waktu seakan melambat.

Kael bergumam, "Ini... ruang batin Nethermind..."

Zenki berdiri di tengah lingkaran, menatap tembok tempat aura gelap itu berasal.

"Satu cara untuk menghadapinya," katanya. "Tarik dia ke sini."

Tangan Zenki terangkat. Aura ungu menyambar ke tembok, dan... makhluk bayangan muncul-terseret masuk ke dalam dimensi Nethermind milik Zenki.

Bentuk makhluk itu tak stabil-berdenyut seperti amarah tanpa wujud. Tapi di dalam ruang ini, Zenki bisa melihat lebih dalam: sosok itu adalah potongan kenangan. Fragmen penderitaan. Seperti residu spiritual dari seseorang... atau sesuatu yang pernah ada.

Zenki melangkah maju, aura ungu mengalir dari tubuhnya.

"Aku tidak akan melawanmu dengan rasa takut," katanya, "tapi dengan kejelasan."

Ia mengangkat tangannya, dan dari batu Nethermind, cahaya membentuk pedang tipis dari energi mental.

Pertarungan dalam Nethermind baru saja dimulai.

Dalam ruang Nethermind...

Langkah Zenki menggema di antara kehampaan ungu. Pilar-pilar cahaya menyala redup di sekelilingnya, berdenyut mengikuti irama jantungnya. Di seberangnya, makhluk bayangan itu berdiri. Ia tak memiliki wajah, hanya bentuk humanoid gelap yang tampak bergetar, seperti sedang menahan kesakitan.

Namun Zenki bisa merasakannya. Perasaan itu-kehilangan, kemarahan, ketakutan-mengalir seperti kabut dingin menyelubungi pikirannya.

"Aku tahu kau bisa mendengarku," ucap Zenki pelan. Suaranya bergema, bukan lewat udara, tapi lewat dinding-dinding batin. "Kau bukan sekadar monster. Kau... pernah jadi manusia."

Makhluk itu menggeram, dan bayangannya mencuat tajam, membentuk semacam duri-duri emosional. Tapi Zenki tetap berdiri.

"Kau merasa dikhianati, ya?" lanjutnya. "Ditinggalkan."

Seketika, makhluk itu menjerit-sebuah raungan batin yang membuat ruang Nethermind bergetar. Sekilas, tubuhnya berubah: dari bentuk bayangan menjadi siluet seorang anak muda. Rambut acak-acakan. Seragam sekolah lusuh. Mata penuh luka, bukan secara fisik... tapi jiwa yang koyak.

Zenki terdiam. "Siapa namamu?"

Siluet itu tidak menjawab. Namun gelombang emosinya mengalir deras-membentuk potongan-potongan ingatan di udara: bayangan ruang kelas kosong, suara tawa yang perlahan hilang, buku-buku berserakan, lalu... sepi. Sepi yang dalam dan panjang.

Zenki mendekat, satu langkah, lalu dua.

"Aku juga pernah sendirian," ucapnya lirih. "Merasa nggak ada yang ngerti. Nggak ada yang bisa bantu. Tapi kau nggak harus tetap terperangkap di sini."

Makhluk itu menggigil.

"Biar aku bantu," bisik Zenki, kini berdiri di depannya. Ia mengulurkan tangan.

Bayangan itu terdiam. Perlahan, satu tangan hitam-retak dan rapuh-terangkat. Menyentuh jari Zenki. Saat itu juga, gelombang energi meledak lembut, dan ruang Nethermind mulai tenang.

Cahaya ungu menyelimuti keduanya. Perlahan, bayangan itu mulai memudar-tapi bukan menghilang. Ia terserap ke dalam batu kecil yang terbentuk di udara. Kristal ungu muda. Jernih. Tenang.

Zenki memandanginya sejenak. "Kau bebas sekarang."

Suara lirih muncul di benaknya, entah dari siapa: Terima kasih...

semuanya tenang, Zenki berdiri di tengah ruangan dengan batu Nethermind di tangannya. Chandra dan Kael memandanginya, terkejut dengan perubahannya yang begitu besar.

Chandra memiringkan kepala, menatap Zenki yang kini tampak lebih tenang, dengan mata yang masih menyala ungu. Lalu, ia mengangkat alis sambil berkata dengan nada bercanda.

"Jadi, Zenki, ini semua tentang kamu aja ya? Gue kayak nggak kebagian apa-apa nih."

Zenki sedikit tersenyum, meski masih sedikit lelah. "Kamu nggak perlu masuk ke Nethermind juga, Chandra. Cuma kalau kamu mau, bisa aja. Gue nggak tahu, sih, bakal ada 'boss level' yang cocok buat kamu."

Chandra tertawa ringan. "Aduh, jadi gue cuma jadi penonton gitu aja, ya? Bosen banget, deh!"

Zenki menyeringai. "Tenang aja, siapa tahu nanti ada giliran kamu. Gue butuh juga kok dukungan dari orang-orang yang ngerti situasi kayak kamu."

Chandra mengangguk santai. "Oke, kalau gitu gue siap jadi support-nya kamu... dari belakang."

Dengan tawa ringan, ketiganya berjalan keluar dari ruang peralatan musik. Meskipun masih ada ancaman yang mengintai, setidaknya ada sedikit ketenangan yang muncul, dan mereka bisa menikmati momen itu, meskipun sebentar.

Setelah kejadian di ruang musik dan pertempuran Zenki dengan makhluk bayangan, Chandra merasa semakin bingung dengan kekuatan yang muncul dalam dirinya. Mereka berjalan kembali ke halaman belakang, duduk di bawah pohon rindang, sementara Kael merapikan beberapa peralatan di dekat mereka.

Chandra akhirnya memutuskan untuk berbicara.

"Kael..." suara Chandra terdengar ragu. "Kau pernah bilang, setiap esper memiliki kekuatan yang unik, kan?"

Kael menoleh dan mengangguk. "Benar. Semua kekuatan itu adalah cerminan dari pikiran dan jiwa penggunanya."

Chandra mengerutkan kening, berpikir sejenak. "Tapi, aku... aku nggak ngerti kenapa kekuatanku bisa seperti ini. Aku bisa menggerakkan benda dengan pikiran, dan semakin kuat semakin terasa... seperti ada sesuatu yang aku kontrol, tapi aku nggak tahu bagaimana cara mengendalikannya dengan tepat."

Kael mengamati wajah Chandra sejenak, kemudian menghela napas. "Kekuatanmu itu telekinesis, tapi tidak seperti yang kau kira. Ini lebih dari sekadar memindahkan objek fisik."

"Apa maksudmu?" tanya Chandra, sedikit bingung.

Kael tersenyum tipis, seolah ada sesuatu yang menarik baginya dalam memahami kekuatan Chandra. "Kekuatan telekinesis milikmu sepertinya terhubung dengan pikiran yang lebih mendalam. Seiring waktu, kekuatan itu mungkin mulai berhubungan dengan sesuatu yang lebih besar-semacam kontrol atas ruang atau energi mental. Kau bisa menggerakkan benda-benda di sekitarmu, tetapi ada potensi lebih dalam dirimu yang perlu dipahami."

Chandra memutar bola matanya, agak jengkel. "Jadi aku harus nunggu sampai aku bisa menggerakkan dunia atau apa? Ini nggak masuk akal! Aku cuma ingin tahu cara buat ngontrolnya tanpa... terlalu bikin kekacauan."

Kael tertawa pelan. "Jangan terlalu terburu-buru. Kekuatannya akan berkembang seiring pengalaman dan latihan. Kau akan mulai mengerti saat waktunya tiba. Jangan khawatir, kami di sini untuk membantu."

Chandra menatap Kael dengan wajah serius, meski sedikit cemas. "Tapi, apa ada cara cepat buat ngerti semua ini? Kadang aku merasa kekuatanku bisa lebih berbahaya daripada yang aku kira."

Kael menatapnya dalam-dalam, seolah menilai. "Kadang-kadang, kekuatan yang besar itu memang terasa berat. Tapi, ingatlah ini: Kekuatan sejati berasal dari pengendalian diri, bukan sekadar kemampuan fisik."

Chandra mengangguk, meski masih merasa bimbang. "Oke, kalau begitu. Aku akan coba lebih sabar, meskipun nggak gampang."

Kael meletakkan tangan di bahunya. "Itulah yang aku suka tentangmu, Chandra. Kamu nggak mudah menyerah."

****

Keesokan harinya, suasana pagi di rumah Zenki terasa lebih tenang. Cahaya matahari masuk melalui jendela dapur, sementara Chandra sedang mengaduk serealnya. Zenki duduk di seberangnya, masih menatap buku warisan yang belum sempat ia baca lebih dalam. Kael berdiri di ambang pintu, secangkir kopi hitam di tangannya.

Chandra memecah keheningan dengan bercanda, "Masih enak ya hidupnya, kalian berdua, bisa ngilang-ngilang atau masuk ke pikiran orang. Gue? Ngangkat-ngangkat barang, kayak tukang pindahan spiritual."

Zenki tersenyum, kemudian menyahut, "Tapi lo udah nutup pintu dengan tangan lo sendiri, itu juga keren."

Kael menyarankan, "Telekinesis bukan cuma soal ngangkat barang, Chandra. Kalau lo fokus, lo bisa ngeraih hal-hal yang nggak keliatan sama orang lain. Bisa lebih dari sekadar ngegerakin benda."

Chandra cuma mengangkat bahu, "Ya, gue sih belum pernah coba. Kalau bisa ngambil cemilan dari dapur tanpa berdiri, baru gue percaya."

Zenki ikut menambahkan, "Lo bisa jadi punya tangan kedua, Chandra. Bisa ngelakuin banyak hal sekaligus, bahkan ngelindungin diri lo sendiri."

Kael tersenyum pelan, "Lo udah mulai pakai kekuatan itu tanpa lo sadar. Kadang kita gak tahu seberapa besar kekuatan kita sampai kita berani nyoba."

Chandra tertawa ringan. "Hmm, mungkin sih... tapi gue tetep lebih tertarik sama kekuatan buat ngambil cemilan dari jarak jauh."

</p></div>
  <div id="bab6" class="section"><h2>Bab 6</h2><p>Langit mendung menggantung rendah di atas kota, seolah ikut merunduk bersama perasaan Chandra. Sekolah sedang libur, tapi pikirannya jauh dari istirahat. Ia bangun lebih pagi dari biasanya, dan tanpa banyak berpikir, mengenakan jaket lalu keluar rumah. Meninggalkan suara Zenki dan Kael yang samar terdengar dari ruang tengah.

Ia butuh sendiri. Butuh hening. Tapi hening tidak datang meski ia berjalan jauh dari rumah.

Langkah-langkahnya membawanya ke tempat yang asing tapi familiar - gang sempit di belakang gedung ruko tua, tempat ia pertama kali mempertanyakan kekuatan yang dimilikinya. Tempat di mana ia melawan sekelompok preman yang kini jadi bagian dari sejarah yang ingin ia lupakan... atau mungkin, ingin ia ulangi.

Chandra berdiri di tengah lorong itu. Bau tembok lembap dan sisa rokok masih sama. Tapi yang berbeda adalah dadanya yang penuh. Penuh rasa tertinggal. Penuh amarah. Penuh tanya.

"Zenki sudah dapat batunya... Kael selalu tahu apa yang dia lakukan..."

Tangannya mengepal. Ujung jarinya gemetar.

Dan tanpa sadar, tong sampah di pojok lorong terangkat lalu mental membentur dinding dengan keras.

"Lalu... aku?"

Suara langkah terdengar. Beberapa preman muncul dari pojokan yang gelap. Wajah mereka menyiratkan ingatan buruk akan kekalahan. Tapi kali ini, mereka melihat sesuatu yang berbeda di mata Chandra.

Kali ini, bukan hanya kekuatan yang meledak. Tapi juga kehilangan arah.

"Heh, kamu lagi," kata salah satu preman, dengan senyum sinis, "Kamu pikir bisa ngalahin kita lagi?"

Chandra hanya menatap mereka dengan tatapan tajam. Semua amarah yang terpendam kini bergejolak, dan tanpa berkata-kata lebih lanjut, ia melangkah maju. Bukan untuk berbicara, tetapi untuk mengeluarkan apa yang sudah terlalu lama ia pendam.

Dengan satu gerakan, tangan Chandra terangkat, dan tong sampah di ujung lorong melayang tinggi, berputar cepat seperti benda yang terperangkap dalam arus angin kencang. Tanpa peringatan, ia melemparkan tong sampah itu dengan keras ke arah pemimpin preman. Tubuh pria itu langsung terlempar ke dinding.

Preman-preman yang lain, yang terkejut dengan serangan mendadak, mencoba bergerak, tapi mereka terlambat. Chandra sudah berada di depan mereka dalam sekejap, tangannya bergerak cepat, mengirimkan tendangan yang begitu keras hingga salah satu dari mereka jatuh terpelanting.

"Kenapa... kalian selalu mengganggu?" suara Chandra terdengar keras, penuh tekanan, dan lebih dari sekadar pertanyaan. Itu seperti sebuah pertarungan melawan bayangannya sendiri, melawan keraguan yang terus mengganggunya.

Salah satu preman yang masih berdiri mencoba untuk merespon, tetapi ia segera terhenti ketika tubuh Chandra bergerak lagi, memanfaatkan kekuatan telekinesisnya untuk menghimpit pergerakan lawan. Kali ini, bukan sekadar dorongan, tetapi tekanan luar biasa yang membuat mereka terdiam.

"Apa kalian pikir aku masih sama seperti dulu?" Chandra bertanya, suaranya penuh dengan kekuatan yang lebih dari sekadar fisik. "Aku nggak butuh alasan untuk melawan. Aku cuma ingin tahu... kenapa aku merasa kosong."

Dengan satu gerakan, Chandra melepaskan genggaman kekuatannya. Semua benda yang terbang kembali jatuh ke tanah, dan keheningan kembali menyelimuti lorong. Preman-preman itu terdiam, sebagian terengah-engah, sementara Chandra berdiri dengan nafas sedikit tersengal.

Dia berbalik, dan tanpa menghiraukan mereka lagi, berjalan pergi. Tanpa kata, tanpa balasan. Kekuatan yang baru saja ia lepaskan tak memberi jawaban, hanya sebuah kesepian yang lebih dalam.

"Jangan sampai aku melihat kalian lagi," kata Chandra, suaranya datar, tidak ada emosi yang tertinggal. Ia tahu, meskipun ia menang hari ini, itu bukan kemenangan yang ia cari. Tapi setidaknya, ia kembali merasa hidup-meskipun masih banyak yang harus ia cari.

Chandra melangkah menjauh dari gang itu, langkahnya berat namun mantap. Setiap detik yang berlalu seperti semakin menambah beban dalam dirinya, tapi ia tak bisa berhenti. Setiap gerakan itu seperti upaya untuk melepaskan sesuatu yang tertahan terlalu lama, meskipun ia tak tahu apa yang sedang ia perjuangkan.

Langkah kaki yang menggema di lorong kosong itu terasa begitu berat. Pikirannya berputar-tentang Zenki yang kini punya batunya, tentang Kael yang selalu tahu apa yang harus dilakukan, tentang dirinya yang masih terperangkap dalam kebingungannya sendiri. Chandra tahu, kekuatannya memang besar, tapi kekuatan itu terasa seperti beban yang tak pernah bisa ia lepas. Seolah setiap kali ia mulai merasa dekat dengan jawaban, ada lebih banyak lagi yang harus dipertanyakan.

Ia berhenti di tepi jalan. Dari jauh, terdengar suara deru mesin kendaraan, namun semuanya terasa seperti kabur, seolah suara itu datang dari dunia yang berbeda. Chandra menatap langit yang semakin gelap. Hujan sebentar lagi akan turun, tapi ia tak peduli. Ia hanya ingin menjauh dari kerumunan, dari orang-orang, dari harapan-harapan yang menggantung di atasnya.

Tapi tiba-tiba, suara langkah kaki terdengar di belakangnya, dan sebelum ia sempat berbalik, seseorang sudah berdiri di hadapannya. Kael.

"Lagi-lagi kamu pergi tanpa bilang apa-apa?" suara Kael terdengar lebih seperti sebuah pernyataan daripada pertanyaan. Matanya yang tajam menilai, namun ia tak terlihat marah, hanya khawatir.

Chandra menatapnya sekilas, lalu mengalihkan pandangannya ke jalan di depannya. "Aku... cuma butuh waktu sendiri," jawabnya singkat, namun cukup untuk membuat Kael tahu ada sesuatu yang lebih besar yang tengah ia hadapi.

Kael terdiam beberapa detik, lalu berkata, "Kamu nggak akan mendapatkan apa-apa dari lari seperti ini, Chandra."

Chandra mendengus, merasa frustasi. "Aku nggak lari. Aku cuma... nggak tahu lagi harus ke mana."

Kael mendekat sedikit, tak terlalu mendesak, namun cukup dekat untuk memberi kenyamanan tanpa kata-kata. "Kamu nggak sendirian. Kalau kamu merasa bingung, kita bisa cari jalan bareng-bareng," kata Kael, suaranya lebih lembut kali ini. "Tapi, jangan lari dari pertanyaan-pertanyaan itu. Kekuatanmu lebih dari sekadar benteng. Mungkin kamu harus pelajari kenapa kamu merasa kosong. Jangan hanya meledak begitu saja."

Chandra menatapnya lama. Ia tahu Kael benar. Ia tahu itu. Namun kenyataan itu terasa seperti beban yang berat, yang bahkan lebih berat daripada sekedar bertarung dengan preman di gang sempit. Menyadari dirinya yang merasa kosong itu seperti membuka luka yang tak ingin ia sentuh.

"Lihat, aku... aku cuma nggak mau merasa ditinggal. Setiap orang di sekitar aku kayak... punya tujuannya sendiri. Zenki udah dapat batunya, Kael selalu punya jawaban, tapi aku..." Chandra meremas tangannya. "Aku cuma nggak tahu apa yang aku cari."

Kael menghela napas pelan, lalu menepuk bahu Chandra dengan ringan. "Kadang, kita nggak harus langsung tahu jawabannya. Tapi yang pasti, kamu nggak sendirian dalam perjalanan ini."

Chandra menoleh dan memberikan senyum kecil. "Kamu selalu tahu apa yang harus dikatakan, ya?"

Kael hanya tertawa kecil. "Kadang aku cuma bisa nyuruh kamu berhenti melarikan diri dari diri sendiri."

Chandra terdiam sejenak, lalu menarik napas dalam. Ia tahu Kael benar. Kadang jawaban itu bukan sesuatu yang bisa dipaksakan, tetapi sesuatu yang perlu dihadapi, satu langkah pada satu waktu. Tidak ada jalan pintas untuk memahami kekuatan itu, atau untuk memahami dirinya sendiri.

"Biar hujan turun, kita pergi makan sesuatu?" tawar Kael, mencoba membawa sedikit keceriaan ke suasana yang berat itu.

Chandra mengangguk pelan, merasakan sedikit kelegaan di dalam dadanya. Mungkin, untuk pertama kalinya hari itu, ia merasa sedikit lebih ringan.

Bersama Kael, mereka berjalan menyusuri jalan yang basah oleh hujan, langkah mereka selaras dalam diam yang penuh makna. Dan meskipun Chandra masih belum sepenuhnya mengerti tujuan perjalanannya, untuk pertama kalinya, ia merasa sedikit lebih siap untuk menemui apa pun yang akan datang.

semakin mendung, namun langkah kaki mereka tak berhenti. Hujan mulai turun perlahan, menyapu debu yang menempel di jalanan. Chandra dan Kael berjalan berdampingan, seakan tak ada kata yang perlu diucapkan untuk mengisi kekosongan antara mereka. Suara tetesan hujan di atap gedung dan deru kendaraan yang lewat menyatu, menciptakan irama yang nyaman meskipun dunia di sekitar mereka masih terasa berat.

Kael memecah keheningan dengan suara ringan, "Kamu tahu nggak, kadang kita cuma butuh waktu untuk berdiri di tempat yang sama, tanpa harus selalu bergerak ke depan."

Chandra menoleh sekilas, melihat ekspresi Kael yang serius, namun ada sesuatu di matanya yang menunjukkan bahwa kata-kata itu bukan hanya untuknya. "Lalu apa yang harus aku lakukan, Kael? Aku nggak tahu harus mulai dari mana."

"Mulailah dari hal kecil," jawab Kael, melirik Chandra sambil tersenyum. "Kamu sudah memulai dengan hal yang paling besar. Kamu nggak melihatnya, tapi kekuatanmu itu bukan sekedar kemampuan telekinesis, itu cara kamu berhubungan dengan dunia. Mungkin, kamu butuh menemukan cara untuk menerima dunia ini sebelum kamu bisa mengendalikannya."

Chandra terdiam, mencerna kata-kata Kael. Memang, selama ini ia hanya berfokus pada kontrol, pada cara mengendalikan kekuatannya, tanpa pernah benar-benar memahami apa yang membuat kekuatan itu ada. Apa yang ingin ia lakukan dengannya. Apa yang ia inginkan dari semua ini.

Mereka tiba di sebuah warung makan sederhana yang sepi. Di dalam, seorang pria paruh baya tengah membersihkan meja. Hujan yang semakin deras membuat warung itu terasa lebih hangat, lebih aman. Mereka duduk di salah satu meja yang ada, dan meskipun Chandra masih merasa beban di pundaknya, ada sesuatu yang memberi sedikit rasa nyaman.

"Panas," ujar Kael sambil membuka jaketnya. "Hujan kayak gini enaknya makan sesuatu yang hangat."

Chandra hanya mengangguk. Ia tidak terlalu peduli pada apa yang ia pesan, hanya ingin melupakan kebingungannya untuk sementara.

Mereka duduk diam, menunggu pesanan datang. Chandra menatap ke luar jendela, melihat tetesan air hujan yang berjatuhan dari langit. Setiap tetesnya seakan membawa pertanyaan yang terus menggantung dalam pikirannya. Seperti hujan yang tak pernah berhenti, pikirannya terus bergulir, berputar-putar mencari jawaban yang ia rasa semakin jauh untuk dijangkau.

"Mungkin kamu nggak perlu tahu semuanya sekarang," kata Kael, seolah bisa membaca pikiran Chandra. "Kamu nggak harus tahu kenapa kamu punya kekuatan ini atau apa tujuanmu. Yang penting, kamu mulai belajar untuk menghadapinya, bukan menghindarinya."

Chandra menoleh, melihat Kael dengan tatapan yang lebih lembut dari sebelumnya. "Aku rasa... aku terlalu lama berpikir kalau aku harus melakukannya sendirian."

Kael tersenyum. "Kamu nggak sendirian, Chandra. Kapan pun kamu merasa hilang, kamu bisa cari kami. Nggak usah takut untuk butuh bantuan."

Hujan di luar semakin lebat, tapi suasana di dalam warung itu terasa lebih tenang, lebih damai. Chandra mulai merasa sedikit lebih ringan, meski hatinya masih penuh dengan keraguan. Tapi mungkin, seperti hujan yang turun untuk menyegarkan bumi, waktu dan pemahaman perlahan akan menyegarkannya kembali.

Pesanan mereka datang, dan mereka makan dengan tenang. Tidak ada percakapan berat atau masalah yang perlu diselesaikan. Hanya dua orang yang duduk bersama, menikmati momen yang sederhana, dan itu sudah cukup.

Saat mereka selesai makan dan beranjak dari tempat duduk mereka, hujan mulai reda. Langit masih mendung, namun ada secercah cahaya yang mulai menembus awan.

"Terima kasih, Kael," kata Chandra, suara ringan tapi penuh makna. "Aku nggak tahu apa yang akan terjadi, tapi aku rasa... aku bisa menghadapi semuanya."

Kael mengangguk, tampak puas dengan keputusan Chandra yang sedikit lebih tenang. "Aku yakin kamu bisa, Chandra. Setiap langkahmu, meski kecil, itu sudah berarti."

Mereka melangkah keluar dari warung, menerjang hujan yang kini hanya tinggal sisa-sisanya. Dengan setiap langkah, Chandra merasa sedikit lebih yakin. Tidak ada yang tahu apa yang akan datang, tapi dia tahu satu hal: dia tidak perlu menghadapi semuanya sendirian.

----
Sementara itu..

Zenki duduk di meja makan, menatap rak buku yang kosong dan sebuah kotak pizza yang sudah setengah habis. Sejak Kael dan Chandra pergi, rumah itu terasa lebih sunyi. Tanpa kehadiran Chandra yang sering menggerutu atau Kael yang sibuk dengan alat-alat misteriusnya, Zenki mulai merasa sedikit aneh.

"Hmm... apa aku harus masak sendiri?" Zenki berpikir sambil melirik kompor yang tampak menantang. Dia membuka kulkas, menemukan bahan-bahan yang tak dikenalnya, dan memutuskan untuk membuat sesuatu yang... misterius. Entah itu telur dadar atau semacam eksperimen kimia.

Zenki menghela napas, mulai mencampur bahan-bahan dengan sedikit kebingungannya, sambil terus berusaha menebak, "Apa yang bisa salah dengan telur dan saus tomat, ya?"

Dari luar jendela, terdengar suara langkah kaki Chandra dan Kael yang kembali, disertai teriakan Zenki.

"APA INI?!"

Zenki yang panik segera berlari ke dapur dan mencoba menyelamatkan masakannya yang mulai mengeluarkan asap. "Aduh, kenapa jadi begini sih!" dia menggoyangkan panci dengan frustasi. "Kenapa aku selalu terjebak dengan kekacauan kayak gini?"

Pintu depan terbuka, dan Kael serta Chandra melangkah masuk, tampak lelah setelah beraktivitas seharian. Mereka langsung mencium bau yang mencurigakan, sebuah campuran aroma terbakar dan sesuatu yang mirip plastik.

"Zenki... ada apa ini?" Chandra bertanya sambil menutup hidungnya.

Zenki, dengan wajah panik dan rambut yang sedikit berantakan, berusaha tersenyum. "Cuma masakan sederhana. Ada telur, saus tomat, dan... entah apa lagi." Dia menunjuk ke panci yang sudah mengeluarkan asap tipis.

Chandra menatap panci itu, matanya sedikit terbelalak. "Itu... apa yang terjadi? Kenapa ada asap dari telur?"

Zenki menarik napas panjang, berusaha tenang. "Mungkin aku... agak sedikit berlebihan dengan api, gitu. Tapi tenang saja, aku bisa... aku bisa-"

Kael yang baru saja duduk di meja makan menatap Zenki, lalu melihat Chandra yang terlihat geli. "Gimana kalau mulai dengan membuat mie instan?" Kael menyarankan, mencoba menahan tawa.

Zenki menghela napas, menunduk. "Aku cuma ingin masak sesuatu yang enak. Tapi kayaknya aku lebih jago bikin masalah."

Chandra tersenyum dan duduk di sebelah Kael. "Sepertinya kita harus mulai mencari tutorial masak untukmu, Zenki. Atau paling tidak, beli makanan dari luar."

Zenki mengangguk kecewa, lalu dengan santai berkata, "Baiklah, kalau begitu. Tapi next time, aku mau coba lagi. Kali ini, mungkin aku bakal bikin nasi goreng dengan kompor... tanpa api yang terlalu besar."

Kael dan Chandra saling berpandangan dan tertawa ringan, kemudian Kael menambahkan, "Kalau begitu, aku rasa kita harus siap-siap untuk asap lagi, ya?"

Zenki tertawa kecil, merasa sedikit lebih baik. Meskipun ia kadang membuat kekacauan, setidaknya ia tahu mereka akan tetap ada untuknya.

""""

Saat kael ingin membuka pembicaraan terdengar suara pintu yang dibuka lagi mengalihkan perhatian mereka. Seorang tetangga datang mendekat. Wajahnya serius, dan ada sedikit rasa khawatir yang tampak di matanya. "Hei, kalian tahu nggak sih, ada yang mengacau di sekitar sini lagi? Ada masalah lebih besar daripada masalah dapur."

Zenki, yang tiba-tiba terhenti dari kekhawatirannya soal masakan, langsung mengangkat alis. "Masalah? Maksudnya, masalah apa?"

Tetangga itu mengerutkan kening. "Beberapa preman besar baru saja keluar dari penjara dan sepertinya mereka sedang mencari... sesuatu. Aku dengar, mereka berkeliaran mencari orang yang bisa mengimbangi kekuatan mereka."

Chandra yang mendengar itu langsung terdiam. Wajahnya kembali serius. "Jangan bilang kalau ini ada hubungannya dengan apa yang terjadi di gang tadi."

Zenki, yang tak mengerti sepenuhnya, tiba-tiba merasakan ketegangan yang menyelimuti suasana. Ia menatap Chandra yang terlihat semakin khawatir. "Jadi, mereka akan datang lagi?" tanyanya, namun Chandra sudah melangkah lebih cepat menuju pintu.

"Sepertinya, iya," jawab Chandra tegas. "Aku harus menyelesaikan ini."

"Chandra..." Zenki ingin mencegahnya, tapi ia tahu kali ini Chandra sudah mengambil keputusan. "Kamu nggak sendirian, kan? Aku akan ikut."

Kael, yang sejak awal lebih tenang, menatap mereka berdua. "Kalau kalian pergi, saya ikut. Tapi hati-hati."

Chandra hanya mengangguk dan melangkah keluar, tidak menghiraukan percakapan lebih lanjut. Yang penting sekarang adalah menyelesaikan masalah itu - masalah yang bukan hanya tentang preman-preman, tapi tentang pengendalian dirinya dan kekuatan yang terus tumbuh tanpa kendali.

Tiga orang itu menuju tempat yang lebih gelap dan lebih berbahaya, di mana ketegangan yang mereka hadapi bukan hanya ancaman fisik, tetapi juga ancaman dari dalam diri mereka masing-masing.

Langit semakin gelap saat mereka melangkah lebih jauh ke kawasan kota yang lebih terpencil. Suara langkah kaki mereka terdengar teredam oleh udara malam yang dingin. Chandra memimpin, tangannya sudah memegang erat palang besi yang diambilnya dari pinggir jalan, sementara Zenki dan Kael mengikuti di belakang. Mereka tidak tahu pasti apa yang akan mereka hadapi, tapi ada sesuatu yang membuat mereka tidak bisa mundur.

"Tempat ini... terasa aneh," ujar Zenki, sedikit cemas, melihat keadaan sekitar yang semakin sepi. Gang-gang yang semula ramai kini seperti terperangkap dalam kesunyian yang mencekam.

Chandra tidak menjawab, matanya terfokus pada jalan di depannya. Semakin mendekati mereka ke pusat permasalahan ini, semakin ia merasakan kekuatan yang tumbuh dalam dirinya, yang belum sepenuhnya bisa ia kontrol.

Sampai di sebuah sudut jalan yang lebih gelap, mereka berhenti. Di depan mereka, tampak sosok-sosok yang dikenal baik oleh Chandra. Beberapa preman yang dulu pernah dia hadapi, kini berdiri dalam kelompok besar. Wajah-wajah mereka tampak lebih kasar, lebih kejam, seolah-olah mereka sudah menunggu kedatangan Chandra.

"Jadi, kamu yang ingin jadi pahlawan, ya?" salah satu dari mereka berkata, sambil tersenyum sinis. "Apa kamu pikir kita akan mundur hanya karena kamu datang lagi?"

Chandra menatap mereka dengan penuh tekad, namun hatinya bergetar. Ia tahu bahwa ini lebih besar daripada sekadar pertarungan fisik. Ada sesuatu yang mengganggu perasaannya, semacam bayangan yang bergerak di dalam pikirannya. Kekuatannya... perasaan itu kembali datang. Kekuatan yang belum sepenuhnya ia pahami.

"Jangan biarkan mereka menyentuhmu," Kael berbisik pelan, matanya memindai gerakan-gerakan lawan.

Chandra mengangguk, lalu melangkah maju. "Aku nggak takut."

Namun, sebelum ia bisa melangkah lebih jauh, suasana berubah tiba-tiba. Terdengar suara gemuruh dari atas, seperti ada sesuatu yang jatuh dengan keras. Semua mata langsung tertuju ke arah suara itu.

Di atas atap, sosok itu berdiri tegap. Dari kejauhan tampak seperti manusia biasa, tapi saat ia melompat turun dan mendarat tanpa suara di antara Chandra dan para preman, atmosfer berubah drastis. Udara jadi dingin, berat, seolah menekan napas dari paru-paru siapa pun yang berdiri di sana.

Kael langsung siaga. "Itu... bukan manusia biasa."

Zenki menatap tajam. "Aku juga bisa merasakannya. Aura itu... tidak hidup. Tapi juga tidak mati."

Salah satu preman yang tadi berdiri paling depan langsung mundur, wajahnya pucat pasi. "B-Bos Raka?"

Pria yang disebut itu melangkah pelan. Rambutnya acak-acakan, matanya kosong tapi menyala dengan cahaya kehijauan. Senyum yang ia berikan terlalu lebar untuk ukuran manusia. Sesuatu tentang tubuhnya terasa... keliru.

"Aku bukan lagi Raka," gumamnya, suaranya dua lapis. Satu dalam, kasar, satu lagi berbisik menyeramkan seperti berasal dari bawah tanah.

Chandra menggertakkan gigi. "Dia dirasuki..."

Salah satu preman menjatuhkan rokoknya dan kabur tanpa banyak bicara. Yang lain terlalu takut untuk bergerak.

Raka-orang yang dulunya Raka-mendongak menatap Chandra. "Kau... yang pernah mengalahkan tubuh ini. Aku ingin tahu... apakah jiwamu juga sekuat itu."

Lalu, secepat kilat, dia menghilang dari tempatnya berdiri. Hanya Kael yang cukup cepat untuk menarik Chandra ke belakang saat tanah di tempat tadi mereka berdiri langsung retak seperti dihantam godam tak kasat mata.

"Ini bukan pertarungan biasa!" teriak Kael. "Chandra, fokus! Ini ujianmu!"

Tapi Chandra berdiri terpaku, bukan karena takut... tapi karena untuk pertama kalinya, dia bisa mendengar sesuatu yang aneh-suara bisikan samar, langsung di dalam kepalanya, seolah berasal dari sosok itu... atau dari kekuatan dalam dirinya sendiri.

"Pilihannya hanya dua, Chandra," kata suara itu. "Bangkit... atau hilang."

Gelombang energi spiritual mulai mendesak dari tubuh Raka yang dirasuki. Bangunan di sekitar mulai bergetar. Jalan retak. Cahaya lampu berkedip. Dan udara penuh dengan ketegangan yang bisa meledak kapan saja.

Chandra mengepalkan tangannya, rahangnya mengeras.

Dan layar hitam menyelimuti semuanya.

</p></div>
  <div id="bab7" class="section"><h2>Bab 7</h2><p>Chandra dan Raka berdiri berhadapan, saling menatap tajam seperti dua arwah yang tak sudi mundur. Mata mereka saling mengunci dalam ketegangan yang nyaris membakar udara. Zenki dan Kael berdiri tak jauh, namun kali ini memilih untuk tidak ikut campur. Mereka tahu-ini adalah momen milik Chandra. Saat di mana ia harus berdiri sendiri, menghadapi seorang manusia yang kini telah dirasuki oleh entitas kelam.

Aura merah pekat mulai mengepul dari tubuh Raka, berputar membentuk lingkaran energi yang berdenyut liar. Emosi, kemarahan, keegoisan-semuanya berbaur dalam kekacauan yang menyesakkan. Tubuh Raka tampak menggigil oleh kekuatan yang bukan miliknya.

Chandra menegang, rahangnya mengeras. Ia bisa merasakan tekanan itu, kekuatan destruktif yang siap meledak. Ia mengangkat tangannya, merentangkan telapak dengan gerakan tegas.

"Apa yang sedang kau lakukan, makhluk brengsek!" teriak Chandra, suaranya menggelegar di lorong yang sunyi.

Dengan kekuatan telekinesisnya, ia mengangkat beberapa bongkahan batu dari tanah dan melemparkannya lurus ke arah Raka. Tapi serangan itu justru terpental, berbalik arah seolah ditolak oleh kekuatan yang lebih dalam dan gelap. Batu-batu itu menghantam dinding, satu di antaranya melesat ke arah Chandra sendiri, memaksanya menunduk menghindar.

---

"Sudah lama ya, bocah tengil," desis Raka, suaranya serak seperti dua suara bertumpuk menjadi satu. "Kupikir kau cuma anak sok jagoan. Tapi ternyata, kau lebih menyebalkan dari yang kuduga."

Chandra mengeram, tangannya mengepal di sisi tubuhnya. "Kau bukan Raka lagi. Apa pun yang ada di dalammu sekarang, bukan manusia."

Zenki dan Kael berdiri beberapa meter di belakang, waspada namun tidak ikut campur. Kael bahkan bersedekap, matanya mengawasi dengan tajam namun dingin. Ini ujian bagi Chandra-sebuah pertarungan yang tak lagi soal otot, tapi jati diri.

Chandra menancapkan satu kakinya ke lantai lorong, debu berputar di sekelilingnya saat kekuatan telekinesisnya mulai terfokus. Kedua tangannya terentang, seperti menarik tali tak kasatmata dari udara.

"Aku tahu kau bukan Raka," gumamnya. "Tapi aku juga bukan anak lemah dari masa lalu."

Suara di kepala Chandra mendesis pelan, bukan suara orang lain-melainkan dorongan instingnya sendiri. Suara medan. Ia mulai melihat garis-garis samar mengalir di udara, jalur energi di sekeliling Raka yang membentuk semacam kubah pelindung.

"Aura penolak..." bisik Chandra, matanya menyipit. Ia mengubah pendekatan.

Alih-alih melempar batu, ia mengangkat dua batang besi dari tanah, bukan untuk dilempar, tapi diputar dengan kecepatan tinggi. Seperti gergaji melayang, kedua besi itu berputar dan membentuk medan sentrifugal, menabrak dinding energi Raka secara terus menerus dari sisi kanan dan kiri.

KRIINGG-!

Satu celah kecil terbentuk-hanya sepersekian detik, tapi cukup.

Chandra menggerakkan tangannya dengan presisi. Dari kantongnya, ia menarik sepotong peniti kecil-tak lebih dari logam tak berguna. Tapi di tangan Chandra, itu menjadi peluru tajam yang meluncur lurus ke arah celah di medan pelindung Raka.

TUK!

Raka terhuyung. Tidak terluka parah, tapi cukup untuk membuatnya mundur satu langkah.

"Kau... menyusup," desis entitas dalam dirinya. "Licik... seperti para penjaga warisan."

Chandra mengambil napas dalam-dalam. Ia tahu ini baru awal. Apa pun yang merasuki Raka bukan sekadar entitas liar-ia menyebut sesuatu tentang 'penjaga warisan'.

Suara tawa rendah menggema dari mulut Raka, tapi bukan suaranya sendiri. Ada nada gema asing, seolah lebih dari satu entitas bicara melalui tubuhnya.

"Tak kusangka warisan telekinesis masih bertahan... Tapi kau belum pantas, bocah."

Tiba-tiba aura merah di sekeliling Raka melebar, membentuk siluet seperti jaring laba-laba di udara. Jalur energi itu menggantung seperti benang halus, dan Chandra bisa merasakannya-gelombang psikis yang mencoba menyusup ke pikirannya.

"...Dia menarikku masuk?" Chandra bergumam.

Terlambat.

Matanya melebar, dan dunia di sekitarnya runtuh ke dalam kegelapan. Dinding lorong menghilang. Tanah tempat ia berdiri retak dan berubah menjadi hamparan ruang kosong, seolah pikirannya ditarik masuk ke medan spiritual Raka-tempat entitas itu bersemayam.

Chandra berdiri di tengah kehampaan, tubuhnya perlahan membentuk citra cahaya biru keunguan, seperti proyeksi mental dari dirinya sendiri. Di kejauhan, sosok Raka berdiri diam, dengan bayangan besar menjulang di belakangnya-makhluk tanpa wajah, matanya menyala merah, dan tubuhnya seperti kabut tebal berlapis tulang.

"Selamat datang di ruang batin sang pembenci," kata makhluk itu. "Di sini, kekuatan tak berarti. Yang bicara adalah luka... dan kemauan."

Chandra mengepalkan tangannya. Ia menatap makhluk itu tanpa gentar.

"Kalau begitu... mari kita bicara dengan luka kami."

Dan dari belakang Chandra, simbol-simbol biru mulai menyala. Lambang telekinesisnya-lingkaran dan garis-garis silang-muncul dalam formasi baru. Satu helai cahaya menari ke arah jari-jarinya, membentuk seperti benang kendali. Kekuatan telekinesisnya-bahkan di dunia spiritual-mulai membentuk medan yang nyata.

Chandra melangkah maju dalam kehampaan, setiap jejak kakinya membentuk riak cahaya di udara kosong. Tali-tali cahaya yang menjulur dari jari-jarinya bergerak lincah seperti cambuk halus, siap menyerang.

Sosok bayangan raksasa di balik Raka mengangkat lengannya. Dari tubuhnya melesat serpihan-serpihan hitam seperti pecahan kaca, berputar cepat, melesat ke arah Chandra dengan niatan mencabik pikirannya.

Zzzzt!

Chandra menggerakkan tangannya. Serpihan-serpihan itu tertahan di udara oleh medan tak terlihat. Namun tekanan psikisnya berat-berat sekali. Seperti mencegah pecahan masa lalu sendiri menusuk jiwanya.

"Telekinesis bukan cuma kekuatan untuk mengangkat benda," gumam Chandra, menahan tekanan yang menusuk dari segala arah. "Tapi juga... untuk menolak apa yang tak seharusnya masuk."

Ia melangkah maju lagi, dan kali ini benang-benang telekinesisnya menyentuh bayangan Raka. Satu cambuk cahaya menghantam, membuat siluet makhluk itu mundur setengah langkah.

"KAU BUKAN AKU!" teriak Chandra, dan untuk sesaat, udara spiritual di sekelilingnya bergetar.

Namun ketika makhluk itu mengaum, seluruh ruang runtuh menjadi gelap pekat. Cahaya dari Chandra nyaris padam... sampai sebuah suara terdengar-lembut, nyaris seperti napas.

> "Jangan lawan dia dengan kemarahan... dengarkan kekacauanmu, kendalikan."

Suara itu tidak datang dari luar. Ia merasuk dari dalam kepalanya, seperti gema jauh dari masa lalu. Chandra menoleh, dan di sekelilingnya, muncul bayangan samar: seorang pria berambut panjang, mengenakan jubah putih kelabu, berdiri tenang dengan lambang telekinesis di dahinya. Sosok itu tersenyum kecil, lalu meletakkan dua jari ke pelipisnya.

> "Telekinesis bukan hanya daya dorong... tapi keselarasan antara pikiran dan dunia. Dengarkan. Lihat."

Chandra menarik napas panjang. Dunia spiritual di sekitarnya berhenti bergetar. Ia memejamkan mata-dan ketika membuka kembali, cahaya biru dari tubuhnya tak lagi bergelombang. Ia stabil. Terkendali.

"Baiklah," bisiknya. "Kalau kau bayangan... aku akan jadi tangan yang menolakmu kembali ke terang."

Cahaya biru terang kini menyelubungi tubuh Chandra, membentuk siluet medan energi di sekelilingnya-seolah dunia spiritual pun mengakui keseimbangan barunya. Benang-benang telekinesis yang sebelumnya bergetar tak beraturan kini bergerak mulus, presisi, mengitari tubuhnya dalam orbit sempurna.

Sementara itu, sosok makhluk di balik Raka mengaum keras. Kabut hitam yang menyelimuti tubuh Raka mendesak lebih kuat, seolah hendak mempertahankan dominasi terakhirnya.

"Cukup bermain-main," desis Chandra. Ia mengepalkan tangan.

Tiba-tiba, seluruh medan spiritual berguncang. Puluhan bongkahan psikis-batu, puing, serpihan masa lalu-melayang di sekeliling Chandra, lalu melesat lurus ke arah makhluk itu.

Makhluk itu berusaha menangkis, namun benang telekinesis Chandra telah lebih dahulu menjerat tubuh bayangan itu, memisahkan dirinya dari tubuh Raka.

"Pergilah... kembali ke kegelapan yang menunggumu," ucap Chandra, nada suaranya tajam namun tenang.

Dengan satu gerakan jari, ia menciptakan lingkaran cahaya-sebuah sigil telekinesis yang berputar cepat seperti roda. Makhluk itu meraung, diseret ke tengah lingkaran itu, tubuhnya mencair dalam cahaya yang menyerap kebencian dan amarah.

> WUUUUOOOOHHHHHHHHHHHH!

Suara itu menggema hingga ke dunia nyata.

Tubuh Raka terangkat beberapa sentimeter di udara, lalu jatuh perlahan ke tanah. Kabut hitam di sekelilingnya lenyap, menguap menjadi serpihan halus. Nafasnya berat, tapi normal. Matanya perlahan terbuka-kosong, bingung, namun bebas.

Chandra terhuyung, lututnya nyaris menyentuh tanah.

Zenki langsung menyambutnya, menahan tubuhnya sebelum ambruk sepenuhnya. "Kau berhasil..."

Chandra menatap tangannya yang masih bergetar, lalu tersenyum samar. "Telekinesis... ternyata lebih dari yang kupikirkan."

Kael hanya mengangguk dari kejauhan. Ia melihat sesuatu di Chandra-bukan hanya kekuatan, tapi arah. Jalur yang mulai terbuka.

Langit spiritual mulai mereda. Dunia kembali tenang, setidaknya untuk saat ini.

Malam pun turun perlahan, menumpahkan cahaya remang di seantero kota. Hujan yang tadi sempat turun kini hanya menyisakan aroma tanah basah dan udara yang lembab. Di dalam rumah kecil mereka, suasana terasa lebih hening dari biasanya.

Zenki tengah duduk di lantai ruang tengah, membongkar alat masak bekas eksperimen makan malamnya yang gagal total. Kael, seperti biasa, bersandar di jendela sambil menatap langit. Di tangannya, sebatang cokelat yang entah sejak kapan dia miliki, perlahan dikunyah tanpa ekspresi.

Chandra diam di kamarnya, lampu temaram menyinari buku warisan yang terbuka di pangkuannya. Tapi bukan huruf-huruf di halaman itu yang menarik perhatiannya-melainkan bayangan dirinya sendiri di jendela. Ia menatap pantulan itu dalam-dalam.

"Apa aku berubah... atau cuma mulai melihat siapa diriku sebenarnya?" gumamnya lirih.

Pikirannya kembali pada duel tadi. Pada bisikan masa lalu yang muncul sejenak-suara lembut dari seorang esper telekinesis yang lebih dulu menapaki jalan itu. Ia belum tahu siapa sosok itu, tapi perasaan yang ditinggalkannya... hangat. Nyaris seperti tangan tak terlihat yang menuntunnya melewati kabut.

Chandra menutup bukunya perlahan.

"Aku belum selesai," katanya pelan, tapi tegas. "Tapi malam ini... aku menang."

Di luar kamar, Zenki berteriak, "Kalau kau gak keluar buat makan dalam lima menit, aku masak lagi!"

Chandra tersenyum. "Tuhan, jangan sampai itu terjadi."

Ia berdiri, menarik nafas panjang, lalu membuka pintu kamarnya. Untuk saat ini, ia bukan hanya Chandra yang sedang mencari jati diri. Ia adalah bagian dari sesuatu yang lebih besar. Dan malam ini, langkahnya terasa sedikit lebih ringan.

Chandra berjalan pelan ke dapur, aroma sisa masakan hangus masih tercium samar. Di atas meja, wajan dengan bekas percikan saus misterius membuatnya menggeleng pelan. Zenki duduk bersila di lantai dengan ekspresi bersalah, sambil mencoba mengelap meja yang sudah kotor separuh.

"Aku cuma coba bikin telur dadar isi... tapi dia berubah bentuk jadi monster," ujar Zenki polos.

Chandra mengangkat alis. "Monster yang mengandung karet gelang dan garam tiga sendok makan?"

Zenki membuka mulut, lalu menutupnya lagi. "Mungkin... sedikit terlalu ambisius."

Tanpa berkata apa-apa lagi, Chandra mulai membuka kulkas. Ia mengeluarkan bahan-bahan seadanya-mie telur, daun bawang, sebutir telur, dan sedikit sisa daging ayam rebus dari kemarin.

Kael muncul di ambang pintu dapur, masih mengunyah cokelat. "Jadi, kau menyelamatkan dunia dan menyelamatkan makan malam dalam hari yang sama?"

Chandra tidak menoleh. "Seseorang harus melakukannya."

Dalam sepuluh menit, aroma mie goreng rumahan memenuhi udara. Sederhana, tapi hangat. Saat mereka duduk bersama di lantai ruang tengah, masing-masing memegang mangkuk panas, suasana terasa seperti jeda damai dalam tengah badai besar yang belum berakhir.

Zenki menyuap mie-nya dengan antusias. "Ini enak banget. Mungkin kekuatan sejati telekinesis adalah di dapur."

Chandra tertawa kecil. "Kalau begitu, aku baru menyentuh permukaannya."

Kael diam beberapa saat sebelum akhirnya berkata, "Apa yang kau rasakan saat menghadapi entitas itu?"

Chandra menatap ke dalam mangkuknya, lalu perlahan menjawab, "Takut. Tapi bukan takut pada makhluk itu... aku takut kehilangan kendali atas diriku sendiri. Tapi di dalam kegelapan itu, ada sesuatu yang memanggil. Bukan musuh. Bukan juga teman. Seperti... bagian dari diriku yang ingin didengar."

Kael mengangguk pelan. "Itu artinya kau mulai terhubung. Kekuatan warisan bukan sekadar alat-mereka adalah bagian dari sejarah. Dari jiwa."

Chandra menatap mereka berdua, lalu tersenyum tipis. "Apa pun yang menanti kita... aku ingin tahu lebih banyak. Tentang warisan ini. Tentang siapa yang dulu pernah memilikinya."

Zenki mengangkat mangkuknya ke udara. "Kalau begitu, demi masa depan dan mie goreng, kita harus terus hidup!"

Kael menatapnya datar. "Kau... terlalu banyak menonton anime."

"Tapi aku hidup karenanya!" jawab Zenki bangga.

Mereka tertawa. Malam itu, meskipun dunia di luar masih menyimpan banyak misteri dan kegelapan, di dalam rumah kecil itu, tiga anak muda-esper yang membawa beban kekuatan luar biasa-berbagi momen ringan, sederhana, dan benar-benar manusiawi.

Dan di luar jendela, di langit malam yang kembali tenang, sebuah bintang jatuh melintas cepat. Mungkin kebetulan. Mungkin juga pertanda-bahwa cerita mereka baru saja dimulai.

Keesokan pagi----

matahari menembus tirai ruang makan, membentuk garis-garis hangat di lantai kayu. Aroma telur dadar dan nasi goreng menyebar ke seluruh rumah. Zenki, masih dengan rambut awut-awutan, duduk di kursi dapur sambil menguap lebar.

"Ini nasi goreng buatan Chandra yang katanya bisa menyembuhkan semua luka," gumam Kael, duduk bersilang kaki di kursi dekat jendela. Tatapannya mengarah ke halaman belakang, tapi telinganya waspada. "Atau setidaknya... luka di perut."

Chandra meletakkan wajan dan menyeringai. "Kalau kalian tetap hidup setelah ini, berarti aku layak dapet gelar chef."

Zenki menyendokkan satu suapan dan langsung terdiam. Ia mengunyah perlahan, lalu matanya membelalak. "...Ini enak banget."

Kael tidak langsung mencicipi. Ia menatap ke luar, ke pohon mangga yang bergoyang perlahan tertiup angin. "Ada yang berubah."

Chandra dan Zenki saling melirik.

"Perasaan atau penglihatan espermu?" tanya Chandra pelan.

Kael menjawab tanpa berpaling. "Terlalu tenang. Biasanya... sesuatu mendahului gangguan besar."

Zenki menghela napas, mendorong piringnya. "Kita baru saja dapat momen tenang, jangan rusak dulu."

"Justru itu," Kael akhirnya mengambil sendok. "Ketenangan kadang cuma jeda napas sebelum seseorang tenggelam."

Mereka terdiam sejenak, hanya ditemani bunyi burung dan suara langkah kaki tetangga yang lewat depan rumah. Tapi jauh di kejauhan, di balik langit cerah, seekor burung gagak hitam melintas-dan menghilang seolah ditelan udara.

Tiga hari sebelum mama Chandra pulang. Tiga hari sebelum semuanya mulai berubah.

Sekolah. Jam 7:30 pagi.

Gerbang sekolah sudah ramai. Suara langkah kaki, tawa, dan sapaan bercampur seperti simfoni pagi yang biasa. Namun bagi Chandra, Zenki, dan Kael, dunia terasa setengah senyap-seperti ada lapisan tipis yang memisahkan mereka dari keramaian itu.

"Liat nggak? Orang-orang kelihatan... capek," bisik Zenki, menunjuk ke arah beberapa siswa yang wajahnya lesu, mata sayu, seolah tak tidur semalaman.

Kael memperhatikan mereka satu-satu. "Ini bukan cuma kurang tidur. Ini seperti... mimpi yang mencuri tenaga."

Chandra mengangguk pelan. "Tadi malam aku juga ngerasa aneh. Pas bangun, rasanya kayak udah berlari jauh, padahal cuma tidur."

Mereka berjalan melewati lorong, menyusuri koridor yang mengarah ke kelas. Cahaya lampu terasa lebih dingin dari biasanya. Beberapa murid tampak menguap lebar, bahkan ada yang tertidur di meja.

Zenki menelan ludah. "Kalau ini efek samping dari makhluk bayangan waktu itu... mungkin sisa energinya masih berputar di sini."

"Bukan sisa. Tapi jejak," Kael mengoreksi sambil mengedarkan pandangan ke seluruh lorong. "Dan jejak bisa mengundang sesuatu kembali."

Mereka berhenti sejenak di depan ruang musik. Pintu tertutup rapat, tapi ada getaran samar-tidak terlihat, tidak terdengar, hanya terasa oleh esper.

Chandra menoleh ke Kael. "Kita periksa nanti pulang sekolah?"

Kael menatap pintu itu dalam diam, lalu mengangguk. "Malam ini."

Di dalam kelas. Jam 08:15.

Pelajaran fisika baru dimulai. Ibu Ratna sibuk menulis rumus di papan tulis. Chandra duduk di tengah, Zenki di sampingnya, menguap panjang sambil menopang dagu.

"Semalam jam berapa tidur?" bisik Chandra.

"Jam dua. Mimpi aneh lagi... kayak ada bayangan diriku sendiri ngejar dari belakang," jawab Zenki setengah lesu.

Chandra menoleh, alisnya terangkat. "Bayangan? Sama kayak waktu di ruang musik?"

Zenki mengangguk pelan, lalu mengedip. "Eh, kau kenapa? Tadi pagi kelihatan diem banget."

"Aku... cuma kepikiran soal simbol di buku. Ada rasa kayak... kita kehabisan waktu."

Mereka terdiam sebentar. Tiba-tiba, secarik kertas dilipat dilempar dari arah belakang. Mendarat tepat di meja Zenki.

Zenki membukanya-tulisan tangan Kael.
"Aku titip pesan: habis pulang sekolah, kita ke ruang musik. Ada yang berubah."
Di bawahnya:
"P.S.: Jangan terlalu serius. Kalian kelihatan kayak murid baru yang nyasar di kelas alien."

Chandra menahan senyum. "Dia ngirim dari mana, sih?"

Zenki menoleh ke belakang. Di luar jendela, di halaman kecil antar kelas, Kael berdiri santai sambil membaca buku, seolah sengaja memperlihatkan dirinya.

"Dia punya waktu, tenaga, dan kemampuan buat jadi aneh setiap saat," gumam Zenki.

Chandra terkekeh pelan. "Untung dia di pihak kita."

</p></div>
  <div id="bab8" class="section"><h2>Bab 8</h2><p>Setelah kelas di sekolah selesai, Chandra dan Zenki keluar dari kelas dengan langkah ringan, meskipun pikiran mereka masih dipenuhi pertanyaan. Ruang musik semakin dekat, dan getaran samar yang mereka rasakan tadi semakin kuat seiring mereka melangkah. Suasana sekolah terasa semakin asing dan penuh dengan ketegangan yang terpendam.

"Menurutmu, Kael benar? Ada yang berubah di ruang musik?" tanya Chandra, mengalihkan perhatian Zenki dari lamunan.

Zenki mengangkat bahu. "Yang jelas, kalau ada yang aneh, kita nggak bisa tinggal diam."

Mereka tiba di depan pintu ruang musik. Pintu itu tertutup rapat, namun ada aura yang menggantung di udara—sesuatu yang tidak terlihat, namun dapat dirasakan oleh mereka yang memiliki kemampuan esper. Chandra menatap Zenki, dan tanpa kata-kata lebih lanjut, mereka mendorong pintu itu.

Begitu pintu terbuka, udara dalam ruang musik terasa lebih berat, lebih pekat. Lampu-lampu yang biasanya terang, kini redup, seakan dipenuhi kabut tipis. Di tengah ruangan, bangku-bangku gitar dan alat musik lainnya tergeletak berantakan, seperti ada sesuatu yang baru saja mengacaukan tempat itu. Namun, yang paling mencolok adalah dinding yang tergores oleh sesuatu yang gelap—simbol yang tidak pernah mereka lihat sebelumnya.

"Ini..." Chandra berbisik, mendekati dinding yang tergores. "Bukan simbol dari buku, tapi... semacam penghubung."

Zenki melangkah maju, merasakan getaran yang semakin kuat. "Ini jejak yang Kael maksud. Tapi kenapa ada di sini?"

Chandra mencoba meraba dinding itu, merasa energi gelap yang terperangkap di dalamnya. Ia merasakan sesuatu yang aneh di dalam dirinya, sebuah dorongan yang memaksa dirinya untuk lebih mendalami jejak itu.

"Sesuatu telah datang ke sini," kata Zenki, suaranya berat. "Dan itu nggak hanya jejak."

Tiba-tiba, suara langkah kaki terdengar dari luar ruangan. Tanpa ada waktu untuk bertindak, sosok yang sangat mereka kenal muncul di ambang pintu—Kael.

"Sudah kuduga, kalian pasti akan segera sampai di sini," Kael berkata dengan nada datar, meskipun ada sedikit kerutan di dahinya. "Jangan sentuh itu."

"Tapi ini... ada pengaruhnya, kan?" tanya Chandra, mencoba untuk memahami apa yang sedang terjadi.

Kael mengangguk pelan. "Simbol ini bukan sekadar gambar. Ini adalah saluran—mungkin untuk memanggil sesuatu. Kita tidak tahu siapa yang membuatnya, atau tujuan mereka, tapi kita harus segera menghadapinya."

Zenki memandang simbol itu dengan tatapan tajam. "Kalau kita hancurkan simbol ini, apakah itu akan menghentikan apa yang akan datang?"

Kael diam sejenak, tampaknya sedang mempertimbangkan. "Tidak. Itu hanya mengurangi efeknya. Yang penting adalah menjaga agar kekuatan yang terhubung dengan simbol ini tidak bisa lepas. Dan itu hanya bisa dilakukan dengan cara kita melibatkan... kekuatan yang sama."

Chandra merasa keraguannya semakin besar. "Maksudmu... kita harus menggunakan kekuatan kita untuk menahan ini?"

"Ya," jawab Kael. "Kalian berdua sudah cukup berkembang untuk melakukannya. Tapi ada risiko yang lebih besar. Menggunakan kekuatan kalian berarti kita membuka diri pada kemungkinan yang lebih gelap—sesuatu yang tak terduga."

Zenki dan Chandra saling berpandangan. Mereka tahu, meskipun ada rasa takut yang menggantung, mereka tak punya pilihan lain.

"Jadi, apa yang harus kita lakukan?" tanya Chandra, sudah siap menghadapi apa pun yang ada di depan mereka.

Kael melemparkan pandangannya ke dinding yang penuh dengan simbol. "Kita harus masuk ke dalam dunia simbol ini. Menghadapinya di sana, di tempat di mana energi ini berakar. Di situlah kita bisa menghentikannya."

Chandra menarik napas dalam-dalam, menyiapkan dirinya untuk apa yang akan datang. Zenki mengangguk, seakan memberi isyarat bahwa mereka sudah siap.

Kael melangkah maju, membuka jalan untuk mereka. "Mari kita lakukan ini. Sekarang."

Begitu mereka melangkah maju, cahaya di ruang musik semakin redup, dan seluruh dunia sekitar mereka terasa seperti menyusut. Mereka mulai merasakan tarikan kekuatan yang gelap—sesuatu yang bersembunyi di dalam bayangan, menunggu untuk dilepaskan.

Di luar, burung gagak hitam itu kembali terbang melintas di langit yang cerah—seakan menjadi pertanda bahwa sesuatu yang lebih besar sedang mendekat.

Kael memperhatikan sekelilingnya dengan penuh kewaspadaan. Ruang musik yang biasanya sunyi kini terasa seperti ruang yang terperangkap dalam kesunyian yang mendalam, seakan ada yang sedang mengamati mereka dari bayangan. Saat pintu dibuka, Kael langsung merasakan perubahan yang aneh, seperti udara yang lebih tebal di sekitar mereka.

Zenki dan Chandra memasuki ruang tersebut, meski mereka tahu bahwa ada sesuatu yang tidak beres, mereka merasa lebih aman bersama Kael. Kael bergerak lebih dulu, menutup pintu dengan hati-hati dan memastikan tak ada celah. "Jaga jarak, tetap tenang," katanya, suara rendah namun tegas.

Di hadapan mereka, ruang musik yang luas itu dipenuhi dengan kesunyian. Namun, semakin mereka berada di dalam, semakin jelas getaran samar yang terasa di udara—getaran yang mengguncang lebih dalam ke dalam jiwa. Kael merasakan keberadaan itu, mengendap, menunggu saat yang tepat.

"Bayangan," gumam Kael, tak lagi perlu menjelaskan lebih jauh. Ia tahu bahwa ini adalah makhluk yang mereka hadapi. Kael menggerakkan tangannya perlahan, memfokuskan kekuatan Duskform di sekitar tubuhnya. Sesuatu yang gelap dan berbentuk kabur mulai muncul dari sudut ruangan.

"Ini milik siapa?" tanya Chandra, matanya memandang ketegangan yang mulai menyelimuti ruangan.

Kael menatap ke arah bayangan yang berusaha bergerak lebih dekat. "Bukan kalian yang diincar. Tapi lebih baik kalian menjauh."

Zenki ingin melangkah maju, namun Kael menahan geraknya dengan tangan terangkat. "Diam. Aku bisa menangani ini."

Dari bayangan itu, perlahan muncul sosok yang tak berbentuk jelas—hanya berupa gelap yang bergerak melawan cahaya. Kael menyipitkan mata, menunggu hingga bayangan itu semakin mendekat, saat itulah dia melancarkan serangan.

Dengan gerakan cepat, Kael mengaktifkan kekuatan Duskform-nya, tubuhnya seketika menghilang dan muncul kembali dalam bayang-bayang yang lebih gelap. Keberadaannya seolah menyatu dengan kegelapan ruang tersebut. Kael memfokuskan tenaganya, dan dalam sekejap, ruang musik itu dipenuhi dengan ledakan kekuatan yang mengguncang seluruh ruangan.

Bayangan itu berusaha melawan, namun dengan ketegasan Kael, ia bisa meremas dan menghancurkan bentuk gelap itu menjadi serbuk halus yang lenyap begitu saja. Kael menarik napas dalam-dalam, dan ketika bayangan itu menghilang, ketegangan di ruangan itu mereda.

Zenki dan Chandra terperangah, menyaksikan kemampuan Kael yang tak pernah mereka lihat sebelumnya. "Kau... Kau bisa melakukan itu?" tanya Zenki, tak bisa menyembunyikan kekagumannya.

Kael kembali ke posisinya, tangan terlipat di dada. "Aku tak hanya menghilang. Aku bisa menghapus jejak. Ini bukan pertama kalinya aku menghadapi makhluk seperti itu."

Chandra menatap Kael dengan serius. "Kenapa baru sekarang kau menunjukkan kemampuan ini? Kita—"

"Karena kalian belum siap," Kael memotong, suaranya penuh penekanan. "Kadang, yang lebih baik adalah menyembunyikan kekuatan hingga waktunya tepat. Sekarang, kalian sudah bisa melihat sendiri."

Mereka terdiam sejenak, membiarkan keheningan kembali menguasai ruang musik yang kini terasa lebih normal. Namun, meskipun ancaman itu sudah berlalu, Kael tahu ini baru permulaan. Jejak-jejak bayangan itu belum selesai mengganggu mereka.

"Tapi kita belum selesai," Kael menambahkan, menatap mereka dengan ekspresi serius. "Kita harus segera kembali dan mempersiapkan langkah selanjutnya. Masih ada banyak yang harus kita hadapi."

Dengan cepat, Kael mengarahkan langkahnya keluar dari ruang musik, disusul oleh Chandra dan Zenki yang masih terkejut. Mereka tahu bahwa ini baru bagian kecil dari ancaman yang lebih besar, dan Kael, yang selama ini lebih banyak mengamati, baru saja membuka babak baru!

"Apakah itu hanya sebuah peringatan?" tanya Chandra, berjalan di samping Kael dengan ekspresi serius.

"Sepertinya begitu," jawab Kael, matanya menatap kosong ke arah koridor yang kini sepi, hanya diisi oleh suara langkah kaki mereka. "Makhluk itu... bukan sekadar bayangan. Itu adalah bentuk energi yang terperangkap, jejak yang masih ada dari peristiwa sebelumnya."

Zenki, yang baru saja mengumpulkan pikirannya, menambahkan, "Jadi, ini semacam ancaman yang belum sepenuhnya hilang? Kenapa bisa ada energi sisa seperti itu?"

Kael berhenti sejenak, memutar badan dan menatap kedua sahabatnya. "Ada banyak hal yang tidak bisa kalian lihat. Setiap kekuatan yang terlibat dalam dunia ini meninggalkan bekas, seperti luka yang tidak sembuh. Dan terkadang, luka-luka itu bisa hidup kembali."

Chandra mengernyit. "Tapi kita sudah menghadapinya sebelumnya. Aku rasa kita belum sepenuhnya mengerti apa yang kita hadapi."

"Betul," Kael mengangguk. "Karena itulah aku lebih memilih untuk bertindak sendirian. Namun, sekarang... kalian harus siap lebih banyak lagi."

Zenki mengerutkan kening. "Siap untuk apa?"

"Ancaman yang lebih besar. Yang tidak hanya berasal dari makhluk-makhluk seperti itu," jawab Kael pelan, namun tegas. "Ada kekuatan yang lebih gelap, yang bisa memanipulasi jiwa dan pikiran. Dan mereka sudah mulai bergerak."

Keheningan menyelimuti mereka sejenak. Chandra dan Zenki saling melirik, mencoba memahami kata-kata Kael.

Kael melanjutkan, "Sekarang, kita harus lebih berhati-hati. Kekuatan-kekuatan ini tidak terlihat dengan mudah. Mereka bisa menyusup ke dalam pikiran kalian, memutarbalikkan kenyataan. Jadi, jangan pernah lengah."

Mereka bertiga kembali berjalan, kali ini lebih cepat, menujukan tujuan yang lebih jelas—untuk mempersiapkan diri menghadapi ancaman yang lebih besar, yang belum mereka pahami sepenuhnya.

Di luar sekolah, langit yang tadinya cerah mulai sedikit mendung, dan udara terasa lebih berat, seolah dunia itu sendiri turut merasakan ketegangan yang membayangi mereka.

Setibanya di rumah, Zenki langsung menuju dapur untuk mengambil camilan, sementara Chandra duduk di meja makan, merenung. Kael tidak bergabung dengan mereka, ia memilih untuk duduk di balkon belakang, mengamati langit yang kelabu.

Kael merasakan sesuatu yang lain. Sebuah ancaman yang lebih besar dari sekadar makhluk bayangan. Sesuatu yang akan menguji kekuatan mereka lebih jauh, lebih dalam, lebih mengerikan.

Chandra mendekat dengan ragu. "Kael, apa yang sebenarnya sedang terjadi?"

Kael menoleh, melihat tatapan penuh harap dan kebingungan di mata Chandra. Ia tahu, bahwa meskipun mereka sudah melalui banyak hal bersama, mereka belum siap sepenuhnya menghadapi apa yang akan datang.

"Hal yang lebih besar sedang bergerak," kata Kael akhirnya. "Dan kita harus siap dengan segala kemungkinan."

Chandra tidak berkata apa-apa lagi. Dia mengerti, bahwa ini bukan hanya soal melawan makhluk atau entitas bayangan. Ini adalah tentang bertahan hidup dalam dunia yang lebih besar dari yang mereka ketahui. Dunia yang penuh dengan kekuatan yang lebih gelap.

Zenki yang datang kembali dengan secangkir teh menatap Kael. "Apa kita benar-benar bisa menghadapinya?"

Kael tersenyum tipis, namun ada sedikit kesan kesedihan di baliknya. "Jika kita bersatu, kita bisa. Tapi ingat, setiap kekuatan memiliki harga."

Mereka terdiam, menyadari bahwa persahabatan dan kekuatan mereka tidak cukup untuk menghadapi apa yang akan datang. Tapi satu hal yang pasti: mereka akan menghadapi semuanya bersama.

Dua Hari Sebelum Mama Pulang
Pagi itu, hujan rintik-rintik turun membasahi genting rumah. Langit kelabu menyelimuti kota sejak subuh, seolah ikut menyimpan rahasia yang belum terucap. Kael sudah bangun sejak fajar, duduk bersila di ruang tengah, dikelilingi simbol-simbol aneh yang ia gambar di lantai dengan kapur putih. Matanya terpejam, napasnya pelan dan teratur.

Zenki mengintip dari dapur, memegang mug kopi hangat. “Dia udah begitu dari tadi?” bisiknya ke Chandra.

“Sejak jam empat. Gue sempat kebangun, dia udah duduk di situ,” jawab Chandra pelan. Ia baru saja mengganti baju seragam. Rambutnya masih sedikit basah.

“Ngapain sih dia?”

Chandra hanya mengangkat bahu. Tapi saat itu Kael membuka mata perlahan. “Aku sedang mendeteksi celah dalam lapisan spiritual sekolah ini. Semakin dekat, semakin... rapuh.”

Zenki mengangkat alis. “Celah kayak... retakan?”

“Lebih buruk,” jawab Kael sambil berdiri, gerakan tubuhnya tenang namun tajam. “Semacam pintu. Tapi bukan kita yang membukanya.”

Chandra dan Zenki saling pandang.

Kael mengambil jaketnya dari gantungan. “Hari ini, aku pergi sendiri. Kalian tetap di sekolah, bertindak biasa. Tapi waspadai perubahan suasana.”

“Ke mana?” tanya Chandra cepat.

Kael sudah berjalan ke depan pintu, tak menoleh. “Tempat lama yang pernah kututup. Sekarang… ada yang mencoba membukanya lagi.”

Jam 10:42 – Lokasi: Bekas Gedung Teater Tua, belakang distrik barat
Gedung itu terbengkalai, atapnya sebagian runtuh, dindingnya ditumbuhi lumut. Tapi Kael melangkah masuk tanpa ragu.

Suara detakan jam tua menyambutnya begitu ia melewati ambang pintu yang retak. Di dalam, suasana seperti terjebak di antara waktu.

Kael menyentuh lantai kayu berdebu, menelusuri bekas simbol Aetherion yang pernah ia segel bertahun lalu. Kini, retakan samar bercahaya ungu muncul di sana—retakan spiritual.

"…Sudah sejauh ini," gumam Kael. Ia merentangkan tangan, bayangan hitam menyelimuti tubuhnya sejenak saat kekuatan Duskform mengalir.

Dari dalam retakan, suara lirih seperti bisikan mulai terdengar:
"Kau tak bisa menahannya selamanya, Kael Varuna..."

Kael mendengus. “Aku juga tidak berniat menahan. Tapi kalian akan kembali—dengan syaratku.”

Dengan gerakan cepat, ia menghantam simbol di lantai dengan segel esper. Cahaya hitam meledak, menciptakan gelombang tekanan yang membuat dinding gemetar. Retakan itu berkedip, lalu memudar...

Namun saat Kael berdiri, nafasnya memburu, matanya menajam. Sesuatu… tertinggal. Sesuatu yang tak bisa ia usir sepenuhnya.

Di sekolah – jam 13:00, ruang kelas
Chandra merasakan migrain mendadak. Ia menunduk, mencengkeram meja. Zenki segera meraih pundaknya.

“Kau kenapa?”

Chandra menarik napas dalam-dalam. “Tadi... ada suara di kepala. Bukan suara sendiri. Bukan suara yang dikenal.”

Zenki langsung menoleh ke luar jendela. Langit mulai memucat, bukan karena cuaca, tapi karena tekanan yang tak terlihat.

Mereka tahu. Kael sedang menghadapi sesuatu. Dan mereka... akan segera dipanggil ikut masuk ke dalamnya.

Tempat Tua yang Pernah Kupanggil “Sarang”
Langkahku berat saat keluar dari gedung itu. Bukan karena luka, tapi karena beban yang kupikul kembali terasa di punggung ini—seperti ransel tua berisi kenangan yang tak bisa dibuang.

Di luar, hujan masih turun pelan. Aku menengadah, membiarkannya membasahi wajah. Kadang, hujan membantu menutupi rasa. Tapi tidak hari ini.

Retakan itu... bukan hanya bekas. Ia adalah panggilan. Dan lebih buruknya lagi, panggilan itu dijawab.

Aku memejamkan mata sejenak.

"Kael Varuna."

Suara itu menggema dari dalam pikiranku, familiar dan dingin seperti malam pertama aku menerima batu Duskform. Suara dari entitas itu—yang dulu kujadikan perjanjian, dan kini mulai menagihnya kembali.

"Aku masih memegang bagian dari janjimu, bukan?" tanyaku lirih dalam benak.

"Dan bagianmu adalah menjaga keseimbangan. Tapi kau mulai terlalu lembut."

Aku menggeram. “Itu karena mereka berbeda. Mereka bukan kita.”

Bayangan samar muncul di tepi penglihatanku—bentuk makhluk bersayap hitam dengan wajah kosong dan simbol menyala di dadanya. Ia melayang, tak sepenuhnya nyata, tapi cukup kuat untuk dirasakan.

"Yang berbeda kadang lebih berbahaya. Mereka punya hati. Dan hati bisa retak."

Aku menarik napas dalam, lalu mengaktifkan Duskform sepenuhnya. Dunia menjadi senyap—warna memudar, suara menghilang. Aku menjejak ke dalam dimensi bayangan, hanya untuk melacak sisa-sisa energi yang tertinggal dari retakan tadi.

Di dimensi ini, waktu melambat, dan bayangan bicara lebih keras. Aku melihatnya—retakan lain, tersembunyi di balik dinding realita, membentuk semacam lingkaran: Jejak Esper yang pernah gugur.

Aku belum siap. Tapi waktu tak peduli apakah aku siap atau tidak. Dunia ini mulai goyah, dan para murid itu—Chandra, Zenki—mereka akan segera berada di garis depan. Entah mereka mau atau tidak.

Aku melangkah keluar dari Duskform. Dunia kembali berwarna. Hujan semakin deras.

Ponselku bergetar. Pesan dari Chandra:
“Kael, semuanya baik? Kami ngerasa ada yang nggak beres di sekolah.”

Aku menatap layar ponsel beberapa detik, lalu membalas:
“Belum. Tapi akan.”

Kukunci ponsel dan menatap langit.
Dan kali ini, aku tidak akan hanya menjadi bayangan di belakang.

Hari -2, malam hari.

Kael berdiri di atap sekolah, angin malam mengacak rambutnya yang masih basah setelah mandi cepat di rumah. Dari ketinggian itu, lampu-lampu kota terlihat seperti bintang yang tersesat di bumi. Tapi matanya tidak tertuju ke sana. Ia menatap gedung sekolah dengan pandangan kosong namun waspada.

Ia memejamkan mata.

Dan seketika dunia berubah.

Dalam satu tarikan napas, ia menyelam ke dalam ruang antara—dimensi tipis yang hanya bisa disentuh oleh esper dengan keterampilan tinggi. Dunia jadi hening. Waktu seperti melambat, dan bayangan mulai bermunculan di sudut pandangnya—seperti kenangan yang ingin bangkit.

Langkah-langkahnya membawanya ke ruang musik lagi. Tapi kini, tak ada pintu. Tak ada tembok. Hanya lingkaran cahaya samar dengan bayangan melayang di dalamnya.

Kael melangkah masuk ke ruang yang sudah berubah. Lantai hitam mengilap seperti cermin minyak, udara dipenuhi kabut ungu yang bergerak seperti napas makhluk tidur. Piano tua berdiri di tengah, dengan seorang gadis kecil duduk di sana, memainkan melodi yang tak beraturan—seperti lagu duka yang diputar terbalik.

"Sudah kubilang, jangan sentuh ruang ini," ucap Kael pelan sambil mengayunkan langkah mendekat. "Tapi ya... siapa juga yang dengerin mantan kriminal."

Gadis itu tak menoleh. Nada pianonya berhenti tiba-tiba, seperti senar diputus paksa. "Kau tak bisa menghentikanku."

Kael mengangkat satu alis. "Kalau aku dapat koin setiap kali dengar kalimat itu, aku udah pensiun."

Dinding tiba-tiba mencair, berubah jadi dinding mata. Tangan-tangan hitam menjulur dari balik bayangan, melengkung seperti akar yang lapar.

Kael tersenyum tipis. "Ah... akhirnya. Aku bosen pura-pura jadi guru les."

Tangan-tangan itu menyambar.

Dalam sekejap, tubuh Kael memudar. Kabut hitam menyebar, membentuk siluet manusia dengan mata kuning menyala dari dalam kegelapan. Duskform aktif.

Tangan pertama mencoba menggenggamnya—menembus kabut.

Tangan kedua mencoba memukul—kabutnya berpencar dan muncul di belakang.

"Aduh, payah," ucap Kael, muncul kembali di sisi gadis itu sambil berdiri di atas piano. Ia jongkok, melihat ke bawah. "Kau seharusnya latih mereka dulu sebelum disuruh nyerang veteran, tahu?"

Gadis itu mendesis, dan seluruh ruangan berubah menjadi lorong tak berujung. Bayangan Kael sendiri muncul—versi dirinya yang lebih muda, lebih buas, dan lebih penuh amarah.

"Ini triknya sekarang?" tanya Kael santai. "Ngelempar masa lalu ke mukaku?"

Bayangan Kael menyerang. Gerakannya brutal dan cepat. Pukulan, tendangan, serangan bayangan. Tapi Kael hanya menghindar dengan tenang, tubuhnya membentuk kabut dan berpindah-pindah posisi.

"Yap, itu versi aku waktu baru keluar dari Aetherion. Gaya besar, otak kosong," ejek Kael sambil menangkis tendangan. "Sialnya, tetap keren."

Pertarungan mereka jadi seperti tarian gelap. Setiap pukulan saling menebas udara, tapi tak menyentuh inti. Kabut Duskform merayap di sekeliling ruangan, mengiris penghalang-penghalang ilusi.

Akhirnya, Kael memegang leher versi bayangannya sendiri dan menatap langsung ke matanya.

"Terima kasih udah bikin aku inget... kenapa aku nggak mau jadi orang itu lagi."

Dengan ledakan kabut hitam, bayangan itu lenyap. Gadis di tengah ruangan menjerit, aura hitamnya mengembang menjadi makhluk seperti kelabang raksasa—gabungan kenangan, kesedihan, dan kegelapan spiritual.

Kael memutar lehernya. "Oke... level boss. Finally."

Kelabang itu menyemburkan lidah hitam ke arahnya. Kael berputar di udara, membentuk tombak dari kabut Duskform dan melemparkannya ke mulut makhluk itu—menyegel semburannya dalam satu hentakan.

"Aku udah bosan dengan gaya horor slow-burn ini," ucap Kael, melompat ke atas kepala makhluk itu. "Sekarang giliran kau yang dengerin aku—"

Ia mengarahkan kedua tangannya ke bawah. Kabut hitam mengalir deras, berubah menjadi segel bercahaya yang menyerap makhluk itu secara perlahan, membekukan amarahnya jadi keheningan.

"—Pergilah dengan tenang."

Makhluk itu meledak jadi serpihan cahaya kelam yang berputar pelan lalu menghilang. Ruangan kembali sepi. Piano tua kembali, rusak tapi utuh.

Kael berdiri di tengah, menghela napas. Kabutnya meresap kembali ke tubuhnya.

"...Udah lama nggak sparring serius. Lumayan buat peregangan."

Ia berjalan keluar dari ruang itu, kembali ke atap sekolah. Langit malam tenang, tapi Kael tahu—ini baru permulaan.

Dan kali ini, dia tak akan hanya mengamati dari bayangan.

Malam itu, setelah pertarungan sengit yang menguras tenaga, Kael memilih untuk tidak kembali ke sekolah. Langkahnya berat, tubuhnya terasa kaku, namun perasaan yang bergolak di dalam hatinya lebih kuat dari segala kelelahan. Ia berjalan menelusuri jalanan yang sepi, menyusuri gang-gang kota yang temaram oleh lampu jalanan.

Setelah beberapa saat, akhirnya ia tiba di rumah yang kini ia tinggali bersama Chandra dan Zenki. Pintu depan terbuka tanpa suara saat ia memutar kunci. Tanpa menyalakan lampu, ia melangkah masuk ke dalam rumah yang terasa sunyi.

Di ruang tengah, Chandra dan Zenki tengah duduk, tampak sedang membahas sesuatu dengan serius. Begitu mendengar suara pintu terbuka, keduanya segera mengalihkan perhatian.

Chandra yang baru saja mengangkat kepala menatap Kael dengan mata tajam. "Kau pulang juga," katanya, suaranya penuh tanya. "Kenapa kau terlambat? Apa yang terjadi di sana?"

Zenki menoleh dari tempat duduknya, ekspresinya lebih cemas. "Kael, kau baik-baik saja? Kami mendengar suara pertarungan yang besar tadi."

Kael menghela napas panjang, menatap keduanya tanpa menjawab langsung. Ada sesuatu yang ingin ia sampaikan, tapi perasaannya kacau. Perlahan, ia berjalan menuju dapur dan mulai menyiapkan segelas air. "Aku baik-baik saja," jawabnya akhirnya, meski suaranya terdengar sedikit lelah.

Chandra dan Zenki saling memandang, keduanya bisa merasakan bahwa ada lebih banyak yang belum Kael ungkapkan. Namun, Chandra memilih untuk tidak memaksa, hanya mengangguk pelan. "Kalau kau ingin bicara, kami di sini."

Kael mengangguk, merasa sedikit lega dengan perhatian mereka, meskipun ia tahu bahwa rasa ketegangan masih tetap ada, seperti bayangan yang menunggu untuk dihadapi.

Kael akhirnya duduk di meja makan, menyandarkan punggungnya dengan lelah. Chandra dan Zenki hanya menatapnya, menunggu, sebelum akhirnya Kael mengangkat gelasnya dan berkata, "Kalian tahu, aku baru saja bertarung melawan makhluk bayangan, tapi sepertinya aku harus melawan satu musuh besar lagi..."

Zenki dan Chandra menunggu, penasaran.

"Menurunkan berat badan," Kael menambahkan sambil tersenyum lemah. "Kurasa aku harus berlatih lebih keras daripada melawan makhluk itu. Sudah waktunya aku ikut diet."

Chandra mengernyitkan dahi. "Jadi, selain bertarung dengan makhluk, sekarang kau bertarung dengan makanan juga?"

Kael mengangguk serius, meskipun senyum tak bisa disembunyikan. "Betul, ini pertarungan terbesar dalam hidupku."

Zenki tertawa kecil. "Jika itu pertarungan terberat, mungkin kita bisa minta bantuan Chandra untuk membuatkan menu diet yang aman, ya?"

Chandra mengangkat tangan. "Aku? Aku yang harus bertanggung jawab atas ini? Lebih baik Kael mulai lari pagi!"

Kael menatap keduanya, tersenyum lebar. "Jangan khawatir, kalau aku lari pagi, aku akan sangat cepat, mungkin lebih cepat dari bayanganku sendiri."

Zenki tertawa. "Akhirnya ada hal yang bisa Kael kalahkan selain makhluk bayangan!"

Chandra menambahkan, "Ya, siapa tahu, mungkin dalam beberapa minggu, Kael jadi lebih cepat dari kita dalam hal lari."

Mereka semua tertawa, suasana hangat dan ringan mengisi ruang tamu, meskipun tak ada yang tahu bagaimana pertarungan yang sebenarnya akan berlangsung, baik di dunia nyata maupun dalam dunia diet Kael.

</p></div>
  <div id="bab9" class="section"><h2>Bab 9</h2><p>Pagi itu datang lambat. Cahaya matahari menyusup dari sela tirai kamar, menggambarkan pola-pola lembut di lantai. Dari kejauhan, samar-samar terdengar suara televisi kecil di ruang tengah-mungkin Zenki yang bangun duluan, lagi-lagi nonton kartun pagi sambil ngemil sereal.

Tapi Chandra tak bangkit.

Ia menatap langit-langit kamarnya dengan mata kosong, membiarkan waktu berlalu sampai ia akhirnya melirik ponsel. 7:49. Hari Minggu.

Widget kalender muncul di layar.
"Besok: Mama pulang (jadwal perjalanan)"

"Besok?" gumamnya. Ia mengernyit, duduk perlahan di tempat tidur. "Nggak, harusnya... bukannya hari ini?"

Kebingungan mulai merayap. Ia membuka chat terakhir dari mama-nya. Terakhir terlihat: tiga hari lalu. Pesan-pesannya belum terbaca. Ada perasaan dingin yang mengendap di dadanya.

Notifikasi baru menunggu di atas. Sebuah pesan dari nomor tak dikenal.

> [RSUD Kota KYOKU - Bagian Informasi]
Kepada keluarga Ny. Sari Prameswari, kami menginformasikan bahwa beliau mengalami kecelakaan lalu lintas dan saat ini dirawat di ruang ICU. Mohon segera menghubungi pihak rumah sakit untuk informasi lebih lanjut.

Layar ponsel bergetar ringan di tangan Chandra, lalu jatuh membentur selimut.

Suaranya tercekat. Dunia mendadak menyempit, seolah gravitasi menariknya ke dasar.

Zenki mengetuk pintu dari luar.
"Chandra? Lo bangun, kan? Kael masak mi instan tapi... euh, nggak yakin itu bisa dimakan."

Tak ada jawaban. Hanya hening.

Zenki menunggu sebentar, lalu perlahan membuka pintu.

Saat ia melihat Chandra duduk di ujung ranjang, menatap kosong ke dinding dengan tangan gemetar, Zenki langsung tahu sesuatu salah.

"Chandra...?"

Chandra menoleh, matanya memerah.
"Zenki... mama gue... kecelakaan."

Zenki membeku di ambang pintu, seolah tak yakin ia mendengar dengan benar.

"Kecelakaan?" bisiknya.

Chandra mengangguk pelan, lalu menggeser ponselnya ke arah Zenki. Ia tak sanggup berkata apa-apa lagi.

Zenki mengambilnya, membaca pesan dari rumah sakit. Wajahnya mengeras, matanya bergeser dari layar ke sahabatnya.

"Lo... mau kita ke sana sekarang?" tanyanya pelan.

Sebelum Chandra sempat menjawab, langkah berat terdengar dari lorong belakang. Kael muncul, tangan masih memegang cangkir teh yang mengepul.

"Ada apa?" tanyanya sambil menatap ekspresi mereka berdua.

Zenki menyodorkan ponsel ke arah Kael tanpa sepatah kata pun.

Kael membaca cepat, lalu diam beberapa detik. Uap teh mengepul di antara mereka, mengisi keheningan yang berat.

"...Kita berangkat sekarang," katanya akhirnya, tenang tapi tegas. "Tapi lo harus siap, Chan. Rumah sakit bakal banyak pertanyaan. Mungkin juga... hal yang nggak pengin lo dengar."

Chandra menunduk. Tangan kirinya mengepal di atas lutut, tapi ia mengangguk.

"Aku siap," gumamnya. Suaranya serak, tapi matanya sudah tidak gemetar seperti tadi.

Kael menaruh cangkirnya di atas meja dekat pintu, lalu menoleh pada Zenki.
"Siapkan jaket, dan tas kecil. Gue urus transportasi."

Zenki bergerak cepat ke kamarnya.
Sementara itu, Chandra masih duduk di tepi ranjang, membiarkan semuanya bergerak di sekelilingnya. Tapi di dalam dadanya, ada sesuatu yang baru mulai tumbuh-bukan hanya kesedihan, tapi juga tekad.

Zenki membeku di ambang pintu, seolah tak yakin ia mendengar dengan benar.

"Kecelakaan?" bisiknya.

Chandra mengangguk pelan, lalu menggeser ponselnya ke arah Zenki. Ia tak sanggup berkata apa-apa lagi.

Zenki mengambilnya, membaca pesan dari rumah sakit. Wajahnya mengeras, matanya bergeser dari layar ke sahabatnya.

"Lo... mau kita ke sana sekarang?" tanyanya pelan.

Sebelum Chandra sempat menjawab, langkah berat terdengar dari lorong belakang. Kael muncul, tangan masih memegang cangkir teh yang mengepul.

"Ada apa?" tanyanya sambil menatap ekspresi mereka berdua.

Zenki menyodorkan ponsel ke arah Kael tanpa sepatah kata pun.

Kael membaca cepat, lalu diam beberapa detik. Uap teh mengepul di antara mereka, mengisi keheningan yang berat.

"...Kita berangkat sekarang," katanya akhirnya, tenang tapi tegas. "Tapi lo harus siap, Chan. Rumah sakit bakal banyak pertanyaan. Mungkin juga... hal yang nggak pengin lo dengar."

Chandra menunduk. Tangan kirinya mengepal di atas lutut, tapi ia mengangguk.

"Aku siap," gumamnya. Suaranya serak, tapi matanya sudah tidak gemetar seperti tadi.

Kael menaruh cangkirnya di atas meja dekat pintu, lalu menoleh pada Zenki.
"Siapkan jaket, dan tas kecil. Gue urus transportasi."

Zenki bergerak cepat ke kamarnya.
Sementara itu, Chandra masih duduk di tepi ranjang, membiarkan semuanya bergerak di sekelilingnya. Tapi di dalam dadanya, ada sesuatu yang baru mulai tumbuh-bukan hanya kesedihan, tapi juga tekad.

Langit pagi mendung. Awan-awan kelabu menggantung rendah di atas jalanan kota, seolah ikut menahan napas bersama Chandra.

Mereka bertiga duduk dalam taksi yang melaju tanpa banyak suara. Sopir di depan tampaknya mengerti suasana, karena radio dimatikan dan kaca belakang dibiarkan sedikit terbuka, membiarkan udara lembab masuk pelan-pelan.

Zenki duduk di sebelah Chandra, sesekali melirik sahabatnya yang menatap kosong ke luar jendela. Tangannya menggenggam erat ponsel, seperti masih berharap akan ada pesan baru masuk dari Mama.

Kael duduk di kursi depan, diam, menatap lurus ke depan dengan mata tajam tapi tenang. Tangan kirinya menggenggam tepi pintu mobil, sementara tangan kanan sesekali mengecek sesuatu dari dompet hitam kecil di saku jaketnya-kartu identitas atau mungkin... sesuatu lain.

Setelah lima belas menit, Zenki akhirnya bicara pelan.

"Gue yakin Mama lo kuat, Chan."

Chandra hanya mengangguk pelan. "Dia selalu pulang. Selalu. Bahkan kalau kerjaannya berat banget, dia tetap sempat masak buat gue..." Suaranya melemah. "Gue bahkan belum sempat bilang makasih terakhir kali."

Zenki menunduk. Tak tahu harus menjawab apa.

Taksi melewati pertigaan besar, lalu mulai memasuki kawasan rumah sakit. Bangunan abu-abu tinggi dengan papan nama RSUD tampak di kejauhan. Di pelataran depan, orang-orang berjalan dengan wajah lelah dan raut cemas.

Chandra menelan ludah. Tangannya gemetar saat ponsel memberi notifikasi baru:

> [Lokasi] RSUD KYOKU, Lantai 3 - ICU

Kael akhirnya menoleh. "Begitu kita sampai, gue yang bicara dulu dengan petugas. Lo tetap tenang. Apa pun yang terjadi... kita hadapi bareng-bareng."

Taksi berhenti. Chandra menarik napas dalam, dan pintu terbuka dengan bunyi pelan.

Saat ia melangkah keluar, tanah di bawah sepatunya terasa berat. Tapi di belakangnya, langkah Zenki dan Kael mengikuti dengan mantap.

Mereka bertiga berdiri di depan pintu rumah sakit. Dunia terasa berubah. Seolah semuanya jadi lebih nyata, lebih sunyi, dan lebih penting dari sebelumnya.

Lorong rumah sakit terasa dingin dan asing. Bau antiseptik tajam menyengat hidung, bercampur aroma samar kopi basi dari ruang tunggu sebelah.

Chandra berjalan paling depan, diapit Zenki dan Kael. Matanya menatap papan petunjuk di atas-ICU, Lantai 3.

Lift berbunyi pelan saat pintunya terbuka. Mereka masuk bertiga. Di dalam, tak ada suara selain derit lembut mesin.

Namun, saat lift mulai bergerak ke atas, Kael mengerutkan dahi. Ia merasakan sesuatu-tekanan halus di udara, seperti perubahan suhu yang tak bisa dijelaskan.

Zenki merasakannya juga. Ia melirik ke cermin di sudut kabin. Sekilas, ada bayangan berdiri di belakang mereka, padahal lift hanya diisi tiga orang.

Bayangan itu tinggi dan kurus, dengan bentuk tubuh samar, dan mata hitam kosong seperti dua lubang dalam kabut.

Chandra tidak melihatnya. Ia terlalu tenggelam dalam pikirannya sendiri.

Zenki ingin berkata sesuatu, tapi Kael hanya menggeleng pelan, lirih. "Abaikan."

Lift berbunyi-lantai tiga.

Bayangan itu menghilang seiring pintu terbuka.

---

Lorong ICU lebih sunyi. Hanya ada bunyi alat pemantau dan langkah suster yang cepat. Seorang wanita muda berpakaian rapi mendekati mereka.

"Anda keluarga dari Ny. Sari Prameswari?" tanyanya lembut.

Chandra mengangguk. Suaranya tidak keluar.

"Beliau dalam kondisi stabil untuk saat ini. Masih belum sadar, tapi kami sedang melakukan pemantauan intensif. Kalian bisa melihat dari balik kaca."

Zenki menepuk bahu Chandra pelan. "Ayo."

Mereka berjalan menyusuri lorong. Di sisi kiri, dinding kaca memperlihatkan kamar ICU. Di sana, Mama Chandra terbaring lemah, dipenuhi selang dan monitor.

Chandra berdiri diam. Wajahnya pucat. Tapi ia tidak menangis. Ia hanya berdiri, menggenggam tangan sendiri erat-erat.

Di belakang mereka, entitas bayangan kembali muncul di ujung lorong-lebih jelas kini, matanya menatap langsung ke arah mereka.

Tapi tak ada yang berbalik.

Kael melipat tangan. Zenki menatap lurus ke Mama Chandra. Dan Chandra...

Chandra melangkah maju, meletakkan tangannya di kaca, lalu berbisik, "Ma, aku di sini. Aku nggak akan pergi."

Makhluk itu tetap di sana, menunggu. Tapi tak ada ruang untuk ketakutan di antara mereka.

Chandra menatap ibunya dari balik kaca. Wajah Mama pucat, tubuhnya tak bergerak, hanya suara detak mesin dan kedipan angka di monitor yang membuktikan bahwa ia masih di sana.

Zenki berdiri di sampingnya, diam, sementara Kael sedikit menjauh, berdiri dekat dinding, menajamkan naluri. Aura entitas bayangan yang tadi mereka lihat belum hilang-ia tahu ada sesuatu yang belum selesai.

Beberapa menit berlalu.

Lalu tiba-tiba-
Alarm monitor berbunyi.
Cepat, panik. Cahaya merah berkedip.

Beberapa suster dan seorang dokter berlari masuk ke kamar ICU, menutup tirai. Chandra terkejut dan refleks menyentuh kaca.

"Ada apa?!"

Zenki menoleh ke Kael, yang wajahnya sudah mengeras.

"Kael...?"

Kael bergumam, hampir tak terdengar. "Kematian... sudah masuk ruangan itu."

"Tidak... tidak..." Chandra mulai panik. "Nggak bisa sekarang. Dia belum sempat pulang... Dia belum sempat-"

Seorang suster keluar beberapa menit kemudian, wajahnya muram. Ia menghampiri mereka perlahan.

"Kami mohon maaf... Ibu Sari mengalami henti jantung mendadak. Kami sudah melakukan prosedur, tapi..."

Chandra tak mendengar sisanya. Dunia seolah memudar. Suara-suara memantul tak jelas.

Zenki langsung memegang bahunya, kuat. Tapi Chandra menjatuhkan diri ke lantai, punggungnya menyandar ke dinding, menatap lurus ke depan tanpa kata. Air matanya tak keluar, tapi tubuhnya bergetar.

Di ujung lorong... entitas bayangan itu tersenyum samar. Ia tidak menyerang, tidak muncul dalam wujud mengerikan. Ia hanya berdiri-menyaksikan-sebagai lambang dari kehilangan yang tak bisa dilawan.

Kael maju, berdiri di antara makhluk itu dan Chandra, matanya menyala pelan. Aura Duskform milik Kael menyelimuti sekitarnya, lalu Chandra tiba tiba memberi arahan ke kael:

"Jangan sekarang."

Makhluk itu memudar... dan menghilang.

Chandra memejamkan mata. Di antara kehampaan itu, satu suara bergema dalam pikirannya-suara Mama, yang terakhir ia dengar dalam pesan suara tiga hari lalu:

> "Jaga dirimu ya, Nak. Mama pulang sebentar lagi."

Tapi tidak ada "sebentar lagi." Hanya sisa kata yang menggantung di ruang hampa.

Beberapa jam kemudian.

Hujan turun deras di luar rumah sakit. Mereka bertiga berdiri di bawah atap halte kecil, menunggu angkutan umum berikutnya. Tidak ada yang bicara.

Zenki memegangi payung, melindungi Chandra dari hujan, tapi Chandra tetap diam-tatapannya kosong, tubuhnya terasa lebih berat dari biasanya.

Akhirnya, mobil van tua berhenti. Mereka naik, duduk di bangku panjang, bergoyang lembut mengikuti jalanan basah. Kael duduk di seberang, menatap keluar jendela dengan ekspresi keras tapi penuh pikiran. Zenki menggenggam lututnya, menatap Chandra dengan cemas.

Tak satu pun dari mereka bicara selama perjalanan pulang.

Rumah tampak lebih sunyi dari biasanya.
itu gelap saat mereka masuk. Hanya suara deras hujan di luar dan detak jarum jam di dinding yang terdengar. Kael melepas jaketnya, menggantungnya tanpa bicara. Zenki berjalan lebih dulu ke dapur, mungkin ingin membuat teh, tapi langkahnya pun ragu-ragu.

Chandra berdiri di ambang ruang tengah. Semuanya terasa seperti mimpi yang berat-seolah tubuhnya bergerak tapi jiwanya tertinggal di kamar rumah sakit, di sisi ranjang yang kini kosong.

"Chandra," suara Kael datar namun dalam, "kalau kamu perlu sendiri, kami ngerti."

Tapi Chandra menggeleng pelan. "Aku... cuma mau masuk kamar dulu."

Ia berjalan menuju kamarnya, membuka pintu, dan menutupnya perlahan. Tidak menguncinya-ia tahu tak ada yang akan mengganggunya malam ini.

Chandra duduk sendiri dalam gelap kamar. Hujan di luar masih mengguyur seperti menggoda pikirannya untuk meledak. Tapi yang keluar dari dirinya bukan teriakan, bukan tangis. Hanya... keheningan.

Ia menunduk. Tangan kirinya mengepal. Dada terasa sesak, tapi bukan karena kesedihan semata. Ada yang berubah. Dalam dirinya. Sejak rumah sakit.

Bibirnya bergerak pelan, nyaris tanpa suara.
"Ma... aku gak tahu harus apa sekarang..."

Tiba-tiba... getaran halus terasa di ujung jari. Chandra mengangkat tangan, dan dalam remang cahaya dari luar jendela, ia melihat kilatan samar berwarna biru. Kecil. Ringan. Seperti percikan listrik-tapi bukan listrik.

Itu bukan batu. Bukan artefak. Tapi percikan kekuatan murni. Dan itu muncul bukan karena amarah. Tapi karena kehilangan.

Ia menarik napas tajam. Lalu meletakkan telapak tangannya di dada.

Biru itu menyebar sedikit, seperti garis halus yang tumbuh, mengalir dari dalam-seperti akar.

Bukan hanya kekuatan. Ini... adalah bentuk baru dari pemahaman. Kepekaan terhadap dunia di sekitarnya. Terhadap rasa dan ikatan.

Kael pernah bilang: "Telekinesis bukan cuma soal menggerakkan barang. Tapi memahami beban mereka."

Chandra yang sudah merasa kelelahan setelah seharian menghadapi berbagai peristiwa yang menegangkan, apalagi setelah kehilangan orang yang melahirkan dan merawatnya sejak kecil, akhirnya terlelap dalam tiduran yang dalam. Suasana yang sepi membuatnya terbuai dalam keletihan, membiarkan dirinya terlepas dari beban yang ada.

Zenki dan Kael, yang melihat pintu kamar Chandra masih terbuka, saling bertukar pandang sebelum mendekat. Mereka memasuki kamar dengan hati-hati dan melihat Chandra yang sudah tertidur, wajahnya tampak tenang meski rautnya masih menyisakan sedikit kelelahan. Dengan lembut, Kael mendekat dan menutup pintu kamar perlahan, memastikan tidak ada suara atau gangguan yang akan mengganggu kedamaian tidurnya.

Keesokan paginya

Cahaya matahari pagi mulai menembus masuk melalui jendela, menyinari sudut-sudut rumah Chandra dengan lembut. Di dalam kamar, Chandra masih terlelap, tenggelam dalam tidur panjang yang memang sangat ia butuhkan. Tidak ada satu pun yang berniat membangunkannya-Zenki dan Kael sangat memahami kondisi Chandra saat ini. Mereka tahu, setelah semua yang terjadi, ia butuh waktu untuk tenang.

Di ruang tamu, Kael duduk bersandar di ambang pintu, menikmati pagi sambil menyeruput kopi hitam pahit yang ia seduh sendiri. Sementara itu, Zenki duduk di dekatnya, menyantap mie goreng buatan Kael dengan lahap, tak menyisakan setengah pun.

"Wah, mie buatanmu nggak kalah enak dari masakan Chandra," celetuk Zenki di sela-sela suapan, memecah keheningan saat Kael sedang menikmati kopinya.

Kael tersenyum tipis dan menjawab santai, "Ya, kalau cuma masak mie sih, masih bisa lah."

Tiba-tiba, suara engsel pintu kamar berderit pelan. Pintu terbuka, dan Chandra melangkah keluar dengan langkah gontai. Wajahnya tampak lesu, lemas, dan pucat, jelas belum benar-benar pulih dari kelelahan dan luka emosional yang ia pendam.

Melihat itu, Kael langsung sigap. Ia menunjuk ke piring mie yang masih mengepul ringan di meja.

"Ndra, itu ada mie, udah gua masakin buat lu. Makan, sebelum keburu dingin," ucapnya lembut, suaranya nyaris seperti bisikan, seolah tak ingin menambah beban pada Chandra.

Chandra hanya menjawab singkat, dengan suara lemah, "Iya, nanti ku makan."

Zenki dan Kael saling melirik sekilas-mereka tahu, hari ini bukan tentang memaksanya bangkit. Tapi cukup dengan ada di sisinya, perlahan mereka yakin Chandra akan kembali kuat.

Chandra lalu duduk perlahan di kursi ruang tamu, menarik napas pendek sebelum bertanya dengan suara serak dan lemah, "Lu pada kagak sekolah?"

Kael menjawab tanpa ragu, nada suaranya mantap dan tegas, "Gapapa sesekali bolos. Lagian, teman macam apa yang ninggalin temannya yang lagi sedih dan berduka cuma demi sekolah?"

Mendengar itu, Chandra tersenyum tipis, senyum yang jarang terlihat sejak kejadian itu. "Makasih ya... lu pada," ucapnya tulus, dari hati yang perlahan mulai menghangat.

Ia mulai menyantap mie yang disajikan Kael, perlahan tapi pasti, suapan demi suapan mengisi kekosongan di perut dan hatinya. Sementara itu, Zenki yang sudah selesai makan bersandar di kursi dengan perut kenyang, mengelus perutnya sambil menghembuskan napas lega. Di sisi lain, Kael meneguk tegukan terakhir dari kopinya, menikmati sisa rasa pahit yang menenangkan.

Sunyi sejenak menyelimuti ruangan, hingga akhirnya Zenki memecah keheningan, merasa tak betah dengan suasana yang terlalu hening dan canggung.

"Chandra... setelah semua kejadian kemarin, ada hal aneh lagi yang lu rasain gak?" tanyanya hati-hati, namun penuh rasa ingin tahu.

Belum sempat Chandra menjawab, Kael menyela dengan nada santai namun mengingatkan, "Woy, buru-buru amat nanyanya, Zen. Chandra aja belum kelar makan."

Zenki hanya nyengir kecil, merasa sedikit malu. Sementara itu, Chandra hanya menunduk sambil tersenyum tipis-untuk pertama kalinya pagi itu, ia merasa sedikit lebih ringan.

"Ada," ucapnya pelan, suaranya seperti bisikan yang mencuri perhatian Kael dan Zenki seketika.

Kael langsung menegakkan posisi duduknya. Zenki pun tak lagi bersandar, tubuhnya maju sedikit, penuh atensi.

"Apa yang lu rasain?" tanya Kael, kali ini serius tapi tetap tenang.

Chandra mengangkat tangan kanannya perlahan, memperlihatkan telapak yang gemetar sedikit. "Tadi malam... waktu gue duduk sendiri di kamar... ada yang muncul. Bukan kayak waktu gue ngamuk... tapi kayak... sesuatu dari dalam. Rasanya... biru."

"Biru?" ulang Zenki, bingung.

"Biru... kayak sinar. Kayak akar yang tumbuh dari dada, dari dalam. Lembut... tapi dalam banget. Gue ngerasa kayak... gue nyambung sama sesuatu. Sama semuanya. Sama... dia juga," suara Chandra gemetar, namun penuh makna.

Zenki terdiam, mendadak tak bisa menyela. Sementara Kael mengangguk pelan.

"Gue ngerti maksud lu," ucap Kael. "Itu bukan cuma kekuatan. Itu resonansi. Bentuk dari keterikatan lu dengan dunia. Kalau lu bisa mencapai itu tanpa amarah atau ketakutan... berarti lu udah masuk ke tahap selanjutnya."

Chandra memejamkan mata sejenak, mencoba mengingat kembali momen itu. "Itu bukan tentang ngangkat barang. Tapi ngerasain beratnya. Kayak lu bilang waktu itu, Kael..."

Kael menatapnya tajam namun lembut. "Dan itu bukan hal yang semua orang bisa capai. Bahkan banyak esper yang mentok karena gak pernah ngerti bagian itu."

Zenki mengusap dagunya, lalu bersuara pelan, "Apa itu berarti lu udah... nyatu sama kekuatan lu, Ndra?"

Chandra mengangguk pelan. "Atau mungkin... baru mulai nyatu. Tapi gue ngerasa... ibu gue-meski dia udah gak ada, perasaan itu masih nyisa. Kayak jejaknya ninggalin sesuatu. Dan itu yang muncul dalam bentuk percikan itu."

Sunyi menyelimuti ruangan beberapa detik. Kael bangkit dari duduknya, berjalan pelan ke arah jendela, menatap keluar sejenak.

"Kalau gitu, kita harus mulai persiapan," katanya tiba-tiba, nadanya berubah serius.

Zenki kaget. "Persiapan apa?"

Kael berbalik, wajahnya tampak lebih tegas dari sebelumnya. "Chandra baru masuk tahap baru. Dan kita gak bisa santai-santai. Entitas yang masuk ke Raka kemarin... itu bukan yang terakhir."

Chandra menegang. "Lu pikir... bakal ada yang lain?"

Kael mengangguk. "Bukan cuma pikir. Gue yakin. Gue lihat pola energi yang mulai muncul dari ruang spiritual. Dan kalau firasat gue benar, kita butuh semua kekuatan yang kita punya-dan lebih."

Zenki menatap Chandra dan Kael bergantian. "Jadi... kita bakal latihan?"

Kael tersenyum tipis. "Bukan cuma latihan. Kita akan bentuk tim. Dan mulai dari sekarang, rumah ini... markas kita."

Chandra menatap Kael, lalu Zenki, dan entah bagaimana, untuk pertama kalinya setelah kepergian ibunya... ia merasa tidak sendirian. Ia mengangguk pelan, menyambut langkah baru itu.

"Ayo mulai," ucapnya lirih. "Sebelum yang lain datang."

</p></div>
  <div id="bab10" class="section"><h2>Bab 10</h2><p>Langit sore di Kyoku memerah tipis, seolah mencerminkan rasa kehilangan yang perlahan mulai berubah menjadi sesuatu yang lebih dalam-sebuah kekuatan yang belum berbentuk.

Rumah mereka kini tak lagi sekadar tempat berteduh. Meja ruang tamu dipenuhi coretan-coretan kasar tentang pola energi, simbol-simbol spiritual, dan catatan tentang entitas bayangan. Dinding sisi barat dipasangi papan gabus tempat Kael menempelkan foto-foto, sketsa, dan diagram jalur kekuatan yang ia amati. Salah satu sudut rumah bahkan disulap menjadi ruang latihan meditasi sederhana-beralaskan karpet tipis, ditandai dengan lingkaran kapur dan beberapa batu penyeimbang aura.

Chandra duduk bersila di tengah ruangan itu, matanya terpejam, sementara Zenki di sebelahnya, dalam posisi yang sama, mencoba mengatur napas sesuai dengan bimbingan Kael yang berdiri mengawasi.

"Fokus bukan pada apa yang lo rasakan dari dalam," ucap Kael tenang, "tapi pada apa yang berubah di sekitar lo ketika lo hadir sepenuhnya."

Zenki mengerutkan alis. "Gue gak ngerasain apa-apa, selain dengkul gue mulai kesemutan."

Kael menghela napas pelan. "Makanya lo belum siap buka lapisan kedua dari Nethermind lo."

"Lapisan kedua?" Chandra membuka mata. "Bukannya kemarin Zenki udah bisa masuk dunia spiritual?"

Kael mengangguk. "Itu baru gerbang. Nethermind itu bukan cuma dunia bayangan. Di dalamnya ada lapisan emosi, kesadaran kolektif, bahkan mimpi yang terlupakan. Untuk masuk ke sana, lo gak cukup cuma kuat. Lo harus... jujur."

Zenki memejamkan mata lagi, mencoba memahami maksudnya. Tapi pikirannya masih kacau. Bayangan Raka, suara tangisan di lorong rumah sakit, dan kemunculan makhluk hitam itu semua bercampur di benaknya.

Sementara itu, Chandra merasa halusnya getaran dari dalam dirinya kembali muncul. Seperti akar biru yang kemarin, tapi kini lebih perlahan, lebih dalam. Ia mencoba membayangkan suara ibunya, bukan saat terakhir, tapi saat kecil-ketika ia demam dan sang ibu mengusap keningnya sambil bernyanyi pelan.

> "Langit masih tinggi, Nak. Tapi kakimu udah cukup kuat buat jalan..."

Suatu rasa hangat mengalir dari dadanya. Cahaya biru samar menyebar di udara sekitarnya. Zenki terkejut, membuka mata saat melihat partikel halus bercahaya melayang dari tubuh Chandra-bukan hanya telekinesis, tapi sesuatu yang menyentuh ruang spiritual.

"...Dia berhasil," gumam Kael. "Dia membuka resonansi pertamanya."

"Rasanya... kayak gue denger suara nyokap, tapi juga suara lo berdua... dan... dunia. Tapi bukan suara beneran. Kayak gema yang lembut."

Kael mengangguk pelan. "Itu resonance. Lo gak cuma nyatu sama kekuatan lo, Ndra. Tapi sama luka lo, sama kehilangan lo, dan... sama kita."

Tiba-tiba, aura dingin menusuk dari balik dinding.

Kael segera berdiri tegak. "Kalian diam di sini."

Langkahnya cepat menuju jendela belakang, membuka tirai sedikit. Di luar-langit sudah gelap, dan dari atap rumah tetangga, seekor makhluk melata seperti kabut bergelantungan. Tubuhnya tipis seperti tali asap hitam, dengan mata merah menyala samar.

Zenki merasakan tekanan itu juga. "Itu... bukan yang dari rumah sakit?"

Chandra berdiri. "Gue bisa bantu."

"Tidak," tegas Kael. "Kalian belum siap buat bentrok langsung. Gue bisa tarik ini ke luar batas kota."

Namun, makhluk itu bergerak duluan. Ia tak menyerang-ia berbicara.

"Pilar biru telah bangkit... dan karena itu, sang penjaga lama harus bangun kembali."

Kael menyipitkan mata. "Apa maksudmu?"

"Tujuh pilar... Tujuh resonansi... dan satu yang telah tidur terlalu lama. Jika ia terbangun, dunia ini akan terpecah."

Makhluk itu menghilang, melebur menjadi bayangan yang meresap ke bumi. Tapi kata-katanya tertinggal seperti asap di udara.

Chandra berdiri membatu. "Pilar biru... itu gue?"

Zenki melirik Kael. "Apa maksudnya 'penjaga lama'?"

Kael berjalan kembali ke ruang latihan, diam beberapa saat sebelum akhirnya berkata, "Ada satu makhluk spiritual yang disebut dalam teks kuno-Sang Penjaga Resonansi. Ia bukan musuh, tapi juga bukan kawan. Ia hanya muncul jika ada resonansi yang membahayakan keseimbangan dunia."

Zenki berkedip. "Lo yakin itu bukan cuma dongeng, Kael?"

Kael menggeleng. "Gue gak yakin lagi. Gue tahu satu-satunya cara untuk menghadapinya-adalah dengan menyatukan ketujuh pilar. Dan kita baru punya dua."

Sunyi menyelimuti ruangan.

Chandra perlahan menatap kedua temannya. "Kalau gitu... kita cari yang lainnya. Siapa pun mereka. Sebelum sang penjaga bangun sepenuhnya."

Kael mengangguk. "Kita mulai pencarian besok. Tapi malam ini... kita meditasi. Kita masuk ke dalam resonance kalian. Kita telusuri akar kekuatan kalian dari dalam. Bukan untuk bertarung. Tapi untuk mengenal diri sendiri."

Zenki menatap api kecil dari lilin meditasi. "Kalau gue takut... gimana?"

Kael menjawab tenang. "Takut bukan dosa. Tapi kalau lo lari dari rasa takut... lo gak bakal nemu siapa lo sebenarnya."

Dan malam itu, di bawah langit Kyoku yang mulai diterpa hujan gerimis, tiga esper muda itu memulai perjalanan ke dalam jiwa masing-masing.

Ke dalam resonance.

POV chandara

Resonance - Chandra

Sementara itu, di sisi lain, Chandra mendapati dirinya berada dalam dunia yang berbeda. Ketika matanya terpejam dan pikirannya menyatu dengan lingkaran meditasi, ia merasa tubuhnya melayang. Tapi bukan ke bawah-melainkan ke dalam cahaya.

Ia membuka mata, dan menemukan dirinya berdiri di tengah lapangan rumput yang basah embun. Udara harum, seperti pagi hari setelah hujan. Di kejauhan, langit jingga memudar ke biru pucat, dan pohon-pohon tinggi menjulang seolah mengawasi tanpa suara.

Tapi ini bukan tempat nyata.

Di tengah lapangan itu, berdiri rumah lamanya-bukan rumah sekarang, tapi rumah masa kecilnya, lengkap dengan jendela kayu dan pagar rapuh yang pernah ia warnai sendiri. Suara nyanyian terdengar dari dalam.

> "Langit masih tinggi, Nak..."

Langkah Chandra gemetar saat ia mendekati pintu. Ia tahu ini bukan benar-benar nyata. Tapi juga bukan ilusi. Ini ingatan yang hidup. Resonansi yang membentuk ruang batinnya.

Ia masuk.

Di dalam, tak ada siapa-siapa. Tapi setiap benda punya gema. Sapu yang bersandar di dinding-tawa ibunya. Kursi kayu tua-suara ayahnya sebelum pergi. Dan di atas meja makan, ada satu benda: batu kecil berwarna biru, memancarkan cahaya yang selaras dengan dadanya.

Ketika ia menyentuh batu itu, ruangan berubah.

Tembok runtuh perlahan, dan rumah itu larut menjadi bentuk cahaya. Chandra berdiri di tengah pusaran cahaya biru, dan mendengar suara yang lebih dalam-bukan suara manusia, tapi gema spiritual yang menyatu dengan nadinya.

"Resonansi bukan tentang kekuatan... tapi tentang keterhubungan."

Di hadapannya, terbentuk simbol biru-bukan sekadar simbol kekuatan, tapi lambang Pilar Kesadaran. Ia melihat bayangan Kael dan Zenki di balik lapisan cahaya. Mereka ada di sana. Bersamanya.

Dan untuk pertama kalinya, Chandra merasa... utuh.

---

Udara di ruangan meditasi terasa berbeda. Lebih tenang. Lebih padat dengan kehadiran spiritual.

Kael menatap mereka Chandra . Bibirnya terangkat sedikit.

"Selamat datang... di resonance mu Chandra ."

</p></div>
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
