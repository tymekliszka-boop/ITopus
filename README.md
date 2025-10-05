<!doctype html>
<html lang="pl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>ITopus — Minimal Chic</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="header">
    <div class="brand">
      <div class="logo">ITopus</div>
      <div class="subtitle">Galeria zdjęć — bez zdjęć fabrycznych</div>
    </div>
    <div class="actions">
      <button class="icon-btn" id="fullscreenBtn">Pełny ekran</button>
      <button class="primary-btn" id="loginBtn">Zaloguj</button>
    </div>
  </header>

  <section class="topbar">
    <div class="search-area">
      <input id="searchInput" class="search" type="search" placeholder="Szukaj po tytule lub opisie" />
      <select id="categorySelect" class="select">
        <option value="all">Wszystkie kategorie</option>
        <option value="nature">Przyroda</option>
        <option value="people">Ludzie</option>
        <option value="architecture">Architektura</option>
        <option value="abstract">Abstrakcja</option>
      </select>
    </div>
    <div class="counter" id="photoCount">0 zdjęć</div>
  </section>

  <main class="main">
    <section class="uploader" id="dropzone">
      <div class="uploader-card">
        <div class="uploader-graphic" aria-hidden="true">
          <svg width="56" height="56" viewBox="0 0 24 24"><path fill="currentColor" d="M5 20h14v-2H5v2zm7-18l-5 6h3v6h4v-6h3l-5-6z"/></svg>
        </div>
        <div class="uploader-text">
          <div class="uploader-title">Przeciągnij i upuść zdjęcia lub</div>
          <div class="uploader-actions">
            <button id="chooseFilesBtn" class="outline-btn">Wybierz pliki</button>
            <input id="fileInput" type="file" accept="image/*" multiple hidden>
          </div>
          <div class="uploader-note">Możesz dodać tytuł i kategorię po przesłaniu</div>
        </div>
      </div>
    </section>

    <section class="gallery">
      <div class="gallery-header">
        <h2>Twoje zdjęcia</h2>
        <div class="gallery-tools">
          <button id="sortBtn" class="tertiary-btn">Sortuj: Najnowsze</button>
        </div>
      </div>
      <div id="grid" class="grid"></div>
    </section>
  </main>

  <div id="metaModal" class="modal" aria-hidden="true">
    <div class="modal-card">
      <button id="modalClose" class="modal-close">✕</button>
      <img id="metaPreview" alt="" class="modal-image" />
      <input id="metaTitle" placeholder="Tytuł (opcjonalnie)" />
      <select id="metaCategory">
        <option value="">Wybierz kategorię</option>
        <option value="nature">Przyroda</option>
        <option value="people">Ludzie</option>
        <option value="architecture">Architektura</option>
        <option value="abstract">Abstrakcja</option>
      </select>
      <div class="modal-actions">
        <button id="metaDelete" class="outline-btn danger">Usuń</button>
        <button id="metaSave" class="primary-btn">Zapisz</button>
      </div>
    </div>
  </div>

  <div id="toast" class="toast" aria-hidden="true"></div>

  <script src="script.js"></script>
</body>
</html>
