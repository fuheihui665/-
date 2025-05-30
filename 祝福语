<!DOCTYPE html>
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
                           咬上一口仿佛时间都静止了
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
                           甜粽党发言完毕
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


        <!-- 复制成功提示 -->
        <div id="toast" class="fixed bottom-6 left-1/2 transform -translate-x-1/2 bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg opacity-0 transition-opacity duration-300 flex items-center">
            <i class="fa-regular fa-check-circle mr-2"></i>
            <span id="toast-message">复制成功</span>
        </div>

        <!-- 页脚 -->
        <footer class="mt-16 text-center text-neutral/50 text-sm">
            <p>伏黑惠</p>
        </footer>
    </div>

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
</body>
</html>
    
