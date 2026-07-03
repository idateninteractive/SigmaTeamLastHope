<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Silent Fields - Red & White Exhibition</title>
    <link rel="stylesheet" href="/style.css" />
  </head>
  <body class="min-h-screen bg-white text-red-600 font-sans selection:bg-red-600 selection:text-white relative overflow-x-hidden pb-16 transition-colors duration-500">
    
    <!-- ================= INVISIBLE TITLE CODENAME TRIGGER ================= -->
    <div 
      id="codename-strip"
      class="h-1.5 bg-red-600 cursor-pointer transition-all duration-700 hover:h-6 flex items-center justify-center text-[10px] tracking-[0.4em] text-white overflow-hidden select-none font-mono"
      title="Reveal codename"
    >
      SILENT FIELDS // SPECIAL SIGMATEAM EDITION
    </div>

    <!-- MAIN APP WRAPPER -->
    <div class="max-w-6xl mx-auto px-4 py-8">
      
      <!-- ================= HEADER ================= -->
      <header id="app-header" class="flex flex-col sm:flex-row justify-between items-center gap-6 mb-10 border-b-2 border-red-600 pb-6 transition-colors duration-300">
        <div class="flex items-center gap-3">
          <div class="w-11 h-11 border-2 border-red-600 flex items-center justify-center font-mono font-bold text-xl hover:bg-red-600 hover:text-white transition-colors duration-300 cursor-pointer" onclick="location.reload()">
            Σ
          </div>
          <div>
            <div class="flex items-center gap-2">
              <span class="font-mono text-base tracking-widest uppercase font-bold">SILENT FIELDS</span>
              <span class="text-[9px] border border-red-600 px-1.5 py-0.5 font-mono uppercase tracking-wider">
                V1.4
              </span>
            </div>
            <p class="text-[11px] uppercase tracking-wider opacity-85 mt-0.5 font-mono">
              Red & White wallpaper exhibition
            </p>
          </div>
        </div>

        <div class="flex flex-wrap items-center gap-3">
          <!-- Dark & Day Toggle Button -->
          <button 
            id="theme-toggle"
            class="p-2 border-2 border-red-600 hover:bg-red-50 hover:text-red-700 transition-all duration-300 flex items-center gap-2 text-xs font-mono cursor-pointer"
          >
            <!-- Moon Icon (Dark Mode On) -->
            <svg id="theme-icon-dark" class="w-4 h-4 text-red-600 shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"></path>
            </svg>
            <!-- Sun Icon (Day Mode On) -->
            <svg id="theme-icon-light" class="w-4 h-4 text-red-500 shrink-0 hidden" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364-6.364l-.707.707M6.343 17.657l-.707.707m0-12.728l.707.707m12.728 12.728l.707.707M12 8a4 4 0 100 8 4 4 0 000-8z"></path>
            </svg>
            <span id="theme-text">DARK ON</span>
          </button>

          <!-- View Tab Toggle -->
          <div class="flex border-2 border-red-600">
            <button
              id="tab-gallery"
              class="px-4 py-1.5 text-xs font-mono tracking-widest uppercase transition-all duration-300 flex items-center gap-1.5 bg-red-600 text-white cursor-pointer"
            >
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"></path>
              </svg>
              EXHIBIT
            </button>
            <button
              id="tab-admin"
              class="px-4 py-1.5 text-xs font-mono tracking-widest uppercase transition-all duration-300 flex items-center gap-1.5 text-red-600 hover:bg-red-50 cursor-pointer"
            >
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
              </svg>
              PANEL
            </button>
          </div>

          <!-- Exit / Log out -->
          <button 
            id="admin-logout-btn"
            class="hidden items-center gap-1.5 text-xs font-mono border-2 border-red-600 bg-red-600 text-white px-3 py-1.5 hover:bg-transparent hover:text-red-600 transition-all uppercase tracking-wider cursor-pointer"
          >
            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"></path>
            </svg>
            EXIT
          </button>
        </div>
      </header>

      <!-- ================= DYNAMIC CODENAME SHOWCASE ================= -->
      <div 
        id="codename-banner" 
        class="hidden mb-10 text-center py-8 border-2 border-dashed border-red-600 bg-white"
      >
        <h2 class="text-4xl md:text-5xl font-mono font-bold uppercase tracking-[0.5em] text-red-600">
          SILENT FIELDS
        </h2>
        <p class="text-[11px] tracking-widest uppercase font-mono mt-3 text-red-600/90">
          A RED-SCALE RETROSPECTIVE SPECIFICATION // SIGMATEAM CREATIVE LABS
        </p>
      </div>

      <!-- ================= VIEW 1: PUBLIC GALLERY (EXHIBIT) ================= -->
      <main id="gallery-view" class="space-y-8">
        <!-- Category Selector & Search Bar -->
        <div id="filter-card" class="p-6 border-2 border-red-600 bg-white flex flex-col md:flex-row md:items-center justify-between gap-6 transition-colors duration-300">
          <div class="space-y-2">
            <h2 class="font-mono text-sm tracking-widest uppercase font-bold flex items-center gap-2">
              <svg class="w-4 h-4 text-red-600" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M17.657 18.657A8 8 0 016.343 7.343S7 9 9 10c0-2 .5-5 2.986-7C14 5 16.09 5.777 17.656 7.343A7.975 7.975 0 0120 13a7.975 7.975 0 01-2.343 5.657z"></path>
              </svg>
              FILTER SPECIFICATIONS
            </h2>
            <div id="category-buttons" class="flex flex-wrap gap-2">
              <!-- Rendered via JS -->
            </div>
          </div>

          <div class="w-full md:max-w-xs space-y-1.5">
            <span class="block font-mono text-[10px] tracking-widest uppercase opacity-85">
              SEARCH REPOSITORY
            </span>
            <div class="relative">
              <svg class="absolute left-3 top-2.5 w-4 h-4 opacity-70" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
              </svg>
              <input 
                id="search-input"
                type="text" 
                placeholder="ENTER TAG OR NAME..."
                class="w-full border-2 border-red-600 pl-9 pr-4 py-2 text-xs font-mono uppercase tracking-widest transition-all bg-white text-red-600 placeholder-red-600/40 focus:outline-none focus:bg-red-600 focus:text-white"
              />
            </div>
          </div>
        </div>

        <!-- Wallpapers Grid -->
        <div id="gallery-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Rendered via JS -->
        </div>

        <!-- No Results -->
        <div id="no-results" class="hidden border-2 border-dashed border-red-600 p-16 text-center bg-white">
          <svg class="w-12 h-12 mx-auto mb-4 opacity-50" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
          </svg>
          <p class="font-mono text-xs uppercase tracking-widest font-semibold">
            NO ARTWORK MATCHES THE SELECTED PROFILE.
          </p>
        </div>
      </main>

      <!-- ================= VIEW 2: ADMIN PORTAL ================= -->
      <main id="admin-view" class="hidden">
        
        <!-- ================= ADMIN LOGIN ================= -->
        <div id="admin-login-card" class="max-w-md mx-auto my-8 border-2 border-red-600 p-8 bg-white relative transition-colors duration-300">
          <!-- Decorative corners -->
          <div class="absolute top-0 left-0 w-4 h-4 border-t-2 border-l-2 border-red-600"></div>
          <div class="absolute top-0 right-0 w-4 h-4 border-t-2 border-r-2 border-red-600"></div>
          <div class="absolute bottom-0 left-0 w-4 h-4 border-b-2 border-l-2 border-red-600"></div>
          <div class="absolute bottom-0 right-0 w-4 h-4 border-b-2 border-r-2 border-red-600"></div>

          <div class="text-center mb-8">
            <svg class="w-8 h-8 mx-auto mb-3" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
            </svg>
            <h3 class="font-mono text-base tracking-widest uppercase font-bold">SIGMATEAM TERMINAL ACCESS</h3>
            <p class="text-[10px] uppercase tracking-wider opacity-80 mt-1 font-mono">
              SECURE WALLPAPER CONTROL CONSOLE (SigmaTeam/SigmaTeam)
            </p>
          </div>

          <form id="login-form" class="space-y-6">
            <div>
              <label class="block font-mono text-xs uppercase tracking-widest mb-1.5 font-bold">
                Username
              </label>
              <input 
                id="login-username"
                type="text" 
                required
                placeholder="ENTER USERNAME"
                class="w-full border-2 border-red-600 p-3 font-mono text-sm transition-all uppercase tracking-wider bg-white text-red-600 focus:outline-none focus:bg-red-600 focus:text-white"
              />
            </div>

            <div>
              <label class="block font-mono text-xs uppercase tracking-widest mb-1.5 font-bold">
                Password
              </label>
              <input 
                id="login-password"
                type="password" 
                required
                placeholder="ENTER PASSWORD"
                class="w-full border-2 border-red-600 p-3 font-mono text-sm transition-all bg-white text-red-600 focus:outline-none focus:bg-red-600 focus:text-white"
              />
            </div>

            <div id="login-error" class="hidden flex items-center gap-2 border-2 border-red-600 p-3.5 text-xs font-mono bg-red-50 text-red-600">
              <svg class="w-4 h-4 shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path>
              </svg>
              <span id="login-error-text">Access Denied: Invalid credentials.</span>
            </div>

            <button 
              type="submit"
              class="w-full py-3 bg-red-600 text-white hover:bg-white hover:text-red-600 border-2 border-red-600 font-mono font-bold tracking-widest uppercase transition-all duration-300 cursor-pointer"
            >
              SECURE SIGN IN
            </button>
          </form>
          
          <div class="mt-8 pt-4 border-t border-dashed border-red-600/40 text-center">
            <span class="text-[9px] font-mono tracking-widest opacity-75">
              AUTHORIZED PERSONNEL USE ONLY
            </span>
          </div>
        </div>

        <!-- ================= LOGGED IN CONTROL PANEL ================= -->
        <div id="admin-dashboard-content" class="hidden space-y-10">
          <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            
            <!-- File Upload Frame -->
            <div id="upload-card" class="lg:col-span-2 border-2 border-red-600 p-6 relative bg-white transition-colors duration-300">
              <h3 class="font-mono text-sm tracking-widest uppercase font-bold mb-6 flex items-center gap-2 border-b border-red-600 pb-2">
                <svg class="w-4 h-4 text-red-600" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"></path>
                </svg>
                ADD COMPOSITION
              </h3>

              <form id="upload-form" class="space-y-6">
                <!-- Dropzone -->
                <div 
                  id="dropzone"
                  class="border-2 border-dashed border-red-600/50 hover:border-red-600 hover:bg-red-50/50 p-6 text-center cursor-pointer transition-all flex flex-col items-center justify-center min-h-[170px] relative"
                >
                  <input 
                    id="upload-file-input"
                    type="file" 
                    accept="image/*"
                    class="hidden"
                  />

                  <div id="dropzone-prompt" class="space-y-2">
                    <svg class="w-10 h-10 mx-auto opacity-70" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
                    </svg>
                    <p class="font-mono text-xs uppercase tracking-wider font-semibold">
                      Drag & Drop Image Here or Click to Browse
                    </p>
                    <p class="text-[10px] font-mono opacity-70">
                      Supports Red/White theme JPEG, PNG, WEBP, or SVG formats
                    </p>
                  </div>

                  <div id="dropzone-preview" class="hidden w-full flex flex-col items-center gap-3">
                    <img 
                      id="preview-img-element"
                      src="" 
                      alt="Preview" 
                      class="max-h-24 object-contain border-2 border-red-600"
                    />
                    <p id="preview-filename" class="text-xs font-mono truncate max-w-xs"></p>
                    <button 
                      id="flush-upload-btn"
                      type="button"
                      class="text-[9px] font-mono border border-red-600 px-2 py-0.5 hover:bg-red-600 hover:text-white cursor-pointer"
                    >
                      FLUSH IMAGE
                    </button>
                  </div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                  <div>
                    <label class="block font-mono text-xs uppercase tracking-widest mb-1.5 font-bold">
                      Wallpaper Title
                    </label>
                    <input 
                      id="upload-title"
                      type="text" 
                      required
                      placeholder="E.G. SCARLET REEDS"
                      class="w-full border-2 border-red-600 p-2.5 font-mono text-xs transition-all uppercase bg-white text-red-600 placeholder-red-600/40 focus:outline-none focus:bg-red-600 focus:text-white"
                    />
                  </div>

                  <div>
                    <label class="block font-mono text-xs uppercase tracking-widest mb-1.5 font-bold">
                      Composition Category
                    </label>
                    <select 
                      id="upload-category"
                      class="w-full border-2 border-red-600 p-2.5 font-mono text-xs transition-all bg-white text-red-600 focus:outline-none focus:bg-red-600 focus:text-white"
                    >
                      <option value="Minimalist">Minimalist</option>
                      <option value="Nature">Nature</option>
                      <option value="Abstract">Abstract</option>
                      <option value="Custom">Custom</option>
                    </select>
                  </div>
                </div>

                <div id="upload-error" class="hidden flex items-center gap-2 border border-red-600 p-3 text-xs bg-red-50 text-red-600 font-mono">
                  <svg class="w-4 h-4 shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path>
                  </svg>
                  <span id="upload-error-text">Please select an image and enter a title.</span>
                </div>

                <div id="upload-success" class="hidden flex items-center gap-2 border border-red-600 p-3.5 text-xs bg-red-50 text-red-600 font-mono">
                  <svg class="w-4 h-4 shrink-0 text-red-600" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                  </svg>
                  <span>COMPOSITION REGISTERED SUCCESSFULLY IN SYSTEM STORAGE!</span>
                </div>

                <button 
                  type="submit"
                  class="w-full py-3 bg-red-600 text-white hover:bg-white hover:text-red-600 border-2 border-red-600 font-mono font-bold tracking-widest uppercase transition-all duration-300 flex items-center justify-center gap-2 cursor-pointer"
                >
                  <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M12 4v16m8-8H4"></path>
                  </svg>
                  PUBLISH COMPOSITION
                </button>
              </form>
            </div>

            <!-- Operations Status Console -->
            <div id="stats-card" class="border-2 border-red-600 p-6 flex flex-col justify-between relative bg-white transition-colors duration-300">
              <div>
                <h3 class="font-mono text-sm tracking-widest uppercase font-bold mb-6 flex items-center gap-2 border-b border-red-600 pb-2">
                  <svg class="w-4 h-4 text-red-600" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                  </svg>
                  OPERATIONS STATUS
                </h3>

                <div class="space-y-4">
                  <div class="border border-red-600/60 p-4">
                    <span class="font-mono text-[10px] uppercase tracking-widest block opacity-75">
                      TOTAL EXHIBITS
                    </span>
                    <span id="stats-count" class="text-3xl font-mono font-bold block mt-1">4</span>
                  </div>

                  <div class="border border-red-600/60 p-4">
                    <span class="font-mono text-[10px] uppercase tracking-widest block opacity-75">
                      SYSTEM PROFILE
                    </span>
                    <span id="stats-profile" class="text-xs font-mono font-bold uppercase block mt-1">
                      LIGHT FIELDS CONTRAST
                    </span>
                  </div>

                  <div class="border border-red-600/60 p-4">
                    <span class="font-mono text-[10px] uppercase tracking-widest block opacity-75">
                      GATEWAY CREDENTIALS
                    </span>
                    <span class="text-xs font-mono font-semibold block mt-1 flex items-center gap-1">
                      <svg class="w-4 h-4 text-red-600" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path>
                      </svg>
                      SIGMATEAM OPERATOR
                    </span>
                  </div>
                </div>
              </div>

              <div class="pt-6 border-t border-dashed border-red-600/40 text-center">
                <p class="text-[10px] font-mono tracking-widest opacity-70 uppercase">
                  SECURE CONSOLE // ONLINE
                </p>
              </div>
            </div>

          </div>

          <!-- Active Admin Repository Manager list -->
          <div class="space-y-6">
            <h3 class="font-mono text-sm tracking-widest uppercase font-bold border-b-2 border-red-600 pb-2 flex items-center gap-2">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-4v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
              </svg>
              FLUSH OR DELETE ARCHIVES
            </h3>

            <div id="admin-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
              <!-- Rendered via JS -->
            </div>
          </div>
        </div>
      </main>

    </div>

    <!-- ================= LIGHTBOX PREVIEW MODAL ================= -->
    <div id="lightbox-modal" class="fixed inset-0 bg-neutral-950/95 backdrop-blur-sm z-50 flex items-center justify-center p-4 hidden">
      <div id="lightbox-content-card" class="border-2 border-red-600 max-w-4xl w-full bg-white transition-colors duration-300">
        
        <div class="p-4 border-b-2 border-red-600 flex justify-between items-center text-red-600 bg-black/5">
          <span id="lightbox-title" class="font-mono text-xs uppercase tracking-widest font-bold">
            ARTWORK PREVIEW
          </span>
          <button 
            id="lightbox-close-btn"
            class="hover:bg-red-600 hover:text-white p-1.5 border border-red-600 transition-colors cursor-pointer"
          >
            <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
          </button>
        </div>

        <div class="p-4 bg-zinc-950 flex items-center justify-center border-b-2 border-red-600">
          <img 
            id="lightbox-img"
            src="" 
            alt="Preview" 
            class="max-h-[55vh] object-contain border border-red-600/40"
          />
        </div>

        <div class="p-5 grid grid-cols-1 sm:grid-cols-3 gap-4 font-mono text-[11px] text-red-600">
          <div class="border-r border-red-600/20 pr-4">
            <span class="block opacity-75 uppercase tracking-widest mb-1 text-[9px]">COMPOSITION ID</span>
            <span id="lightbox-id-val" class="font-bold block uppercase"></span>
          </div>
          <div class="border-r border-red-600/20 pr-4">
            <span class="block opacity-75 uppercase tracking-widest mb-1 text-[9px]">MAX RESOLUTION</span>
            <span class="font-bold block">3840 x 2160 (4K UHD)</span>
          </div>
          <div>
            <span class="block opacity-75 uppercase tracking-widest mb-1 text-[9px]">ARCHIVE DATE</span>
            <span id="lightbox-date-val" class="font-bold block"></span>
          </div>
        </div>

        <div class="p-4 border-t border-red-600 bg-red-600/5 flex justify-end gap-3">
          <button 
            id="lightbox-download-btn"
            class="px-4 py-2 bg-red-600 text-white hover:bg-transparent hover:text-red-600 border border-red-600 transition-all font-mono text-xs font-bold tracking-widest uppercase flex items-center gap-2 cursor-pointer"
          >
            <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4-4m0 0L8 8m4-4v12"></path>
            </svg>
            DOWNLOAD FILE
          </button>
          <button 
            id="lightbox-dismiss-btn"
            class="px-4 py-2 border border-red-600 text-red-600 hover:bg-red-600 hover:text-white transition-all font-mono text-xs font-bold tracking-widest uppercase cursor-pointer"
          >
            DISMISS
          </button>
        </div>

      </div>
    </div>

    <!-- ================= DELETE CONFIRMATION DIALOG ================= -->
    <div id="delete-modal" class="fixed inset-0 bg-neutral-950/90 backdrop-blur-sm z-50 flex items-center justify-center p-4 hidden">
      <div class="bg-zinc-950 border-4 border-red-600 max-w-md w-full p-6 text-center text-red-500">
        <svg class="w-12 h-12 text-red-600 mx-auto mb-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-4v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
        </svg>
        <h3 class="font-mono text-base font-bold uppercase tracking-widest mb-2 text-white">
          CONFIRM ACTION
        </h3>
        <p class="font-mono text-[11px] opacity-90 mb-6 uppercase tracking-wider leading-relaxed text-red-400">
          ARE YOU ABSOLUTELY SURE YOU WANT TO DESTRUCTIVELY PURGE THIS COMPOSITION FROM THE SYSTEM REPOSITORY? THIS CANNOT BE RECOVERED.
        </p>

        <div class="flex gap-4">
          <button 
            id="confirm-delete-btn"
            class="flex-1 py-2.5 bg-red-600 text-black hover:bg-black hover:text-red-500 border-2 border-red-600 font-mono font-bold tracking-widest uppercase transition-all cursor-pointer"
          >
            CONFIRM PURGE
          </button>
          <button 
            id="cancel-delete-btn"
            class="flex-1 py-2.5 border-2 border-red-600 text-red-500 hover:bg-neutral-900 font-mono font-bold tracking-widest uppercase transition-all cursor-pointer"
          >
            ABORT
          </button>
        </div>
      </div>
    </div>


    <!-- ================= VANILLA APPLICATION SCRIPT ================= -->
    <script>
      // State & Data
      const DEFAULT_WALLPAPERS = [
        {
          id: "1",
          title: "Abstract Scarlet Fluid Flow",
          url: "https://images.unsplash.com/photo-1541701494587-cb58502866ab?auto=format&fit=crop&w=1200&q=80",
          resolution: "3840 x 2160",
          category: "Abstract",
          uploadedAt: "2026-07-03"
        },
        {
          id: "2",
          title: "Minimalist Red Blossom",
          url: "https://images.unsplash.com/photo-1528459801416-a9e53bbf4e17?auto=format&fit=crop&w=1200&q=80",
          resolution: "3840 x 2160",
          category: "Nature",
          uploadedAt: "2026-07-03"
        },
        {
          id: "3",
          title: "Scarlet Modern Art Canvas",
          url: "https://images.unsplash.com/photo-1579783902614-a3fb3927b6a5?auto=format&fit=crop&w=1200&q=80",
          resolution: "3840 x 2160",
          category: "Minimalist",
          uploadedAt: "2026-07-03"
        },
        {
          id: "4",
          title: "Misty Snowy Crimson Pines",
          url: "https://images.unsplash.com/photo-1502082553048-f009c37129b9?auto=format&fit=crop&w=1200&q=80",
          resolution: "3840 x 2160",
          category: "Nature",
          uploadedAt: "2026-07-03"
        }
      ];

      let wallpapers = [];
      let currentCategory = "All";
      let searchQuery = "";
      let isDark = localStorage.getItem("silent_fields_dark") === "true";
      let isLoggedIn = sessionStorage.getItem("is_logged_in") === "true";
      let activeTab = "gallery"; // "gallery" or "admin"
      let deleteTargetId = null;
      let uploadFileBase64 = null;

      const categories = ["All", "Nature", "Abstract", "Minimalist", "Custom"];

      // DOM Elements
      const codenameStrip = document.getElementById("codename-strip");
      const codenameBanner = document.getElementById("codename-banner");
      const themeToggle = document.getElementById("theme-toggle");
      const themeIconDark = document.getElementById("theme-icon-dark");
      const themeIconLight = document.getElementById("theme-icon-light");
      const themeText = document.getElementById("theme-text");
      const tabGallery = document.getElementById("tab-gallery");
      const tabAdmin = document.getElementById("tab-admin");
      const adminLogoutBtn = document.getElementById("admin-logout-btn");
      
      const galleryView = document.getElementById("gallery-view");
      const adminView = document.getElementById("admin-view");
      const adminLoginCard = document.getElementById("admin-login-card");
      const adminDashboardContent = document.getElementById("admin-dashboard-content");

      const categoryButtonsContainer = document.getElementById("category-buttons");
      const searchInput = document.getElementById("search-input");
      const galleryGrid = document.getElementById("gallery-grid");
      const noResults = document.getElementById("no-results");

      const loginForm = document.getElementById("login-form");
      const loginUsernameInput = document.getElementById("login-username");
      const loginPasswordInput = document.getElementById("login-password");
      const loginErrorDiv = document.getElementById("login-error");

      const uploadForm = document.getElementById("upload-form");
      const dropzone = document.getElementById("dropzone");
      const uploadFileInput = document.getElementById("upload-file-input");
      const dropzonePrompt = document.getElementById("dropzone-prompt");
      const dropzonePreview = document.getElementById("dropzone-preview");
      const previewImgElement = document.getElementById("preview-img-element");
      const previewFilename = document.getElementById("preview-filename");
      const flushUploadBtn = document.getElementById("flush-upload-btn");
      const uploadTitleInput = document.getElementById("upload-title");
      const uploadCategorySelect = document.getElementById("upload-category");
      const uploadErrorDiv = document.getElementById("upload-error");
      const uploadSuccessDiv = document.getElementById("upload-success");

      const adminGrid = document.getElementById("admin-grid");
      const statsCount = document.getElementById("stats-count");
      const statsProfile = document.getElementById("stats-profile");

      const lightboxModal = document.getElementById("lightbox-modal");
      const lightboxImg = document.getElementById("lightbox-img");
      const lightboxTitle = document.getElementById("lightbox-title");
      const lightboxIdVal = document.getElementById("lightbox-id-val");
      const lightboxDateVal = document.getElementById("lightbox-date-val");
      const lightboxDownloadBtn = document.getElementById("lightbox-download-btn");
      const lightboxCloseBtn = document.getElementById("lightbox-close-btn");
      const lightboxDismissBtn = document.getElementById("lightbox-dismiss-btn");

      const deleteModal = document.getElementById("delete-modal");
      const confirmDeleteBtn = document.getElementById("confirm-delete-btn");
      const cancelDeleteBtn = document.getElementById("cancel-delete-btn");

      // Initialize
      function init() {
        // Load wallpapers
        const stored = localStorage.getItem("wallpapers_list");
        if (stored) {
          try {
            wallpapers = JSON.parse(stored);
          } catch(e) {
            wallpapers = [...DEFAULT_WALLPAPERS];
          }
        } else {
          wallpapers = [...DEFAULT_WALLPAPERS];
          localStorage.setItem("wallpapers_list", JSON.stringify(wallpapers));
        }

        // Apply theme
        applyTheme();

        // Set Tab UI
        switchTab(activeTab);

        // Render Category Buttons
        renderCategoryButtons();

        // Render Gallery Grid
        renderGallery();

        // Listen for search
        searchInput.addEventListener("input", (e) => {
          searchQuery = e.target.value;
          renderGallery();
        });
      }

      // Theme Management
      function applyTheme() {
        if (isDark) {
          document.body.classList.add("bg-black", "text-red-500");
          document.body.classList.remove("bg-white", "text-red-600");
          themeIconDark.classList.add("hidden");
          themeIconLight.classList.remove("hidden");
          themeText.textContent = "DAY ON";
          statsProfile.textContent = "DARKROOM CONTRAST";
          
          document.querySelectorAll("#filter-card, #admin-login-card, #upload-card, #stats-card, #lightbox-content-card, .wallpaper-card").forEach(el => {
            el.classList.add("bg-zinc-950", "border-red-600/80");
            el.classList.remove("bg-white", "border-red-600");
          });
        } else {
          document.body.classList.add("bg-white", "text-red-600");
          document.body.classList.remove("bg-black", "text-red-500");
          themeIconDark.classList.remove("hidden");
          themeIconLight.classList.add("hidden");
          themeText.textContent = "DARK ON";
          statsProfile.textContent = "LIGHT FIELDS CONTRAST";
          
          document.querySelectorAll("#filter-card, #admin-login-card, #upload-card, #stats-card, #lightbox-content-card, .wallpaper-card").forEach(el => {
            el.classList.remove("bg-zinc-950", "border-red-600/80");
            el.classList.add("bg-white", "border-red-600");
          });
        }
        localStorage.setItem("silent_fields_dark", isDark);
      }

      themeToggle.addEventListener("click", () => {
        isDark = !isDark;
        applyTheme();
      });

      // Codename strip
      codenameStrip.addEventListener("click", () => {
        if (codenameBanner.classList.contains("hidden")) {
          codenameBanner.classList.remove("hidden");
        } else {
          codenameBanner.classList.add("hidden");
        }
      });

      // Tab Swapping
      function switchTab(tab) {
        activeTab = tab;
        if (tab === "gallery") {
          tabGallery.className = "px-4 py-1.5 text-xs font-mono tracking-widest uppercase transition-all duration-300 flex items-center gap-1.5 bg-red-600 text-white border-2 border-red-600 cursor-pointer";
          tabAdmin.className = "px-4 py-1.5 text-xs font-mono tracking-widest uppercase transition-all duration-300 flex items-center gap-1.5 text-red-600 hover:bg-red-50 border-2 border-transparent cursor-pointer";
          galleryView.classList.remove("hidden");
          adminView.classList.add("hidden");
          adminLogoutBtn.classList.add("hidden");
        } else {
          tabAdmin.className = "px-4 py-1.5 text-xs font-mono tracking-widest uppercase transition-all duration-300 flex items-center gap-1.5 bg-red-600 text-white border-2 border-red-600 cursor-pointer";
          tabGallery.className = "px-4 py-1.5 text-xs font-mono tracking-widest uppercase transition-all duration-300 flex items-center gap-1.5 text-red-600 hover:bg-red-50 border-2 border-transparent cursor-pointer";
          galleryView.classList.add("hidden");
          adminView.classList.remove("hidden");
          
          if (isLoggedIn) {
            adminLoginCard.classList.add("hidden");
            adminDashboardContent.classList.remove("hidden");
            adminLogoutBtn.classList.remove("hidden");
            renderAdminDashboard();
          } else {
            adminLoginCard.classList.remove("hidden");
            adminDashboardContent.classList.add("hidden");
            adminLogoutBtn.classList.add("hidden");
          }
        }
      }

      tabGallery.addEventListener("click", () => switchTab("gallery"));
      tabAdmin.addEventListener("click", () => switchTab("admin"));

      // Category Rendering
      function renderCategoryButtons() {
        categoryButtonsContainer.innerHTML = "";
        categories.forEach(cat => {
          const btn = document.createElement("button");
          btn.textContent = cat;
          btn.className = `px-3 py-1 text-xs font-mono tracking-wider transition-all uppercase border-2 border-red-600 cursor-pointer ${
            currentCategory === cat 
              ? "bg-red-600 text-white" 
              : "text-red-600 hover:bg-red-600 hover:text-white"
          }`;
          btn.addEventListener("click", () => {
            currentCategory = cat;
            renderCategoryButtons();
            renderGallery();
          });
          categoryButtonsContainer.appendChild(btn);
        });
      }

      // Main Gallery Renderer
      function renderGallery() {
        galleryGrid.innerHTML = "";
        
        const filtered = wallpapers.filter(w => {
          const matchesSearch = w.title.toLowerCase().includes(searchQuery.toLowerCase()) || 
                                w.category.toLowerCase().includes(searchQuery.toLowerCase());
          const matchesCategory = currentCategory === "All" || w.category === currentCategory;
          return matchesSearch && matchesCategory;
        });

        if (filtered.length === 0) {
          noResults.classList.remove("hidden");
          galleryGrid.classList.add("hidden");
          return;
        }

        noResults.classList.add("hidden");
        galleryGrid.classList.remove("hidden");

        filtered.forEach(wallpaper => {
          const card = document.createElement("div");
          card.className = `border-2 border-red-600 overflow-hidden flex flex-col justify-between transition-all hover:scale-[1.01] wallpaper-card ${
            isDark ? "bg-zinc-950 border-red-600/80" : "bg-white"
          }`;
          
          card.innerHTML = `
            <div class="aspect-video w-full overflow-hidden bg-neutral-900 relative border-b-2 border-red-600">
              <img 
                src="${wallpaper.url}" 
                alt="${wallpaper.title}"
                class="w-full h-full object-cover transition-transform duration-700 hover:scale-105"
                referrerpolicy="no-referrer"
              />
              <div class="absolute top-3 left-3 bg-red-600 text-white font-mono text-[9px] px-2 py-0.5 tracking-widest uppercase">
                ${wallpaper.category}
              </div>
              
              <!-- Hover Overlay Action Panel -->
              <div class="absolute inset-0 bg-red-950/80 transition-opacity duration-300 flex items-center justify-center opacity-0 hover:opacity-100 gap-4">
                <button class="preview-trigger bg-white text-red-600 p-3 hover:bg-red-600 hover:text-white transition-all cursor-pointer">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path>
                  </svg>
                </button>
                <button class="download-trigger bg-white text-red-600 p-3 hover:bg-red-600 hover:text-white transition-all cursor-pointer">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4-4m0 0L8 8m4-4v12"></path>
                  </svg>
                </button>
              </div>
            </div>

            <div class="p-5 flex-grow flex flex-col justify-between gap-4">
              <div>
                <div class="flex items-center gap-2">
                  <span class="font-mono text-[10px] tracking-widest opacity-80 uppercase block">${wallpaper.resolution}</span>
                  <span class="opacity-40 font-mono text-[9px]">//</span>
                  <span class="font-mono text-[10px] tracking-widest opacity-80 block">${wallpaper.uploadedAt}</span>
                </div>
                <h4 class="font-mono text-base font-bold uppercase tracking-wider mt-2.5 truncate text-red-600">${wallpaper.title}</h4>
              </div>

              <div class="pt-3.5 border-t border-dashed border-red-600/30 flex items-center justify-between">
                <button class="preview-text-trigger text-xs font-mono font-bold tracking-widest uppercase hover:underline flex items-center gap-1 cursor-pointer">
                  <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path>
                  </svg>
                  VIEW SCREEN
                </button>
                <button class="download-btn-trigger px-3 py-1 text-[11px] font-mono tracking-widest uppercase border border-red-600 hover:bg-red-600 hover:text-white transition-all cursor-pointer">
                  GET FILE
                </button>
              </div>
            </div>
          `;

          // Handlers
          const triggerPreview = () => openLightbox(wallpaper);
          const triggerDownload = () => downloadFile(wallpaper);

          card.querySelector(".preview-trigger").addEventListener("click", triggerPreview);
          card.querySelector(".preview-text-trigger").addEventListener("click", triggerPreview);
          card.querySelector(".download-trigger").addEventListener("click", triggerDownload);
          card.querySelector(".download-btn-trigger").addEventListener("click", triggerDownload);

          galleryGrid.appendChild(card);
        });
      }

      // Lightbox Actions
      function openLightbox(wallpaper) {
        lightboxImg.src = wallpaper.url;
        lightboxTitle.textContent = `ARTWORK PREVIEW // ${wallpaper.title}`;
        lightboxIdVal.textContent = wallpaper.id;
        lightboxDateVal.textContent = wallpaper.uploadedAt;
        
        lightboxDownloadBtn.onclick = () => downloadFile(wallpaper);

        lightboxModal.classList.remove("hidden");
      }

      function closeLightbox() {
        lightboxModal.classList.add("hidden");
      }

      lightboxCloseBtn.addEventListener("click", closeLightbox);
      lightboxDismissBtn.addEventListener("click", closeLightbox);

      function downloadFile(wallpaper) {
        const link = document.createElement('a');
        link.href = wallpaper.url;
        link.download = `${wallpaper.title.toLowerCase().replace(/\s+/g, '_')}.jpg`;
        link.click();
      }

      // Authentication
      loginForm.addEventListener("submit", (e) => {
        e.preventDefault();
        const user = loginUsernameInput.value.trim();
        const pass = loginPasswordInput.value.trim();

        if (user === "SigmaTeam" && pass === "SigmaTeam") {
          isLoggedIn = true;
          sessionStorage.setItem("is_logged_in", "true");
          loginUsernameInput.value = "";
          loginPasswordInput.value = "";
          loginErrorDiv.classList.add("hidden");
          switchTab("admin");
        } else {
          loginErrorDiv.classList.remove("hidden");
        }
      });

      adminLogoutBtn.addEventListener("click", () => {
        isLoggedIn = false;
        sessionStorage.removeItem("is_logged_in");
        switchTab("admin");
      });

      // Admin Dashboard Management
      function renderAdminDashboard() {
        statsCount.textContent = wallpapers.length;
        adminGrid.innerHTML = "";

        wallpapers.forEach(wallpaper => {
          const item = document.createElement("div");
          item.className = `border-2 border-red-600 ${
            isDark ? "bg-zinc-950 border-red-600/80" : "bg-white"
          } overflow-hidden flex flex-col justify-between`;

          item.innerHTML = `
            <div class="aspect-video relative border-b border-red-600/40 bg-zinc-900">
              <img 
                src="${wallpaper.url}" 
                alt="${wallpaper.title}" 
                class="w-full h-full object-cover"
                referrerpolicy="no-referrer"
              />
              <div class="absolute top-2 right-2 bg-red-600 text-white text-[9px] font-mono px-1.5 py-0.5 uppercase">
                ${wallpaper.category}
              </div>
            </div>

            <div class="p-4 flex-grow flex flex-col justify-between gap-3 text-red-600">
              <div>
                <h4 class="font-mono text-xs font-bold uppercase truncate">${wallpaper.title}</h4>
                <p class="text-[10px] font-mono opacity-80 mt-1">${wallpaper.resolution}</p>
              </div>

              <button class="delete-trigger w-full py-1.5 text-[11px] font-mono tracking-widest uppercase text-red-600 hover:bg-red-600 hover:text-white border border-red-600 transition-colors flex items-center justify-center gap-1 cursor-pointer">
                <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-4v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
                </svg>
                DELETE FILE
              </button>
            </div>
          `;

          item.querySelector(".delete-trigger").addEventListener("click", () => {
            deleteTargetId = wallpaper.id;
            deleteModal.classList.remove("hidden");
          });

          adminGrid.appendChild(item);
        });
      }

      // Deletion Logic
      confirmDeleteBtn.addEventListener("click", () => {
        if (deleteTargetId) {
          wallpapers = wallpapers.filter(w => w.id !== deleteTargetId);
          localStorage.setItem("wallpapers_list", JSON.stringify(wallpapers));
          deleteTargetId = null;
          deleteModal.classList.add("hidden");
          renderAdminDashboard();
          renderGallery();
        }
      });

      cancelDeleteBtn.addEventListener("click", () => {
        deleteTargetId = null;
        deleteModal.classList.add("hidden");
      });

      // Upload System Actions
      dropzone.addEventListener("click", () => {
        uploadFileInput.click();
      });

      // Drag and drop events
      ["dragenter", "dragover"].forEach(eventName => {
        dropzone.addEventListener(eventName, (e) => {
          e.preventDefault();
          dropzone.classList.add("bg-red-600/10", "scale-[0.99]");
        }, false);
      });

      ["dragleave", "drop"].forEach(eventName => {
        dropzone.addEventListener(eventName, (e) => {
          e.preventDefault();
          dropzone.classList.remove("bg-red-600/10", "scale-[0.99]");
        }, false);
      });

      dropzone.addEventListener("drop", (e) => {
        const dt = e.dataTransfer;
        const files = dt.files;
        if (files.length) {
          handleSelectedFile(files[0]);
        }
      });

      uploadFileInput.addEventListener("change", (e) => {
        if (e.target.files.length) {
          handleSelectedFile(e.target.files[0]);
        }
      });

      function handleSelectedFile(file) {
        if (!file.type.startsWith("image/")) {
          showUploadError("ONLY IMAGE FILES (JPG, PNG, WEBP, SVG) ARE PERMITTED.");
          return;
        }

        const reader = new FileReader();
        reader.readAsDataURL(file);
        reader.onloadend = function() {
          uploadFileBase64 = reader.result;
          previewImgElement.src = uploadFileBase64;
          previewFilename.textContent = file.name;
          
          // Auto fill title nicely
          const cleanName = file.name.split(".")[0]
            .split(/[-_]/)
            .map(word => word.charAt(0).toUpperCase() + word.slice(1))
            .join(" ");
          uploadTitleInput.value = cleanName;

          dropzonePrompt.classList.add("hidden");
          dropzonePreview.classList.remove("hidden");
          uploadErrorDiv.classList.add("hidden");
        }
      }

      flushUploadBtn.addEventListener("click", (e) => {
        e.stopPropagation();
        flushUpload();
      });

      function flushUpload() {
        uploadFileBase64 = null;
        previewImgElement.src = "";
        previewFilename.textContent = "";
        uploadFileInput.value = "";
        uploadTitleInput.value = "";
        dropzonePrompt.classList.remove("hidden");
        dropzonePreview.classList.add("hidden");
        uploadErrorDiv.classList.add("hidden");
        uploadSuccessDiv.classList.add("hidden");
      }

      function showUploadError(msg) {
        uploadErrorDiv.querySelector("span").textContent = msg;
        uploadErrorDiv.classList.remove("hidden");
        uploadSuccessDiv.classList.add("hidden");
      }

      uploadForm.addEventListener("submit", (e) => {
        e.preventDefault();
        
        if (!uploadFileBase64) {
          showUploadError("A VAULT COMPOSITION REQUIREMENT: PLEASE DROP OR SELECT A CHROMATIC FILE.");
          return;
        }

        const title = uploadTitleInput.value.trim();
        if (!title) {
          showUploadError("PLEASE SPECIFY A TITLE FOR THE DIGITAL COMPOSITION.");
          return;
        }

        const category = uploadCategorySelect.value;
        const todayStr = new Date().toISOString().split('T')[0];

        const newWallpaper = {
          id: String(Date.now()),
          title: title,
          url: uploadFileBase64,
          resolution: "3840 x 2160",
          category: category,
          uploadedAt: todayStr
        };

        wallpapers.unshift(newWallpaper);
        localStorage.setItem("wallpapers_list", JSON.stringify(wallpapers));
        
        uploadSuccessDiv.classList.remove("hidden");
        uploadErrorDiv.classList.add("hidden");

        setTimeout(() => {
          flushUpload();
          renderAdminDashboard();
          renderGallery();
        }, 1200);
      });

      // Initialize the workspace
      init();
    </script>
  </body>
</html>
