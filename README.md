# Diodepttrai.github.io
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quizizz Lịch Sử 12 - Ôn Thi Giữa Học Kỳ I</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome & Google Fonts -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:ital,wght@0,400;0,500;0,600;0,700;0,800;0,900;1,400;1,600&family=Lexend:wght@400;500;600;700;800&family=Nunito:wght@400;600;700;800;900&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        quizizz: {
                            dark: '#0f172a',
                            purple: '#1e1b4b',
                            cardBg: '#1e293b',
                            cardBorder: '#334155',
                            accent: '#eab308',
                            lightPurple: '#818cf8',
                            red: '#22c55e',
                            wrongRed: '#ef4444',
                            yellow: '#f59e0b',
                            blue: '#3b82f6',
                            orange: '#f97316'
                        }
                    },
                    fontFamily: {
                        vietnam: ['"Be Vietnam Pro"', 'sans-serif'],
                        lexend: ['Lexend', 'sans-serif'],
                        nunito: ['Nunito', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Be Vietnam Pro', 'Nunito', sans-serif;
            background: linear-gradient(135deg, #090d16 0%, #1e1b4b 50%, #0f172a 100%);
            color: #ffffff;
            min-height: 100vh;
            user-select: none;
            overflow-x: hidden;
            -webkit-tap-highlight-color: transparent;
        }

        .font-game {
            font-family: 'Lexend', 'Be Vietnam Pro', 'Nunito', sans-serif;
        }

        /* Responsive touch targets and mobile optimization */
        button, label, input {
            touch-action: manipulation;
        }

        .glass-panel {
            background: rgba(30, 41, 59, 0.85);
            backdrop-filter: blur(12px);
            border: 2px solid rgba(234, 179, 8, 0.3);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.4);
        }

        .btn-quizizz {
            transition: all 0.15s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            transform-style: preserve-3d;
        }

        .btn-quizizz:active {
            transform: translateY(4px);
            box-shadow: 0 0 0 0 rgba(0,0,0,0) !important;
        }

        .q-option-red {
            background-color: #22c55e;
            border-bottom: 5px solid #15803d;
        }
        .q-option-blue {
            background-color: #3b82f6;
            border-bottom: 5px solid #1d4ed8;
        }
        .q-option-yellow {
            background-color: #eab308;
            border-bottom: 5px solid #a16207;
            color: #0f172a;
        }
        .q-option-green {
            background-color: #f43f5e;
            border-bottom: 5px solid #be123c;
        }

        /* Flashcard 3D flip */
        .perspective-1000 {
            perspective: 1000px;
            -webkit-perspective: 1000px;
        }
        .transform-style-3d {
            transform-style: preserve-3d;
            -webkit-transform-style: preserve-3d;
            transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .backface-hidden {
            backface-visibility: hidden !important;
            -webkit-backface-visibility: hidden !important;
        }
        .flashcard-front {
            transform: rotateY(0deg);
            -webkit-transform: rotateY(0deg);
        }
        .flashcard-back {
            transform: rotateY(180deg);
            -webkit-transform: rotateY(180deg);
        }
        .rotate-y-180 {
            transform: rotateY(180deg);
            -webkit-transform: rotateY(180deg);
        }

        /* Particles */
        .bg-particle {
            position: absolute;
            border-radius: 50%;
            pointer-events: none;
            opacity: 0.15;
            animation: floatSlow 12s infinite ease-in-out;
        }

        @keyframes floatSlow {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-30px) rotate(180deg); }
        }

        .streak-fire {
            animation: flame 0.8s infinite alternate ease-in-out;
        }
        @keyframes flame {
            0% { transform: scale(1) rotate(-3deg); }
            100% { transform: scale(1.15) rotate(3deg); }
        }

        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0f172a;
        }
        ::-webkit-scrollbar-thumb {
            background: #eab308;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #facc15;
        }
    </style>
