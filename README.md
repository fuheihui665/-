
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>祝福语复制工具</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#4F46E5',
                        secondary: '#EC4899',
                        accent: '#8B5CF6',
                        neutral: '#1F2937',
                        'neutral-light': '#F3F4F6',
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                    animation: {
                        'fade-in': 'fadeIn 0.5s ease-in-out',
                        'bounce-light': 'bounceLight 1s ease-in-out',
                    },
                    keyframes: {
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' },
                        },
                        bounceLight: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-5px)' },
                        }
                    }
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            }
            .card-hover {
                @apply transition-all duration-300 hover:shadow-lg hover:-translate-y-1;
            }
            .btn-primary {
                @apply bg-primary hover:bg-primary/90 text-white font-medium py-2 px-4 rounded-lg transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-primary/50;
            }
            .btn-success {
                @apply bg-green-500 hover:bg-green-600 text-white font-medium py-2 px-4 rounded-lg transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-green-400/50;
            }
            .blessing-container {
                counter-reset: blessing-counter;
            }
            .blessing-item::before {
                counter-increment: blessing-counter;
                content: counter(blessing-counter) ". ";
                color: #4F46E5;
                font-weight: bold;
                margin-right: 8px;
            }
        }
    </style>
</head>
<body class="bg-gradient-to-br from-indigo-50 to-purple-50 min-h-screen font-sans">
    <div class="container mx-auto px-4 py-12 max-w-5xl">
        <!-- 页面标题 -->
        <header class="text-center mb-12 animate-fade-in">
            <h1 class="text-[clamp(2rem,5vw,3.5rem)] font-bold text-neutral mb-4 text-shadow">
                <span class="text-primary">祝福</span><span class="text-secondary">语</span>
                <span class="text-accent">复制工具</span>
            </h1>
            <p class="text-lg text-neutral/70 max-w-2xl mx-auto">放开那三国2祝福语 欢迎转发</p>
        </header>

         <!-- 祝福语列表 -->
        <main class="grid grid-cols-1 md:grid-cols-2 gap-6 blessing-container">
            <!-- 第1句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-1">
                            祝大家端午安康
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-1">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第2句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-2">
                           香囊寄思
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-2">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第3句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-3">
                            粽子飘香
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-3">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第4句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-4">
                            万树千山粽是情
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-4">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第5句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-5">
                            送你一颗好运粽
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-5">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第6句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-6">
                          五月五赛龙舟
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-6">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第7句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-7">
                           好的东西就需要分享
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-7">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第8句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-8">
                            愿幸福的粽叶裹住你
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-8">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第9句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-9">
                            送你一只香甜粽子
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-9">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第10句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-10">
                            想拉着你的手一起看龙舟
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-10">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>
    

   
            <!-- 第11句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-11">
                            禁止端午节不理我
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-11">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第12句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-12">
                            今年送你的粽子不一般
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-12">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第13句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-13">
                            祝你端午吉祥如意
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-13">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第14句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-14">
                           希望你粽是幸运
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-14">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第15句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-15">
                            蒲月初五是端午
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-15">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第16句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-16">
                           青绿的粽叶包裹浓浓的真情
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-16">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第17句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-17">
                           五色的丝线迎风飞舞
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-17">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第18句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-18">
                            五色新丝缠角粽
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-18">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第19句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-19">
                            汨罗江在诉说着一段神奇的故事
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-19">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第20句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-20">
                           又是佳节好时光
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-20">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>
    

 
            <!-- 第21句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-21">
                           热烈龙舟划动着千年的祈愿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-21">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第22句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-22">
                            愿你品尝出人生的夸姣和蒲月五的情怀
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-22">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第23句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-23">
                           吃的是粽子甜的是生活
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-23">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第24句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-24">
                          长长丝线绑健康
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-24">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第25句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-25">
                            六月的轻风飘来淡淡的粽香
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-25">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第26句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-26">
                          甜甜粽馅溢飘香
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-26">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第27句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-27">
                            希望祝福能随着艾叶的淡淡清香飘到你那里
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-27">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第28句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-28">
                            赛舟驰骋处处祥
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-28">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第29句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-29">
                         汨罗江在诉说着一段传奇的故事
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-29">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第30句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-30">
                           五月端午粽糕飘香
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-30">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>



            <!-- 第31句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-31">
                          粽叶艾草继续着不变的清香
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-31">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第32句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-32">
                            投粽江河喂鱼以祭屈原
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-32">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第33句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-33">
                          片片艾叶片片情
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-33">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第34句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-34">
                           温婉甜粽在线打call
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-34">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第35句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-35">
                          咸甜之争烽烟再起
                  </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-35">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第36句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-36">
                           只有油润不腻味道香甜的肉粽才是王道
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-36">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第37句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-37">
                          深红色的咸肉泛着油光
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-37">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第38句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-38">
                           咬上一口仿佛时间都静
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-38">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第39句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-39">
                          还有鲜香无比的蛋黄肉粽
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-39">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第40句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-40">
                          丰富的口感让我欲罢不能
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-40">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>



            <!-- 第41句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-41">
                            肉粽知道灵魂的去处
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-41">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第42句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-42">
                          肉粽党发言完毕
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-42">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第43句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-43">
                            清清爽爽的甜粽才是人间值得
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-43">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第44句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-44">
                           雪白的糯米包着甜甜的蜜枣
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-44">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第45句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-45">
                           一定要让粽子在凉水里冷静一下
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-45">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第46句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-46">
                         粘上点白糖就更绝了
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-46">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第47句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-47">
                           白糖会使糯米更加的香甜弹牙
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-47">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第48句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-48">
                            那种幸福从脚尖直冲到天灵盖的感觉
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-48">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第49句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-49">
                            永生都难以忘记
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-49">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第50句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-50">
                           甜粽党发言完毕条
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-50">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第51句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-51">
                            到底是甜粽还是咸粽呢
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-51">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第52句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-52">
                          我觉得你要比粽子甜上那么一点
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-52">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第53句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-53">
                            乘着龙舟给你捎来端午的问候
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-53">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第54句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-54">
                            乘着龙舟给你捎来端午的问候
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-54">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第55句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-55">
                            祝你健康平安过个清清凉凉的夏天
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-55">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第56句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-56">
                          红红的樱桃红红的枣
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-56">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第57句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-57">
                            用艾叶把烦恼都赶跑
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-57">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第58句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-58">
                            愿你拥有人间最美好最珍贵的一切
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-58">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第59句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-59">
                            无
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-59">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第60句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-60">
                          无
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-60">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>
    

   
            <!-- 第61句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-61">
                            小小的粽子里藏着我最真的心意
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-61">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第62句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-62">
                           愿你平安喜乐
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-62">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第63句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-63">
                            在江面的龙舟上再续永恒的主题
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-63">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第64句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-64">
                           相比粽子的甜咸我在意的是假期的长短
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-64">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第65句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-65">
                            无
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-65">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第66句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-66">
                          一层层的粽叶包裹的都是生活的香甜
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-66">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第67句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-67">
                           整个六月都飘着艾叶配粽子的香气
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-67">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第68句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-68">
                            我永远支持甜粽
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-68">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第69句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-69">
                            没什么好说的粽子就该是咸的﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-69">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第70句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-70">
                            无
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-70">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>
    

 
            <!-- 第71句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-71">
                           甜的咸的其实都行
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-71">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第72句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-72">
                           让我们一起干了这杯雄黄酒﻿ 
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-72">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第73句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-73">
                            这枚香袋是我亲手做的﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-73">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第74句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-74">
                          用千娇百媚的芭蕉叶把你轻轻包裹﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-74">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第75句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-75">
                           让纸鸢带着我的祝福飞向你﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-75">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第76句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-76">
                            挂着彩绳放风筝是端午最开心的事了﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-76">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第77句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-77">
                            平安吉祥端午安康
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-77">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第78句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-78">
                            艾蒿高高门前舞
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-78">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第79句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-79">
                           苇叶和糯米也包含着对屈原的无限敬意
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-79">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第80句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-80">
                           路漫漫其修远兮
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-80">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>



            <!-- 第81句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-81">
                          吾将上下而求索
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-81">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第82句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-82">
                            吃粽子的同时也要记得驱五毒哦﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-82">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第83句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-83">
                           万人齐赛龙舟真是再壮观不过了
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-83">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第84句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-84">
                          这五彩的丝线缠着的是我的无尽牵挂
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-84">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第85句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-85">
                            我可是最棒的龙舟手﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-85">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第86句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-86">
                           希望你的六月有西瓜的清凉
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-86">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第87句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-87">
                          无
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-87">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第88句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-88">
                           希望六月能善待你﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-88">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第89句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-89">
                           一株暗香四溢的艾草传递着我的情意﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-89">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第90句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-90">
                         端午假期能见到你才是最幸福的事﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-90">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>



            <!-- 第91句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-91">
                          粽子和我的爱意一样都是甜的﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-91">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第92句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-92">
                         清润端阳节﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-92">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第93句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-93">
                           茅檐插艾新﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-93">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第94句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-94">
                       浴兰包粽念忠臣﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-94">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第95句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-95">
                          千古不亡湘水身﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-95">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第96句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-96">
                         甜的咸的我都吃﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-96">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第97句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-97">
                           咸蛋黄遇见白糯米﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-97">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第98句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-98">
                          幸运的我遇见最好的你﻿
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-98">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第99句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-99">
                           我从咸粽区来看甜粽区的你
                        </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-99">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- 第100句祝福语 -->
            <div class="bg-white rounded-xl shadow-md p-6 card-hover">
                <div class="flex flex-col md:flex-row gap-4">
                    <div class="md:w-4/5">
                        <p class="text-neutral text-lg blessing-item" id="blessing-100">
                           无
                    </p>
                    </div>
                    <div class="md:w-1/5 flex justify-center md:justify-end">
                        <button class="copy-btn btn-primary flex items-center" data-target="blessing-100">
                            <i class="fa-regular fa-copy mr-2"></i>
                            <span>复制</span>
                        </button>
                    </div>
                </div>
            </div>


        <!-- 复制成功提示 -->
        <div id="toast" class="fixed bottom-6 left-1/2 transform -translate-x-1/2 bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg opacity-0 transition-opacity duration-300 flex items-center">
            <i class="fa-regular fa-check-circle mr-2"></i>
            <span id="toast-message">复制成功</span>
        </div>

        <!-- 页脚 -->
        <footer class="mt-16 text-center text-neutral/50 text-sm">
            <p>伏黑惠</p>
        </footer>


    <script>
        // 获取所有复制按钮
        const copyButtons = document.querySelectorAll('.copy-btn');
        const toast = document.getElementById('toast');
        const toastMessage = document.getElementById('toast-message');

        // 为每个复制按钮添加点击事件
        copyButtons.forEach(button => {
            button.addEventListener('click', () => {
                // 获取要复制的祝福语元素
                const targetId = button.getAttribute('data-target');
                const blessingElement = document.getElementById(targetId);
                
                // 创建临时文本区域并复制内容
                const textArea = document.createElement('textarea');
                textArea.value = blessingElement.textContent.trim().replace(/^\d+\.\s/, ''); // 移除序号
                document.body.appendChild(textArea);
                textArea.select();
                document.execCommand('copy');
                document.body.removeChild(textArea);
                
                // 更改按钮样式和文本
                const originalHTML = button.innerHTML;
                button.innerHTML = '<i class="fa-regular fa-check mr-2"></i><span>已复制</span>';
                button.classList.remove('btn-primary');
                button.classList.add('btn-success');
                
                // 显示提示信息
                showToast('复制成功');
                
                // 3秒后恢复按钮原状
                setTimeout(() => {
                    button.innerHTML = originalHTML;
                    button.classList.remove('btn-success');
                    button.classList.add('btn-primary');
                }, 1000);
            });
        });

        // 显示提示信息函数
        function showToast(message) {
            toastMessage.textContent = message;
            toast.classList.replace('opacity-0', 'opacity-100');
            
            // 3秒后隐藏提示
            setTimeout(() => {
                toast.classList.replace('opacity-100', 'opacity-0');
            }, 1000);
        }

        // 页面加载动画
        document.addEventListener('DOMContentLoaded', () => {
            const cards = document.querySelectorAll('.card-hover');
            cards.forEach((card, index) => {
                setTimeout(() => {
                    card.classList.add('animate-fade-in');
                }, 100 * index);
            });
        });
    </script>

    
