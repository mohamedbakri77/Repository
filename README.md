<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Black Hat</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: black;
            overflow: hidden;
            position: relative;
            flex-direction: column; /* تنظيم العناصر عمودياً */
        }

        h1 {
            font-size: 5rem;
            font-family: Arial, sans-serif;
            position: relative;
            z-index: 10;
            display: inline-block;
            margin-top: 20px; /* مسافة فوق الكلمة */
        }

        .black {
            color: white;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
            transform: skew(-10deg);
        }

        .hat {
            color: red;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
            transform: skew(10deg);
            cursor: pointer; /* تغيير المؤشر إلى يد */
        }

        /* إضافة صورة */
        .background-image {
            position: absolute;
            top: 10%; /* موقع الصورة */
            left: 50%; /* مركز الصورة */
            transform: translateX(-50%); /* لتوسيط الصورة */
            width: 80%; /* عرض الصورة */
            height: auto; /* الحفاظ على نسبة العرض إلى الارتفاع */
            z-index: 5;
            opacity: 0.8; /* شفافية الصورة */
        }

        /* عنوان أسفل الكلمة الرئيسية */
        .subtitle {
            color: red;
            font-size: 2rem;
            margin-top: 20px; /* مسافة فوق العنوان */
            text-align: center;
            z-index: 10; /* فوق الصورة */
        }

        /* أيقونات الشبكات الاجتماعية */
        .social-icons {
            margin-top: 30px; /* مسافة فوق الأيقونات */
            display: flex; /* استخدام flex لترتيب الأيقونات */
            gap: 20px; /* المسافة بين الأيقونات */
            justify-content: center; /* توسيط الأيقونات */
        }

        .icon {
            font-size: 3rem; /* حجم الأيقونات */
            transition: transform 0.3s, filter 0.3s; /* تأثير التحريك */
            cursor: pointer; /* تغيير المؤشر إلى يد */
        }

        /* ألوان الأيقونات */
        .facebook {
            color: #3b5998; /* أزرق */
        }

        .youtube {
            color: #FF0000; /* أحمر */
        }

        .twitter {
            color: #1DA1F2; /* أزرق فاتح */
        }

        .tiktok {
            color: #69C9EF; /* لون تيك توك */
        }

        /* تأثير الضغط على الأيقونات */
        .icon:active {
            transform: scale(0.9); /* تصغير الأيقونة عند الضغط */
            filter: brightness(0.8); /* تقليل السطوع */
        }

        /* حقوق النشر */
        .rights {
            margin-top: 20px; /* مسافة فوق حقوق النشر */
            color: white;
            font-size: 1.2rem;
            text-align: center;
            z-index: 10; /* فوق الصورة */
        }

        /* نص فوق الصفحة */
        .warning {
            color: red;
            font-size: 3rem;
            position: absolute;
            top: 20px; /* المسافة من الأعلى */
            text-align: center;
            z-index: 15; /* فوق كل شيء */
        }

        /* أسماء الأيقونات */
        .icon-names {
            color: white;
            text-align: center;
            margin-top: 10px; /* مسافة فوق أسماء الأيقونات */
            font-size: 1rem;
            z-index: 10; /* فوق الصورة */
        }
    </style>
</head>
<body>
    <!-- النص العلوي -->
    <div class="warning">ماذا تريد من دخول هذا الموقع؟!!!!</div>

    <h1>
        <span class="black">Black</span> 
        <span class="hat" id="blackHat">Hat</span>
    </h1>

    <!-- الصورة -->
    <img src="https://i.postimg.cc/ryWTbkHb/pexels-frank-k-895836-1851243.jpg" alt="Background" class="background-image">

    <div class="social-icons">
        <a href="https://www.facebook.com" target="_blank">
            <i class="fab fa-facebook icon facebook"></i>
        </a>
        <a href="https://www.youtube.com" target="_blank">
            <i class="fab fa-youtube icon youtube"></i>
        </a>
        <a href="https://www.tiktok.com" target="_blank">
            <i class="fab fa-tiktok icon tiktok"></i>
        </a>
        <a href="https://www.twitter.com" target="_blank">
            <i class="fab fa-twitter icon twitter"></i>
        </a>
    </div>

    <!-- أسماء الأيقونات -->
    <div class="icon-names">
        <span>فيسبوك</span> | 
        <span>يوتيوب</span> | 
        <span>تيك توك</span> | 
        <span>تويتر</span>
    </div>

    <!-- حقوق النشر -->
    <div class="rights">حقوق Hamo Aldoli النشر والطباعه والبرامجة</div>

    <script>
        // إظهار رسالة عند النقر على كلمة "Hat"
        const blackHat = document.getElementById('blackHat');
        blackHat.addEventListener('click', function() {
            alert('لقد ضغطت على كلمة Hat!');
        });
    </script>
</body>
</html>
