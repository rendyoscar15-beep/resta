<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VIRAL KINI - Video Berita Terupdate</title>
    <style>
        :root { --primary: #e11d48; --dark: #0f172a; --accent: #2563eb; }
        * { margin:0; padding:0; box-sizing:border-box; font-family: 'Segoe UI', sans-serif; }
        body { background: #f8fafc; color: #1e293b; line-height: 1.6; }

        /* Header & Ticker */
        .ticker { background: #000; color: #fff; padding: 8px 5%; font-size: 13px; font-weight: bold; }
        header { background: #fff; padding: 15px 5%; border-bottom: 3px solid var(--primary); display: flex; justify-content: space-between; box-shadow: 0 2px 10px rgba(0,0,0,0.1); sticky; top:0; z-index:100; }
        .logo { font-size: 24px; font-weight: 800; color: var(--primary); }

        /* Layout */
        .container { max-width: 1100px; margin: 20px auto; display: flex; flex-wrap: wrap; padding: 0 15px; gap: 20px; }
        main { flex: 2; min-width: 300px; }
        aside { flex: 1; min-width: 300px; }

        /* Video Box - Dioptimalkan untuk Doodstream */
        .video-box { background: #000; border-radius: 12px; overflow: hidden; position: relative; margin: 20px 0; box-shadow: 0 10px 30px rgba(0,0,0,0.3); }
        .iframe-wrapper { position: relative; padding-bottom: 56.25%; height: 0; }
        .iframe-wrapper iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none; }
        
        /* Adsterra Smartlink Overlay */
        .video-overlay { 
            position: absolute; top: 0; left: 0; width: 100%; height: 100%; 
            background: rgba(0,0,0,0.5) url('https://cdn-icons-png.flaticon.com/512/0/375.png') no-repeat center;
            background-size: 80px; z-index: 50; cursor: pointer; transition: 0.3s;
        }
        .video-overlay:hover { background-color: rgba(0,0,0,0.2); }

        /* Server Buttons */
        .server-list { display: flex; gap: 10px; margin-top: 10px; }
        .server-btn { background: #334155; color: white; padding: 8px 15px; border-radius: 5px; font-size: 12px; cursor: pointer; border: none; font-weight: bold; }
        .server-btn.active { background: var(--primary); }

        /* Article & Ads */
        .card { background: #fff; padding: 25px; border-radius: 12px; margin-bottom: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); }
        .ad-slot { width: 100%; text-align: center; margin: 15px 0; padding: 10px; background: #f1f5f9; border: 1px dashed #cbd5e1; border-radius: 8px; }
        .btn-smart { display: block; width: 100%; background: var(--accent); color: white; text-align: center; padding: 15px; border-radius: 8px; text-decoration: none; font-weight: bold; margin: 10px 0; }

        /* Sidebar Trending */
        .trending-item { display: flex; gap: 10px; margin-bottom: 15px; text-decoration: none; color: inherit; align-items: center; }
        .trending-item img { width: 90px; height: 60px; object-fit: cover; border-radius: 6px; }

        footer { background: #000; color: white; text-align: center; padding: 40px; margin-top: 40px; }
    </style>
</head>
<body>

    <!-- TEMPEL SCRIPT SOCIAL BAR ADSTERRA DI SINI -->

    <div class="ticker"><marquee>BREAKING NEWS: Berita Viral Hari Ini Terekam Kamera - Simak Video Selengkapnya!</marquee></div>

    <header>
        <div class="logo">VIRAL<span>KINI</span></div>
        <div style="color: var(--primary); font-weight: bold;">LIVE 🔴</div>
    </header>

    <div class="container">
        <main>
            <!-- IKLAN BANNER ATAS (728x90) -->
            <div class="ad-slot">
                <p>IKLAN BANNER 728x90</p>
                <!-- Tempel Kode Banner Adsterra Di Sini -->
            </div>

            <article class="card">
                <small style="color: var(--primary); font-weight: bold;">#VIRALHARIINI</small>
                <h1 style="margin: 10px 0; font-size: 26px;">Detik-detik Kejadian Viral yang Menghebohkan Jagat Maya</h1>
                
                <div class="video-box">
                    <!-- Overlay Smartlink -->
                    <div id="videoOverlay" class="video-overlay" onclick="openAdAndPlay()"></div>
                    
                    <div class="iframe-wrapper">
                        <!-- ID VIDEO DOODSTREAM: Ganti 'xxxxxx' dengan ID video Anda -->
                        <iframe id="mainPlayer" src="https://dood.to/e/xxxxxx" allowfullscreen scrolling="no"></iframe>
                    </div>
                </div>

                <div class="server-list">
                    <button class="server-btn active" onclick="changeServer('https://dood.to/e/xxxxxx', this)">Server 1</button>
                    <button class="server-btn" onclick="changeServer('https://streamwish.to/e/yyyyyy', this)">Server 2</button>
                    <button class="server-btn" onclick="window.open(SMARTLINK_URL)">Download HD</button>
                </div>

                <a href="URL_SMARTLINK_ANDA" target="_blank" class="btn-smart">KLIK UNTUK VIDEO FULL (TANPA SENSOR)</a>

                <div style="margin-top: 20px;">
                    <h3>Deskripsi Berita:</h3>
                    <p>Warga dihebohkan dengan rekaman video berdurasi 1 menit yang memperlihatkan aksi tidak terduga. Hingga saat ini video tersebut telah dibagikan lebih dari 10.000 kali di platform media sosial. Tim kami sedang menelusuri lokasi kejadian lebih lanjut...</p>
                </div>

                <!-- IKLAN NATIVE BANNER -->
                <div class="ad-slot" style="background: #fff; border: 1px solid #eee;">
                    <p>IKLAN NATIVE ADSTERRA</p>
                    <!-- Tempel Kode Native Banner Adsterra Di Sini -->
                </div>
            </article>
        </main>

        <aside>
            <div class="card">
                <h3 style="border-left: 4px solid var(--primary); padding-left: 10px; margin-bottom: 15px;">LAGI VIRAL</h3>
                
                <!-- Trending List -->
                <a href="#" onclick="window.open(SMARTLINK_URL)" class="trending-item">
                    <img src="https://via.placeholder.com/90x60" alt="v1">
                    <div>
                        <div style="font-size: 13px; font-weight: bold;">Kejadian di Tol Cipali KM 90...</div>
                        <small>2 jam yang lalu</small>
                    </div>
                </a>

                <a href="#" onclick="window.open(SMARTLINK_URL)" class="trending-item">
                    <img src="https://via.placeholder.com/90x60" alt="v2">
                    <div>
                        <div style="font-size: 13px; font-weight: bold;">Aksi Heroik Driver Ojol...</div>
                        <small>5 jam yang lalu</small>
                    </div>
                </a>

                <!-- IKLAN BANNER SIDEBAR -->
                <div class="ad-slot" style="min-height: 250px;">
                    <p>IKLAN BANNER 300x250</p>
                    <!-- Tempel Kode Banner 300x250 Di Sini -->
                </div>
            </div>
        </aside>
    </div>

    <footer>
        <p>&copy; 2024 ViralKini Media - Konten Viral Tercepat</p>
    </footer>

    <script>
        // CONFIG: Masukkan Smartlink Adsterra Anda di sini
        const SMARTLINK_URL = "https://www.highcpmgate.com/xxxxxx";

        function openAdAndPlay() {
            // 1. Buka Iklan Smartlink
            window.open(SMARTLINK_URL, '_blank');
            // 2. Hilangkan Overlay
            document.getElementById('videoOverlay').style.display = 'none';
        }

        function changeServer(url, btn) {
            // Ganti URL Video
            document.getElementById('mainPlayer').src = url;
            // Tampilkan kembali overlay untuk iklan baru
            document.getElementById('videoOverlay').style.display = 'flex';
            
            // Ubah UI Tombol
            let btns = document.getElementsByClassName('server-btn');
            for(let b of btns) b.classList.remove('active');
            btn.classList.add('active');
        }
    </script>

    <!-- TEMPEL SCRIPT POPUNDER ADSTERRA DI SINI (SEBELUM TAG /BODY) -->

</body>
</html>
