<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GMMJ PLANS</title>
  <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --silver-color: #00796b;
      --gold-color: #ff9800;
      --plus-color: #4527a0;
      --text-color: #333;
      --light-gray: #f5f5f5;
      --border-radius: 12px;
    }
    
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    
    body {
      font-family: "Tajawal", sans-serif;
      background: #f9f9f9;
      margin: 0;
      padding: 1rem;
      direction: rtl;
      color: var(--text-color);
      line-height: 1.6;
    }
    
    .page-title {
      text-align: center;
      margin: 0.5rem 0;
      font-size: 1.2rem;
      color: #555;
      font-weight: 500;
    }
    
    h1 {
      text-align: center;
      margin: 1.5rem 0;
      font-size: 1.8rem;
      color: var(--text-color);
      position: relative;
    }
    
    h1::after {
      content: "";
      display: block;
      width: 100px;
      height: 3px;
      background: linear-gradient(to right, var(--silver-color), var(--gold-color), var(--plus-color));
      margin: 0.5rem auto;
      border-radius: 3px;
    }
    
    .plans-container {
      max-width: 1200px;
      margin: 2rem auto;
      padding: 0 1rem;
    }

    .plans {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      flex-wrap: wrap;
    }

    .plan {
      background: white;
      border-radius: var(--border-radius);
      padding: 0;
      width: 100%;
      max-width: 360px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: all 0.3s ease;
      margin-bottom: 1.5rem;
      position: relative;
      border: 1px solid #eee;
    }

    .plan:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0,0,0,0.15);
    }

    .plan-header {
      color: white;
      padding: 1.5rem;
      text-align: center;
      position: relative;
    }

    .silver {
      background: linear-gradient(135deg, #b2dfdb, #00796b);
    }

    .gold {
      background: linear-gradient(135deg, #ffb74d, #ff9800);
    }

    .plus {
      background: linear-gradient(135deg, #b39ddb, #4527a0);
    }

    .plan-header h3 {
      margin: 0;
      font-size: 1.5rem;
      font-weight: 700;
    }

    .audience {
      font-size: 0.9rem;
      margin: 0.8rem auto;
      opacity: 0.9;
      padding: 0.5rem;
      border-radius: 20px;
      max-width: 90%;
      font-weight: 500;
      background-color: rgba(255,255,255,0.2);
    }

    .price {
      font-size: 2rem;
      margin: 1rem 0;
      text-align: center;
      font-weight: 700;
    }

    .price small {
      font-size: 1rem;
      display: block;
      margin-top: 0.3rem;
    }

    .original-price {
      text-decoration: line-through;
      color: #f44336;
      font-size: 1.2rem;
      margin-left: 0.5rem;
    }

    .features {
      list-style: none;
      padding: 1.5rem;
    }

    .features li {
      margin-bottom: 0.8rem;
      padding-right: 1rem;
      position: relative;
    }

    .features li::before {
      content: "•";
      color: var(--silver-color);
      position: absolute;
      right: 0;
    }

    .plan-gold .features li::before {
      color: var(--gold-color);
    }

    .plan-plus .features li::before {
      color: var(--plus-color);
    }

    .features li.not {
      opacity: 0.6;
      text-decoration: line-through;
    }

    .features li.not::before {
      content: "✕";
      color: #f44336;
    }

    .btn {
      display: block;
      margin: 1.5rem auto;
      color: white;
      text-align: center;
      padding: 0.8rem;
      border: none;
      border-radius: var(--border-radius);
      cursor: pointer;
      text-decoration: none;
      width: 85%;
      font-weight: 700;
      font-size: 1rem;
      transition: all 0.3s;
      position: relative;
      overflow: hidden;
    }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }

    .btn-silver {
      background: var(--silver-color);
    }

    .btn-gold {
      background: white;
      color: var(--gold-color);
    }

    .btn-plus {
      background: var(--plus-color);
    }

    .badge {
      position: absolute;
      top: 15px;
      left: -30px;
      background: #e65100;
      color: white;
      padding: 0.4rem 2rem;
      border-radius: 8px;
      font-size: 0.8rem;
      font-weight: bold;
      transform: rotate(-45deg);
      width: 120px;
      text-align: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }

    .popular-plan {
      transform: scale(1.01);
      margin-top: -10px;
      border: 2px solid var(--gold-color);
      position: relative;
    }

    .features-section {
      margin-top: 1rem;
      border-top: 1px dashed #eee;
      padding-top: 1rem;
    }

    .features-section h4 {
      color: #555;
      margin-bottom: 0.8rem;
      font-size: 1.1rem;
      padding-right: 1rem;
      border-right: 3px solid var(--silver-color);
    }

    .plan-gold .features-section h4 {
      border-right-color: var(--gold-color);
    }

    .plan-plus .features-section h4 {
      border-right-color: var(--plus-color);
    }

    .badge-discount {
      display: inline-block;
      background-color: #00c853;
      color: #fff;
      padding: 6px 14px;
      border-radius: 30px;
      font-size: 14px;
      font-weight: bold;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      position: absolute;
      right: 1rem;
      top: 47.55rem !important;
      z-index: 2;
      transform: rotate(5deg);
    }

    .badge-discount .icon {
      background-color: #fff;
      color: #00c853;
      padding: 2px 6px;
      border-radius: 50%;
      font-weight: bold;
      margin-right: 5px;
      display: inline-block;
    }

    .testimonials {
      background-color: #f5f5f5;
      padding: 0.5rem;
      border-radius: var(--border-radius);
      margin-top: 1rem;
      font-size: 0.9rem;
      border-right: 3px solid var(--gold-color);
    }

    .testimonials q {
      font-style: italic;
      display: block;
      margin-bottom: 0.5rem;
    }

    .testimonials .author {
      font-weight: bold;
      text-align: left;
    }

    .urgency-banner {
      background-color: #fff8e1;
      padding: 0.8rem;
      text-align: center;
      border-radius: var(--border-radius);
      margin: 1rem 0;
      border: 1px dashed #ffb300;
      font-size: 0.9rem;
    }

    .guarantee-badge {
      background-color: #e8f5e9;
      color: var(--silver-color);
      padding: 0.5rem;
      border-radius: var(--border-radius);
      text-align: center;
      margin-top: 1rem;
      font-size: 0.9rem;
      border: 1px solid #c8e6c9;
    }

    .lucide-lucide-undo-icon-lucide-undo{
     color: #00c853;
     margin-top: 45.6rem;
     margin-right: 7rem !important;
     position: absolute;
     transform: rotate(-50deg);
     z-index: 999;  
    }

    footer {
  width: 100%;
  text-align: center;
  font-size: 13px;
  color: #666;
  padding: 15px;
  margin-top: 40px;
  background-color: rgba(255, 255, 255, 0.5); /* شفافية خفيفة */
  border-top: 1px dashed #ccc; /* مثل خط الفاتورة */
  font-family: 'Courier New', monospace; /* تعطي إحساس الفاتورة */
}

    /* Responsive Adjustments */
    @media (max-width: 1024px) {
      .plans {
        gap: 1.2rem;
      }
      
      .plan {
        max-width: 320px;
      }
      
      .popular-plan {
        transform: none;
        margin-top: 0;
      }
    }

    @media (max-width: 768px) {
      .plans {
        gap: 1rem;
      }
      
      .plan {
        max-width: 100%;
      }
      
      .popular-plan {
        order: -1;
      }
      
      .badge-discount {
        right: 0.5rem;
        top: 0.5rem;
      }
    }

    @media (max-width: 480px) {
      body {
        padding: 0.5rem;
      }
      
      .page-title {
        font-size: 1rem;
      }
      
      h1 {
        font-size: 1.5rem;
        margin: 1rem 0;
      }
      
      .plan-header h3 {
        font-size: 1.3rem;
      }
      
      .price {
        font-size: 1.8rem;
      }
      
      .badge {
        font-size: 0.7rem;
        left: -35px;
        width: 110px;
      }
    }
  </style>
</head>
<body>
  <h1>اختر الباقة التي تناسبك</h1>

  <div class="urgency-banner">
    ⏳ نستقبل 5 متاجر بس كل شهر… لا تفوّت دورك!
  </div>

  <div class="plans-container">
    <div class="plans">
      <!-- Silver Plan -->
      <div class="plan plan-silver">
        <div class="plan-header silver">
          <h3>باقة جي بيسك</h3>
          <div class="audience audience-silver">أنسب خيار للانطلاق</div>
          <div class="price price-silver">49.99 <small>ر.س/شهري</small></div>
          <a href="#" class="btn btn-silver">أختر جي بيسك</a>
        </div>
        <ul class="features">
          <li>تصميم المنتجات والعروض</li>
          <li>متابعة العملاء والرد عليهم</li>
          <li>رفع حتى 15 منتج</li>
          <li>تحسين وصف المنتجات لزيادة المبيعات</li>
          <li class="not">هوية بصرية</li>      
          <li class="not">إدارة كاملة</li>
        </ul>

        <div class="features-section">
          <h4>تقارير وأداء</h4>
          <ul class="features">
            <li class="not">تقرير شهري عن أداء المتجر</li>
            <li class="not">تحليل بيانات العملاء</li>
          </ul>
        </div>

        <div class="features-section">
          <h4>تسويق</h4>
          <ul class="features">
            <li class="not">بنر اعلاني</li>
            <li class="not">أستراتيجيات تسويقية وافكار ذكية</li>
          </ul>
        </div>

        <div class="features-section">
          <h4>تحديثات موسمية</h4>
          <ul class="features">
            <li class="not">تحديث واجهة المتجر حسب المواسم</li>
            <li class="not">نرتب لك عروض المواسم بشكل تلقائي واحترافي</li>
          </ul>
        </div>

        <div class="guarantee-badge">
          ضمان استعادة الأموال خلال 7 أيام إذا لم تكن راضيًا
        </div>
      </div>

      <!-- Gold Plan (Popular) -->
      <div class="plan plan-gold popular-plan">
        <div class="badge">الأكثر طلباً</div>
        <div class="badge-discount">
          <span class="icon">🔥</span> كل شيء علينا… وأنت بس راقب الأرباح
        </div>
          <svg xmlns="http://www.w3.org/2000/svg" width="35" height="35" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide-lucide-undo-icon-lucide-undo"><path d="M3 7v6h6"/><path d="M21 17a9 9 0 0 0-9-9 9 9 0 0 0-6 2.3L3 13"/></svg>

        <div class="plan-header gold">
          <h3>باقة جي برو</h3>
          <div class="audience audience-gold">مثالية لكل من يريد يرتب متجره ويزيد مبيعاته</div>
          <div class="price price-gold">
            189 ر.س 
            <small>ر.س/شهري</small>
            <span class="original-price">249 ر.س</span>
          </div>
          <a href="#" class="btn btn-gold">أختر جي برو</a>
        </div>

        <div class="testimonials">
          <q>يعجبني تفكيره في انجاح المتجر ويهتم في المتجر وكأنه متجره حرفيًا ويعجبني حماسه وشغفه ويشتغل على المتجر من الصفر </q>
          <div class="author"> سلاشي -</div>
        </div>

        <ul class="features">
          <li>تصميم المنتجات والعروض</li>
          <li>متابعة العملاء والرد معهم</li>
          <li>رفع حتى 50 منتج</li>
          <li>تحسين وصف المنتجات لزيادة المبيعات</li>
          <li>هوية بصرية</li>
          <li>إدارة كاملة</li>
        </ul>

        <div class="features-section">
          <h4>تقارير وأداء</h4>
          <ul class="features">
            <li>تقرير شهري عن أداء المتجر</li>
            <li>تحليل بيانات العملاء</li>
          </ul>
        </div>

        <div class="features-section">
          <h4>تسويق</h4>
          <ul class="features">
            <li>تصميم 3 بنرات اعلانية</li>
            <li>أستراتيجيات تسويقية وافكار ذكية ( برو )</li>
          </ul>
        </div>

        <div class="features-section">
          <h4>تحديثات موسمية</h4>
          <ul class="features">
            <li>تحديث واجهة المتجر حسب المواسم</li>
            <li>نرتب لك عروض المواسم بشكل تلقائي واحترافي</li>
          </ul>
        </div>

        <div class="guarantee-badge" style="background-color: #fff3e0; border-color: #ffe0b2; color: #e65100;">
          ⭐ يُنصح بهِ لأصحاب المتاجر الناجحة
        </div>
      </div>

      <!-- Plus Plan -->
      <div class="plan plan-plus">
        <div class="plan-header plus">
          <h3>باقة جي بلس</h3>
          <div class="audience audience-plus">باقة تريحك… وتضبط شغلك</div>
          <div class="price price-plus">
            89.99 ر.س
            <small>ر.س/شهري</small>
          </div>
          <a href="#" class="btn btn-plus">أختر جي بلس</a>
        </div>
        <ul class="features">
          <li>تصميم المنتجات والعروض</li>
          <li>متابعة العملاء والرد عليهم</li>
          <li>رفع حتى 30 منتج</li>
          <li>تحسين وصف المنتجات لزيادة المبيعات</li>
          <li>هوية بصرية</li>
          <li class="not">إدارة كاملة</li>
        </ul>

        <div class="features-section">
          <h4>تقارير وأداء</h4>
          <ul class="features">
            <li class="not">تقرير شهري عن أداء المتجر</li>
            <li class="not">تحليل بيانات العملاء </li>
          </ul>
        </div>

        <div class="features-section">
          <h4>تسويق</h4>
          <ul class="features">
            <li>تصميم بنر اعلاني واحد</li>
            <li> أستراتيجيات تسويقية وافكار ذكية</li>
          </ul>
        </div>

        <div class="features-section">
          <h4>تحديثات موسمية</h4>
          <ul class="features">
            <li class="not">تحديث واجهة المتجر حسب المواسم</li>
            <li class="not">نرتب لك عروض المواسم بشكل تلقائي واحترافي</li>
          </ul>
        </div>

        <div class="guarantee-badge">
          دعم فني على مدار الساعة
        </div>
      </div>
    </div>
  </div>

  <footer style="text-align:center; padding: 20px; font-size: 14px; color: #888;">
    © 2025 جميع الحقوق محفوظة – GMMJ DESIGN | تصميم وابتكار بإحساس
  </footer>
</body>
</html>