</head>
<body class="flex flex-col min-h-screen relative overflow-x-hidden">

    <!-- Floating Particles -->
    <div class="bg-particle w-64 h-64 bg-amber-500 top-10 left-5"></div>
    <div class="bg-particle w-96 h-96 bg-indigo-600 bottom-10 right-5"></div>
    <div class="bg-particle w-48 h-48 bg-rose-500 top-1/2 left-1/3"></div>

    <!-- HEADER CONTROLS -->
    <header class="w-full z-40 bg-slate-900/90 backdrop-blur-md border-b border-slate-700 px-3 sm:px-4 py-2.5 sm:py-3 flex justify-between items-center sticky top-0 shadow-lg">
        <div class="flex items-center space-x-2 sm:space-x-3 cursor-pointer" onclick="showView('home')">
            <div class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-gradient-to-tr from-amber-500 to-indigo-600 flex items-center justify-center font-game text-xl sm:text-2xl font-black text-white shadow-md transform hover:rotate-6 transition flex-shrink-0">
                📜
            </div>
            <div>
                <h1 class="font-game font-bold text-base sm:text-xl tracking-wide bg-clip-text text-transparent bg-gradient-to-r from-amber-300 via-yellow-200 to-sky-300 leading-tight">
                    QUIZIZZ LỊCH SỬ 12
                </h1>
                <p class="text-[10px] sm:text-xs text-amber-200 font-semibold hidden sm:block">Ôn Thi Giữa Học Kỳ I • Đề Cương Chuẩn</p>
            </div>
        </div>

        <div class="flex items-center space-x-1.5 sm:space-x-3">
            <div id="header-streak" class="hidden flex items-center bg-slate-800 border border-amber-500/50 rounded-full px-2.5 sm:px-3 py-1 space-x-1 shadow-inner">
                <span class="text-base sm:text-xl streak-fire">🔥</span>
                <span id="streak-count" class="font-game font-bold text-amber-400 text-xs sm:text-sm">0</span>
                <span class="text-[10px] sm:text-xs text-slate-300 hidden xs:inline">Streak</span>
            </div>

            <div id="header-xp" class="flex items-center bg-amber-950 border border-amber-400/40 rounded-full px-2.5 sm:px-3 py-1 space-x-1 sm:space-x-1.5 shadow-inner">
                <i class="fa-solid fa-trophy text-amber-400 text-xs sm:text-sm"></i>
                <span id="user-xp" class="font-game font-bold text-amber-300 text-xs sm:text-sm">0 XP</span>
            </div>

            <button id="sound-btn" onclick="toggleSound()" class="w-8 h-8 sm:w-9 sm:h-9 rounded-full bg-slate-800 border border-slate-600 flex items-center justify-center text-amber-200 hover:text-white transition active:scale-90">
                <i class="fa-solid fa-volume-high text-xs sm:text-sm"></i>
            </button>

            <button onclick="showView('home')" class="w-8 h-8 sm:w-9 sm:h-9 rounded-full bg-slate-800 border border-slate-600 flex items-center justify-center text-amber-200 hover:text-white transition active:scale-90">
                <i class="fa-solid fa-house text-xs sm:text-sm"></i>
            </button>
        </div>
    </header>

    <!-- MAIN CONTAINER -->
    <main class="flex-grow container mx-auto px-3 sm:px-4 py-4 sm:py-6 max-w-5xl z-10">

        <!-- ================= 1. HOME DASHBOARD ================= -->
        <section id="view-home" class="space-y-8 animate-fadeIn">
            <div class="glass-panel rounded-3xl p-6 sm:p-8 relative overflow-hidden text-center sm:text-left border border-amber-500/40">
                <div class="sm:w-2/3 relative z-10 space-y-4">
                    <span class="inline-block px-3 py-1 rounded-full bg-amber-500/20 text-amber-300 text-xs font-bold border border-amber-400/30 uppercase tracking-widest">
                        Trường THCS & THPT Chu Văn An • Hiệp Thạnh
                    </span>
                    <h2 class="text-3xl sm:text-4xl font-black font-game text-white leading-tight">
                        Chinh Phục 10 Điểm <br><span class="bg-clip-text text-transparent bg-gradient-to-r from-amber-300 via-yellow-200 to-amber-400">Lịch Sử 12 Giữa Kỳ 1!</span>
                    </h2>
                    <p class="text-slate-200 text-sm sm:text-base leading-relaxed">
                        Ngân hàng 74 câu hỏi trắc nghiệm & đúng sai bám sát 100% đề cương kèm tư liệu tham khảo: Thế giới trong & sau Chiến tranh lạnh, ASEAN và Cách mạng tháng Tám 1945 - Kháng chiến chống Pháp!
                    </p>
                    <div class="pt-2 flex flex-wrap gap-3 justify-center sm:justify-start">
                        <button onclick="startSpeedRun()" class="btn-quizizz px-6 py-3.5 bg-gradient-to-r from-amber-500 to-yellow-600 hover:from-amber-400 text-white font-game font-bold text-lg rounded-2xl shadow-lg border-b-4 border-amber-800 flex items-center space-x-2">
                            <i class="fa-solid fa-bolt text-yellow-200"></i>
                            <span>THI THỬ TỔNG HỢP (25 CÂU)</span>
                        </button>
                        <button onclick="showView('flashcards')" class="btn-quizizz px-5 py-3.5 bg-slate-800/80 hover:bg-slate-700 text-slate-100 font-game font-bold text-base rounded-2xl border border-amber-500/50 flex items-center space-x-2">
                            <i class="fa-solid fa-layer-group text-amber-400"></i>
                            <span>LẬT FLASHCARD LÝ THUYẾT</span>
                        </button>
                    </div>
                </div>
                <div class="hidden sm:block absolute -right-6 -bottom-6 w-80 h-80 opacity-90 pointer-events-none">
                    <i class="fa-solid fa-landmark text-9xl text-amber-500/20 absolute top-12 right-16 transform rotate-12 animate-pulse"></i>
                </div>
            </div>

            <!-- Topic Filter Selector -->
            <div class="space-y-4">
                <div class="flex items-center justify-between">
                    <h3 class="font-game font-bold text-2xl text-amber-100 flex items-center space-x-2">
                        <i class="fa-solid fa-compass text-amber-400"></i>
                        <span>CHỌN CHỦ ĐỀ VÀ DẠNG LUYỆN TẬP</span>
                    </h3>
                    <span class="text-xs bg-slate-900 text-amber-300 font-semibold px-3 py-1 rounded-full border border-amber-600">
                        74 Cụm Câu Hỏi Đầy Đủ
                    </span>
                </div>

                <!-- Topic selection pills -->
                <div class="flex flex-wrap gap-2">
                    <button onclick="setTopicFilter('all')" id="topic-btn-all" class="topic-btn active px-4 py-2 rounded-xl font-game font-bold text-xs bg-amber-500 text-slate-950 border border-amber-400 shadow">
                        Tất cả 3 Chủ Đề
                    </button>
                    <button onclick="setTopicFilter('cd1')" id="topic-btn-cd1" class="topic-btn px-4 py-2 rounded-xl font-game font-bold text-xs bg-slate-800 text-amber-200 hover:bg-slate-700 border border-slate-600">
                        Chủ đề 1: Thế giới & Chiến tranh lạnh
                    </button>
                    <button onclick="setTopicFilter('cd2')" id="topic-btn-cd2" class="topic-btn px-4 py-2 rounded-xl font-game font-bold text-xs bg-slate-800 text-amber-200 hover:bg-slate-700 border border-slate-600">
                        Chủ đề 2: ASEAN
                    </button>
                    <button onclick="setTopicFilter('cd3')" id="topic-btn-cd3" class="topic-btn px-4 py-2 rounded-xl font-game font-bold text-xs bg-slate-800 text-amber-200 hover:bg-slate-700 border border-slate-600">
                        Chủ đề 3: CM Tháng Tám & Kháng chiến
                    </button>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-5 pt-2">
                    <!-- MCQ Mode -->
                    <div onclick="startPracticeMode('mcq')" class="glass-panel rounded-2xl p-6 border-b-4 border-amber-500 hover:border-amber-400 hover:-translate-y-1 transition cursor-pointer group">
                        <div class="flex items-center justify-between mb-4">
                            <div class="w-12 h-12 rounded-xl bg-amber-500/20 border border-amber-400/40 flex items-center justify-center text-amber-400 text-2xl group-hover:scale-110 transition">
                                <i class="fa-solid fa-list-check"></i>
                            </div>
                            <span class="text-xs font-bold bg-amber-950 text-amber-300 px-2.5 py-1 rounded-lg">Phần I</span>
                        </div>
                        <h4 class="font-game font-bold text-xl text-white mb-2 group-hover:text-amber-300 transition">Trắc Nghiệm 4 Lựa Chọn (51 Câu)</h4>
                        <p class="text-xs text-slate-300 leading-relaxed mb-4">
                            Tự động đảo câu hỏi ngẫu nhiên và chuẩn hóa thứ tự (Câu 1, Câu 2...), rèn luyện tốc độ xử lý câu hỏi trắc nghiệm.
                        </p>
                        <div class="flex justify-between items-center text-xs text-slate-300 font-semibold">
                            <span id="mcq-count-label">51 Câu hỏi chuẩn</span>
                            <span class="text-amber-400 flex items-center">Luyện Tập <i class="fa-solid fa-arrow-right ml-1"></i></span>
                        </div>
                    </div>

                    <!-- True/False Mode -->
                    <div onclick="startPracticeMode('tf')" class="glass-panel rounded-2xl p-6 border-b-4 border-sky-500 hover:border-sky-400 hover:-translate-y-1 transition cursor-pointer group">
                        <div class="flex items-center justify-between mb-4">
                            <div class="w-12 h-12 rounded-xl bg-sky-500/20 border border-sky-400/40 flex items-center justify-center text-sky-400 text-2xl group-hover:scale-110 transition">
                                <i class="fa-solid fa-scale-balanced"></i>
                            </div>
                            <span class="text-xs font-bold bg-sky-950 text-sky-300 px-2.5 py-1 rounded-lg">Phần II</span>
                        </div>
                        <h4 class="font-game font-bold text-xl text-white mb-2 group-hover:text-sky-300 transition">Trắc Nghiệm Đúng / Sai (23 Chùm Tư Liệu)</h4>
                        <p class="text-xs text-slate-300 leading-relaxed mb-4">
                            Cấu trúc mới thi THPT: Phân tích các đoạn tư liệu lịch sử và đánh giá 4 mệnh đề a, b, c, d đúng hay sai.
                        </p>
                        <div class="flex justify-between items-center text-xs text-slate-300 font-semibold">
                            <span id="tf-count-label">23 Chùm câu (92 mệnh đề)</span>
                            <span class="text-sky-400 flex items-center">Đánh Giá <i class="fa-solid fa-arrow-right ml-1"></i></span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Quick Knowledge Summary -->
            <div class="glass-panel rounded-2xl p-6 border border-amber-500/30">
                <div class="flex items-center space-x-3 mb-4">
                    <i class="fa-solid fa-star text-amber-300 text-2xl"></i>
                    <h3 class="font-game font-bold text-xl text-white">CÁC MỐC LỊCH SỬ CỐT LÕI CẦN NHỚ</h3>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4 text-xs text-slate-200">
                    <div class="bg-slate-900/70 p-3 rounded-xl border border-amber-800/40 space-y-1">
                        <span class="font-bold text-amber-300 block mb-1">🌍 Chủ đề 1: Thế giới & CT Lạnh</span>
                        - 24/10/1945: Hiến chương LHQ có hiệu lực.<br>
                        - 3/1947: Thông điệp Truman mở đầu CT Lạnh.<br>
                        - 11/1989: Bức tường Béc-lin sụp đổ.<br>
                        - 12/1991: Liên Xô tan rã, trật tự 2 cực I-an-ta sụp đổ.
                    </div>
                    <div class="bg-slate-900/70 p-3 rounded-xl border border-amber-800/40 space-y-1">
                        <span class="font-bold text-sky-300 block mb-1">🌏 Chủ đề 2: ASEAN</span>
                        - 8/8/1967: Thành lập ASEAN (Tuyên bố Băng Cốc).<br>
                        - 1976: Ký Hiệp ước Bali (TAC) chuyển sang liên kết.<br>
                        - 2007: Thông qua Hiến chương ASEAN.<br>
                        - 31/12/2015: Chính thức thành lập Cộng đồng ASEAN (3 trụ cột).
                    </div>
                    <div class="bg-slate-900/70 p-3 rounded-xl border border-amber-800/40 space-y-1">
                        <span class="font-bold text-emerald-300 block mb-1">🇻🇳 Chủ đề 3: CM T8 & Đấu tranh</span>
                        - 13/8/1945: Quân lệnh số 1 phát lệnh Tổng khởi nghĩa.<br>
                        - 18/8/1945: 4 tỉnh giành CQ sớm nhất (BG, HD, HT, QN).<br>
                        - 2/9/1945: Bác Hồ đọc Tuyên ngôn Độc lập.<br>
                        - 19/12/1946: Lời kêu gọi Toàn quốc kháng chiến.
                    </div>
                </div>
            </div>
        </section>

        <!-- ================= 2. QUIZ PLAYING GAME SCREEN ================= -->
        <section id="view-quiz" class="hidden space-y-4 sm:space-y-6">
            <div class="glass-panel rounded-2xl p-3 sm:p-4 flex flex-wrap items-center justify-between gap-2.5 sm:gap-4">
                <div class="flex items-center space-x-2 sm:space-x-3 w-full sm:w-auto justify-between sm:justify-start">
                    <span id="quiz-progress-text" class="font-game font-bold text-amber-200 text-xs sm:text-sm whitespace-nowrap">
                        Câu 1 / 51
                    </span>
                    <div class="w-32 sm:w-48 bg-slate-950 h-2.5 sm:h-3 rounded-full overflow-hidden border border-amber-700/60">
                        <div id="quiz-progress-bar" class="bg-gradient-to-r from-amber-500 to-yellow-400 h-full w-0 transition-all duration-300"></div>
                    </div>
                </div>

                <div class="w-full sm:w-1/3 flex items-center space-x-2">
                    <i class="fa-solid fa-clock text-amber-400 animate-spin text-xs sm:text-base"></i>
                    <div class="w-full bg-slate-950 h-3 sm:h-4 rounded-full overflow-hidden border border-amber-500/40 relative">
                        <div id="timer-bar" class="bg-gradient-to-r from-amber-400 to-rose-500 h-full w-full transition-all duration-100 linear"></div>
                    </div>
                    <span id="timer-text" class="font-game font-bold text-amber-300 text-xs sm:text-sm w-7 sm:w-8 text-right">30s</span>
                </div>

                <div class="flex items-center justify-end w-full sm:w-auto">
                    <span id="quiz-combo-badge" class="bg-amber-500/20 text-amber-300 border border-amber-400/50 font-game font-bold text-[11px] sm:text-xs px-2.5 py-0.5 sm:px-3 sm:py-1 rounded-full">
                        Multiplier x1.0
                    </span>
                </div>
            </div>

            <div class="glass-panel rounded-2xl sm:rounded-3xl p-4 sm:p-8 relative border border-amber-400/30 shadow-2xl space-y-4 sm:space-y-6">
                <div class="flex items-center justify-between gap-2">
                    <span id="q-category-tag" class="text-[10px] sm:text-xs font-bold uppercase tracking-wider text-amber-300 bg-amber-950 px-2.5 py-1 rounded-full border border-amber-600 truncate max-w-[220px] sm:max-w-none">
                        Chủ đề: Lịch Sử 12
                    </span>
                    <span id="q-points-value" class="font-game font-bold text-xs sm:text-sm text-amber-400 flex-shrink-0">
                        +1000 Pts
                    </span>
                </div>

                <div id="question-box" class="space-y-3 sm:space-y-4">
                    <h3 id="question-text" class="font-game font-bold text-lg sm:text-2xl text-white leading-snug sm:leading-relaxed whitespace-pre-line break-words">
                        Đang tải câu hỏi...
                    </h3>
                </div>

                <div id="answers-container" class="grid grid-cols-1 md:grid-cols-2 gap-3 sm:gap-4 pt-1 sm:pt-2">
                </div>

                <div id="explanation-box" class="hidden p-3.5 sm:p-4 rounded-2xl bg-slate-900/95 border border-amber-400/50 space-y-3 animate-fadeIn">
                    <div id="feedback-header" class="flex items-center space-x-2 font-game font-bold text-base sm:text-lg">
                    </div>
                    <div id="explanation-text" class="text-xs sm:text-sm text-slate-100 leading-relaxed">
                    </div>
                    <div class="flex justify-end">
                        <button id="next-btn" onclick="nextQuestion()" class="btn-quizizz w-full sm:w-auto px-6 py-3 sm:py-2.5 bg-gradient-to-r from-amber-500 to-yellow-600 hover:from-amber-400 text-white font-game font-bold text-base rounded-xl shadow-md border-b-4 border-amber-800 active:scale-95">
                            Tiếp theo <i class="fa-solid fa-chevron-right ml-1"></i>
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- ================= 3. FLASHCARD MODE ================= -->
        <section id="view-flashcards" class="hidden space-y-4 sm:space-y-6">
            <div class="flex items-center justify-between gap-2">
                <div>
                    <h3 class="font-game font-bold text-xl sm:text-2xl text-amber-100">
                        <i class="fa-solid fa-layer-group text-amber-400 mr-1.5"></i>Flashcard Lý Thuyết
                    </h3>
                    <p class="text-[11px] sm:text-xs text-amber-200">Chạm vào thẻ để lật xem đáp án!</p>
                </div>
                <button onclick="showView('home')" class="px-2.5 py-1.5 bg-slate-800 hover:bg-slate-700 border border-slate-600 rounded-xl text-xs font-bold text-amber-200 flex-shrink-0">
                    <i class="fa-solid fa-arrow-left mr-1"></i> Trở về
                </button>
            </div>

            <div class="flex flex-col items-center justify-center space-y-4 sm:space-y-6">
                <div class="w-full max-w-lg h-72 sm:h-80 perspective-1000 cursor-pointer" onclick="flipFlashcard()">
                    <div id="flashcard-inner" class="w-full h-full transform-style-3d relative rounded-3xl shadow-2xl border-2 border-amber-400/50 text-center">
                        <div class="absolute inset-0 backface-hidden flashcard-front p-8 flex flex-col justify-between items-center bg-gradient-to-br from-slate-900 via-indigo-950 to-slate-900 rounded-3xl border-2 border-amber-400/50 shadow-2xl">
                            <span class="text-xs font-bold text-amber-300 uppercase tracking-widest bg-amber-950 px-3 py-1 rounded-full border border-amber-700/50">
                                CÂU HỎI LỊCH SỬ
                            </span>
                            <div class="my-auto">
                                <h4 id="flashcard-question" class="font-game font-bold text-xl sm:text-2xl text-white leading-snug">
                                    Thành lập LHQ có ý nghĩa gì?
                                </h4>
                            </div>
                            <p class="text-xs text-amber-300 flex items-center">
                                <i class="fa-solid fa-hand-pointer mr-1"></i> Bấm để xem câu trả lời
                            </p>
                        </div>

                        <div class="absolute inset-0 backface-hidden flashcard-back p-8 flex flex-col justify-between items-center bg-gradient-to-br from-amber-950 via-slate-900 to-indigo-950 rounded-3xl border-2 border-amber-400/50 shadow-2xl">
                            <span class="text-xs font-bold text-amber-300 uppercase tracking-widest bg-amber-950 px-3 py-1 rounded-full border border-amber-700/50">
                                ĐÁP ÁN CHUẨN
                            </span>
                            <div class="my-auto overflow-y-auto max-h-48 px-2">
                                <p id="flashcard-answer" class="text-sm sm:text-base text-slate-100 font-semibold leading-relaxed whitespace-pre-line">
                                    Nội dung câu trả lời...
                                </p>
                            </div>
                            <span id="flashcard-counter" class="text-xs text-amber-300 font-game">
                                Thẻ 1 / 15
                            </span>
                        </div>
                    </div>
                </div>

                <div class="flex items-center space-x-4">
                    <button onclick="prevFlashcard()" class="btn-quizizz px-5 py-2.5 bg-slate-800 border border-slate-600 rounded-xl font-game font-bold text-sm text-slate-200 hover:text-white">
                        <i class="fa-solid fa-chevron-left mr-1"></i> Thẻ Trước
                    </button>
                    <button onclick="shuffleFlashcards()" class="btn-quizizz px-4 py-2.5 bg-amber-600 border border-amber-500 rounded-xl font-game font-bold text-sm text-amber-100 hover:bg-amber-500">
                        <i class="fa-solid fa-shuffle"></i>
                    </button>
                    <button onclick="nextFlashcard()" class="btn-quizizz px-5 py-2.5 bg-slate-800 border border-slate-600 rounded-xl font-game font-bold text-sm text-slate-200 hover:text-white">
                        Thẻ Sau <i class="fa-solid fa-chevron-right ml-1"></i>
                    </button>
                </div>
            </div>
        </section>

        <!-- ================= 4. POST-QUIZ RESULT ================= -->
        <section id="view-result" class="hidden space-y-8 animate-fadeIn">
            <div class="glass-panel rounded-3xl p-8 text-center relative overflow-hidden border border-amber-400/40 space-y-6">
                <div class="inline-block w-20 h-20 rounded-full bg-gradient-to-tr from-amber-400 to-indigo-500 p-1 shadow-2xl mx-auto animate-bounce">
                    <div class="w-full h-full bg-slate-950 rounded-full flex items-center justify-center text-amber-400 text-3xl">
                        <i class="fa-solid fa-crown"></i>
                    </div>
                </div>

                <div class="space-y-2">
                    <h2 class="font-game font-black text-3xl sm:text-4xl text-white">HOÀN THÀNH BÀI THI LỊCH SỬ!</h2>
                    <p id="result-rank-title" class="text-lg font-bold text-amber-300">
                        Danh hiệu: "Nhà Sử Học Trẻ"
                    </p>
                </div>

                <div class="grid grid-cols-2 sm:grid-cols-4 gap-4 max-w-2xl mx-auto pt-2">
                    <div class="bg-slate-900/80 p-4 rounded-2xl border border-amber-700/50">
                        <span class="text-xs text-slate-300 font-semibold block">TỔNG ĐIỂM</span>
                        <span id="res-score" class="font-game font-black text-2xl sm:text-3xl text-amber-300">0</span>
                    </div>
                    <div class="bg-slate-900/80 p-4 rounded-2xl border border-amber-700/50">
                        <span class="text-xs text-slate-300 font-semibold block">ĐỘ CHÍNH XÁC</span>
                        <span id="res-accuracy" class="font-game font-black text-2xl sm:text-3xl text-emerald-400">0%</span>
                    </div>
                    <div class="bg-slate-900/80 p-4 rounded-2xl border border-amber-700/50">
                        <span class="text-xs text-slate-300 font-semibold block">CÂU ĐÚNG</span>
                        <span id="res-correct" class="font-game font-black text-2xl sm:text-3xl text-sky-400">0/0</span>
                    </div>
                    <div class="bg-slate-900/80 p-4 rounded-2xl border border-amber-700/50">
                        <span class="text-xs text-slate-300 font-semibold block">MAX STREAK</span>
                        <span id="res-streak" class="font-game font-black text-2xl sm:text-3xl text-rose-400">🔥 0</span>
                    </div>
                </div>

                <div class="flex flex-wrap justify-center gap-4 pt-4">
                    <button onclick="showView('home')" class="btn-quizizz px-6 py-3 bg-slate-800 hover:bg-slate-700 text-white font-game font-bold rounded-2xl border-b-4 border-slate-950">
                        <i class="fa-solid fa-house mr-1"></i> TRANG CHỦ
                    </button>
                    <button onclick="restartCurrentQuiz()" class="btn-quizizz px-6 py-3 bg-gradient-to-r from-amber-500 to-yellow-600 text-white font-game font-bold rounded-2xl shadow-lg border-b-4 border-amber-800">
                        <i class="fa-solid fa-rotate-right mr-1"></i> LÀM LẠI LẦN NỮA
                    </button>
                </div>
            </div>

            <!-- DETAILED REVIEW -->
            <div class="glass-panel rounded-3xl p-6 sm:p-8 border border-amber-500/30 space-y-6">
                <div class="flex items-center justify-between border-b border-amber-700/50 pb-4">
                    <h3 class="font-game font-bold text-2xl text-amber-100 flex items-center space-x-2">
                        <i class="fa-solid fa-magnifying-glass text-amber-400"></i>
                        <span>XEM LẠI CHI TIẾT ĐÁP ÁN & LỜI GIẢI</span>
                    </h3>
                </div>

                <div id="review-list-container" class="space-y-4">
                </div>
            </div>
        </section>

    </main>

    <!-- MEME POPUP -->
    <div id="meme-popup" class="fixed inset-0 bg-black/60 z-50 flex items-center justify-center p-4 pointer-events-none opacity-0 transition-opacity duration-200">
        <div id="meme-card" class="bg-gradient-to-tr from-amber-900 to-slate-900 border-4 border-amber-400 rounded-3xl p-6 text-center max-w-sm w-full shadow-2xl transform scale-75 transition-transform duration-200">
            <span id="meme-emoji" class="text-6xl block mb-2">🎉</span>
            <h3 id="meme-title" class="font-game font-black text-3xl text-amber-300">ĐỈNH KOBE!</h3>
            <p id="meme-sub" class="font-game text-sm text-slate-100 mt-1">Chuỗi trả lời đúng bùng nổ!</p>
        </div>
    </div>

    <footer class="w-full border-t border-amber-900/60 bg-slate-950 text-center py-4 text-xs text-amber-400 z-10">
        <p>Quizizz Lịch Sử 12 - Học Kì I • Trường THCS & THPT Chu Văn An (Hiệp Thạnh)</p>
    </footer>

    <!-- JAVASCRIPT LOGIC & 100% COMPLETE DATASET EXTRACTION WITH FULL TEXT PASSAGES -->
    <script>
        let userXP = 0;
        let currentStreak = 0;
        let maxStreak = 0;
        let soundEnabled = true;
        let audioCtx = null;

        let selectedTopicFilter = 'all'; // 'all', 'cd1', 'cd2', 'cd3'
        let currentQuestions = [];
        let currentIndex = 0;
        let userAnswers = [];
        let timerInterval = null;
        let timeLeft = 30;
        let currentScore = 0;

        let flashcards = [];
        let currentFcIndex = 0;
        let isFcFlipped = false;

        /* WEB AUDIO SYNTHESIZER */
        function playAudio(type) {
            if (!soundEnabled) return;
            try {
                if (!audioCtx) {
                    audioCtx = new (window.AudioContext || window.webkitAudioContext)();
                }
                if (audioCtx.state === 'suspended') {
                    audioCtx.resume();
                }
                const now = audioCtx.currentTime;
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();
                osc.connect(gain);
                gain.connect(audioCtx.destination);

                if (type === 'click') {
                    osc.frequency.setValueAtTime(400, now);
                    gain.gain.setValueAtTime(0.05, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.05);
                    osc.start(now);
                    osc.stop(now + 0.05);
                } else if (type === 'correct') {
                    osc.type = 'triangle';
                    osc.frequency.setValueAtTime(523.25, now);
                    osc.frequency.setValueAtTime(659.25, now + 0.08);
                    osc.frequency.setValueAtTime(783.99, now + 0.16);
                    gain.gain.setValueAtTime(0.15, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.35);
                    osc.start(now);
                    osc.stop(now + 0.35);
                } else if (type === 'wrong') {
                    osc.type = 'sawtooth';
                    osc.frequency.setValueAtTime(220, now);
                    osc.frequency.setValueAtTime(164.81, now + 0.12);
                    gain.gain.setValueAtTime(0.2, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.3);
                    osc.start(now);
                    osc.stop(now + 0.3);
                } else if (type === 'streak') {
                    osc.type = 'sine';
                    osc.frequency.setValueAtTime(440, now);
                    osc.frequency.setValueAtTime(880, now + 0.1);
                    gain.gain.setValueAtTime(0.2, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.4);
                    osc.start(now);
                    osc.stop(now + 0.4);
                }
            } catch(e) {
                console.warn("Audio error:", e);
            }
        }

        function toggleSound() {
            soundEnabled = !soundEnabled;
            const btn = document.getElementById('sound-btn');
            if (soundEnabled) {
                btn.innerHTML = '<i class="fa-solid fa-volume-high text-sm"></i>';
                btn.classList.remove('text-red-400');
                playAudio('click');
            } else {
                btn.innerHTML = '<i class="fa-solid fa-volume-xmark text-sm"></i>';
                btn.classList.add('text-red-400');
            }
        }

        function showView(viewId) {
            playAudio('click');
            ['view-home', 'view-quiz', 'view-flashcards', 'view-result'].forEach(id => {
                const el = document.getElementById(id);
                if (el) el.classList.add('hidden');
            });
            
            const target = document.getElementById('view-' + viewId);
            if (target) target.classList.remove('hidden');

            if (viewId === 'home' || viewId === 'result') {
                if (timerInterval) clearInterval(timerInterval);
                document.getElementById('header-streak').classList.add('hidden');
            } else if (viewId === 'quiz') {
                document.getElementById('header-streak').classList.remove('hidden');
            } else if (viewId === 'flashcards') {
                initFlashcards();
            }
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        /* 100% COMPLETE QUESTION EXTRACTION FROM DOCUMENT */
        const historyMCQ = [
            // CHỦ ĐỀ 1 (25 CÂU)
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Trật tự Thế giới & CT Lạnh',
                question: 'Câu 1: Đầu năm 1945, đâu là vấn đề cấp bách đặt ra cho các nước Đồng minh chống phát xít?',
                options: ['A. Phân chia lại thuộc địa của các nước.', 'B. Tổ chức lại thế giới sau chiến tranh.', 'C. Thiết lập trật tự thế giới mới hai cực.', 'D. Phục hồi và phát triển kinh tế thế giới.'],
                correct: 1,
                explanation: 'Đầu năm 1945, CTTG2 bước vào giai đoạn kết thúc, 3 vấn đề cấp bách đặt ra: Tiêu diệt phát xít, Tổ chức lại thế giới sau chiến tranh, và Phân chia phạm vi ảnh hưởng.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Liên hợp quốc',
                question: 'Câu 2: Ngày 01/01/1942, đại diện 26 quốc gia chống phát xít đã ký kết văn kiện nào sau đây tại Oa-sinh-tơn?',
                options: ['A. Tuyên bố Liên hợp quốc.', 'B. Hiến chương Liên hợp quốc.', 'C. Hiệp ước Bắc Đại Tây Dương (NATO).', 'D. Tuyên bố Băng Cốc.'],
                correct: 0,
                explanation: 'Ngày 1/1/1942, đại diện 26 quốc gia chống phát xít đã thông qua Tuyên bố Liên hợp quốc cam kết tiêu diệt chủ nghĩa phát xít.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Liên hợp quốc',
                question: 'Câu 3: Tổ chức Liên hợp quốc chính thức được thành lập sau sự kiện lịch sử nào sau đây?',
                options: ['A. Hiến chương Liên hợp quốc chính thức có hiệu lực (24/10/1945).', 'B. Hội nghị I-an-ta kết thúc công tác chuẩn bị (2/1945).', 'C. Chiến tranh thế giới thứ nhất kết thúc hoàn toàn (11/1918).', 'D. Hiệp ước Bắc Đại Tây Dương (NATO) được ký kết (4/1949).'],
                correct: 0,
                explanation: 'Ngày 24/10/1945, Hiến chương Liên hợp quốc chính thức có hiệu lực, đánh dấu sự ra đời của tổ chức Liên hợp quốc.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Liên hợp quốc',
                question: 'Câu 4: Mục tiêu và nguyên tắc hoạt động của Liên hợp quốc được quy định bởi văn kiện quan trọng nào?',
                options: ['A. Hiến chương.', 'B. Hiến pháp.', 'C. Tuyên ngôn.', 'D. Hiệp định.'],
                correct: 0,
                explanation: 'Hiến chương Liên hợp quốc là văn kiện pháp lý quan trọng nhất quy định rõ mục tiêu và nguyên tắc hoạt động của tổ chức.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Liên hợp quốc',
                question: 'Câu 5: Cơ quan nào của Liên hợp quốc giữ vai trò trọng yếu trong việc duy trì hòa bình và an ninh quốc tế?',
                options: ['A. Hội đồng Bảo an.', 'B. Đại hội đồng.', 'C. Ban Thư ký.', 'D. Hội đồng Kinh tế và Xã hội.'],
                correct: 0,
                explanation: 'Hội đồng Bảo an là cơ quan duy nhất của LHQ giữ vai trò trọng yếu trong việc duy trì hòa bình và an ninh quốc tế.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Liên hợp quốc',
                question: 'Câu 6: Đâu là một trong những nội dung của mục tiêu, hành động mang tính toàn cầu đến năm 2030 của Liên hợp quốc?',
                options: ['A. Chống nạn thất nghiệp.', 'B. Quyền tự do chính trị.', 'C. Chống bạo lực gia đình.', 'D. Chất lượng giáo dục.'],
                correct: 3,
                explanation: 'Chất lượng giáo dục (Goal 4) nằm trong 17 Mục tiêu Phát triển Bền vững (SDGs) đến năm 2030 của Liên hợp quốc.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Liên hợp quốc',
                question: 'Câu 7: Sự phát triển của Liên hợp quốc từ 51 quốc gia sáng lập (1945) lên 193 thành viên hiện nay phản ánh xu thế tất yếu nào của lịch sử?',
                options: ['A. Xu thế toàn cầu hóa, đa phương hóa quan hệ quốc tế và sự thắng lợi của phong trào giải phóng dân tộc.', 'B. Sự mở rộng không ngừng của các liên minh quân sự tư bản chủ nghĩa.', 'C. Sự thất bại hoàn toàn của trật tự thế giới đa cực trong nền chính trị hiện đại.', 'D. Sự suy giảm quyền lực tuyệt đối của các tổ chức khu vực như ASEAN hay EU.'],
                correct: 0,
                explanation: 'Sự mở rộng thành viên LHQ phản ánh thắng lợi của phong trào giải phóng dân tộc và xu thế đa phương hóa quan hệ quốc tế.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Đối ngoại Việt Nam',
                question: 'Câu 8: Tác động từ việc Việt Nam đảm nhiệm thành công vai trò Ủy viên không thường trực Hội đồng Bảo an Liên hợp quốc (nhiệm kỳ 2008-2009 và 2020-2021) là:',
                options: ['A. Nâng cao uy tín, vị thế quốc tế và khẳng định đường lối đối ngoại độc lập, tự chủ, đa phương hóa.', 'B. Giúp Việt Nam ngay lập tức trở thành cường quốc kinh tế hàng đầu khu vực Đông Nam Á.', 'C. Buộc các nước lớn phải hủy bỏ hoàn toàn chính sách bao vây cấm vận đối với Việt Nam.', 'D. Thay đổi toàn bộ cơ chế hoạt động của Hội đồng Bảo an theo hướng có lợi cho các nước nghèo.'],
                correct: 0,
                explanation: 'Thành công tại HĐBA LHQ nâng cao rõ rệt vị thế, uy tín quốc tế của Việt Nam trên trường quốc tế.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Chiến tranh lạnh',
                question: 'Câu 9: Bản chất của Chiến tranh lạnh (1947 - 1989) là:',
                options: ['A. Cuộc đối đầu căng thẳng toàn diện trên mọi lĩnh vực giữa hai phe TBCN và XHCN do Mỹ và Liên Xô đứng đầu.', 'B. Cuộc chiến tranh thương mại đơn thuần giữa các tập đoàn tư bản phương Tây.', 'C. Cuộc xung đột vũ trang quy mô lớn diễn ra trên lãnh thổ Mỹ và Liên Xô.', 'D. Sự tranh chấp lãnh thổ giữa các nước thuộc địa ở châu Á và châu Phi.'],
                correct: 0,
                explanation: 'Chiến tranh lạnh là cuộc đối đầu căng thẳng trên hầu hết các lĩnh vực giữa hai phe do Mỹ và Liên Xô đứng đầu.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Sau Chiến tranh lạnh',
                question: 'Câu 10: Sự khác biệt căn bản giữa cuộc cạnh tranh quyền lực sau Chiến tranh lạnh so với thời kỳ Chiến tranh lạnh là gì?',
                options: ['A. Tập trung vào cạnh tranh sức mạnh tổng hợp quốc gia (kinh tế, khoa học) thay vì đe dọa quân sự thuần túy.', 'B. Sử dụng chiến tranh hạt nhân trực tiếp giữa các nước lớn.', 'C. Không còn bất kỳ sự cạnh tranh nào giữa các quốc gia.', 'D. Chỉ diễn ra trên lĩnh vực thể thao và văn hóa nghệ thuật.'],
                correct: 0,
                explanation: 'Sau Chiến tranh lạnh, các quốc gia điều chỉnh chiến lược lấy phát triển kinh tế, sức mạnh tổng hợp làm trọng tâm.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Liên hợp quốc',
                question: 'Câu 11: Nguyên tắc hoạt động nào sau đây KHÔNG phải là nguyên tắc cơ bản được quy định trong Hiến chương Liên hợp quốc?',
                options: ['A. Tự do gia nhập các khối quân sự đa phương trên thế giới.', 'B. Bình đẳng về chủ quyền giữa các quốc gia thành viên.', 'C. Tôn trọng toàn vẹn lãnh thổ và độc lập chính trị của các nước.', 'D. Giải quyết các tranh chấp quốc tế bằng phương pháp hòa bình.'],
                correct: 0,
                explanation: 'Gia nhập khối quân sự không phải là nguyên tắc cơ bản trong Hiến chương LHQ.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Trật tự I-an-ta',
                question: 'Câu 12: Quyết định nào sau đây KHÔNG phải là của Hội nghị I-an-ta (tháng 02/1945)?',
                options: ['A. Thống nhất mục tiêu tiêu diệt tận gốc chủ nghĩa phát xít.', 'B. Thành lập tổ chức quốc tế Liên hợp quốc.', 'C. Thành lập Tổ chức Thương mại Thế giới (WTO).', 'D. Phân chia phạm vi ảnh hưởng ở châu Âu và châu Á.'],
                correct: 2,
                explanation: 'WTO thành lập năm 1995, không thuộc quyết định của Hội nghị Ianta 1945.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Phong trào GPDT',
                question: 'Câu 13: Đóng góp lớn nhất của Liên hợp quốc đối với phong trào giải phóng dân tộc trên thế giới trong thế kỷ XX là gì?',
                options: ['A. Thông qua Tuyên ngôn về thủ tiêu hoàn toàn chủ nghĩa thực dân (1960), ủng hộ quyền tự quyết.', 'B. Trực tiếp viện trợ vũ khí cho tất cả các cuộc khởi nghĩa vũ trang ở các nước thuộc địa.', 'C. Đưa lực lượng giữ gìn hòa bình vào giải phóng các vùng đất thuộc địa bị chiếm đóng.', 'D. Đã buộc tất cả các nước thực dân phải trao trả độc lập ngay sau năm 1945.'],
                correct: 0,
                explanation: 'Năm 1960, LHQ thông qua Tuyên ngôn thủ tiêu hoàn toàn chủ nghĩa thực dân thúc đẩy phi thực dân hóa trên toàn cầu.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Trật tự I-an-ta',
                question: 'Câu 14: Một trong những khu vực được Hội nghị I-an-ta (1945) quy định thuộc phạm vi ảnh hưởng của Mỹ là:',
                options: ['A. Tây Âu.', 'B. Đông Âu.', 'C. Mông Cổ.', 'D. Trung Đông.'],
                correct: 0,
                explanation: 'Theo thỏa thuận Ianta, khu vực Tây Âu thuộc phạm vi ảnh hưởng của Mỹ và các nước phương Tây.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Sụp đổ Trật tự 2 cực',
                question: 'Câu 15: Sự kiện lịch sử nào vào tháng 12/1991 đã đánh dấu sự sụp đổ hoàn toàn của Trật tự hai cực I-an-ta?',
                options: ['A. Sự sụp đổ của Liên bang Xô viết (Liên Xô tan rã).', 'B. Bức tường Béc-lin bị xóa bỏ (1989).', 'C. Nước Đức thống nhất (1990).', 'D. Định ước Hen-xinh-ki được ký kết (1975).'],
                correct: 0,
                explanation: 'Tháng 12/1991, Liên Xô sụp đổ đánh dấu Trật tự hai cực Ianta hoàn toàn chấm dứt.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Quan hệ Quốc tế',
                question: 'Câu 16: Xu thế hòa hoãn Đông - Tây bắt đầu xuất hiện từ đầu những năm 70 của thế kỷ XX với biểu hiện nào sau đây?',
                options: ['A. Những cuộc gặp gỡ cấp cao Xô - Mỹ và các thỏa thuận hạn chế vũ khí tiến công chiến lược (SALT-1).', 'B. Liên Xô và Mỹ tuyên bố rút khỏi tất cả các căn cứ quân sự ở nước ngoài.', 'C. Sự giải thể ngay lập tức của hai khối NATO và Vác-sa-va.', 'D. Mỹ hoàn toàn chấm dứt viện trợ cho chính quyền Sài Gòn.'],
                correct: 0,
                explanation: 'Các cuộc gặp cấp cao Xô - Mỹ ký kết SALT-1 (1972) mở đầu cho xu thế hòa hoãn Đông - Tây.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Chấm dứt CT Lạnh',
                question: 'Câu 17: Đâu là một trong những nguyên nhân Mỹ và Liên Xô quyết định chấm dứt cuộc Chiến tranh lạnh (1947 - 1989)?',
                options: ['A. Sự suy giảm thế và lực của cả hai nước do cuộc chạy đua vũ trang tốn kém.', 'B. Nước Mỹ gặp khủng hoảng nghiêm trọng do các bang ly khai.', 'C. Liên Xô vươn lên vượt trội hoàn toàn về kinh tế.', 'D. Nhân dân hai nước phản đối Chiến tranh lạnh.'],
                correct: 0,
                explanation: 'Cuộc chạy đua vũ trang tốn kém làm suy giảm tiềm lực kinh tế của cả hai siêu cường Mỹ và Liên Xô.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Khởi đầu CT Lạnh',
                question: 'Câu 18: Sự kiện nào được coi là khởi đầu cho chính sách đối đầu chống Liên Xô của Mỹ, mở đầu cuộc Chiến tranh lạnh?',
                options: ['A. Thông điệp của Tổng thống Tơ-ru-man tại Quốc hội Mỹ (tháng 03/1947).', 'B. Mỹ triển khai Kế hoạch Mác-san trợ giúp châu Âu (tháng 06/1947).', 'C. Thành lập Khối quân sự Bắc Đại Tây Dương - NATO (tháng 04/1949).', 'D. Thành lập Tổ chức Hiệp ước Vác-sa-va (tháng 05/1955).'],
                correct: 0,
                explanation: 'Thông điệp Tổng thống Truman (3/1947) là mốc mở đầu cho thời kỳ Chiến tranh lạnh.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Cục diện Hai cực',
                question: 'Câu 19: Sự ra đời của khối NATO (1949) và Tổ chức Hiệp ước Vác-sa-va (1955) dẫn đến hệ quả gì trong quan hệ quốc tế?',
                options: ['A. Đã đánh dấu sự phát triển vượt bậc của hai nước.', 'B. Chấm dứt mối quan hệ đồng minh giữa Xô - Mỹ.', 'C. Hàng loạt các tổ chức quân sự trên thế giới ra đời.', 'D. Đánh dấu sự xác lập của cục diện hai cực, hai phe.'],
                correct: 3,
                explanation: 'Sự ra đời của 2 liên minh quân sự NATO và Vác-sa-va xác lập cục diện hai cực hai phe về quân sự.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Trật tự mới',
                question: 'Câu 20: Trật tự thế giới đang trong quá trình hình thành sau Chiến tranh lạnh có đặc điểm nổi bật là:',
                options: ['A. Xu thế đa cực với sự vươn lên của nhiều trung tâm quyền lực.', 'B. Trật tự đơn cực tuyệt đối do Mỹ hoàn toàn chi phối.', 'C. Trật tự hai cực mới giữa Mỹ và Nhật Bản.', 'D. Sự thống trị hoàn toàn của các nước tư bản phương Tây.'],
                correct: 0,
                explanation: 'Sau Chiến tranh lạnh, trật tự thế giới mới đang hình thành theo xu hướng đa cực.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Nhóm G7',
                question: 'Câu 21: Quốc gia nào sau đây nằm trong nhóm G7?',
                options: ['A. Thái Lan.', 'B. Việt Nam.', 'C. Nhật Bản.', 'D. Ai Cập.'],
                correct: 2,
                explanation: 'Nhóm G7 bao gồm 7 quốc gia công nghiệp phát triển: Mỹ, Anh, Pháp, Đức, Nhật Bản, Canada, Ý.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Biểu tượng CT Lạnh',
                question: 'Câu 22: Một trong những biểu tượng cho sự kết thúc Chiến tranh lạnh là:',
                options: ['A. Liên Xô chính thức sụp đổ (1991).', 'B. Bức tường Béc-lin sụp đổ (11/1989).', 'C. Chiến tranh Việt Nam kết thúc (1975).', 'D. Vấn đề Nam Xu-đăng được giải quyết.'],
                correct: 1,
                explanation: 'Sự sụp đổ Bức tường Béc-lin (11/1989) là biểu tượng hàng đầu cho sự kết thúc Chiến tranh lạnh ở châu Âu.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Nhóm G20',
                question: 'Câu 23: “Chiếm 2/3 dân số, 90% GDP, 80% thương mại toàn cầu”. Những số liệu này đang nói đến tổ chức nào?',
                options: ['A. G20.', 'B. NICs.', 'C. EU.', 'D. ASEAN.'],
                correct: 0,
                explanation: 'Nhóm G20 đại diện cho khoảng 2/3 dân số thế giới, 90% GDP và 80% thương mại toàn cầu.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Chiến lược Phát triển',
                question: 'Câu 24: Vì sao sau Chiến tranh lạnh, các quốc gia lại coi phát triển kinh tế là trung tâm trong chiến lược quốc gia?',
                options: ['A. Vì sức mạnh tổng hợp quốc gia (đặc biệt là kinh tế) quyết định vị thế và quyền lực trong trật tự mới.', 'B. Vì tất cả các cuộc xung đột quân sự trên thế giới đã chấm dứt vĩnh viễn.', 'C. Vì ngân sách dành cho quốc phòng đã bị cấm bởi Luật pháp quốc tế.', 'D. Vì các nước lớn đã tự nguyện chia sẻ tài nguyên kinh tế cho nhau.'],
                correct: 0,
                explanation: 'Sức mạnh tổng hợp quốc gia dựa trên trụ cột kinh tế quyết định vị thế của mỗi quốc gia.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Xu thế thế giới',
                question: 'Câu 25: Nội dung nào sau đây KHÔNG phản ánh đúng xu thế phát triển của thế giới sau Chiến tranh lạnh?',
                options: ['A. Một trật tự thế giới mới hình thành theo hướng đa cực.', 'B. Các nước điều chỉnh chiến lược tập trung phát triển kinh tế.', 'C. Các cuộc xung đột quân sự vẫn còn diễn ra ở một số khu vực.', 'D. Mỹ đã thực hiện thành công âm mưu thiết lập trật tự thế giới đơn cực.'],
                correct: 3,
                explanation: 'Mỹ không thể thực hiện thành công trật tự đơn cực do sự vươn lên mạnh mẽ của các trung tâm quyền lực khác.'
            },

            // CHỦ ĐỀ 2 (9 CÂU)
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Thành lập ASEAN',
                question: 'Câu 26: Yếu tố chủ quan quan trọng nhất thúc đẩy sự ra đời của ASEAN năm 1967 là gì?',
                options: ['A. Nhu cầu hợp tác liên kết khu vực để cùng phát triển kinh tế và hạn chế sự can thiệp của các cường quốc.', 'B. Sự ép buộc quân sự từ phía các nước tư bản phương Tây.', 'C. Nhằm xây dựng một khối liên minh quân sự chống lại Liên Xô.', 'D. Sự hỗ trợ tài chính trực tiếp từ Ngân hàng Thế giới.'],
                correct: 0,
                explanation: 'Sự liên kết khu vực giúp các nước Đông Nam Á hợp tác phát triển kinh tế và hạn chế ảnh hưởng từ các nước lớn.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Nguyên tắc ASEAN',
                question: 'Câu 27: Văn kiện pháp lý đầu tiên đặt nền móng cho các nguyên tắc quan hệ giữa các nước ASEAN là:',
                options: ['A. Hiệp ước Thân thiện và Hợp tác ở Đông Nam Á (Hiệp ước Bali 1976).', 'B. Hiến chương ASEAN (2007).', 'C. Tuyên bố Băng Cốc (1967).', 'D. Tuyên bố Hòa bình ZOPFAN (1971).'],
                correct: 0,
                explanation: 'Hiệp ước Bali (1976) xác định những nguyên tắc cốt lõi trong quan hệ đối ngoại giữa các nước thành viên.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Mở rộng ASEAN',
                question: 'Câu 28: Nội dung nào sau đây là khó khăn trong quá trình mở rộng thành viên của ASEAN từ sau khi Chiến tranh lạnh kết thúc (1989)?',
                options: ['A. Sự khác biệt về thể chế chính trị.', 'B. Tác động từ các nước châu Âu.', 'C. Mâu thuẫn gay gắt về tôn giáo.', 'D. Tác động từ chủ nghĩa khủng bố.'],
                correct: 0,
                explanation: 'Sự khác biệt về thể chế chính trị giữa các quốc gia Đông Nam Á từng là trở ngại lớn cho mở rộng ASEAN.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Cộng đồng ASEAN',
                question: 'Câu 29: Mục tiêu xây dựng Cộng đồng ASEAN là:',
                options: ['A. Biến ASEAN thành tổ chức hợp tác mạnh nhất.', 'B. Các nước đoàn kết giúp đỡ nhau khi bị xâm lược.', 'C. Củng cố khối đoàn kết của ASEAN trên vấn đề quân sự.', 'D. Đưa ASEAN trở thành một cộng đồng ràng buộc hơn.'],
                correct: 3,
                explanation: 'Xây dựng Cộng đồng ASEAN nhằm nâng cao mức độ liên kết chặt chẽ và có tính ràng buộc pháp lý cao hơn.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Cơ sở pháp lý ASEAN',
                question: 'Câu 30: Đâu là cơ sở pháp lý để các nước Đông Nam Á xây dựng Cộng đồng ASEAN?',
                options: ['A. Hiến chương ASEAN.', 'B. Tuyên bố Băng Cốc.', 'C. Hiến chương Liên hợp quốc.', 'D. Hiệp ước Bali 1976.'],
                correct: 0,
                explanation: 'Hiến chương ASEAN thông qua năm 2007 tạo cơ sở pháp lý vững chắc cho việc hình thành Cộng đồng ASEAN.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Bước ngoặt ASEAN',
                question: 'Câu 31: Sự kiện nào đánh dấu bước ngoặt chuyển biến của ASEAN từ hợp tác lỏng lẻo sang liên kết chặt chẽ?',
                options: ['A. Hội nghị Cấp cao ASEAN lần thứ nhất tại Bali (1976) và ký Hiệp ước Bali.', 'B. Sự gia nhập của thành viên thứ 10 Cam-pu-chia (1999).', 'C. Việc ban hành Hiến chương ASEAN có hiệu lực năm 2008.', 'D. Sự ra đời của Tuyên bố ZOPFAN năm 1971.'],
                correct: 0,
                explanation: 'Hội nghị Bali (1976) với việc ký kết Hiệp ước TAC là bước ngoặt chuyển ASEAN sang giai đoạn liên kết chặt chẽ.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Trụ cột Cộng đồng ASEAN',
                question: 'Câu 32: Ba trụ cột chính cấu thành Cộng đồng ASEAN (chính thức thành lập ngày 31/12/2015) bao gồm:',
                options: ['A. Cộng đồng Chính trị - An ninh, Cộng đồng Kinh tế, Cộng đồng Văn hóa - Xã hội.', 'B. Cộng đồng Quân sự, Cộng đồng Kinh tế, Cộng đồng Giáo dục.', 'C. Cộng đồng An ninh quốc phòng, Cộng đồng Thương mại, Cộng đồng Du lịch.', 'D. Cộng đồng Ngoại giao, Cộng đồng Tài chính, Cộng đồng Dân số.'],
                correct: 0,
                explanation: '3 trụ cột Cộng đồng ASEAN: APSC (Chính trị-An ninh), AEC (Kinh tế), ASCC (Văn hóa-Xã hội).'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Biển Đông & Hiệp ước Bali',
                question: 'Câu 33: Nguyên tắc hoạt động nào của Hiệp ước Bali (1976) vẫn giữ nguyên giá trị cốt lõi trong giải quyết các tranh chấp Biển Đông hiện nay?',
                options: ['A. Tôn trọng độc lập, chủ quyền, toàn vẹn lãnh thổ và giải quyết tranh chấp bằng phương pháp hòa bình.', 'B. Cho phép sử dụng đe dọa quân sự đối với các nước nhỏ.', 'C. Đơn phương thành lập các vùng cấm bay trên biển.', 'D. Bỏ qua các quy định của Luật pháp quốc tế UNCLOS 1982.'],
                correct: 0,
                explanation: 'Giải quyết hòa bình các tranh chấp trên cơ sở tôn trọng độc lập chủ quyền là giá trị cốt lõi của ASEAN.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Bản chất Cộng đồng ASEAN',
                question: 'Câu 34: Sự ra đời của Cộng đồng ASEAN (2015) có bản chất là gì?',
                options: ['A. Sự nâng cấp quá trình liên kết khu vực lên mức độ sâu rộng, có tổ chức và ràng buộc pháp lý cao hơn.', 'B. Việc sáp nhập 10 quốc gia Đông Nam Á thành một liên bang.', 'C. Sự thành lập một liên minh phòng thủ quân sự chống lại các nước tư bản.', 'D. Việc xóa bỏ hoàn toàn vai trò của các Chính phủ quốc gia.'],
                correct: 0,
                explanation: 'Cộng đồng ASEAN nâng tầm liên kết khu vực sâu rộng hơn về tổ chức và thể chế pháp lý.'
            },

            // CHỦ ĐỀ 3 (17 CÂU)
            {
                topic: 'cd3',
                category: 'Chủ đề 3: CM Tháng Tám 1945',
                question: 'Câu 35: Một trong những địa phương giành được chính quyền sớm nhất trong Tổng khởi nghĩa tháng Tám năm 1945 là:',
                options: ['A. Thanh Hóa.', 'B. Quảng Nam.', 'C. Hưng Yên.', 'D. Cao Bằng.'],
                correct: 1,
                explanation: '4 tỉnh giành chính quyền sớm nhất trong cả nước ngày 18/8/1945 là: Bắc Giang, Hải Dương, Hà Tĩnh và Quảng Nam.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: CM Tháng Tám 1945',
                question: 'Câu 36: Một trong những địa phương giành chính quyền sau cùng trong Tổng khởi nghĩa tháng Tám năm 1945 là:',
                options: ['A. Cần Thơ.', 'B. Hà Tiên.', 'C. Móng Cái.', 'D. Lai Châu.'],
                correct: 1,
                explanation: 'Hai tỉnh giành chính quyền muộn nhất cả nước là Đồng Nai Nhiễm và Hà Tiên (ngày 28/8/1945).'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: CM Tháng Tám 1945',
                question: 'Câu 37: Ngày 13/8/1945, Trung ương Đảng và Tổng bộ Việt Minh đã thông qua quyết định nào dưới đây?',
                options: ['A. Quyết định khởi nghĩa ở Hà Nội.', 'B. Phát động cao trào kháng Nhật.', 'C. Phát lệnh Tổng khởi nghĩa cả nước.', 'D. Thống nhất lực lượng vũ trang Việt Nam.'],
                correct: 2,
                explanation: 'Đêm 13/8/1945, Ủy ban Khởi nghĩa toàn quốc ra Quân lệnh số 1 chính thức phát lệnh Tổng khởi nghĩa.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: CM Tháng Tám 1945',
                question: 'Câu 38: Hội nghị toàn quốc của Đảng Cộng sản Đông Dương họp ở Tân Trào (14 - 15/8/1945) đã:',
                options: ['A. Thống nhất các lực lượng vũ trang.', 'B. Quyết định khởi nghĩa ở Hà Nội.', 'C. Quyết định phát động Tổng khởi nghĩa giành chính quyền.', 'D. Giải phóng dân tộc trong năm 1945.'],
                correct: 2,
                explanation: 'Hội nghị toàn quốc của Đảng họp tại Tân Trào thông qua quyết định phát động Tổng khởi nghĩa giành chính quyền.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: CM Tháng Tám 1945',
                question: 'Câu 39: Thời cơ khách quan thuận lợi của Cách mạng tháng Tám là sự kiện nào sau đây?',
                options: ['A. Nhật đảo chính lật đổ Pháp trên toàn Đông Dương (9/3/1945).', 'B. Mỹ ném hai quả bom nguyên tử xuống Nhật (6, 9/8/1945).', 'C. Đức đã đầu hàng quân Đồng minh vô điều kiện (9/5/1945).', 'D. Phát xít Nhật đầu hàng Đồng minh vô điều kiện (15/8/1945).'],
                correct: 3,
                explanation: 'Sự kiện Phát xít Nhật đầu hàng Đồng minh vô điều kiện (15/8/1945) tạo thời cơ khách quan thuận lợi ngàn năm có một.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: CM Tháng Tám 1945',
                question: 'Câu 40: Sự kiện nào sau đây đánh dấu nước Việt Nam Dân chủ Cộng hòa được thành lập?',
                options: ['A. Hồ Chí Minh đọc Tuyên ngôn độc lập (2/9/1945).', 'B. Đại hội Quốc dân họp ở Tân Trào (8/1945).', 'C. Hội nghị đại biểu toàn quốc của Đảng (8/1945).', 'D. Tiến hành Tổng tuyển cử bầu Quốc hội (1/1946).'],
                correct: 0,
                explanation: 'Ngày 2/9/1945, Bác Hồ đọc Tuyên ngôn Độc lập chính thức khai sinh ra nước Việt Nam Dân chủ Cộng hòa.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: CM Tháng Tám 1945',
                question: 'Câu 41: Một trong những nguyên nhân khách quan dẫn tới thắng lợi của Cách mạng tháng Tám (1945) là:',
                options: ['A. Những thắng lợi của khối Đồng minh chống phát xít.', 'B. Sự chuẩn bị của Đảng trong 15 năm.', 'C. Tinh thần đoàn kết của nhân dân.', 'D. Sự giúp đỡ của Liên Xô, Trung Quốc.'],
                correct: 0,
                explanation: 'Thắng lợi của phe Đồng minh tiêu diệt phát xít Đức, Nhật là nguyên nhân khách quan quan trọng.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: CM Tháng Tám 1945',
                question: 'Câu 42: Đại hội Quốc dân họp ở Tân Trào (từ ngày 16 - 17/8/1945) đã thể hiện:',
                options: ['A. Ý chí thống nhất đoàn kết và nguyện vọng của toàn dân.', 'B. Cuộc Tổng khởi nghĩa đã diễn ra và thắng lợi nhanh chóng.', 'C. Chủ trương Tổng khởi nghĩa giành chính quyền của Đảng.', 'D. Quyết tâm phối hợp với phe Đồng minh để chống phát xít.'],
                correct: 0,
                explanation: 'Đại hội Quốc dân Tân Trào thể hiện sự đoàn kết, nhất trí cao độ của toàn thể nhân dân Việt Nam.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Sụp đổ Phong kiến',
                question: 'Câu 43: Sự kiện nào dưới đây đánh dấu chế độ phong kiến ở Việt Nam đã sụp đổ hoàn toàn?',
                options: ['A. Giành được chính quyền ở Hà Nội.', 'B. Vua Bảo Đại đã tuyên bố thoái vị (30/8/1945).', 'C. Khởi nghĩa thắng lợi trong cả nước.', 'D. Hồ Chí Minh đọc Tuyên ngôn Độc lập.'],
                correct: 1,
                explanation: 'Ngày 30/8/1945, Vua Bảo Đại thoái vị trao ấn kiếm cho chính quyền cách mạng, chấm dứt chế độ phong kiến.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Ý nghĩa Lịch sử',
                question: 'Câu 44: Thắng lợi nào của nhân dân Việt Nam đã góp phần xóa bỏ chủ nghĩa phát xít trên thế giới?',
                options: ['A. Cách mạng tháng Tám 1945.', 'B. Hiệp định Giơ-ne-vơ được ký kết.', 'C. Hiệp định Pa-ri được ký kết.', 'D. Chính quyền Xô viết thành lập.'],
                correct: 0,
                explanation: 'Cách mạng tháng Tám đánh bại phát xít Nhật ở Đông Dương, góp phần cùng quân Đồng minh tiêu diệt chủ nghĩa phát xít.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Nguyên nhân Thắng lợi',
                question: 'Câu 45: Nguyên nhân nào sau đây là nhân tố quyết định dẫn tới thắng lợi của Tổng khởi nghĩa tháng Tám năm 1945?',
                options: ['A. Sự lãnh đạo sáng suốt của Đảng Cộng sản Đông Dương.', 'B. Tinh thần đoàn kết quốc tế vô sản.', 'C. Nhật đầu hàng quân Đồng minh.', 'D. Thắng lợi của Hồng quân Liên Xô.'],
                correct: 0,
                explanation: 'Sự lãnh đạo đúng đắn, sáng suốt của Đảng đứng đầu là Chủ tịch Hồ Chí Minh là nhân tố quyết định nhất.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Bác Hồ & CM Tháng Tám',
                question: 'Câu 46: Nhận định nào sau đây đúng về vai trò của Chủ tịch Hồ Chí Minh đối với thắng lợi của Cách mạng tháng Tám 1945?',
                options: ['A. Trực tiếp cùng với Đảng lãnh đạo cuộc Cách mạng tháng Tám thắng lợi.', 'B. Liên hệ với Trung Quốc, Liên Xô để tranh thủ sự ủng hộ cho cách mạng.', 'C. Lập và thông qua danh sách chính phủ lâm thời của nước Việt Nam mới.', 'D. Trực tiếp lãnh đạo lực lượng vũ trang đánh chiếm cơ quan đầu não kẻ thù.'],
                correct: 0,
                explanation: 'Chủ tịch Hồ Chí Minh là linh hồn, trực tiếp cùng Trung ương Đảng lãnh đạo Tổng khởi nghĩa thành công.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Bối cảnh Kháng chiến',
                question: 'Câu 47: Một trong những nội dung của tình hình thế giới khi cuộc kháng chiến chống Pháp (1945 - 1954) của nhân dân Việt Nam nổ ra là:',
                options: ['A. Hệ thống xã hội chủ nghĩa đang hình thành.', 'B. Cách mạng Cuba đã giành được thắng lợi.', 'C. Xu thế hòa hoãn Đông - Tây đã xuất hiện.', 'D. Chiến lược toàn cầu của Mỹ đang thất bại.'],
                correct: 0,
                explanation: 'Sau CTTG2, hệ thống xã hội chủ nghĩa được hình thành từ châu Âu sang châu Á.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Kháng chiến Nam Bộ',
                question: 'Câu 48: Khi Pháp xâm lược Nam Bộ (9/1945), Đảng và Chính phủ Việt Nam đã có hành động nào sau đây?',
                options: ['A. Đã tiến hành đàm phán khẩn cấp với Pháp.', 'B. Tố cáo hành vi của Pháp đến Liên hợp quốc.', 'C. Đưa toàn bộ quân đội vào Nam chiến đấu.', 'D. Huy động cả nước để chi viện cho Nam Bộ.'],
                correct: 3,
                explanation: 'Đảng và Chính phủ phát động phong trào Nam tiến, huy động nhân lực, vật lực cả nước chi viện cho Nam Bộ.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Đường lối Kháng chiến',
                question: 'Câu 49: Một trong những nội dung của đường lối kháng chiến chống Pháp (1945 - 1954) là:',
                options: ['A. Đoàn kết kháng chiến.', 'B. Vườn không nhà trống.', 'C. Toàn dân kháng chiến.', 'D. Đánh nhanh thắng nhanh.'],
                correct: 2,
                explanation: 'Đường lối kháng chiến chống Pháp: Toàn dân, toàn diện, trường kỳ, tự lực cánh sinh và tranh thủ sự ủng hộ quốc tế.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Chiến dịch Biên giới 1950',
                question: 'Câu 50: Quân dân Việt Nam đã giành quyền chủ động trên chiến trường chính Bắc Bộ sau thắng lợi của chiến dịch nào sau đây?',
                options: ['A. Tầm Vũ (1948).', 'B. Biên giới (1950).', 'C. Việt Bắc (1947).', 'D. Hòa Bình (1951).'],
                correct: 1,
                explanation: 'Chiến dịch Biên giới thu - đông 1950 thắng lợi giúp ta giành quyền chủ động chiến lược trên chiến trường chính Bắc Bộ.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Điện Biên Phủ 1954',
                question: 'Câu 51: Âm mưu chính của Pháp - Mỹ khi xây dựng tập đoàn cứ điểm Điện Biên Phủ là nhằm:',
                options: ['A. Thu hút và tiêu diệt bộ đội chủ lực Việt Nam.', 'B. Bảo vệ vùng Tây Bắc, khóa chặt biên giới.', 'C. Giành lại thế chủ động trên chiến trường.', 'D. Ngăn chặn sự liên lạc giữa Việt Nam và Lào.'],
                correct: 0,
                explanation: 'Pháp - Mỹ coi Điện Biên Phủ là cái bẫy nhằm thu hút và tiêu diệt lực lượng chủ lực của ta.'
            }
        ];

        /* CLUSTER TRUE / FALSE QUESTIONS (23 CLUSTERS WITH FULL TEXT PASSAGES) */
        const historyTF = [
            // CHỦ ĐỀ 1 (6 CHÙM)
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Tư liệu Liên hợp quốc',
                question: 'Chùm câu 1: Đọc đoạn tư liệu về Mục đích và Nguyên tắc của Liên hợp quốc:',
                passage: 'Điều 1: Hiến chương Liên hợp quốc quy định mục đích của Liên hợp quốc là: 1. Duy trì hòa bình và an ninh quốc tế, và để đạt được mục đích đó, thực hiện các biện pháp tập thể có hiệu quả... 2. Phát triển mối quan hệ hữu nghị giữa các dân tộc dựa trên cơ sở tôn trọng nguyên tắc bình đẳng về quyền lợi và tự quyết của các dân tộc... Điều 2: Tổ chức này được xây dựng trên nguyên tắc bình đẳng chủ quyền của tất cả các quốc gia thành viên.\n(Hiến chương Liên hợp quốc 1945, NXB Chính trị Quốc gia, 2002)',
                statements: [
                    'a) Mục đích bao trùm và hàng đầu của Liên hợp quốc là duy trì hòa bình và an ninh quốc tế.',
                    'b) Hiến chương Liên hợp quốc thừa nhận nguyên tắc tự quyết của các dân tộc.',
                    'c) Nguyên tắc bình đẳng chủ quyền chỉ áp dụng cho các cường quốc lớn thắng trận.',
                    'd) Đoạn tư liệu khẳng định Liên hợp quốc được thành lập nhằm can thiệp trực tiếp vào nội bộ các nước.'
                ],
                correct: [true, true, false, false],
                explanation: 'a) Đúng. b) Đúng. c) Sai (Áp dụng bình đẳng cho TẤT CẢ các quốc gia thành viên). d) Sai (Hiến chương quy định không can thiệp vào công việc nội bộ).'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Tư liệu Hội đồng Bảo an',
                question: 'Chùm câu 2: Đọc đoạn tư liệu về Trách nhiệm của Hội đồng Bảo an Liên hợp quốc:',
                passage: 'Để bảo đảm cho Liên hợp quốc hành động nhanh chóng và có hiệu quả, các thành viên Liên hợp quốc trao cho Hội đồng Bảo an trách nhiệm chính trong việc duy trì hòa bình và an ninh quốc tế, và thừa nhận rằng khi làm những nghĩa vụ do trách nhiệm đó đặt ra, Hội đồng Bảo an hành động với tư cách thay mặt cho các thành viên Liên hợp quốc.\n(Giáo trình Luật Quốc tế, NXB Công an Nhân dân, 2018)',
                statements: [
                    'a) Hội đồng Bảo an là cơ quan duy nhất chịu trách nhiệm về văn hóa và giáo dục của Liên hợp quốc.',
                    'b) Khi Hội đồng Bảo an ra quyết định về an ninh, các thành viên Liên hợp quốc có nghĩa vụ tôn trọng.',
                    'c) Quyết định của Hội đồng Bảo an đại diện cho quyền lực tập thể của các quốc gia thành viên.',
                    'd) Đoạn tư liệu chứng minh Đại hội đồng phải thông qua tất cả quyết định quân sự của Hội đồng Bảo an.'
                ],
                correct: [false, true, true, false],
                explanation: 'a) Sai (HĐBA duy trì hòa bình/an ninh). b) Đúng. c) Đúng. d) Sai (HĐBA có quyền quyết định độc lập mang tính ràng buộc).'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Tư liệu Quan hệ Quốc tế',
                question: 'Chùm câu 3: Đọc đoạn tư liệu về Phương thức quan hệ quốc tế:',
                passage: 'Bài học của thời kì Chiến tranh lạnh đã chứng tỏ phương thức quan hệ quốc tế lấy đối đầu chính trị - quân sự là chủ yếu không còn phù hợp, phải chịu nhiều tổn thất hoặc thất bại như hai nước Xô - Mỹ và một bị thương, một bị mất. Trong khi đó, phương thức lấy hợp tác và cạnh tranh về kinh tế - chính trị là chính lại thu được nhiều tiến bộ, kết quả như các nước Đức, Nhật và NICs. Sự hưng thịnh hay suy vong của một quốc gia quyết định bởi sức mạnh tổng hợp của quốc gia đó, mà chủ yếu là thực lực kinh tế và khoa học - kỹ thuật.\n(Vũ Dương Ninh (Chủ biên), Một số chuyên đề lịch sử thế giới, NXB Đại học Quốc gia Hà Nội, Hà Nội, 2002, tr.401)',
                statements: [
                    'a) Hợp tác về kinh tế - chính trị làm suy yếu tiềm lực phát triển của từng nước.',
                    'b) Tình trạng đối đầu của Mỹ và Liên Xô trong Chiến tranh lạnh khiến cho hai nước chịu nhiều tổn thất.',
                    'c) Thực lực kinh tế và khoa học - kỹ thuật có vai trò quan trọng đối với sự phát triển của một quốc gia.',
                    'd) Đoạn tư liệu thể hiện xu thế phát triển chính của thế giới sau Chiến tranh lạnh.'
                ],
                correct: [false, true, true, true],
                explanation: 'a) Sai (Hợp tác kinh tế giúp các nước thu nhiều kết quả tích cực). b, c, d) Đúng.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Tư liệu Tuyên bố Manta',
                question: 'Chùm câu 4: Đọc đoạn tư liệu Tuyên bố Manta chấm dứt Chiến tranh lạnh (12/1989):',
                passage: 'Tại cuộc gặp cấp cao ở Manta, Tổng bí thư Đảng Cộng sản Liên Xô M. Goóc-ba-chốp và Tổng thống Mỹ G. Bơ-xơ (cha) tuyên bố hai nước không còn xem nhau là kẻ thù và chính thức cùng tuyên bố chấm dứt Chiến tranh lạnh.\n(Tạp chí Quan hệ Quốc tế, Số 12/1989)',
                statements: [
                    'a) Cuộc gặp cấp cao Manta diễn ra giữa lãnh đạo hai siêu cường Mỹ và Liên Xô.',
                    'b) Hai bên chính thức tuyên bố chấm dứt thời kỳ Chiến tranh lạnh kéo dài hơn bốn thập kỷ.',
                    'c) Tuyên bố Manta đã giải thể ngay lập tức Liên bang Xô viết.',
                    'd) Sự kiện Manta tạo ra chuyển biến tích cực trong tổng thể quan hệ giữa Mỹ và Liên Xô.'
                ],
                correct: [true, true, false, true],
                explanation: 'a) Đúng (Gorbachov & Bush). b) Đúng. c) Sai (Liên Xô tan rã tháng 12/1991). d) Đúng.'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Tư liệu Trật tự mới',
                question: 'Chùm câu 5: Đọc đoạn tư liệu về Trật tự thế giới sau Chiến tranh lạnh:',
                passage: 'Trật tự thế giới mới này được hình thành như thế nào, còn tùy thuộc ở nhiều nhân tố: Sự phát triển về kinh tế, chính trị, quân sự của các cường quốc Mỹ, Nga, Trung Quốc, Anh, Pháp, Nhật Bản, Đức trong cuộc chạy đua về sức mạnh quốc gia tổng hợp... Sự lớn mạnh của lực lượng cách mạng thế giới (sự thành công của công cuộc cải cách, đổi mới ở các nước xã hội chủ nghĩa)...; Sự phát triển của cách mạng khoa học - kỹ thuật sẽ còn tiếp tục tạo ra những "đột phá" và biến chuyển trên diện thế giới.\n(Nguyễn Anh Thái (Chủ biên), Lịch sử thế giới hiện đại, NXB Giáo dục Việt Nam, Hà Nội, 2021, tr.424)',
                statements: [
                    'a) Một trong những đặc điểm nổi bật của trật tự thế giới mới được thiết lập sau Chiến tranh lạnh là thế giới bị chia thành hai hệ thống xã hội đối lập.',
                    'b) Nhân tố đóng vai trò quyết định đến sự hình thành trật tự thế giới hiện nay là cuộc chạy đua sức mạnh quốc gia tổng hợp, trong đó sức mạnh kinh tế là trụ cột.',
                    'c) Một trong những nhân tố tác động đến sự hình thành trật tự thế giới mới sau Chiến tranh lạnh là sự vươn lên mạnh mẽ của các nước Á, Phi, Mỹ Latinh.',
                    'd) "Trật tự thế giới mới" được nhắc đến trong đoạn tư liệu trên là trật tự thế giới "hai cực I-an-ta".'
                ],
                correct: [false, true, true, false],
                explanation: 'a) Sai (Đó là đặc điểm Trật tự Ianta cũ). b) Đúng. c) Đúng. d) Sai (Đang nói về trật tự đa cực hiện đại).'
            },
            {
                topic: 'cd1',
                category: 'Chủ đề 1: Tư liệu Thông điệp Truman',
                question: 'Chùm câu 6: Đọc đoạn tư liệu Diễn văn của Tổng thống Mỹ Truman tại Quốc hội (12/3/1947):',
                passage: 'Tôi tin rằng chính sách của Hoa Kỳ phải là hỗ trợ các dân tộc tự do đang chống lại cỗ máy khuất phục bởi các thiểu số có vũ trang hoặc bởi áp lực từ bên ngoài... Mọi quốc gia hiện nay phải lựa chọn giữa các chế độ sinh hoạt khác nhau. Một chế độ dựa trên tự do... Chế độ kia dựa trên ý chí của thiểu số cưỡng ép đa số.\n(Diễn văn của Tổng thống Truman tại Quốc hội Mỹ, 12/3/1947)',
                statements: [
                    'a) Thông điệp của Truman chính thức khởi động chính sách chống Liên Xô và các nước XHCN.',
                    'b) Văn kiện phân chia thế giới thành hai chế độ sinh hoạt đối lập nhau.',
                    'c) Mục tiêu của Mỹ là hỗ trợ tất cả các phong trào cách mạng vô sản trên toàn cầu.',
                    'd) Thông điệp này là mốc mở đầu cho thời kỳ Chiến tranh lạnh do Mỹ phát động.'
                ],
                correct: [true, true, false, true],
                explanation: 'a, b) Đúng. c) Sai (Mỹ chống lại các phong trào cách mạng vô sản). d) Đúng.'
            },

            // CHỦ ĐỀ 2 (7 CHÙM)
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Tư liệu Tuyên bố Băng Cốc',
                question: 'Chùm câu 7: Đọc đoạn tư liệu Tuyên bố Băng Cốc thành lập ASEAN (1967):',
                passage: 'Đại diện 5 nước (In-đô-nê-xi-a, Ma-lai-xi-a, Phi-lip-pin, Xanh-ga-po, Thái Lan) tuyên bố thành lập Hiệp hội các quốc gia Đông Nam Á. Mục tiêu: Thúc đẩy tăng trưởng kinh tế, tiến bộ xã hội và phát triển văn hóa trong khu vực thông qua các nỗ lực chung trên tinh thần bình đẳng và hợp tác.\n(Tuyên bố Băng Cốc 1967, Tài liệu ASEAN)',
                statements: [
                    'a) Tuyên bố Băng Cốc là văn kiện sáng lập ra tổ chức ASEAN.',
                    'b) ASEAN ban đầu gồm 5 quốc gia sáng lập thuộc khu vực Đông Nam Á.',
                    'c) Mục tiêu ban đầu của ASEAN khi mới thành lập là xây dựng liên minh quân sự.',
                    'd) Tuyên bố nhấn mạnh tinh thần hợp tác bình đẳng giữa các quốc gia thành viên.'
                ],
                correct: [true, true, false, true],
                explanation: 'a, b) Đúng (Indo, Malay, Phil, Sing, Thái). c) Sai (ASEAN không phải liên minh quân sự). d) Đúng.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Tư liệu Hiệp ước Bali',
                question: 'Chùm câu 8: Đọc đoạn tư liệu Hiệp ước Thân thiện và Hợp tác ở Đông Nam Á (Hiệp ước Bali 1976):',
                passage: 'Hiệp ước Thân thiện và Hợp tác ở Đông Nam Á (TAC) quy định các nguyên tắc cơ bản: Tôn trọng độc lập, chủ quyền, bình đẳng, toàn vẹn lãnh thổ; Không can thiệp vào công việc nội bộ của nhau; Giải quyết các bất đồng hoặc tranh chấp bằng biện pháp hòa bình; Tuyên bố không sử dụng vũ lực.\n(Văn kiện Cấp cao ASEAN lần thứ nhất, Bali, 1976)',
                statements: [
                    'a) Hiệp ước Bali xác định các nguyên tắc pháp lý cốt lõi trong quan hệ đối ngoại ASEAN.',
                    'b) Nguyên tắc không can thiệp vào công việc nội bộ là một trụ cột của Hiệp ước.',
                    'c) Hiệp ước Bali cho phép các nước thành viên sử dụng quân đội giải quyết tranh chấp.',
                    'd) Hiệp ước đánh dấu bước chuyển biến quan trọng trong quá trình củng cố ASEAN.'
                ],
                correct: [true, true, false, true],
                explanation: 'a, b) Đúng. c) Sai (Cấm sử dụng hoặc đe dọa sử dụng vũ lực). d) Đúng.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Tư liệu Tuyên bố Kuala Lumpur',
                question: 'Chùm câu 9: Đọc đoạn tư liệu Tuyên bố thành lập Cộng đồng ASEAN (2015):',
                passage: 'Ngày 22/11/2015, tại Hội nghị Cấp cao ASEAN lần thứ 27 tại Cua-la Lăm-pơ, các nhà lãnh đạo đã ký Tuyên bố lịch sử thành lập Cộng đồng ASEAN, chính thức có hiệu lực từ ngày 31/12/2015. Đây là cột mốc lịch sử đánh dấu sự trưởng thành vượt bậc của ASEAN.\n(Tuyên bố Cua-la Lăm-pơ, 2015)',
                statements: [
                    'a) Cộng đồng ASEAN chính thức tuyên bố thành lập vào cuối năm 2015.',
                    'b) Tuyên bố thành lập Cộng đồng được ký kết tại Ma-lai-xi-a.',
                    'c) Cộng đồng ASEAN ra đời đánh dấu sự kết thúc hoàn toàn của tổ chức ASEAN.',
                    'd) Sự kiện chuyển ASEAN sang giai đoạn liên kết sâu rộng hơn.'
                ],
                correct: [true, true, false, true],
                explanation: 'a, b) Đúng (Ký tại Kuala Lumpur). c) Sai (Đánh dấu sự trưởng thành nâng cấp liên kết). d) Đúng.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Tư liệu Cộng đồng AEC',
                question: 'Chùm câu 10: Đọc đoạn tư liệu về Cộng đồng Kinh tế ASEAN (AEC):',
                passage: 'AEC hướng tới tạo ra một thị trường và cơ sở sản xuất thống nhất, một khu vực kinh tế có sức cạnh tranh cao, phát triển kinh tế đồng đều và hội nhập hoàn toàn vào nền kinh tế toàn cầu. AEC thúc đẩy tự do lưu chuyển hàng hóa, dịch vụ, đầu tư, vốn và lao động tay nghề.\n(12 chủ đề lịch sử chuyên sâu, NXB Thanh Niên, 2024)',
                statements: [
                    'a) AEC là trụ cột liên kết kinh tế trọng tâm của Cộng đồng ASEAN.',
                    'b) AEC hướng tới tự do di chuyển của lao động phổ thông không qua đào tạo.',
                    'c) Tạo ra một thị trường chung và cơ sở sản xuất thống nhất là mục tiêu của AEC.',
                    'd) AEC quy định bắt buộc các nước phải sử dụng chung một đồng tiền.'
                ],
                correct: [true, false, true, false],
                explanation: 'a) Đúng. b) Sai (Chỉ tự do di chuyển lao động tay nghề). c) Đúng. d) Sai (ASEAN không dùng đồng tiền chung).'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Tư liệu Tuyên bố ZOPFAN',
                question: 'Chùm câu 11: Đọc đoạn tư liệu Tuyên bố về khu vực hòa bình, tự do và trung lập (ZOPFAN 1971):',
                passage: 'Quyết tâm sử dụng những nỗ lực cần thiết bước đầu để bảo đảm việc công nhận và tôn trọng Đông Nam Á là một khu vực hòa bình, tự do và trung lập, không có sự can thiệp dưới bất kỳ hình thức và phương cách nào của các nước ngoài khu vực. Các nước Đông Nam Á cần phối hợp nỗ lực nhằm mở rộng các lĩnh vực hợp tác để góp phần tăng cường sức mạnh, tình đoàn kết, mối quan hệ gắn bó hơn nữa.\n(ASEAN, Tuyên bố về khu vực hòa bình, tự do và trung lập, ngày 27/11/1971)',
                statements: [
                    'a) Nội dung tư liệu đề cập sự kiện các nước Đông Nam Á thành lập khu vực hòa bình, tự do, trung lập.',
                    'b) Nội dung tuyên bố nhấn mạnh ASEAN không chấp nhận sự can thiệp của các nước ngoài khu vực.',
                    'c) ZOPFAN khẳng định vai trò không duy trì hòa bình, thống nhất và trung lập của Đông Nam Á.',
                    'd) Tuyên bố về khu vực hòa bình, tự do và trung lập vẫn có giá trị đối với tổ chức ASEAN ngày nay.'
                ],
                correct: [true, true, false, true],
                explanation: 'a, b) Đúng. c) Sai (Khẳng định quyết tâm duy trì hòa bình, trung lập). d) Đúng.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Tư liệu Cạnh tranh Nước lớn',
                question: 'Chùm câu 12: Đọc đoạn tư liệu Cạnh tranh nước lớn ở Đông Nam Á (Trần Xuân Hiệp):',
                passage: 'Bước sang thế kỷ XXI, cuộc cạnh tranh quyết liệt giữa các cường quốc trên thế giới diễn ra nhằm định vị lại trật tự thế giới mới. Riêng đối với khu vực Đông Nam Á, nơi Cộng đồng ASEAN đang phát triển mạnh mẽ, thì việc tranh giành ảnh hưởng giữa các nước lớn tại đây trở nên nóng bỏng hơn bao giờ hết. Trong bối cảnh nhiều thay đổi phức tạp đó, các cường quốc đã tìm cách lôi kéo ASEAN vào quỹ đạo chi phối của mình, tạo ra thế kiểm soát lẫn nhau trong tình hình ngày càng phức tạp trong mối quan hệ quốc tế.\n(Trần Xuân Hiệp, Cộng đồng ASEAN từ ý tưởng đến hiện thực, NXB Thế giới, Hà Nội, 2021, tr.52)',
                statements: [
                    'a) Sự cạnh tranh ảnh hưởng giữa các nước lớn ở khu vực Đông Nam Á đặt ra nhiều thách thức cho Cộng đồng ASEAN.',
                    'b) Đầu thế kỷ XXI, sự phát triển mạnh mẽ của ASEAN góp phần thúc đẩy xu thế đa cực.',
                    'c) Đoạn tư liệu đề cập đến bối cảnh ra đời và quá trình hoạt động của Hiệp hội các quốc gia Đông Nam Á.',
                    'd) Tăng cường hợp tác nội khối sâu sắc và chặt chẽ hơn là cơ sở để ASEAN tránh nguy cơ bị lôi kéo.'
                ],
                correct: [true, true, false, true],
                explanation: 'a, b) Đúng. c) Sai (Nội dung nói về cạnh tranh ảnh hưởng nước lớn đầu thế kỉ XXI). d) Đúng.'
            },
            {
                topic: 'cd2',
                category: 'Chủ đề 2: Tư liệu Tiến trình ASEAN',
                question: 'Chùm câu 13: Đọc bảng thông tin các mốc lịch sử xây dựng Cộng đồng ASEAN (1997, 2003, 2007, 2015):',
                passage: 'Bảng thông tin các mốc lịch sử xây dựng Cộng đồng ASEAN:\n• 1997: Tầm nhìn ASEAN 2020 nêu rõ việc xây dựng Cộng đồng ASEAN, định hướng cho sự phát triển trong tương lai.\n• 2003: Tuyên bố Bali đẩy mạnh chuẩn bị cho Cộng đồng ASEAN.\n• 2007: Hiến chương ASEAN tạo cơ sở pháp lý (nguyên tắc, thể chế và định hướng), thúc đẩy các hoạt động liên kết khu vực.\n• 2015: Tuyên bố Cua-la Lăm-pơ chính thức thành lập Cộng đồng ASEAN, có hiệu lực từ ngày 31/12/2015.',
                statements: [
                    'a) Cộng đồng ASEAN ra đời là bước ngoặt, đồng thời cũng là đích đến cuối cùng của tổ chức này.',
                    'b) Cộng đồng ASEAN được hình thành vào năm 2007, ngay sau khi Hiến chương ASEAN được thông qua.',
                    'c) Bảng thông tin trên thể hiện các mốc chính trong tiến trình xây dựng Cộng đồng ASEAN.',
                    'd) Cộng đồng ASEAN tạo nền tảng vững chắc để Đông Nam Á vươn lên thành trung tâm hợp tác năng động.'
                ],
                correct: [false, false, true, true],
                explanation: 'a) Sai (Không phải đích đến cuối cùng, ASEAN tiếp tục phát triển). b) Sai (Thành lập ngày 31/12/2015). c, d) Đúng.'
            },

            // CHỦ ĐỀ 3 (10 CHÙM)
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Hội nghị TW 8',
                question: 'Chùm câu 14: Đọc đoạn tư liệu Nghị quyết Hội nghị Trung ương 8 (tháng 5/1941):',
                passage: 'Trong lúc này nếu không giải quyết được vấn đề dân tộc giải phóng, không đòi được độc lập, tự do cho toàn thể dân tộc, thì chẳng những toàn thể quốc gia dân tộc còn chịu mãi kiếp ngựa trâu, mà quyền lợi của bộ phận, giai cấp đến nghìn năm cũng không đòi lại được.\n(Văn kiện Đảng Toàn tập, Tập 7, NXB Chính trị Quốc gia)',
                statements: [
                    'a) Trích đoạn khẳng định nhiệm vụ giải phóng dân tộc là mục tiêu bức thiết hàng đầu.',
                    'b) Hội nghị chủ trương đặt quyền lợi giai cấp lên trên quyền lợi sinh tồn của dân tộc.',
                    'c) Tinh thần này thể hiện sự chuyển hướng chiến lược sáng tạo của Đảng.',
                    'd) Quyền lợi giai cấp chỉ giải quyết được khi dân tộc đã giành được độc lập.'
                ],
                correct: [true, false, true, true],
                explanation: 'a) Đúng. b) Sai (Hội nghị đặt quyền lợi giải phóng dân tộc lên hàng đầu). c, d) Đúng.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Chỉ thị Kháng Nhật',
                question: 'Chùm câu 15: Đọc đoạn tư liệu Chỉ thị Nhật - Pháp bắn nhau và hành động của chúng ta (3/1945):',
                passage: 'Cuộc đảo chính của Nhật dẫn đến sự khủng hoảng chính trị sâu sắc. Điều kiện khởi nghĩa ở Đông Dương chín mồi nhanh chóng. Ban Thường vụ Trung ương Đảng quyết định thay khẩu hiệu "Đánh đuổi Pháp - Nhật" bằng khẩu hiệu "Đánh đuổi phát xít Nhật", phát động cao trào Kháng Nhật cứu nước.\n(Văn kiện Đảng Toàn tập, Tập 8, NXB Chính trị Quốc gia)',
                statements: [
                    'a) Chỉ thị ra đời ngay sau khi Nhật tiến hành đảo chính Pháp (9/3/1945).',
                    'b) Đảng xác định kẻ thù chính duy nhất của nhân dân Đông Dương lúc này là phát xít Nhật.',
                    'c) Cao trào Kháng Nhật cứu nước được phát động làm bước tập dượt trực tiếp cho Tổng khởi nghĩa.',
                    'd) Chỉ thị phát động Tổng khởi nghĩa giành chính quyền trên toàn quốc ngay trong tháng 3/1945.'
                ],
                correct: [true, true, true, false],
                explanation: 'a, b, c) Đúng. d) Sai (Mới phát động Cao trào kháng Nhật làm tiền đề, chưa Tổng khởi nghĩa).'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Quân lệnh số 1',
                question: 'Chùm câu 16: Đọc đoạn tư liệu Quân lệnh số 1 của Ủy ban Khởi nghĩa Toàn quốc (đêm 13/8/1945):',
                passage: 'Giờ Tổng khởi nghĩa đã đến! Cơ hội cho quân dân Việt Nam vùng dậy giành lấy quyền độc lập có một không hai... Chúng ta phải hành động cho nhanh, với một tinh thần vô cùng quả cảm, không được chần chừ!\n(Tài liệu Lịch sử Cách mạng tháng Tám, NXB Sự Thật, 1985)',
                statements: [
                    'a) Quân lệnh số 1 chính thức phát động Tổng khởi nghĩa trên phạm vi toàn quốc.',
                    'b) Tuyên bố khẳng định thời cơ thuận lợi ngàn năm có một đã xuất hiện.',
                    'c) Quân lệnh yêu cầu quân dân phải hành động thần tốc, không được chần chừ.',
                    'd) Văn kiện được ban hành sau khi Chủ tịch Hồ Chí Minh đọc Tuyên ngôn Độc lập.'
                ],
                correct: [true, true, true, false],
                explanation: 'a, b, c) Đúng. d) Sai (Quân lệnh số 1 ra đêm 13/8/1945, trước khi đọc Tuyên ngôn Độc lập 2/9/1945).'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Tuyên ngôn Độc lập',
                question: 'Chùm câu 17: Đọc đoạn tư liệu trích Tuyên ngôn Độc lập của Chủ tịch Hồ Chí Minh (2/9/1945):',
                passage: 'Tất cả mọi người sinh ra đều có quyền bình đẳng. Tạo hóa cho họ những quyền không ai có thể xâm phạm được; trong những quyền ấy, có quyền được sống, quyền tự do và quyền mưu cầu hạnh phúc... Nước Việt Nam có quyền hưởng tự do và độc lập, và sự thật đã thành một nước tự do độc lập.\n(Hồ Chí Minh Toàn tập, Tập 4, NXB Chính trị Quốc gia)',
                statements: [
                    'a) Bản Tuyên ngôn Độc lập trích dẫn Tuyên ngôn Độc lập của Mỹ và Tuyên ngôn Nhân quyền của Pháp.',
                    'b) Tuyên ngôn Độc lập phát triển từ quyền con người nâng lên thành quyền tự do, độc lập của dân tộc.',
                    'c) Tuyên ngôn Độc lập chính thức khai sinh ra nước Việt Nam Dân chủ Cộng hòa.',
                    'd) Văn kiện thừa nhận sự cai trị hợp pháp của thực dân Pháp tại Việt Nam.'
                ],
                correct: [true, true, true, false],
                explanation: 'a, b, c) Đúng. d) Sai (Văn kiện tuyên bố xóa bỏ mọi hợp đồng và đặc quyền của Pháp tại Việt Nam).'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Bảo vệ Độc lập',
                question: 'Chùm câu 18: Đọc đoạn tư liệu khẳng định quyết tâm bảo vệ độc lập trong Tuyên ngôn Độc lập (2/9/1945):',
                passage: 'Nước Việt Nam có quyền hưởng tự do và độc lập, và sự thật đã thành một nước tự do độc lập. Toàn thể dân tộc Việt Nam quyết đem tất cả tinh thần và lực lượng, tính mạng và của cải để giữ vững quyền tự do, độc lập ấy.\n(Chủ tịch Hồ Chí Minh, Tuyên ngôn Độc lập nước Việt Nam Dân chủ Cộng hòa, ngày 02/09/1945)',
                statements: [
                    'a) Trích đoạn khẳng định hai giá trị pháp lý và thực tiễn thiêng liêng: quyền tự do, độc lập và quyết tâm bảo vệ.',
                    'b) Bản Tuyên ngôn Độc lập là văn kiện lịch sử đánh dấu sự ra đời của nước Việt Nam Dân chủ Cộng hòa.',
                    'c) Bản Tuyên ngôn Độc lập được soạn thảo nhằm tuyên bố sự chấp nhận bảo hộ của quân Đồng minh.',
                    'd) Quyết tâm "đem tất cả tinh thần và lực lượng..." trở thành kim chỉ nam cho hai cuộc kháng chiến.'
                ],
                correct: [true, true, false, true],
                explanation: 'a, b) Đúng. c) Sai (Tuyên bố nền độc lập tự do hoàn toàn). d) Đúng.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Lời kêu gọi Toàn quốc',
                question: 'Chùm câu 19: Đọc đoạn tư liệu Lời kêu gọi Toàn quốc kháng chiến của Chủ tịch Hồ Chí Minh (19/12/1946):',
                passage: 'Chúng ta muốn hòa bình, chúng ta phải nhân nhượng. Nhưng chúng ta càng nhân nhượng, thực dân Pháp càng tới lấn, vì chúng quyết tâm cướp nước ta một lần nữa! Không! Chúng ta thà hy sinh tất cả, chứ nhất định không chịu mất nước, nhất định không chịu làm nô lệ.\n(Hồ Chí Minh Toàn tập, Tập 4, NXB Chính trị Quốc gia)',
                statements: [
                    'a) Lời kêu gọi khẳng định thiện chí hòa bình và giới hạn của sự nhân nhượng.',
                    'b) Văn kiện tố cáo âm mưu xâm lược quay trở lại của thực dân Pháp.',
                    'c) Lời kêu gọi thể hiện ý chí sắt đá thà hy sinh tất cả để giữ vững độc lập.',
                    'd) Lời kêu gọi được phát đi sau khi Hiệp định Giơ-ne-vơ đã được ký kết.'
                ],
                correct: [true, true, true, false],
                explanation: 'a, b, c) Đúng. d) Sai (Lời kêu gọi phát đi đêm 19/12/1946 mở đầu cuộc kháng chiến toàn quốc).'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Kháng chiến kiến quốc',
                question: 'Chùm câu 20: Đọc đoạn tư liệu Chỉ thị Kháng chiến kiến quốc (25/11/1945):',
                passage: 'Cuộc cách mạng của ta lúc này vẫn là cuộc cách mạng giải phóng dân tộc. Kẻ thù chính của ta lúc này là thực dân Pháp xâm lược, phải tập trung chĩa mũi nhọn đấu tranh vào chúng. Mở rộng Mặt trận Việt Minh và củng cố chính quyền nhân dân.\n(Văn kiện Đảng Toàn tập, Tập 8, NXB Chính trị Quốc gia)',
                statements: [
                    'a) Chỉ thị xác định kẻ thù hiểm yếu số một của cách mạng Việt Nam là thực dân Pháp.',
                    'b) Kháng chiến kiến quốc đề ra hai nhiệm vụ chiến lược song song vừa kháng chiến vừa xây dựng đất nước.',
                    'c) Văn kiện chủ trương liên minh quân sự với thực dân Pháp để chống quân Tưởng.',
                    'd) Củng cố chính quyền cách mạng được xác định là nhiệm vụ cấp bách.'
                ],
                correct: [true, true, false, true],
                explanation: 'a, b) Đúng. c) Sai (Xác định chĩa mũi nhọn vào thực dân Pháp xâm lược). d) Đúng.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Đại hội II',
                question: 'Chùm câu 21: Đọc đoạn tư liệu Báo cáo Chính trị tại Đại hội đại biểu toàn quốc lần thứ II (2/1951):',
                passage: 'Đại hội quyết định đưa Đảng ra hoạt động công khai với tên gọi Đảng Lao động Việt Nam. Xây dựng Đảng thành một Đảng tiên phong của giai cấp công nhân và nhân dân lao động, lãnh đạo cuộc kháng chiến chống Pháp đến thắng lợi hoàn toàn.\n(Văn kiện Đảng Toàn tập, Tập 12, NXB Chính trị Quốc gia)',
                statements: [
                    'a) Đại hội II đánh dấu mốc Đảng ra hoạt động công khai với tên Đảng Lao động Việt Nam.',
                    'b) Đại hội quyết định giải thể hoàn toàn hệ thống chính quyền cách mạng.',
                    'c) Đại hội II được đánh giá là "Đại hội Kháng chiến thắng lợi".',
                    'd) Nhiệm vụ hàng đầu của Đảng Lao động Việt Nam là lãnh đạo kháng chiến chống Pháp.'
                ],
                correct: [true, false, true, true],
                explanation: 'a) Đúng. b) Sai (Tiếp tục củng cố chính quyền và lãnh đạo kháng chiến đến thắng lợi). c, d) Đúng.'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Ý nghĩa CM T8',
                question: 'Chùm câu 22: Đọc đoạn tư liệu về Ý nghĩa lịch sử Cách mạng tháng Tám (Trường Chinh):',
                passage: 'Không những giật tung được xiềng xích của bọn đế quốc phát xít, Cách mạng tháng Tám lại lật nhào được chế độ quân chủ thành lập trên đất nước ta hàng chục thế kỷ, làm cho nước Việt Nam thành một nước cộng hòa dân chủ...\nCách mạng tháng Tám tỏ rõ tinh thần chống phát xít và yêu chuộng dân chủ và hòa bình của nhân dân Việt Nam... Cách mạng tháng Tám đã chọc thủng được hệ thống thuộc địa của chủ nghĩa đế quốc ở một trong những mắt xích yếu nhất của nó, mở đầu cho quá trình tan rã không thể cứu vãn được của chủ nghĩa thực dân thế giới.\n(Trường Chinh, Cách mạng dân tộc dân chủ nhân dân Việt Nam - Tác phẩm chọn lọc, Tập I, NXB Sự thật, Hà Nội, 1975, tr.388 - 391)',
                statements: [
                    'a) Cách mạng tháng Tám đã đập tan hai tầng áp bức là đế quốc phát xít và phong kiến.',
                    'b) Sự kiện Vua Bảo Đại tuyên bố thoái vị đánh dấu chế độ phong kiến sụp đổ hoàn toàn.',
                    'c) Cách mạng tháng Tám đưa nhân dân Việt Nam từ thân phận nô lệ trở thành người chủ đất nước.',
                    'd) Cách mạng tháng Tám chỉ giải quyết nhiệm vụ chống phong kiến chia ruộng đất.'
                ],
                correct: [true, true, true, false],
                explanation: 'a, b, c) Đúng. d) Sai (Cách mạng tháng Tám hoàn thành xuất sắc nhiệm vụ giải phóng dân tộc và lật đổ phong kiến).'
            },
            {
                topic: 'cd3',
                category: 'Chủ đề 3: Tư liệu Thời cơ CM T8',
                question: 'Chùm câu 23: Đọc đoạn tư liệu Thời cơ và điều kiện Tổng khởi nghĩa tháng Tám (SGK Lịch sử 12):',
                passage: 'Đến ngày 15/8/1945, Nhật Bản tuyên bố đầu hàng Đồng minh không điều kiện. Ngay sau khi Nhật Bản tuyên bố đầu hàng Đồng minh, quân Nhật ở Đông Dương rệu rã, Chính phủ thân Nhật Trần Trọng Kim hoang mang. Điều kiện khách quan thuận lợi cho cuộc Tổng khởi nghĩa đã đến.\nTrước đó, từ tháng 3 đến tháng 8/1945, cao trào kháng Nhật, cứu nước đã diễn ra trong cả nước, góp phần chuẩn bị lực lượng, tập dượt cho quần chúng đấu tranh, sẵn sàng tổng khởi nghĩa giành chính quyền khi thời cơ đến.\n(Sách giáo khoa Lịch sử 12, bộ Kết nối tri thức với cuộc sống, trang 32)',
                statements: [
                    'a) Tư liệu đề cập đến điều kiện thuận lợi mọi mặt cho Tổng khởi nghĩa tháng Tám.',
                    'b) Điều kiện chủ quan giữ vai trò quyết định thắng lợi của Cách mạng tháng Tám.',
                    'c) Trong cao trào kháng Nhật, thời cơ cho tổng khởi nghĩa xuất hiện và chín mùi.',
                    'd) Khi Nhật Bản tuyên bố đầu hàng Đồng minh, tình thế cách mạng đã xuất hiện.'
                ],
                correct: [true, true, true, true],
                explanation: 'a, b, c, d) Cả 4 mệnh đề đều ĐÚNG theo phân tích bối cảnh và nguyên nhân thắng lợi của Cách mạng tháng Tám.'
            }
        ];

        /* FLASHCARD THEORY DATASET */
        const historyFlashcards = [
            {
                q: 'Liên hợp quốc chính thức thành lập ngày nào?',
                a: 'Ngày 24/10/1945 (ngày Hiến chương Liên hợp quốc chính thức có hiệu lực).'
            },
            {
                q: '5 nước Ủy viên thường trực Hội đồng Bảo an LHQ là ai?',
                a: 'Mỹ, Nga, Trung Quốc, Anh, Pháp (có quyền phủ quyết - Veto).'
            },
            {
                q: 'Khởi đầu Chiến tranh lạnh là sự kiện nào?',
                a: 'Thông điệp của Tổng thống Mỹ Truman tại Quốc hội Mỹ ngày 12/3/1947.'
            },
            {
                q: 'Sự kiện đánh dấu Trật tự 2 cực I-an-ta sụp đổ?',
                a: 'Tháng 12/1991, Liên bang Xô viết (Liên Xô) sụp đổ và tan rã.'
            },
            {
                q: 'Xu thế trật tự thế giới sau Chiến tranh lạnh?',
                a: 'Trật tự thế giới mới đang hình thành theo hướng ĐA CỰC.'
            },
            {
                q: 'Tổ chức ASEAN thành lập ngày nào? Ở đâu?',
                a: 'Thành lập ngày 08/08/1967 tại Băng Cốc (Thái Lan) bởi 5 nước sáng lập (Indo, Malay, Phil, Sing, Thái).'
            },
            {
                q: 'Bước ngoặt củng cố liên kết khu vực của ASEAN?',
                a: 'Hội nghị Cấp cao ASEAN lần I tại Bali (1976) và ký Hiệp ước Thân thiện và Hợp tác (TAC).'
            },
            {
                q: 'Cộng đồng ASEAN thành lập ngày nào? Gồm mấy trụ cột?',
                a: 'Chính thức thành lập ngày 31/12/2015. Gồm 3 trụ cột: Chính trị-An ninh (APSC), Kinh tế (AEC), Văn hóa-Xã hội (ASCC).'
            },
            {
                q: '4 tỉnh giành chính quyền sớm nhất trong CM Tháng Tám 1945?',
                a: 'Bắc Giang, Hải Dương, Hà Tĩnh, Quảng Nam (giành chính quyền ngày 18/8/1945).'
            },
            {
                q: 'Hai tỉnh giành chính quyền muộn nhất trong CM Tháng Tám?',
                a: 'Đồng Nai Nhiễm và Hà Tiên (giành chính quyền ngày 28/8/1945).'
            },
            {
                q: 'Sự kiện chấm dứt hoàn toàn chế độ phong kiến Việt Nam?',
                a: 'Vua Bảo Đại tuyên bố thoái vị ngày 30/8/1945 tại Huế.'
            },
            {
                q: 'Khai sinh ra nước Việt Nam Dân chủ Cộng hòa?',
                a: 'Ngày 2/9/1945, Bác Hồ đọc Tuyên ngôn Độc lập tại Quảng trường Ba Đình.'
            },
            {
                q: 'Đường lối kháng chiến chống Pháp (1945 - 1954)?',
                a: 'Toàn dân, toàn diện, trường kỳ, tự lực cánh sinh và tranh thủ sự ủng hộ quốc tế.'
            },
            {
                q: 'Chiến dịch giúp ta giành quyền chủ động trên chiến trường chính Bắc Bộ?',
                a: 'Chiến dịch Biên giới thu - đông năm 1950.'
            },
            {
                q: 'Đại hội đại biểu toàn quốc lần thứ II của Đảng (2/1951)?',
                a: 'Đảng ra hoạt động công khai với tên gọi Đảng Lao động Việt Nam; được đánh giá là "Đại hội Kháng chiến thắng lợi".'
            }
        ];

        /* TOPIC FILTER LOGIC */
        function setTopicFilter(topic) {
            playAudio('click');
            selectedTopicFilter = topic;
            
            document.querySelectorAll('.topic-btn').forEach(btn => {
                btn.classList.remove('bg-amber-500', 'text-slate-950', 'active', 'border-amber-400');
                btn.classList.add('bg-slate-800', 'text-amber-200');
            });
            
            const activeBtn = document.getElementById(`topic-btn-${topic}`);
            if (activeBtn) {
                activeBtn.classList.remove('bg-slate-800', 'text-amber-200');
                activeBtn.classList.add('bg-amber-500', 'text-slate-950', 'active', 'border-amber-400');
            }

            // Update badge text
            let filteredMCQ = historyMCQ;
            let filteredTF = historyTF;
            if (topic !== 'all') {
                filteredMCQ = historyMCQ.filter(q => q.topic === topic);
                filteredTF = historyTF.filter(q => q.topic === topic);
            }

            document.getElementById('mcq-count-label').innerText = `${filteredMCQ.length} Câu hỏi chọn lọc`;
            document.getElementById('tf-count-label').innerText = `${filteredTF.length} Chùm câu (${filteredTF.length * 4} mệnh đề)`;
        }

        /* SHUFFLE & RENUMBERING UTILS */
        function shuffleArray(array) {
            const arr = [...array];
            for (let i = arr.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [arr[i], arr[j]] = [arr[j], arr[i]];
            }
            return arr;
        }

        function getCleanQuestionText(q, index) {
            if (!q || !q.question) return '';
            const rawText = q.question.replace(/^(Câu|Chùm câu)\s*\d+[\s:\-.]*/i, '').trim();
            const prefix = (q.statements) ? `Chùm câu ${index + 1}: ` : `Câu ${index + 1}: `;
            return prefix + rawText;
        }

        /* FLASHCARD LOGIC */
        function initFlashcards() {
            flashcards = [...historyFlashcards];
            currentFcIndex = 0;
            isFcFlipped = false;
            renderFlashcard();
        }

        function renderFlashcard() {
            const fc = flashcards[currentFcIndex];
            if (!fc) return;
            const inner = document.getElementById('flashcard-inner');
            inner.classList.remove('rotate-y-180');
            isFcFlipped = false;

            setTimeout(() => {
                document.getElementById('flashcard-question').innerText = fc.q;
                document.getElementById('flashcard-answer').innerText = fc.a;
                document.getElementById('flashcard-counter').innerText = `Thẻ ${currentFcIndex + 1} / ${flashcards.length}`;
            }, 150);
        }

        function flipFlashcard() {
            playAudio('click');
            const inner = document.getElementById('flashcard-inner');
            isFcFlipped = !isFcFlipped;
            if (isFcFlipped) {
                inner.classList.add('rotate-y-180');
            } else {
                inner.classList.remove('rotate-y-180');
            }
        }

        function nextFlashcard() {
            playAudio('click');
            currentFcIndex = (currentFcIndex + 1) % flashcards.length;
            renderFlashcard();
        }

        function prevFlashcard() {
            playAudio('click');
            currentFcIndex = (currentFcIndex - 1 + flashcards.length) % flashcards.length;
            renderFlashcard();
        }

        function shuffleFlashcards() {
            playAudio('click');
            flashcards.sort(() => Math.random() - 0.5);
            currentFcIndex = 0;
            renderFlashcard();
        }

        /* GAME MODES START */
        function startPracticeMode(mode) {
            playAudio('click');
            let pool = (mode === 'mcq') ? historyMCQ : historyTF;
            if (selectedTopicFilter !== 'all') {
                pool = pool.filter(q => q.topic === selectedTopicFilter);
            }
            currentQuestions = shuffleArray(pool);
            initQuizGame();
        }

        function startSpeedRun() {
            playAudio('click');
            let poolMCQ = historyMCQ;
            let poolTF = historyTF;
            if (selectedTopicFilter !== 'all') {
                poolMCQ = historyMCQ.filter(q => q.topic === selectedTopicFilter);
                poolTF = historyTF.filter(q => q.topic === selectedTopicFilter);
            }
            const mixed = [...poolMCQ, ...poolTF];
            currentQuestions = shuffleArray(mixed).slice(0, 25);
            initQuizGame();
        }

        function initQuizGame() {
            currentScore = 0;
            currentStreak = 0;
            maxStreak = 0;
            currentIndex = 0;
            userAnswers = [];
            updateHeaderStats();
            showView('quiz');
            loadQuestion();
        }

        function updateHeaderStats() {
            document.getElementById('user-xp').innerText = `${userXP} XP`;
            document.getElementById('streak-count').innerText = currentStreak;
        }

        function startTimer() {
            if (timerInterval) clearInterval(timerInterval);
            timeLeft = 30;
            const timerBar = document.getElementById('timer-bar');
            const timerText = document.getElementById('timer-text');
            
            timerBar.style.width = '100%';
            timerText.innerText = `${timeLeft}s`;

            timerInterval = setInterval(() => {
                timeLeft -= 0.1;
                if (timeLeft <= 0) {
                    timeLeft = 0;
                    clearInterval(timerInterval);
                    timerText.innerText = '0s';
                    timerBar.style.width = '0%';
                    handleTimeout();
                } else {
                    const pct = (timeLeft / 30) * 100;
                    timerBar.style.width = `${pct}%`;
                    timerText.innerText = `${Math.ceil(timeLeft)}s`;
                }
            }, 100);
        }

        function handleTimeout() {
            playAudio('wrong');
            currentStreak = 0;
            updateHeaderStats();
            const q = currentQuestions[currentIndex];
            
            userAnswers.push({
                question: getCleanQuestionText(q, currentIndex),
                userAns: 'Hết thời gian',
                correctAns: getCorrectAnsText(q),
                isCorrect: false,
                explanation: q.explanation,
                pts: 0
            });

            showExplanation(false, '⏰ Đã Hết Thời Gian!', q.explanation);
        }

        function getCorrectAnsText(q) {
            if (q.options) return q.options[q.correct];
            if (q.statements) return q.correct.map((val, idx) => `${['a','b','c','d'][idx]}: ${val ? 'Đúng' : 'Sai'}`).join(' | ');
            return '';
        }

        function loadQuestion() {
            if (timerInterval) clearInterval(timerInterval);
            
            const q = currentQuestions[currentIndex];
            if (!q) {
                finishQuiz();
                return;
            }

            const pct = ((currentIndex) / currentQuestions.length) * 100;
            document.getElementById('quiz-progress-bar').style.width = `${pct}%`;
            document.getElementById('quiz-progress-text').innerText = `Câu ${currentIndex + 1} / ${currentQuestions.length}`;
            document.getElementById('q-category-tag').innerText = q.category || 'Lịch Sử 12';
            
            const multiplier = 1 + Math.min(Math.floor(currentStreak / 3) * 0.5, 2.0);
            document.getElementById('quiz-combo-badge').innerText = `Multiplier x${multiplier.toFixed(1)}`;
            document.getElementById('q-points-value').innerText = `+${Math.round(1000 * multiplier)} Pts`;

            document.getElementById('question-text').innerText = getCleanQuestionText(q, currentIndex);
            document.getElementById('explanation-box').classList.add('hidden');

            const answersContainer = document.getElementById('answers-container');

            if (q.options) {
                // MCQ Single Choice
                answersContainer.className = "grid grid-cols-1 md:grid-cols-2 gap-3 sm:gap-4 pt-1 sm:pt-2";
                const colorClasses = ['q-option-red', 'q-option-blue', 'q-option-yellow', 'q-option-green'];
                answersContainer.innerHTML = q.options.map((opt, idx) => `
                    <button onclick="selectMCQOption(${idx})" class="btn-quizizz p-3.5 sm:p-4 rounded-2xl ${colorClasses[idx % 4]} text-left font-game font-bold text-sm sm:text-base text-white hover:brightness-110 shadow-lg flex items-center space-x-3 transition transform active:scale-95">
                        <span class="w-7 h-7 sm:w-8 sm:h-8 rounded-xl bg-black/20 flex items-center justify-center text-xs sm:text-sm font-extrabold flex-shrink-0">${['A','B','C','D'][idx]}</span>
                        <span class="leading-snug break-words">${opt}</span>
                    </button>
                `).join('');
            } else if (q.statements) {
                // True / False Cluster
                answersContainer.className = "flex flex-col space-y-3 w-full col-span-1 md:col-span-2";
                answersContainer.innerHTML = `
                    ${q.passage ? `
                        <div class="p-3.5 sm:p-4 rounded-2xl bg-amber-950/60 border border-amber-500/50 text-amber-100 text-xs sm:text-sm leading-relaxed shadow-inner mb-1">
                            <div class="font-bold text-amber-300 flex items-center space-x-2 mb-1.5 text-xs sm:text-sm uppercase tracking-wider">
                                <i class="fa-solid fa-book-open text-amber-400"></i>
                                <span>TƯ LIỆU THAM KHẢO:</span>
                            </div>
                            <p class="whitespace-pre-line text-slate-200 font-sans leading-relaxed">${q.passage}</p>
                        </div>
                    ` : ''}
                    <div class="space-y-2.5 sm:space-y-3 bg-slate-900/90 p-3 sm:p-4 rounded-2xl border border-amber-600/50">
                        ${q.statements.map((stmt, idx) => `
                            <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2 p-2.5 sm:p-3 bg-slate-800/80 rounded-xl border border-slate-700">
                                <span class="text-xs sm:text-sm font-semibold text-slate-100 flex-grow leading-snug">${stmt}</span>
                                <div class="flex items-center space-x-2 flex-shrink-0 justify-end pt-1 sm:pt-0 border-t sm:border-t-0 border-slate-700/50 sm:border-transparent">
                                    <label class="flex items-center space-x-1.5 cursor-pointer px-3 py-2 rounded-xl bg-emerald-900/70 active:bg-emerald-800 border border-emerald-500/60 text-emerald-300 font-game text-xs font-bold transition">
                                        <input type="radio" name="tf_${idx}" value="true" class="w-4 h-4 accent-emerald-400">
                                        <span>ĐÚNG</span>
                                    </label>
                                    <label class="flex items-center space-x-1.5 cursor-pointer px-3 py-2 rounded-xl bg-rose-900/70 active:bg-rose-800 border border-rose-500/60 text-rose-300 font-game text-xs font-bold transition">
                                        <input type="radio" name="tf_${idx}" value="false" class="w-4 h-4 accent-rose-400">
                                        <span>SAI</span>
                                    </label>
                                </div>
                            </div>
                        `).join('')}
                    </div>
                    <button onclick="evaluateTF()" class="btn-quizizz w-full py-3 bg-gradient-to-r from-amber-500 to-yellow-600 font-game font-bold text-white text-base sm:text-lg rounded-2xl shadow-lg border-b-4 border-amber-800 hover:brightness-110 active:scale-98">
                        GỬI ĐÁP ÁN ĐÚNG/SAI <i class="fa-solid fa-paper-plane ml-2"></i>
                    </button>
                `;
            }

            startTimer();
        }

        function selectMCQOption(selectedIndex) {
            if (timerInterval) clearInterval(timerInterval);
            const q = currentQuestions[currentIndex];
            const isCorrect = selectedIndex === q.correct;
            
            processResult(isCorrect, q.options[selectedIndex], getCorrectAnsText(q), q.explanation);
        }

        function evaluateTF() {
            if (timerInterval) clearInterval(timerInterval);
            const q = currentQuestions[currentIndex];
            let correctCount = 0;
            const userSelections = [];

            q.statements.forEach((_, idx) => {
                const radios = document.getElementsByName(`tf_${idx}`);
                let sel = null;
                radios.forEach(r => { if (r.checked) sel = (r.value === 'true'); });
                userSelections.push(sel);
                if (sel === q.correct[idx]) correctCount++;
            });

            const isFullyCorrect = correctCount === q.statements.length;
            const userText = userSelections.map((v, i) => `${['a','b','c','d'][i]}: ${v === true ? 'Đúng' : v === false ? 'Sai' : 'Chưa chọn'}`).join(' | ');

            processResult(isFullyCorrect, userText, getCorrectAnsText(q), q.explanation, correctCount / q.statements.length);
        }

        function processResult(isCorrect, userAnsText, correctAnsText, explanationText, partialRatio = 1) {
            const multiplier = 1 + Math.min(Math.floor(currentStreak / 3) * 0.5, 2.0);
            let ptsGained = 0;

            if (isCorrect) {
                currentStreak++;
                if (currentStreak > maxStreak) maxStreak = currentStreak;
                ptsGained = Math.round(1000 * multiplier * (timeLeft / 30 + 0.5) * partialRatio);
                userXP += ptsGained;
                currentScore += ptsGained;
                playAudio('correct');

                if (currentStreak > 0 && currentStreak % 3 === 0) {
                    triggerMemePopup(currentStreak);
                }
            } else {
                currentStreak = 0;
                playAudio('wrong');
            }

            updateHeaderStats();

            userAnswers.push({
                question: getCleanQuestionText(currentQuestions[currentIndex], currentIndex),
                userAns: userAnsText,
                correctAns: correctAnsText,
                isCorrect: isCorrect,
                explanation: explanationText,
                pts: ptsGained
            });

            showExplanation(isCorrect, isCorrect ? '🎉 CHÍNH XÁC!' : '❌ CHƯA CHÍNH XÁC!', explanationText);
        }

        function triggerMemePopup(streakNum) {
            playAudio('streak');
            const popup = document.getElementById('meme-popup');
            const card = document.getElementById('meme-card');
            const emojis = ['🔥', '⚡', '👑', '🚀', '🧠'];
            const titles = ['ĐỈNH KOBE!', 'XUẤT SẮC!', 'THẦN ĐỒNG SỬ!', 'SIÊU CẤP!', 'BÙNG NỔ!'];
            
            document.getElementById('meme-emoji').innerText = emojis[Math.floor(Math.random() * emojis.length)];
            document.getElementById('meme-title').innerText = titles[Math.floor(Math.random() * titles.length)];
            document.getElementById('meme-sub').innerText = `Chuỗi đúng x${streakNum} liên tiếp! Thưởng thêm XP!`;

            popup.classList.remove('opacity-0', 'pointer-events-none');
            card.classList.remove('scale-75');
            card.classList.add('scale-100');

            setTimeout(() => {
                popup.classList.add('opacity-0', 'pointer-events-none');
                card.classList.remove('scale-100');
                card.classList.add('scale-75');
            }, 1400);
        }

        function showExplanation(isCorrect, headerTitle, explanationText) {
            const box = document.getElementById('explanation-box');
            const header = document.getElementById('feedback-header');
            const textEl = document.getElementById('explanation-text');

            box.classList.remove('hidden');
            if (isCorrect) {
                header.className = "flex items-center space-x-2 font-game font-bold text-lg text-emerald-400";
                header.innerHTML = `<i class="fa-solid fa-circle-check text-2xl"></i> <span>${headerTitle}</span>`;
            } else {
                header.className = "flex items-center space-x-2 font-game font-bold text-lg text-rose-400";
                header.innerHTML = `<i class="fa-solid fa-circle-xmark text-2xl"></i> <span>${headerTitle}</span>`;
            }

            textEl.innerText = explanationText;
        }

        function nextQuestion() {
            playAudio('click');
            currentIndex++;
            if (currentIndex < currentQuestions.length) {
                loadQuestion();
            } else {
                finishQuiz();
            }
        }

        function finishQuiz() {
            if (timerInterval) clearInterval(timerInterval);
            
            const correctCount = userAnswers.filter(a => a.isCorrect).length;
            const accuracy = currentQuestions.length > 0 ? Math.round((correctCount / currentQuestions.length) * 100) : 0;

            document.getElementById('res-score').innerText = currentScore;
            document.getElementById('res-accuracy').innerText = `${accuracy}%`;
            document.getElementById('res-correct').innerText = `${correctCount}/${currentQuestions.length}`;
            document.getElementById('res-streak').innerText = `🔥 ${maxStreak}`;

            let title = "Học Sinh Chăm Chỉ";
            if (accuracy >= 90) title = "👑 Thủ Khoa Lịch Sử 12 (10 Điểm!)";
            else if (accuracy >= 75) title = "⚡ Nhà Sử Học Xuất Sắc";
            else if (accuracy >= 50) title = "🔥 Đạt Chuẩn Kiến Thức";
            document.getElementById('result-rank-title').innerText = `Danh hiệu: "${title}"`;

            const container = document.getElementById('review-list-container');
            container.innerHTML = userAnswers.map((item, idx) => `
                <div class="p-4 rounded-2xl border ${item.isCorrect ? 'bg-emerald-950/40 border-emerald-500/50' : 'bg-rose-950/40 border-rose-500/50'} space-y-2">
                    <div class="flex items-start justify-between">
                        <h4 class="font-bold text-sm text-white">${item.question}</h4>
                        <span class="text-xs font-bold px-2.5 py-0.5 rounded-full ${item.isCorrect ? 'bg-emerald-900 text-emerald-300' : 'bg-rose-900 text-rose-300'}">
                            ${item.isCorrect ? 'Đúng (+ ' + item.pts + ' XP)' : 'Sai'}
                        </span>
                    </div>
                    <div class="text-xs space-y-1">
                        <p class="text-amber-200"><span class="font-semibold text-amber-400">Bạn chọn:</span> ${item.userAns}</p>
                        <p class="text-emerald-300"><span class="font-semibold text-emerald-400">Đáp án đúng:</span> ${item.correctAns}</p>
                    </div>
                    <div class="p-2.5 rounded-xl bg-slate-900/80 border border-amber-700/50 text-xs text-slate-200 leading-relaxed">
                        💡 <span class="font-semibold text-amber-300">Giải thích:</span> ${item.explanation}
                    </div>
                </div>
            `).join('');

            showView('result');
        }

        function restartCurrentQuiz() {
            startPracticeMode('mcq');
        }

        window.onload = function() {
            updateHeaderStats();
            showView('home');
        };
    </script>
</body>
</html>
