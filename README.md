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
{id: 1, content: "激动人心的暑期要来啦"},
{id: 2, content: "这个暑期大家怎么安排"},
{id: 3, content: "去海边是个不错的选择"},
{id: 4, content: "海风轻拂笑声满途"},
{id: 5, content: "暑期逐浪乐一夏"},
{id: 6, content: "赤足踏浪沙暖风轻"},
{id: 7, content: "盛夏进行时"},
{id: 8, content: "怎么办我已经闻到海风的味道了"},
{id: 9, content: "暑期心飞扬"},
{id: 10, content: "还有什么比夏天在水里玩更开心的呢"},
{id: 11, content: "夏天更要动起来"},
{id: 12, content: "放下手机走出空调房"},
{id: 13, content: "拥抱自然的同时要注意防晒"},
{id: 14, content: "快乐暑期天天开心"},
{id: 15, content: "朋友们你们放假吗"},
{id: 16, content: "不放假也要给自己创造假期"},
{id: 17, content: "炎热的夏天和沙滩最配了"},
{id: 18, content: "暑期转眼就来到忧愁烦恼都赶跑"},
{id: 19, content: "暑期来临让烦恼歇歇班"},
{id: 20, content: "暑期快乐到压力往后倒"},
{id: 21, content: "热情胜过酷暑的天气"},
{id: 22, content: "放暑期啦给心情也放个假"},
{id: 23, content: "这个暑期给放三2充电呀"}, 
{id: 24, content: "快乐暑期和我一起变强"},
{id: 25, content: "何以消烦暑"},
{id: 26, content: "端坐一院中"},
{id: 27, content: "眼前无长物"},
{id: 28, content: "窗下有清风"},
{id: 29, content: "懒摇白羽扇"},
{id: 30, content: "裸袒青林中"},
{id: 31, content: "散发乘夕凉"},
{id: 32, content: "开轩卧闲敞"},
{id: 33, content: "荷风送香气"},
{id: 34, content: "竹露滴清响"},
{id: 35, content: "僧舍清凉竹树新"},
{id: 36, content: "初经一雨洗诸尘"},
{id: 37, content: "微风忽起吹莲叶"},
{id: 38, content: "青玉盘中泻水银"},
{id: 39, content: "风蒲猎猎小池塘"},
{id: 40, content: "过雨荷花满院香"},
{id: 41, content: "沈李浮瓜冰雪凉"},
{id: 42, content: "南风不用蒲葵扇"},
{id: 43, content: "纱帽闲眠对水鸥"},
{id: 44, content: "尽室林塘涤暑烦"},
{id: 45, content: "旷然如不在尘寰"},
{id: 46, content: "谁人敢议清风价"},
{id: 47, content: "无乐能过百日闲"},
{id: 48, content: "烈日炎炎嗨翻天"},
{id: 49, content: "清凉有夏暑中有你"},
{id: 50, content: "祝大家暑期快乐"},
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

    
