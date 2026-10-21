<!DOCTYPE html>
<html lang="es" class="dark">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Mis Apuntes</title>
  <!-- El color de la barra superior del sistema se sincroniza con el tema elegido -->
  <meta id="themeColorMeta" name="theme-color" content="#202124">
  <link rel="manifest" href="./manifest.json">
  <link rel="icon" type="image/png" sizes="192x192" href="./icon-192.png">
  <link rel="apple-touch-icon" href="./icon-192.png">
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['Roboto', 'sans-serif'],
            display: ['Google Sans', 'Roboto', 'sans-serif']
          }
        }
      }
    };

    // Aplicar el tema guardado inmediatamente antes de renderizar para evitar destellos y actualizar la barra superior del celular
    (function() {
      const savedTheme = localStorage.getItem('mis_apuntes_theme') || 'dark';
      const htmlEl = document.documentElement;
      const metaEl = document.getElementById('themeColorMeta');
      if (savedTheme === 'dark') {
        htmlEl.classList.add('dark');
        htmlEl.classList.remove('light');
        if (metaEl) metaEl.setAttribute('content', '#202124');
      } else {
        htmlEl.classList.remove('dark');
        htmlEl.classList.add('light');
        if (metaEl) metaEl.setAttribute('content', '#ffffff');
      }
    })();
  </script>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&family=Google+Sans:wght@400;500;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" rel="stylesheet">
  <style>
    body { font-family: 'Roboto', sans-serif; -webkit-tap-highlight-color: transparent; }
    h1, h2, h3, .font-display { font-family: 'Google Sans', 'Roboto', sans-serif; }
    .material-symbols-outlined { font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24; user-select: none; }
    .material-symbols-outlined.filled { font-variation-settings: 'FILL' 1, 'wght' 400, 'GRAD' 0, 'opsz' 24; }
    
    /* Vista Cuadrícula estilo Google Keep (Masonry adaptable sin recortar el botón de fijar) */
    .notes-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px;
      align-items: start;
    }
    @media (min-width: 768px) {
      .notes-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 14px;
      }
    }
    @media (min-width: 1024px) {
      .notes-grid {
        grid-template-columns: repeat(4, minmax(0, 1fr));
        gap: 16px;
      }
    }
    .notes-grid .note-card {
      min-height: 120px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      overflow: hidden;
    }

    /* Vista Rectangular (Lista vertical de 1 columna a lo ancho) */
    .notes-list {
      max-width: 640px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .notes-list .note-card {
      width: 100%;
    }

    .note-card {
      transition: box-shadow 0.2s, border-color 0.2s, background-color 0.2s, transform 0.15s;
    }
    
    /* Rich text editor placeholder & lists */
    [contenteditable]:empty:before {
      content: attr(data-placeholder);
      color: #9aa0a6;
      pointer-events: none;
      display: block;
    }
    .rich-editor ul { list-style-type: disc; padding-left: 1.5rem; margin: 0.25rem 0; }
    .rich-editor b, .rich-editor strong { font-weight: 700; }
    .rich-editor u { text-decoration: underline; }
    .inline-icon {
      font-family: 'Material Symbols Outlined';
      font-weight: normal;
      font-style: normal;
      font-size: 1.15em;
      line-height: 1;
      vertical-align: middle;
      display: inline-block;
      margin: 0 2px;
      user-select: none;
      font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
    }
    /* Colores de contorno para los iconos minimalistas */
    .icon-diamond { color: #38bdf8; }
    .icon-favorite { color: #ef4444; }
    .icon-check { color: #22c55e; }
    .icon-location_on { color: #eab308; }
  </style>
</head>
<body class="bg-white dark:bg-[#202124] text-[#202124] dark:text-[#e8eaed] min-h-screen flex flex-col transition-colors duration-200">

  <!-- Barra Superior -->
  <header class="sticky top-0 z-30 h-16 px-3 sm:px-6 flex items-center justify-between border-b border-gray-200 dark:border-[#5f6368]/40 bg-white/95 dark:bg-[#202124]/95 backdrop-blur">
    <div class="flex items-center gap-2 sm:gap-3">
      <button id="menuBtn" type="button" class="p-2.5 rounded-full hover:bg-gray-100 dark:hover:bg-[#303134] transition" title="Menú principal">
        <span class="material-symbols-outlined">menu</span>
      </button>
      <div class="flex items-center gap-2.5 cursor-pointer" onclick="switchView('notes')">
        <span id="headerTitle" class="font-display text-xl font-medium tracking-tight">Mis Apuntes</span>
      </div>
    </div>

    <!-- Buscador -->
    <div class="flex-1 max-w-xl mx-2 sm:mx-8">
      <div class="relative flex items-center bg-[#f1f3f4] dark:bg-[#303134] rounded-full px-4 py-2 focus-within:bg-white dark:focus-within:bg-[#3c4043] focus-within:shadow-md transition">
        <span class="material-symbols-outlined text-gray-500 dark:text-gray-300 mr-2 text-[20px]">search</span>
        <input id="searchInput" type="text" placeholder="Buscar tus notas" class="w-full bg-transparent focus:outline-none text-sm sm:text-base placeholder-gray-500 dark:placeholder-gray-400">
        <button id="clearSearchBtn" type="button" class="hidden p-1 rounded-full hover:bg-gray-200 dark:hover:bg-gray-600">
          <span class="material-symbols-outlined text-sm">close</span>
        </button>
      </div>
    </div>

    <!-- Acciones Derecha -->
    <div class="flex items-center gap-1 sm:gap-2">
      <button id="viewToggleBtn" type="button" class="p-2.5 rounded-full hover:bg-gray-100 dark:hover:bg-[#303134] transition" title="Cambiar entre vista de cuadrícula y lista">
        <span id="viewToggleIcon" class="material-symbols-outlined">view_agenda</span>
      </button>
      <button id="themeToggleBtn" type="button" class="p-2.5 rounded-full hover:bg-gray-100 dark:hover:bg-[#303134] transition" title="Modo oscuro / claro">
        <span id="themeToggleIcon" class="material-symbols-outlined">light_mode</span>
      </button>
    </div>
  </header>

  <!-- Menú Lateral Desplegable -->
  <div id="drawerBackdrop" class="fixed inset-0 bg-black/50 z-40 hidden opacity-0 transition-opacity duration-200"></div>
  <aside id="sidebarDrawer" class="fixed top-0 left-0 bottom-0 w-72 bg-white dark:bg-[#202124] z-50 transform -translate-x-full transition-transform duration-200 shadow-2xl flex flex-col py-3 overflow-y-auto">
    <div class="px-6 py-3 flex items-center justify-between border-b border-gray-100 dark:border-gray-800 mb-2">
      <div class="flex items-center gap-2.5">
        <span class="font-display text-lg font-medium">Mis Apuntes</span>
      </div>
      <button id="closeDrawerBtn" type="button" class="p-1.5 rounded-full hover:bg-gray-100 dark:hover:bg-[#303134]">
        <span class="material-symbols-outlined">close</span>
      </button>
    </div>

    <nav class="space-y-0.5 pr-3">
      <button data-nav="notes" type="button" class="nav-item w-full flex items-center gap-5 px-6 py-3 rounded-r-full text-sm font-medium transition">
        <span class="material-symbols-outlined">edit_note</span>
        <span>Apuntes</span>
      </button>
      <button data-nav="assemblies" type="button" class="nav-item w-full flex items-center gap-5 px-6 py-3 rounded-r-full text-sm font-medium transition">
        <span class="material-symbols-outlined">description</span>
        <span>Asambleas</span>
      </button>
      
      <div class="pt-3 pb-1 px-6 flex items-center justify-between text-xs font-medium uppercase tracking-wider text-gray-500 dark:text-gray-400">
        <span>Etiquetas</span>
        <button id="editLabelsBtn" type="button" class="hover:text-gray-800 dark:hover:text-white">Editar</button>
      </div>
      <div id="sidebarLabelsList" class="space-y-0.5"></div>

      <div class="border-t border-gray-100 dark:border-gray-800 my-2"></div>
      <button data-nav="archive" type="button" class="nav-item w-full flex items-center gap-5 px-6 py-3 rounded-r-full text-sm font-medium transition">
        <span class="material-symbols-outlined">archive</span>
        <span>Archivo</span>
      </button>
      <button data-nav="trash" type="button" class="nav-item w-full flex items-center gap-5 px-6 py-3 rounded-r-full text-sm font-medium transition">
        <span class="material-symbols-outlined">delete</span>
        <span>Papelera</span>
      </button>
    </nav>
  </aside>

  <!-- Contenido Principal -->
  <main class="flex-1 max-w-6xl w-full mx-auto px-3 sm:px-6 py-5 pb-24">

    <!-- Barra rápida para crear nuevo apunte (Al tocarla abre el editor a pantalla completa como Google Keep) -->
    <div id="composerSection" class="max-w-xl mx-auto mb-6">
      <div id="composerCollapsed" class="rounded-2xl border border-gray-300 dark:border-[#5f6368] shadow-sm px-4 py-3 flex items-center justify-between cursor-pointer bg-white dark:bg-[#303134] hover:shadow-md transition">
        <span class="text-gray-500 dark:text-gray-300 font-medium text-sm sm:text-base">Crear un apunte...</span>
        <div class="flex items-center gap-1">
          <button id="quickImageBtn" type="button" class="p-2 rounded-full hover:bg-black/5 dark:hover:bg-white/10" title="Nueva nota con imagen">
            <span class="material-symbols-outlined text-gray-600 dark:text-gray-300">image</span>
          </button>
        </div>
      </div>
      <input id="hiddenImageInput" type="file" accept="image/*" class="hidden">
    </div>

    <!-- Sección Fijadas -->
    <section id="pinnedSection" class="hidden mb-7">
      <h2 class="text-xs font-medium uppercase tracking-wider text-gray-500 dark:text-gray-400 mb-2.5 px-2">Fijados</h2>
      <div id="pinnedGrid" class="notes-grid"></div>
    </section>

    <!-- Sección Otras Notas -->
    <section id="othersSection">
      <h2 id="othersHeading" class="hidden text-xs font-medium uppercase tracking-wider text-gray-500 dark:text-gray-400 mb-2.5 px-2">Otros</h2>
      <div id="notesGrid" class="notes-grid"></div>
    </section>

    <!-- Estado Vacío -->
    <div id="emptyState" class="hidden flex-col items-center justify-center py-20 text-center text-gray-400 dark:text-gray-500">
      <span id="emptyStateIcon" class="material-symbols-outlined text-6xl mb-3">edit_note</span>
      <p id="emptyStateText" class="text-base">Los apuntes que agregues aparecerán aquí</p>
    </div>

  </main>

  <!-- Botón flotante (+) estilo Google Keep para crear apunte rápido -->
  <button id="fabNewNoteBtn" type="button" class="fixed bottom-6 right-6 z-30 w-14 h-14 rounded-2xl bg-[#303134] dark:bg-[#8ab4f8] text-white dark:text-[#202124] shadow-xl flex items-center justify-center hover:scale-105 active:scale-95 transition" title="Nuevo apunte">
    <span class="material-symbols-outlined text-3xl">add</span>
  </button>

  <!-- Cartel Flotante de Instalación Directa PWA -->
  <div id="pwaInstallBanner" class="fixed bottom-4 left-4 right-4 sm:left-auto sm:right-6 sm:w-96 z-40 hidden bg-white dark:bg-[#303134] border border-gray-200 dark:border-[#5f6368] rounded-2xl shadow-2xl p-4 transition-all duration-300">
    <div class="flex items-start gap-3">
      <img src="./icon-192.png" alt="Mis Apuntes" onerror="this.style.display='none'" class="w-11 h-11 rounded-xl object-cover flex-shrink-0">
      <div class="flex-1 min-w-0">
        <h4 class="font-display font-medium text-sm text-[#202124] dark:text-[#e8eaed]">Instalar Mis Apuntes</h4>
        <p id="pwaBannerText" class="text-xs text-gray-600 dark:text-gray-300 mt-0.5 leading-relaxed">
          Instala la aplicación para abrirla directo desde tu pantalla de inicio y usarla sin conexión.
        </p>
        <div class="flex items-center gap-2 mt-3">
          <button id="pwaInstallActionBtn" type="button" class="px-4 py-1.5 rounded-lg bg-[#8ab4f8] text-[#202124] font-medium text-xs hover:brightness-95 active:scale-95 transition shadow-sm">
            Instalar aplicación
          </button>
          <button id="pwaDismissBtn" type="button" class="px-3 py-1.5 rounded-lg text-xs font-medium text-gray-600 dark:text-gray-300 hover:bg-black/5 dark:hover:bg-white/10 transition">
            Más tarde
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Editor de Apuntes y Asambleas a PANTALLA COMPLETA (Dinámica idéntica a Google Keep) -->
  <div id="editModal" class="fixed inset-0 z-50 hidden flex-col bg-white dark:bg-[#202124] transition-colors duration-200">
    <div id="editModalCard" class="w-full h-full flex flex-col overflow-hidden bg-white dark:bg-[#202124] transition-colors duration-200">
      
      <!-- Barra Superior de Navegación y Formato Transparente -->
      <div class="flex items-center justify-between px-2 sm:px-4 py-2 border-b border-black/10 dark:border-white/10 bg-transparent text-gray-800 dark:text-gray-100 gap-1">
        <!-- Botón Atrás (Guarda y cierra como en Google Keep) -->
        <button id="modalBackBtn" type="button" class="p-2 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition flex-shrink-0" title="Guardar y volver">
          <span class="material-symbols-outlined">arrow_back</span>
        </button>

        <!-- Herramientas de Formato y Emojis Minimalistas con contorno en color -->
        <div class="flex items-center gap-0.5 sm:gap-1 overflow-x-auto py-0.5">
          <button id="btnFormatBold" type="button" onmousedown="event.preventDefault()" onclick="applyFormatModal('bold')" class="p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Negrita">
            <span class="material-symbols-outlined text-[20px]">format_bold</span>
          </button>
          <button id="btnFormatUnderline" type="button" onmousedown="event.preventDefault()" onclick="applyFormatModal('underline')" class="p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Subrayado">
            <span class="material-symbols-outlined text-[20px]">format_underlined</span>
          </button>
          <button id="btnFormatList" type="button" onmousedown="event.preventDefault()" onclick="applyFormatModal('insertUnorderedList')" class="p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Viñetas">
            <span class="material-symbols-outlined text-[20px]">format_list_bulleted</span>
          </button>
          <div class="h-4 w-px bg-black/15 dark:bg-white/15 mx-0.5"></div>
          <button type="button" onmousedown="event.preventDefault()" onclick="insertMinimalIconModal('diamond')" class="p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Insertar Diamante">
            <span class="material-symbols-outlined text-[19px] icon-diamond">diamond</span>
          </button>
          <button type="button" onmousedown="event.preventDefault()" onclick="insertMinimalIconModal('favorite')" class="p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Insertar Corazón">
            <span class="material-symbols-outlined text-[19px] icon-favorite">favorite</span>
          </button>
          <button type="button" onmousedown="event.preventDefault()" onclick="insertMinimalIconModal('check')" class="p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Insertar Check">
            <span class="material-symbols-outlined text-[19px] icon-check">check</span>
          </button>
          <button type="button" onmousedown="event.preventDefault()" onclick="insertMinimalIconModal('person')" class="p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Insertar Persona">
            <span class="material-symbols-outlined text-[19px]">person</span>
          </button>
          <button type="button" onmousedown="event.preventDefault()" onclick="insertMinimalIconModal('location_on')" class="p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Insertar Ubicación">
            <span class="material-symbols-outlined text-[19px] icon-location_on">location_on</span>
          </button>
        </div>

        <!-- Acciones derechas: Fijar y Archivar -->
        <div class="flex items-center gap-0.5 flex-shrink-0">
          <button id="modalPinBtn" type="button" class="p-2 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Fijar apunte">
            <span id="modalPinIcon" class="material-symbols-outlined">push_pin</span>
          </button>
          <button id="modalArchiveBtn" type="button" class="p-2 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition" title="Archivar">
            <span class="material-symbols-outlined">archive</span>
          </button>
        </div>
      </div>

      <!-- Cuerpo Scrollable a Pantalla Completa -->
      <div class="flex-1 overflow-y-auto px-4 sm:px-8 py-4 max-w-4xl w-full mx-auto space-y-3">
        <div id="modalImageWrap" class="hidden relative rounded-xl overflow-hidden mb-3">
          <img id="modalImage" src="" class="w-full max-h-96 object-contain bg-black/5 dark:bg-white/5">
          <button id="modalRemoveImgBtn" type="button" class="absolute bottom-3 right-3 p-2 bg-black/60 text-white rounded-full hover:bg-black/80">
            <span class="material-symbols-outlined text-sm">delete</span>
          </button>
        </div>

        <input id="modalTitle" type="text" placeholder="Título" class="w-full bg-transparent font-display font-medium text-xl sm:text-2xl focus:outline-none placeholder-gray-500 dark:placeholder-gray-400">

        <!-- Cuerpo de Apunte Regular -->
        <div id="modalBody" contenteditable="true" data-placeholder="Apunte" class="rich-editor min-h-[60vh] text-base leading-relaxed focus:outline-none"></div>

        <!-- Contenedor Programa de Asamblea -->
        <div id="modalAssemblyContainer" class="hidden space-y-5 pt-2 pb-10"></div>

        <div id="modalLabelsChips" class="flex flex-wrap gap-1.5 pt-2"></div>
      </div>

      <!-- Barra Inferior del Editor a Pantalla Completa -->
      <div class="px-4 py-2.5 border-t border-black/10 dark:border-white/10 flex items-center justify-between relative bg-transparent">
        <div class="flex items-center gap-1">
          <button id="modalColorBtn" type="button" class="p-2.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10" title="Color de fondo">
            <span class="material-symbols-outlined text-[21px]">palette</span>
          </button>
          <button id="modalImgBtn" type="button" class="p-2.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10" title="Agregar imagen">
            <span class="material-symbols-outlined text-[21px]">image</span>
          </button>
          <button id="modalLabelBtn" type="button" class="p-2.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10" title="Etiquetas">
            <span class="material-symbols-outlined text-[21px]">label</span>
          </button>
          <button id="modalDeleteBtn" type="button" class="p-2.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10" title="Enviar a la papelera">
            <span class="material-symbols-outlined text-[21px]">delete</span>
          </button>
        </div>

        <button id="modalSaveCloseBtn" type="button" class="px-5 py-2 rounded-full font-medium text-sm bg-black/10 dark:bg-white/10 hover:bg-black/15 dark:hover:bg-white/20 transition">
          Listo
        </button>

        <!-- Menú emergente de Colores -->
        <div id="modalColorMenu" class="hidden absolute bottom-14 left-3 z-30 p-2.5 bg-white dark:bg-[#303134] rounded-2xl shadow-2xl border border-gray-200 dark:border-gray-700 flex gap-2 flex-wrap max-w-[280px]"></div>

        <!-- Menú emergente de Etiquetas -->
        <div id="modalLabelMenu" class="hidden absolute bottom-14 left-24 z-30 p-3 bg-white dark:bg-[#303134] rounded-2xl shadow-2xl border border-gray-200 dark:border-gray-700 w-56 space-y-1.5"></div>
      </div>
    </div>
  </div>

  <!-- Modal Editar Etiquetas -->
  <div id="labelsModal" class="fixed inset-0 z-50 hidden items-center justify-center bg-black/50 p-4">
    <div class="bg-white dark:bg-[#303134] w-full max-w-sm rounded-2xl shadow-2xl p-4 space-y-3 border border-gray-200 dark:border-gray-700">
      <h3 class="font-display font-medium text-base">Editar etiquetas</h3>
      <div class="flex items-center gap-2 border-b border-gray-200 dark:border-gray-600 pb-2">
        <input id="newLabelInput" type="text" placeholder="Crear nueva etiqueta" class="flex-1 bg-transparent text-sm focus:outline-none">
        <button id="addLabelBtn" type="button" class="p-1 rounded hover:bg-gray-100 dark:hover:bg-gray-700">
          <span class="material-symbols-outlined text-lg">check</span>
        </button>
      </div>
      <div id="editLabelsModalList" class="max-h-52 overflow-y-auto space-y-1"></div>
      <div class="flex justify-end pt-2 border-t border-gray-200 dark:border-gray-700">
        <button id="closeLabelsModalBtn" type="button" class="px-4 py-1.5 text-sm font-medium rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700">Listo</button>
      </div>
    </div>
  </div>

  <!-- Scripts de la Aplicación y Firebase -->
  <script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/11.0.1/firebase-app.js";
    import { getAuth, signInAnonymously, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.0.1/firebase-auth.js";
    import { getFirestore, collection, doc, setDoc, onSnapshot } from "https://www.gstatic.com/firebasejs/11.0.1/firebase-firestore.js";

    const firebaseConfig = {
      apiKey: "AIzaSyD7faGohDt5oknciF9l3c89Y1b3i1cokQM",
      authDomain: "mis-apuntes-9ca97.firebaseapp.com",
      projectId: "mis-apuntes-9ca97",
      storageBucket: "mis-apuntes-9ca97.firebasestorage.app",
      messagingSenderId: "674283641481",
      appId: "1:674283641481:web:fbbcea8d704011cc3ac458"
    };

    const KEEP_COLORS = {
      default: { light: '#ffffff', dark: '#202124', borderLight: '#e0e0e0', borderDark: '#5f6368', name: 'Predeterminado' },
      coral:   { light: '#faafa8', dark: '#77172e', borderLight: '#f28b82', borderDark: '#77172e', name: 'Coral' },
      peach:   { light: '#f39f76', dark: '#692b17', borderLight: '#fbbc04', borderDark: '#692b17', name: 'Durazno' },
      sand:    { light: '#fff8b8', dark: '#7c4a03', borderLight: '#fff475', borderDark: '#7c4a03', name: 'Arena' },
      mint:    { light: '#e2f6d3', dark: '#264d3b', borderLight: '#ccff90', borderDark: '#264d3b', name: 'Menta' },
      sage:    { light: '#b4ddd3', dark: '#0c625d', borderLight: '#a7ffeb', borderDark: '#0c625d', name: 'Salvia' },
      fog:     { light: '#d4e4ed', dark: '#256377', borderLight: '#cbf0f8', borderDark: '#256377', name: 'Niebla' },
      storm:   { light: '#aeccdc', dark: '#284255', borderLight: '#aecbfa', borderDark: '#284255', name: 'Tormenta' },
      dusk:    { light: '#d3bfdb', dark: '#472e5b', borderLight: '#d7aefb', borderDark: '#472e5b', name: 'Atardecer' },
      blossom: { light: '#f6e2dd', dark: '#6c394f', borderLight: '#fdcfe8', borderDark: '#6c394f', name: 'Flor' }
    };

    const ASSEMBLY_ID_1 = 'asamblea-confia-jehova-2026-2027';
    const ASSEMBLY_ID_2 = 'asamblea-haz-de-jehova-2026-2027';

    function createAssembly1() {
      return {
        id: ASSEMBLY_ID_1,
        type: 'assembly',
        title: '"El que confía en Jehová es feliz" (Proverbios 16:20)',
        subtitle: 'Asamblea de circuito con el superintendente de circuito | 2026-2027',
        body: '',
        color: 'sand',
        pinned: true,
        archived: false,
        trashed: false,
        labels: [],
        updatedAt: Date.now(),
        assemblyData: {
          sessions: [
            {
              name: 'MAÑANA',
              items: [
                { id: 'm1', time: '9:40', title: 'Música', isNoteable: false, notes: '' },
                { id: 'm2', time: '9:50', title: 'Canción 31 y oración', isNoteable: false, notes: '' },
                { id: 'm3', time: '10:00', title: '¿Por qué debemos confiar en Jehová con todo el corazón?', isNoteable: true, notes: '' },
                { id: 'm4', time: '10:15', title: 'Serie de discursos: Imitemos a los que confiaron en Jehová — Barac', isNoteable: true, notes: '' },
                { id: 'm5', time: '10:30', title: 'Serie de discursos: Imitemos a los que confiaron en Jehová — La mujer sunamita', isNoteable: true, notes: '' },
                { id: 'm6', time: '10:45', title: 'Serie de discursos: Imitemos a los que confiaron en Jehová — Daniel, Hananías, Misael y Azarías', isNoteable: true, notes: '' },
                { id: 'm7', time: '11:05', title: 'Canción 57 y anuncios', isNoteable: false, notes: '' },
                { id: 'm8', time: '11:15', title: 'Ayudemos a otros a confiar en el "Dios vivo y verdadero"', isNoteable: true, notes: '' },
                { id: 'm9', time: '11:35', title: 'Discurso de bautismo: "Tu Padre, que mira en secreto, te lo pagará"', isNoteable: true, notes: '' },
                { id: 'm10', time: '12:05', title: 'Canción 29', isNoteable: false, notes: '' }
              ]
            },
            {
              name: 'TARDE',
              items: [
                { id: 't1', time: '1:20', title: 'Música', isNoteable: false, notes: '' },
                { id: 't2', time: '1:30', title: 'Canción 8 y oración', isNoteable: false, notes: '' },
                { id: 't3', time: '1:35', title: 'Discurso público: ¿En quién sí se puede confiar?', isNoteable: true, notes: '' },
                { id: 't4', time: '2:05', title: 'Resumen de La Atalaya', isNoteable: true, notes: '' },
                { id: 't5', time: '2:35', title: 'Canción 135 y anuncios', isNoteable: false, notes: '' },
                { id: 't6', time: '2:45', title: 'Serie de discursos: Confíe en la sabiduría de Jehová... al educar a sus hijos', isNoteable: true, notes: '' },
                { id: 't7', time: '3:00', title: 'Serie de discursos: Confíe en la sabiduría de Jehová... al hacer planes para el futuro', isNoteable: true, notes: '' },
                { id: 't8', time: '3:15', title: 'Serie de discursos: Confíe en la sabiduría de Jehová... al enfrentar tentaciones', isNoteable: true, notes: '' },
                { id: 't9', time: '3:30', title: '"El que confía en Jehová es feliz"', isNoteable: true, notes: '' },
                { id: 't10', time: '4:00', title: 'Canción 54 y oración', isNoteable: false, notes: '' }
              ]
            },
            {
              name: 'PREGUNTAS DE REPASO',
              items: [
                { id: 'q1', time: '1', title: '¿Cómo demostramos que confiamos en Jehová con todo nuestro corazón? (Prov. 3:5, 6)', isNoteable: true, notes: '' },
                { id: 'q2', time: '2', title: '¿Cómo podemos imitar a Barac, a la mujer sunamita y a Daniel, Hananías, Misael y Azarías? (Luc. 16:10; Sal. 50:15; 119:112)', isNoteable: true, notes: '' },
                { id: 'q3', time: '3', title: '¿Qué nos ayudará a iniciar conversaciones con personas que tienen formas de pensar o antecedentes muy diferentes a los nuestros? (1 Cor. 9:19-23)', isNoteable: true, notes: '' },
                { id: 'q4', time: '4', title: '¿Por qué debemos confiar en la sabiduría de Jehová? (Prov. 3:13, 18; 16:3; 22:6; 1 Cor. 10:13)', isNoteable: true, notes: '' },
                { id: 'q5', time: '5', title: '¿Por qué debemos confiar siempre en Jehová? (Prov. 16:20)', isNoteable: true, notes: '' }
              ]
            }
          ]
        }
      };
    }

    function createAssembly2() {
      return {
        id: ASSEMBLY_ID_2,
        type: 'assembly',
        title: '"Haz de Jehová tu mayor alegría" (Salmo 37:4, nota)',
        subtitle: 'Asamblea de circuito con representante de la sucursal | 2026-2027',
        body: '',
        color: 'mint',
        pinned: true,
        archived: false,
        trashed: false,
        labels: [],
        updatedAt: Date.now(),
        assemblyData: {
          sessions: [
            {
              name: 'MAÑANA',
              items: [
                { id: 'am1', time: '9:40', title: 'Música', isNoteable: false, notes: '' },
                { id: 'am2', time: '9:50', title: 'Canción 7 y oración', isNoteable: false, notes: '' },
                { id: 'am3', time: '10:00', title: '¿Cómo podemos hacer de Jehová nuestra mayor alegría?', isNoteable: true, notes: '' },
                { id: 'am4', time: '10:15', title: '"Feliz aquel [...] al que se le perdona su pecado"', isNoteable: true, notes: '' },
                { id: 'am5', time: '10:30', title: '"¡Dichosos los que viven en tu casa!"', isNoteable: true, notes: '' },
                { id: 'am6', time: '10:55', title: 'Canción 37 y anuncios', isNoteable: false, notes: '' },
                { id: 'am7', time: '11:05', title: 'Feliz el que se refugia en Jehová', isNoteable: true, notes: '' },
                { id: 'am8', time: '11:35', title: 'Discurso de bautismo: "Tu Padre, que mira en secreto, te lo pagará"', isNoteable: true, notes: '' },
                { id: 'am9', time: '12:05', title: 'Canción 38', isNoteable: false, notes: '' }
              ]
            },
            {
              name: 'TARDE',
              items: [
                { id: 'at1', time: '1:20', title: 'Música', isNoteable: false, notes: '' },
                { id: 'at2', time: '1:30', title: 'Canción 111', isNoteable: false, notes: '' },
                { id: 'at3', time: '1:35', title: 'Experiencias', isNoteable: true, notes: '' },
                { id: 'at4', time: '1:45', title: 'Resumen de La Atalaya', isNoteable: true, notes: '' },
                { id: 'at5', time: '2:15', title: 'Serie de discursos: Tres claves para ser felices de verdad — Una vida sencilla', isNoteable: true, notes: '' },
                { id: 'at6', time: '2:30', title: 'Serie de discursos: Tres claves para ser felices de verdad — Los buenos amigos', isNoteable: true, notes: '' },
                { id: 'at7', time: '2:45', title: 'Serie de discursos: Tres claves para ser felices de verdad — Una familia unida', isNoteable: true, notes: '' },
                { id: 'at8', time: '3:00', title: 'Canción 88 y anuncios', isNoteable: false, notes: '' },
                { id: 'at9', time: '3:10', title: '"¡Feliz el pueblo que tiene por Dios a Jehová!"', isNoteable: true, notes: '' },
                { id: 'at10', time: '3:55', title: 'Canción 161 y oración', isNoteable: false, notes: '' }
              ]
            },
            {
              name: 'PREGUNTAS DE REPASO',
              items: [
                { id: 'aq1', time: '1', title: '¿Cómo podemos hacer de Jehová nuestra mayor alegría? (Sal. 37:4)', isNoteable: true, notes: '' },
                { id: 'aq2', time: '2', title: '¿Cómo podemos ser felices a pesar de nuestros errores? (Sal. 32:1, 2)', isNoteable: true, notes: '' },
                { id: 'aq3', time: '3', title: '¿Por qué debería ser el servicio a Jehová lo más importante en tu vida? (Sal. 84:4, 10)', isNoteable: true, notes: '' },
                { id: 'aq4', time: '4', title: '¿Cómo podemos ser felices a pesar de los problemas? (Sal. 34:8; 18:25)', isNoteable: true, notes: '' },
                { id: 'aq5', time: '5', title: '¿Qué podemos hacer para no dejarnos engañar por la felicidad ficticia? (1 Tim. 6:7, 8; Prov. 18:24; Sal. 127:1, 2)', isNoteable: true, notes: '' },
                { id: 'aq6', time: '6', title: '¿Cómo les ayuda Jehová a sus siervos a ser felices de verdad? (Miq. 2:12; Sant. 3:17; 1 Ped. 5:8)', isNoteable: true, notes: '' }
              ]
            }
          ]
        }
      };
    }

    let notes = [];
    let labels = ['Reuniones', 'Revisitas', 'Ideas'];
    let currentView = 'notes';
    let isListView = localStorage.getItem('mis_apuntes_view_mode') === 'list';
    let searchQuery = '';
    let activeEditorElement = null;
    let activeModalNoteId = null;
    let isCreatingNewNote = false;

    const NOTES_STORAGE_KEY = 'mis_apuntes_notes_permanent';
    const LABELS_STORAGE_KEY = 'mis_apuntes_labels_permanent';
    const THEME_STORAGE_KEY = 'mis_apuntes_theme';

    // Colorea automáticamente cualquier icono minimalista existente o nuevo
    function upgradeInlineIconsInHTML(htmlStr) {
      if (!htmlStr || typeof htmlStr !== 'string') return htmlStr;
      return htmlStr.replace(/<span([^>]*class="[^"]*inline-icon[^"]*"[^>]*)>\s*(diamond|favorite|check|person|location_on)\s*<\/span>/gi, (match, attrs, iconName) => {
        const key = iconName.trim().toLowerCase();
        return `<span class="inline-icon icon-${key}" contenteditable="false">${key}</span>`;
      });
    }

    function mergeAssemblyStructurePreservingUserNotes(existingAssembly, officialTemplate) {
      if (!existingAssembly || !existingAssembly.assemblyData) return officialTemplate;
      const merged = JSON.parse(JSON.stringify(officialTemplate));
      merged.type = 'assembly';
      merged.labels = []; // Las asambleas nunca llevan etiquetas de notas comunes
      merged.color = existingAssembly.color || officialTemplate.color;
      merged.pinned = existingAssembly.pinned !== undefined ? existingAssembly.pinned : officialTemplate.pinned;
      merged.archived = !!existingAssembly.archived;
      merged.trashed = !!existingAssembly.trashed;
      merged.updatedAt = existingAssembly.updatedAt || officialTemplate.updatedAt;

      const userNotesMap = {};
      existingAssembly.assemblyData.sessions?.forEach(sec => {
        sec.items?.forEach(it => {
          if (it.id && it.notes) userNotesMap[it.id] = upgradeInlineIconsInHTML(it.notes);
        });
      });

      merged.assemblyData.sessions.forEach(sec => {
        sec.items.forEach(it => {
          if (userNotesMap[it.id]) {
            it.notes = userNotesMap[it.id];
          }
        });
      });
      return merged;
    }

    function sanitizeNotesAndAssemblies() {
      let changed = false;
      notes.forEach(n => {
        // Garantizar que cualquier asamblea tenga su tipo correcto y no tenga etiquetas de apuntes
        if (n.id === ASSEMBLY_ID_1 || n.id === ASSEMBLY_ID_2 || n.assemblyData || n.type === 'assembly') {
          if (n.type !== 'assembly') { n.type = 'assembly'; changed = true; }
          if (Array.isArray(n.labels) && n.labels.length > 0) {
            n.labels = [];
            changed = true;
          }
        } else {
          if (!Array.isArray(n.labels)) {
            n.labels = [];
            changed = true;
          }
          if (n.body) {
            const upgraded = upgradeInlineIconsInHTML(n.body);
            if (upgraded !== n.body) {
              n.body = upgraded;
              changed = true;
            }
          }
        }
      });
      return changed;
    }

    function ensureBuiltInAssemblies() {
      const builtInTemplates = [createAssembly1(), createAssembly2()];
      let changed = false;

      builtInTemplates.forEach(template => {
        const idx = notes.findIndex(n => n.id === template.id);
        if (idx === -1) {
          notes.push(template);
          changed = true;
        } else {
          notes[idx] = mergeAssemblyStructurePreservingUserNotes(notes[idx], template);
        }
      });

      if (sanitizeNotesAndAssemblies()) {
        changed = true;
      }

      if (changed) saveToLocalStorage();
    }

    function loadFromLocalStorage() {
      const savedLabels = localStorage.getItem(LABELS_STORAGE_KEY) || localStorage.getItem('mis_apuntes_labels_v2');
      if (savedLabels) {
        try { labels = JSON.parse(savedLabels); } catch (e) {}
      }
      localStorage.setItem(LABELS_STORAGE_KEY, JSON.stringify(labels));

      const permanentNotes = localStorage.getItem(NOTES_STORAGE_KEY);
      const legacyV4 = localStorage.getItem('mis_apuntes_notes_v4');
      const legacyV3 = localStorage.getItem('mis_apuntes_notes_v3');

      const rawNotes = permanentNotes || legacyV4 || legacyV3;

      if (rawNotes) {
        try {
          notes = JSON.parse(rawNotes);
        } catch (e) {
          notes = [];
        }
      } else {
        notes = [
          {
            id: 'welcome-note-1',
            type: 'note',
            title: '¡Bienvenido a Mis Apuntes! ✨',
            body: 'Esta es tu app para tomar los mejores apuntes y notas.<br><br><ul><li>Usa la barra superior transparente para poner <b>negrita</b>, <u>subrayado</u> o viñetas.</li><li>Inserta iconos minimalistas directamente en tus textos: <span class="inline-icon icon-diamond" contenteditable="false">diamond</span> <span class="inline-icon icon-favorite" contenteditable="false">favorite</span> <span class="inline-icon icon-check" contenteditable="false">check</span> <span class="inline-icon icon-person" contenteditable="false">person</span> <span class="inline-icon icon-location_on" contenteditable="false">location_on</span></li></ul>',
            color: 'sand',
            pinned: true,
            archived: false,
            trashed: false,
            labels: ['Ideas'],
            image: null,
            updatedAt: Date.now()
          }
        ];
      }

      ensureBuiltInAssemblies();
      saveToLocalStorage();
    }

    function saveToLocalStorage() {
      localStorage.setItem(NOTES_STORAGE_KEY, JSON.stringify(notes));
      localStorage.setItem(LABELS_STORAGE_KEY, JSON.stringify(labels));
    }

    let db = null;
    let currentUser = null;
    try {
      const app = initializeApp(firebaseConfig);
      const auth = getAuth(app);
      db = getFirestore(app);
      signInAnonymously(auth).catch(console.error);
      onAuthStateChanged(auth, async (user) => {
        currentUser = user;
        if (user) {
          const notesRef = collection(db, 'users', user.uid, 'notes');
          onSnapshot(notesRef, async (snapshot) => {
            const cloudIds = new Set();
            snapshot.docs.forEach(d => {
              const cn = d.data();
              if (!cn || !cn.id) return;
              cloudIds.add(cn.id);
              const localIdx = notes.findIndex(n => n.id === cn.id);
              if (localIdx >= 0) {
                const localNote = notes[localIdx];
                if ((cn.updatedAt || 0) >= (localNote.updatedAt || 0)) {
                  notes[localIdx] = cn;
                }
              } else {
                notes.push(cn);
              }
            });

            ensureBuiltInAssemblies();
            saveToLocalStorage();
            renderApp();

            for (const localNote of notes) {
              if (!cloudIds.has(localNote.id)) {
                try {
                  await setDoc(doc(db, 'users', user.uid, 'notes', localNote.id), localNote);
                } catch (err) {
                  console.error('Error respaldando nota en la nube:', err);
                }
              }
            }
          }, (error) => {
            console.warn('Error en suscripción de Firebase:', error);
          });
        }
      });
    } catch (e) {
      console.warn('Modo local:', e);
    }

    async function persistNote(note) {
      if (note.type === 'assembly') {
        note.labels = [];
      }
      note.updatedAt = Date.now();
      const idx = notes.findIndex(n => n.id === note.id);
      if (idx >= 0) notes[idx] = note;
      else notes.unshift(note);
      saveToLocalStorage();
      renderApp();
      if (db && currentUser) {
        try {
          await setDoc(doc(db, 'users', currentUser.uid, 'notes', note.id), note);
        } catch (e) { console.error(e); }
      }
    }

    // Gestión de Tema Oscuro / Claro persistente + color de la barra de estado del celular
    function isDarkMode() {
      return document.documentElement.classList.contains('dark');
    }

    function syncThemeUI() {
      const dark = isDarkMode();
      const iconEl = document.getElementById('themeToggleIcon');
      if (iconEl) iconEl.textContent = dark ? 'light_mode' : 'dark_mode';

      const metaTheme = document.getElementById('themeColorMeta');
      if (metaTheme) {
        metaTheme.setAttribute('content', dark ? '#202124' : '#ffffff');
      }
    }

    function getColorStyles(colorKey) {
      const entry = KEEP_COLORS[colorKey] || KEEP_COLORS.default;
      const dark = isDarkMode();
      return {
        bg: dark ? entry.dark : entry.light,
        border: dark ? entry.borderDark : entry.borderLight
      };
    }

    function updateFormatButtonsState() {
      const boldBtn = document.getElementById('btnFormatBold');
      const underlineBtn = document.getElementById('btnFormatUnderline');
      const listBtn = document.getElementById('btnFormatList');
      if (!boldBtn || !underlineBtn || !listBtn) return;

      const activeClasses = ['bg-black/20', 'dark:bg-white/25', 'text-[#202124]', 'dark:text-white', 'ring-1', 'ring-black/20', 'dark:ring-white/30'];

      const setBtnActive = (btn, isActive) => {
        activeClasses.forEach(cls => btn.classList.toggle(cls, !!isActive));
      };

      try {
        setBtnActive(boldBtn, document.queryCommandState('bold'));
        setBtnActive(underlineBtn, document.queryCommandState('underline'));
        setBtnActive(listBtn, document.queryCommandState('insertUnorderedList'));
      } catch (e) {}
    }

    document.addEventListener('selectionchange', () => {
      if (!editModal.classList.contains('hidden')) {
        updateFormatButtonsState();
      }
    });

    window.applyFormatModal = function(command) {
      const target = activeEditorElement || document.getElementById('modalBody');
      if (!target) return;
      target.focus();
      document.execCommand(command, false, null);
      updateFormatButtonsState();
    };

    window.insertMinimalIconModal = function(iconName) {
      const target = activeEditorElement || document.getElementById('modalBody');
      if (!target) return;
      target.focus();

      const sel = window.getSelection();
      if (!sel) return;

      let range;
      if (sel.rangeCount > 0 && target.contains(sel.anchorNode)) {
        range = sel.getRangeAt(0);
        range.deleteContents();
      } else {
        range = document.createRange();
        range.selectNodeContents(target);
        range.collapse(false);
      }

      const iconSpan = document.createElement('span');
      iconSpan.className = `inline-icon icon-${iconName}`;
      iconSpan.setAttribute('contenteditable', 'false');
      iconSpan.textContent = iconName;

      const spaceNode = document.createTextNode('\u00A0');

      range.insertNode(spaceNode);
      range.insertNode(iconSpan);

      // Colocar el cursor inmediatamente después del espacio que sigue al icono para escribir a continuación
      const newRange = document.createRange();
      newRange.setStartAfter(spaceNode);
      newRange.collapse(true);
      sel.removeAllRanges();
      sel.addRange(newRange);

      target.dispatchEvent(new Event('input', { bubbles: true }));
      updateFormatButtonsState();
    };

    window.switchView = function(view) {
      currentView = view;
      closeDrawer();
      const titleMap = {
        notes: 'Mis Apuntes',
        assemblies: 'Asambleas',
        archive: 'Archivo',
        trash: 'Papelera'
      };
      if (view.startsWith('label:')) {
        document.getElementById('headerTitle').textContent = view.replace('label:', '');
      } else {
        document.getElementById('headerTitle').textContent = titleMap[view] || 'Mis Apuntes';
      }

      const composerSec = document.getElementById('composerSection');
      const fabBtn = document.getElementById('fabNewNoteBtn');
      if (view === 'notes' || view.startsWith('label:')) {
        composerSec.classList.remove('hidden');
        fabBtn.classList.remove('hidden');
      } else {
        composerSec.classList.add('hidden');
        fabBtn.classList.add('hidden');
      }
      renderApp();
    };

    const drawerBackdrop = document.getElementById('drawerBackdrop');
    const sidebarDrawer = document.getElementById('sidebarDrawer');

    function openDrawer() {
      drawerBackdrop.classList.remove('hidden');
      requestAnimationFrame(() => {
        drawerBackdrop.classList.remove('opacity-0');
        sidebarDrawer.classList.remove('-translate-x-full');
      });
    }

    function closeDrawer() {
      drawerBackdrop.classList.add('opacity-0');
      sidebarDrawer.classList.add('-translate-x-full');
      setTimeout(() => drawerBackdrop.classList.add('hidden'), 200);
    }

    document.getElementById('menuBtn').addEventListener('click', openDrawer);
    document.getElementById('closeDrawerBtn').addEventListener('click', closeDrawer);
    drawerBackdrop.addEventListener('click', closeDrawer);

    function applyLayoutModeUI() {
      const iconEl = document.getElementById('viewToggleIcon');
      const pinnedGrid = document.getElementById('pinnedGrid');
      const notesGrid = document.getElementById('notesGrid');

      iconEl.textContent = isListView ? 'grid_view' : 'view_agenda';
      pinnedGrid.className = isListView ? 'notes-list' : 'notes-grid';
      notesGrid.className = isListView ? 'notes-list' : 'notes-grid';
    }

    function renderApp() {
      syncThemeUI();
      applyLayoutModeUI();
      renderSidebarNav();
      renderNotesGrids();

      if (activeModalNoteId) {
        const note = notes.find(n => n.id === activeModalNoteId);
        if (note) {
          const styles = getColorStyles(note.color);
          editModalCard.style.backgroundColor = styles.bg;
        }
      }
    }

    function renderSidebarNav() {
      const labelsContainer = document.getElementById('sidebarLabelsList');
      labelsContainer.innerHTML = '';
      labels.forEach(label => {
        const btn = document.createElement('button');
        btn.type = 'button';
        btn.dataset.nav = `label:${label}`;
        btn.className = 'nav-item w-full flex items-center gap-5 px-6 py-3 rounded-r-full text-sm font-medium transition';
        btn.innerHTML = `<span class="material-symbols-outlined">label</span><span>${label}</span>`;
        btn.onclick = () => switchView(`label:${label}`);
        labelsContainer.appendChild(btn);
      });

      document.querySelectorAll('.nav-item').forEach(btn => {
        const nav = btn.dataset.nav;
        if (nav === currentView) {
          btn.classList.add('bg-[#feefc3]', 'dark:bg-[#41331c]', 'text-[#202124]', 'dark:text-[#e8eaed]');
        } else {
          btn.classList.remove('bg-[#feefc3]', 'dark:bg-[#41331c]');
        }
      });
    }

    function isAssemblyNote(note) {
      return note.type === 'assembly' || note.id === ASSEMBLY_ID_1 || note.id === ASSEMBLY_ID_2 || !!note.assemblyData;
    }

    // Creación de Tarjetas con Botón de Fijar (Pin) en TODAS las notas
    function createNoteCardElement(note) {
      const card = document.createElement('div');
      const styles = getColorStyles(note.color);
      card.className = 'note-card rounded-2xl border p-3.5 sm:p-4 cursor-pointer hover:shadow-md relative group';
      card.style.backgroundColor = styles.bg;
      card.style.borderColor = styles.border;

      const isAssembly = isAssemblyNote(note);

      // Botón de Fijar directo en cada tarjeta
      const pinBtn = document.createElement('button');
      pinBtn.type = 'button';
      pinBtn.className = `absolute top-2.5 right-2.5 z-10 p-1.5 rounded-full hover:bg-black/10 dark:hover:bg-white/10 transition ${note.pinned ? 'opacity-100' : 'opacity-70 sm:opacity-0 sm:group-hover:opacity-100'}`;
      pinBtn.title = note.pinned ? 'Desfijar apunte' : 'Fijar apunte';
      pinBtn.innerHTML = `<span class="material-symbols-outlined text-[20px] ${note.pinned ? 'filled' : ''}">push_pin</span>`;
      pinBtn.addEventListener('click', (e) => {
        e.stopPropagation();
        note.pinned = !note.pinned;
        persistNote(note);
      });

      let topContent = '';
      if (note.image) {
        topContent += `<img src="${note.image}" class="w-full ${isListView ? 'max-h-52' : 'h-28'} object-cover rounded-xl mb-2.5">`;
      }

      if (isAssembly) {
        topContent += `
          <div class="flex items-center gap-1 text-[11px] font-medium uppercase tracking-wider opacity-75 mb-1 pr-7">
            <span class="material-symbols-outlined text-sm">description</span>
            <span class="truncate">Asamblea</span>
          </div>
        `;
      }

      if (note.title) {
        topContent += `<h3 class="font-display font-medium text-sm sm:text-base mb-1.5 pr-7 line-clamp-2">${note.title}</h3>`;
      } else {
        topContent += `<div class="h-4"></div>`;
      }

      if (isAssembly && note.subtitle) {
        topContent += `<p class="text-xs opacity-80 mb-2 line-clamp-2">${note.subtitle}</p>`;
        let totalNotes = 0;
        note.assemblyData?.sessions?.forEach(s => s.items.forEach(it => {
          if (it.notes && it.notes.trim() !== '') totalNotes++;
        }));
        topContent += `<div class="text-[11px] font-medium px-2.5 py-1 rounded-md bg-black/5 dark:bg-white/10 inline-block">
          ${totalNotes} ${totalNotes === 1 ? 'apunte' : 'apuntes'}
        </div>`;
      } else if (note.body) {
        const clampClass = isListView ? 'line-clamp-8' : 'line-clamp-5';
        topContent += `<div class="rich-editor text-xs sm:text-sm leading-relaxed ${clampClass} break-words overflow-hidden">${upgradeInlineIconsInHTML(note.body)}</div>`;
      }

      let bottomContent = '';
      if (!isAssembly && Array.isArray(note.labels) && note.labels.length > 0) {
        bottomContent = `<div class="flex flex-wrap gap-1 mt-2.5 pt-1">
          ${note.labels.map(l => `<span class="text-[11px] px-2 py-0.5 rounded-full bg-black/10 dark:bg-white/10 truncate max-w-full">${l}</span>`).join('')}
        </div>`;
      }

      const contentWrap = document.createElement('div');
      contentWrap.className = 'overflow-hidden flex-1 flex flex-col justify-between';
      contentWrap.innerHTML = `<div class="overflow-hidden">${topContent}</div>${bottomContent}`;

      card.appendChild(pinBtn);
      card.appendChild(contentWrap);
      card.addEventListener('click', () => openEditModal(note.id));
      return card;
    }

    function renderNotesGrids() {
      const pinnedGrid = document.getElementById('pinnedGrid');
      const notesGrid = document.getElementById('notesGrid');
      const pinnedSection = document.getElementById('pinnedSection');
      const othersHeading = document.getElementById('othersHeading');
      const emptyState = document.getElementById('emptyState');

      pinnedGrid.innerHTML = '';
      notesGrid.innerHTML = '';

      const filtered = notes.filter(note => {
        const isAssembly = isAssemblyNote(note);

        if (searchQuery) {
          const q = searchQuery.toLowerCase();
          const inTitle = (note.title || '').toLowerCase().includes(q);
          const inBody = (note.body || '').toLowerCase().includes(q);
          return !note.trashed && (inTitle || inBody);
        }
        if (currentView === 'trash') return !!note.trashed;
        if (currentView === 'archive') return !note.trashed && !!note.archived;
        if (currentView === 'assemblies') return !note.trashed && !note.archived && isAssembly;
        if (currentView.startsWith('label:')) {
          const lbl = currentView.replace('label:', '').trim();
          // Las asambleas nunca se muestran dentro de etiquetas comunes; y las notas solo si tienen exactamente esa etiqueta
          return !note.trashed && !note.archived && !isAssembly && Array.isArray(note.labels) && note.labels.includes(lbl);
        }
        // Vista principal "Apuntes": solo notas normales (no asambleas)
        return !note.trashed && !note.archived && !isAssembly;
      });

      if (filtered.length === 0) {
        pinnedSection.classList.add('hidden');
        othersHeading.classList.add('hidden');
        emptyState.classList.remove('hidden');
        emptyState.classList.add('flex');
        return;
      }

      emptyState.classList.add('hidden');
      emptyState.classList.remove('flex');

      const pinned = filtered.filter(n => n.pinned);
      const others = filtered.filter(n => !n.pinned);

      if (pinned.length > 0) {
        pinnedSection.classList.remove('hidden');
        othersHeading.classList.toggle('hidden', others.length === 0);
        pinned.forEach(n => pinnedGrid.appendChild(createNoteCardElement(n)));
      } else {
        pinnedSection.classList.add('hidden');
        othersHeading.classList.add('hidden');
      }

      others.forEach(n => notesGrid.appendChild(createNoteCardElement(n)));
    }

    function buildColorPalette(containerId, onSelect) {
      const container = document.getElementById(containerId);
      container.innerHTML = '';
      Object.keys(KEEP_COLORS).forEach(key => {
        const btn = document.createElement('button');
        btn.type = 'button';
        const styles = getColorStyles(key);
        btn.className = 'w-8 h-8 rounded-full border transition transform hover:scale-110';
        btn.style.backgroundColor = styles.bg;
        btn.style.borderColor = styles.border;
        btn.title = KEEP_COLORS[key].name;
        btn.onclick = (e) => {
          e.stopPropagation();
          onSelect(key);
          container.classList.add('hidden');
        };
        container.appendChild(btn);
      });
    }

    // Editor a Pantalla Completa
    const editModal = document.getElementById('editModal');
    const editModalCard = document.getElementById('editModalCard');

    function startNewFullScreenNote(withImagePicker = false) {
      const defaultLabels = currentView.startsWith('label:') ? [currentView.replace('label:', '').trim()] : [];
      const draftNote = {
        id: 'note-' + Date.now(),
        type: 'note',
        title: '',
        body: '',
        color: 'default',
        pinned: false,
        archived: false,
        trashed: false,
        labels: [...defaultLabels],
        image: null,
        updatedAt: Date.now()
      };
      notes.unshift(draftNote);
      isCreatingNewNote = true;
      openEditModal(draftNote.id, true);

      if (withImagePicker) {
        document.getElementById('hiddenImageInput').click();
      }
    }

    document.getElementById('composerCollapsed').addEventListener('click', () => startNewFullScreenNote(false));
    document.getElementById('fabNewNoteBtn').addEventListener('click', () => startNewFullScreenNote(false));
    document.getElementById('quickImageBtn').addEventListener('click', (e) => {
      e.stopPropagation();
      startNewFullScreenNote(true);
    });

    function renderModalLabelsChips(note) {
      const chips = document.getElementById('modalLabelsChips');
      if (!note || isAssemblyNote(note) || !Array.isArray(note.labels)) {
        chips.innerHTML = '';
        return;
      }
      chips.innerHTML = note.labels.map(l => `<span class="text-xs px-2.5 py-1 rounded-full bg-black/10 dark:bg-white/10">${l}</span>`).join('');
    }

    function renderModalImage(note) {
      const wrap = document.getElementById('modalImageWrap');
      const img = document.getElementById('modalImage');
      if (note && note.image) {
        img.src = note.image;
        wrap.classList.remove('hidden');
      } else {
        img.src = '';
        wrap.classList.add('hidden');
      }
    }

    function openEditModal(noteId, focusBody = false) {
      const note = notes.find(n => n.id === noteId);
      if (!note) return;
      activeModalNoteId = noteId;
      activeEditorElement = null;

      const isAssembly = isAssemblyNote(note);

      const styles = getColorStyles(note.color);
      editModalCard.style.backgroundColor = styles.bg;

      // Actualizar también el color de la barra superior del teléfono mientras la nota está a pantalla completa
      const metaTheme = document.getElementById('themeColorMeta');
      if (metaTheme) metaTheme.setAttribute('content', styles.bg);

      document.getElementById('modalTitle').value = note.title || '';
      document.getElementById('modalPinIcon').classList.toggle('filled', !!note.pinned);

      // Ocultar botón de etiquetas cuando se abre un programa de asamblea para que solo pertenezca a Asambleas
      const modalLabelBtn = document.getElementById('modalLabelBtn');
      if (modalLabelBtn) {
        modalLabelBtn.classList.toggle('hidden', isAssembly);
      }
      document.getElementById('modalColorMenu').classList.add('hidden');
      document.getElementById('modalLabelMenu').classList.add('hidden');

      renderModalImage(note);
      renderModalLabelsChips(note);

      const modalBody = document.getElementById('modalBody');
      const assemblyContainer = document.getElementById('modalAssemblyContainer');

      if (isAssembly) {
        modalBody.classList.add('hidden');
        assemblyContainer.classList.remove('hidden');
        renderAssemblyProgramInsideModal(note);
      } else {
        assemblyContainer.classList.add('hidden');
        modalBody.classList.remove('hidden');
        modalBody.innerHTML = upgradeInlineIconsInHTML(note.body || '');
        activeEditorElement = modalBody;
      }

      editModal.classList.remove('hidden');
      editModal.classList.add('flex');

      if (focusBody && !isAssembly) {
        setTimeout(() => {
          modalBody.focus();
          updateFormatButtonsState();
        }, 60);
      } else {
        updateFormatButtonsState();
      }
    }

    function renderAssemblyProgramInsideModal(note) {
      const container = document.getElementById('modalAssemblyContainer');
      container.innerHTML = '';

      if (note.subtitle) {
        const sub = document.createElement('p');
        sub.className = 'text-xs font-medium opacity-75 pb-2 border-b border-black/10 dark:border-white/10';
        sub.textContent = note.subtitle;
        container.appendChild(sub);
      }

      note.assemblyData.sessions.forEach((session, sIdx) => {
        const sec = document.createElement('div');
        sec.className = 'space-y-2';
        sec.innerHTML = `<h4 class="font-display font-bold text-xs tracking-wider uppercase px-2 py-1 rounded bg-black/10 dark:bg-white/10 inline-block">${session.name}</h4>`;

        const list = document.createElement('div');
        list.className = 'space-y-1.5';

        session.items.forEach((item, iIdx) => {
          const itemBox = document.createElement('div');
          itemBox.className = 'rounded-lg border border-black/10 dark:border-white/10 overflow-hidden bg-white/40 dark:bg-black/20';

          if (!item.isNoteable) {
            itemBox.innerHTML = `
              <div class="px-3 py-2 flex items-center gap-3 text-xs sm:text-sm opacity-75">
                <span class="font-mono font-medium min-w-[42px]">${item.time}</span>
                <span>${item.title}</span>
              </div>
            `;
          } else {
            const hasNotes = item.notes && item.notes.trim() !== '';
            itemBox.innerHTML = `
              <button type="button" class="w-full px-3 py-2.5 flex items-start justify-between gap-2 text-left hover:bg-black/5 dark:hover:bg-white/5 transition">
                <div class="flex items-start gap-3 text-sm font-medium">
                  <span class="font-mono text-xs opacity-75 mt-0.5 min-w-[42px]">${item.time}</span>
                  <span>${item.title}</span>
                </div>
                <span class="material-symbols-outlined text-base opacity-60 expand-icon">${hasNotes ? 'expand_less' : 'expand_more'}</span>
              </button>
              <div class="assembly-editor-wrap ${hasNotes ? '' : 'hidden'} px-3 pb-3 pt-1 border-t border-black/5 dark:border-white/5">
                <div contenteditable="true" data-sidx="${sIdx}" data-iidx="${iIdx}" data-placeholder="Escribe tus apuntes de este tema aquí..." class="rich-editor assembly-topic-editor min-h-[70px] text-sm leading-relaxed focus:outline-none p-2 rounded bg-white/60 dark:bg-black/30">${upgradeInlineIconsInHTML(item.notes || '')}</div>
              </div>
            `;

            const headerBtn = itemBox.querySelector('button');
            const editorWrap = itemBox.querySelector('.assembly-editor-wrap');
            const editorDiv = itemBox.querySelector('.assembly-topic-editor');
            const icon = itemBox.querySelector('.expand-icon');

            headerBtn.addEventListener('click', () => {
              const hidden = editorWrap.classList.toggle('hidden');
              icon.textContent = hidden ? 'expand_more' : 'expand_less';
              if (!hidden) {
                activeEditorElement = editorDiv;
                editorDiv.focus();
              }
            });

            editorDiv.addEventListener('focus', () => {
              activeEditorElement = editorDiv;
            });

            editorDiv.addEventListener('input', () => {
              note.assemblyData.sessions[sIdx].items[iIdx].notes = editorDiv.innerHTML;
              note.updatedAt = Date.now();
              saveToLocalStorage();
            });
          }

          list.appendChild(itemBox);
        });

        sec.appendChild(list);
        container.appendChild(sec);
      });
    }

    function saveAndCloseModal() {
      if (activeModalNoteId) {
        const idx = notes.findIndex(n => n.id === activeModalNoteId);
        if (idx >= 0) {
          const note = notes[idx];
          note.title = document.getElementById('modalTitle').value.trim();
          if (!isAssemblyNote(note)) {
            note.body = document.getElementById('modalBody').innerHTML.trim();
          } else {
            note.labels = [];
          }

          const isEmptyText = (!note.body || note.body === '<br>') && !note.title && !note.image;
          if (isCreatingNewNote && !isAssemblyNote(note) && isEmptyText) {
            notes.splice(idx, 1);
            saveToLocalStorage();
            renderApp();
          } else {
            note.updatedAt = Date.now();
            persistNote(note);
          }
        }
      }
      isCreatingNewNote = false;
      activeModalNoteId = null;
      activeEditorElement = null;
      editModal.classList.add('hidden');
      editModal.classList.remove('flex');
      document.getElementById('modalColorMenu').classList.add('hidden');
      document.getElementById('modalLabelMenu').classList.add('hidden');
      syncThemeUI();
    }

    document.getElementById('modalBackBtn').addEventListener('click', saveAndCloseModal);
    document.getElementById('modalSaveCloseBtn').addEventListener('click', saveAndCloseModal);

    document.getElementById('modalPinBtn').addEventListener('click', () => {
      const note = notes.find(n => n.id === activeModalNoteId);
      if (!note) return;
      note.pinned = !note.pinned;
      document.getElementById('modalPinIcon').classList.toggle('filled', note.pinned);
    });

    document.getElementById('modalColorBtn').addEventListener('click', (e) => {
      e.stopPropagation();
      document.getElementById('modalLabelMenu').classList.add('hidden');
      buildColorPalette('modalColorMenu', (colorKey) => {
        const note = notes.find(n => n.id === activeModalNoteId);
        if (!note) return;
        note.color = colorKey;
        const styles = getColorStyles(colorKey);
        editModalCard.style.backgroundColor = styles.bg;
        const metaTheme = document.getElementById('themeColorMeta');
        if (metaTheme) metaTheme.setAttribute('content', styles.bg);
      });
      document.getElementById('modalColorMenu').classList.toggle('hidden');
    });

    function renderModalLabelCheckboxes() {
      const note = notes.find(n => n.id === activeModalNoteId);
      if (!note || isAssemblyNote(note)) return;
      if (!Array.isArray(note.labels)) note.labels = [];
      const menu = document.getElementById('modalLabelMenu');
      menu.innerHTML = '<div class="text-xs font-medium opacity-75 mb-1">Etiquetas</div>';
      labels.forEach(lbl => {
        const row = document.createElement('label');
        row.className = 'flex items-center gap-2 text-sm cursor-pointer py-1';
        const checked = note.labels.includes(lbl);
        row.innerHTML = `<input type="checkbox" ${checked ? 'checked' : ''} class="rounded"> <span>${lbl}</span>`;
        row.querySelector('input').onchange = (e) => {
          if (e.target.checked) {
            if (!note.labels.includes(lbl)) note.labels.push(lbl);
          } else {
            note.labels = note.labels.filter(x => x !== lbl);
          }
          renderModalLabelsChips(note);
        };
        menu.appendChild(row);
      });
    }

    document.getElementById('modalLabelBtn').addEventListener('click', (e) => {
      e.stopPropagation();
      document.getElementById('modalColorMenu').classList.add('hidden');
      renderModalLabelCheckboxes();
      document.getElementById('modalLabelMenu').classList.toggle('hidden');
    });

    document.getElementById('modalImgBtn').addEventListener('click', () => {
      document.getElementById('hiddenImageInput').click();
    });

    document.getElementById('modalRemoveImgBtn').addEventListener('click', () => {
      const note = notes.find(n => n.id === activeModalNoteId);
      if (!note) return;
      note.image = null;
      renderModalImage(note);
    });

    document.getElementById('modalArchiveBtn').addEventListener('click', () => {
      const note = notes.find(n => n.id === activeModalNoteId);
      if (!note) return;
      note.archived = !note.archived;
      saveAndCloseModal();
    });

    document.getElementById('modalDeleteBtn').addEventListener('click', () => {
      const note = notes.find(n => n.id === activeModalNoteId);
      if (!note) return;
      note.trashed = !note.trashed;
      saveAndCloseModal();
    });

    document.querySelectorAll('[data-nav]').forEach(btn => {
      btn.addEventListener('click', () => switchView(btn.dataset.nav));
    });

    const searchInput = document.getElementById('searchInput');
    const clearSearchBtn = document.getElementById('clearSearchBtn');
    searchInput.addEventListener('input', (e) => {
      searchQuery = e.target.value.trim();
      clearSearchBtn.classList.toggle('hidden', !searchQuery);
      renderNotesGrids();
    });
    clearSearchBtn.addEventListener('click', () => {
      searchInput.value = '';
      searchQuery = '';
      clearSearchBtn.classList.add('hidden');
      renderNotesGrids();
    });

    document.getElementById('viewToggleBtn').addEventListener('click', () => {
      isListView = !isListView;
      localStorage.setItem('mis_apuntes_view_mode', isListView ? 'list' : 'grid');
      renderApp();
    });

    // Alternar Tema Oscuro / Claro y guardarlo permanentemente en localStorage
    document.getElementById('themeToggleBtn').addEventListener('click', () => {
      const htmlEl = document.documentElement;
      const willBeDark = !htmlEl.classList.contains('dark');
      if (willBeDark) {
        htmlEl.classList.add('dark');
        htmlEl.classList.remove('light');
        localStorage.setItem(THEME_STORAGE_KEY, 'dark');
      } else {
        htmlEl.classList.remove('dark');
        htmlEl.classList.add('light');
        localStorage.setItem(THEME_STORAGE_KEY, 'light');
      }
      renderApp();
    });

    const hiddenImageInput = document.getElementById('hiddenImageInput');
    hiddenImageInput.addEventListener('change', (e) => {
      const file = e.target.files[0];
      if (!file) return;
      const reader = new FileReader();
      reader.onload = (ev) => {
        if (activeModalNoteId) {
          const note = notes.find(n => n.id === activeModalNoteId);
          if (note) {
            note.image = ev.target.result;
            renderModalImage(note);
          }
        }
      };
      reader.readAsDataURL(file);
      hiddenImageInput.value = '';
    });

    const labelsModal = document.getElementById('labelsModal');
    function renderLabelsModalList() {
      const list = document.getElementById('editLabelsModalList');
      list.innerHTML = '';
      labels.forEach((lbl, idx) => {
        const row = document.createElement('div');
        row.className = 'flex items-center justify-between py-1 px-2 rounded hover:bg-black/5 dark:hover:bg-white/5';
        row.innerHTML = `
          <span class="text-sm">${lbl}</span>
          <button type="button" class="p-1 text-gray-400 hover:text-red-500"><span class="material-symbols-outlined text-base">delete</span></button>
        `;
        row.querySelector('button').onclick = () => {
          const removedLabel = labels[idx];
          labels.splice(idx, 1);
          notes.forEach(n => {
            if (Array.isArray(n.labels)) {
              n.labels = n.labels.filter(l => l !== removedLabel);
            }
          });
          saveToLocalStorage();
          renderLabelsModalList();
          renderApp();
        };
        list.appendChild(row);
      });
    }
    document.getElementById('editLabelsBtn').addEventListener('click', () => {
      closeDrawer();
      renderLabelsModalList();
      labelsModal.classList.remove('hidden');
      labelsModal.classList.add('flex');
    });
    document.getElementById('closeLabelsModalBtn').addEventListener('click', () => {
      labelsModal.classList.add('hidden');
      labelsModal.classList.remove('flex');
    });
    document.getElementById('addLabelBtn').addEventListener('click', () => {
      const val = document.getElementById('newLabelInput').value.trim();
      if (val && !labels.includes(val)) {
        labels.push(val);
        document.getElementById('newLabelInput').value = '';
        saveToLocalStorage();
        renderLabelsModalList();
        renderApp();
      }
    });

    let deferredInstallPrompt = null;
    const pwaInstallBanner = document.getElementById('pwaInstallBanner');
    const pwaInstallActionBtn = document.getElementById('pwaInstallActionBtn');
    const pwaDismissBtn = document.getElementById('pwaDismissBtn');

    function isAppInstalled() {
      return window.matchMedia('(display-mode: standalone)').matches || window.navigator.standalone === true;
    }

    window.addEventListener('beforeinstallprompt', (e) => {
      e.preventDefault();
      deferredInstallPrompt = e;
      if (!isAppInstalled() && sessionStorage.getItem('pwa_banner_dismissed') !== '1') {
        pwaInstallBanner.classList.remove('hidden');
      }
    });

    pwaInstallActionBtn.addEventListener('click', async () => {
      if (!deferredInstallPrompt) return;
      pwaInstallBanner.classList.add('hidden');
      deferredInstallPrompt.prompt();
      const { outcome } = await deferredInstallPrompt.userChoice;
      if (outcome === 'accepted') {
        pwaInstallBanner.classList.add('hidden');
      }
      deferredInstallPrompt = null;
    });

    pwaDismissBtn.addEventListener('click', () => {
      sessionStorage.setItem('pwa_banner_dismissed', '1');
      pwaInstallBanner.classList.add('hidden');
    });

    window.addEventListener('appinstalled', () => {
      deferredInstallPrompt = null;
      pwaInstallBanner.classList.add('hidden');
    });

    if ('serviceWorker' in navigator) {
      window.addEventListener('load', () => {
        navigator.serviceWorker.register('./sw.js').then((reg) => {
          reg.update();
        }).catch((err) => console.warn('SW error:', err));
      });
    }

    // Garantizar que al iniciar nunca haya ninguna nota abierta
    editModal.classList.add('hidden');
    editModal.classList.remove('flex');
    loadFromLocalStorage();
    renderApp();
  </script>
</body>
</html>
