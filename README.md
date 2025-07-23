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
{id: 1, content: "暑期祝福语来啦"},
{id: 2, content: "踏沙拾贝掬浪欢歌"},
{id: 3, content: "暑期狂欢快乐无限~"},
{id: 4, content: "踏浪拾光"},
{id: 5, content: "海风送爽踏浪来"},
{id: 6, content: "以下给大家带来几种夏日套餐"},
{id: 7, content: "休养生息套餐"},
{id: 8, content: "WIFI西瓜空调"},
{id: 9, content: "清凉度假套餐"},
{id: 10, content: "酷爽放三2套餐"},
{id: 11, content: "炎炎夏日属于我的只有放开那三国2"},
{id: 12, content: "蝉鸣微风空调肥宅快乐水"},
{id: 13, content: "你说的真好我竟然感受到了一丝清凉"},
{id: 14, content: "夏天的灵魂就是空调和西瓜"},
{id: 15, content: "夏天的风会吹来好消息"},
{id: 16, content: "炎炎夏日也挡不住我爱玩的心"},
{id: 17, content: "是时候把我的新时装换上了"},
{id: 18, content: "不瞒你说夏天并没有影响我的食欲"},
{id: 19, content: "我好像饿得更快了"},
{id: 20, content: "还是待在空调房玩放三2最舒服了"},
{id: 21, content: "让盛夏的阳光晒走你的阴霾吧"},
{id: 22, content: "希望天天都是夏日可以冲浪"},
{id: 23, content: "待在空调房盖着棉被玩放三2"},
{id: 24, content: "楼上带我一个一起玩三国"},
{id: 25, content: "夏天一定要吃烧烤啊"},
{id: 26, content: "烧烤就要配啤酒"},
{id: 27, content: "这个暑期给放三2充电"},
{id: 28, content: "为战力冲冲冲"},
{id: 29, content: "我把西瓜的第一口给你吃"},
{id: 30, content: "暑假到了也要注意身体哦"},
{id: 31, content: "炎热的夏天和沙滩最配了"},
{id: 32, content: "终于可以去电影院了"},
{id: 33, content: "夏天就是要去海边"},
{id: 34, content: "海边度假心情好"},
{id: 35, content: "和我一起去游泳吧"},
{id: 36, content: "何以销烦暑"},
{id: 37, content: "端居一院中"},
{id: 38, content: "眼前无长物"},
{id: 39, content: "窗下有清风"},
{id: 40, content: "热散由心静"},
{id: 41, content: "凉生为室空"},
{id: 42, content: "此时身自得"},
{id: 43, content: "难更与人同"},
{id: 44, content: "携杖来追柳外凉"},
{id: 45, content: "画桥南畔倚胡床"},
{id: 46, content: "月明船笛参差起"},
{id: 47, content: "风定莲池自在香"},
{id: 48, content: "云收雨过波添"},
{id: 49, content: "楼高水冷瓜甜"},
{id: 50, content: "绿树阴垂画檐"},
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

    
