<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>متجر الكينج</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 10px;
    padding: 10px;
    overflow-x: hidden;
    background-color: #f8f9fa;
  }

  header {
    background-color: #343a40;
    color: #f8f9fa;
    padding: 10px;
    text-align: center;
  }

  main {
    margin: 20px auto;
    overflow-x: auto;
    white-space: nowrap;
    text-align: center;
  }

  .app {
    display: inline-block;
    background-color: #f5f5f5;
    border: 1px solid #ccc;
    border-radius: 20px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    margin: 5px;
    padding: 10px;
    text-align: center;
    min-width: 150px;
    cursor: pointer;
    transition: transform 0.3s ease;
    font-size: 10px; /* تصغير حجم النص */
  }

  .app:hover {
    transform: translateY(-3px);
  }

  .app img {
    max-width: 50px;
    max-height: 50px;
    border-radius: 50%;
  }

  .app-details {
    display: none;
    margin-top: 10px;
    padding: 10px;
    background-color: #f5f5f5;
    border-radius: 10px;
  }

  .app-details p {
    margin-bottom: 10px;
  }

  .download-btn-container {
    position: relative;
  }

  .download-btn {
    background-color: #007bff;
    color: #fff;
    padding: 5px 10px; /* تصغير حجم الزر */
    border-radius: 25px;
    text-decoration: none;
    cursor: pointer;
    position: relative;
    z-index: 100;
    transition: background-color 0.3s ease;
    font-size: 12px; /* تصغير حجم النص داخل الزر */
  }

  .download-btn:hover {
    background-color: #0056b3;
  }

  .progress-bar-container {
    position: absolute;
    bottom: -8px;
    left: 0;
    width: 100%;
    height: 4px;
    background-color: #0056b3;
    border-radius: 2px;
    overflow: hidden;
  }

  .progress-bar {
    width: 0;
    height: 100%;
    background-color: #007bff;
    transition: width 0.3s ease;
  }

  .overlay {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    z-index: 9999;
  }

  .show-overlay {
    display: block;
  }

  .full-screen-app {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: #ffffff;
    border: 1px solid #e0e0e0;
    border-radius: 10px;
    padding: 20px;
    max-width: 90%;
    max-height: 90%;
    overflow: auto;
    z-index: 10000;
  }

</style>
</head>
<body>
<header>
  <h1> متجر الكينج</h1>
  <input type="text" id="searchInput" placeholder="ابحث هنا...">
  <button onclick="search()">ابحث</button>
