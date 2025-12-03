<script>
  import { onMount } from 'svelte';
  import { 
    ShieldAlert, 
    Dices, 
    Fish, 
    Copyright, 
    Siren, 
    Ban,
    ChevronLeft,
    Globe
  } from 'lucide-svelte';

  let currentDate = "";
  let blockedDomain = "";
  let currentYear = new Date().getFullYear();

  onMount(() => {
    blockedDomain = window.location.hostname;
    currentDate = new Date().toLocaleString('id-ID', {
      weekday: 'long',
      year: 'numeric',
      month: 'long',
      day: 'numeric',
      hour: '2-digit',
      minute: '2-digit'
    });
  });
</script>

<svelte:head>
  <meta charset="UTF-8" />
  <meta name="description"
    content="Halaman blokir Internet Positif dari Kementerian Komunikasi dan Digital Republik Indonesia. Situs ini diblokir karena melanggar peraturan perundang-undangan di Indonesia." />
  <meta name="keywords"
    content="Internet Positif, Trust+, Komdigi, blokir situs, konten negatif, pemblokiran, UU ITE, Indonesia, keamanan internet, filter konten, konten terlarang, Trust Positif" />
  <meta name="author" content="Kementerian Komunikasi dan Digital Republik Indonesia" />
  <meta name="language" content="id" />
  <meta name="geo.country" content="id" />
  <meta name="geo.region" content="id_ID" />
  <meta name="geo.placename" content="Indonesia" />
  <meta name="robots" content="index,follow" />
  <meta name="googlebot" content="index,follow" />
  <meta name="google" content="notranslate" />
  <meta name="rating" content="general" />
  <meta name="revisit-after" content="7 days" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="mobile-web-app-capable" content="yes" />
  <meta name="apple-mobile-web-app-capable" content="yes" />
  <meta name="apple-mobile-web-app-status-bar-style" content="default" />
  <meta name="theme-color" content="#d93025" />
  <meta property="og:title" content="Internet Positif - Akses Dibatasi | Komdigi Trust+ Filtering System" />
  <meta property="og:description"
    content="Situs ini tidak dapat diakses karena termasuk dalam kategori yang dilarang berdasarkan peraturan di Indonesia." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://trustpositif.komdigi.go.id/blocked" />
  <meta property="og:image" content="https://trustpositif.komdigi.go.id/og-image.jpg" />
  <meta property="og:locale" content="id_ID" />
  <meta property="og:site_name" content="Internet Positif" />
  <meta name="twitter:card" content="summary" />
  <meta name="twitter:title" content="Internet Positif - Akses Dibatasi" />
  <meta name="twitter:description"
    content="Situs ini tidak dapat diakses karena termasuk dalam kategori yang dilarang berdasarkan peraturan di Indonesia." />
  <meta name="twitter:image" content="https://trustpositif.komdigi.go.id/twitter-image.jpg" />
  <link rel="canonical" href="https://trustpositif.komdigi.go.id" />
  
  <title>Internet Positif - Akses Dibatasi | Komdigi Trust+ Filtering System</title>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  {@html `<script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "WebPage",
      "name": "Internet Positif - Akses Dibatasi",
      "description": "Halaman blokir Internet Positif dari Kementerian Komunikasi dan Digital RI",
      "publisher": {
        "@type": "Organization",
        "name": "Kementerian Komunikasi dan Digital RI",
        "url": "https://www.komdigi.go.id",
        "logo": "https://www.komdigi.go.id/logo.png"
      }
    }
    </script>`}
</svelte:head>

