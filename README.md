# yaruci0723-Coco.github.io
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>書法道技123圖像測驗 — 翰墨書院版</title>
<!-- Tailwind CSS -->
<script src="https://cdn.tailwindcss.com"></script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Serif+TC:wght@400;700;900&family=Noto+Sans+TC:wght@400;700;900&display=swap');

/* 自訂字級標準 */
.txt-general {
font-size: 20pt !important;
line-height: 1.4 !important;
}

.txt-title {
font-size: 22pt !important;
font-weight: 900 !important;
}

.txt-15 {
font-size: 15pt !important;
}

.title-font {
font-family: 'BiauKai', 'DFKai-SB', '標楷體', 'Noto Serif TC', serif;
}

body, button, input, select, textarea, div, p, span, th, td {
font-family: 'Noto Serif TC', 'Microsoft JhengHei', '微軟正黑體', serif;
}

/* 宣紙紋理與柔和陰影 */
.xuan-bg {
background-color: #fbf9f3;
background-image: radial-gradient(#efece0 1.2px, transparent 0), radial-gradient(#efece0 1.2px, transparent 0);
background-size: 16px 16px;
background-position: 0 0, 8px 8px;
}

.scroll-paper {
background: linear-gradient(135deg, #fdfcf7 0%, #faf6eb 100%);
box-shadow: inset 0 0 40px rgba(139, 115, 85, 0.12), 0 10px 25px -5px rgba(0, 0, 0, 0.08);
}

/* 古典雙線邊框 */
.classic-border {
border: 4px double #8c6b4f;
}

/* 硃砂紅光暈與竹金光暈 */
.glow-green {
box-shadow: 0 0 20px rgba(74, 222, 128, 0.4), inset 0 0 8px rgba(34, 197, 94, 0.2);
animation: pulse-glow 2.5s infinite alternate;
}
.glow-blue {
box-shadow: 0 0 20px rgba(140, 107, 79, 0.4), inset 0 0 8px rgba(140, 107, 79, 0.2);
animation: pulse-glow 2.5s infinite alternate;
}
.glow-hell {
box-shadow: 0 0 20px rgba(184, 28, 34, 0.4), inset 0 0 8px rgba(156, 27, 31, 0.2);
animation: pulse-glow 1.8s infinite alternate;
}

@keyframes pulse-glow {
0% { transform: scale(0.99); opacity: 0.95; }
100% { transform: scale(1.01); opacity: 1; }
}

/* 翰墨毛筆與印章攻擊動畫 */
@keyframes brush-stroke {
0% { transform: translate(0, 0) rotate(0deg); opacity: 1; }
40% { transform: translate(45px, -15px) rotate(-15deg); opacity: 1; filter: drop-shadow(0 4px 8px rgba(0,0,0,0.3)); }
100% { transform: translate(0, 0) rotate(0deg); opacity: 1; }
}
.brush-attacking {
animation: brush-stroke 0.6s cubic-bezier(0.25, 1, 0.5, 1);
}

@keyframes seal-shake {
0%, 100% { transform: translate(0, 0) scale(1); filter: none; }
20%, 60% { transform: translate(-8px, 4px) scale(0.95); filter: sepia(0.5) hue-rotate(-30deg); }
40%, 80% { transform: translate(8px, -4px) scale(1.05); filter: sepia(0.5) hue-rotate(-30deg); }
}
.seal-hit {
animation: seal-shake 0.6s ease-in-out;
}

@keyframes seal-stomp {
0% { transform: translate(0, 0) scale(1); }
30% { transform: translate(-30px, 15px) scale(1.15) rotate(-5deg); }
100% { transform: translate(0, 0) scale(1); }
}
.seal-attacking {
animation: seal-stomp 0.6s ease-in-out;
}

@keyframes brush-hit {
0%, 100% { transform: translate(0, 0); filter: none; }
25% { transform: translate(6px, -4px) rotate(8deg); filter: blur(0.5px) grayscale(0.5); }
75% { transform: translate(-6px, 4px) rotate(-8deg); filter: blur(0.5px) grayscale(0.5); }
}
.brush-hit {
animation: brush-hit 0.5s ease-in-out;
}

/* 捲軸展開動畫 */
@keyframes scroll-unroll {
from { max-height: 0px; opacity: 0; }
to { max-height: 1500px; opacity: 1; }
}
.scroll-unrolled {
animation: scroll-unroll 1s ease-out forwards;
}

/* 客製化捲軸滾動條 */
::-webkit-scrollbar {
width: 7px;
height: 7px;
}
::-webkit-scrollbar-track {
background: #f5efe2;
}
::-webkit-scrollbar-thumb {
background: #8c6b4f;
border-radius: 4px;
}
</style>
</head>
<body class="bg-[#fbf9f3] text-[#2c2c2c] min-h-screen relative overflow-x-hidden xuan-bg flex flex-col justify-between">

<!-- 頂部古典計分與進度條 -->
<header id="game-header" class="hidden w-full max-w-5xl mx-auto px-4 pt-4 z-10">
<div class="scroll-paper border-2 border-[#8c6b4f] rounded-lg p-3 shadow-md relative overflow-hidden">
<!-- 裝飾花紋角 -->
<div class="absolute top-0 left-0 w-3 h-3 border-t-2 border-l-2 border-[#8c6b4f]"></div>
<div class="absolute top-0 right-0 w-3 h-3 border-t-2 border-r-2 border-[#8c6b4f]"></div>
<div class="absolute bottom-0 left-0 w-3 h-3 border-b-2 border-l-2 border-[#8c6b4f]"></div>
<div class="absolute bottom-0 right-0 w-3 h-3 border-b-2 border-r-2 border-[#8c6b4f]"></div>

<div class="flex flex-col sm:flex-row justify-between items-center gap-2 mb-2 font-bold tracking-wide txt-general">
<div class="flex items-center space-x-2">
<span class="text-[#9c1b1f] font-black">尋道學子: <span id="header-username" class="underline decoration-dotted">-</span></span>
<span class="text-slate-300">|</span>
<span class="text-[#8c6b4f]" id="header-mode-title">一般模式</span>
</div>
<div class="flex items-center space-x-4">
<span class="text-[#b4833b] font-black">分數: <span id="header-score">0</span></span>
<span class="text-emerald-700">對: <span id="header-correct-count">0</span></span>
<span class="text-[#9c1b1f]">錯: <span id="header-wrong-count">0</span></span>
</div>
</div>
<!-- 進度條 -->
<div class="relative w-full bg-[#f4efe2] h-6 rounded-full overflow-hidden border border-[#d3cbb6] mt-2">
<div id="progress-bar-fill" class="bg-gradient-to-r from-[#d1a153] to-[#9c1b1f] h-full w-0 transition-all duration-300"></div>
<div class="absolute inset-0 flex items-center justify-center font-black text-[#1a1a1a] drop-shadow-sm txt-general">
進度: <span id="header-progress-text" class="ml-2">0 / 0</span>
</div>
</div>
</div>
</header>

<!-- 遊戲主要視窗容器 -->
<main class="flex-grow flex items-center justify-center w-full max-w-6xl mx-auto p-3 md:p-6 relative">

<!-- 1. 首頁與模式選擇 — 雙頁書卷改版 -->
<section id="screen-modes" class="w-full max-w-4xl z-10 flex flex-col items-center">

<div class="w-full text-center mb-6 relative flex flex-col items-center">
<div class="w-full max-w-2xl bg-gradient-to-b from-[#8c6b4f]/15 to-transparent rounded-t-xl py-3 border-t-2 border-x-2 border-[#8c6b4f]/40 relative overflow-hidden flex flex-col items-center justify-center px-4">
<div class="flex items-center space-x-3 z-10">
書法道技 123
</h1>
</div>
<p class="txt-general text-[#8c6b4f] mt-2 tracking-widest font-bold">碑帖圖像遊戲</p>
</div>
<div class="w-full max-w-2xl h-0.5 bg-gradient-to-r from-transparent via-[#8c6b4f] to-transparent"></div>
</div>

<!-- 中間區域：名字輸入與學子登錄 -->
<div class="w-full max-w-lg mb-6 scroll-paper border classic-border rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center space-y-4 shadow-lg z-20">
<p class="text-[#9c1b1f] font-black tracking-widest text-center txt-general">
「翰墨舞乾坤，落筆見真章」
</p>
<div class="w-full max-w-[320px]">
<input type="text" id="input-username" placeholder="請輸入學子姓名..."
class="w-full bg-[#fdfcf7] border border-[#8c6b4f]/60 text-[#1a1a1a] placeholder-[#8c6b4f]/50 font-black py-3 px-4 rounded-lg focus:outline-none focus:border-[#9c1b1f] focus:ring-1 focus:ring-[#9c1b1f]/30 text-center tracking-wider shadow-inner font-bold txt-general">
</div>
</div>

<!-- 下半部：「線裝書卷」直接呈現 -->
<div class="w-full max-w-4xl scroll-paper classic-border rounded-2xl shadow-xl p-3 sm:p-5 relative">
<!-- 線裝書裝飾中央中縫線 -->
<div class="absolute left-1/2 top-0 bottom-0 w-0.5 bg-[#8c6b4f]/30 -translate-x-1/2 z-30 hidden md:block border-l border-dashed border-[#8c6b4f]/20"></div>
<!-- 書角包邊裝飾 -->
<div class="absolute top-0 left-0 w-8 h-8 border-t-4 border-l-4 border-[#8c6b4f] rounded-tl-xl opacity-75"></div>
<div class="absolute bottom-0 right-0 w-8 h-8 border-b-4 border-r-4 border-[#8c6b4f] rounded-br-xl opacity-75"></div>

<div class="w-full h-full flex flex-col md:flex-row bg-[#fdfaf2] rounded-lg overflow-hidden relative text-[#2c2c2c] min-h-[340px]">

<!-- 左側書頁：模式介紹 -->
<div id="book-left-page" class="w-full md:w-1/2 p-6 sm:p-8 flex flex-col justify-center border-b md:border-b-0 md:border-r border-[#8c6b4f]/20 bg-[#fdfcf7] transition-all duration-300">
<div class="space-y-4">
<!-- 標題 -->
<h3 id="mode-book-title" class="title-font txt-title text-[#9c1b1f] tracking-wider border-b border-[#8c6b4f]/10 pb-2">一般模式</h3>
<!-- 說明文字 -->
<p id="mode-book-desc" class="txt-general text-[#4a4a4a] leading-relaxed font-semibold">
全題庫核心必考題50題。
</p>
</div>
</div>

<!-- 右側書頁：入口按鈕 -->
<div id="book-right-page" class="w-full md:w-1/2 p-6 sm:p-8 flex flex-col justify-center items-center bg-[#fdfcf7] relative">
<div class="w-full py-4 flex flex-col items-center justify-center space-y-6">
<span class="font-black text-[#8c6b4f] tracking-widest block text-center txt-general">
✨ 準備好了嗎？ ✒️
</span>

<!-- 挑戰入口按鈕：各模式光暈套用於按鈕外框 -->
<div class="relative w-full max-w-[280px] group mt-4">
<div id="challenge-btn-glow" class="absolute -inset-1 rounded-full blur transition duration-300 opacity-65 glow-blue"></div>
<button type="button" id="btn-start-challenge" class="relative w-full py-4 bg-[#9c1b1f] text-[#fdfaf2] hover:bg-[#801418] font-bold rounded-full border border-[#8c6b4f]/30 hover:border-white active:scale-95 transition-all tracking-widest whitespace-nowrap shadow-md txt-general">
進入挑戰
</button>
</div>
</div>
</div>

</div>
</div>

<!-- 下方控制列：分頁導航器 ＆ 方框外的後台入口 -->
<div class="w-full max-w-4xl flex flex-col sm:flex-row justify-between items-center mt-6 px-4 relative gap-4 sm:gap-0">
<!-- 第三象限（下半部左側）：方框外的後台入口 -->
<div class="sm:absolute sm:left-4 sm:top-1/2 sm:-translate-y-1/2 z-20">
<button type="button" id="btn-go-admin" class="txt-general text-[#8c6b4f] hover:text-[#9c1b1f] underline font-black transition flex items-center space-x-2 bg-[#fdfcf7] border border-[#8c6b4f]/30 px-4 py-2 rounded-lg shadow-sm">
<span>🚪 夫子點名冊</span>
</button>
</div>

<!-- 書頁翻頁導航器 -->
<div class="flex items-center space-x-6 mx-auto">
<button type="button" id="btn-prev-mode" class="p-3 bg-[#fdfcf7] hover:bg-[#f5efe2] rounded-full border border-[#8c6b4f] transition shadow-sm">
<svg class="w-6 h-6 text-[#8c6b4f]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
<path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M15 19l-7-7 7-7" />
</svg>
</button>
<div class="flex space-x-3" id="mode-indicators">
<!-- 動態指示圓點 -->
</div>
<button type="button" id="btn-next-mode" class="p-3 bg-[#fdfcf7] hover:bg-[#f5efe2] 
