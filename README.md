<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>النيابة العامة - نيابة غرب الأمانة الإبتدائية</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;700&display=swap');

body {font-family:'Cairo', sans-serif; margin:0; background:#f0f4fa; color:#222;}
header {
  background: linear-gradient(135deg,#003366,#0055aa);
  color:#fff;
  padding:20px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  flex-wrap:wrap;
  position: sticky;
  top:0;
  z-index:1000;
  box-shadow:0 0 20px rgba(0,0,0,0.3);
  transition: transform 0.3s ease;
}
header.scroll {transform: translateY(-10px);}
header img {width:80px; opacity:0.95;}
.header-text {text-align:center; flex:1; animation: glowHeader 2s infinite alternate;}
.header-text h1 {margin:0;font-size:1.8em;font-weight:bold; text-shadow:0 0 10px #00f;}
.header-text h2 {margin:3px 0;font-size:1.3em;font-weight:500;color:white;}
.header-text h3 {margin:3px 0;font-size:1.1em;font-weight:400;}
.header-text .address {font-size:0.95em; opacity:0.8;}
.email-head {margin-top:5px; font-weight:bold; font-size:0.9em;}
@keyframes glowHeader {0% {text-shadow: 0 0 5px #fff;} 100% {text-shadow: 0 0 20px #00f;}}

.marquee {overflow:hidden; white-space:nowrap; background:#0077cc; color:#fff;}
.marquee p {display:inline-block; padding-left:100%; animation: marquee 15s linear infinite; font-weight:bold; padding:10px 0;}
@keyframes marquee {0% { transform:translateX(0%);} 100% { transform:translateX(-100%);}}

/* الأقسام */
.section {background:#fff; margin:20px; padding:20px; border-radius:12px; box-shadow:0 4px 6px rgba(0,0,0,0.1);}
h2 {color:#003366; margin-bottom:10px; text-shadow:0 0 5px #0055aa;}
button {padding:10px 20px; background: linear-gradient(90deg,#003366,#0077cc); color:white; border:none; border-radius:8px; cursor:pointer; margin-top:10px; transition:0.3s;}
button:hover {background: linear-gradient(90deg,#0055aa,#0099ff);}

/* أيقونات لامعة */
.icon-container {display:flex; justify-content:center; gap:20px; margin-top:10px;}
.icon-container a {display:flex; align-items:center; justify-content:center; width:50px; height:50px; border-radius:50%; background:#003366; color:white; font-size:20px; text-decoration:none; transition: all 0.5s; box-shadow:0 0 5px #003366; animation: glow 2s infinite alternate;}
.icon-container a:hover {transform:scale(1.2); background:#0077cc; color:white;}
@keyframes glow {0% {box-shadow:0 0 5px #003366;} 100% {box-shadow:0 0 20px #00f;}}

/* النوافذ المنسدلة */
select, input[type=file], input[type=text], input[type=tel] {padding:10px; margin:8px 0; border-radius:6px; border:1px solid #ccc; width:100%; font-size:16px; transition:0.3s; cursor:pointer;}
select:hover,input[type=file]:hover,input[type=text]:hover,input[type=tel]:hover {border-color:#0077cc; box-shadow:0 0 5px #0077cc;}

/* QR code */
.qr-code {text-align:center; margin:20px 0;}
.qr-code img {width:120px; height:120px;}

/* Footer */
footer {background:#003366; color:white; padding:15px; text-align:center; font-size:14px;}
footer p {margin:5px;}
</style>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<script src="https://cdn.jsdelivr.net/npm/emailjs-com@3.2.0/dist/email.min.js"></script>
<script>
(function(){emailjs.init("YOUR_PUBLIC_KEY");})();
</script>
</head>
<body>

<header id="mainHeader">
  <img src="logo.png" alt="شعار النيابة">
  <div class="header-text">
    <h1>النيابة العامة</h1>
    <h2>نيابة إستئناف شمال الأمانة</h2>
    <h3>نيابة غرب الأمانة الإبتدائية</h3>
    <p class="address">العنوان: صنعاء - شارع الحرية</p>
    <p class="email-head">البريد الإلكتروني: info@west-niaba.com</p>
  </div>
</header>

<div class="marquee">
  <p>مرحبا بكم في موقع نيابة غرب الأمانة الإبتدائية</p>
</div>

<div class="qr-code">
  <p>امسح رمز الباركود للوصول للموقع من أي جهاز</p>
  <img src="https://api.qrserver.com/v1/create-qr-code/?size=120x120&data=https://yourwebsite.com" alt="QR Code">
</div>

<div class="icon-container">
  <a href="https://www.facebook.com/share/1ExkmPipt5/" target="_blank"><i class="fab fa-facebook-f"></i></a>
  <a href="https://wa.me/967778940199" target="_blank"><i class="fab fa-whatsapp"></i></a>
</div>

<!-- تحميل نموذج الشكوى مستقل -->
<div class="section">
  <h2>تحميل نموذج الشكوى</h2>
  <input type="file" accept=".pdf">
</div>

<!-- إرسال الشكوى إلكترونياً -->
<div class="section">
  <h2>إرسال الشكوى إلكترونياً</h2>
  <label>اختر الصفة</label>
  <select id="complaintRole" onchange="showRelativeOptionsComplaint()">
    <option value="شاكي">شاكي</option>
    <option value="وكيل الشاكي">وكيل الشاكي</option>
    <option value="محامي الشاكي">محامي الشاكي</option>
    <option value="قريب الشاكي">قريب الشاكي</option>
  </select>
  <select id="relativeRoleComplaint" style="display:none;">
    <option>الأب</option>
    <option>الأخ</option>
    <option>العم</option>
    <option>ابن العم</option>
    <option>الخال</option>
    <option>ابن الخال</option>
    <option>الصهر</option>
  </select>
  <label>ارفاق ملف الشكوى PDF</label>
  <input type="file" id="complaintPDF" accept=".pdf">
  <label>ارفاق صورة الوثيقة الشخصية</label>
  <input type="file" id="idImage" accept="image/*">
  <button onclick="sendComplaintEmail()">إرسال الشكوى</button>
</div>

<!-- الطلبات القضائية -->
<div class="section">
  <h2>إرسال الطلبات القضائية</h2>
  <label>اختر نوع الطلب</label>
  <select id="requestType">
    <option>طلب تسليم المضبوطات</option>
    <option>طلب كف خطاب</option>
    <option>طلب صورة قرار النيابة</option>
    <option>طلب إرسال الأوليات من قسم الشرطة</option>
    <option>طلب إرسال محبوس للنيابة</option>
  </select>
  <input type="text" id="requestName" placeholder="ادخل اسمك">
  <input type="tel" id="requestPhone" placeholder="رقم هاتفك">
  <label>اختر الصفة</label>
  <select id="requestRole">
    <option>شاكي</option>
    <option>مشكوبه</option>
    <option>وكيل</option>
    <option>محامي</option>
    <option>قريب</option>
  </select>
  <label>ارفق ملف الطلب PDF</label>
  <input type="file" id="requestPDF" accept=".pdf">
  <button onclick="sendRequestEmail()">إرسال الطلب</button>
</div>

<!-- الأخبار القضائية -->
<div class="section">
  <h2>آخر الأخبار القضائية</h2>
  <a href="https://www.facebook.com/share/1ExkmPipt5/" target="_blank">اضغط هنا لمتابعة الأخبار على فيسبوك</a>
</div>

<!-- أوقات الدوام -->
<div class="section">
  <h2>أوقات الدوام</h2>
  <p>من السبت إلى الأربعاء: ٩ صباحًا – ٢ ظهرًا</p>
</div>

<!-- استشارات قانونية -->
<div class="section">
  <h2>استشارات قانونية</h2>
  <p>لتعرف حقك القانوني</p>
  <a href="https://wa.me/967778940199" target="_blank"><button>تواصل عبر واتساب</button></a>
</div>

<!-- من نحن -->
<div class="section" id="about">
  <h2>من نحن</h2>
  <p>النيابة العامة - نيابة إستئناف شمال الأمانة - نيابة غرب الأمانة الإبتدائية، تعمل لتقريب العدالة من المواطنين.</p>
</div>

<footer>
  <p>جميع الحقوق محفوظة &copy; نيابة غرب الأمانة الإبتدائية</p>
  <p>إعداد وتصميم وإخراج م. أحمد السريحي</p>
</footer>

<script>
window.addEventListener("scroll", function(){
  const header=document.getElementById("mainHeader");
  if(window.scrollY>50){ header.classList.add("scroll"); }
  else{ header.classList.remove("scroll"); }
});

function showRelativeOptionsComplaint(){
  const val=document.getElementById("complaintRole").value;
  document.getElementById("relativeRoleComplaint").style.display=(val==="قريب الشاكي")?"block":"none";
}

function sendComplaintEmail(){
  const role = document.getElementById("complaintRole").value;
  let relative="";
  if(role==="قريب الشاكي"){ relative=document.getElementById("relativeRoleComplaint").value; }
  const pdfFile = document.getElementById("complaintPDF").files[0];
  const idFile = document.getElementById("idImage").files[0];
  if(!pdfFile){ alert("يرجى ارفاق ملف الشكوى PDF"); return; }
  if(!idFile){ alert("يرجى ارفاق صورة الوثيقة"); return; }

  emailjs.send("YOUR_SERVICE_ID","YOUR_TEMPLATE_ID",{
    role: role,
    relative: relative
  }).then(function(){
    alert("✅ تم إرسال الشكوى بنجاح!\nنعمل لأجل تقريب العدالة منكم");
  }, function(err){
    alert("حدث خطأ أثناء إرسال الشكوى: " + JSON.stringify(err
