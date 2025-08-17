<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>النيابة العامة - نيابة إستئناف شمال الأمانة</title>
<style>
/* الخط العربي العصري */
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;700&display=swap');

/* الخطوط الأساسية */
body {
    font-family: 'Cairo', Tahoma, Geneva, Verdana, sans-serif;
    margin:0;
    background:#f0f4fa;
}

/* رأس الصفحة ثابت */
header {
    background: linear-gradient(135deg,#003366,#0055aa);
    color:#fff;
    padding:30px 20px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    width:100vw;
    box-sizing:border-box;
    position: sticky;
    top: 0;
    z-index: 1000;
    flex-wrap: wrap;
}

.header-container {
    display:flex;
    align-items:center;
    gap:20px;
    text-align:center;
    flex-wrap: wrap;
}

header .logo {
    width:80px;
    opacity:0.3;
}

.header-text h1 {
    font-size:1.8em;
    margin:0;
    font-weight:bold;
}

.header-text h2 {
    font-size:1.3em;
    margin:3px 0;
    font-weight:500;
    color:#fff; /* اجعل النص أبيض */
}

.header-text h3 {
    font-size:1.1em;
    margin:3px 0;
    font-weight:400;
}

.header-text .address {
    font-size:0.95em;
    margin-top:5px;
    font-weight:300;
    opacity:0.8;
}

/* أيقونات التواصل السريعة */
.quick-links {
    display:flex;
    gap:10px;
    align-items:center;
}
.quick-links a {
    display:block;
    width:40px;
    height:40px;
    border-radius:50%;
    background:#fff;
    text-align:center;
    line-height:40px;
    font-size:20px;
    color:#003366;
    text-decoration:none;
    transition: all 0.3s;
}
.quick-links a:hover {
    background:#0077cc;
    color:#fff;
}

/* شريط الترحيب */
.marquee {
  overflow: hidden;
  white-space: nowrap;
  box-sizing: border-box;
  background:#0077cc;
  color:#fff;
}

.marquee p {
  display: inline-block;
  padding-left: 100%;
  animation: marquee 15s linear infinite;
  font-weight:bold;
  font-size:1em;
  padding:10px 0;
}

@keyframes marquee {
  0% { transform: translateX(0%); }
  100% { transform: translateX(-100%); }
}

/* الأقسام */
.section {
    background:#fff;
    margin:20px;
    padding:20px;
    border-radius:12px;
    box-shadow:0 4px 6px rgba(0,0,0,0.1);
}

h2 {color:#003366;}
.field {margin-bottom:15px;}
label {display:block;margin-bottom:5px;color:#003366;font-weight:bold;}
input, select, textarea, button {
    width:100%;
    padding:10px;
    border-radius:12px;
    border:1px solid #aaa;
    box-sizing:border-box;
    background:linear-gradient(135deg,#cce0ff,#e6f0ff);
}
button {
    background: linear-gradient(90deg,#003366,#0077cc);
    color:#fff;
    border:none;
    cursor:pointer;
    font-weight:bold;
}
button:hover {background: linear-gradient(90deg,#0055aa,#0099ff);}

.links {display:flex;justify-content:space-around;margin:15px 0;flex-wrap:wrap;}
.links a {
    display:block;
    background:#0055aa;
    color:white;
    text-decoration:none;
    padding:10px;
    border-radius:8px;
    width:40%;
    text-align:center;
    font-weight:bold;
    margin:5px 0;
}
.links a:hover {background:#003366;}

.barcode{text-align:center;margin-top:20px;}
.barcode img{max-width:100%; height:auto;}

#savedMsg{color:green;font-weight:bold;margin-top:10px;}

/* الفوتر */
footer {
    background:#003366;
    color:white;
    padding:20px;
    text-align:center;
    font-size:14px;
}
footer p{margin:5px;}

/* Responsive */
@media (max-width:600px){
  .header-text h1 {font-size:1.5em;}
  .header-text h2 {font-size:1.2em;}
  .header-text h3 {font-size:1em;}
  .header-text .address {font-size:0.9em;}
  .links a {width:80%;}
  .quick-links {justify-content:center;}
}
</style>
<!-- أيقونات فونت ممتازة -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>

<header>
  <div class="header-container">
    <img src="https://i.imgur.com/3X9MsdY.png" alt="شعار النيابة" class="logo">
    <div class="header-text">
      <h1>النيابة العامة</h1>
      <h2>نيابة إستئناف شمال الأمانة</h2>
      <h3>نيابة غرب الأمانة الإبتدائية</h3>
      <p class="address">العنوان: صنعاء - شارع الحرية</p>
    </div>
  </div>
  <div class="quick-links">
    <a href="https://facebook.com" target="_blank"><i class="fab fa-facebook-f"></i></a>
    <a href="https://wa.me/967778940199" target="_blank"><i class="fab fa-whatsapp"></i></a>
  </div>
</header>

<div class="marquee">
  <p>مرحبا بكم في موقع نيابة غرب الأمانة الإبتدائية</p>
</div>

<div class="section">
<h2>التواصل</h2>
<div class="links">
    <a href="https://facebook.com" target="_blank">صفحتنا على فيسبوك</a>
    <a href="https://wa.me/967778940199" target="_blank">تواصل واتساب</a>
</div>
<div class="barcode">
    <p>رمز الباركود:</p>
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=120x120&data=https://facebook.com" alt="QR">
</div>
<p><b>البريد الرسمي:</b> <a href="mailto:info@west-niaba.com">info@west-niaba.com</a></p>
</div>

<div class="section">
<h2>شروط قبول الدعوى</h2>
<button onclick="alert('١- تقديم شكوى واضحة\\n٢- إرفاق المستندات\\n٣- ذكر السنة الهجرية\\n٤- ذكر بيانات الشاكي كاملة')">عرض الشروط</button>
</div>

<div class="section">
<h2>إرسال شكوى إلكترونياً</h2>
<form id="complaintForm">
    <div class="field">
        <label>الاسم:</label>
        <input type="text" id="name" placeholder="ادخل الاسم الكامل" required>
    </div>
    <div class="field">
        <label>الصفة:</label>
        <select id="role">
            <option value="شاكي">شاكي</option>
            <option value="مشكو به">مشكو به</option>
        </select>
    </div>
    <div class="field">
        <label>رقم الهاتف:</label>
        <input type="tel" id="phone" placeholder="ادخل رقم الهاتف" required>
    </div>
    <div class="field">
        <label>السنة الهجرية:</label>
        <input type="text" id="year" placeholder="ادخل السنة الهجرية" required>
    </div>
    <div class="field">
        <label>موضوع الشكوى:</label>
        <textarea id="subject" rows="4" placeholder="اكتب موضوع الشكوى" required></textarea>
    </div>
    <div class="field">
        <label>البريد الإلكتروني:</label>
        <input type="email" id="email" placeholder="ادخل البريد الإلكتروني" required>
    </div>
    <button type="submit">إرسال للبريد وحفظ</button>
</form>
<div id="savedMsg"></div>
</div>

<div class="section">
<h2>من نحن</h2>
<p>النيابة العامة - نيابة إستئناف شمال الأمانة - نيابة غرب الأمانة الإبتدائية<br>
البوابة الإعلامية - نظام سير الدعوة الجزائية لمكتب النائب العام - الدائرة الرقمية<br>
(تقريب العدالة للمواطنين)</p>
</div>

<div class="section">
<h2>تواصل بنا</h2>
<p>📧 البريد: <a href="mailto:info@west-niaba.com">info@west-niaba.com</a></p>
<p>💬 واتساب: <a href="https://wa.me/967778940199">اضغط هنا للتواصل</a></p>
</div>

<div class="section">
<h2>أوقات الدوام</h2>
<p>من السبت إلى الأربعاء: 8 صباحاً – 3 مساءً</p>
</div>

<footer>
<p>جميع الحقوق محفوظة &copy; نيابة غرب الأمانة الإبتدائية</p>
<p>تصميم وتنفيذ وإخراج م. أحمد السريحي</p>
</footer>

<script>
document.getElementById('complaintForm').addEventListener('submit', function(e){
    e.preventDefault();
    const data = {
        name: document.getElementById('name').value,
        role: document.getElementById('role').value,
        phone: document.getElementById('phone').value,
        year: document.getElementById('year').value,
        subject: document.getElementById('subject').value,
        email: document.getElementById('email').value,
        date: new Date().toLocaleString()
    };
    let all = JSON.parse(localStorage.getItem('complaints') || '[]');
    all.push(data);
    localStorage.setItem('complaints', JSON.stringify(all));
    document.getElementById('savedMsg').innerText = '✅ تم حفظ الشكوى وإرسالها بنجاح';
    const body = `الاسم: ${data.name}%0D%0Aالصفة: ${data.role}%0D%0Aرقم الهاتف: ${data.phone}%0D%0Aالسنة الهجرية: ${data.year}%0D%0Aالموضوع: ${data.subject}%0D%0Aالبريد: ${data.email}`;
    window.location.href = `mailto:info@west-niaba.com?subject=شكوى جديدة&body=${body}`;
    this.reset();
});
</script>

</body>
</html>
