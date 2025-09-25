<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>SMK Negeri 7 Batam - Profil Sekolah</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <a class="brand" href="#">SMK Negeri 7 Batam</a>
      <button id="nav-toggle" class="nav-toggle" aria-label="Buka menu">☰</button>
      <nav id="main-nav" class="main-nav">
        <ul>
          <li><a href="#home">Beranda</a></li>
          <li><a href="#about">Tentang</a></li>
          <li><a href="#programs">Program Keahlian</a></li>
          <li><a href="#news">Berita</a></li>
          <li><a href="#gallery">Galeri</a></li>
          <li><a href="#contact">Kontak</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <!-- Hero -->
    <section id="home" class="hero">
      <div class="container hero-inner">
        <div class="hero-text">
          <h1>INOVATIF DAN BERBUDAYA</h1>
          <p>Selamat datang di website resmi SMK Negeri 7 Batam — tempat berkembangnya kompetensi dan karakter.</p>
          <a class="btn" href="#about">Selengkapnya</a>
        </div>
        <div class="hero-image">
          <!-- ganti src dengan foto sekolah -->
          <img src="assets/hero-placeholder.jpg" alt="Gedung sekolah">
        </div>
      </div>
    </section>

    <!-- About -->
    <section id="about" class="section about">
      <div class="container">
        <h2>Tentang Sekolah</h2>
        <p>SMK Negeri 7 Batam adalah ... (isi singkat profil sekolah, visi & misi).</p>
        <div class="cards">
          <article class="card">
            <h3>Visi</h3>
            <p>Menjadi sekolah kejuruan unggul...</p>
          </article>
          <article class="card">
            <h3>Misi</h3>
            <p>Meningkatkan kompetensi peserta didik...</p>
          </article>
          <article class="card">
            <h3>Akreditasi</h3>
            <p>A / B / C (ubah sesuai keadaan)</p>
          </article>
        </div>
      </div>
    </section>

    <!-- Programs -->
    <section id="programs" class="section programs">
      <div class="container">
        <h2>Program Keahlian</h2>
        <div class="program-grid">
          <div class="program">
            <img src="assets/program1.jpg" alt="Teknik Komputer dan Jaringan">
            <h4>Teknik Komputer & Jaringan</h4>
            <p>Deskripsi singkat program.</p>
          </div>
          <div class="program">
            <img src="assets/program2.jpg" alt="Multimedia">
            <h4>Multimedia</h4>
            <p>Deskripsi singkat program.</p>
          </div>
          <div class="program">
            <img src="assets/program3.jpg" alt="Otomotif">
            <h4>Otomotif</h4>
            <p>Deskripsi singkat program.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- News -->
    <section id="news" class="section news">
      <div class="container">
        <h2>Berita & Pengumuman</h2>
        <div class="news-list">
          <article class="news-item">
            <h3><a href="#">Judul Pengumuman / Berita 1</a></h3>
            <time datetime="2025-09-24">24 Sep 2025</time>
            <p>Ringkasan berita singkat. <a href="#">Baca selengkapnya →</a></p>
          </article>
          <article class="news-item">
            <h3><a href="#">Judul Berita 2</a></h3>
            <time datetime="2025-09-10">10 Sep 2025</time>
            <p>Ringkasan berita singkat.</p>
          </article>
        </div>
      </div>
    </section>

    <!-- Gallery -->
    <section id="gallery" class="section gallery">
      <div class="container">
        <h2>Galeri</h2>
        <div class="gallery-grid">
          <img src="assets/thumb1.jpg" alt="Foto 1">
          <img src="assets/thumb2.jpg" alt="Foto 2">
          <img src="assets/thumb3.jpg" alt="Foto 3">
          <img src="assets/thumb4.jpg" alt="Foto 4">
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="section contact">
      <div class="container">
        <h2>Kontak</h2>
        <p>Alamat: Jl. Contoh No.1, Batam</p>
        <p>Telepon: (0778) 123456</p>
        <p>Email: info@smknegeri7batam.sch.id</p>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container footer-inner">
      <p>&copy; <span id="year"></span> SMK Negeri 7 Batam. Semua hak cipta dilindungi.</p>
      <p class="small">Dibuat dengan ❤️</p>
    </div>
  </footer>

  <script>
    // tahun otomatis
    document.getElementById('year').textContent = new Date().getFullYear();

    // nav toggle mobile
    const navToggle = document.getElementById('nav-toggle');
    const mainNav = document.getElementById('main-nav');
    navToggle.addEventListener('click', () => {
      mainNav.classList.toggle('open');
    });

    // smooth scroll (opsional)
    document.querySelectorAll('a[href^="#"]').forEach(a => {
      a.addEventListener('click', function(e){
        e.preventDefault();
        const el = document.querySelector(this.getAttribute('href'));
        if(!el) return;
        el.scrollIntoView({behavior: 'smooth', block: 'start'});
        if (mainNav.classList.contains('open')) mainNav.classList.remove('open');
      });
    });
  </script>
</body>
</html>