</header>
<main>

  <!-- تطبيق 1 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src=" https://i.pinimg.com/736x/39/38/da/3938dac852a8962f8d4567e5579c7c8d.jpg" alt="تطبيق 1">
    <h2>عمر العنابي</h2>
    <div class="app-details">
      <p>الاسم :واتساب_عمر_العنابي V63.7:الاصدار 2024/6/4تاريخ الاصدار </p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar1', ' https://apps2.de0cfc686c69b8188bf4d167666f6c9e.r2.cloudflarestorage.com/users/4jN2p3DkmMa56/JiwSDr2lkuA4nA0_1717015360.apk?response-content-disposition=attachment%3B%20filename%3D%22OBWhatsApp_V63.7_Omar_Burgundy.apk%22&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=1cde638146bee296e532d15e2c58b261%2F20240612%2F%2Fs3%2Faws4_request&X-Amz-Date=20240612T192646Z&X-Amz-SignedHeaders=host&X-Amz-Expires=3600&X-Amz-Signature=042b08641f12397703dc7985f956ff7005d514bd646ee92ccfcc3ee31514981e ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- تطبيق 2 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/1b/6b/30/1b6b300c657656d4a66c4b15f2645f2e.jpg" alt="تطبيق 2">
    <h2>عمر الازرق</h2>
    <div class="app-details">
      <p>الاسم :واتساب_عمر_الازرق V63.7:الاصدار 2024/6/4تاريخ الاصدار</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar2', 'https://apps2.de0cfc686c69b8188bf4d167666f6c9e.r2.cloudflarestorage.com/users/4jN2p3DkmMa56/sqCd9fMLOfsTyQX_1717017573.apk?response-content-disposition=attachment%3B%20filename%3D%22OB3WhatsApp_V63.7_Omar_anapi_blu.apk%22&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=1cde638146bee296e532d15e2c58b261%2F20240612%2F%2Fs3%2Faws4_request&X-Amz-Date=20240612T194053Z&X-Amz-SignedHeaders=host&X-Amz-Expires=3600&X-Amz-Signature=166ce2e5a2057573089ecc632d0fff142018525072a4bd3c2847ffe8a5ad1ae4')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar2" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 3 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/5b/fa/2f/5bfa2f0055d160da83eaa0f775627653.jpg" alt="تطبيق 3">
    <h2>عمر الاخضر</h2>
    <div class="app-details">
      <p>الاسم :واتساب_عمر_الاخضر V63.7:الاصدار 2024/6/4تاريخ الاصدار</p>
      <div class="downlad-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar3', 'https://apps2.de0cfc686c69b8188bf4d167666f6c9e.r2.cloudflarestorage.com/users/4jN2p3DkmMa56/H09xwtNW4fBXIdy_1717024240.apk?response-content-disposition=attachment%3B%20filename%3D%22OB4WhatsApp_V63.7_Omar_green.apk%22&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=1cde638146bee296e532d15e2c58b261%2F20240612%2F%2Fs3%2Faws4_request&X-Amz-Date=20240612T194315Z&X-Amz-SignedHeaders=host&X-Amz-Expires=3600&X-Amz-Signature=b5fcf7c0d58a0944a66897accbc325a6ba08942ca5e0a47f313b8f09ac91a6a6')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar3" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 4 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/28/2b/0c/282b0c6fd7397e5ef29f0764fffc017b.jpg" alt="تطبيق 4">
    <h2>عمر الوردي</h2>
    <div class="app-details">
      <p>الاسم :واتساب_عمر_الوردي V63.7:الاصدار 2024/6/4تاريخ الاصدار</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar4', 'https://apps2.de0cfc686c69b8188bf4d167666f6c9e.r2.cloudflarestorage.com/users/4jN2p3DkmMa56/1AhXwZDCGGj2LVM_1717012509.apk?response-content-disposition=attachment%3B%20filename%3D%22OB2WhatsApp_V63.7_Omar_pink.apk%22&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=1cde638146bee296e532d15e2c58b261%2F20240612%2F%2Fs3%2Faws4_request&X-Amz-Date=20240612T193352Z&X-Amz-SignedHeaders=host&X-Amz-Expires=3600&X-Amz-Signature=7931678dc291c22e3e7ea2d146f9ec22328102782866a2a1dac965c4cb36e315')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar4" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- إضافة تطبيقات أخرى هنا -->

</main>
  <main>

  <!-- تطبيق 1 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/48/74/a1/4874a189545408c84fff0b744df5b5d5.jpg" alt="تطبيق 1">
    <h2>انستا الذهبي</h2>
    <div class="app-details">
      <p>انستاجرام التاج معدل تستطع من خلاله اخفاء انك متصل واخفى مشاهده الرسائل وتحميل الفيديوهات بدون علامات مائيه.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar1', ' https://dll.omar-ym.com/apps/instagold/8.0/InstaGold_v8.0.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- تطبيق 2 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/bf/58/69/bf58695e4e3955aa79dda5b72f564dc7.jpg" alt="تطبيق 2">
    <h2>تلجرام الذهبي</h2>
    <div class="app-details">
      <p>تلجرام ذهبي تعديل ومميزات اضافيه.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar2', ' https://downloadf1.appsfire.co/TeleGold/3.4.0/Telegram_Gold_v3.4.0.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar2" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 3 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/c3/dd/61/c3dd61136946bc3f9df1f62b748fedd4.jpg" alt="تطبيق 3">
    <h2>تويتر التاج</h2>
    <div class="app-details">
      <p>تويتر التاج تويتر معدل من خلاله تسطيع عمل.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar3', ' https://downloadf1.appsfire.co/twitter/2.40/X_Gold_v2.40.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar3" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 4 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/ae/ef/c7/aeefc73fe9d42fdd212d36b9a778722b.jpg" alt="تطبيق 4">
    <h2>يوتيوب التاج</h2>
    <div class="app-details">
      <p>يوتيوب التاج يوتيوب معدل تستطيع من خلاله تحميل الفيديوهات وحفضها على الجهاز</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar4', ' https://downloadf1.appsfire.co/YTGold/10.0/YouTube_Gold_V10.0.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- إضافة تطبيقات أخرى هنا -->

