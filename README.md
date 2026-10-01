<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متجر الأثاث العصري الفاخر - تصميم مخصص حسب الطلب</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Cairo', sans-serif;
        }
        body {
            background-color: #EAEDED;
            color: #0F1111;
        }
        /* Amazon Style Header */
        header {
            background-color: #131921;
            color: white;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .nav-top {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 20px;
            gap: 15px;
        }
        .logo {
            font-size: 24px;
            font-weight: 900;
            color: #FF9900;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        .search-bar {
            flex: 1;
            display: flex;
            max-width: 700px;
            background: white;
            border-radius: 4px;
            overflow: hidden;
            border: 2px solid transparent;
            transition: border 0.2s;
        }
        .search-bar:focus-within {
            border-color: #FEBD69;
        }
        .search-select {
            background: #F3F3F3;
            border: none;
            padding: 0 10px;
            font-size: 13px;
            color: #555;
            cursor: pointer;
            border-left: 1px solid #ddd;
        }
        .search-input {
            flex: 1;
            padding: 10px 15px;
            border: none;
            font-size: 15px;
            outline: none;
        }
        .search-btn {
            background: #FEBD69;
            border: none;
            padding: 0 20px;
            font-size: 18px;
            cursor: pointer;
            color: #111;
            transition: background 0.2s;
        }
        .search-btn:hover {
            background: #F3A847;
        }
        .nav-tools {
            display: flex;
            align-items: center;
            gap: 20px;
        }
        .tool-item {
            color: white;
            text-decoration: none;
            font-size: 13px;
            display: flex;
            flex-direction: column;
        }
        .tool-item span.bold {
            font-weight: 700;
            font-size: 15px;
        }
        .cart-tool {
            display: flex;
            align-items: center;
            gap: 5px;
            font-weight: 700;
            font-size: 16px;
            color: white;
            text-decoration: none;
            position: relative;
        }
        .cart-badge {
            background: #FF9900;
            color: #111;
            border-radius: 50%;
            padding: 2px 6px;
            font-size: 12px;
            position: absolute;
            top: -8px;
            right: 12px;
            font-weight: 900;
        }

        /* Sub Navigation / Categories Bar */
        .nav-bottom {
            background-color: #232F3E;
            padding: 8px 20px;
            display: flex;
            gap: 20px;
            overflow-x: auto;
            white-space: nowrap;
        }
        .nav-bottom a {
            color: white;
            text-decoration: none;
            font-size: 14px;
            padding: 5px 10px;
            border-radius: 2px;
            border: 1px solid transparent;
        }
        .nav-bottom a:hover {
            border-color: white;
        }

        /* Hero Banner */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1618221195710-dd6b41faaea6?q=80&w=1600&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            height: 380px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 20px;
        }
        .hero-content h1 {
            font-size: 38px;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }
        .hero-content p {
            font-size: 18px;
            margin-bottom: 20px;
            text-shadow: 0 1px 2px rgba(0,0,0,0.5);
        }
        .hero-btn {
            background: #FF9900;
            color: #111;
            padding: 12px 30px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 700;
            font-size: 16px;
            transition: background 0.2s;
        }
        .hero-btn:hover {
            background: #F3A847;
        }

        /* Main Container */
        .container {
            max-width: 1400px;
            margin: -60px auto 30px auto;
            padding: 0 20px;
            position: relative;
            z-index: 10;
        }

        /* Sections Grid */
        .section-title {
            font-size: 24px;
            font-weight: 700;
            margin: 30px 0 15px 0;
            color: #0F1111;
        }
        .grid-products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
        }
        .product-card {
            background: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
            display: flex;
            flex-direction: column;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .product-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 6px 16px rgba(0,0,0,0.12);
        }
        .product-img-container {
            width: 100%;
            height: 220px;
            overflow: hidden;
            border-radius: 6px;
            margin-bottom: 15px;
            position: relative;
        }
        .product-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }
        .product-card:hover .product-img {
            transform: scale(1.05);
        }
        .badge-discount {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #CC0C39;
            color: white;
            padding: 4px 8px;
            font-size: 12px;
            font-weight: 700;
            border-radius: 4px;
        }
        .product-title {
            font-size: 16px;
            font-weight: 700;
            color: #0F1111;
            margin-bottom: 8px;
            line-height: 1.4;
            height: 44px;
            overflow: hidden;
        }
        .product-rating {
            display: flex;
            align-items: center;
            gap: 5px;
            color: #FFA41C;
            font-size: 13px;
            margin-bottom: 10px;
        }
        .product-rating span {
            color: #007185;
        }
        .product-price {
            display: flex;
            align-items: baseline;
            gap: 8px;
            margin-bottom: 15px;
        }
        .current-price {
            font-size: 22px;
            font-weight: 950;
            color: #B12704;
        }
        .old-price {
            font-size: 14px;
            color: #565959;
            text-decoration: line-through;
        }
        .add-to-cart-btn {
            background: #FFD814;
            border: 1px solid #FCD200;
            border-radius: 20px;
            padding: 10px;
            font-weight: 700;
            cursor: pointer;
            width: 100%;
            text-align: center;
            transition: background 0.2s;
        }
        .add-to-cart-btn:hover {
            background: #F7CA00;
        }

        /* Footer Style */
        footer {
            background-color: #232F3E;
            color: white;
            margin-top: 50px;
        }
        .footer-top {
            background-color: #37475A;
            text-align: center;
            padding: 15px;
            font-size: 14px;
            cursor: pointer;
        }
        .footer-top:hover {
            background-color: #485769;
        }
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 30px;
            padding: 40px 20px;
        }
        .footer-col h3 {
            font-size: 16px;
            margin-bottom: 15px;
            color: #FFF;
        }
        .footer-col ul {
            list-style: none;
        }
        .footer-col ul li {
            margin-bottom: 10px;
        }
        .footer-col ul li a {
            color: #DDD;
            text-decoration: none;
            font-size: 14px;
        }
        .footer-col ul li a:hover {
            text-decoration: underline;
        }
        .footer-bottom {
            background-color: #131921;
            text-align: center;
            padding: 20px;
            font-size: 13px;
            color: #999;
            border-top: 1px solid #3A4553;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="nav-top">
            <a href="#" class="logo">
                <i class="fa-solid fa-couch"></i> أثاث إكسبريس
            </a>
            <div class="search-bar">
                <select class="search-select">
                    <option>كل الأقسام</option>
                    <option>غرف المعيشة</option>
                    <option>غرف النوم</option>
                    <option>المكاتب</option>
                </select>
                <input type="text" class="search-input" placeholder="ابحث عن أثاث مخصص، طقم صالون، طاولات...">
                <button class="search-btn"><i class="fa-solid fa-search"></i></button>
            </div>
            <div class="nav-tools">
                <a href="#" class="tool-item">
                    <span>مرحباً بك، أحمد</span>
                    <span class="bold">الحساب والطلبات</span>
                </a>
                <a href="#" class="cart-tool">
                    <i class="fa-solid fa-cart-shopping fa-lg"></i>
                    <span>السلة</span>
                    <span class="cart-badge">3</span>
                </a>
            </div>
        </div>
        <div class="nav-bottom">
            <a href="#living">غرف المعيشة</a>
            <a href="#bedroom">غرف النوم الفاخرة</a>
            <a href="#office">أثاث المكاتب الذكية</a>
            <a href="#custom">تصميم مخصص حسب الطلب</a>
            <a href="#offers">عروض اليوم المميزة</a>
            <a href="#support">خدمة العملاء</a>
        </div>
    </header>

    <!-- Hero Banner -->
    <section class="hero">
        <div class="hero-content">
            <h1>أثاث عصري مخصص بجودة عالمية</h1>
            <p>صمم منزلك بأحدث تصاميم الأثاث الفاخر المصنوع حسب الطلب وبأعلى معايير المتانة.</p>
            <a href="#living" class="hero-btn">تسوق الأقسام الآن</a>
        </div>
    </section>

    <!-- Main Container -->
    <div class="container">

        <!-- Section 1: Living Room -->
        <h2 class="section-title" id="living">غرف المعيشة والصالونات الفاخرة</h2>
        <div class="grid-products">
            <div class="product-card">
                <div class="product-img-container">
                    <span class="badge-discount">-30%</span>
                    <img src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?q=80&w=800&auto=format&fit=crop" alt="كنبة زاوية عصرية" class="product-img">
                </div>
                <div class="product-title">طقم كنبة زاوية مودرن مخمل فاخر مع وسائد مريحة (تصميم مخصص)</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star-half-stroke"></i>
                    <span>1,428</span>
                </div>
                <div class="product-price">
                    <span class="current-price">٢,٤٩٩ د.إ</span>
                    <span class="old-price">٣,٥٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>

            <div class="product-card">
                <div class="product-img-container">
                    <span class="badge-discount">-20%</span>
                    <img src="https://images.unsplash.com/photo-1586023492125-27b2c045efd7?q=80&w=800&auto=format&fit=crop" alt="كرسي مفرد" class="product-img">
                </div>
                <div class="product-title">كرسي استرخاء مفرد (فوتيه) بتصميم اسكندنافي أنيق مع قاعدة خشبية</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-regular fa-star"></i>
                    <span>850</span>
                </div>
                <div class="product-price">
                    <span class="current-price">٧٩٩ د.إ</span>
                    <span class="old-price">٩٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>

            <div class="product-card">
                <div class="product-img-container">
                    <span class="badge-discount">-25%</span>
                    <img src="https://images.unsplash.com/photo-1533779283484-8ed494033b2d?q=80&w=800&auto=format&fit=crop" alt="طاولة قهوة" class="product-img">
                </div>
                <div class="product-title">طاولة قهوة مركزية خشب طبيعي بتصميم هندسي مع درج تخزين مخفي</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    <span>620</span>
                </div>
                <div class="product-price">
                    <span class="current-price">٥٩٩ د.إ</span>
                    <span class="old-price">٧٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>

            <div class="product-card">
                <div class="product-img-container">
                    <img src="https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?q=80&w=800&auto=format&fit=crop" alt="وحدة تلفزيون" class="product-img">
                </div>
                <div class="product-title">وحدة تلفزيون معلقة عصرية مع إضاءة LED خلفية وأرفف زجاجية</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star-half-stroke"></i>
                    <span>410</span>
                </div>
                <div class="product-price">
                    <span class="current-price">١,٢٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>
        </div>

        <!-- Section 2: Bedroom -->
        <h2 class="section-title" id="bedroom">غرف النوم وأطقم الأسرة الملكية</h2>
        <div class="grid-products">
            <div class="product-card">
                <div class="product-img-container">
                    <span class="badge-discount">-35%</span>
                    <img src="https://images.unsplash.com/photo-1540518614846-7ede433c4ef0?q=80&w=800&auto=format&fit=crop" alt="سرير مزدوج" class="product-img">
                </div>
                <div class="product-title">سرير مزدوج فاخر مقاس كينج مع ظهر مبطن بتصميم كابتونيه عصري</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    <span>2,100</span>
                </div>
                <div class="product-price">
                    <span class="current-price">٣,١٩٩ د.إ</span>
                    <span class="old-price">٤,٨٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>

            <div class="product-card">
                <div class="product-img-container">
                    <img src="https://images.unsplash.com/photo-1595526114035-0d45ed16cfbf?q=80&w=800&auto=format&fit=crop" alt="دولاب ملابس" class="product-img">
                </div>
                <div class="product-title">دولاب ملابس كبير بباب سحب زجاجي مع إضاءة داخلية وتصميم منظم</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-regular fa-star"></i>
                    <span>530</span>
                </div>
                <div class="product-price">
                    <span class="current-price">٤,٢٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>

            <div class="product-card">
                <div class="product-img-container">
                    <img src="https://images.unsplash.com/photo-1616046229478-9901c5536a45?q=80&w=800&auto=format&fit=crop" alt="طاولة تسريحة" class="product-img">
                </div>
                <div class="product-title">طاولة تسريحة مكياج مع مرآة مضيئة وكرسي مبطن فاخر</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star-half-stroke"></i>
                    <span>390</span>
                </div>
                <div class="product-price">
                    <span class="current-price">١,٤٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>

            <div class="product-card">
                <div class="product-img-container">
                    <span class="badge-discount">-15%</span>
                    <img src="https://images.unsplash.com/photo-1507652313519-d4e9174996dd?q=80&w=800&auto=format&fit=crop" alt="كومودينو" class="product-img">
                </div>
                <div class="product-title">طاولة خدمة جانبية (كومودينو) لغرفة النوم بدرجين بتصميم خشبي فخم</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    <span>480</span>
                </div>
                <div class="product-price">
                    <span class="current-price">٣٩٩ د.إ</span>
                    <span class="old-price">٤٧٠ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>
        </div>

        <!-- Section 3: Office Furniture -->
        <h2 class="section-title" id="office">أثاث المكاتب الذكية وغرف العمل</h2>
        <div class="grid-products">
            <div class="product-card">
                <div class="product-img-container">
                    <span class="badge-discount">-25%</span>
                    <img src="https://images.unsplash.com/photo-1518455027359-f3f8164ba6bd?q=80&w=800&auto=format&fit=crop" alt="مكتب عمل" class="product-img">
                </div>
                <div class="product-title">مكتب عمل تنفيذي حديث مع فتحات لتنظيم الأسلاك وسطح خشبي مقاوم للخدش</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star-half-stroke"></i>
                    <span>910</span>
                </div>
                <div class="product-price">
                    <span class="current-price">١,٨٩٩ د.إ</span>
                    <span class="old-price">٢,٤٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>

            <div class="product-card">
                <div class="product-img-container">
                    <img src="https://images.unsplash.com/photo-1580481077494-e3299ac25e94?q=80&w=800&auto=format&fit=crop" alt="كرسي مكتب" class="product-img">
                </div>
                <div class="product-title">كرسي مكتب إداري شبكي مريح مع دعم كامل للفقرات وارتفاع قابل للتعديل</div>
                <div class="product-rating">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    <span>1,230</span>
                </div>
                <div class="product-price">
                    <span class="current-price">٨٩٩ د.إ</span>
                </div>
                <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i> إضافة إلى السلة</button>
            </div>
        </div>

    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-top" onclick="window.scrollTo({top: 0, behavior: 'smooth'});">
            العودة إلى الأعلى
        </div>
        <div class="footer-content">
            <div class="footer-col">
                <h3>عرفنا أكثر</h3>
                <ul>
                    <li><a href="#">معلومات عن الشركة</a></li>
                    <li><a href="#">وظائف</a></li>
                    <li><a href="#">الاستدامة</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>تواصل معنا</h3>
                <ul>
                    <li><a href="#">خدمة العملاء</a></li>
                    <li><a href="#">تتبع الشحنات</a></li>
                    <li><a href="#">سياسة الإرجاع والاستبدال</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>حسابك</h3>
                <ul>
                    <li><a href="#">حسابك الشخصي</a></li>
                    <li><a href="#">سلة المشتريات</a></li>
                    <li><a href="#">المفضلة</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>تسوق بثقة</h3>
                <ul>
                    <li><a href="#">ضمان الجودة المصنعية</a></li>
                    <li><a href="#">الدفع الآمن عند الاستلام</a></li>
                    <li><a href="#">خدمة التركيب المجاني</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 متجر أثاث إكسبريس (تصميم مخصص حسب الطلب). جميع الحقوق محفوظة.</p>
        </div>
    </footer>

</body>
</html>
