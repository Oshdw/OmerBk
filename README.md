# OmerBk
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مخطط علم أدوية المضادات الحيوية</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Tajawal', sans-serif;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 450px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 350px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
    </style>
</head>
<body class="bg-gray-100">

    <div class="container mx-auto p-4 md:p-8">

        <header class="text-center mb-12">
            <h1 class="text-4xl md:text-5xl font-black text-[#4C5B8C]">مخطط علم أدوية المضادات الحيوية</h1>
            <p class="text-lg text-gray-600 mt-2">نظرة شاملة على آليات عمل المضادات الحيوية وتصنيفاتها الرئيسية</p>
        </header>

        <main class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

            <div class="lg:col-span-3 bg-white rounded-lg shadow-lg p-6">
                <h2 class="text-2xl font-bold text-[#00A6A6] mb-4 flex items-center">
                    <span class="text-3xl ml-3">🧱</span> 1. مثبطات تصنيع جدار الخلية
                </h2>
                <p class="text-gray-700 mb-6">
                    هذه الأدوية تستهدف بناء جدار الخلية البكتيرية، مما يؤدي إلى ضعفها وموتها. تعتبر هذه المجموعة من أقدم وأهم المضادات الحيوية. الرسم البياني يوضح التوزيع النسبي لأشهر الفئات ضمن هذه المجموعة.
                </p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 items-center">
                    <div>
                        <div class="chart-container">
                            <canvas id="cellWallChart"></canvas>
                        </div>
                    </div>
                    <div>
                        <div class="space-y-4">
                            <div class="p-4 bg-blue-50 rounded-lg">
                                <h3 class="font-bold text-blue-800">مجموعة البيتا لاكتام (β-Lactams)</h3>
                                <p class="text-sm text-blue-700">تشمل البنسلينات، السيفالوسبورينات، الكاربابينيمات، والمونوباكتامات. تتميز بفاعليتها العالية.</p>
                            </div>
                            <div class="p-4 bg-red-50 rounded-lg">
                                <h3 class="font-bold text-red-800">الجليكوببتيدات (Glycopeptides)</h3>
                                <p class="text-sm text-red-700">مثل الفانكومايسين، فعالة ضد البكتيريا موجبة الجرام المقاومة مثل MRSA.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="lg:col-span-3 bg-white rounded-lg shadow-lg p-6">
                <h2 class="text-2xl font-bold text-[#F28F3B] mb-4 flex items-center">
                    <span class="text-3xl ml-3">🧬</span> 2. مثبطات تصنيع البروتين
                </h2>
                <p class="text-gray-700 mb-6">
                    تستهدف هذه المجموعة الريبوسومات البكتيرية لمنع إنتاج البروتينات الضرورية لحياة البكتيريا. الرسم البياني يقارن بين الفئات المختلفة بناءً على مدى استخدامها وتنوعها.
                </p>
                 <div class="grid grid-cols-1 md:grid-cols-2 gap-6 items-center">
                    <div class="md:order-2">
                        <div class="chart-container">
                            <canvas id="proteinInhibitorsChart"></canvas>
                        </div>
                    </div>
                    <div class="md:order-1">
                       <div class="space-y-4">
                            <div class="p-3 bg-green-50 rounded-lg">
                                <h3 class="font-bold text-green-800">مثبطات 30S</h3>
                                <p class="text-sm text-green-700">تشمل الأمينوغليكوزيدات والتتراسيكلينات، وتؤثر على قراءة الشفرة الوراثية.</p>
                            </div>
                            <div class="p-3 bg-yellow-50 rounded-lg">
                                <h3 class="font-bold text-yellow-800">مثبطات 50S</h3>
                                <p class="text-sm text-yellow-700">تشمل الماكروليدات واللينكوساميدات، وتمنع تكوين سلسلة البروتين.</p>
                            </div>
                             <div class="p-3 bg-purple-50 rounded-lg">
                                <h3 class="font-bold text-purple-800">الكلورامفينيكول</h3>
                                <p class="text-sm text-purple-700">واسع الطيف لكن استخدامه محدود بسبب آثاره الجانبية الخطيرة.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="bg-white rounded-lg shadow-lg p-6">
                <h2 class="text-2xl font-bold text-[#D95F5F] mb-4 flex items-center">
                    <span class="text-3xl ml-3">🔬</span> 3. مثبطات تصنيع الحمض النووي
                </h2>
                <p class="text-gray-700">
                    تعمل هذه الأدوية على تعطيل إنزيمات أساسية لتضاعف وإصلاح الحمض النووي البكتيري (DNA و RNA).
                </p>
                <div class="mt-4 space-y-3">
                    <p><strong class="text-gray-800">الفلوروكينولونات:</strong> تثبط إنزيم DNA gyrase.</p>
                    <p><strong class="text-gray-800">الريفامبين:</strong> يثبط إنزيم RNA polymerase.</p>
                </div>
            </div>

            <div class="bg-white rounded-lg shadow-lg p-6">
                <h2 class="text-2xl font-bold text-[#00A6A6] mb-4 flex items-center">
                    <span class="text-3xl ml-3">🍃</span> 4. مضادات الأيض
                </h2>
                <p class="text-gray-700 mb-4">
                    تمنع تصنيع حمض الفوليك، وهو مركب حيوي لنمو البكتيريا، عبر استهداف خطوتين في مسار التصنيع.
                </p>
                <div class="flex flex-col items-center text-center">
                    <div class="p-3 bg-orange-100 border-2 border-orange-300 rounded-lg shadow">
                        <p class="font-bold">Sulfonamides</p>
                    </div>
                    <div class="h-8 w-1 bg-orange-300 my-1"></div>
                    <div class="p-3 bg-orange-100 border-2 border-orange-300 rounded-lg shadow">
                        <p class="font-bold">Trimethoprim</p>
                    </div>
                     <div class="h-8 w-1 bg-red-400 my-1"></div>
                    <div class="p-3 bg-red-200 border-2 border-red-400 rounded-lg shadow">
                        <p class="font-bold text-red-800">لا يتم تصنيع حمض الفوليك</p>
                    </div>
                </div>
            </div>

            <div class="bg-white rounded-lg shadow-lg p-6">
                <h2 class="text-2xl font-bold text-[#4C5B8C] mb-4 flex items-center">
                    <span class="text-3xl ml-3">💧</span> 5. مؤثرات على غشاء الخلية
                </h2>
                <p class="text-gray-700">
                    تتسبب في تلف غشاء الخلية البكتيرية، مما يؤدي إلى تسرب محتوياتها وموتها. تستخدم غالبًا للعدوى المقاومة.
                </p>
                 <div class="mt-4 p-4 bg-indigo-100 rounded-lg text-center">
                    <p class="font-bold text-indigo-800">البوليميكسينات (Polymyxins)</p>
                    <p class="text-sm text-indigo-700">فعالة ضد البكتيريا سالبة الجرام المقاومة للأدوية المتعددة.</p>
                </div>
            </div>
        </main>

        <footer class="text-center mt-12 text-sm text-gray-500">
            <p>تم إنشاء هذا المخطط لتسهيل المراجعة البصرية. المعلومات المقدمة هي لغرض تعليمي فقط.</p>
        </footer>
    </div>

    <script>
        const tooltipTitleCallback = (tooltipItems) => {
            const item = tooltipItems[0];
            let label = item.chart.data.labels[item.dataIndex];
            if (Array.isArray(label)) {
                return label.join(' ');
            }
            return label;
        };

        const commonChartOptions = {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    position: 'bottom',
                    labels: {
                        font: {
                            family: 'Tajawal',
                            size: 12
                        }
                    }
                },
                tooltip: {
                    callbacks: {
                        title: tooltipTitleCallback
                    },
                    bodyFont: {
                        family: 'Tajawal'
                    },
                    titleFont: {
                        family: 'Tajawal'
                    }
                }
            }
        };
        
        const palette = ['#00A6A6', '#F28F3B', '#D95F5F', '#4C5B8C', '#F2C84B'];

        const cellWallCtx = document.getElementById('cellWallChart').getContext('2d');
        new Chart(cellWallCtx, {
            type: 'doughnut',
            data: {
                labels: ['البنسلينات', 'السيفالوسبورينات', 'الكاربابينيمات', 'الجليكوببتيدات'],
                datasets: [{
                    label: 'التوزيع النسبي',
                    data: [40, 35, 15, 10],
                    backgroundColor: palette,
                    borderColor: '#FFFFFF',
                    borderWidth: 3
                }]
            },
            options: commonChartOptions
        });

        const proteinInhibitorsCtx = document.getElementById('proteinInhibitorsChart').getContext('2d');
        new Chart(proteinInhibitorsCtx, {
            type: 'bar',
            data: {
                labels: ['الماكروليدات', 'التتراسيكلينات', 'الأمينوغليكوزيدات', 'اللينكوساميدات', 'الكلورامفينيكول'],
                datasets: [{
                    label: 'مؤشر الاستخدام والتنوع',
                    data: [90, 80, 65, 60, 20],
                    backgroundColor: palette,
                    borderColor: palette.map(color => color + 'B3'),
                    borderWidth: 1
                }]
            },
            options: {
                ...commonChartOptions,
                indexAxis: 'y',
                scales: {
                    x: {
                        beginAtZero: true,
                        ticks: {
                             font: { family: 'Tajawal' }
                        }
                    },
                    y: {
                       ticks: {
                             font: { family: 'Tajawal' }
                        }
                    }
                },
                plugins: {
                    ...commonChartOptions.plugins,
                    legend: {
                        display: false
                    }
                }
            }
        });
    </script>
</body>
</html>