</main>
  <main>

  <!-- تطبيق 1 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/35/49/99/3549990c0404ffeb83233ecca09f90ce.jpg" alt="تطبيق 1">
    <h2>بلاس الذهبي</h2>
    <div class="app-details">
      <p> التطبيق:وتساب بلاس الذهبي</p>
      <p>v11.36 :الاصدار</p>
      <p>2024-05-07:تاريخ النشر</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar1', 'https://downloadf1.appsfire.co/abuarab/11.36/WA2_Abo3rab_v11.36.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- تطبيق 2 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcRvo8m6RB8v4ZcJsFABk_bqvAR2334pGXBmtfpG5mpwoL5B1cm2" alt="تطبيق 2">
    <h2>بلاس الازرق</h2>
    <div class="app-details">
      <p>التطبيق:وتساب بلاس الازرق</p>
      <p>v11.36 :الاصدار</p>
      <p>2024-05-07:تاريخ النشر</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar2', 'https://downloadf1.appsfire.co/abuarab/11.36/WA4_Abo3rab_v11.36.apk')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar2" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 3 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/a8/b1/9c/a8b19c0d70aa5bae13db7b05e43ff9ac.jpg" alt="تطبيق 3">
    <h2>بلاس الاحمر</h2>
    <div class="app-details">
      <p>التطبيق:وتساب بلاس الاحمر</p>
      <p>v11.36 :الاصدار</p>
      <p>2024-05-07:تاريخ النشر</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar3', ' https://downloadf1.appsfire.co/abuarab/11.36/WA3_Abo3rab_v11.36.apk')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar3" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 4 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/62/7e/ec/627eec094ea1b30168989cdd2a91ba70.jpg" alt="تطبيق 4">
    <h2>بلاس الاخضر</h2>
    <div class="app-details">
      <p>التطبيق:وتساب بلاس الاخضر</p>
      <p>v11.36 :الاصدار</p>
      <p>2024-05-07:تاريخ النشر</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar4', 'https://downloadf1.appsfire.co/abuarab/11.36/WA_Abo3rab_v11.36.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- إضافة تطبيقات أخرى هنا -->
</main>
<main>  

  <!-- تطبيق 1 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/98/32/a0/9832a05e8d6f4fb3f189813c1ce3f35a.jpg" alt="تطبيق 1">
    <h2>vidmat</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar1', 'https://files.modyolo.com/VidMate/VidMate%20v5.1904%20(Premium).apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- تطبيق 2 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/58/e2/a6/58e2a6359449ce6573517e4fed5a5288.jpg" alt="تطبيق 2">
    <h2>snaptube</h2>
    <div class="app-details">
      <p>هو التطبيق الاول في التقييم في تحميل الفيديوهات.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar2', 'https://up.apkbaba.com/apps/Snaptube-6-18-0-6182910-(Apkbaba.com).apk')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar2" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 3 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/91/39/41/9139416122e9433a8280459569a4c0fc.jpg" alt="تطبيق 3">
    <h2>كين مستر</h2>
    <div class="app-details">
      <p>التطبيق:كين مستر</p>
      <p>تطبيق لعمل مونتاج والتعديل على الفيديوهات</p>
      <p>مميزات التطبيق: بدون علامات مائيه</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar3', ' https://up.bramj3d.com/bramjapk/KineMaster_Gold_bramj3d.com.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar3" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 4 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://apkapks.com/img/uploads/posticon175/2023/08/Tiktok.gold-175-66.webp" alt="تطبيق 4">
    <h2>تيك توك التاج</h2>
    <div class="app-details">
      <p>تيك توك التاج معدل مع ازاله العلامات المائيه عند التحمبل والمزيد من المميزات اكتشفها بنفسك .</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar4', 'https://apkapks.com/apk/noplay/Tiktok.gold.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
      <p>تحميل التطبيق المساعد لتسجيل الدخول</p>
      <button class="download-btn" onclick="startDownload(event, 'progressBar2', ' https://apkapks.com/apk/noplay/tiktok.plugin.apk ')">تحميل</button>
    </div>
  </div>
  
  <!-- إضافة تطبيقات أخرى هنا -->

