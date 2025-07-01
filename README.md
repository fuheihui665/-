<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>祝福语</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#165DFF',
            success: '#00B42A',
            neutral: '#F5F7FA',
            'neutral-light': '#F9FAFB',
          },
          fontFamily: {
            inter: ['Inter', 'system-ui', 'sans-serif'],
          },
          boxShadow: {
            'micro': '0 1px 4px rgba(0,0,0,0.05)',
          },
          borderRadius: {
            'sm': '4px',
          }
        },
      }
    }
  </script>
  
  <style type="text/tailwindcss">
    body {
      overscroll-behavior: none;
    }
    .blessing-card {
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }
    .blessing-card:hover {
      transform: translateX(4px);
      box-shadow: 0 2px 8px rgba(22, 93, 255, 0.1);
    }
  </style>
</head>
<body class="font-inter bg-neutral-light min-h-screen">

  <main class="max-w-6xl mx-auto px-4 pb-12">
    <div class="grid grid-cols-1 gap-3" id="blessingContainer">
      <!-- 祝福语卡片动态生成 -->
    </div>
  </main>

  <footer class="bg-white border-t border-gray-200 py-3">
    <div class="text-center text-xs text-gray-500">
       祝福语工具     </div>
  </footer>

  <div id="toast" class="fixed bottom-6 left-1/2 transform -translate-x-1/2 bg-success text-white px-4 py-2 rounded-sm shadow-md opacity-0 transition-opacity duration-300">
    <i class="fa fa-check mr-1"></i>
    <span>已复制</span>
  </div>

  <script>
       const blessings = [
{ id: 1, content: "冰镇快乐畅玩暑期" },
{ id: 2, content: "祝大家7月快乐" },
{ id: 3, content: "顺顺利利" },
{ id: 4, content: "夏天快乐" },
{ id: 5, content: "7月一定要留下美好回忆" },
{ id: 6, content: "旅游高峰要到了" },
{ id: 7, content: "不想出去看人山人海" },
{ id: 8, content: "只想躺在空调房里玩放三2" },
{ id: 9, content: "还有人能忍住不开空调吗" },
{ id: 10, content: "求下雨求降温" },
{ id: 11, content: "夏日炎炎心要甜" },
{ id: 12, content: "西瓜冰啤享清闲" },
{ id: 13, content: "阳光海浪沙滩边" },
{ id: 14, content: "压力烦恼随浪花走远" },
{ id: 15, content: "尽情拥抱这夏天" },
{ id: 16, content: "冰镇西瓜甜到心尖" },
{ id: 17, content: "好友相聚笑声连连" },
{ id: 18, content: "夏日快乐就在眼前" },
{ id: 19, content: "泳池派对尽情闹" },
{ id: 20, content: "烧烤飘香晚风好" },
{ id: 21, content: "盛夏时光皆尽欢" },
{ id: 22, content: "晚风轻拂星满天" },
{ id: 23, content: "露营烧烤乐无边" },
{ id: 24, content: "夏日悠长好梦甜" },
{ id: 25, content: "冰饮在手暑气消" },
{ id: 26, content: "欢歌笑语兴致高" },
{ id: 27, content: "玩转夏日乐淘淘" },
{ id: 28, content: "冰汽水冒泡" },
{ id: 29, content: "西瓜最中间那块留给你" },
{ id: 30, content: "夏天就要这么甜" },
{ id: 31, content: "烧烤摊的烟火气" },
{ id: 32, content: "晚风里的碰杯声" },
{ id: 33, content: "好吃的和好玩的我都要" },
{ id: 34, content: "去海边踩水花" },
{ id: 35, content: "去山顶吹海风" },
{ id: 36, content: "把快乐装满行囊" },
{ id: 37, content: "阳光热烈" },
{ id: 38, content: "笑容更要热烈" },
{ id: 39, content: "蝉鸣是背景音" },
{ id: 40, content: "树荫是休息区" },
{ id: 41, content: "享受你的夏日节奏" },
{ id: 42, content: "夏日微风里畅享轻松时光" },
{ id: 43, content: "携快乐同行" },
{ id: 44, content: "让每一刻都浸满惬意笑容" },
{ id: 45, content: "于闲暇里拥抱自然美好" },
{ id: 46, content: "愿欢乐常随左右" },
{ id: 47, content: "尽享夏日悠闲与畅快" },
{ id: 48, content: "漫步街头寻一份自在惬意" },
{ id: 49, content: "树荫下小坐品一杯清茶" },
{ id: 50, content: "享片刻宁静时光" },
    ];

    // 渲染函数
    function renderBlessings() {
      const container = document.getElementById('blessingContainer');
      container.innerHTML = blessings.map(blessing => `
        <div class="blessing-card bg-white rounded-sm shadow-micro p-3">
          <div class="flex items-center mb-2">
            <div class="w-6 h-6 bg-primary/10 rounded-full flex items-center justify-center mr-2">
              <span class="text-primary font-semibold text-xs">${blessing.id}</span>
            </div>
            <p class="text-gray-800 text-xs ${blessing.content === '无' ? 'text-gray-400 italic' : ''}">
              ${blessing.content || '（无内容）'}
            </p>
          </div>
          <div class="flex justify-between items-center">
            <span class="text-xs text-gray-400">ID: ${blessing.id.toString().padStart(3, '0')}</span>

            <button class="copy-btn px-8 py-3 bg-primary text-white text-xs rounded-sm" data-id="${blessing.id}">
              <i class="fa fa-copy mr-0.5"></i> 复制
            </button>
          </div>
        </div>
      `).join('');

      // 绑定复制事件
      document.querySelectorAll('.copy-btn').forEach(btn => {
        btn.addEventListener('click', () => {
          const id = parseInt(btn.dataset.id);
          const content = blessings.find(b => b.id === id).content;
          if (content === '无') return showToast('无内容');
          navigator.clipboard.writeText(content).then(() => showToast());
        });
      });
    }

    
    // 初始化渲染
    document.addEventListener('DOMContentLoaded', renderBlessings);

    // 提示框
    function showToast(msg = '已复制') {
      const toast = document.getElementById('toast');
      toast.querySelector('span').textContent = msg;
      toast.classList.add('opacity-100');
      setTimeout(() => toast.classList.remove('opacity-100'), 1500);
    }
  </script>

    
