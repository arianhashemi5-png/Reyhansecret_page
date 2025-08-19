# Reyhansecret_page
<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🌌 دنیای خیال ریحان 💙</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    @import url('https://cdn.jsdelivr.net/gh/rastikerdar/vazir-font@v30.1.0/dist/font-face.css');

    body {
      font-family: 'Vazir', sans-serif;
      margin: 0;
      padding: 0;
      overflow-x: hidden;
      background: #0b0c2a;
      color: #e0f2fe;
    }

    /* شفق قطبی بالای صفحه */
    #aurora {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 40vh;
      background: linear-gradient(120deg, #0f0c4f, #2a1f8f, #0f0c4f);
      animation: auroraShift 10s infinite alternate;
      z-index: 0;
      opacity: 0.8;
    }

    @keyframes auroraShift {
      0% { background-position: 0% 50%; }
      100% { background-position: 100% 50%; }
    }

    /* ستاره‌ها */
    .star {
      position: absolute;
      width: 2px;
      height: 2px;
      background: #fff;
      border-radius: 50%;
      opacity: 0.8;
      animation: twinkle 2s infinite alternate;
    }

    @keyframes twinkle {
      0% { opacity: 0.2; transform: scale(0.8);}
      50% { opacity: 1; transform: scale(1.2);}
      100% { opacity: 0.3; transform: scale(1);}
    }

    /* متن مرکزی */
    #content {
      position: relative;
      z-index: 2;
      max-width: 800px;
      margin: 10vh auto 10vh auto;
      padding: 2rem;
      background: rgba(0, 0, 40, 0.6);
      border-radius: 2rem;
      box-shadow: 0 0 30px rgba(0,0,0,0.5);
    }

    #content p {
      line-height: 1.8rem;
      font-size: 1.2rem;
      text-align: justify;
    }

    /* پایین صفحه: قلب‌ها و ذرات */
    .heart, .spark {
      position: absolute;
      z-index: 1;
      animation: floatUp linear infinite;
    }

    .heart {
      width: 20px;
      height: 20px;
      background: #1e90ff;
      clip-path: polygon(50% 0%, 61% 14%, 75% 14%, 87% 27%, 87% 45%, 50% 100%, 13% 45%, 13% 27%, 25% 14%, 39% 14%);
      opacity: 0.7;
    }

    .spark {
      width: 4px;
      height: 4px;
      background: #00f;
      border-radius: 50%;
      opacity: 0.5;
    }

    @keyframes floatUp {
      0% { transform: translateY(0) scale(0.5);}
      100% { transform: translateY(-120vh) scale(1);}
    }

  </style>
</head>
<body>
  <div id="aurora"></div>

  <!-- ستاره‌ها -->
  <script>
    const starCount = 120;
    for(let i=0;i<starCount;i++){
      const star = document.createElement('div');
      star.classList.add('star');
      star.style.top = Math.random() * 100 + 'vh';
      star.style.left = Math.random() * 100 + 'vw';
      star.style.animationDuration = (Math.random()*3 + 2) + 's';
      document.body.appendChild(star);
    }
  </script>

  <!-- متن مرکزی -->
  <div id="content">
    <h1 class="text-4xl font-bold text-center mb-6">💙 خوش آمدی ریحان 💙</h1>
    <p>
      در این دنیای کوچک اما پرنور، هر موج نور و هر ستاره‌ای که چشمک می‌زند، بخشی از قلب توست.  
      هر لحظه، هر فکر و هر لبخندت با رنگ آبی و خیال عجین شده است.  
      اینجا جایی است برای کشف خیال‌های نو، برای لمس نورهایی که آرام آرام دل را پر می‌کنند و برای تجربه‌ای که خاص توست.  
      میان موج‌های نور و قلب‌های آبی، داستانی تازه شروع می‌شود؛ داستانی که تنها تو می‌دانی چگونه باید پیش برود.
    </p>
    <p class="mt-4">
      🌌 هر قلب آبی، هر ذره‌ی نور، و هر موج شفق، یادآوری است از عمقِ جادویی وجود تو.  
      دنیا برای تو ساخته شده و اینجا، هر جزئیات کوچک برای تو طراحی شده است.  
    </p>
    <p class="mt-4 text-center text-xl font-semibold">💙 ریحان، جهان کوچک ما با نور و خیال، همیشه جای توست 🌌💙</p>
  </div>

  <!-- پایین صفحه: قلب‌ها و ذرات -->
  <script>
    function createFloating(className, count){
      for(let i=0;i<count;i++){
        const el = document.createElement('div');
        el.classList.add(className);
        el.style.left = Math.random()*100 + 'vw';
        el.style.animationDuration = (5 + Math.random()*5) + 's';
        el.style.opacity = 0.3 + Math.random()*0.7;
        document.body.appendChild(el);
      }
    }
    createFloating('heart', 25);
    createFloating('spark', 50);
  </script>
</body>
</html>