</main>
  <main>

  <!-- تطبيق 1 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/62/f1/8b/62f18b4243d51818bcd70de7f9dfa0c6.jpg" alt="تطبيق 1">
    <h2>حواء البنفسجي</h2>
    <div class="app-details">
      <p>وتساب حواء البنفسجي وتساب معدل يحتوي على جميع مميزات وتساب GB.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar1', ' https://download2388.mediafire.com/i1cus8bw1qhgvgDhzrv4kcxwczgpU2PCzWP0Aem3QC_PNu5g16N3Fpt0I0AK-pS29THwwHHxfaezajiKTg1MYOqCqGC6L1nCTa8xmvTHRdPtf4ViyeByZC_7Aisu19RCvbCTtowDcHa1fRAO9bO2Y9PLI1PfHILKmkGIIdZiC2p5/d4gk9snpdmkc2k3/HawaWhatsApp_Violet_v38.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- تطبيق 2 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/bc/9c/d5/bc9cd5250f75a7b48712a9345965266e.jpg" alt="تطبيق 2">
    <h2>ادم الاسود</h2>
    <div class="app-details">
      <p> وتساب ادم الاسود وتساب يحتوي على مميزات GB.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar2', ' https://cdn1.droidyplay.com/download/adamwhatsapp_black/?wpdmdl=80&refresh=66539467835161716753511 ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar2" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 3 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/ff/40/a6/ff40a6679deb1e2ba7091d69a6a181ee.jpg" alt="تطبيق 3">
    <h2>حواء الاحمر</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar3', ' https://download2388.mediafire.com/vd52sc4tudfg0c8gjRpPhg38YYbMDNHJMVCL4tU0aF50kTIecdMB0OCZlPtjkr5CMF8odR_i9fKaE6PEtFBHA1ph3HayY1AGvNoZswx-wjVMNgw0UZgILOZIZvfa2X-Ybpku3rvzywcRZC7cuHNhAte_p-oNg4bxTUqpyUCmQPbH/bjnlojthv02nu8h/Hawa2WhatsApp_Red_v38.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar3" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 4 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/72/b5/de/72b5deb4d8d2ef19d98491a082d50b1b.jpg" alt="تطبيق 4">
    <h2>ادم البني</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar4', ' https://cdn1.droidyplay.com/download/adam2whatsapp_brown_v38/?wpdmdl=79&refresh=665394aa048b01716753578 ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- إضافة تطبيقات أخرى هنا -->
