<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أثاث إكسبريس | Custom Furniture</title>
    <style>
        * { box-sizing: border-box; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; text-align: center; background-color: #f3f4f6; padding: 0; margin: 0; color: #1f2937; }
        header { background: linear-gradient(135deg, #0f172a, #1e293b); color: white; padding: 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
        .top-bar { display: flex; justify-content: space-between; align-items: center; max-width: 1200px; margin: 0 auto; flex-wrap: wrap; gap: 10px; }
        .logo-area { display: flex; align-items: center; gap: 10px; text-align: right; }
        .logo-circle { background: white; color: #0f172a; width: 45px; height: 45px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: bold; font-size: 18px; }
        .cart-box { background: rgba(255,255,255,0.1); padding: 8px 15px; border-radius: 20px; font-size: 13px; border: 1px solid rgba(255,255,255,0.2); display: flex; align-items: center; gap: 5px; }
        
        .container { max-width: 1100px; margin: 20px auto; padding: 0 15px; display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 20px; }
        .card { background: white; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 10px rgba(0,0,0,0.05); text-align: right; display: flex; flex-direction: column; justify-content: space-between; }
        .card img { width: 100%; height: 180px; object-fit: cover; background-color: #e5e7eb; }
        .card-content { padding: 15px; }
        .card h3 { margin: 0 0 5px 0; font-size: 16px; color: #0f172a; }
        .card p { color: #64748b; font-size: 13px; margin: 0 0 10px 0; }
        .price { color: #d97706; font-weight: bold; font-size: 15px; margin-bottom: 12px; display: block; }
        .btn { display: block; width: 100%; background: #fbbf24; color: #0f172a; border: none; padding: 10px; border-radius: 8px; font-weight: bold; cursor: pointer; text-align: center; text-decoration: none; transition: 0.3s; }
        .btn:hover { background: #f59e0b; }
    </style>
</head>
<body>

    <header>
        <div class="top-bar">
            <div class="logo-area">
                <div class="logo-circle">CF</div>
                <div>
                    <h1 style="margin:0; font-size:18px;">أثاث إكسبريس</h1>
                    <span style="font-size:10px; color:#94a3b8;">تصميم مخصص حسب الطلب</span>
                </div>
            </div>
            <div class="cart-box">
                🛒 <span>السلة:</span> <strong id="cart-count">0</strong>
            </div>
        </div>
    </header>

    <div class="container">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=500&q=80" alt="كنب مدرن">
            <div class="card-content">
                <h3>طقم كنب مدرن فاخر</h3>
                <p>تفصيل حسب المقاس والقماش المفضل لديك</p>
                <span class="price">1,499 د.إ</span>
                <button class="btn" onclick="alert('تمت الإضافة إلى السلة!')">إضافة إلى السلة</button>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1540518614846-7ede433c4ef0?auto=format&fit=crop&w=500&q=80" alt="غرفة نوم">
            <div class="card-content">
                <h3>غرفة نوم راقية متكاملة</h3>
                <p>تصاميم عصرية تناسب كافة المساحات</p>
                <span class="price">4,299 د.إ</span>
                <button class="btn" onclick="alert('تمت الإضافة إلى السلة!')">إضافة إلى السلة</button>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1595428774223-ef52624120d2?auto=format&fit=crop&w=500&q=80" alt="طاولة طعام">
            <div class="card-content">
                <h3>طاولة طعام فاخرة مع كراسي</h3>
                <p>خشب طبيعي بتصميم أنيق ومقاوم</p>
                <span class="price">2,399 د.إ</span>
                <button class="btn" onclick="alert('تمت الإضافة إلى السلة!')">إضافة إلى السلة</button>
            </div>
        </div>
    </div>

</body>
</html>
