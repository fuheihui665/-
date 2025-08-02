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
    {"id": 1, "content": "阳光派对嗨翻今夏"},
    {"id": 2, "content": "活力夏日嗨不停"},
    {"id": 3, "content": "沁爽一夏乐不思暑"},
    {"id": 4, "content": "放肆狂欢"},
    {"id": 5, "content": "嗨翻盛夏"},
    {"id": 6, "content": "夏日悠长心情舒畅"},
    {"id": 7, "content": "清凉一夏自在无忧"},
    {"id": 8, "content": "阳光灿烂笑容常伴"},
    {"id": 9, "content": "绿荫相伴夏日安然"},
    {"id": 10, "content": "清风送爽夏日吉祥"},
    {"id": 11, "content": "心静享清凉一夏"},
    {"id": 12, "content": "西瓜管够快乐无限"},
    {"id": 13, "content": "荷风送香夏日安康"},
    {"id": 14, "content": "浪花欢笑暑热尽消"},
    {"id": 15, "content": "夏日甜如蜜"},
    {"id": 16, "content": "无"},
    {"id": 17, "content": "树荫底下好乘凉"},
    {"id": 18, "content": "晚风轻拂好梦入眠"},
    {"id": 19, "content": "注意防暑保持清爽"},
    {"id": 20, "content": "热情似火活力满满"},
    {"id": 21, "content": "燃情一夏乐翻天"},
    {"id": 22, "content": "盛夏狂欢正当时"},
    {"id": 23, "content": "热力全开放肆玩"},
    {"id": 24, "content": "冰爽夏日透心凉"},
    {"id": 25, "content": "畅游碧波消酷暑"},
    {"id": 26, "content": "悠享慢夏好时光"},
    {"id": 27, "content": "荷风摇翠影"},
    {"id": 28, "content": "柳岸踏歌行"},
    {"id": 29, "content": "蝉鸣消暑意"},
    {"id": 30, "content": "竹径觅清凉"},
    {"id": 31, "content": "曲桥观鱼跃"},
    {"id": 32, "content": "芳榭沐荷香"},
    {"id": 33, "content": "榴火燃夏趣"},
    {"id": 34, "content": "兰舟荡碧波"},
    {"id": 35, "content": "浓荫蔽赤日"},
    {"id": 36, "content": "清茗话悠长"},
    {"id": 37, "content": "鱼衔云影碎"},
    {"id": 38, "content": "风送藕香飞"},
    {"id": 39, "content": "碧浪追凉去"},
    {"id": 40, "content": "白鹅引颈歌"},
    {"id": 41, "content": "摇扇呼萤火"},
    {"id": 42, "content": "提灯捕夜风"},
    {"id": 43, "content": "跳珠惊翠盖"},
    {"id": 44, "content": "赤足戏清涟"},
    {"id": 45, "content": "散发乘夕凉"},
    {"id": 46, "content": "开轩卧闲敞"},
    {"id": 47, "content": "何以消烦暑"},
    {"id": 48, "content": "端坐一院中"},
    {"id": 49, "content": "眼前无长物"},
    {"id": 50, "content": "窗下有清风"},

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

    