</main>
 <main> 
  <!-- تطبيق 1 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/b3/37/99/b33799aced568090514bbf9f85e7c51a.jpg" alt="تطبيق 1">
    <h2>فيسبوك</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar1', 'https://download2389.mediafire.com/943zn6jqw6rgB0MU3mmMOXV7M0gNXJKsjxy0loXcFdbaInaBvr92lDSuoiT5dLP9XNIxhfKgbt0yBB3vaEzZR2o64wa9kfa93p1CZfeNDFgpCjb5FL-yMiTs56G4VdneeOCup1PmQoFghitVSRHiLIuc1OsRaaXf6s8PtAZEY0TPMQ/ebspbg2rp9rh4m3/facebook_Gold_v18.apk')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- تطبيق 2 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://apkappss.net/wp-content/uploads/2023/10/Imo-Gold-Logo.webp" alt="تطبيق 2">
    <h2>إيمو</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar2', 'https://dl.pramgplus.com/uploads/Imo_Plus_Gold_PramgPlus.Com.apk')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar2" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 3 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/81/f9/84/81f9842aa3f3882c3a1d072a026e83cb.jpg" alt="تطبيق 3">
    <h2>الاخضر الرسمي</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar3', ' https://scontent.whatsapp.net/v/t61.25591-34/10000000_1823955271452531_7338973506414288154_n.apk/WhatsApp.apk?ccb=1-7&_nc_sid=c49adc&_nc_ohc=x7uDcNzFtc4Q7kNvgEwcatj&_nc_ht=scontent.whatsapp.net&oh=01_Q5AaIPfnJY9W-QiPLAipdILtUDO434eXxKt2qxKpT6RVRKRq&oe=667AE805 ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar3" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 4 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://i.pinimg.com/736x/b0/08/d8/b008d8f21a5bf03fd1c0f50eadbe5c44.jpg" alt="تطبيق 4">
    <h2>اعمال الرسمي</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar4', ' https://dw.uptodown.net/dwn/-MiKFXlQbdOsYiuL7JqYihz-hycer2Y99v_kq84U0HVUUQlKvU6sE3-My-OeiwY6Jc5jT0_YxWLGVrau207een6c77VAgIUsA9DJZAH_C093q0ZYA9sHwA7q5oRxKcpX/nCWKN7xLgmMud_K8jcUDuwjlTa8aSfjhaEiwsPX5Y8NHvKVI073T6PwIbe7XBZVqorL2ivLBdwicG5HhsFk9jkW-cI9yfSmU-0-kp_LaaJt8oSRzF4s7lEy3STHO932h/fgChLvZUkZpDQRj7LQLL9607zddV_cbYxqGc-LoYWY9Mi2XRF6Xo33AXOA5T304pB9RktKQOdpABAez6R0QIFxhLd6o7GzZdXtTaG7IHMKDfGr_KJQW_bV45WECGQzar/whatsapp-business-2-24-11-80.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- إضافة تطبيقات أخرى هنا -->
