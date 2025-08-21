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
     2025年8月22日5:40更新</div>
  </footer>

  <div id="toast" class="fixed bottom-6 left-1/2 transform -translate-x-1/2 bg-success text-white px-4 py-2 rounded-sm shadow-md opacity-0 transition-opacity duration-300">
    <i class="fa fa-check mr-1"></i>
    <span>已复制</span>
  </div>
  <script>
       const blessings = [
    { id: 1, content: "跃动夏日挥洒青春" },
    { id: 2, content: "跃动青春乐翻天" },
    { id: 3, content: "转眼就到了暑期的尾声" },
    { id: 4, content: "夏天我们喜欢你" },
    { id: 5, content: "天气有凉快一点吗" },
    { id: 6, content: "每到开学心情都很复杂" },
    { id: 7, content: "已经在期盼下一个暑期了" },
    { id: 8, content: "下一个长假在哪里" },
    { id: 9, content: "呼唤长假" },
    { id: 10, content: "今年的避暑方式是玩放三2" },
    { id: 11, content: "夏末安康前程似锦" },
    { id: 12, content: "暑意渐消好运常伴" },
    { id: 13, content: "假期尾声快乐永存" },
    { id: 14, content: "夏日悠长秋来收获" },
    { id: 15, content: "夏风拂去秋月将至" },
    { id: 16, content: "盛夏余温温暖一秋" },
    { id: 17, content: "光阴入酒敬此夏秋" },
    { id: 18, content: "夏日不负未来可期" },
    { id: 19, content: "暑期收官学业精进" },
    { id: 20, content: "玩心收敛动力满格" },
    { id: 21, content: "蓄力一夏开学必胜" },
    { id: 22, content: "告别暑假迎接新学期" },
    { id: 23, content: "星依云渚冷" },
    { id: 24, content: "露滴盘中圆" },
    { id: 25, content: "好花生木末" },
    { id: 26, content: "衰蕙愁空园" },
    { id: 27, content: "夜天如玉砌" },
    { id: 28, content: "池叶极青钱" },
    { id: 29, content: "仅厌舞衫薄" },
    { id: 30, content: "稍知花簟寒" },
    { id: 31, content: "晓风何拂拂" },
    { id: 32, content: "北斗光阑干" },
    { id: 33, content: "露如微霰下前池" },
    { id: 34, content: "月过回塘万竹悲" },
    { id: 35, content: "浮世本来多聚散" },
    { id: 36, content: "红蕖何事亦离披" },
    { id: 37, content: "悠扬归梦惟灯见" },
    { id: 38, content: "濩落生涯独酒知" },
    { id: 39, content: "岂到白头长只尔" },
    { id: 40, content: "嵩阳松雪有心期" },
    { id: 41, content: "一雨萧然万瓦鸣" },
    { id: 42, content: "好风如水坐来生" },
    { id: 43, content: "江声入夜惊围屋" },
    { id: 44, content: "秋色明朝定满城" },
    { id: 45, content: "郊外共知农事足" },
    { id: 46, content: "里中争说长官清" },
    { id: 47, content: "野人何以酬佳兴" },
    { id: 48, content: "自汲新泉破茗烹" },
    { id: 49, content: "愿你为秋天开个好头" },
    { id: 50, content: "与快乐相伴" },
    { id: 51, content: "无" },
    ];

    // 渲染函数
    function renderBlessings() {
      const container = document.getElementById('blessingContainer');
      container.innerHTML = blessings.map(blessing => `
        <div class="blessing-card bg-white rounded-sm shadow-micro p-3">
          <div class="flex items-center mb-2">
            <div class="w-6 h-6 bg-primary/10 rounded-full flex items-center justify-center mr-2">
              <span class="text-primary font-semibold text-sm">${blessing.id}</span>
            </div>
            <p class="text-gray-800 text-base ${blessing.content === '无' ? 'text-gray-400 italic' : ''}">
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
  
