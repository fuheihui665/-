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
{id: 1, content: "流萤织梦晚风裁夏"},
{id: 2, content: "愿你夏日清凉舒爽"},
{id: 3, content: "冰镇西瓜甜透你心"},
{id: 4, content: "阳光灿烂笑容常伴"},
{id: 5, content: "树荫清风伴你左右"},
{id: 6, content: "冰棍汽水快乐无限"},
{id: 7, content: "海浪沙滩尽情欢笑"},
{id: 8, content: "向日葵般明媚向阳"},
{id: 9, content: "夏风送爽心情飞扬"},
{id: 10, content: "萤火虫点亮你夏夜"},
{id: 11, content: "所有美好都在盛夏奔向你"},
{id: 12, content: "暑气消散好运常驻"},
{id: 13, content: "清凉一夏自在无忧"},
{id: 14, content: "西瓜空调夏日标配"},
{id: 15, content: "泳池浪花畅快淋漓"},
{id: 16, content: "花香蝉鸣夏日悠长"},
{id: 17, content: "愿清凉海风常伴你左右"},
{id: 18, content: "树荫蝉鸣编织夏日乐章"},
{id: 19, content: "冰爽汽水冲走所有烦忧"},
{id: 20, content: "西瓜空调是夏天的真爱"},
{id: 21, content: "星空下畅聊夏夜无限长"},
{id: 22, content: "阳光海浪沙滩笑声飞扬"},
{id: 23, content: "晚风捎来远方的清凉问候"},
{id: 24, content: "所有美好故事都发生在夏天"},
{id: 25, content: "愿你拥有一个难忘的夏日"},
{id: 26, content: "空调房里冰西瓜快乐似神仙"},
{id: 27, content: "冰镇酸梅汤生津"},
{id: 28, content: "荷塘月色送清香"},
{id: 29, content: "晚风轻拂暑气消"},
{id: 30, content: "别院深深夏簟清"},
{id: 31, content: "石榴开遍透帘明"},
{id: 32, content: "荷花芳草垂杨渡"},
{id: 33, content: "荷风送香气"},
{id: 34, content: "竹露滴清响"},
{id: 35, content: "松阴一架半弓苔"},
{id: 36, content: "偶欲看书又懒开"},
{id: 37, content: "竹喧先觉雨"},
{id: 38, content: "山暗已闻雷"},
{id: 39, content: "银烛秋光冷画屏"},
{id: 40, content: "轻罗小扇扑流萤"},
{id: 41, content: "高柳蝉声咽"},
{id: 42, content: "深林鸟影稀"},
{id: 43, content: "雨过不知龙去处"},
{id: 44, content: "一池草色万蛙鸣"},
{id: 45, content: "江南仲夏天"},
{id: 46, content: "时雨下如川"},
{id: 47, content: "卢橘垂金蛋"},
{id: 48, content: "甘蕉吐白莲"},
{id: 49, content: "田家避暑月"},
{id: 50, content: "斗酒共谁欢"},
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

    
