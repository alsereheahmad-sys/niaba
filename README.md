# niaba<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نيابة غرب الأمانة الابتدائية</title>
<style>
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        background: linear-gradient(to bottom, #f0f4f8, #d9e4ec);
        color: #222;
    }
    header {
        background-color: #003366;
        color: white;
        padding: 15px;
        text-align: center;
        position: relative;
    }
    header img {
        position: absolute;
        top: 10px;
        right: 15px;
        height: 60px;
    }
    h1, h2 {
        margin: 10px 0;
    }
    nav {
        background-color: #0055aa;
        padding: 10px;
        text-align: center;
    }
    nav a {
        color: white;
        margin: 0 15px;
        text-decoration: none;
        font-weight: bold;
    }
    nav a:hover {
        text-decoration: underline;
    }
    section {
        padding: 20px;
        background: white;
        margin: 15px auto;
        border-radius: 10px;
        max-width: 900px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
    label {
        display: block;
        margin-top: 10px;
        font-weight: bold;
    }
    input, textarea, select {
        width: 100%;
        padding: 8px;
        margin-top: 5px;
        border-radius: 5px;
        border: 1px solid #ccc;
    }
    button {
        margin-top: 10px;
        padding: 10px 15px;
        background-color: #0055aa;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }
    button:hover {
        background-color: #003f7f;
    }
    .footer {
        background-color: #003366;
        color: white;
        padding: 15px;
        text-align: center;
        margin-top: 20px;
    }
    #barcode {
        display: block;
        margin: 20px auto;
    }
</style>
<script src="https://cdn.jsdelivr.net/npm/jsbarcode@3.11.5/dist/JsBarcode.all.min.js"></script>
</head>
<body>

<header>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9c/Emblem_of_Yemen.svg/1200px-Emblem_of_Yemen.svg.png" alt="شعار الجمهورية">
    <h1>الجمهورية اليمنية</h1>
    <h2>النيابة العامة - نيابة إستئناف الشمال</h2>
    <h3>نيابة غرب الأمانة الإبتدائية</h3>
</header>

<nav>
    <a href="#welcome">الرئيسية</a>
    <a href="#complaint">تقديم شكوى</a>
    <a href="#tracking">الاستعلام</a>
    <a href="#info">المعلومات</a>
</nav>

<section id="welcome">
    <h2>كلمة ترحيبية</h2>
    <p>نرحب بكم في بوابة نيابة غرب الأمانة الابتدائية الإلكترونية، حيث نضع العدالة بين يديكم، ونقرب الخدمات القانونية إليكم بكل شفافية وسهولة.</p>
    <p>نسعى لتقريب العدالة وتسهيل خدمات النيابة لكم.</p>
    <p>بوابتكم للعدالة والشفافية، هنا حيث يصبح الحق في متناول الجميع.</p>
</section>

<section id="complaint">
    <h2>تقديم الشكوى الإلكترونية</h2>
    <form action="mailto:Prosecutionwest@gmail.com" method="post" enctype="text/plain">
        <label>الاسم الكامل:</label>
        <input type="text" name="name" required>
        <label>رقم الهاتف:</label>
        <input type="tel" name="phone" required>
        <label>نص الشكوى:</label>
        <textarea name="complaint" rows="5" required></textarea>
        <label>إرفاق ملف الشكوى (PDF):</label>
        <input type="file" name="file" accept="application/pdf">
        <button type="submit">إرسال الشكوى</button>
    </form>
</section>

<section id="tracking">
    <h2>الاستعلام عن حركة ملف القضية</h2>
    <label>رقم القضية:</label>
    <input type="text">
    <label>السنة الهجرية:</label>
    <input type="text">
    <button>بحث</button>
</section>

<section>
    <h2>شروط قبول الشكوى الإلكترونية</h2>
    <ol>
        <li>أن تكون عن واقعة حصلت في نطاق اختصاص نيابة غرب الأمانة.</li>
        <li>أن تكون لمقدم الشكوى مصلحة قائمة يفرضها القانون.</li>
        <li>أن تكون لمقدم الشكوى صفة أو عن من يمثله قانونًا، وإرفاق ما يفيد ذلك.</li>
        <li>أن لا تكون بخصوص شكوى قد تم الفصل فيها بحكم أو قرار.</li>
        <li>أن تشمل اسم الشاكي والمشكو به، وبيانات الواقعة.</li>
        <li>أن تشمل موضوع الشكوى وأسانيدها القانونية وأدلتها.</li>
        <li>أن تقدم خلال المدة القانونية.</li>
        <li>إرفاق هوية مقدمها (بطاقة، جواز سفر...).</li>
        <li>أن تكون مطبوعة PDF وموقعة.</li>
    </ol>
</section>

<section id="barcode-section">
    <h2>رمز الباركود للموقع</h2>
    <svg id="barcode"></svg>
</section>

<section id="info">
    <h2>معلومات التواصل</h2>
    <p>العنوان: صنعاء، شارع الحرية</p>
    <p>أوقات الدوام: من الأحد إلى الأربعاء، 9 صباحًا - 2 ظهرًا</p>
    <p><a href="https://www.facebook.com/share/1ExkmPipt5/" target="_blank">صفحة الفيسبوك</a></p>
    <p><a href="https://wa.me/967778940199" target="_blank">واتساب: 778940199</a></p>
    <p>خريطة الموقع:</p>
    <iframe src="https://www.google.com/maps?q=15.3694,44.1910&hl=ar&z=15&output=embed" width="100%" height="300"></iframe>
</section>

<div class="footer">
    <p>© 2025 نيابة غرب الأمانة الابتدائية - جميع الحقوق محفوظة</p>
</div>

<script>
    // إنشاء الباركود بحيث يوجه للموقع نفسه
    JsBarcode("#barcode", window.location.href, {
        format: "CODE128",
        lineColor: "#000",
        width: 2,
        height: 50,
        displayValue: true
    });
</script>

</body>
</html>
