<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>النيابة العامة - نيابة غرب الأمانة الإبتدائية</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;700&display=swap');

body {font-family:'Cairo', sans-serif;margin:0;min-height:100vh;background: linear-gradient(270deg, #00aaff, #0055aa, #00ffaa, #ff55aa, #ffaa00);background-size: 1000% 1000%;animation: gradientBG 30s ease infinite;color:#222;}
@keyframes gradientBG {0% { background-position:0% 50%; } 50% { background-position:100% 50%; } 100% { background-position:0% 50%; }}

header {background: rgba(0,0,0,0.5); color:#fff; padding:20px; display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; position: sticky; top:0; z-index:1000; box-shadow:0 0 20px rgba(0,0,0,0.5);}
header img {width:80px; opacity:0.95; cursor:pointer;}
.header-text {text-align:center; flex:1;}
.header-text h1 {margin:0;font-size:1.8em;font-weight:bold; text-shadow:0 0 10px #00f;}
.header-text h2 {margin:3px 0;font-size:1.3em;font-weight:500;color:white;}
.header-text h3 {margin:3px 0;font-size:1.1em;font-weight:400;}
.header-text .address {font-size:0.95em; opacity:0.8;}
.email-head {margin-top:5px; font-weight:bold; font-size:0.9em;}

nav {background:#003366; display:flex; justify-content:center; flex-wrap:wrap;}
nav a {color:white; text-decoration:none; padding:12px 20px; display:inline-block; transition:0.3s;}
nav a:hover {background:#0055aa; border-radius:10px;}

.marquee {overflow:hidden; white-space:nowrap; background:rgba(0,119,204,0.8); color:#fff;}
.marquee p {display:inline-block; padding-left:100%; animation: marquee 15s linear infinite; font-weight:bold; padding:10px 0;}
@keyframes marquee {0% { transform:translateX(0%); } 100% { transform:translateX(-100%); }}

.section {background: rgba(255,255,255,0.95); margin:20px; padding:20px; border-radius:20px; box-shadow:0 8px 20px rgba(0,0,0,0.3);}
h2 {color:#003366; margin-bottom:10px; text-shadow:0 0 5px #0055aa;}
button {padding:12px 25px; background: linear-gradient(90deg,#003366,#0077cc); color:white; border:none; border-radius:15px; cursor:pointer; margin-top:10px; transition:0.3s; font-weight:600;}
button:hover {background: linear-gradient(90deg,#0055aa,#0099ff); box-shadow:0 0 15px rgba(0,0,0,0.3); transform:translateY(-2px);}
input, textarea, select {padding:12px; margin:8px 0; border-radius:12px; border:1px solid #ccc; width:100%; font-size:16px; transition:0.3s; outline:none;}
input:focus, textarea:focus, select:focus {border-color:#3498db; box-shadow:0 0 8px rgba(52,152,219,0.3);}
.error-msg {color:red; font-size:13px; margin-top:-10px; margin-bottom:10px; display:none;}
.success-popup {display:none; position: fixed; top:50%; left:50%; transform: translate(-50%, -50%); background:#fff; border-radius:15px; box-shadow:0 0 25px rgba(0,0,0,0.5); padding:25px 40px; text-align:center; font-size:18px; z-index:9999; color:green;}
.success-popup button {margin-top:15px; background:green; border-radius:12px; padding:10px 20px;}
.icon-container {display:flex; justify-content:center; gap:20px; margin-top:10px;}
.icon-container a {display:flex; align-items:center; justify-content:center; width:50px; height:50px; border-radius:50%; background:#003366; color:white; font-size:20px; text-decoration:none; transition: all 0.5s; box-shadow:0 0 5px #003366;}
.icon-container a:hover {transform:scale(1.2); background:#0077cc; color:white;}
.qr-code {text-align:center; margin:20px 0;}
.qr-code img {width:120px; height:120px;}
footer {background: rgba(0,51,102,0.8); color:white; padding:15px; text-align:center; font-size:14px;}
footer p {margin:5px;}
.popup-overlay {display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.6); z-index:9998; justify-content:center; align-items:center;}
.popup-content {background:#fff; padding:20px 30px; border-radius:15px; text-align:center; max-width:400px; width:90%;}
.card {background:#f0f8ff; padding:10px; margin:10px; border-radius:15px; box-shadow:0 4px 10px rgba(0,0,0,0.2);}
@media(max-width:500px){ .section{padding:15px;} nav a{padding:10px 15px;} }
</style>
<script src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
<script>
(function(){emailjs.init("user_youractualuserid");})(); // ضع هنا User ID من EmailJS

function showSuccessPopup(msg){ document.getElementById('successPopup').querySelector('p').innerText=msg; document.getElementById('successPopup').style.display='block'; }
function closePopup(){document.getElementById('successPopup').style.display='none'; }
function validateForm(form){ let valid=true; [...form.querySelectorAll('input, select')].forEach(input=>{ if(input.hasAttribute('required') && !input.value){input.nextElementSibling.style.display='block'; valid=false;} else{ if(input.nextElementSibling) input.nextElementSibling.style.display='none'; } }); return valid; }

// تغيير الشعار وحفظه في LocalStorage
function changeLogo(input){ 
 if(input.files && input.files[0]){ 
   const reader = new FileReader(); 
   reader.onload = function(e){ 
     document.getElementById('logoImg').src=e.target.result; 
     localStorage.setItem('savedLogo', e.target.result); 
     input.style.display='none'; 
   } 
   reader.readAsDataURL(input.files[0]); 
 } 
}
// تحميل الشعار المحفوظ عند فتح الصفحة
window.addEventListener('DOMContentLoaded', ()=>{ 
 const savedLogo = localStorage.getItem('savedLogo'); 
 if(savedLogo){ document.getElementById('logoImg').src = savedLogo; } 
});

function sendEmailJS(formId,serviceID,templateID){ 
 const form = document.getElementById(formId); 
 form.addEventListener('submit', function(e){ 
   e.preventDefault(); 
   if(!validateForm(form)) return; 
   emailjs.sendForm(serviceID, templateID, form).then(()=>{ form.reset(); showSuccessPopup("✅ تم الإرسال بنجاح!"); }, (err)=>{alert("حدث خطأ: "+err);}); 
 }); 
}

function openFormsPopup(){ document.getElementById('formsPopup').style.display='flex'; }
function closeFormsPopup(){ document.getElementById('formsPopup').style.display='none'; }

function openWhatsAppQuery(){ document.getElementById('whatsappPopup').style.display='flex'; }
function sendWhatsAppQuery(){ 
  const select = document.getElementById('whatsappRole'); 
  const role = select.value; 
  const fileInput = document.getElementById('whatsappFile'); 
  if(!role){ alert("الرجاء اختيار الصفة!"); return; } 
  if(fileInput.files.length==0){ alert("الرجاء إرفاق ما يثبت الصفة!"); return; }
  let msg = `مرحبا، أريد الاستعلام عن القضية. صفة: ${role}`; 
  const phone = '967778940199'; 
  window.open(`https://wa.me/${phone}?text=${encodeURIComponent(msg)}`, '_blank'); 
  document.getElementById('whatsappPopup').style.display='none'; 
}

function openAbout(){ document.getElementById('aboutPopup').style.display='flex'; }
function closeAbout(){ document.getElementById('aboutPopup').style.display='none'; }
</script>
</head>
<body>

<header>
<input type="file" id="logoInput" onchange="changeLogo(this)">
<img id="logoImg" src="logo.png" alt="شعار النيابة">
<div class="header-text">
<h1>النيابة العامة</h1>
<h2>نيابة إستئناف شمال الأمانة</h2>
<h3>نيابة غرب الأمانة الإبتدائية</h3>
<p class="address">العنوان: صنعاء - شارع الحرية</p>
<p class="email-head">البريد الإلكتروني: Prosecutionwest@gmail.com</p>
</div>
</header>

<nav>
<a href="#home">الرئيسية</a>
<a href="#aboutSection">من نحن</a>
<a href="#citizenForm" onclick="openFormsPopup()">نماذج</a>
<a href="#newsSection">الأخبار</a>
<a href="#whatsappSection">الاستعلام</a>
<a href="#contact">تواصل معنا</a>
</nav>

<div class="marquee"><p>مرحبا بكم في موقع نيابة غرب الأمانة الإبتدائية</p></div>

<div class="icon-container">
<a href="https://www.facebook.com/share/1ExkmPipt5/" target="_blank"><i class="fab fa-facebook-f"></i></a>
<a href="https://wa.me/967778940199" target="_blank"><i class="fab fa-whatsapp"></i></a>
</div>

<div class="qr-code">
<p>امسح رمز الباركود للوصول للموقع من أي جهاز</p>
<img src="https://api.qrserver.com/v1/create-qr-code/?size=120x120&data=https://alsereheahmad-sys.github.io/niaba/" alt="QR Code">
</div>

<!-- النماذج -->
<div class="popup-overlay" id="formsPopup">
<div class="popup-content">
<h3>النماذج</h3>
<button onclick="closeFormsPopup()">إغلاق</button>
<div class="card">نموذج تحميل شكوى</div>
<div class="card">نموذج ارسال طلب قضائي</div>
<div class="card">نموذج تحديد موطن الاطراف في القضية</div>
</div>
</div>

<!-- نموذج تحديد موطن أطراف القضية -->
<div class="section" id="citizenForm">
<h2>تحديد موطن أطراف القضية</h2>
<form id="citizenFormActual">
<input type="text" name="name" placeholder="الاسم" required><div class="error-msg">الرجاء إدخال الاسم</div>
<input type="tel" name="phone" placeholder="رقم الهاتف" required><div class="error-msg">الرجاء إدخال رقم الهاتف</div>
<select name="role" required>
<option value="">اختر الصفة</option>
<option>شاكي</option>
<option>مشكوبه</option>
<option>وكيل</option>
<option>محامي</option>
<option>قريب</option>
</select><div class="error-msg">الرجاء اختيار الصفة</div>
<input type="file" name="pdfFile" accept=".pdf" required><div class="error-msg">الرجاء رفع ملف PDF</div>
<button type="submit">إرسال النموذج</button>
</form>
</div>

<!-- نموذج إرسال الشكوى -->
<div class="section" id="emailComplaintForm">
<h2>إرسال شكوى مباشرة</h2>
<form id="emailComplaintFormActual">
<input type="text" name="name" placeholder="الاسم الكامل" required><div class="error-msg">الرجاء إدخال الاسم</div>
<label>صورة الوثيقة الشخصية</label>
<input type="file" name="idPhoto" accept=".jpg,.jpeg,.png" required><div class="error-msg">الرجاء رفع صورة الوثيقة</div>
<label>رفع ملف الشكوى PDF</label>
<input type="file" name="complaintPDF" accept=".pdf" required><div class="error-msg">الرجاء رفع ملف PDF</div>
<button type="submit">إرسال الشكوى</button>
</form>
</div>

<!-- متابعة الأخبار -->
<div class="section" id="newsSection">
<h2>متابعة آخر الأخبار القضائية على فيسبوك</h2>
<div class="icon-container">
<a href="https://www.facebook.com/share/1ExkmPipt5/" target="_blank"><i class="fab fa-facebook-f"></i></a>
</div>
</div>

<!-- الاستعلام واتساب -->
<div class="section" id="whatsappSection">
<h2>الاستعلام على واتساب</h2>
<button onclick="openWhatsAppQuery()">فتح الاستعلام</button>
</div>

<div class="popup-overlay" id="whatsappPopup">
<div class="popup-content">
<h3>الاستعلام على واتساب</h3>
<select id="whatsappRole" required>
<option value="">اختر الصفة</option>
<option>شاكي</option>
<option>مشكوبه</option>
<option>وكيل</option>
<option>محامي</option>
</select>
<label>أرفق ما يثبت الصفة (PDF)</label>
<input type="file" id="whatsappFile" accept=".pdf" required>
<br><button onclick="sendWhatsAppQuery()">إرسال إلى واتساب</button>
<button onclick="document.getElementById('whatsappPopup').style.display='none'">إلغاء</button>
</div>
</div>

<!-- من نحن -->
<div class="section" id="aboutSection">
<h2>من نحن</h2>
<button onclick="openAbout()">عرض التفاصيل</button>
</div>

<div class="popup-overlay" id="aboutPopup">
<div class="popup-content">
<h3>النيابة العامة</h3>
<p>نيابة إستئناف شمال الأمانة</p>
<p>نيابة غرب الأمانة الإبتدائية</p>
<p>مسار التحول الرقمي</p>
<p>هدفنا: تقريب العدالة للمواطنين</p>
<button onclick="closeAbout()">إغلاق</button>
</div>
</div>

<!-- أوقات الدوام -->
<div class="section">
<h2>أوقات الدوام الرسمي</h2>
<p>من السبت إلى الأربعاء: ٩ صباحًا – ٢ ظهرًا</p>
</div>

<footer>
<p>جميع الحقوق محفوظة &copy; 2025</p>
<p>نيابة غرب الأمانة</p>
<p>تصميم وتنفيذ وإعداد م. أحمد السريحي</p>
</footer>

<div class="success-popup" id="successPopup">
<p></p>
<button onclick="closePopup()">حسناً</button>
</div>

<script>
// استبدل القيم التالية بالقيم الحقيقية من EmailJS
sendEmailJS('citizenFormActual','service_actualid','template_actualid');
sendEmailJS('emailComplaintFormActual','service_actualid','template_actualid');
</script>
</body>
</html>
