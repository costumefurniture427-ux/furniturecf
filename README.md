<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>كتالوج المفروشات | Custom Furniture</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; text-align: center; background-color: #f3f4f6; padding: 0; margin: 0; color: #1f2937; }
        header { background: linear-gradient(135deg, #0f172a, #1e293b); color: white; padding: 25px 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
        .top-bar { display: flex; justify-content: space-between; align-items: center; max-width: 1200px; margin: 0 auto 15px auto; flex-wrap: wrap; gap: 15px; }
        .logo-area { display: flex; align-items: center; gap: 12px; }
        .logo-circle { background: white; color: #0f172a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: bold; font-size: 20px; box-shadow: 0 2px 8px rgba(0,0,0,0.2); }
        .cart-box { background: rgba(255,255,255,0.1); padding: 10px 18px; border-radius: 30px; font-size: 14px; border: 1px solid rgba(255,255,255,0.2); display: flex; align-items: center; gap: 8px; }
        nav { display: flex; justify-content: center; gap: 25px; background: rgba(255,255,255,0.05); padding: 12px; border-radius: 12px; margin-top: 15px; flex-wrap: wrap; }
        nav a { color: #e2e8f0; text-decoration: none; font-weight: 600; font-size: 15px; transition: 0.3s; }
        nav a:hover { color: #38bdf8; }
        .search-container { margin: 25px auto; max-width: 600px; padding: 0 20px; }
        .search-box { width: 100%; padding: 14px 20px; border-radius: 30px; border: 1px solid #cbd5e1; font-size: 15px; outline: none; box-shadow: 0 2px 6px rgba(0,0,0,0.05); }
        .container { max-width: 1100px; margin: 30px auto; padding: 0 20px; display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; }
        .card { background: white; border-radius: 16px; overflow: hidden; box-shadow: 0 4px 12px rgba(0,0,0,0.06); transition: transform 0.3s ease; text-align: right; }
        .card:hover { transform: translateY(-5px); }
        .card img { width: 100%; height: 220px; object-fit: cover; }
        .card-content { padding: 20px; }
        .card h3 { margin: 0 0 8px 0; font-size: 18px; color: #0f172a; }
        .card p { color: #64748b; font-size: 14px; margin: 0 0 15px 0; }
        .btn { display: block; width: 100%; background: #0f172a; color: white; border: none; padding: 12px; border-radius: 8px; font-weight: bold; cursor: pointer; text-align: center; text-decoration: none; transition: 0.3s; }
        .btn:hover { background: #1e293b; }
    </style>
</head>
<body>

    <header>
        <div class="top-bar">
            <div class="logo-area">
                <div class="logo-circle">CF</div>
                <div style="text-align: right;">
                    <h1 style="margin:0; font-size:20px;">Custom Furniture</h1>
                    <span style="font-size:11px; color:#94a3b8;">PREMIUM FURNITURE CATALOG</span>
                </div>
            </div>
            <div class="cart-box">
                🛒 <span>عربة التسوق (Cart):</span> <strong id="cart-count">0</strong>
            </div>
        </div>
        <p style="margin: 10px 0 0 0; font-size: 14px; color: #cbd5e1;">اختر التصميم والأثاث الراقي المناسب لمنزلك واطلبه مباشرة</p>
        
        <nav>
            <a href="#">الرئيسية (Home)</a>
            <a href="#">المنتجات (Products)</a>
            <a href="#">تواصل معنا (Contact Us)</a>
        </nav>
    </header>

    <div class="search-container">
        <input type="text" class="search-box" placeholder="ابحث عما تريده (كنب، غرف نوم، ستائر، تي في يونت، ورق جدران...)">
    </div>

    <div class="container">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=600&q=80" alt="كنب مدرن">
            <div class="card-content">
                <h3>طقم كنب مدرن</h3>
                <p>تفصيل حسب المقاس والقماش المفضل لديك</p>
                <button class="btn" onclick="alert('تمت الإضافة إلى السلة بنجاح!')">اطلب الآن</button>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1540518614846-7ede433c4ef0?auto=format&fit=crop&w=600&q=80" alt="غرفة نوم">
            <div class="card-content">
                <h3>غرفة نوم راقية</h3>
                <p>تصاميم عصرية تناسب كافة المساحات</p>
                <button class="btn" onclick="alert('تمت الإضافة إلى السلة بنجاح!')">اطلب الآن</button>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1595428774223-ef52624120d2?auto=format&fit=crop&w=600&q=80" alt="طاولة طعام">
            <div class="card-content">
                <h3>طاولة طعام فاخرة</h3>
                <p>خشب طبيعي بتصميم أنيق ومقاوم</p>
                <button class="btn" onclick="alert('تمت الإضافة إلى السلة بنجاح!')">اطلب الآن</button>
            </div>
        </div>
    </div>

</body>
</html>