<div class="page-wrapper">
  <div class="split-card">
    <aside class="brand-sidebar">
      <div class="brand-content">
        <div class="shield-container">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none"
            stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
            <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path>
            <path d="M12 8v4"></path>
            <path d="M12 16h.01"></path>
          </svg>
        </div>
        <h1>INTERNET<br>POSITIF</h1>
        <div class="divider"></div>
        <div class="subtitle">TRUST+ FILTERING SYSTEM</div>
      </div>
      
      <div class="sidebar-pattern"></div>
    </aside>

    <main class="main-content">
      <div class="content-header">
        <div class="status-badge">
          <Ban size={16} />
          <span>Akses Dibatasi</span>
        </div>
        <div class="domain-info">
          <h2>{blockedDomain}</h2>
        </div>
        <p class="alert-text">
          Situs ini tidak dapat diakses karena terindikasi mengandung konten yang melanggar peraturan perundang-undangan di Indonesia.
        </p>
      </div>

      <div class="section-label">Kategori Pelanggaran</div>
      <div class="violation-grid">
        <div class="violation-card">
          <ShieldAlert size={24} />
          <span>Pornografi</span>
        </div>
        <div class="violation-card">
          <Dices size={24} />
          <span>Perjudian</span>
        </div>
        <div class="violation-card">
          <Fish size={24} />
          <span>Phishing</span>
        </div>
        <div class="violation-card">
          <Copyright size={24} />
          <span>Hak Cipta</span>
        </div>
        <div class="violation-card">
          <Siren size={24} />
          <span>Radikalisme</span>
        </div>
        <div class="violation-card">
          <Ban size={24} />
          <span>SARA/Hoaks</span>
        </div>
      </div>

      <div class="section-label">Dasar Hukum</div>
      <div class="legal-list">
        <div class="legal-item">
          <Globe size={18} class="legal-icon" />
          <div class="legal-text">
            <strong>UU No. 19 Tahun 2016</strong>
            <p>Perubahan Atas UU No. 11 Tahun 2008 tentang Informasi dan Transaksi Elektronik</p>
            <p class="legal-desc">Pasal 27-29: Larangan atas konten melanggar kesusilaan, perjudian, pencemaran nama baik, ancaman, hoaks, ujaran kebencian dan SARA diatur secara terpisah dalam Pasal 27, 28, dan 29 UU No. 19 Tahun 2016.</p>
          </div>
        </div>
        <div class="legal-item">
          <Globe size={18} class="legal-icon" />
          <div class="legal-text">
            <strong>Peraturan Menteri Kominfo No. 5 Tahun 2020</strong>
            <p>Tentang Penyelenggara Sistem Elektronik Lingkup Privat</p>
            <p class="legal-desc">Mengatur kewajiban untuk memblokir konten negatif dan melawan hukum dalam sistem elektronik.</p>
          </div>
        </div>
      </div>

      <div class="action-area">
        <div class="time-info">
          <small>Waktu Pemblokiran:</small>
          <span>{currentDate}</span>
        </div>
        <button on:click={() => history.back()} class="back-button">
          <ChevronLeft size={18} />
          Kembali
        </button>
      </div>

      <footer class="content-footer">
        <div class="kominfo-brand">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 600" width="24" height="24">
            <path d="M256 16L32 112v160c0 142.97 134.77 260 224 295 89.23-35 224-152.03 224-295V112L256 16z" fill="#d93025" />
            <path d="M256 64L80 144v144c0 99.41 100.81 168 176 192 75.19-24 176-92.59 176-192V144L256 64z" fill="#ea4335" />
            <path d="M216 200v160" stroke="white" stroke-width="38" stroke-linecap="round" />
            <path d="M296 200H136" stroke="white" stroke-width="38" stroke-linecap="round" />
            <path d="M336 232v96" stroke="white" stroke-width="26" stroke-linecap="round" />
            <path d="M288 280h96" stroke="white" stroke-width="26" stroke-linecap="round" />
          </svg>
          <span>&copy; {currentYear} Kementerian Komunikasi dan Digital RI</span>
        </div>
        <div class="footer-links">
          <a href="https://www.komdigi.go.id" target="_blank">www.komdigi.go.id</a>
          <span class="dot">•</span>
          <a href="https://trustpositif.komdigi.go.id" target="_blank">Internet Positif</a>
          <span class="dot">•</span>
          <a href="https://aduankonten.id" target="_blank" class="report">Aduan Konten</a>
        </div>
      </footer>
    </main>
  </div>
</div>

