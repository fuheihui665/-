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
    { id: 1, content: "蝉鸣消暑竹径觅凉" },
    { id: 2, content: "跃动夏日" },
    { id: 3, content: "荷风送爽夏意浓" },
    { id: 4, content: "愿热浪不扰清梦" },
    { id: 5, content: "凉茶常润心田" },
    { id: 6, content: "四季皆有好风景" },
    { id: 7, content: "送你一捧晨露清风" },
    { id: 8, content: "愿暑热不侵身" },
    { id: 9, content: "愿你以清风为友" },
    { id: 10, content: "与绿荫作伴" },
    { id: 11, content: "愿快乐如夏花般绽放" },
    { id: 12, content: "好运如夏阳般炽热" },
    { id: 13, content: "健康如夏草般坚韧" },
    { id: 14, content: "平安如夏夜般宁静" },
    { id: 15, content: "愿你整个夏天都闪闪发光" },
    { id: 16, content: "看云卷云舒" },
    { id: 17, content: "听潮起潮落" },
    { id: 18, content: "让生活充满诗意" },
    { id: 19, content: "让时光温柔以待" },
    { id: 20, content: "愿你今夏无忧" },
    { id: 21, content: "让心在自然中舒展" },
    { id: 22, content: "让爱在时光里流淌" },
    { id: 23, content: "这么快就立秋了" },
    { id: 24, content: "暑气还没过要记得防暑降温" },
    { id: 25, content: "乳鸦啼散玉屏空" },
    { id: 26, content: "一枕新凉一扇风" },
    { id: 27, content: "睡起秋声无觅处" },
    { id: 28, content: "满阶梧叶月明中" },
    { id: 29, content: "始惊三伏尽" },
    { id: 30, content: "又遇立秋时" },
    { id: 31, content: "露彩朝还冷" },
    { id: 32, content: "云峰晚更奇" },
    { id: 33, content: "垄香禾半熟" },
    { id: 34, content: "原迥草微衰" },
    { id: 35, content: "幸好清光里" },
    { id: 36, content: "安仁谩起悲" },
    { id: 37, content: "秋日寻诗独自行" },
    { id: 38, content: "藕花香冷水风情" },
    { id: 39, content: "一凉转觉诗难做" },
    { id: 40, content: "付与梧桐夜雨声" },
    { id: 41, content: "露簟荻竹清" },
    { id: 42, content: "风扇蒲葵轻" },
    { id: 43, content: "一与故人别" },
    { id: 44, content: "再见新蝉鸣" },
    { id: 45, content: "是夕凉飙起" },
    { id: 46, content: "闲境入幽情" },
    { id: 47, content: "回灯见栖鹤" },
    { id: 48, content: "隔竹闻吹笙" },
    { id: 49, content: "夜茶一两杓" },
    { id: 50, content: "秋吟三数声" },
    { id: 51, content: "所思渺千里" },
    { id: 52, content: "云水长洲城" },
    { id: 53, content: "兹晨戒流火" },
    { id: 54, content: "商飙早已惊" },
    { id: 55, content: "云天收夏色" },
    { id: 56, content: "木叶动秋声" },
    { id: 57, content: "万事销身外" },
    { id: 58, content: "生涯在镜中" },
    { id: 59, content: "惟将两鬓雪" },
    { id: 60, content: "明日对秋风" },
    { id: 61, content: "独行独语曲江头" },
    { id: 62, content: "回马迟迟上乐游" },
    { id: 63, content: "萧飒凉风与衰鬓" },
    { id: 64, content: "谁教计会一时秋" },
    { id: 65, content: "不期朱夏尽" },
    { id: 66, content: "凉吹暗迎秋" },
    { id: 67, content: "天汉成桥鹊" },
    { id: 68, content: "星娥会玉楼" },
    { id: 69, content: "寒声喧耳外" },
    { id: 70, content: "白露滴林头" },
    { id: 71, content: "一叶惊心绪" },
    { id: 72, content: "如何得不愁" },
    { id: 73, content: "三伏熏蒸四大愁" },
    { id: 74, content: "暑中方信此生浮" },
    { id: 75, content: "岁华过半休惆怅" },
    { id: 76, content: "且对西风贺立秋" },
    { id: 77, content: "律变新秋至" },
    { id: 78, content: "萧条自此初" },
    { id: 79, content: "花酣莲报谢" },
    { id: 80, content: "叶在柳呈疏" },
    { id: 81, content: "百重堆案掣身闲" },
    { id: 82, content: "一叶秋声对榻眠" },
    { id: 83, content: "空山如弄琴愿君好心情" },
    { id: 84, content: "夜短昼长纸短情长" },
    { id: 85, content: "你的圣代是什么味道草莓还是巧克力" },
    { id: 86, content: "冰镇柠檬水是夏天里最简单的快乐" },
    { id: 87, content: "没有比冰镇可乐更让人愉悦的了" },
    { id: 88, content: "淡淡的薰衣草香为你提神" },
    { id: 89, content: "用萤火虫为你照亮方向" },
    { id: 90, content: "追随蜻蜓的脚步" },
    { id: 91, content: "冲完澡要吃西瓜" },
    { id: 92, content: "要记得午睡让精神饱满" },
    { id: 93, content: "最近多雨要记得随身带伞" },
    { id: 94, content: "凉茶绿豆降暑妙招" },
    { id: 95, content: "祝你坏运气清零" },
    { id: 96, content: "祝你好运加满" },
    { id: 97, content: "希望夏天假期可以长一点" },
    { id: 98, content: "愿清凉海风常伴你左右" },
    { id: 99, content: "树荫蝉鸣编织夏日乐章" },
    { id: 100, content: "冰爽汽水冲走所有烦忧" },

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

    
