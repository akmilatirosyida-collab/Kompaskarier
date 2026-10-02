<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kompas Karier RIASEC: Jelajah Minat Masa Depan - SMPN 3 Cilegon</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        if (window.tailwind) {
            tailwind.config = {
                theme: {
                    extend: {
                        colors: {
                            brand: {
                                50: '#F0F7FF',
                                100: '#E0EFFF',
                                200: '#BAE0FD',
                                300: '#7CC5FB',
                                400: '#38A7F8',
                                500: '#0E8CE8',
                                600: '#0270C8',
                                700: '#0358A2',
                                800: '#074B85',
                                900: '#0C3F6F',
                                950: '#08284B',
                            }
                        }
                    }
                }
            }
        }
    </script>

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;800&family=Fredoka:wght@500;600;700&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

    <!-- Print & Global Layout Styles Nuansa Biru -->
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: 'Plus Jakarta Sans', system-ui, -apple-system, sans-serif;
            background: linear-gradient(135deg, #F0F7FF 0%, #E0F2FE 45%, #EAF2FD 100%);
            background-attachment: fixed;
            color: #1E293B;
            line-height: 1.5;
        }
        .font-heading {
            font-family: 'Fredoka', cursive, sans-serif;
        }
        .font-cert {
            font-family: 'Cinzel', serif;
        }
        .content-section {
            display: none;
        }
        .content-section.active {
            display: block !important;
            animation: fadeIn 0.25s ease-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(6px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .scale-bounce {
            transition: transform 0.15s ease, background-color 0.15s ease, box-shadow 0.15s ease;
        }
        .scale-bounce:hover {
            transform: translateY(-2px);
        }
        .scale-bounce:active {
            transform: scale(0.98);
        }
        .signature-img {
            mix-blend-mode: multiply;
            filter: contrast(140%) brightness(95%);
        }
        /* Efek transisi kartu materi bertahap */
        .materi-slide {
            display: none;
            opacity: 0;
            transform: scale(0.98);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .materi-slide.active {
            display: flex;
            opacity: 1;
            transform: scale(1);
        }
        
        /* Cetak Khusus Dokumen */
        @media print {
            .no-print { display: none !important; }
            body { 
                background: white !important; 
                padding: 0 !important; 
                margin: 0 !important;
                color: black !important;
            }
            .content-section { display: none !important; }

            body.print-mode-tes #sec-tes,
            body.print-mode-tes #tes-view-hasil { 
                display: block !important; 
            }
            body.print-mode-lkpd #sec-lkpd,
            body.print-mode-lkpd #lkpd-print-container { 
                display: block !important; 
            }
            body.print-mode-refleksi #sec-refleksi,
            body.print-mode-refleksi #refleksi-print-container { 
                display: block !important; 
            }
            body.print-mode-sertifikat #sec-sertifikat,
            body.print-mode-sertifikat #certificate-container { 
                display: block !important; 
            }
        }
    </style>
