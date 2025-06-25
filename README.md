<!DOCTYPE html>
<html lang="ur">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>toolcR</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-900 text-white font-sans p-4">
  <script>
    let timeLeft = 25;
    let timer;

    function startTimer(button) {
      const watchNowBtn = button;
      const timerDisplay = watchNowBtn.nextElementSibling;
      watchNowBtn.disabled = true;
      timer = setInterval(() => {
        timeLeft--;
        timerDisplay.textContent = `Remaining: ${timeLeft} seconds`;
        if (timeLeft <= 0) {
          clearInterval(timer);
          timerDisplay.textContent = "";
          watchNowBtn.disabled = false;
          timeLeft = 25; // ٹائمر دوبارہ 25 سیکنڈ پر ری سیٹ
        }
      }, 1000);
    }
  </script>

  <!-- سیکشن 1 -->
  <div class="mb-6">
    <!-- اوپر ایڈ -->
    <div id="adTop1" class="w-full max-w-md mb-2">
      ### گوگل ایڈ موب ###
    </div>

    <!-- امیج -->
    <img id="topImage1" src="" alt="امیج 1" class="w-full max-w-md rounded-lg shadow-lg mb-2">

    <!-- نیچے ایڈ -->
    <div id="adBottom1" class="w-full max-w-md mb-2">
      ### گوگل ایڈ موب ###
    </div>

    <!-- واچ ناؤ بٹن -->
    <div class="text-center">
      <button id="watchNowBtn1" class="bg-green-500 text-white font-bold py-2 px-4 rounded-full hover:bg-green-600 transition duration-300 disabled:bg-gray-500" onclick="startTimer(this)">
        Watch Now
      </button>
      <p id="timer1" class="mt-1 text-sm"></p>
    </div>
  </div>

  <!-- سیکشن 2 (یہاں سے آپ دوبارہ پیسٹ کر سکتے ہیں) -->
  <div class="mb-6">
    <!-- اوپر ایڈ -->
    <div id="adTop2" class="w-full max-w-md mb-2">
      ### گوگل ایڈ موب ###
    </div>

    <!-- امیج -->
    <img id="topImage2" src="" alt="امیج 2" class="w-full max-w-md rounded-lg shadow-lg mb-2">

    <!-- نیچے ایڈ -->
    <div id="adBottom2" class="w-full max-w-md mb-2">
      ### گوگل ایڈ موب ###
    </div>

    <!-- واچ ناؤ بٹن -->
    <div class="text-center">
      <button id="watchNowBtn2" class="bg-green-500 text-white font-bold py-2 px-4 rounded-full hover:bg-green-600 transition duration-300 disabled:bg-gray-500" onclick="startTimer(this)">
        Watch Now
      </button>
      <p id="timer2" class="mt-1 text-sm"></p>
    </div>
  </div>

  <!-- اسی طرح آپ دوبارہ پیسٹ کر سکتے ہیں اور IDs (adTop3, topImage3, etc.) تبدیل کر سکتے ہیں -->
</body>
</html>
