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
{id: 1, content: "树荫乘凉蝉鸣悠扬"},
{id: 2, content: "绿荫慢摇夏日长"},
{id: 3, content: "夏日尽享狂欢"},
{id: 4, content: "微风送清凉"},
{id: 5, content: "炎炎夏日属于我的只有放开那三国2"},
{id: 6, content: "炎炎夏日微风空调肥宅快乐水"},
{id: 7, content: "夏日的灵魂就是空调和西瓜"},
{id: 8, content: "放开那三国2我夏天的快乐"},
{id: 9, content: "放三2的夏日永远缤纷"},
{id: 10, content: "夏日不仅熬夜还要吃宵夜"},
{id: 11, content: "夏天放三2见"},
{id: 12, content: "炎炎夏日也挡不住我爱玩的心"},
{id: 13, content: "窗外的风吹动叶子"},
{id: 14, content: "希望夏天可以长一点"},
{id: 15, content: "我永远爱夏天"},
{id: 16, content: "去海边记得做好防晒"},
{id: 17, content: "采一缕清凉的风送给夏日的你"},
{id: 18, content: "夏日的风带来拂面的清爽"},
{id: 19, content: "用快乐做风吹散夏天的炎热"},
{id: 20, content: "用心灵的绿茵遮住太阳"},
{id: 21, content: "雨后的霓虹是最美的夏日风景"},
{id: 22, content: "夏天到了要记得去看荷花"},
{id: 23, content: "夏日多暴雨要记得随身带伞啊"},
{id: 24, content: "凉茶绿豆降暑妙招"},
{id: 25, content: "夏日炎炎小心中暑"},
{id: 26, content: "希望你能找到你的夏日限定"},
{id: 27, content: "冰镇西瓜是我爱夏天的理由"},
{id: 28, content: "愿你灿烂如夏花"},
{id: 29, content: "是时候把我的新时装换上了"},
{id: 30, content: "不瞒你说夏天并没有影响我的食欲"},
{id: 31, content: "快把泳装端上来"},
{id: 32, content: "看图解暑也是极好的"},
{id: 33, content: "希望这个夏天没有蚊子叮我"},
{id: 34, content: "山光忽西落"},
{id: 35, content: "池月渐东上"},
{id: 36, content: "散发乘夕凉"},
{id: 37, content: "开轩卧闲敞"},
{id: 38, content: "荷风送香气"},
{id: 39, content: "竹露滴清响"},
{id: 40, content: "夜热依然午热同"},
{id: 41, content: "开门小立月明中"},
{id: 42, content: "竹深树密虫鸣处"},
{id: 43, content: "时有微凉不是风"},
{id: 44, content: "石梁茅屋有弯碕"},
{id: 45, content: "流水溅溅度两陂"},
{id: 46, content: "晴日暖风生麦气"},
{id: 47, content: "绿阴幽草胜花时"},
{id: 48, content: "绿树阴浓夏日长"},
{id: 49, content: "楼台倒影入池塘"},
{id: 50, content: "水晶帘动微风起"},
{id: 51, content: "满架蔷薇一院香"},
{id: 52, content: "荷叶罗裙一色裁"},
{id: 53, content: "芙蓉向脸两边开"},
{id: 54, content: "乱入池中看不见"},
{id: 55, content: "闻歌始觉有人来"},
{id: 56, content: "菱透浮萍绿锦池"},
{id: 57, content: "夏莺千啭弄蔷薇"},
{id: 58, content: "尽日无人看微雨"},
{id: 59, content: "鸳鸯相对浴红衣"},
{id: 60, content: "乳鸭池塘水浅深"},
{id: 61, content: "熟梅天气半晴阴"},
{id: 62, content: "东风载酒西园醉"},
{id: 63, content: "摘尽枇杷一树金"},
{id: 64, content: "携杖来追柳外凉"},
{id: 65, content: "画桥南畔倚胡床"},
{id: 66, content: "月明船笛参差起"},
{id: 67, content: "风定池莲自在香"},
{id: 68, content: "四顾山光接水光"},
{id: 69, content: "凭栏十里芰荷香"},
{id: 70, content: "清风明月无人管"},
{id: 71, content: "并作南楼一味凉"},
{id: 72, content: "愿蝉鸣声中藏着幸运"},
{id: 73, content: "暴雨过后皆是彩虹"},
{id: 74, content: "暑气渐生关怀不减"},
{id: 75, content: "愿你清凉一夏舒心自在"},
{id: 76, content: "心静自然凉无咎不惊慌"},
{id: 77, content: "愿你的夏天像冰镇汽水"},
{id: 78, content: "气泡里藏满惊喜"},
{id: 79, content: "每一口都清甜沁心"},
{id: 80, content: "愿你尝遍夏日甜蜜"},
{id: 81, content: "日子如冰镇西瓜般清爽"},
{id: 82, content: "梦里都是星辰与海浪??"},
{id: 83, content: "愿你在盛夏被晚风的浪漫拥抱"},
{id: 84, content: "愿你收获专属的光芒"},
{id: 85, content: "心怀滚烫理想"},
{id: 86, content: "脚踏坚实土地"},
{id: 87, content: "把清凉的晚风折成信笺"},
{id: 88, content: "写下盛夏的诗行"},
{id: 89, content: "左手握星辉"},
{id: 90, content: "右手触荷香"},
{id: 91, content: "怀揣山海志"},
{id: 92, content: "笑对岁月长"},
{id: 93, content: "愿烦忧随暮云消散"},
{id: 94, content: "欣喜伴夏花蔓延??"},
{id: 95, content: "愿热浪不扰清梦"},
{id: 96, content: "凉茶常润心田"},
{id: 97, content: "四季皆有好风景"},
{id: 98, content: "祝你夏天快乐"},
{id: 99, content: "夏天要和放三2一起过"},
{id: 100, content: "夏天我们放三2见"},
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

    