</main>   
<main>

  <!-- تطبيق 1 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcQ9vXQHBc44FrzhohQlErrpi-TBJP0P3bkHh_SWbzRMREBrmBFw" alt="تطبيق 1">
    <h2>البلاني الاسود</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar1', ' https://download2390.mediafire.com/zql8mvxuyzagWyJb9wEca2jn9CqL57PZk2YthRRNvt8Gb3PXsztXmkgo9-hVkNV4p9QZS4A-eTFQvRBHQz8wz53rLc_aqph3APvmQBvvJGVJEWc_CEGwB5-jnsDT6JMNPHu9erdnUKuS1zuFrnUjOwZlUGZPnuKbniP1lFL_vFXk/841ihx0stbaknzi/FB2WA_Balck_V21.36_By_Fahed_Al-Balani.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- تطبيق 2 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGa296pygVcdfPDMrn5dVlxImodJcbFUu1zd2vKXmy23OQ2pvz" alt="تطبيق 2">
    <h2>النجم العنابي</h2>
    <div class="app-details">
      <p>وصف التطبيق يذهب هنا.</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar2', ' https://download2335.mediafire.com/vaigiunewyegCwFrS9GWoEeEN4G4LdSK2i4_CehSUUhFcMYMTrCJq3AnUZMDNzzLoT3RjTZ-EiKu72gHFW_tIbZUmp7JbFe3kT2ItuxQo6JNRZkviyTOeZmQPDaRXkFvDT8SWSk3EqlSAgKKPofs6fRf0eWHuQXjeY5tco1CxaEU/9j0ym1i8v9eepjn/AQ2WhatsApp.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar2" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 3 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://alwebnews.com/wp-content/uploads/2024/02/SnapChat-Plus-Logo.webp" alt="تطبيق 3">
    <h2>سناب شات التاج</h2>
    <div class="app-details">
      <p>سناب شات التاج معدل تستطيع اخفاء مشاهده الرسائل او تغيير موقعك </p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar3', ' https://downloadf1.appsfire.co/GoldSC/1.90/GoldSC_V1.90_ByAbu3rab.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar3" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- تطبيق 4 -->
  <div class="app" onclick="toggleDetails(event, this)">
    <img src="https://traidmod.com/wp-content/uploads/2023/12/WhatsApp-Business-Gold-Logo.webp" alt="تطبيق 4">
    <h2>وتساب اعمال التاج</h2>
    <div class="app-details">
      <p>وتساب للاعمال معدل تاريخ النشر (2024/5</p>
      <div class="download-btn-container">
        <button class="download-btn" onclick="startDownload(event, 'progressBar4', ' https://download2340.mediafire.com/pqnva8lmmk8gSJ2hoviDQUnzmGxylAxt5fuDJCyzyumx3TOyuRBytnfhcjhLTlFmbGvP2O7rVv3ETc10Ex8jjvd4dF7UfpC6ozfm61wDgLkvhge-yGLvJgJ6mgMH1DJ807t85QU3pC1Kaocdg69EWJ3natVk6BWpIAt06thsAL-mPA/w73o749axjhugqq/WA_Business_Gold_Clone_v3.0.apk ')">تحميل</button>
        <div class="progress-bar-container">
          <div id="progressBar1" class="progress-bar"></div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- إضافة تطبيقات أخرى هنا -->

</main>
</main>
</main>
<footer>
  <p>&copy;  متجر الكينج الشامل جميع الحقوق محفوظه تصميم وبرمجه عاهد خشافه.</p>
</footer>
<div class="overlay" onclick="closeFullScreenApp()"></div>
<div class="full-screen-app"></div>
<script>
  function toggleDetails(event, app) {
    event.stopPropagation();
    var fullScreenApp = document.querySelector('.full-screen-app');
    var appContent = app.cloneNode(true);
    appContent.classList.add('show-overlay');
    appContent.querySelector('.app-details').style.display = 'block';
    fullScreenApp.innerHTML = '';
    fullScreenApp.appendChild(appContent);
    document.querySelector('.overlay').style.display = 'block';
    document.querySelector('.full-screen-app').style.display = 'block';
  }

  function closeFullScreenApp() {
    document.querySelector('.overlay').style.display = 'none';
    document.querySelector('.full-screen-app').style.display = 'none';
  }

  function search() {
    var searchInput = document.getElementById('searchInput').value.toLowerCase();
    var apps = document.getElementsByClassName('app');
    for (var i = 0; i < apps.length; i++) {
      var appName = apps[i].getElementsByTagName('h2')[0].innerText.toLowerCase();
      var appDescription = apps[i].getElementsByClassName('app-details')[0].innerText.toLowerCase();
      if (appName.includes(searchInput) || appDescription.includes(searchInput)) {
        apps[i].style.display = "inline-block";
      } else {
        apps[i].style.display = "none";
      }
    }
  }

  function startDownload(event, progressBarId, downloadLink) {
    event.stopPropagation();
    var progressBar = document.getElementById(progressBarId);

    // Reset and show the progress bar
    progressBar.style.width = '0';
    progressBar.style.display = 'block';

    // Simulate download progress
    var downloadInterval = setInterval(function() {
      if (progressBar.style.width === '100%') {
        clearInterval(downloadInterval); // Stop the progress bar when download is complete
        progressBar.style.display = 'none'; // Hide the progress bar after completion
      } else {
        var currentWidth = parseFloat(progressBar.style.width);
        currentWidth += 10; // Increment the progress bar width
        progressBar.style.width = currentWidth + '%';
      }
    }, 500); // Update the progress bar every 0.5 seconds

    // Simulate download completion after a certain time (3 seconds in this example)
    setTimeout(function() {
      window.open(downloadLink, "_blank");
    }, 3000);
  }
</script>
</body>
</html>
