<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>مراجعة الفورامينفرا - 150 سؤالاً | Gio Ahmed Hasan</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            background: #eef3e9;
            font-family: 'Segoe UI', 'Tahoma', 'Traditional Arabic', Arial, sans-serif;
            padding: 20px;
            color: #1f3a2a;
        }
        .wrapper {
            max-width: 1450px;
            margin: 0 auto;
            background: #fffffa;
            border-radius: 48px;
            box-shadow: 0 25px 45px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        .top-bar {
            background: #2b5e2b;
            padding: 18px 32px;
            color: white;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 18px;
            border-bottom: 5px solid #f3b33d;
        }
        .title-area h1 { font-size: 1.9rem; margin-bottom: 5px; }
        .info-panel { display: flex; align-items: center; gap: 20px; flex-wrap: wrap; }
        .creator { background: #f3b33d; padding: 6px 20px; border-radius: 50px; font-weight: bold; color: #2b5e2b; }
        .avatar { width: 65px; height: 65px; border-radius: 50%; border: 3px solid #ffe1a0; object-fit: cover; }
        .whatsapp-link { background: #25D366; padding: 7px 18px; border-radius: 40px; text-decoration: none; color: white; font-weight: bold; display: inline-flex; align-items: center; gap: 8px; transition: 0.2s; }
        .whatsapp-link:hover { background: #128C7E; transform: scale(1.02);}
        .stats { background: #eaf2e4; padding: 12px 28px; display: flex; justify-content: space-between; flex-wrap: wrap; font-weight: bold; border-bottom: 1px solid #c8dcb2; }
        .main-content { padding: 30px 32px 40px; }
        .section-header { font-size: 1.8rem; border-right: 8px solid #f3b33d; padding-right: 18px; margin: 35px 0 20px 0; font-weight: 800; }
        .grid-2col { display: grid; grid-template-columns: repeat(auto-fill, minmax(380px, 1fr)); gap: 24px; }
        .quiz-card { background: #fefef5; border-radius: 28px; padding: 18px 22px; box-shadow: 0 6px 14px rgba(0,0,0,0.04); border: 1px solid #deedce; transition: 0.2s; }
        .quiz-card:hover { transform: translateY(-3px); box-shadow: 0 12px 22px rgba(0,0,0,0.08); }
        .q-title { font-weight: 800; font-size: 1rem; margin-bottom: 14px; color: #1c3a1c; line-height: 1.4; }
        .opt-list { display: flex; flex-direction: column; gap: 8px; margin: 10px 0; }
        .opt-item { background: #f5f9f0; padding: 6px 14px; border-radius: 50px; display: flex; align-items: center; gap: 12px; cursor: pointer; }
        .tf-group { display: flex; gap: 20px; margin: 12px 0; }
        .tf-group label { background: #f5f9f0; padding: 6px 22px; border-radius: 40px; display: flex; align-items: center; gap: 8px; cursor: pointer; }
        .feedback-msg { margin-top: 14px; padding: 10px 12px; border-radius: 22px; display: none; font-size: 0.85rem; border-right: 5px solid; }
        .feedback-msg.show { display: block; }
        .fb-correct { background: #e1f4de; border-right-color: #2d782d; }
        .fb-wrong { background: #ffe2e1; border-right-color: #c9352f; }
        .source-proof { font-size: 0.75rem; color: #3f6b3a; margin-top: 6px; font-style: italic; border-top: 1px dashed #c2dcac; padding-top: 5px; }
        .reset-button { background: #9e6a3a; border: none; color: white; padding: 7px 28px; border-radius: 40px; font-weight: bold; font-size: 0.9rem; cursor: pointer; margin-top: 10px; }
        footer { background: #eaf0e3; text-align: center; padding: 18px; font-size: 0.8rem; border-top: 1px solid #ccdfb6; }
        @media (max-width: 800px) { .grid-2col { grid-template-columns: 1fr; } .top-bar { flex-direction: column; text-align: center; } }
    </style>
</head>
<body>
<div class="wrapper">
    <div class="top-bar">
        <div class="title-area">
            <h1>🦠 أُحفورة الفورامينفرا</h1>
            <p>100 MCQ + 50 صح/خطأ · جميع الأسئلة فريدة</p>
        </div>
        <div class="info-panel">
            <div class="creator">📖 تم الإنشاء بواسطة <strong>Gio Ahmed Hasan</strong></div>
            <img class="avatar" src="https://i.postimg.cc/pV9jC9J9/Screenshot-20260512-173337.jpg" alt="Gio Ahmed Hasan">
            <a href="https://wa.me/201156229265?text=السلام%20عليكم%20أستاذ%20Gio%20أحتاج%20مساعدة%20في%20أسئلة%20الفورامينفرا" class="whatsapp-link" target="_blank">💬 واتساب 01156229265</a>
        </div>
    </div>
    <div class="stats">
        <span>📌 إجمالي 150 سؤالاً · 100 اختياري + 50 صح/خطأ</span>
        <span>✅ اختَر إجابة لظهور التصحيح والدليل من الكتاب</span>
        <button id="resetGlobal" class="reset-button">🔄 إعادة تعيين جميع الإجابات</button>
    </div>
    <div class="main-content">
        <div class="section-header">📚 الجزء الأول: 100 سؤال اختياري (MCQ)</div>
        <div id="mcqContainer" class="grid-2col"></div>
        <div class="section-header">📝 الجزء الثاني: 50 سؤال صح أو خطأ</div>
        <div id="tfContainer" class="grid-2col"></div>
    </div>
    <footer>📖 جميع الأسئلة مستخلصة من محتوى الكتاب (صفحات 19-105)</footer>
</div>

<script>
    // 100 سؤال اختياري
    const mcq = [
        {q:"تنتمي الفورامينفرا إلى أي شعبة؟",opts:["اللحميات Sarcodina","الهدبيات","السوطيات","البوغيات"],ans:0,proof:"ص20"},
        {q:"الطائفة التي تتبعها الفورامينفرا؟",opts:["جذريات الأقدام Rhizopoda","اللحميات","الساركودينا","الراديولاريا"],ans:0,proof:"ص21"},
        {q:"عدد أنواع الفورامينفرا الحية؟",opts:["4500","1000","250","12000"],ans:0,proof:"ص21"},
        {q:"أول ظهور للفورامينفرا في أي عصر؟",opts:["الكمبري","الأردوفيشي","الديفوني","الكربوني"],ans:0,proof:"ص21"},
        {q:"ما تستخدم كأحفير مرشد؟",opts:["الطافية Pelagic","القاعية","الكيتينية","الميليولينية"],ans:0,proof:"ص21"},
        {q:"لون الهلام الأولي الغالب؟",opts:["برتقالي/أصفر","أخضر","أزرق","أحمر"],ans:0,proof:"ص22"},
        {q:"أي طبقة تفرز الصدفة؟",opts:["الهلام الخارجي","الداخلي","النواة","الفجوة"],ans:0,proof:"ص22"},
        {q:"الأقدام الكاذبة المتشابكة تسمى؟",opts:["شبكة ريتيكيولوبوديا","أرجل لحمية","مخالب","زوائد"],ans:0,proof:"ص21"},
        {q:"الأقدام الكاذبة تستخدم في؟",opts:["بناء الصدفة والغذاء","السباحة فقط","التنفس","الإخراج"],ans:0,proof:"ص23"},
        {q:"كيف تقتل الفريسة؟",opts:["مواد سامة","خنق","تسميم","صعق"],ans:0,proof:"ص23"},
        {q:"امتصاص المواد العضوية المذابة يسمى؟",opts:["Absorption","ترشيح","افتراس","تكافل"],ans:0,proof:"ص24"},
        {q:"الجدار الخزفي تحت الضوء المستقطب لونه؟",opts:["بني","أزرق","أخضر","عديم"],ans:0,proof:"ص32"},
        {q:"الجدار دقيق التحبب يتكون من؟",opts:["بلورات كالسيت دقيقة","رمل","كيتين","سيليكا"],ans:0,proof:"ص33"},
        {q:"الشكل القيني يشبه؟",opts:["قارورة","كرة","أنبوبة","نجمة"],ans:0,proof:"ص34"},
        {q:"الحاجز بين الحجرات يسمى؟",opts:["الدرز Suture","الثلم","الفتحة","السرة"],ans:0,proof:"ص35"},
        {q:"أبسط ترتيب للحجرات؟",opts:["أحادي التسلسل المستقيم","ثنائي","ثلاثي","مخروطي"],ans:0,proof:"ص40"},
        {q:"جنس Textularia ترتيبه؟",opts:["ثنائي التسلسل","أحادي","مليوليدي","لاف"],ans:0,proof:"ص40"},
        {q:"Biloculina يضيف حجرات بزاوية؟",opts:["180°","120°","90°","72°"],ans:0,proof:"ص42"},
        {q:"الفتحة الاستوائية توجد في؟",opts:["اللافه بمستوى واحد","المخروطية","ثنائية","وحيدة"],ans:0,proof:"ص43"},
        {q:"من المخاطر الكيميائية؟",opts:["تذبذب الملوحة وCO2","التيارات","الأشواك","الافتراس"],ans:0,proof:"ص45"},
        {q:"تسود في الأعماق الكبيرة؟",opts:["ذات الجدار التجمعي","الكلسية","الزجاجية","الخزفية"],ans:0,proof:"ص49"},
        {q:"تختفي الكلسية عند عمق؟",opts:["3000م","1000م","200م","500م"],ans:0,proof:"ص49"},
        {q:"القيعان الغنية بالبكتيريا؟",opts:["الغرينية","الرملية","الصخرية","السهول"],ans:0,proof:"ص49"},
        {q:"الفورامينفرا الملتصقة بالصخور أصدافها؟",opts:["قرصية/مروحية","مغزلية","كروية","أنبوبية"],ans:0,proof:"ص50"},
        {q:"جدار Miliolidae يحتوي على؟",opts:["نقر صغيرة","كيتين","مسام شعاعية","أشواك"],ans:0,proof:"ص61"},
        {q:"Peneroplis صدفته؟",opts:["مضغوطة لفة مغلقة","ثلاثية","كروية","أنبوبية"],ans:0,proof:"ص63"},
        {q:"أقصى قطر لـ Nummulites؟",opts:["12سم","3سم","30سم","1سم"],ans:0,proof:"ص74"},
        {q:"الراديولاريا تتحرك بـ؟",opts:["الأقدام الكاذبة","السياط","الأهداب","تيارات"],ans:0,proof:"ص87"},
        {q:"هيكل الراديولاريا من؟",opts:["سليكا غير متبلورة","كربونات","كيتين","فوسفات"],ans:0,proof:"ص87"},
        {q:"العلاقة مع الطحالب تسمى؟",opts:["تكافل Mutualism","تطفل","تعايش","افتراس"],ans:0,proof:"ص25"},
        {q:"صفة الصدفة المتكافلة؟",opts:["جدار رقيق نافذ للضوء","سميك","بدون مسام","فتحة مغلقة"],ans:0,proof:"ص26"},
        {q:"الجيل التزاوجي يسمى؟",opts:["Microspheric","Megalospheric","Schizont","Gamont"],ans:0,proof:"ص29"},
        {q:"الجيل اللاتزاوحي يسمى؟",opts:["Megalospheric","Microspheric","Agamont","Trophozoite"],ans:0,proof:"ص29"},
        {q:"أقدم جدار للفورامينفرا؟",opts:["التجمعي","الخزفي","الزجاجي","الكيتيني"],ans:0,proof:"ص30"},
        {q:"الفتحة الأولية تسمى؟",opts:["Primary aperture","Foramen","Septal","Accessory"],ans:0,proof:"ص43"},
        {q:"الفتحة في الحلزوني عالي الالتفاف؟",opts:["وسط السرة","القمة","الهامش","القاعدة"],ans:0,proof:"ص43"},
        {q:"الزخرفة الطولية تسمى؟",opts:["Costate","Granulose","Striated","Rugose"],ans:0,proof:"ص43"},
        {q:"المليولينية تفضل؟",opts:["ملوحة عالية ومياه ضحلة","عذبة","أعماق","قطبية"],ans:0,proof:"ص56"},
        {q:"أقصى كثافة للطافية عند عمق؟",opts:["10-50م","100-200م","500م","السطح"],ans:0,proof:"ص51"},
        {q:"طريقة موراي تعتمد على؟",opts:["نسبة Rotaliina/Textulariina/Miliolina","حجم الصدفة","عدد الحجرات","اللون"],ans:0,proof:"ص54"},
        {q:"في المخروطية منخفضة اللف الوجه الحلزوني؟",opts:["إلى أعلى","إلى أسفل","جانبياً","عشوائي"],ans:0,proof:"ص55"},
        {q:"ازدهرت Nummulitidae في؟",opts:["الأيوسين","الطباشيري","البرمي","الميوسين"],ans:0,proof:"ص104"},
        {q:"Lituolidae جدارها؟",opts:["تجمعي","زجاجي","خزفي","كيتيني"],ans:0,proof:"ص68"},
        {q:"Trocholina تمثل نمط؟",opts:["مخروطي Trochoidal","مستوي","ثنائي","واحد"],ans:0,proof:"ص42"},
        {q:"اتجاه اللف يتأثر بـ؟",opts:["درجة الحرارة","الملوحة","العمق","الغذاء"],ans:0,proof:"ص48"},
        {q:"أول عائلة من الكمبري؟",opts:["Astrorhizidae","Fusulinidae","Miliolidae","Globigerinidae"],ans:0,proof:"ص102"},
        {q:"Orbitolina من عائلة؟",opts:["Orbitolinidae","Globotruncanidae","Rotaliidae","Nummulitidae"],ans:0,proof:"ص73"},
        {q:"معادلة نظائر الأكسجين؟",opts:["T=16.9-4.2(dc-dw)","T=4.2(dc+dw)","T=20-5δ","T=2δ"],ans:0,proof:"ص60"},
        {q:"Quasifusilina من عائلة؟",opts:["Fusulinidae","Miliolidae","Globigerinidae","Rotaliidae"],ans:0,proof:"ص79"},
        {q:"فتحة وحيدة التسلسل؟",opts:["نهائية Terminal","سرية","استوائية","قاعدية"],ans:0,proof:"ص43"},
        {q:"Dentalina ترتيبه؟",opts:["أحادي التسلسل","ثنائي","ثلاثي","مليوليدي"],ans:0,proof:"ص83"},
        {q:"أكل لحوم الجنس يسمى؟",opts:["Cannibalism","Symbiosis","Parasitism","Commensalism"],ans:0,proof:"ص24"},
        {q:"Frondicularia صدفتها؟",opts:["ورقية مبسطة","كروية","أنبوبية","مغزلية"],ans:0,proof:"ص83"},
        {q:"Miliolidae جدارها؟",opts:["خزفي","زجاجي","تجمعي","كيتيني"],ans:0,proof:"ص61"},
        {q:"Lagena عدد حجراتها؟",opts:["واحدة","اثنتان","ثلاث","عديدة"],ans:0,proof:"ص84"},
        {q:"Allogromia جدارها؟",opts:["كيتيني","تجمعي","خزفي","زجاجي"],ans:0,proof:"ص45"},
        {q:"Ammodiscus يتكون من؟",opts:["حجرتين","واحدة","ثلاث","عديدة"],ans:0,proof:"ص68"},
        {q:"عمق النطاق الضوئي؟",opts:["200م","50م","500م","1000م"],ans:0,proof:"ص48"},
        {q:"Cyclammina صدفتها؟",opts:["لافه مغلقة","وحيدة","ثنائية","مخروطية"],ans:0,proof:"ص69"},
        {q:"الفتحة القاعدية تسمى؟",opts:["Basal aperture","Terminal","Umbilical","Equatorial"],ans:0,proof:"ص43"},
        {q:"Globigerina صفتها؟",opts:["هامة جدار مثقب","قاعية","عدسية","وحيدة"],ans:0,proof:"ص83"},
        {q:"انخفاض الحرارة يسبب؟",opts:["لف يساري","لف يميني","لا تأثير","فقد اللف"],ans:0,proof:"ص48"},
        {q:"الغشاء العضوي يبطن؟",opts:["جدار الصدفة","النواة","الفجوات","الأقدام"],ans:0,proof:"ص45"},
        {q:"Rotalia ترتيبها؟",opts:["مخروطي","أحادي","ثنائي","مليوليدي"],ans:0,proof:"ص88"},
        {q:"الأعمدة الكلسية وظيفتها؟",opts:["توازن هيدروديناميكي","هضم","تنفس","تكاثر"],ans:0,proof:"ص26"},
        {q:"Operculina صدفتها؟",opts:["لافه مفتوح","مغلق","مخروطي","واحد"],ans:0,proof:"ص73"},
        {q:"Alveolina شكلها؟",opts:["كروي/مغزلي","مسطح","أنبوبي","مخروطي"],ans:0,proof:"ص63"},
        {q:"Globigerinidae ظهرت في؟",opts:["الترياسي","الكمبري","الديفوني","البرمي"],ans:0,proof:"ص103"},
        {q:"Heterohelix ترتيبها؟",opts:["ثنائي","أحادي","ثلاثي","مخروطي"],ans:0,proof:"ص77"},
        {q:"الجدار التجمعي يتكون من؟",opts:["حبيبات ملتقطة","كيتين","كالسيت","سيليكا"],ans:0,proof:"ص30"},
        {q:"ظاهرة التغذية على أفراد الجنس؟",opts:["Cannibalism","Symbiosis","Parasitism","Commensalism"],ans:0,proof:"ص24"},
        {q:"جنس Lagena من أي عائلة؟",opts:["Lagenidae","Miliolidae","Globigerinidae","Rotaliidae"],ans:0,proof:"ص84"},
        {q:"الفتحة المنخلية توجد في؟",opts:["بعض الأجناس","جميعها","لا توجد","نادرة"],ans:0,proof:"ص43"},
        {q:"الجدار الزجاجي يتميز بـ؟",opts:["شفاف مثقب","معتم","كيتيني","خشن"],ans:0,proof:"ص33"},
        {q:"عائلة Fusulinidae انقرضت في؟",opts:["البرمي","الطباشيري","الجوراسي","الترياسي"],ans:0,proof:"ص104"},
        {q:"الراديولاريا تعيش؟",opts:["طافية","قاعية","متصلة","مستعمرة"],ans:0,proof:"ص87"},
        {q:"جنس Textularia جداره؟",opts:["تجمعي","خزفي","زجاجي","كيتيني"],ans:0,proof:"ص70"},
        {q:"دورة حياة الفورامينفرا تشمل؟",opts:["جنسي ولا جنسي","جنسي فقط","لاجنسي فقط","انشطار"],ans:0,proof:"ص28"},
        {q:"الأصداف القرصية تعيش؟",opts:["ملتصقة بالأعشاب","حرة","طافية","مدفونة"],ans:0,proof:"ص56"}
    ];

    // 50 سؤال صح/خطأ
    const tf = [
        {s:"الفورامينفرا من شعبة اللحميات",is:true,proof:"ص20"},
        {s:"جميعها تعيش في المياه العذبة",is:false,proof:"ص21"},
        {s:"الأقدام الكاذبة تستخدم في بناء الصدفة",is:true,proof:"ص23"},
        {s:"الجدار الكيتيني يترك أحافير وفيرة",is:false,proof:"ص30"},
        {s:"فوزولينيدا جدارها معقد",is:true,proof:"ص58"},
        {s:"Discorbis له صدفة مخروطية",is:true,proof:"ص87"},
        {s:"فتحة وحيدة التسلسل سرية",is:false,proof:"ص43"},
        {s:"الأشواك تساعد على الطفو",is:true,proof:"ص48"},
        {s:"هيكل الراديولاريا من كربونات الكالسيوم",is:false,proof:"ص87"},
        {s:"التكافل يساعد في ترسيب كربونات الكالسيوم",is:true,proof:"ص26"},
        {s:"المليولينية تعيش في ملوحة منخفضة",is:false,proof:"ص56"},
        {s:"Nodosaria وحيدة الحجرة",is:false,proof:"ص84"},
        {s:"Globotruncanidae تميز الطباشيري العلوي",is:true,proof:"ص77"},
        {s:"نظائر الأكسجين تستخدم للحرارة القديمة",is:true,proof:"ص60"},
        {s:"جميع القاعية تعيش فوق الرواسب",is:false,proof:"ص50"},
        {s:"الجدار الزجاجي غير مثقب",is:false,proof:"ص33"},
        {s:"Quinqueloculina زاوية 72°",is:true,proof:"ص42"},
        {s:"الكلسية تزداد تحت 4000م",is:false,proof:"ص49"},
        {s:"Astrorhizidae أقدم عائلة من الكمبري",is:true,proof:"ص102"},
        {s:"الجدار الرقيق يساعد على نفاذ الضوء",is:true,proof:"ص26"},
        {s:"Lockhartia موجود في الأيوسين",is:true,proof:"ص81"},
        {s:"الجدار الخزفي لونه أبيض ناصع",is:true,proof:"ص32"},
        {s:"التغذية على الفتات في الأعماق المظلمة",is:true,proof:"ص25"},
        {s:"Ammodiscus له حجرتان",is:true,proof:"ص68"},
        {s:"الجيل الميكروسفيري لاجنسي",is:false,proof:"ص29"},
        {s:"الفتحة المتعددة موجودة في بعض الأجناس",is:true,proof:"ص43"},
        {s:"الطافية تعيش في القطبية فقط",is:false,proof:"ص51"},
        {s:"الجدار التجمعي يلتقط حبيبات من البيئة",is:true,proof:"ص30"},
        {s:"Globigerina من القاعية",is:false,proof:"ص83"},
        {s:"Nodosariidae أحادية التسلسل",is:true,proof:"ص83"},
        {s:"الأقدام الكاذبة للسباحة فقط",is:false,proof:"ص23"},
        {s:"جدار الأراجونيت نادر",is:true,proof:"ص32"},
        {s:"الصدفة المغلقة تظهر اللفة الأخيرة فقط",is:true,proof:"ص42"},
        {s:"Lagena وحيدة الحجرة",is:true,proof:"ص84"},
        {s:"القاعية تزداد في البيئات قليلة الأكسجين",is:false,proof:"ص58"},
        {s:"Alveolina من Alveolinidae",is:true,proof:"ص63"},
        {s:"الفتحة المنخلية موجودة",is:true,proof:"ص43"},
        {s:"جميع الفورامينفرا كلسية",is:false,proof:"ص30"},
        {s:"Globorotalia طافية",is:true,proof:"ص79"},
        {s:"Fusulinidae انقرضت بالبرمي",is:true,proof:"ص104"},
        {s:"الراديولاريا قاعية",is:false,proof:"ص87"},
        {s:"Textularia جدارها تجمعي",is:true,proof:"ص70"},
        {s:"تتكاثر جنسياً فقط",is:false,proof:"ص28"},
        {s:"الأصداف القرصية ملتصقة بالأعشاب",is:true,proof:"ص56"},
        {s:"Nummulites يستخدم في تقسيم الأيوسين",is:true,proof:"ص104"},
        {s:"الهلام الداخلي يحتوي النواة",is:true,proof:"ص22"},
        {s:"الأقدام الكاذبة تمسك الفريسة",is:true,proof:"ص23"},
        {s:"Heterohelix قاعية",is:false,proof:"ص77"},
        {s:"Alveolinidae تظهر في الطباشيري السفلي",is:true,proof:"ص63"},
        {s:"الجدار الزجاجي شفاف مثقب",is:true,proof:"ص33"}
    ];

    const mcqContainer = document.getElementById("mcqContainer");
    const tfContainer = document.getElementById("tfContainer");

    mcq.forEach((item, idx) => {
        const card = document.createElement("div");
        card.className = "quiz-card";
        let optsHtml = "";
        item.opts.forEach((opt, optIdx) => {
            optsHtml += `<label class="opt-item"><input type="radio" name="mcq${idx}" value="${optIdx}"> ${String.fromCharCode(65+optIdx)}. ${opt}</label>`;
        });
        card.innerHTML = `<div class="q-title">${idx+1}. ${item.q}</div><div class="opt-list">${optsHtml}</div><div class="feedback-msg" id="fbMcq${idx}"></div>`;
        mcqContainer.appendChild(card);
        card.querySelectorAll(`input[name="mcq${idx}"]`).forEach(radio => {
            radio.addEventListener("change", (e) => {
                const selected = parseInt(e.target.value);
                const fb = document.getElementById(`fbMcq${idx}`);
                fb.classList.add("show");
                if(selected === item.ans) {
                    fb.className = "feedback-msg show fb-correct";
                    fb.innerHTML = `✅ صحيح!<div class="source-proof">📖 ${item.proof}</div>`;
                } else {
                    fb.className = "feedback-msg show fb-wrong";
                    fb.innerHTML = `❌ خطأ. الصحيح: ${String.fromCharCode(65+item.ans)}. ${item.opts[item.ans]}<div class="source-proof">📚 ${item.proof}</div>`;
                }
            });
        });
    });

    tf.forEach((item, idx) => {
        const card = document.createElement("div");
        card.className = "quiz-card";
        card.innerHTML = `<div class="q-title">${idx+1}. ${item.s}</div><div class="tf-group"><label><input type="radio" name="tf${idx}" value="true"> صح ✔️</label><label><input type="radio" name="tf${idx}" value="false"> خطأ ❌</label></div><div class="feedback-msg" id="fbTf${idx}"></div>`;
        tfContainer.appendChild(card);
        card.querySelectorAll(`input[name="tf${idx}"]`).forEach(radio => {
            radio.addEventListener("change", (e) => {
                const selected = e.target.value === "true";
                const fb = document.getElementById(`fbTf${idx}`);
                fb.classList.add("show");
                if(selected === item.is) {
                    fb.className = "feedback-msg show fb-correct";
                    fb.innerHTML = `✅ صحيح!<div class="source-proof">📖 ${item.proof}</div>`;
                } else {
                    fb.className = "feedback-msg show fb-wrong";
                    fb.innerHTML = `❌ خطأ. الصحيح: ${item.is ? "صح" : "خطأ"}<div class="source-proof">📚 ${item.proof}</div>`;
                }
            });
        });
    });

    document.getElementById("resetGlobal").addEventListener("click", () => {
        document.querySelectorAll('input[type="radio"]').forEach(r => r.checked = false);
        document.querySelectorAll('.feedback-msg').forEach(fb => {
            fb.classList.remove("show", "fb-correct", "fb-wrong");
            fb.innerHTML = "";
        });
    });
</script>
</body>
</html>
