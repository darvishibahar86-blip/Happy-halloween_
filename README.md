# Happy-halloween_
<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<title>کارت دعوت هالووین</title>
<style>
    body {
        margin: 0;
        padding: 0;
        font-family: "Vazirmatn", sans-serif;
        background: #0d0d0d;
        color: #fff;
        direction: rtl;
        text-align: center;
    }

    .container {
        width: 100%;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 20px;
    }

    .page {
        display: none;
        max-width: 600px;
        border: 2px solid #ff8800;
        padding: 25px;
        border-radius: 15px;
        background: rgba(40, 0, 60, 0.5);
        box-shadow: 0 0 25px #ff8800;
        animation: fade 0.5s ease;
    }

    @keyframes fade {
        from {opacity: 0;}
        to {opacity: 1;}
    }

    .buttons {
        margin-top: 20px;
    }

    button {
        background: #ff8800;
        color: #000;
        border: none;
        padding: 10px 20px;
        font-size: 18px;
        border-radius: 10px;
        cursor: pointer;
        margin: 5px;
        transition: 0.3s;
    }

    button:hover {
        background: #ffbb33;
    }

    h2 {
        color: #ffbb33;
        margin-bottom: 15px;
    }
</style>
</head>

<body>

<div class="container">

    <!-- صفحه ۱ -->
    <div class="page" id="page1">
        <h2>🎃 دعوت‌نامه هالووین 🎃</h2>
        <p>می‌خوام به یه مهمونی هالووین دعوتت کنم!  
        یه شب پر از ترس‌های بامزه، خنده‌های شیطونی و کلی سورپرایز منتظرته.</p>
    </div>

    <!-- صفحه ۲ -->
    <div class="page" id="page2">
        <h2>🕸 زمان و مکان</h2>
        <p><b>تاریخ:</b> 31 اکتبر</p>
        <p><b>ساعت:</b> 6 عصر تا پاسی از شب</p>
        <p><b>مکان:</b> دانشگاه تهران مرکز — قسمت سلف دانشگاه</p>
    </div>

    <!-- صفحه ۳ -->
    <div class="page" id="page3">
        <h2>👻 خوراکی با حرف اول اسم!</h2>
        <p>هرکی باید یه خوراکی بیاره که با حرف اول اسمش شروع بشه!</p>
        <p>مثلاً:</p>
        <p>آوا → آب‌نبات ترسناک</p>
        <br>
        <p><b>در آخر، هرکی خلاقانه‌ترین و جالب‌ترین خوراکی رو بیاره، امتیازش بالاتر می‌شه و جایزه می‌گیره!</b></p>
        <p>🎁 جایزه: <b>جام طلایی ترسِ خلاقانه</b></p>
    </div>

    <!-- صفحه ۴ -->
    <div class="page" id="page4">
        <h2>🧪 نکات بامزه</h2>
        <p>ماسک، گریم، یا هرچیزی که قیافه‌تو ترسناک‌تر کنه، امتیاز ویژه داره!</p>
        <p>اگر دوست داری، <b>کاستوم شخصیت موردعلاقه‌ت</b> رو هم بپوش — یا هرچیزی که فکر می‌کنی <b>ترسناک‌ترت می‌کنه</b>.</p>
        <p>هرچی خلاقانه‌تر باشه، جذاب‌تره!</p>
    </div>

    <!-- صفحه ۵ -->
    <div class="page" id="page5">
        <h2>🦇 پیام پایانی</h2>
        <p>منتظرتم تا با هم یه شب هالووینی بسازیم که تا مدت‌ها یادت نره.</p>
        <p>با عشق و شیطنت،</p>
        <p><b>آوا</b></p>
    </div>

    <!-- دکمه‌ها -->
    <div class="buttons">
        <button onclick="prevPage()">قبلی</button>
        <button onclick="nextPage()">بعدی</button>
    </div>

</div>

<script>
    let currentPage = 1;
    const totalPages = 5;

    function showPage(num) {
        document.querySelectorAll('.page').forEach(p => p.style.display = 'none');
        document.getElementById('page' + num).style.display = 'block';
    }

    function nextPage() {
        if (currentPage < totalPages) {
            currentPage++;
            showPage(currentPage);
        }
    }

    function prevPage() {
        if (currentPage > 1) {
            currentPage--;
            showPage(currentPage);
        }
    }

    showPage(currentPage);
</script>

</body>
</html>
