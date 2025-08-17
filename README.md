<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>النيابة العامة - نيابة إستئناف شمال الأمانة</title>
<style>
body {
    font-family: Tahoma, sans-serif;
    margin:0;
    background:#f0f4fa;
}
header {
    background: linear-gradient(90deg,#003366,#0055aa);
    color:#fff;
    padding:50px 15px 15px 15px;
    text-align:center;
    position: relative;
}
header img {
    position: absolute;
    top:10px;
    left:10px;
    width:80px;
    opacity:0.3;
}
marquee {
    background:#0077cc;
    color:#fff;
    padding:8px;
    font-weight:bold;
}
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
.links {display:flex;justify-content:space-around;margin:15px 0;}
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
}
.links a:hover {background:#003366;}
.barcode{text-align:center;margin-top:20px;}
.barcode img{width:120px;height:120px;}
#savedMsg{color:green;font-weight:bold;margin-top:10px;}
footer {
    background:#003366;
    color:white;
    padding:20px;
    text-align:center;
    font-size:14px;
}
footer p{margin:5px;}
</style>
</head>
<body>

<header>
<img src="https://i.imgur.com/3X9MsdY.png" alt="شعار النيابة">
<h1>النيابة العامة</h1>
<h3>نيابة إستئناف شمال الأمانة</h3>
<h4>نيابة غرب الأمانة الإبتدائية</h4>
</header>

<marquee>مرحبا بكم في موقع نيابة غرب الأمانة الإبتدائية</marquee>

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
        <input type="text" id="name" required>
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
        <input type="tel" id="phone" required>
    </div>
    <div class="field">
        <label>السنة الهجرية:</label>
        <input type="text" id="year" required>
    </div>
    <div class="field">
        <label>موضوع الشكوى:</label>
        <textarea id="subject" rows="4" required></textarea>
    </div>
    <div class="field">
        <label>البريد الإلكتروني:</label>
        <input type="email" id="email" required>
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
