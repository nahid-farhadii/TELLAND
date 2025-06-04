<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>شماره کارت‌</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Vazirmatn&display=swap');

    body {
      font-family: "Vazirmatn", sans-serif;
      background-image: url('logo.jpg'); /* تصویر لوگو به عنوان بک‌گراند */
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
      backdrop-filter: blur(4px);
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      margin: 0;
      padding: 2rem;
      gap: 1rem;
    }

    .card {
      background-color: rgba(255, 255, 255, 0.9);
      border: 2px solid #ddd;
      border-radius: 20px;
      padding: 2rem;
      width: 320px;
      text-align: center;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .bank {
      font-size: 1.3rem;
      font-weight: bold;
      margin-bottom: 1rem;
    }

    .card-number {
      font-size: 1.4rem;
      direction: ltr;
      margin: 0.8rem 0;
      letter-spacing: 2px;
    }

    .owner {
      font-size: 1rem;
      color: #333;
    }

    button {
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      font-size: 1rem;
      border: none;
      border-radius: 8px;
      background-color: #4caf50;
      color: white;
      cursor: pointer;
    }

    button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

  <div class="card">
    <div class="bank">بانک ملت</div>
    <div class="card-number" id="card1">6104 3378 5964 7890</div>
    <div class="owner">به نام: امیر محمدی</div>
    <button onclick="copyToClipboard('card1')">کپی</button>
  </div>

  <div class="card">
    <div class="bank">بانک ملی</div>
    <div class="card-number" id="card2">6037 9918 2497 1264</div>
    <div class="owner">به نام: امیر محمدی</div>
    <button onclick="copyToClipboard('card2')">کپی</button>
  </div>

  <div class="card">
    <div class="bank">بانک صادرات</div>
    <div class="card-number" id="card3">6276 4121 3244 1098</div>
    <div class="owner">به نام: امیر محمدی</div>
    <button onclick="copyToClipboard('card3')">کپی</button>
  </div>

  <div class="card">
    <div class="bank">بانک تجارت</div>
    <div class="card-number" id="card4">5859 8310 0045 2378</div>
    <div class="owner">به نام: امیر محمدی</div>
    <button onclick="copyToClipboard('card4')">کپی</button>
  </div>

  <script>
    function copyToClipboard(id) {
      const text = document.getElementById(id).innerText;
      navigator.clipboard.writeText(text)
        .then(() => alert('شماره کارت کپی شد'))
        .catch(() => alert('کپی نشد'));
    }
  </script>

</body>
</html>