<style>
  :root {
    --brand-red: #d93025;
    --brand-dark-red: #b71c1c;
    --text-main: #111827;
    --text-muted: #4b5563;
    --bg-page: #f3f4f6;
    --surface: #ffffff;
    --border: #e5e7eb;
    
    --badge-bg: #fee2e2;
    --badge-text: #991b1b;
    --surface-muted: #f9fafb;
    --surface-hover: #ffffff;
    --button-bg: #111827;
    --button-text: #ffffff;
    --button-hover-bg: #000000;
    --dot-color: #9ca3af;
  }

  @media (prefers-color-scheme: dark) {
    :root {
      --brand-red: #ef4444;
      --text-main: #ededed;
      --text-muted: #d4d4d8;
      --bg-page: #000000;
      --surface: #0a0a0a;
      --border: #262626;
      
      --badge-bg: #450a0a;
      --badge-text: #fca5a5;
      --surface-muted: #171717;
      --surface-hover: #262626;
      --button-bg: #ef4444;
      --button-text: #ffffff;
      --button-hover-bg: #dc2626;
      --dot-color: #52525b;
    }
  }

  :global(*) {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  :global(body) {
    font-family: 'Plus Jakarta Sans', sans-serif;
    background-color: var(--bg-page);
    color: var(--text-main);
    line-height: 1.5;
  }

  .page-wrapper {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
  }

  .split-card {
    display: flex;
    flex-direction: column;
    background: var(--surface);
    width: 100%;
    max-width: 1100px;
    border-radius: 24px;
    overflow: hidden;
    box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.15);
  }

  /* Sidebar (Mobile: Top Header) */
  .brand-sidebar {
    background: linear-gradient(135deg, var(--brand-red) 0%, var(--brand-dark-red) 100%);
    color: white;
    /* Compact padding for mobile */
    padding: 24px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    position: relative;
    overflow: hidden;
    transition: all 0.3s ease;
  }

  .brand-sidebar::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    background-image: radial-gradient(circle at 20% 20%, rgba(255,255,255,0.1) 0%, transparent 20%),
                      radial-gradient(circle at 80% 80%, rgba(255,255,255,0.1) 0%, transparent 20%);
    pointer-events: none;
  }

  /* Compact Shield for Mobile */
  .shield-container {
    margin-bottom: 12px;
    filter: drop-shadow(0 4px 6px rgba(0,0,0,0.2));
  }

  .shield-container :global(svg) {
    width: 48px;
    height: 48px;
    transition: all 0.3s ease;
  }

  /* Compact H1 for Mobile */
  .brand-sidebar h1 {
    font-size: 24px;
    font-weight: 800;
    line-height: 1.1;
    letter-spacing: -0.02em;
    margin-bottom: 12px;
  }

  .divider {
    width: 30px;
    height: 3px;
    background: rgba(255,255,255,0.3);
    border-radius: 2px;
    margin-bottom: 12px;
  }

  .subtitle {
    font-size: 10px;
    font-weight: 600;
    letter-spacing: 0.2em;
    opacity: 0.9;
  }

  /* Main Content */
  .main-content {
    padding: 30px;
    flex: 1;
    display: flex;
    flex-direction: column;
  }

  .content-header {
    margin-bottom: 30px;
    text-align: center;
  }

  .status-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: var(--badge-bg);
    color: var(--badge-text);
    padding: 6px 12px;
    border-radius: 100px;
    font-size: 13px;
    font-weight: 600;
    margin-bottom: 16px;
  }

  .domain-info h2 {
    font-size: 24px;
    font-weight: 700;
    color: var(--text-main);
    margin-bottom: 12px;
    word-break: break-all;
  }

  .alert-text {
    color: var(--text-muted);
    font-size: 15px;
    max-width: 600px;
    margin: 0 auto;
  }

  .section-label {
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    color: var(--text-muted);
    font-weight: 600;
    margin-bottom: 16px;
    border-bottom: 1px solid var(--border);
    padding-bottom: 8px;
  }

  /* Violation Grid */
  .violation-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
    margin-bottom: 30px;
  }

  .violation-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 16px;
    background: var(--surface-muted);
    border-radius: 12px;
    border: 1px solid transparent;
    transition: all 0.2s;
    text-align: center;
    gap: 8px;
  }

  .violation-card:hover {
    background: var(--surface-hover);
    border-color: var(--border);
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    transform: translateY(-2px);
  }

  .violation-card :global(svg) {
    color: var(--brand-red);
  }

  .violation-card span {
    font-size: 13px;
    font-weight: 500;
    color: var(--text-main);
  }

  /* Legal List */
  .legal-list {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 30px;
  }

  .legal-item {
    display: flex;
    gap: 12px;
    align-items: flex-start;
    padding: 12px;
    background: var(--surface-muted);
    border-radius: 12px;
  }

  .legal-item :global(.legal-icon) {
    color: var(--brand-red);
    flex-shrink: 0;
    margin-top: 2px;
  }

  .legal-text strong {
    display: block;
    font-size: 14px;
    margin-bottom: 2px;
    color: var(--text-main);
  }

  .legal-text p {
    font-size: 13px;
    color: var(--text-muted);
    margin: 0;
  }

  .legal-text .legal-desc {
    margin-top: 6px;
    opacity: 0.8;
    line-height: 1.5;
  }

  /* Action Area */
  .action-area {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    margin-top: auto;
    padding-top: 20px;
    border-top: 1px solid var(--border);
  }

  .time-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 13px;
    color: var(--text-muted);
  }

  .back-button {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--button-bg);
    color: var(--button-text);
    padding: 12px 28px 12px 20px;
    border-radius: 100px;
    font-weight: 600;
    font-size: 14px;
    border: none;
    cursor: pointer;
    transition: all 0.2s;
    width: 100%;
    justify-content: center;
  }

  .back-button:hover {
    background: var(--button-hover-bg);
    transform: translateY(-1px);
  }

  /* Footer */
  .content-footer {
    margin-top: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    font-size: 12px;
    color: var(--text-muted);
    padding-top: 10px;
    text-align: center;
  }

  .kominfo-brand {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    font-weight: 600;
    text-align: center;
    line-height: 1.4;
    max-width: 320px;
    margin: 0 auto;
  }

  .footer-links {
    display: flex;
    gap: 8px 16px;
    align-items: center;
    flex-wrap: wrap;
    justify-content: center;
  }

  .footer-links a {
    color: var(--text-muted);
    text-decoration: none;
    transition: color 0.2s;
  }

  .footer-links a:hover {
    color: var(--brand-red);
  }

  .footer-links a.report {
    color: var(--brand-red);
    font-weight: 600;
  }

  .dot {
    color: var(--dot-color);
  }

  /* Desktop Layout (Split Screen) */
  @media (min-width: 768px) {
    .split-card {
      flex-direction: row;
      min-height: 650px;
    }

    .brand-sidebar {
      flex: 0 0 35%;
      min-width: 320px;
      text-align: left;
      align-items: flex-start;
      /* Original Padding for Desktop */
      padding: 60px 40px;
    }

    /* Restore Desktop Sizes */
    .brand-sidebar h1 {
      font-size: 42px;
      margin-bottom: 24px;
    }

    .shield-container {
      margin-bottom: 24px;
    }

    .shield-container :global(svg) {
      width: 80px;
      height: 80px;
    }

    .divider {
      width: 40px;
      height: 4px;
      margin-bottom: 24px;
    }

    .subtitle {
      font-size: 12px;
    }

    .main-content {
      padding: 50px;
      overflow-y: auto;
    }

    .content-header {
      text-align: left;
    }

    .alert-text {
      margin: 0;
      max-width: 100%;
    }

    .violation-grid {
      grid-template-columns: repeat(3, 1fr);
    }

    .action-area {
      flex-direction: row;
      justify-content: space-between;
    }

    .time-info {
      align-items: flex-start;
    }

    .back-button {
      width: auto;
    }

    .content-footer {
      flex-direction: row;
      justify-content: space-between;
      text-align: left;
      align-items: center;
    }

    .kominfo-brand {
      margin: 0;
      max-width: none;
      justify-content: flex-start;
      text-align: left;
    }

    .footer-links {
      justify-content: flex-end;
    }
  }
</style>