</head>
<body class="min-h-screen flex flex-col selection:bg-blue-200 selection:text-blue-900">

    <header class="no-print bg-white/95 backdrop-blur-md border-b border-blue-100 sticky top-0 z-40 shadow-xs">
        
        <!-- Serangkai Logo Resmi di Atas Bagian Tengah -->
        <div class="border-b border-blue-100/60 bg-blue-50/60 py-2.5 px-4 shadow-2xs">
            <div class="max-w-3xl mx-auto flex items-center justify-center gap-2 sm:gap-3 md:gap-4">
                <!-- Logo 1: Tutwuri Handayani - Kemendikdasmen -->
                <a href="https://imgur.com/6b0Vgbx" target="_blank" rel="noopener noreferrer" class="flex items-center justify-center transition-transform duration-200 hover:scale-105" title="Tutwuri Handayani - Kemendikdasmen">
                    <img src="https://i.imgur.com/6b0Vgbx.png" 
                         alt="Logo Kemendikdasmen" 
                         referrerpolicy="no-referrer"
                         class="h-8 sm:h-10 md:h-11 w-auto max-w-[90px] sm:max-w-[120px] object-contain" 
                         onerror="this.onerror=null; this.src='Tutwuri 3.png';">
                </a>
                
                <!-- Logo 2: Kemendikdasmen RAMAH -->
                <a href="https://imgur.com/K8WRtUn" target="_blank" rel="noopener noreferrer" class="flex items-center justify-center transition-transform duration-200 hover:scale-105" title="Kemendikdasmen RAMAH">
                    <img src="https://i.imgur.com/K8WRtUn.png" 
                         alt="Logo Kemendikdasmen RAMAH" 
                         referrerpolicy="no-referrer"
                         class="h-8 sm:h-10 md:h-11 w-auto max-w-[100px] sm:max-w-[130px] object-contain" 
                         onerror="this.onerror=null; this.src='Logo-03.png';">
                </a>
                
                <!-- Logo 3: Sobat SMP -->
                <a href="https://imgur.com/l9Dja22" target="_blank" rel="noopener noreferrer" class="flex items-center justify-center transition-transform duration-200 hover:scale-105" title="Sobat SMP">
                    <img src="https://i.imgur.com/l9Dja22.png" 
                         alt="Logo Sobat SMP" 
                         referrerpolicy="no-referrer"
                         class="h-8 sm:h-10 md:h-11 w-auto max-w-[90px] sm:max-w-[120px] object-contain" 
                         onerror="this.onerror=null; this.src='Logo Sobat SMP 2025.png';">
                </a>
                
                <!-- Logo 4: #PendidikanBermutuUntukSemua -->
                <a href="https://imgur.com/Af8rMHp" target="_blank" rel="noopener noreferrer" class="flex items-center justify-center transition-transform duration-200 hover:scale-105" title="#PendidikanBermutuUntukSemua">
                    <img src="https://i.imgur.com/Af8rMHp.png" 
                         alt="Logo Pendidikan Bermutu Untuk Semua" 
                         referrerpolicy="no-referrer"
                         class="h-8 sm:h-10 md:h-11 w-auto max-w-[110px] sm:max-w-[140px] object-contain" 
                         onerror="this.onerror=null; this.src='Logo-02.png';">
                </a>
            </div>
        </div>

        <div class="max-w-6xl mx-auto px-4 sm:px-6 py-3 flex flex-wrap items-center justify-between gap-3">
            <div class="flex items-center gap-3 cursor-pointer" onclick="navigateTo('beranda')">
                <div class="w-10 h-10 rounded-2xl bg-gradient-to-tr from-blue-600 via-indigo-600 to-sky-500 text-white flex items-center justify-center font-heading text-xl font-bold shadow-md shadow-blue-200">
                    🧭
                </div>
                <div>
                    <h1 class="font-heading text-base sm:text-lg font-bold text-slate-900 leading-tight">
                        Kompas Karier RIASEC
                    </h1>
                    <p class="text-xs text-blue-700 font-semibold">SMP Negeri 3 Cilegon • Bimbingan & Konseling</p>
                </div>
            </div>

            <!-- School Identification Badge -->
            <div class="flex items-center gap-2 bg-blue-100/90 border border-blue-300 px-3.5 py-1.5 rounded-full text-blue-950 text-xs font-bold shadow-2xs">
                <span class="w-2.5 h-2.5 rounded-full bg-blue-600 animate-pulse"></span>
                <span>BK SMPN 3 Cilegon</span>
            </div>
        </div>

        <!-- Horizontal Main Navigation Bar Nuansa Biru -->
        <nav class="border-t border-blue-100/80 bg-white/90">
            <div class="max-w-6xl mx-auto px-2 sm:px-6">
                <ul class="flex items-center gap-1.5 sm:gap-2 overflow-x-auto py-2 text-xs sm:text-sm font-bold text-slate-600">
                    <li><button onclick="navigateTo('beranda')" id="nav-beranda" class="nav-btn px-3.5 py-2 rounded-xl transition whitespace-nowrap bg-blue-600 text-white shadow-xs">🏠 Beranda</button></li>
                    <li><button onclick="navigateTo('tujuan')" id="nav-tujuan" class="nav-btn px-3.5 py-2 rounded-xl transition whitespace-nowrap hover:bg-blue-50 text-slate-600">🎯 Tujuan</button></li>
                    <li><button onclick="navigateTo('materi')" id="nav-materi" class="nav-btn px-3.5 py-2 rounded-xl transition whitespace-nowrap hover:bg-blue-50 text-slate-600">📖 Materi RIASEC</button></li>
                    <li><button onclick="navigateTo('video')" id="nav-video" class="nav-btn px-3.5 py-2 rounded-xl transition whitespace-nowrap hover:bg-blue-50 text-slate-600">🎬 Video Edukasi</button></li>
                    <li><button onclick="navigateTo('tes')" id="nav-tes" class="nav-btn px-3.5 py-2 rounded-xl transition whitespace-nowrap hover:bg-blue-50 text-slate-600">✨ Tes Kepribadian</button></li>
                    <li><button onclick="navigateTo('lkpd')" id="nav-lkpd" class="nav-btn px-3.5 py-2 rounded-xl transition whitespace-nowrap hover:bg-blue-50 text-slate-600">📝 LKPD Digital</button></li>
                    <li><button onclick="navigateTo('refleksi')" id="nav-refleksi" class="nav-btn px-3.5 py-2 rounded-xl transition whitespace-nowrap hover:bg-blue-50 text-slate-600">💬 Refleksi</button></li>
                    <li>
                        <button onclick="bukaSertifikatDenganKunci()" id="nav-sertifikat" class="nav-btn px-3.5 py-2 rounded-xl transition whitespace-nowrap bg-blue-50/70 text-slate-400 border border-blue-200/80 flex items-center gap-1.5">
                            <span id="nav-cert-icon">🔒</span>
                            <span id="nav-cert-text">Sertifikat (Terkunci)</span>
                        </button>
                    </li>
                </ul>
            </div>
        </nav>
    </header>

    <main class="flex-grow max-w-6xl w-full mx-auto px-3 sm:px-6 py-6 md:py-8">

        <section id="sec-beranda" class="content-section active space-y-8">
            
            <!-- Hero Banner: Gradien Biru Samudra & Petualangan -->
            <div class="relative overflow-hidden bg-gradient-to-br from-blue-900 via-indigo-900 to-sky-950 rounded-3xl p-6 sm:p-10 md:p-12 text-white shadow-xl border border-blue-700/40">
                <div class="absolute -top-20 -right-20 w-80 h-80 bg-sky-400/20 rounded-full blur-3xl pointer-events-none"></div>
                <div class="absolute -bottom-20 -left-20 w-80 h-80 bg-blue-500/20 rounded-full blur-3xl pointer-events-none"></div>

                <div class="relative z-10 grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                    
                    <div class="lg:col-span-8 space-y-4 text-center lg:text-left">
                        <div class="inline-flex items-center gap-2 bg-blue-500/30 border border-sky-300/40 px-4 py-1.5 rounded-full text-sky-100 text-xs font-bold shadow-2xs">
                            <span>🧭</span>
                            <span>Eksplorasi Minat & Potensi Diri • Bimbingan Klasikal</span>
                        </div>
                        <h1 class="font-heading text-2xl sm:text-4xl md:text-5xl font-bold leading-tight">
                            Kompas Karier RIASEC: <br class="hidden sm:inline">
                            <span class="text-transparent bg-clip-text bg-gradient-to-r from-sky-300 via-blue-200 to-amber-200">
                                Jelajah Minat Masa Depan
                            </span>
                        </h1>
                        <p class="text-xs sm:text-sm text-blue-100/90 max-w-2xl leading-relaxed">
                            Kenali Potensi Diri, Temukan Jalur Studi, dan Wujudkan Karier Impianmu! Pelajari 6 tipe kepribadian John L. Holland secara mendalam, simak video edukasi interaktif, ikuti tes kepribadian mandiri, isi LKPD digital, dan raih sertifikat resmi kelulusanmu.
                        </p>

                        <div class="pt-3 flex flex-wrap gap-3 justify-center lg:justify-start">
                            <button onclick="navigateTo('tujuan')" class="px-6 py-3 bg-gradient-to-r from-amber-400 to-amber-300 hover:from-amber-300 hover:to-amber-200 text-blue-950 font-bold text-xs sm:text-sm rounded-2xl shadow-lg transition scale-bounce flex items-center gap-2">
                                <span>Mulai Penjelajahan Karier</span>
                                <span>➔</span>
                            </button>
                            <button onclick="navigateTo('materi')" class="px-5 py-3 bg-white/15 hover:bg-white/25 border border-white/25 text-white font-semibold text-xs sm:text-sm rounded-2xl transition flex items-center gap-2">
                                <span>📖</span>
                                <span>Buka Materi Interaktif</span>
                            </button>
                        </div>
                    </div>

                    <!-- Profil Guru BK -->
                    <div class="lg:col-span-4 flex justify-center">
                        <div class="bg-white/15 backdrop-blur-md border border-white/25 rounded-3xl p-5 text-center max-w-[260px] w-full shadow-2xl transition hover:scale-[1.02]">
                            <div class="relative w-32 h-32 sm:w-36 sm:h-36 mx-auto mb-3">
                                <img src="IMG_0621.JPG" alt="Isnani Akmilatir Rosyida, S.Sos" 
                                     class="w-full h-full object-cover rounded-full border-2 border-sky-300 shadow-md bg-blue-950"
                                     onerror="this.outerHTML='<div class=\'w-full h-full rounded-full border-2 border-sky-300 bg-blue-800 flex flex-col items-center justify-center text-white p-2\'><span class=\'text-3xl\'>👩‍🏫</span><span class=\'text-[10px] font-bold mt-1\'>Ibu Guru BK</span></div>'">
                            </div>
                            
                            <div class="space-y-0.5">
                                <h3 class="font-heading text-sm font-bold text-white tracking-wide">
                                    Isnani Akmilatir Rosyida, S.Sos
                                </h3>
                                <p class="text-[11px] text-sky-200 font-medium">
                                    Guru Bimbingan dan Konseling
                                </p>
                                <p class="text-[11px] text-amber-300 font-semibold tracking-wide">
                                    SMP Negeri 3 Cilegon
                                </p>
                            </div>
                        </div>
                    </div>

                </div>
            </div>

            <!-- Kartu Alur Cepat -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                <div onclick="navigateTo('materi')" class="p-5 bg-white/95 backdrop-blur rounded-2xl border border-blue-100 shadow-xs hover:shadow-md transition cursor-pointer hover:border-blue-300 group scale-bounce">
                    <div class="w-11 h-11 rounded-xl bg-blue-100 text-blue-700 flex items-center justify-center mb-3 text-2xl">📖</div>
                    <h4 class="font-heading text-xs sm:text-sm font-bold text-slate-800">1. Pelajari 6 Tipe</h4>
                    <p class="text-[11px] text-slate-500 mt-0.5">Eksplorasi ciri, profesi & jurusan studi.</p>
                </div>

                <div onclick="navigateTo('video')" class="p-5 bg-white/95 backdrop-blur rounded-2xl border border-blue-100 shadow-xs hover:shadow-md transition cursor-pointer hover:border-blue-300 group scale-bounce">
                    <div class="w-11 h-11 rounded-xl bg-indigo-100 text-indigo-700 flex items-center justify-center mb-3 text-2xl">🎬</div>
                    <h4 class="font-heading text-xs sm:text-sm font-bold text-slate-800">2. Video Edukasi BK</h4>
                    <p class="text-[11px] text-slate-500 mt-0.5">Simak video animasi tipe RIASEC.</p>
                </div>

                <div onclick="navigateTo('tes')" class="p-5 bg-white/95 backdrop-blur rounded-2xl border border-blue-100 shadow-xs hover:shadow-md transition cursor-pointer hover:border-blue-300 group scale-bounce">
                    <div class="w-11 h-11 rounded-xl bg-sky-100 text-sky-700 flex items-center justify-center mb-3 text-2xl">✨</div>
                    <h4 class="font-heading text-xs sm:text-sm font-bold text-slate-800">3. Tes 36 Butir</h4>
                    <p class="text-[11px] text-slate-500 mt-0.5">Dapatkan 3 kode Holland & profesi.</p>
                </div>

                <div onclick="navigateTo('lkpd')" class="p-5 bg-white/95 backdrop-blur rounded-2xl border border-blue-100 shadow-xs hover:shadow-md transition cursor-pointer hover:border-blue-300 group scale-bounce">
                    <div class="w-11 h-11 rounded-xl bg-teal-100 text-teal-800 flex items-center justify-center mb-3 text-2xl">📝</div>
                    <h4 class="font-heading text-xs sm:text-sm font-bold text-slate-800">4. LKPD & Sertifikat</h4>
                    <p class="text-[11px] text-slate-500 mt-0.5">Susun rencana dan cetak sertifikat.</p>
                </div>
            </div>
        </section>

        <section id="sec-tujuan" class="content-section space-y-6">
            <div class="bg-white/95 backdrop-blur rounded-3xl p-6 sm:p-8 border border-blue-100 shadow-sm">
                <div class="max-w-3xl">
                    <div class="inline-flex items-center gap-1.5 bg-blue-100 text-blue-900 px-3.5 py-1 rounded-full text-xs font-bold mb-2">
                        <span>🎯</span>
                        <span>RPL Bimbingan Klasikal Bidang Karier</span>
                    </div>
                    <h2 class="font-heading text-2xl sm:text-3xl font-bold text-slate-800">Tujuan Pembelajaran & Layanan</h2>
                    <p class="text-xs sm:text-sm text-slate-600 mt-1">
                        Setelah mengikuti kegiatan bimbingan klasikal ini, peserta didik diharapkan mampu mencapai 3 capaian utama:
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-5 mt-6">
                    <!-- Kognitif C4 -->
                    <div class="bg-gradient-to-b from-blue-50 to-white p-6 rounded-2xl border border-blue-200 flex flex-col justify-between shadow-2xs">
                        <div>
                            <div class="flex items-center justify-between mb-4">
                                <span class="bg-blue-600 text-white text-[11px] font-bold px-3 py-1 rounded-lg">C4 - Menganalisis</span>
                                <span class="text-2xl">🧠</span>
                            </div>
                            <h3 class="font-heading text-lg font-bold text-slate-800 mb-2">Aspek Kognitif</h3>
                            <p class="text-xs text-slate-600 leading-relaxed">
                                Peserta didik mampu <strong>menganalisis karakteristik kepribadian dirinya</strong> berdasarkan hasil tes kepribadian Holland serta menghubungkannya dengan bidang atau profesi yang sesuai.
                            </p>
                        </div>
                        <div class="mt-4 pt-3 border-t border-blue-100 text-blue-800 text-xs font-bold flex items-center gap-1.5">
                            <span>✔</span>
                            <span>Mengenal potensi diri secara analitis</span>
                        </div>
                    </div>

                    <!-- Afektif A4 -->
                    <div class="bg-gradient-to-b from-indigo-50 to-white p-6 rounded-2xl border border-indigo-200 flex flex-col justify-between shadow-2xs">
                        <div>
                            <div class="flex items-center justify-between mb-4">
                                <span class="bg-indigo-600 text-white text-[11px] font-bold px-3 py-1 rounded-lg">A4 - Mengorganisasi</span>
                                <span class="text-2xl">🤝</span>
                            </div>
                            <h3 class="font-heading text-lg font-bold text-slate-800 mb-2">Aspek Afektif</h3>
                            <p class="text-xs text-slate-600 leading-relaxed">
                                Peserta didik mampu <strong>mengorganisasi minat, potensi, dan pilihan profesi</strong> yang sesuai dengan kepribadian dirinya sebagai bahan pertimbangan dalam merencanakan masa depan.
                            </p>
                        </div>
                        <div class="mt-4 pt-3 border-t border-indigo-100 text-indigo-800 text-xs font-bold flex items-center gap-1.5">
                            <span>✔</span>
                            <span>Menghargai keunikan diri</span>
                        </div>
                    </div>

                    <!-- Psikomotorik P4 -->
                    <div class="bg-gradient-to-b from-sky-50 to-white p-6 rounded-2xl border border-sky-200 flex flex-col justify-between shadow-2xs">
                        <div>
                            <div class="flex items-center justify-between mb-4">
                                <span class="bg-sky-600 text-white text-[11px] font-bold px-3 py-1 rounded-lg">P4 - Artikulasi</span>
                                <span class="text-2xl">✍️</span>
                            </div>
                            <h3 class="font-heading text-lg font-bold text-slate-800 mb-2">Aspek Psikomotorik</h3>
                            <p class="text-xs text-slate-600 leading-relaxed">
                                Peserta didik mampu <strong>menyusun rencana tindak lanjut sederhana</strong> berupa langkah-langkah nyata yang dapat dilakukan untuk mengembangkan diri menuju profesi impiannya.
                            </p>
                        </div>
                        <div class="mt-4 pt-3 border-t border-sky-100 text-sky-800 text-xs font-bold flex items-center gap-1.5">
                            <span>✔</span>
                            <span>Rencana nyata di LKPD digital</span>
                        </div>
                    </div>
                </div>

                <div class="mt-8 flex justify-end">
                    <button onclick="navigateTo('materi')" class="px-6 py-2.5 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs font-bold transition scale-bounce flex items-center gap-2 shadow-sm">
                        <span>Lanjut ke Materi RIASEC</span>
                        <span>➔</span>
                    </button>
                </div>
            </div>
        </section>

        <section id="sec-materi" class="content-section space-y-6">
            <div class="bg-white/95 backdrop-blur rounded-3xl p-6 sm:p-9 border border-blue-100 shadow-md">
                
                <div class="flex flex-col lg:flex-row justify-between items-start lg:items-center gap-5 border-b border-blue-100 pb-6">
                    <div>
                        <div class="inline-flex items-center gap-2 text-blue-700 text-xs font-bold uppercase tracking-wider bg-blue-100/70 px-3.5 py-1 rounded-full mb-2">
                            <span>🧭</span>
                            <span>Teori Minat & Kepribadian John L. Holland</span>
                        </div>
                        <h2 class="font-heading text-2xl sm:text-3xl md:text-4xl font-bold text-slate-900">Eksplorasi 6 Tipe RIASEC</h2>
                        <p class="text-sm sm:text-base text-slate-600 mt-1">
                            Pahami karakteristik utama, potensi karier unggulan, serta rekomendasi jalur sekolah dan perkuliahan.
                        </p>
                    </div>

                    <!-- Step Indicator Pills yang Lebih Besar dan Nyaman -->
                    <div class="flex flex-wrap items-center gap-2 bg-blue-50/90 p-2 rounded-2xl border border-blue-200">
                        <button onclick="bukaMateriSlide(0)" id="pill-step-0" class="materi-pill px-3.5 sm:px-4 py-2 rounded-xl text-xs sm:text-sm font-bold transition bg-blue-600 text-white shadow-xs">1. R - Realistik</button>
                        <button onclick="bukaMateriSlide(1)" id="pill-step-1" class="materi-pill px-3.5 sm:px-4 py-2 rounded-xl text-xs sm:text-sm font-bold transition text-slate-700 hover:bg-blue-100">2. I - Investigatif</button>
                        <button onclick="bukaMateriSlide(2)" id="pill-step-2" class="materi-pill px-3.5 sm:px-4 py-2 rounded-xl text-xs sm:text-sm font-bold transition text-slate-700 hover:bg-blue-100">3. A - Artistik</button>
                        <button onclick="bukaMateriSlide(3)" id="pill-step-3" class="materi-pill px-3.5 sm:px-4 py-2 rounded-xl text-xs sm:text-sm font-bold transition text-slate-700 hover:bg-blue-100">4. S - Sosial</button>
                        <button onclick="bukaMateriSlide(4)" id="pill-step-4" class="materi-pill px-3.5 sm:px-4 py-2 rounded-xl text-xs sm:text-sm font-bold transition text-slate-700 hover:bg-blue-100">5. E - Enterprising</button>
                        <button onclick="bukaMateriSlide(5)" id="pill-step-5" class="materi-pill px-3.5 sm:px-4 py-2 rounded-xl text-xs sm:text-sm font-bold transition text-slate-700 hover:bg-blue-100">6. C - Konvensional</button>
                    </div>
                </div>

                <!-- CAROUSEL SLIDE MATERI SATU PERSATU (TANPA KARAKTER HEWAN, DESAIN MODERN & ELEGAN) -->
                <div class="mt-6" id="materi-carousel-container">
                    
                    <!-- SLIDE 1: REALISTIC (R) -->
                    <div class="materi-slide active flex-col gap-6 p-6 sm:p-8 rounded-3xl bg-gradient-to-br from-blue-50/90 via-sky-50/40 to-white border-2 border-blue-200/90 shadow-xs" data-index="0">
                        <div class="flex flex-col sm:flex-row items-center sm:items-start gap-6">
                            <div class="relative shrink-0">
                                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-3xl bg-gradient-to-tr from-blue-600 via-blue-700 to-indigo-600 text-white flex flex-col items-center justify-center shadow-lg shadow-blue-300/40 border-4 border-white">
                                    <span class="font-heading text-3xl sm:text-4xl font-bold tracking-wider">R</span>
                                    <span class="text-xs font-bold text-sky-200 mt-0.5 uppercase tracking-widest">Tipe 1</span>
                                </div>
                                <span class="absolute -bottom-2 -right-1 bg-blue-900 text-white text-xs font-bold px-3 py-1 rounded-full shadow-xs">Kode R</span>
                            </div>
                            <div class="space-y-2 text-center sm:text-left flex-1">
                                <div class="inline-flex items-center gap-2 bg-blue-100 text-blue-800 text-xs sm:text-sm font-bold px-3.5 py-1 rounded-full">
                                    <span>⚙️</span>
                                    <span>Tipe Kepribadian #1 • Si Praktis & Teknik</span>
                                </div>
                                <h3 class="font-heading text-2xl sm:text-3xl font-bold text-slate-900">Realistic (Realistik)</h3>
                                <p class="text-sm sm:text-base text-slate-700 leading-relaxed font-medium">
                                    Individu dengan tipe Realistik menyukai pekerjaan yang bersifat konkret, menggunakan perkakas fisik, merakit komponen mekanik atau elektrik, serta beraktivitas langsung di lapangan terbuka.
                                </p>
                            </div>
                        </div>

                        <!-- Ciri Khas Kunci -->
                        <div class="bg-white/80 p-4 sm:p-5 rounded-2xl border border-blue-100 flex flex-wrap gap-2 items-center">
                            <span class="text-xs sm:text-sm font-bold text-blue-950 mr-2 flex items-center gap-1.5">
                                <span>✨</span> Ciri Khas Utama:
                            </span>
                            <span class="text-xs sm:text-sm bg-blue-50 text-blue-800 font-semibold px-3 py-1 rounded-xl border border-blue-200">Praktis & Solutif</span>
                            <span class="text-xs sm:text-sm bg-blue-50 text-blue-800 font-semibold px-3 py-1 rounded-xl border border-blue-200">Keterampilan Fisik & Mesin</span>
                            <span class="text-xs sm:text-sm bg-blue-50 text-blue-800 font-semibold px-3 py-1 rounded-xl border border-blue-200">Menyukai Karya Nyata</span>
                            <span class="text-xs sm:text-sm bg-blue-50 text-blue-800 font-semibold px-3 py-1 rounded-xl border border-blue-200">Fokus pada Hasil Konkret</span>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-5 pt-1">
                            <div class="bg-white p-5 rounded-2xl border border-blue-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-blue-950 flex items-center gap-2">
                                    <span>💼</span> Rekomendasi Profesi Ideal:
                                </h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Insinyur Mesin & Sipil</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Teknisi Otomotif & Robotika</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Pilot & Teknisi Penerbangan</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Arsitek Konstruksi</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Ahli Kelautan / Perkapalan</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Polisi / Militer (TNI)</span>
                                </div>
                            </div>

                            <div class="bg-white p-5 rounded-2xl border border-blue-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-slate-900 flex items-center gap-2">
                                    <span>🎓</span> Pilihan Jalur Pendidikan & Studi:
                                </h4>
                                <div class="space-y-2.5 text-xs sm:text-sm text-slate-700 leading-relaxed">
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-blue-950 block mb-0.5">Jalur SMK / Vokasi:</strong>
                                        Teknik Kendaraan Ringan (TKR), Teknik Permesinan, Mekatronika, Desain Pemodelan & Informasi Bangunan.
                                    </div>
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-blue-950 block mb-0.5">Jalur Kuliah (S1 / D4):</strong>
                                        Teknik Mesin, Teknik Sipil, Teknik Penerbangan, Ilmu Kelautan & Perikanan, Agroteknologi Modern.
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- SLIDE 2: INVESTIGATIVE (I) -->
                    <div class="materi-slide flex-col gap-6 p-6 sm:p-8 rounded-3xl bg-gradient-to-br from-indigo-50/90 via-blue-50/40 to-white border-2 border-indigo-200/90 shadow-xs" data-index="1">
                        <div class="flex flex-col sm:flex-row items-center sm:items-start gap-6">
                            <div class="relative shrink-0">
                                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-3xl bg-gradient-to-tr from-indigo-600 via-indigo-700 to-blue-600 text-white flex flex-col items-center justify-center shadow-lg shadow-indigo-300/40 border-4 border-white">
                                    <span class="font-heading text-3xl sm:text-4xl font-bold tracking-wider">I</span>
                                    <span class="text-xs font-bold text-indigo-200 mt-0.5 uppercase tracking-widest">Tipe 2</span>
                                </div>
                                <span class="absolute -bottom-2 -right-1 bg-indigo-900 text-white text-xs font-bold px-3 py-1 rounded-full shadow-xs">Kode I</span>
                            </div>
                            <div class="space-y-2 text-center sm:text-left flex-1">
                                <div class="inline-flex items-center gap-2 bg-indigo-100 text-indigo-800 text-xs sm:text-sm font-bold px-3.5 py-1 rounded-full">
                                    <span>🔬</span>
                                    <span>Tipe Kepribadian #2 • Si Peneliti & Logis</span>
                                </div>
                                <h3 class="font-heading text-2xl sm:text-3xl font-bold text-slate-900">Investigative (Investigatif)</h3>
                                <p class="text-sm sm:text-base text-slate-700 leading-relaxed font-medium">
                                    Individu dengan tipe Investigatif memiliki rasa ingin tahu intelektual yang tinggi, senang mengamati, menganalisis data, memecahkan teka-teki logika yang rumit, dan mengeksplorasi sains.
                                </p>
                            </div>
                        </div>

                        <!-- Ciri Khas Kunci -->
                        <div class="bg-white/80 p-4 sm:p-5 rounded-2xl border border-indigo-100 flex flex-wrap gap-2 items-center">
                            <span class="text-xs sm:text-sm font-bold text-indigo-950 mr-2 flex items-center gap-1.5">
                                <span>✨</span> Ciri Khas Utama:
                            </span>
                            <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-800 font-semibold px-3 py-1 rounded-xl border border-indigo-200">Berpikir Kritis & Analitis</span>
                            <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-800 font-semibold px-3 py-1 rounded-xl border border-indigo-200">Rasa Ingin Tahu Ilmiah</span>
                            <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-800 font-semibold px-3 py-1 rounded-xl border border-indigo-200">Berbasis Bukti & Fakta</span>
                            <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-800 font-semibold px-3 py-1 rounded-xl border border-indigo-200">Pemecah Masalah Kompleks</span>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-5 pt-1">
                            <div class="bg-white p-5 rounded-2xl border border-indigo-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-indigo-950 flex items-center gap-2">
                                    <span>💼</span> Rekomendasi Profesi Ideal:
                                </h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-900 font-semibold px-3 py-1.5 rounded-xl border border-indigo-200">Dokter Spesialis / Umum</span>
                                    <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-900 font-semibold px-3 py-1.5 rounded-xl border border-indigo-200">Peneliti Sains & Ahli Biologi</span>
                                    <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-900 font-semibold px-3 py-1.5 rounded-xl border border-indigo-200">Software Engineer / Programmer</span>
                                    <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-900 font-semibold px-3 py-1.5 rounded-xl border border-indigo-200">Data Scientist & AI Specialist</span>
                                    <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-900 font-semibold px-3 py-1.5 rounded-xl border border-indigo-200">Apoteker / Ahli Farmasi</span>
                                    <span class="text-xs sm:text-sm bg-indigo-50 text-indigo-900 font-semibold px-3 py-1.5 rounded-xl border border-indigo-200">Astronom & Fisikawan</span>
                                </div>
                            </div>

                            <div class="bg-white p-5 rounded-2xl border border-indigo-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-slate-900 flex items-center gap-2">
                                    <span>🎓</span> Pilihan Jalur Pendidikan & Studi:
                                </h4>
                                <div class="space-y-2.5 text-xs sm:text-sm text-slate-700 leading-relaxed">
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-indigo-950 block mb-0.5">Jalur SMA / SMK:</strong>
                                        SMA Jurusan MIPA/IPA, SMK Rekayasa Perangkat Lunak (RPL), SMK Farmasi Klinis, SMK Kimia Industri.
                                    </div>
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-indigo-950 block mb-0.5">Jalur Kuliah (S1 / D4):</strong>
                                        Kedokteran Umum/Gigi, Teknik Informatika & Ilmu Komputer, Farmasi, Bioteknologi, Matematika/Fisika Murni.
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- SLIDE 3: ARTISTIC (A) -->
                    <div class="materi-slide flex-col gap-6 p-6 sm:p-8 rounded-3xl bg-gradient-to-br from-sky-50/90 via-indigo-50/30 to-white border-2 border-sky-200/90 shadow-xs" data-index="2">
                        <div class="flex flex-col sm:flex-row items-center sm:items-start gap-6">
                            <div class="relative shrink-0">
                                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-3xl bg-gradient-to-tr from-sky-500 via-blue-600 to-indigo-500 text-white flex flex-col items-center justify-center shadow-lg shadow-sky-300/40 border-4 border-white">
                                    <span class="font-heading text-3xl sm:text-4xl font-bold tracking-wider">A</span>
                                    <span class="text-xs font-bold text-sky-200 mt-0.5 uppercase tracking-widest">Tipe 3</span>
                                </div>
                                <span class="absolute -bottom-2 -right-1 bg-sky-800 text-white text-xs font-bold px-3 py-1 rounded-full shadow-xs">Kode A</span>
                            </div>
                            <div class="space-y-2 text-center sm:text-left flex-1">
                                <div class="inline-flex items-center gap-2 bg-sky-100 text-sky-800 text-xs sm:text-sm font-bold px-3.5 py-1 rounded-full">
                                    <span>🎨</span>
                                    <span>Tipe Kepribadian #3 • Si Kreatif & Ekspresif</span>
                                </div>
                                <h3 class="font-heading text-2xl sm:text-3xl font-bold text-slate-900">Artistic (Artistik)</h3>
                                <p class="text-sm sm:text-base text-slate-700 leading-relaxed font-medium">
                                    Individu dengan tipe Artistik menyukai kebebasan dalam berimajinasi, mengekspresikan gagasan batin ke dalam bentuk karya seni visual, tulisan sastra, kreasi musik, atau rancangan desain yang estetis dan orisinal.
                                </p>
                            </div>
                        </div>

                        <!-- Ciri Khas Kunci -->
                        <div class="bg-white/80 p-4 sm:p-5 rounded-2xl border border-sky-100 flex flex-wrap gap-2 items-center">
                            <span class="text-xs sm:text-sm font-bold text-sky-950 mr-2 flex items-center gap-1.5">
                                <span>✨</span> Ciri Khas Utama:
                            </span>
                            <span class="text-xs sm:text-sm bg-sky-50 text-sky-800 font-semibold px-3 py-1 rounded-xl border border-sky-200">Imajinatif & Inovatif</span>
                            <span class="text-xs sm:text-sm bg-sky-50 text-sky-800 font-semibold px-3 py-1 rounded-xl border border-sky-200">Peka Terhadap Estetika</span>
                            <span class="text-xs sm:text-sm bg-sky-50 text-sky-800 font-semibold px-3 py-1 rounded-xl border border-sky-200">Menyukai Fleksibilitas</span>
                            <span class="text-xs sm:text-sm bg-sky-50 text-sky-800 font-semibold px-3 py-1 rounded-xl border border-sky-200">Ekspresi Orisinal</span>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-5 pt-1">
                            <div class="bg-white p-5 rounded-2xl border border-sky-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-sky-950 flex items-center gap-2">
                                    <span>💼</span> Rekomendasi Profesi Ideal:
                                </h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="text-xs sm:text-sm bg-sky-50 text-sky-900 font-semibold px-3 py-1.5 rounded-xl border border-sky-200">Desainer Grafis & UI/UX</span>
                                    <span class="text-xs sm:text-sm bg-sky-50 text-sky-900 font-semibold px-3 py-1.5 rounded-xl border border-sky-200">Animator 3D & Ilustrator</span>
                                    <span class="text-xs sm:text-sm bg-sky-50 text-sky-900 font-semibold px-3 py-1.5 rounded-xl border border-sky-200">Content Creator & Videografer</span>
                                    <span class="text-xs sm:text-sm bg-sky-50 text-sky-900 font-semibold px-3 py-1.5 rounded-xl border border-sky-200">Penulis Cerita & Novelis</span>
                                    <span class="text-xs sm:text-sm bg-sky-50 text-sky-900 font-semibold px-3 py-1.5 rounded-xl border border-sky-200">Arsitek & Desainer Interior</span>
                                    <span class="text-xs sm:text-sm bg-sky-50 text-sky-900 font-semibold px-3 py-1.5 rounded-xl border border-sky-200">Komposer Musik & Audio Editor</span>
                                </div>
                            </div>

                            <div class="bg-white p-5 rounded-2xl border border-sky-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-slate-900 flex items-center gap-2">
                                    <span>🎓</span> Pilihan Jalur Pendidikan & Studi:
                                </h4>
                                <div class="space-y-2.5 text-xs sm:text-sm text-slate-700 leading-relaxed">
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-sky-950 block mb-0.5">Jalur SMK / Vokasi:</strong>
                                        Desain Komunikasi Visual (DKV), Animasi, Seni Kriya & Desain Produk, Produksi Siaran & Perfilman.
                                    </div>
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-sky-950 block mb-0.5">Jalur Kuliah (S1 / D4):</strong>
                                        Desain Komunikasi Visual (DKV), Seni Rupa Murni, Desain Produk, Sastra & Penulisan Kreatif, Perfilman.
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- SLIDE 4: SOCIAL (S) -->
                    <div class="materi-slide flex-col gap-6 p-6 sm:p-8 rounded-3xl bg-gradient-to-br from-teal-50/90 via-sky-50/40 to-white border-2 border-teal-200/90 shadow-xs" data-index="3">
                        <div class="flex flex-col sm:flex-row items-center sm:items-start gap-6">
                            <div class="relative shrink-0">
                                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-3xl bg-gradient-to-tr from-teal-600 via-teal-700 to-blue-600 text-white flex flex-col items-center justify-center shadow-lg shadow-teal-300/40 border-4 border-white">
                                    <span class="font-heading text-3xl sm:text-4xl font-bold tracking-wider">S</span>
                                    <span class="text-xs font-bold text-teal-200 mt-0.5 uppercase tracking-widest">Tipe 4</span>
                                </div>
                                <span class="absolute -bottom-2 -right-1 bg-teal-800 text-white text-xs font-bold px-3 py-1 rounded-full shadow-xs">Kode S</span>
                            </div>
                            <div class="space-y-2 text-center sm:text-left flex-1">
                                <div class="inline-flex items-center gap-2 bg-teal-100 text-teal-800 text-xs sm:text-sm font-bold px-3.5 py-1 rounded-full">
                                    <span>🤝</span>
                                    <span>Tipe Kepribadian #4 • Si Penolong & Edukator</span>
                                </div>
                                <h3 class="font-heading text-2xl sm:text-3xl font-bold text-slate-900">Social (Sosial)</h3>
                                <p class="text-sm sm:text-base text-slate-700 leading-relaxed font-medium">
                                    Individu dengan tipe Sosial memiliki empati yang hangat, senang mendengarkan dan mendampingi orang lain, mengajarkan hal yang berguna, serta bersemangat memajukan kesejahteraan masyarakat.
                                </p>
                            </div>
                        </div>

                        <!-- Ciri Khas Kunci -->
                        <div class="bg-white/80 p-4 sm:p-5 rounded-2xl border border-teal-100 flex flex-wrap gap-2 items-center">
                            <span class="text-xs sm:text-sm font-bold text-teal-950 mr-2 flex items-center gap-1.5">
                                <span>✨</span> Ciri Khas Utama:
                            </span>
                            <span class="text-xs sm:text-sm bg-teal-50 text-teal-800 font-semibold px-3 py-1 rounded-xl border border-teal-200">Empati & Kepedulian Tinggi</span>
                            <span class="text-xs sm:text-sm bg-teal-50 text-teal-800 font-semibold px-3 py-1 rounded-xl border border-teal-200">Komunikasi Interpersonal</span>
                            <span class="text-xs sm:text-sm bg-teal-50 text-teal-800 font-semibold px-3 py-1 rounded-xl border border-teal-200">Senang Mengajar & Membimbing</span>
                            <span class="text-xs sm:text-sm bg-teal-50 text-teal-800 font-semibold px-3 py-1 rounded-xl border border-teal-200">Kolaboratif dalam Tim</span>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-5 pt-1">
                            <div class="bg-white p-5 rounded-2xl border border-teal-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-teal-950 flex items-center gap-2">
                                    <span>💼</span> Rekomendasi Profesi Ideal:
                                </h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="text-xs sm:text-sm bg-teal-50 text-teal-900 font-semibold px-3 py-1.5 rounded-xl border border-teal-200">Guru Pendidik / Dosen</span>
                                    <span class="text-xs sm:text-sm bg-teal-50 text-teal-900 font-semibold px-3 py-1.5 rounded-xl border border-teal-200">Konselor Bimbingan & Konseling (BK)</span>
                                    <span class="text-xs sm:text-sm bg-teal-50 text-teal-900 font-semibold px-3 py-1.5 rounded-xl border border-teal-200">Psikolog Klinis & Remaja</span>
                                    <span class="text-xs sm:text-sm bg-teal-50 text-teal-900 font-semibold px-3 py-1.5 rounded-xl border border-teal-200">Perawat & Tenaga Kesehatan</span>
                                    <span class="text-xs sm:text-sm bg-teal-50 text-teal-900 font-semibold px-3 py-1.5 rounded-xl border border-teal-200">Pekerja Sosial & Pemberdayaan</span>
                                    <span class="text-xs sm:text-sm bg-teal-50 text-teal-900 font-semibold px-3 py-1.5 rounded-xl border border-teal-200">Trainer Pelatihan / HRD</span>
                                </div>
                            </div>

                            <div class="bg-white p-5 rounded-2xl border border-teal-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-slate-900 flex items-center gap-2">
                                    <span>🎓</span> Pilihan Jalur Pendidikan & Studi:
                                </h4>
                                <div class="space-y-2.5 text-xs sm:text-sm text-slate-700 leading-relaxed">
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-teal-950 block mb-0.5">Jalur SMK / Vokasi:</strong>
                                        Layanan Penunjang Medis (Asisten Keperawatan), Layanan Sosial Masyarakat.
                                    </div>
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-teal-950 block mb-0.5">Jalur Kuliah (S1 / D4):</strong>
                                        Bimbingan & Konseling (BK), Psikologi, Ilmu Pendidikan/Keguruan, Ilmu Keperawatan, Kesejahteraan Sosial.
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- SLIDE 5: ENTERPRISING (E) -->
                    <div class="materi-slide flex-col gap-6 p-6 sm:p-8 rounded-3xl bg-gradient-to-br from-amber-50/90 via-sky-50/40 to-white border-2 border-amber-200/90 shadow-xs" data-index="4">
                        <div class="flex flex-col sm:flex-row items-center sm:items-start gap-6">
                            <div class="relative shrink-0">
                                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-3xl bg-gradient-to-tr from-amber-500 via-amber-600 to-blue-600 text-white flex flex-col items-center justify-center shadow-lg shadow-amber-300/40 border-4 border-white">
                                    <span class="font-heading text-3xl sm:text-4xl font-bold tracking-wider">E</span>
                                    <span class="text-xs font-bold text-amber-200 mt-0.5 uppercase tracking-widest">Tipe 5</span>
                                </div>
                                <span class="absolute -bottom-2 -right-1 bg-amber-800 text-white text-xs font-bold px-3 py-1 rounded-full shadow-xs">Kode E</span>
                            </div>
                            <div class="space-y-2 text-center sm:text-left flex-1">
                                <div class="inline-flex items-center gap-2 bg-amber-100 text-amber-900 text-xs sm:text-sm font-bold px-3.5 py-1 rounded-full">
                                    <span>🚀</span>
                                    <span>Tipe Kepribadian #5 • Si Pemimpin & Wirausaha</span>
                                </div>
                                <h3 class="font-heading text-2xl sm:text-3xl font-bold text-slate-900">Enterprising (Kewirausahaan)</h3>
                                <p class="text-sm sm:text-base text-slate-700 leading-relaxed font-medium">
                                    Individu dengan tipe Enterprising memiliki kepemimpinan alami yang tangguh, percaya diri dalam bernegosiasi bisnis, berani mengambil risiko terukur untuk meraih peluang, dan mahir meyakinkan orang lain.
                                </p>
                            </div>
                        </div>

                        <!-- Ciri Khas Kunci -->
                        <div class="bg-white/80 p-4 sm:p-5 rounded-2xl border border-amber-100 flex flex-wrap gap-2 items-center">
                            <span class="text-xs sm:text-sm font-bold text-amber-950 mr-2 flex items-center gap-1.5">
                                <span>✨</span> Ciri Khas Utama:
                            </span>
                            <span class="text-xs sm:text-sm bg-amber-50 text-amber-900 font-semibold px-3 py-1 rounded-xl border border-amber-200">Kepemimpinan Kuat</span>
                            <span class="text-xs sm:text-sm bg-amber-50 text-amber-900 font-semibold px-3 py-1 rounded-xl border border-amber-200">Persuasif & Komunikatif</span>
                            <span class="text-xs sm:text-sm bg-amber-50 text-amber-900 font-semibold px-3 py-1 rounded-xl border border-amber-200">Berani Mengambil Peluang</span>
                            <span class="text-xs sm:text-sm bg-amber-50 text-amber-900 font-semibold px-3 py-1 rounded-xl border border-amber-200">Berorientasi Prestasi</span>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-5 pt-1">
                            <div class="bg-white p-5 rounded-2xl border border-amber-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-amber-950 flex items-center gap-2">
                                    <span>💼</span> Rekomendasi Profesi Ideal:
                                </h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="text-xs sm:text-sm bg-amber-50 text-amber-950 font-semibold px-3 py-1.5 rounded-xl border border-amber-200">Wirausahawan / Founder Startup</span>
                                    <span class="text-xs sm:text-sm bg-amber-50 text-amber-950 font-semibold px-3 py-1.5 rounded-xl border border-amber-200">Manajer Pemasaran & Brand</span>
                                    <span class="text-xs sm:text-sm bg-amber-50 text-amber-950 font-semibold px-3 py-1.5 rounded-xl border border-amber-200">Direktur / Pemimpin Organisasi</span>
                                    <span class="text-xs sm:text-sm bg-amber-50 text-amber-950 font-semibold px-3 py-1.5 rounded-xl border border-amber-200">Pengacara / Advokat</span>
                                    <span class="text-xs sm:text-sm bg-amber-50 text-amber-950 font-semibold px-3 py-1.5 rounded-xl border border-amber-200">Konsultan Manajemen Bisnis</span>
                                    <span class="text-xs sm:text-sm bg-amber-50 text-amber-950 font-semibold px-3 py-1.5 rounded-xl border border-amber-200">Diplomat / Hubungan Internasional</span>
                                </div>
                            </div>

                            <div class="bg-white p-5 rounded-2xl border border-amber-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-slate-900 flex items-center gap-2">
                                    <span>🎓</span> Pilihan Jalur Pendidikan & Studi:
                                </h4>
                                <div class="space-y-2.5 text-xs sm:text-sm text-slate-700 leading-relaxed">
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-amber-950 block mb-0.5">Jalur SMK / Vokasi:</strong>
                                        Bisnis Daring & Pemasaran (BDP), Manajemen Retail, Manajemen Logistik & Distribusi.
                                    </div>
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-amber-950 block mb-0.5">Jalur Kuliah (S1 / D4):</strong>
                                        Manajemen Bisnis, Kewirausahaan, Ilmu Hukum, Hubungan Internasional, Digital Marketing.
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- SLIDE 6: CONVENTIONAL (C) -->
                    <div class="materi-slide flex-col gap-6 p-6 sm:p-8 rounded-3xl bg-gradient-to-br from-blue-50/90 via-indigo-50/40 to-white border-2 border-blue-200/90 shadow-xs" data-index="5">
                        <div class="flex flex-col sm:flex-row items-center sm:items-start gap-6">
                            <div class="relative shrink-0">
                                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-3xl bg-gradient-to-tr from-blue-700 via-indigo-800 to-sky-600 text-white flex flex-col items-center justify-center shadow-lg shadow-blue-400/40 border-4 border-white">
                                    <span class="font-heading text-3xl sm:text-4xl font-bold tracking-wider">C</span>
                                    <span class="text-xs font-bold text-sky-200 mt-0.5 uppercase tracking-widest">Tipe 6</span>
                                </div>
                                <span class="absolute -bottom-2 -right-1 bg-blue-900 text-white text-xs font-bold px-3 py-1 rounded-full shadow-xs">Kode C</span>
                            </div>
                            <div class="space-y-2 text-center sm:text-left flex-1">
                                <div class="inline-flex items-center gap-2 bg-blue-100 text-blue-900 text-xs sm:text-sm font-bold px-3.5 py-1 rounded-full">
                                    <span>📊</span>
                                    <span>Tipe Kepribadian #6 • Si Teratur & Pengelola Data</span>
                                </div>
                                <h3 class="font-heading text-2xl sm:text-3xl font-bold text-slate-900">Conventional (Konvensional)</h3>
                                <p class="text-sm sm:text-base text-slate-700 leading-relaxed font-medium">
                                    Individu dengan tipe Konvensional menyukai keteraturan yang rapi, sangat teliti dalam mengelola angka dan arsip dokumen, serta andal dalam menjalankan prosedur kerja secara akurat dan konsisten.
                                </p>
                            </div>
                        </div>

                        <!-- Ciri Khas Kunci -->
                        <div class="bg-white/80 p-4 sm:p-5 rounded-2xl border border-blue-100 flex flex-wrap gap-2 items-center">
                            <span class="text-xs sm:text-sm font-bold text-blue-950 mr-2 flex items-center gap-1.5">
                                <span>✨</span> Ciri Khas Utama:
                            </span>
                            <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1 rounded-xl border border-blue-200">Sistematis & Sangat Rapi</span>
                            <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1 rounded-xl border border-blue-200">Ketelitian Angka & Data</span>
                            <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1 rounded-xl border border-blue-200">Taat Prosedur Baku</span>
                            <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1 rounded-xl border border-blue-200">Dapat Diandalkan</span>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-5 pt-1">
                            <div class="bg-white p-5 rounded-2xl border border-blue-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-blue-950 flex items-center gap-2">
                                    <span>💼</span> Rekomendasi Profesi Ideal:
                                </h4>
                                <div class="flex flex-wrap gap-2">
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Akuntan Publik & Auditor</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Staf Administrasi Eksekutif</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Sekretaris Perusahaan</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Analis Keuangan & Pajak</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Pengelola Basis Data / Arsiparis</span>
                                    <span class="text-xs sm:text-sm bg-blue-50 text-blue-900 font-semibold px-3 py-1.5 rounded-xl border border-blue-200">Banker / Staf Layanan Perbankan</span>
                                </div>
                            </div>

                            <div class="bg-white p-5 rounded-2xl border border-blue-100 shadow-2xs space-y-3">
                                <h4 class="font-heading text-sm sm:text-base font-bold text-slate-900 flex items-center gap-2">
                                    <span>🎓</span> Pilihan Jalur Pendidikan & Studi:
                                </h4>
                                <div class="space-y-2.5 text-xs sm:text-sm text-slate-700 leading-relaxed">
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-blue-950 block mb-0.5">Jalur SMK / Vokasi:</strong>
                                        Akuntansi & Keuangan Lembaga (AKL), Otomatisasi & Tata Kelola Perkantoran (OTKP).
                                    </div>
                                    <div class="p-2.5 rounded-xl bg-slate-50 border border-slate-100">
                                        <strong class="text-blue-950 block mb-0.5">Jalur Kuliah (S1 / D4):</strong>
                                        Akuntansi, Manajemen Keuangan, Perbankan, Administrasi Niaga / Publik, Ilmu Kearsipan & Perpustakaan.
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                </div>

                <!-- Kontrol Navigasi Slide Materi yang Nyaman -->
                <div class="flex items-center justify-between pt-6 border-t border-blue-100">
                    <button id="btn-materi-prev" onclick="geserMateri(-1)" class="px-5 py-2.5 rounded-xl text-xs sm:text-sm font-bold text-slate-700 hover:bg-blue-50 transition border border-blue-200 flex items-center gap-2">
                        <span>←</span>
                        <span>Tipe Sebelumnya</span>
                    </button>
                    
                    <span id="materi-page-indicator" class="text-xs sm:text-sm font-bold text-blue-900 bg-blue-100/80 px-4 py-1.5 rounded-full border border-blue-200">
                        Tipe 1 dari 6
                    </span>

                    <button id="btn-materi-next" onclick="geserMateri(1)" class="px-6 py-2.5 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs sm:text-sm font-bold transition scale-bounce flex items-center gap-2 shadow-xs">
                        <span>Tipe Selanjutnya</span>
                        <span>→</span>
                    </button>
                </div>

                <!-- Box Kutipan Guru BK -->
                <div class="mt-6 bg-blue-50/90 border border-blue-200 rounded-2xl p-5 flex items-start gap-4">
                    <span class="text-3xl shrink-0">💡</span>
                    <div class="space-y-1">
                        <h4 class="font-heading text-sm sm:text-base font-bold text-blue-950">Catatan Penting Guru Bimbingan dan Konseling:</h4>
                        <p class="text-xs sm:text-sm text-blue-950/90 leading-relaxed italic">
                            "Setiap orang umumnya memiliki perpaduan unik dari 2 hingga 3 tipe kepribadian tertinggi. Teori John Holland ini dirancang sebagai panduan awal untuk membantumu mengeksplorasi potensi diri, memilih bidang peminatan studi yang tepat, dan merencanakan masa depan sejak dini!"
                        </p>
                    </div>
                </div>

                <div class="flex justify-between items-center pt-4">
                    <button onclick="navigateTo('tujuan')" class="px-4 py-2 border border-slate-200 text-slate-600 rounded-xl text-xs sm:text-sm font-semibold hover:bg-slate-50 transition">← Tujuan Pembelajaran</button>
                    <button onclick="navigateTo('video')" class="px-6 py-3 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs sm:text-sm font-bold transition scale-bounce flex items-center gap-2 shadow-sm">
                        <span>Lanjut ke Video Pembelajaran</span>
                        <span>➔</span>
                    </button>
                </div>
            </div>
        </section>

        <section id="sec-video" class="content-section space-y-6">
            <div class="bg-white/95 backdrop-blur rounded-3xl p-6 sm:p-8 border border-blue-100 shadow-sm space-y-6">
                <div>
                    <span class="text-xs font-bold text-blue-700 uppercase tracking-widest bg-blue-100 px-3 py-1 rounded-full">Media Audio Visual</span>
                    <h2 class="font-heading text-2xl sm:text-3xl font-bold text-slate-800 mt-2">Video Pembelajaran RIASEC</h2>
                    <p class="text-xs text-slate-500 mt-0.5">Simak penjelasan interaktif dari Guru BK dan kenali 6 tipe kepribadian karier</p>
                </div>

                <div class="max-w-4xl mx-auto bg-black rounded-3xl overflow-hidden shadow-xl aspect-video border border-blue-200">
                    <iframe class="w-full h-full" src="https://www.youtube.com/embed/DkAXVIwzT44?start=4" title="Video Pembelajaran RIASEC" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
                </div>

                <div class="max-w-4xl mx-auto bg-blue-50/70 p-6 rounded-2xl border border-blue-200">
                    <h3 class="font-heading text-base font-bold text-slate-800 mb-2 flex items-center gap-2">
                        <span>💬</span> Pertanyaan Pemantik Video
                    </h3>
                    <p class="text-xs text-slate-600 mb-3 leading-relaxed">
                        "Setelah menyimak video di atas, tipe kepribadian mana yang menurutmu paling menggambarkan dirimu saat ini? Mengapa demikian?"
                    </p>
                    <textarea id="jawaban-pemantik" rows="3" placeholder="Tuliskan pendapat singkatmu di sini..." class="w-full p-3 text-xs rounded-xl border border-blue-200 bg-white focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
                    <div class="mt-2 flex justify-between items-center">
                        <span id="pemantik-feedback" class="text-xs text-emerald-700 font-bold hidden">✔ Respon tersimpan!</span>
                        <button onclick="simpanPemantik()" class="px-5 py-2 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs font-bold transition ml-auto">
                            Simpan Respon
                        </button>
                    </div>
                </div>

                <div class="flex justify-between items-center pt-2">
                    <button onclick="navigateTo('materi')" class="px-4 py-2 border border-slate-200 text-slate-600 rounded-xl text-xs font-semibold hover:bg-slate-50 transition">← Materi RIASEC</button>
                    <button onclick="navigateTo('tes')" class="px-6 py-2.5 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs font-bold transition scale-bounce flex items-center gap-2 shadow-xs">
                        <span>Lanjut ke Tes Kepribadian</span>
                        <span>➔</span>
                    </button>
                </div>
            </div>
        </section>

        <section id="sec-tes" class="content-section space-y-6">
            
            <!-- VIEW 5A: INPUT DATA SISWA -->
            <div id="tes-view-identitas" class="bg-white/95 backdrop-blur rounded-3xl p-6 sm:p-8 border border-blue-100 shadow-sm space-y-4 no-print">
                <div class="max-w-xl">
                    <span class="text-xs font-bold text-blue-700 uppercase tracking-widest bg-blue-100 px-3 py-1 rounded-full">Instrumen Mandiri</span>
                    <h2 class="font-heading text-2xl sm:text-3xl font-bold text-slate-800 mt-2">Tes Minat Holland RIASEC (36 Butir)</h2>
                    <p class="text-xs text-slate-500 mt-1">
                        Pilih skor 1 (Sangat Tidak Sesuai) sampai 5 (Sangat Sesuai) yang paling jujur menggambarkan dirimu.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-4 pt-2">
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-1">Nama Lengkap Siswa *</label>
                        <input type="text" id="tes-input-nama" placeholder="Tulis nama lengkapmu..." class="w-full text-xs font-semibold px-3.5 py-2.5 bg-white border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-1">Kelas / Tingkat *</label>
                        <input type="text" id="tes-input-kelas" placeholder="Contoh: 7A / 8B / 9C" class="w-full text-xs font-semibold px-3.5 py-2.5 bg-white border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-1">Asal Sekolah</label>
                        <input type="text" id="tes-input-sekolah" value="SMP Negeri 3 Cilegon" class="w-full text-xs font-semibold px-3.5 py-2.5 bg-white border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>
                </div>
                <button onclick="mulaiKuis()" class="w-full mt-2 py-3 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs sm:text-sm font-bold shadow-md transition scale-bounce flex items-center justify-center gap-2">
                    <span>Mulai Menjawab 36 Butir Pernyataan RIASEC</span>
                    <span>➔</span>
                </button>
            </div>

            <!-- VIEW 5B: INTERAKSI SOAL KUIS (NO-PRINT) -->
            <div id="tes-view-kuis" class="hidden space-y-6 no-print">
                <!-- Progress Card -->
                <div class="bg-blue-50/80 p-4 rounded-2xl border border-blue-200 space-y-2">
                    <div class="flex justify-between items-center text-xs font-bold text-slate-700">
                        <span id="tes-nama-display">Siswa: -</span>
                        <span id="tes-soal-progress" class="text-blue-700 font-bold">Soal 1 dari 36</span>
                        <span id="tes-terjawab-counter" class="bg-blue-100 text-blue-900 text-[11px] px-2.5 py-0.5 rounded-full font-bold">0 Terjawab</span>
                    </div>
                    <div class="w-full bg-slate-200 h-2.5 rounded-full overflow-hidden">
                        <div id="tes-progress-fill" class="bg-gradient-to-r from-blue-500 to-indigo-600 h-full transition-all duration-300 w-[2.7%]"></div>
                    </div>

                    <!-- Selector Grid 1 - 36 -->
                    <div class="pt-2">
                        <div class="text-[10px] font-semibold text-slate-400 mb-1">Pilihan Cepat Nomor Soal:</div>
                        <div id="tes-nomor-grid" class="grid grid-cols-9 sm:grid-cols-12 gap-1"></div>
                    </div>
                </div>

                <!-- Soal Aktif Card -->
                <div class="bg-white p-6 sm:p-8 rounded-3xl border border-blue-100 shadow-xs">
                    <div class="flex items-center justify-between border-b border-slate-100 pb-3 mb-4">
                        <span id="tes-badge-tipe" class="text-xs font-bold px-3 py-1 rounded-full bg-blue-100 text-blue-800">
                            Tipe R - Realistik
                        </span>
                        <span id="tes-badge-no" class="text-xs font-bold text-slate-400 bg-slate-100 px-2.5 py-1 rounded-lg">#1</span>
                    </div>

                    <h3 id="tes-soal-text" class="text-base sm:text-lg font-bold text-slate-800 min-h-[50px] flex items-center leading-relaxed">
                        "Saya senang memperbaiki, merakit, atau membongkar benda dengan tangan sendiri."
                    </h3>

                    <!-- Pilihan Skala 1 - 5 -->
                    <div class="grid grid-cols-1 sm:grid-cols-5 gap-2.5 my-6">
                        <button onclick="pilihSkor(1)" id="btn-skor-1" class="scale-btn p-3 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-400 flex flex-col items-center gap-1 transition scale-bounce">
                            <span class="text-2xl">😞</span>
                            <span class="text-xs font-bold text-slate-800">1</span>
                            <span class="text-[10px] text-slate-500 font-medium text-center">Sangat Tidak Sesuai</span>
                        </button>
                        <button onclick="pilihSkor(2)" id="btn-skor-2" class="scale-btn p-3 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-400 flex flex-col items-center gap-1 transition scale-bounce">
                            <span class="text-2xl">😐</span>
                            <span class="text-xs font-bold text-slate-800">2</span>
                            <span class="text-[10px] text-slate-500 font-medium text-center">Tidak Sesuai</span>
                        </button>
                        <button onclick="pilihSkor(3)" id="btn-skor-3" class="scale-btn p-3 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-400 flex flex-col items-center gap-1 transition scale-bounce">
                            <span class="text-2xl">🙂</span>
                            <span class="text-xs font-bold text-slate-800">3</span>
                            <span class="text-[10px] text-slate-500 font-medium text-center">Cukup Sesuai</span>
                        </button>
                        <button onclick="pilihSkor(4)" id="btn-skor-4" class="scale-btn p-3 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-400 flex flex-col items-center gap-1 transition scale-bounce">
                            <span class="text-2xl">😊</span>
                            <span class="text-xs font-bold text-slate-800">4</span>
                            <span class="text-[10px] text-slate-500 font-medium text-center">Sesuai</span>
                        </button>
                        <button onclick="pilihSkor(5)" id="btn-skor-5" class="scale-btn p-3 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-400 flex flex-col items-center gap-1 transition scale-bounce">
                            <span class="text-2xl">🌟</span>
                            <span class="text-xs font-bold text-slate-800">5</span>
                            <span class="text-[10px] text-slate-500 font-medium text-center">Sangat Sesuai</span>
                        </button>
                    </div>

                    <!-- Prev / Next Controls -->
                    <div class="flex justify-between items-center pt-3 border-t border-slate-100">
                        <button id="btn-soal-prev" onclick="prevSoal()" class="px-4 py-2 rounded-xl text-xs font-bold text-slate-600 hover:bg-slate-100 transition">
                            ← Soal Sebelumnya
                        </button>
                        <div class="flex items-center gap-2">
                            <button id="btn-soal-next" onclick="nextSoal()" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 rounded-xl text-xs font-bold transition">
                                Selanjutnya →
                            </button>
                            <button onclick="selesaikanTes()" class="px-5 py-2 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs font-bold transition scale-bounce flex items-center gap-1.5 shadow-sm">
                                <span>Lihat Hasil Tes</span>
                                <span>🎉</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- VIEW 5C: HASIL TES RESMI DENGAN PROFESI IDEAL & JURUSAN SEKOLAH/KULIAH (PRINTABLE) -->
            <div id="tes-view-hasil" class="hidden space-y-6">
                <div class="bg-white rounded-3xl p-6 sm:p-8 border border-blue-200 shadow-sm" id="hasil-tes-print-container">
                    
                    <!-- Header Laporan Dokumen -->
                    <div class="border-b-2 border-blue-900 pb-4 mb-6 text-center">
                        <h2 class="font-heading text-xl sm:text-2xl font-bold text-slate-900 uppercase tracking-wide">
                            LAPORAN HASIL ASESMEN KEPRIBADIAN KARIER HOLLAND (RIASEC)
                        </h2>
                        <p class="text-xs font-semibold text-blue-800 mt-1">
                            Layanan Bimbingan & Konseling • SMP Negeri 3 Cilegon
                        </p>
                    </div>

                    <!-- Identitas Peserta -->
                    <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4 bg-blue-50/70 p-4 rounded-2xl border border-blue-200 mb-6">
                        <div>
                            <span class="text-[10px] font-bold text-blue-700 bg-blue-100 px-2.5 py-0.5 rounded-full uppercase">
                                Identitas Peserta Tes
                            </span>
                            <h3 id="hasil-nama-siswa" class="font-heading text-xl font-bold text-slate-800 mt-1">Nama Siswa</h3>
                            <p id="hasil-meta-siswa" class="text-xs text-slate-600 mt-0.5">Kelas: - • SMP Negeri 3 Cilegon</p>
                        </div>

                        <div class="bg-gradient-to-br from-blue-600 to-indigo-700 text-white border border-blue-300 px-6 py-3.5 rounded-2xl text-center shadow-sm">
                            <span class="text-[10px] text-blue-100 font-bold block uppercase tracking-wider">3 Kode Holland Teratas</span>
                            <span id="hasil-kode-holland" class="font-heading text-2xl sm:text-3xl font-bold tracking-widest text-white">R - I - A</span>
                        </div>
                    </div>

                    <!-- Banner Dominan -->
                    <div id="hasil-banner-dominan" class="p-5 rounded-2xl bg-gradient-to-r from-blue-700 via-indigo-700 to-sky-700 text-white flex flex-col sm:flex-row items-center gap-4 shadow-sm">
                        <div id="hasil-avatar-dominan" class="w-16 h-16 rounded-2xl bg-white/20 flex items-center justify-center font-heading text-3xl font-bold shrink-0 border border-white/30">
                            R
                        </div>
                        <div>
                            <span class="text-[10px] bg-white/20 px-2.5 py-0.5 rounded-full font-bold uppercase tracking-wide">
                                Tipe Dominan Utama
                            </span>
                            <h4 id="hasil-tipe-judul" class="font-heading text-lg font-bold mt-1">Realistic (Realistik)</h4>
                            <p id="hasil-tipe-desc" class="text-xs text-white/90 leading-relaxed mt-1">
                                Menyukai hal konkret, alat mekanik, teknologi fisik, dan aktivitas langsung di lapangan.
                            </p>
                        </div>
                    </div>

                    <!-- BAGIAN KHUSUS: PROFESI IDEAL & REKOMENDASI JURUSAN SESUAI HASIL TES -->
                    <div class="mt-6 space-y-4">
                        <div class="flex items-center gap-2 border-b border-blue-100 pb-2">
                            <span class="text-xl">🎯</span>
                            <h3 class="font-heading text-base font-bold text-slate-800">
                                Rekomendasi Profesi Ideal & Jalur Pendidikan Masa Depan
                            </h3>
                        </div>

                        <!-- Kontainer Dinamis Profesi & Jurusan -->
                        <div id="hasil-rekomendasi-grid" class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <!-- Diisi secara otomatis oleh JavaScript berdasarkan 3 Kode Holland -->
                        </div>
                    </div>

                    <!-- Bar Skor 6 Dimensi Holland -->
                    <div class="mt-6">
                        <h4 class="font-heading text-sm font-bold text-slate-800 mb-3">Rincian Skor 6 Dimensi Holland (Skor Maksimal: 30)</h4>
                        <div id="hasil-skor-bars" class="space-y-2.5 text-xs font-semibold"></div>
                    </div>

                    <!-- Signature Section for Print with Real TTD -->
                    <div class="mt-8 pt-6 border-t border-slate-200 flex justify-between items-end text-xs text-slate-700">
                        <div>
                            <p class="text-[11px] text-slate-500">Dokumen asesmen karier digital sah.</p>
                            <p class="text-[11px] text-blue-900 font-semibold mt-0.5">SMP Negeri 3 Cilegon</p>
                        </div>
                        <div class="text-right space-y-1">
                            <p id="hasil-tes-tanggal">Cilegon, 18 September 2026</p>
                            <p class="font-medium text-slate-600">Guru Bimbingan dan Konseling,</p>
                            <!-- Ruang kosong untuk tanda tangan manual -->
                            <div class="h-20 my-0.5"></div>
                            <p class="font-bold text-slate-900 underline">Isnani Akmilatir Rosyida, S.Sos</p>
                            <p class="text-[11px] text-slate-600">NIP. 200104012025212014</p>
                        </div>
                    </div>

                    <!-- Action Buttons (No-print) -->
                    <div class="mt-8 pt-4 border-t border-slate-100 flex flex-wrap items-center justify-between gap-3 no-print">
                        <button onclick="cetakDokumen('tes')" class="px-5 py-2.5 bg-blue-900 hover:bg-slate-900 text-white rounded-xl text-xs font-bold transition scale-bounce flex items-center gap-2 shadow-sm">
                            <span>🖨️️ Cetak / Unduh PDF Hasil Tes</span>
                        </button>

                        <div class="flex items-center gap-2">
                            <button onclick="salinKeLkpd()" class="px-5 py-2.5 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs font-bold transition scale-bounce flex items-center gap-1.5 shadow-sm">
                                <span>Terapkan Otomatis ke LKPD</span>
                                <span>➔</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="flex justify-between items-center pt-2 no-print">
                <button onclick="navigateTo('video')" class="px-4 py-2 border border-slate-200 text-slate-600 rounded-xl text-xs font-semibold hover:bg-slate-50 transition">← Video Edukasi</button>
                <button onclick="navigateTo('lkpd')" class="px-6 py-2.5 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs font-bold transition scale-bounce flex items-center gap-2">
                    <span>Lanjut Mengisi LKPD Digital</span>
                    <span>➔</span>
                </button>
            </div>
        </section>

        <section id="sec-lkpd" class="content-section space-y-6">
            <div class="bg-white rounded-3xl p-6 sm:p-8 border border-blue-100 shadow-xs" id="lkpd-print-container">
                
                <div class="border-b-2 border-blue-900 pb-4 mb-6 text-center">
                    <h2 class="font-heading text-lg sm:text-2xl font-bold text-slate-900 uppercase tracking-wide">
                        LEMBAR KERJA PESERTA DIDIK (LKPD)
                    </h2>
                    <h3 class="text-xs sm:text-sm font-bold text-blue-900 uppercase tracking-widest mt-0.5">
                        RENCANA PENGEMBANGAN KARIER MENURUT TEORI JOHN L. HOLLAND
                    </h3>
                    <p class="text-[11px] text-slate-500 mt-1">
                        Bimbingan Klasikal Karier • SMP Negeri 3 Cilegon • Guru BK: Isnani Akmilatir Rosyida, S.Sos
                    </p>
                </div>

                <!-- Identitas Siswa LKPD -->
                <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 bg-blue-50/70 p-4 rounded-2xl border border-blue-200 mb-6">
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-1">Nama Lengkap Siswa:</label>
                        <input type="text" id="lkpd-nama" placeholder="Tulis nama lengkap..." class="w-full text-xs font-semibold px-3 py-2 bg-white border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-1">Kelas / Tingkat:</label>
                        <input type="text" id="lkpd-kelas" placeholder="Tulis kelas..." class="w-full text-xs font-semibold px-3 py-2 bg-white border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-blue-800 mb-1">Hasil Kode Tes RIASEC (3 Teratas):</label>
                        <input type="text" id="lkpd-kode" placeholder="Contoh: R - I - A" class="w-full text-xs font-bold px-3 py-2 bg-white border border-blue-300 text-blue-900 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>
                </div>

                <!-- 7 Pertanyaan Panduan Sesuai RPL -->
                <form id="form-lkpd" class="space-y-4" onsubmit="event.preventDefault();">
                    
                    <div class="bg-white p-4 rounded-2xl border border-blue-100 shadow-2xs">
                        <label class="block text-xs font-bold text-slate-800 mb-1.5">
                            1. Tipe kepribadian utama saya (berdasarkan hasil tes Holland):
                        </label>
                        <input type="text" id="lkpd-q1" placeholder="Contoh: Realistic (R) dan Investigative (I)..." class="w-full text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>

                    <div class="bg-white p-4 rounded-2xl border border-blue-100 shadow-2xs">
                        <label class="block text-xs font-bold text-slate-800 mb-1.5">
                            2. Karakteristik yang paling sesuai dengan diri saya:
                        </label>
                        <textarea id="lkpd-q2" rows="2" placeholder="Jelaskan sifat, kesukaan, dan kebiasaan dirimu yang cocok dengan tipe tersebut..." class="w-full text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500"></textarea>
                    </div>

                    <div class="bg-white p-4 rounded-2xl border border-blue-100 shadow-2xs">
                        <label class="block text-xs font-bold text-slate-800 mb-1.5">
                            3. Profesi yang sesuai dengan minat dan kepribadian saya:
                        </label>
                        <input type="text" id="lkpd-q3" placeholder="Contoh: Insinyur Robotik, Dokter, Arsitek, atau Peneliti Sains..." class="w-full text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>

                    <div class="bg-white p-4 rounded-2xl border border-blue-100 shadow-2xs">
                        <label class="block text-xs font-bold text-slate-800 mb-1.5">
                            4. Mengapa saya tertarik dengan profesi tersebut?
                        </label>
                        <textarea id="lkpd-q4" rows="2" placeholder="Uraikan alasan mendasar dan impianmu mengenai profesi ini..." class="w-full text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500"></textarea>
                    </div>

                    <div class="bg-white p-4 rounded-2xl border border-blue-100 shadow-2xs">
                        <label class="block text-xs font-bold text-slate-800 mb-1.5">
                            5. Kemampuan atau keterampilan yang perlu saya kembangkan:
                        </label>
                        <textarea id="lkpd-q5" rows="2" placeholder="Contoh: Kemampuan analisis logika, ketelitian teknis, atau kemampuan bahasa asing..." class="w-full text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500"></textarea>
                    </div>

                    <div class="bg-white p-4 rounded-2xl border border-blue-100 shadow-2xs">
                        <label class="block text-xs font-bold text-slate-800 mb-1.5">
                            6. Apa langkah nyata yang dapat saya lakukan mulai sekarang?
                        </label>
                        <div class="grid grid-cols-1 sm:grid-cols-3 gap-2">
                            <input type="text" id="lkpd-q6a" placeholder="Langkah 1: giat belajar" class="text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                            <input type="text" id="lkpd-q6b" placeholder="Langkah 2: aktif kegiatan positif" class="text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                            <input type="text" id="lkpd-q6c" placeholder="Langkah 3: melatih bakat" class="text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                        </div>
                    </div>

                    <div class="bg-gradient-to-r from-blue-50 to-indigo-50 p-4 rounded-2xl border border-blue-200">
                        <label class="block text-xs font-bold text-blue-950 mb-1.5">
                            7. Pernyataan Komitmen Rencana Masa Depan Saya:
                        </label>
                        <div class="space-y-2 text-xs font-semibold text-blue-900">
                            <div class="flex flex-wrap items-center gap-2">
                                <span>"Untuk mempersiapkan diri menuju profesi</span>
                                <input type="text" id="lkpd-profesi-target" placeholder="[tulis profesi impianmu]" class="px-2.5 py-1 bg-white border border-blue-300 rounded-lg text-blue-900 font-bold grow max-w-xs focus:ring-2 focus:ring-blue-500">
                                <span>, saya berkomitmen untuk:</span>
                            </div>
                            <textarea id="lkpd-komitmen" rows="2" placeholder="tuliskan komitmen belajarmu dengan sungguh-sungguh..." class="w-full text-xs p-2.5 bg-white border border-blue-300 rounded-xl focus:ring-2 focus:ring-blue-500"></textarea>
                        </div>
                    </div>

                </form>

                <!-- TTD LKPD -->
                <div class="mt-8 pt-6 border-t border-slate-200 flex justify-between items-end text-xs text-slate-700">
                    <div>
                        <p class="text-[11px] text-slate-500">Siswa yang Mengisi,</p>
                        <!-- Ruang kosong untuk tanda tangan manual siswa -->
                        <div class="h-20 flex items-end">
                            <span id="lkpd-signature-nama" class="text-xs font-bold text-slate-800 underline">[Nama Siswa]</span>
                        </div>
                    </div>
                    <div class="text-right space-y-1">
                        <p id="lkpd-tanggal">Cilegon, 18 September 2026</p>
                        <p class="font-medium text-slate-600">Mengetahui Guru BK,</p>
                        <!-- Ruang kosong untuk tanda tangan manual guru BK -->
                        <div class="h-20 my-0.5"></div>
                        <p class="font-bold text-slate-900 underline">Isnani Akmilatir Rosyida, S.Sos</p>
                        <p class="text-[11px] text-slate-600">NIP. 200104012025212014</p>
                    </div>
                </div>

                <!-- Action Controls LKPD -->
                <div class="flex flex-wrap items-center justify-between gap-3 pt-5 border-t border-slate-100 no-print">
                    <button onclick="simpanLkpdLocal()" class="px-4 py-2.5 bg-blue-50 hover:bg-blue-100 text-blue-700 text-xs font-bold rounded-xl transition flex items-center gap-1.5">
                        <span>💾 Simpan Draf LKPD</span>
                    </button>
                    
                    <div class="flex items-center gap-2">
                        <button onclick="cetakDokumen('lkpd')" class="px-5 py-2.5 bg-blue-900 hover:bg-slate-900 text-white text-xs font-bold rounded-xl shadow-md transition scale-bounce flex items-center gap-1.5">
                            <span>🖨️ Cetak / Unduh PDF LKPD</span>
                        </button>
                        <button onclick="navigateTo('refleksi')" class="px-6 py-2.5 bg-blue-600 hover:bg-blue-700 text-white rounded-xl text-xs font-bold transition scale-bounce flex items-center gap-2">
                            <span>Lanjut ke Refleksi</span>
                            <span>➔</span>
                        </button>
                    </div>
                </div>

            </div>
        </section>

        <section id="sec-refleksi" class="content-section space-y-6">
            <div class="bg-white rounded-3xl p-6 sm:p-8 border border-blue-100 shadow-xs" id="refleksi-print-container">
                
                <div class="border-b-2 border-blue-900 pb-4 mb-6 text-center">
                    <h2 class="font-heading text-lg sm:text-2xl font-bold text-slate-900 uppercase tracking-wide">
                        LEMBAR REFLEKSI PEMBELAJARAN BK KARIER
                    </h2>
                    <p class="text-xs text-blue-900 font-semibold mt-1">
                        Mengenal Kepribadian Menurut John L. Holland • SMP Negeri 3 Cilegon
                    </p>
                </div>

                <!-- Identitas Siswa Refleksi -->
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 bg-blue-50/70 p-4 rounded-2xl border border-blue-200 mb-6">
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-1">Nama Siswa:</label>
                        <input type="text" id="ref-nama" placeholder="Tulis nama lengkap..." class="w-full text-xs font-semibold px-3 py-2 bg-white border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-1">Kelas / Tingkat:</label>
                        <input type="text" id="ref-kelas" placeholder="Tulis kelas..." class="w-full text-xs font-semibold px-3 py-2 bg-white border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                    </div>
                </div>

                <div class="space-y-5">
                    <!-- Emotikon Perasaan -->
                    <div class="bg-blue-50/50 p-5 rounded-2xl border border-blue-200">
                        <label class="block text-xs font-bold text-slate-800 mb-3 text-center sm:text-left">
                            Bagaimana perasaanmu setelah mengikuti kegiatan bimbingan klasikal hari ini?
                        </label>
                        <div class="grid grid-cols-2 sm:grid-cols-4 gap-3">
                            <button onclick="pilihEmot(this, 'Sangat Senang')" class="emot-btn p-3.5 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-300 flex flex-col items-center gap-1.5 transition scale-bounce">
                                <span class="text-3xl">😍</span>
                                <span class="text-xs font-bold text-slate-700">Sangat Senang</span>
                            </button>
                            <button onclick="pilihEmot(this, 'Senang')" class="emot-btn p-3.5 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-300 flex flex-col items-center gap-1.5 transition scale-bounce">
                                <span class="text-3xl">😊</span>
                                <span class="text-xs font-bold text-slate-700">Senang</span>
                            </button>
                            <button onclick="pilihEmot(this, 'Biasa Saja')" class="emot-btn p-3.5 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-300 flex flex-col items-center gap-1.5 transition scale-bounce">
                                <span class="text-3xl">😐</span>
                                <span class="text-xs font-bold text-slate-700">Biasa Saja</span>
                            </button>
                            <button onclick="pilihEmot(this, 'Masih Bingung')" class="emot-btn p-3.5 rounded-2xl border-2 border-slate-200 bg-white hover:border-blue-300 flex flex-col items-center gap-1.5 transition scale-bounce">
                                <span class="text-3xl">🤔</span>
                                <span class="text-xs font-bold text-slate-700">Masih Bingung</span>
                            </button>
                        </div>
                        <input type="hidden" id="ref-perasaan-val" value="">
                    </div>

                    <!-- 4 Pertanyaan Refleksi Siswa -->
                    <div class="space-y-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-800 mb-1">
                                🌟 1. Hari ini saya belajar bahwa:
                            </label>
                            <textarea id="ref-1" rows="2" placeholder="Tuliskan pemahaman utamamu tentang teori Holland & pengenalan diri..." class="w-full text-xs p-3 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500"></textarea>
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-slate-800 mb-1">
                                💡 2. Hal baru yang saya ketahui tentang potensi diri saya adalah:
                            </label>
                            <textarea id="ref-2" rows="2" placeholder="Tuliskan penemuan baru tentang minat atau kelebihanmu..." class="w-full text-xs p-3 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500"></textarea>
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-slate-800 mb-1">
                                🚀 3. Profesi yang paling ingin saya eksplorasi lebih dalam adalah:
                            </label>
                            <input type="text" id="ref-3" placeholder="Sebutkan profesi impianmu..." class="w-full text-xs p-2.5 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500">
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-slate-800 mb-1">
                                📌 4. Langkah pertama yang akan saya lakukan setelah bimbingan ini adalah:
                            </label>
                            <textarea id="ref-4" rows="2" placeholder="Tindakan nyata terdekat yang akan kamu kerjakan..." class="w-full text-xs p-3 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500"></textarea>
                        </div>
                    </div>

                    <!-- Signature Section for Print Refleksi -->
                    <div class="mt-8 pt-6 border-t border-slate-200 flex justify-between items-end text-xs text-slate-700">
                        <div>
                            <p class="text-[11px] text-slate-500">Tanda Tangan Siswa,</p>
                            <!-- Ruang kosong untuk tanda tangan manual siswa -->
                            <div class="h-20 flex items-end">
                                <span id="ref-signature-nama" class="text-xs font-bold text-slate-800 underline">[Nama Siswa]</span>
                            </div>
                        </div>
                        <div class="text-right space-y-1">
                            <p id="ref-tanggal">Cilegon, 18 September 2026</p>
                            <p class="font-medium text-slate-600">Guru Bimbingan dan Konseling,</p>
                            <!-- Ruang kosong untuk tanda tangan manual guru BK -->
                            <div class="h-20 my-0.5"></div>
                            <p class="font-bold text-slate-900 underline">Isnani Akmilatir Rosyida, S.Sos</p>
                            <p class="text-[11px] text-slate-600">NIP. 200104012025212014</p>
                        </div>
                    </div>

                    <!-- Submit & Print Refleksi -->
                    <div class="pt-4 flex flex-col sm:flex-row items-center justify-between gap-4 border-t border-slate-100 no-print">
                        <button onclick="cetakDokumen('refleksi')" class="px-5 py-2.5 bg-blue-900 hover:bg-slate-900 text-white rounded-xl text-xs font-bold transition scale-bounce flex items-center gap-1.5 shadow-sm">
                            <span>🖨️ Cetak / Unduh PDF Refleksi</span>
                        </button>
                        <div class="flex items-center gap-2">
                            <button onclick="kirimRefleksiDanBukaSertifikat()" class="px-7 py-3 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-bold text-xs sm:text-sm rounded-xl shadow-lg shadow-blue-600/20 transition scale-bounce flex items-center gap-2">
                                <span>Kirim Refleksi & Buka Sertifikat Resmi</span>
                                <span>🎓</span>
                            </button>
                        </div>
                    </div>

                </div>

            </div>
        </section>

        <section id="sec-sertifikat" class="content-section space-y-6">
            <div class="bg-white rounded-3xl p-4 sm:p-8 border border-blue-200 shadow-md">
                
                <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-3 mb-6 pb-4 border-b border-slate-100 no-print">
                    <div>
                        <h2 class="font-heading text-xl sm:text-2xl font-bold text-slate-800">Sertifikat Kelulusan Asesmen Karier</h2>
                        <p class="text-xs text-slate-500 mt-0.5">Dianugerahkan secara resmi atas keberhasilan menyelesaikan seluruh alur kegiatan Kompas Karier RIASEC.</p>
                    </div>
                    <div class="flex items-center gap-2">
                        <button onclick="cetakDokumen('sertifikat')" class="px-6 py-2.5 bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-600 hover:to-amber-700 text-white font-bold text-xs sm:text-sm rounded-xl shadow-md transition scale-bounce flex items-center gap-2">
                            <span>🖨️ Cetak / Unduh PDF Sertifikat</span>
                            <span>⭐</span>
                        </button>
                    </div>
                </div>

                <!-- CERTIFICATE FRAME (ELEGANT DESIGN) -->
                <div id="certificate-container" class="relative bg-[#FCFDFE] text-slate-900 border-8 border-double border-blue-800/70 rounded-3xl p-6 sm:p-12 shadow-xl mx-auto max-w-4xl overflow-hidden">
                    
                    <div class="absolute -top-12 -left-12 w-28 h-28 bg-blue-200/50 rounded-full blur-xl pointer-events-none"></div>
                    <div class="absolute -bottom-12 -right-12 w-28 h-28 bg-indigo-200/50 rounded-full blur-xl pointer-events-none"></div>
                    
                    <div class="text-center space-y-3 relative z-10">
                        <div class="inline-flex items-center gap-2 px-4 py-1 rounded-full border border-blue-300 bg-blue-50 text-blue-950 text-xs font-bold tracking-widest uppercase">
                            <span>SMP NEGERI 3 CILEGON • LAYANAN BIMBINGAN DAN KONSELING</span>
                        </div>

                        <h1 class="font-cert text-3xl sm:text-5xl font-bold tracking-wider text-slate-900 uppercase pt-2">
                            SERTIFIKAT PENGHARGAAN
                        </h1>
                        <p id="cert-nomor" class="text-xs sm:text-sm text-slate-500 tracking-widest uppercase font-semibold">
                            Nomor: BK-KOMPAS/RIASEC/2026/09
                        </p>

                        <div class="pt-2">
                            <p class="text-xs sm:text-sm text-slate-600 font-medium">Sertifikat ini dengan bangga dianugerahkan kepada:</p>
                            <h2 id="cert-student-name" class="font-heading text-2xl sm:text-4xl font-bold text-blue-900 underline decoration-amber-400 decoration-2 underline-offset-8 mt-2">
                                [Nama Peserta Didik]
                            </h2>
                            <p id="cert-student-class" class="text-xs sm:text-sm text-slate-600 font-semibold mt-3">
                                Kelas: - • SMP Negeri 3 Cilegon
                            </p>
                        </div>

                        <div class="max-w-2xl mx-auto py-3">
                            <p class="text-xs sm:text-sm text-slate-700 leading-relaxed">
                                Atas partisipasi aktif dan keberhasilan menyelesaikan <strong>Asesmen Eksplorasi Minat & Kepribadian Karier</strong> berdasarkan teori John L. Holland dengan perolehan kombinasi 3 Kode Holland utama:
                            </p>
                            <div class="inline-block my-2 px-6 py-2 bg-blue-50 border-2 border-blue-200 rounded-2xl">
                                <span id="cert-holland-code" class="font-heading text-xl sm:text-2xl font-bold text-blue-800 tracking-widest">
                                    R - I - A
                                </span>
                            </div>
                            <p id="cert-holland-tag" class="text-xs font-bold text-slate-700">
                                Profil Dominan: Realistic (Realistik) - Si Praktis & Teknik
                            </p>
                        </div>

                        <!-- Tanda Tangan & Cap Guru BK -->
                        <div class="pt-6 flex justify-between items-end text-xs text-slate-800 max-w-2xl mx-auto">
                            
                            <div class="text-left flex flex-col items-center">
                                <div class="w-20 h-20 rounded-full border-2 border-dashed border-blue-600 bg-blue-50/70 flex flex-col items-center justify-center text-center p-1 shadow-xs">
                                    <span class="text-xl">🏆</span>
                                    <span class="text-[8px] font-bold text-blue-950 tracking-tight leading-tight">KOMPAS KARIER RIASEC</span>
                                </div>
                                <span class="text-[10px] text-slate-400 font-bold mt-1">Verifikasi Sah</span>
                            </div>

                            <div class="text-right space-y-1">
                                <p id="cert-tanggal" class="text-xs text-slate-600">Cilegon, 18 September 2026</p>
                                <p class="text-xs font-semibold text-slate-700">Guru Bimbingan dan Konseling,</p>
                                
                                <!-- Ruang kosong untuk tanda tangan manual guru BK -->
                                <div class="h-20 my-0.5"></div>

                                <p class="font-bold text-slate-900 text-xs sm:text-sm underline">
                                    Isnani Akmilatir Rosyida, S.Sos
                                </p>
                                <p class="text-[11px] text-slate-600 font-medium">
                                    NIP. 200104012025212014
                                </p>
                            </div>

                        </div>

                    </div>
                </div>

            </div>
        </section>

    </main>

    <!-- Footer Instansi -->
    <footer class="no-print bg-white border-t border-blue-100 mt-12 py-6 text-center text-xs text-slate-500 space-y-1">
        <p class="font-bold text-slate-700">Kompas Karier RIASEC • SMP Negeri 3 Cilegon</p>
        <p>Dikembangkan oleh <strong>Isnani Akmilatir Rosyida, S.Sos</strong> (Guru Bimbingan dan Konseling - NIP. 200104012025212014)</p>
        <p class="text-[11px] text-slate-400">Pendidikan Bermutu • Karakter Kuat • Prestasi Hebat</p>
    </footer>

    <!-- Custom Modal Dialog (Pengganti alert) -->
    <div id="custom-modal" class="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-sm hidden items-center justify-center p-4 no-print">
        <div class="bg-white rounded-3xl p-6 max-w-sm w-full shadow-2xl border border-slate-100 text-center">
            <div id="modal-icon-container" class="w-14 h-14 rounded-full flex items-center justify-center mx-auto mb-4 text-2xl font-bold bg-blue-100 text-blue-600">
                ✨
            </div>
            <h3 id="modal-title" class="font-heading text-lg font-bold text-slate-800 mb-2">Informasi</h3>
            <p id="modal-message" class="text-xs text-slate-600 leading-relaxed mb-6 whitespace-pre-line">Keterangan pesan.</p>
            <button onclick="closeModal()" class="w-full py-2.5 rounded-xl bg-blue-600 hover:bg-blue-700 text-white text-xs font-bold shadow-md transition scale-bounce">
                Tutup / Mengerti
            </button>
        </div>
    </div>

    <script>
        // Data 36 Soal Standar Holland RIASEC (6 soal per dimensi)
        const QUESTIONS_DATA = [
            { id: 1, type: 'R', text: 'Saya senang memperbaiki, merakit, atau membongkar benda dengan tangan sendiri.' },
            { id: 2, type: 'R', text: 'Saya menikmati kegiatan yang menggunakan alat pertukangan, mesin, atau perangkat fisik.' },
            { id: 3, type: 'R', text: 'Saya lebih mudah belajar melalui praktik langsung daripada sekadar membaca teori.' },
            { id: 4, type: 'R', text: 'Saya tertarik pada pekerjaan yang aktif bergerak atau menggunakan fisik di luar ruangan.' },
            { id: 5, type: 'R', text: 'Saya senang mencari tahu mekanisme kerja suatu sistem mekanis atau elektronik.' },
            { id: 6, type: 'R', text: 'Saya tertarik pada profesi seperti teknisi, mekanik, polisi, pilot, atau insinyur fisik.' },
            
            { id: 7, type: 'I', text: 'Saya senang memecahkan teka-teki, soal logis, atau masalah ilmiah yang rumit.' },
            { id: 8, type: 'I', text: 'Saya suka meneliti alasan mendasar di balik suatu fenomena atau kejadian alam.' },
            { id: 9, type: 'I', text: 'Saya menikmati kegiatan eksperimen ilmiah, riset fakta, dan analisis data.' },
            { id: 10, type: 'I', text: 'Saya tertarik menganalisis grafik, statistik, rumus, atau laporan ilmiah.' },
            { id: 11, type: 'I', text: 'Saya suka mencoba berbagai metode hipotetis untuk menemukan solusi paling efisien.' },
            { id: 12, type: 'I', text: 'Saya tertarik pada profesi seperti peneliti sains, dokter, analis data, atau programmer.' },
            
            { id: 13, type: 'A', text: 'Saya senang menggambar, mendesain grafis, membuat lagu, atau menulis karya kreatif.' },
            { id: 14, type: 'A', text: 'Saya suka mengekspresikan gagasan dan imajinasi menjadi bentuk karya seni nyata.' },
            { id: 15, type: 'A', text: 'Saya menyukai fleksibilitas dan kebebasan mengekspresikan diri tanpa aturan kaku.' },
            { id: 16, type: 'A', text: 'Saya peka terhadap keindahan warna, komposisi visual, nada musik, atau pentas drama.' },
            { id: 17, type: 'A', text: 'Saya merasa bergairah saat ditantang membuat karya orisinal dan out-of-the-box.' },
            { id: 18, type: 'A', text: 'Saya tertarik pada profesi seperti desainer, penulis cerita, seniman, arsitek, atau musisi.' },
            
            { id: 19, type: 'S', text: 'Saya senang mendengarkan curhat dan membantu teman yang sedang menghadapi kesulitan.' },
            { id: 20, type: 'S', text: 'Saya sangat nyaman berinteraksi, berkomunikasi hangat, dan bekerja sama dalam tim.' },
            { id: 21, type: 'S', text: 'Saya menikmati menjelaskan materi pelajaran agar orang lain menjadi paham.' },
            { id: 22, type: 'S', text: 'Saya merasa bahagia ketika berhasil membuat orang lain merasa terbantu dan dihargai.' },
            { id: 23, type: 'S', text: 'Saya tertarik pada kegiatan kepedulian sosial, mengajar, atau pelayanan medis.' },
            { id: 24, type: 'S', text: 'Saya tertarik pada profesi seperti guru, konselor BK, psikolog, perawat, atau pekerja sosial.' },
            
            { id: 25, type: 'E', text: 'Saya senang memimpin rapat, diskusi kelompok, atau mengorganisir suatu kegiatan.' },
            { id: 26, type: 'E', text: 'Saya percaya diri menyampaikan gagasan untuk memengaruhi atau meyakinkan orang lain.' },
            { id: 27, type: 'E', text: 'Saya tidak ragu mengambil keputusan penting dalam situasi penuh tantangan.' },
            { id: 28, type: 'E', text: 'Saya senang menyusun strategi dan target untuk meraih keuntungan/prestasi sukses.' },
            { id: 29, type: 'E', text: 'Saya tertarik pada dunia bisnis, negosiasi, kewirausahaan, atau promosi penjualan.' },
            { id: 30, type: 'E', text: 'Saya tertarik pada profesi seperti pengusaha, manajer marketing, pengacara, atau diplomat.' },
            
            { id: 31, type: 'C', text: 'Saya senang menyusun jadwal, daftar tugas, atau catatan dokumen dengan sangat rapi.' },
            { id: 32, type: 'C', text: 'Saya sangat teliti dan jeli ketika memeriksa detail angka atau input data laporan.' },
            { id: 33, type: 'C', text: 'Saya merasa nyaman mengikuti prosedur baku dan aturan kerja yang jelas.' },
            { id: 34, type: 'C', text: 'Saya suka mengelompokkan, mengarsipkan, dan mengelola informasi secara sistematis.' },
            { id: 35, type: 'C', text: 'Saya menikmati pekerjaan yang membutuhkan keteraturan, kepastian, dan keakuratan.' },
            { id: 36, type: 'C', text: 'Saya tertarik pada profesi seperti akuntan, sekretaris, staf administrasi, atau auditor.' }
        ];

        // Deskripsi, Profesi & Jalur Studi tiap Dimensi Holland
        const TIPE_DESCRIPTIONS = {
            R: {
                title: 'Realistic (Realistik)',
                tag: 'Si Praktis & Teknik',
                avatar: '👷‍♂️',
                desc: 'Menyukai hal konkret, alat mekanik, teknologi fisik, serta aktivitas aktif di lapangan.',
                profesi: ['Teknisi Otomotif', 'Insinyur Mesin & Robotik', 'Arsitek Bangunan', 'Pilot Penerbangan', 'Polisi / Militer', 'Ahli Konstruksi Sipil'],
                jurusanSMK: 'Teknik Kendaraan Ringan (TKR), Mekatronika, Teknik Mesin, Desain Pemodelan Bangunan.',
                jurusanKuliah: 'Teknik Mesin, Teknik Sipil, Penerbangan/Kedirgantaraan, Ilmu Kelautan & Perikanan.'
            },
            I: {
                title: 'Investigative (Investigatif)',
                tag: 'Si Peneliti & Logis',
                avatar: '🔬',
                desc: 'Senang memecahkan misteri ilmiah, riset data, berpikir kritis analitis, dan logika sains.',
                profesi: ['Dokter Spesialis', 'Peneliti Sains / Ilmuwan', 'Software Programmer', 'Data Scientist', 'Apoteker / Farmasis', 'Analis Medis'],
                jurusanSMK: 'Kimia Industri, Rekayasa Perangkat Lunak (RPL), Farmasi Klinis.',
                jurusanKuliah: 'Kedokteran Umum/Gigi, Teknik Informatika & Ilmu Komputer, Farmasi, Bioteknologi, Matematika Murni.'
            },
            A: {
                title: 'Artistic (Artistik)',
                tag: 'Si Kreatif & Ekspresif',
                avatar: '🎨',
                desc: 'Menyukai kebebasan imajinasi, mengekspresikan ide menjadi seni grafis, tulisan cerita, dan desain unik.',
                profesi: ['Desainer Grafis / UI-UX', 'Animator 3D', 'Content Creator', 'Penulis / Novelis', 'Fotografer & Videografer', 'Komposer Musik'],
                jurusanSMK: 'Desain Komunikasi Visual (DKV), Animasi, Seni Kriya, Produksi Siaran & Film.',
                jurusanKuliah: 'Desain Komunikasi Visual, Seni Rupa Murni, Desain Produk, Sastra & Penulisan Kreatif, Perfilman.'
            },
            S: {
                title: 'Social (Sosial)',
                tag: 'Si Penolong & Edukator',
                avatar: '🤝',
                desc: 'Senang membantu sesama, membimbing, berempati tinggi, dan berkomunikasi ramah dalam kerja tim.',
                profesi: ['Guru Pendidik', 'Konselor BK Remaja', 'Psikolog Klinis', 'Perawat Kesehatan', 'Pekerja Sosial', 'Trainer HRD'],
                jurusanSMK: 'Asisten Keperawatan, Layanan Kesehatan Masyarakat, Pekerjaan Sosial.',
                jurusanKuliah: 'Bimbingan & Konseling (BK), Psikologi, Ilmu Pendidikan/Keguruan, Ilmu Keperawatan, Kesejahteraan Sosial.'
            },
            E: {
                title: 'Enterprising (Kewirausahaan)',
                tag: 'Si Pemimpin & Bisnis',
                avatar: '🦁',
                desc: 'Percaya diri memimpin, senang bernegosiasi bisnis, berani mengambil risiko, dan persuasif.',
                profesi: ['Wirausahawan / Founder Bisnis', 'Manajer Pemasaran', 'Direktur Perusahaan', 'Pengacara', 'Konsultan Bisnis', 'Diplomat'],
                jurusanSMK: 'Bisnis Daring & Pemasaran (BDP), Retail Bisnis, Manajemen Logistik.',
                jurusanKuliah: 'Manajemen Bisnis, Kewirausahaan, Ilmu Hukum, Hubungan Internasional, Marketing Digital.'
            },
            C: {
                title: 'Conventional (Konvensional)',
                tag: 'Si Teratur & Detail',
                avatar: '🐧',
                desc: 'Menyukai keteraturan rapi, teliti memeriksa data/angka, taat aturan, dan menyusun arsip dokumen.',
                profesi: ['Akuntan Publik', 'Staf Administrasi Eksekutif', 'Auditor Keuangan', 'Sekretaris', 'Banker / Teller', 'Pengelola Database'],
                jurusanSMK: 'Akuntansi & Keuangan Lembaga (AKL), Otomatisasi & Tata Kelola Perkantoran (OTKP).',
                jurusanKuliah: 'Akuntansi, Manajemen Keuangan, Perbankan Syariah/Konvensional, Administrasi Bisnis, Ilmu Kearsipan.'
            }
        };

        // State Aplikasi
        let currentMateriIdx = 0;
        let studentData = { name: '', class: '', school: 'SMP Negeri 3 Cilegon' };
        let testAnswers = {};
        let currentQuestionIdx = 0;
        let selectedFeeling = '';
        let isWorkflowCompleted = false;

        // Fungsi Format Tanggal Dinamis Sesuai Waktu Pengisian
        function getTanggalHariIni() {
            const today = new Date();
            const months = [
                'Januari', 'Februari', 'Maret', 'April', 'Mei', 'Juni',
                'Juli', 'Agustus', 'September', 'Oktober', 'November', 'Desember'
            ];
            return `Cilegon, ${today.getDate()} ${months[today.getMonth()]} ${today.getFullYear()}`;
        }

        // Sinkronisasi Tanggal ke Seluruh Dokumen (Hasil Tes, LKPD, Refleksi, Sertifikat)
        function updateDynamicDates() {
            const tanggalAktif = getTanggalHariIni();
            const now = new Date();
            const mm = String(now.getMonth() + 1).padStart(2, '0');
            const yyyy = now.getFullYear();

            const elHasil = document.getElementById('hasil-tes-tanggal');
            if (elHasil) elHasil.innerText = tanggalAktif;

            const elLkpd = document.getElementById('lkpd-tanggal');
            if (elLkpd) elLkpd.innerText = tanggalAktif;

            const elRef = document.getElementById('ref-tanggal');
            if (elRef) elRef.innerText = tanggalAktif;

            const elCert = document.getElementById('cert-tanggal');
            if (elCert) elCert.innerText = tanggalAktif;

            const elCertNo = document.getElementById('cert-nomor');
            if (elCertNo) elCertNo.innerText = `Nomor: BK-KOMPAS/RIASEC/${yyyy}/${mm}`;
        }

        // Navigasi Section Utama
        function navigateTo(sectionId) {
            try {
                const sections = document.querySelectorAll('.content-section');
                sections.forEach(sec => {
                    sec.classList.remove('active');
                    sec.style.display = 'none';
                });

                const activeSec = document.getElementById('sec-' + sectionId);
                if (activeSec) {
                    activeSec.classList.add('active');
                    activeSec.style.display = 'block';
                }

                const navButtons = document.querySelectorAll('.nav-btn');
                navButtons.forEach(btn => {
                    if (btn.id !== 'nav-sertifikat') {
                        btn.classList.remove('bg-blue-600', 'text-white', 'shadow-xs');
                        btn.classList.add('text-slate-600');
                    }
                });

                const activeNav = document.getElementById('nav-' + sectionId);
                if (activeNav && sectionId !== 'sertifikat') {
                    activeNav.classList.add('bg-blue-600', 'text-white', 'shadow-xs');
                    activeNav.classList.remove('text-slate-600');
                }

                window.scrollTo({ top: 0, behavior: 'smooth' });
            } catch (err) {
                console.warn("Navigasi error:", err);
            }
        }

        // Kontrol Slide Materi
        function bukaMateriSlide(index) {
            currentMateriIdx = index;
            const slides = document.querySelectorAll('.materi-slide');
            const pills = document.querySelectorAll('.materi-pill');

            slides.forEach((s, idx) => {
                if (idx === index) {
                    s.classList.add('active');
                } else {
                    s.classList.remove('active');
                }
            });

            pills.forEach((p, idx) => {
                if (idx === index) {
                    p.classList.remove('text-slate-600', 'bg-transparent');
                    p.classList.add('bg-blue-600', 'text-white', 'shadow-xs');
                } else {
                    p.classList.remove('bg-blue-600', 'text-white', 'shadow-xs');
                    p.classList.add('text-slate-600');
                }
            });

            document.getElementById('materi-page-indicator').innerText = `Tipe ${index + 1} dari 6`;
            
            const btnPrev = document.getElementById('btn-materi-prev');
            const btnNext = document.getElementById('btn-materi-next');
            if (btnPrev && btnNext) {
                btnPrev.disabled = index === 0;
                btnPrev.classList.toggle('opacity-50', index === 0);
                btnNext.disabled = index === 5;
                btnNext.classList.toggle('opacity-50', index === 5);
            }
        }

        function geserMateri(step) {
            const nextIdx = currentMateriIdx + step;
            if (nextIdx >= 0 && nextIdx < 6) {
                bukaMateriSlide(nextIdx);
            }
        }

        // Buka Sertifikat dengan validasi alur
        function bukaSertifikatDenganKunci() {
            if (!isWorkflowCompleted) {
                showModal(
                    'Sertifikat Masih Terkunci 🔒',
                    'Sertifikat resmi hanya dapat dibuka setelah kamu menyelesaikan seluruh alur:\n\n1. Tes Kepribadian Holland (36 butir soal)\n2. Pengisian LKPD Digital\n3. Pengiriman Lembar Refleksi Pembelajaran\n\nYuk selesaikan alurnya terlebih dahulu!',
                    'warning'
                );
                return;
            }
            navigateTo('sertifikat');
        }

        // Mulai Tes Asesmen Mandiri
        function mulaiKuis() {
            const nama = document.getElementById('tes-input-nama').value.trim();
            const kelas = document.getElementById('tes-input-kelas').value.trim();
            const sekolah = document.getElementById('tes-input-sekolah').value.trim() || 'SMP Negeri 3 Cilegon';

            if (!nama || !kelas) {
                showModal('Lengkapi Data Siswa', 'Silakan isi Nama Lengkap dan Kelas terlebih dahulu sebelum memulai tes.', 'warning');
                return;
            }

            studentData = { name: nama, class: kelas, school: sekolah };
            document.getElementById('tes-nama-display').innerText = `Siswa: ${nama} (${kelas})`;

            // Sinkronkan ke LKPD & Refleksi
            document.getElementById('lkpd-nama').value = nama;
            document.getElementById('lkpd-kelas').value = kelas;
            document.getElementById('lkpd-signature-nama').innerText = nama;
            document.getElementById('ref-nama').value = nama;
            document.getElementById('ref-kelas').value = kelas;
            document.getElementById('ref-signature-nama').innerText = nama;

            document.getElementById('tes-view-identitas').classList.add('hidden');
            document.getElementById('tes-view-kuis').classList.remove('hidden');
            document.getElementById('tes-view-hasil').classList.add('hidden');

            renderNomorGrid();
            renderQuestion(0);
        }

        // Render Selector Nomor Soal 1-36
        function renderNomorGrid() {
            const grid = document.getElementById('tes-nomor-grid');
            grid.innerHTML = '';
            QUESTIONS_DATA.forEach((q, idx) => {
                const btn = document.createElement('button');
                btn.id = `grid-no-${idx}`;
                btn.innerText = idx + 1;
                btn.className = `py-1 text-[10px] font-bold rounded-lg border transition ${
                    testAnswers[q.id] 
                        ? 'bg-blue-100 text-blue-800 border-blue-300' 
                        : 'bg-white text-slate-600 border-slate-200 hover:bg-slate-100'
                }`;
                btn.onclick = () => renderQuestion(idx);
                grid.appendChild(btn);
            });
        }

        // Render Soal Aktif
        function renderQuestion(index) {
            currentQuestionIdx = index;
            const q = QUESTIONS_DATA[index];

            document.getElementById('tes-soal-progress').innerText = `Soal ${index + 1} dari 36`;
            document.getElementById('tes-badge-no').innerText = `#${index + 1}`;
            document.getElementById('tes-soal-text').innerText = `"${q.text}"`;

            const pct = Math.round(((index + 1) / QUESTIONS_DATA.length) * 100);
            document.getElementById('tes-progress-fill').style.width = `${pct}%`;

            const info = TIPE_DESCRIPTIONS[q.type];
            const badgeTipe = document.getElementById('tes-badge-tipe');
            badgeTipe.innerText = `Tipe ${q.type} - ${info.tag}`;

            document.querySelectorAll('.scale-btn').forEach(b => {
                b.classList.remove('border-blue-600', 'bg-blue-50', 'ring-2', 'ring-blue-400');
                b.classList.add('border-slate-200', 'bg-white');
            });

            const savedScore = testAnswers[q.id];
            if (savedScore) {
                const activeBtn = document.getElementById(`btn-skor-${savedScore}`);
                if (activeBtn) {
                    activeBtn.classList.remove('border-slate-200', 'bg-white');
                    activeBtn.classList.add('border-blue-600', 'bg-blue-50', 'ring-2', 'ring-blue-400');
                }
            }

            const answeredCount = Object.keys(testAnswers).length;
            document.getElementById('tes-terjawab-counter').innerText = `${answeredCount} / 36 Terjawab`;

            document.querySelectorAll('#tes-nomor-grid button').forEach((btn, idx) => {
                btn.classList.remove('ring-2', 'ring-blue-600');
                if (idx === index) {
                    btn.classList.add('ring-2', 'ring-blue-600');
                }
            });
        }

        // Pemilihan Skor 1 - 5
        function pilihSkor(score) {
            const q = QUESTIONS_DATA[currentQuestionIdx];
            testAnswers[q.id] = score;

            document.querySelectorAll('.scale-btn').forEach(b => {
                b.classList.remove('border-blue-600', 'bg-blue-50', 'ring-2', 'ring-blue-400');
                b.classList.add('border-slate-200', 'bg-white');
            });
            const activeBtn = document.getElementById(`btn-skor-${score}`);
            if (activeBtn) {
                activeBtn.classList.remove('border-slate-200', 'bg-white');
                activeBtn.classList.add('border-blue-600', 'bg-blue-50', 'ring-2', 'ring-blue-400');
            }

            const gridBtn = document.getElementById(`grid-no-${currentQuestionIdx}`);
            if (gridBtn) {
                gridBtn.className = 'py-1 text-[10px] font-bold rounded-lg border transition bg-blue-100 text-blue-800 border-blue-300 ring-2 ring-blue-600';
            }

            if (currentQuestionIdx < QUESTIONS_DATA.length - 1) {
                setTimeout(() => {
                    renderQuestion(currentQuestionIdx + 1);
                }, 160);
            }
        }

        function prevSoal() {
            if (currentQuestionIdx > 0) renderQuestion(currentQuestionIdx - 1);
        }

        function nextSoal() {
            if (currentQuestionIdx < QUESTIONS_DATA.length - 1) renderQuestion(currentQuestionIdx + 1);
        }

        function selesaikanTes() {
            const answeredCount = Object.keys(testAnswers).length;
            if (answeredCount < 36) {
                showModal(
                    'Soal Belum Lengkap', 
                    `Kamu baru menjawab ${answeredCount} dari 36 butir soal. Silakan lengkapi semua soal agar hasil kompas kepribadianmu akurat!`, 
                    'warning'
                );
                return;
            }

            const scores = { R: 0, I: 0, A: 0, S: 0, E: 0, C: 0 };
            QUESTIONS_DATA.forEach(q => {
                scores[q.type] += (testAnswers[q.id] || 0);
            });

            const sortedTypes = Object.keys(scores).map(code => ({
                code: code,
                score: scores[code],
                ...TIPE_DESCRIPTIONS[code]
            })).sort((a, b) => b.score - a.score);

            const top3Code = sortedTypes.slice(0, 3).map(t => t.code).join(' - ');

            document.getElementById('hasil-nama-siswa').innerText = studentData.name;
            document.getElementById('hasil-meta-siswa').innerText = `Kelas: ${studentData.class} • ${studentData.school}`;
            document.getElementById('hasil-kode-holland').innerText = top3Code;

            const dominan = sortedTypes[0];
            document.getElementById('hasil-avatar-dominan').innerText = dominan.avatar;
            document.getElementById('hasil-tipe-judul').innerText = `${dominan.title} (${dominan.tag})`;
            document.getElementById('hasil-tipe-desc').innerText = dominan.desc;

            // Render Dinamis: Rekomendasi Profesi & Rekomendasi Jurusan Sekolah/Kuliah
            const rekomendasiGrid = document.getElementById('hasil-rekomendasi-grid');
            rekomendasiGrid.innerHTML = '';

            sortedTypes.slice(0, 3).forEach((item, idx) => {
                const priorityLabels = ['Prioritas #1 (Dominan Utama)', 'Prioritas #2 (Pendukung Kuat)', 'Prioritas #3 (Potensi Tambahan)'];
                const card = document.createElement('div');
                card.className = 'bg-blue-50/60 p-4 sm:p-5 rounded-2xl border border-blue-200/90 shadow-2xs space-y-3';
                card.innerHTML = `
                    <div class="flex items-center justify-between border-b border-blue-100 pb-2">
                        <div class="flex items-center gap-2">
                            <span class="text-2xl">${item.avatar}</span>
                            <div>
                                <h4 class="font-heading text-sm font-bold text-blue-950">${item.title}</h4>
                                <span class="text-[10px] text-blue-700 font-bold uppercase">${priorityLabels[idx]}</span>
                            </div>
                        </div>
                        <span class="bg-blue-600 text-white font-bold text-xs px-2.5 py-0.5 rounded-full">Kode ${item.code}</span>
                    </div>

                    <div>
                        <span class="text-xs font-bold text-slate-800 flex items-center gap-1.5 mb-1.5">
                            <span>💼</span> Profesi Ideal yang Sesuai:
                        </span>
                        <div class="flex flex-wrap gap-1.5">
                            ${item.profesi.map(p => `<span class="text-[11px] bg-white border border-blue-200 text-blue-900 font-semibold px-2 py-0.5 rounded-lg shadow-2xs">${p}</span>`).join('')}
                        </div>
                    </div>

                    <div class="bg-white p-3 rounded-xl border border-blue-100 space-y-1 text-xs">
                        <span class="font-bold text-slate-800 flex items-center gap-1">
                            <span>🎓</span> Pilihan Jurusan Sekolah & Kuliah:
                        </span>
                        <p class="text-[11px] text-slate-600 leading-relaxed">
                            <strong class="text-blue-950">SMK:</strong> ${item.jurusanSMK}
                        </p>
                        <p class="text-[11px] text-slate-600 leading-relaxed">
                            <strong class="text-blue-950">Kuliah (S1/D4):</strong> ${item.jurusanKuliah}
                        </p>
                    </div>
                `;
                rekomendasiGrid.appendChild(card);
            });

            // Render Bar Skor 6 Dimensi
            const barContainer = document.getElementById('hasil-skor-bars');
            barContainer.innerHTML = '';
            sortedTypes.forEach((t, i) => {
                const pct = Math.round((t.score / 30) * 100);
                const barRow = document.createElement('div');
                barRow.className = 'bg-blue-50/50 p-2.5 rounded-xl border border-blue-100';
                barRow.innerHTML = `
                    <div class="flex justify-between items-center mb-1">
                        <span class="text-slate-700">#${i + 1} <strong>${t.code}</strong> - ${t.title}</span>
                        <span class="text-blue-800 font-bold">${t.score}/30 Poin (${pct}%)</span>
                    </div>
                    <div class="w-full bg-slate-200 h-2 rounded-full overflow-hidden">
                        <div class="bg-blue-600 h-full rounded-full" style="width: ${pct}%"></div>
                    </div>
                `;
                barContainer.appendChild(barRow);
            });

            // Sinkronkan ke Data Sertifikat
            document.getElementById('cert-student-name').innerText = studentData.name;
            document.getElementById('cert-student-class').innerText = `Kelas: ${studentData.class} • ${studentData.school}`;
            document.getElementById('cert-holland-code').innerText = top3Code;
            document.getElementById('cert-holland-tag').innerText = `Profil Dominan: ${dominan.title} - ${dominan.tag}`;

            document.getElementById('tes-view-kuis').classList.add('hidden');
            document.getElementById('tes-view-hasil').classList.remove('hidden');

            updateDynamicDates();

            showModal('Tes Selesai! 🎉', `Selamat ${studentData.name}, 3 kode kepribadian Holland kamu adalah ${top3Code}.\n\nRekomendasi profesi dan jurusan pendidikan telah tersusun di lembar hasil tesmu!`, 'success');
        }

        // Salin ke LKPD Digital
        function salinKeLkpd() {
            const kode = document.getElementById('hasil-kode-holland').innerText;
            document.getElementById('lkpd-nama').value = studentData.name;
            document.getElementById('lkpd-kelas').value = studentData.class;
            document.getElementById('lkpd-kode').value = kode;
            document.getElementById('lkpd-q1').value = kode;
            document.getElementById('lkpd-signature-nama').innerText = studentData.name || '[Nama Siswa]';

            navigateTo('lkpd');
            showModal('Tersalin ke LKPD ✨', 'Identitas dan hasil kode tes RIASEC sudah otomatis masuk ke LKPD digitalmu. Silakan lengkapi rencana masa depanmu!', 'success');
        }

        // Fungsi Cetak Dokumen PDF
        function cetakDokumen(mode) {
            updateDynamicDates();
            const currentNama = studentData.name || document.getElementById('tes-input-nama').value.trim() || 'Peserta Didik';
            const currentKelas = studentData.class || document.getElementById('tes-input-kelas').value.trim() || '-';
            
            if (mode === 'lkpd') {
                document.getElementById('lkpd-signature-nama').innerText = document.getElementById('lkpd-nama').value || currentNama;
            } else if (mode === 'refleksi') {
                document.getElementById('ref-signature-nama').innerText = document.getElementById('ref-nama').value || currentNama;
            } else if (mode === 'sertifikat') {
                document.getElementById('cert-student-name').innerText = currentNama;
                document.getElementById('cert-student-class').innerText = `Kelas: ${currentKelas} • SMP Negeri 3 Cilegon`;
            }

            document.body.className = `print-mode-${mode}`;
            window.print();
            
            setTimeout(() => {
                document.body.className = 'min-h-screen flex flex-col selection:bg-blue-200 selection:text-blue-900';
            }, 800);
        }

        // Respon Pemantik Video
        function simpanPemantik() {
            const input = document.getElementById('jawaban-pemantik').value.trim();
            if (!input) {
                showModal('Catatan Kosong', 'Silakan ketikkan pandanganmu mengenai video yang telah ditonton.', 'warning');
                return;
            }
            const feedback = document.getElementById('pemantik-feedback');
            feedback.classList.remove('hidden');
            setTimeout(() => {
                feedback.classList.add('hidden');
            }, 3000);
        }

        // Emotikon Refleksi
        function pilihEmot(btn, feeling) {
            selectedFeeling = feeling;
            document.getElementById('ref-perasaan-val').value = feeling;
            document.querySelectorAll('.emot-btn').forEach(b => {
                b.classList.remove('border-blue-600', 'bg-blue-50', 'ring-2', 'ring-blue-400');
                b.classList.add('border-slate-200', 'bg-white');
            });
            btn.classList.remove('border-slate-200', 'bg-white');
            btn.classList.add('border-blue-600', 'bg-blue-50', 'ring-2', 'ring-blue-400');
        }

        // Simpan LKPD
        function simpanLkpdLocal() {
            const nama = document.getElementById('lkpd-nama').value.trim();
            const kelas = document.getElementById('lkpd-kelas').value.trim();
            if (!nama || !kelas) {
                showModal('Data Belum Lengkap', 'Mohon lengkapi Nama dan Kelas pada LKPD sebelum menyimpan.', 'warning');
                return;
            }
            showModal('Draf Tersimpan! 📝', `Draf LKPD milik ${nama} (${kelas}) berhasil disimpan.`, 'success');
        }

        // Kirim Refleksi & Buka Sertifikat
        function kirimRefleksiDanBukaSertifikat() {
            const nama = document.getElementById('ref-nama').value.trim() || studentData.name;
            const kelas = document.getElementById('ref-kelas').value.trim() || studentData.class;
            const r1 = document.getElementById('ref-1').value.trim();
            const r3 = document.getElementById('ref-3').value.trim();

            if (!nama || !kelas) {
                showModal('Identitas Diperlukan', 'Silakan isi Nama dan Kelas pada lembar refleksi.', 'warning');
                return;
            }
            if (!selectedFeeling) {
                showModal('Pilih Perasaanmu', 'Silakan pilih salah satu emotikon perasaan yang menggambarkan pengalaman belajarmu hari ini.', 'warning');
                return;
            }
            if (!r1 && !r3) {
                showModal('Lengkapi Refleksi', 'Silakan isi minimal hal yang kamu pelajari dan profesi impianmu.', 'warning');
                return;
            }

            studentData.name = nama;
            studentData.class = kelas;
            document.getElementById('ref-signature-nama').innerText = nama;
            document.getElementById('cert-student-name').innerText = nama;
            document.getElementById('cert-student-class').innerText = `Kelas: ${kelas} • SMP Negeri 3 Cilegon`;

            // Buka Akses Sertifikat Resmi
            isWorkflowCompleted = true;
            updateDynamicDates();
            const navCert = document.getElementById('nav-sertifikat');
            navCert.classList.remove('bg-blue-50/70', 'text-slate-400');
            navCert.classList.add('bg-amber-50', 'text-amber-800', 'border-amber-300', 'hover:bg-amber-100');
            document.getElementById('nav-cert-icon').innerText = '🎓';
            document.getElementById('nav-cert-text').innerText = 'Sertifikat (Terbuka)';

            showModal(
                'Selamat! Seluruh Alur Selesai 🎉', 
                `Terima kasih ${nama}! Refleksimu telah berhasil disimpan.\n\nSertifikat Resmi Kelulusan Asesmen Karier kini telah TERBUKA dan siap dicetak/diunduh sebagai PDF!`, 
                'success'
            );

            setTimeout(() => {
                navigateTo('sertifikat');
            }, 1200);
        }

        // Custom Modal UI
        function showModal(title, message, type = 'info') {
            const modal = document.getElementById('custom-modal');
            const modalTitle = document.getElementById('modal-title');
            const modalMsg = document.getElementById('modal-message');
            const iconContainer = document.getElementById('modal-icon-container');

            modalTitle.innerText = title;
            modalMsg.innerText = message;

            if (type === 'warning') {
                iconContainer.className = "w-14 h-14 rounded-full flex items-center justify-center mx-auto mb-4 text-2xl font-bold bg-amber-100 text-amber-600";
                iconContainer.innerText = '⚠️';
            } else if (type === 'success') {
                iconContainer.className = "w-14 h-14 rounded-full flex items-center justify-center mx-auto mb-4 text-2xl font-bold bg-blue-100 text-blue-600";
                iconContainer.innerText = '🌟';
            } else {
                iconContainer.className = "w-14 h-14 rounded-full flex items-center justify-center mx-auto mb-4 text-2xl font-bold bg-blue-100 text-blue-600";
                iconContainer.innerText = '✨';
            }

            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }

        function closeModal() {
            const modal = document.getElementById('custom-modal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        // Inisialisasi awal
        window.addEventListener('load', () => {
            updateDynamicDates();
            navigateTo('beranda');
            bukaMateriSlide(0);
        });
    </script>
</body>
</html>
