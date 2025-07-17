<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Secret Confession</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; }

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ffdde1, #ee9ca7);
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .card {
      background: white;
      padding: 35px 25px;
      border-radius: 20px;
      box-shadow: 0 12px 24px rgba(0,0,0,0.15);
      width: 90%;
      max-width: 420px;
      text-align: center;
      display: none;
      position: relative;
      animation: fadeIn 0.35s ease-in-out;
      transition: all 0.25s ease;
    }

    .card.active {
      display: block;
    }

    .back-button {
      position: absolute;
      top: 18px;
      left: 18px;
      background: #ffc1cc;
      border: none;
      color: #5a2a2a;
      font-weight: 600;
      padding: 6px 14px;
      border-radius: 20px;
      cursor: pointer;
      transition: 0.3s;
    }

    .back-button:hover {
      background: #ffb3bf;
      transform: scale(1.05);
    }

    h2 {
      margin-top: 45px;
      color: #3d1f1f;
      font-size: 24px;
    }

    p {
      color: #5c3d3d;
      font-size: 16px;
      margin-bottom: 25px;
    }

    .btn {
      padding: 12px 22px;
      margin: 8px;
      font-size: 15px;
      border-radius: 25px;
      border: none;
      cursor: pointer;
      transition: 0.2s ease-in-out;
    }

    .btn:hover {
      transform: scale(0.96);
    }

    .btn-main {
      background: #f06292;
      color: white;
    }

    .btn-main:hover {
      background: #e91e63;
    }

    .btn-secondary {
      background: #ffe4ec;
      color: #8e3c50;
      border: 1px solid #ffc4d6;
    }

    .btn-secondary:hover {
      background: #ffd9e5;
    }

    .confession {
      white-space: pre-line;
      color: #3c2b2b;
      font-size: 17px;
      line-height: 1.6;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.95); }
      to { opacity: 1; transform: scale(1); }
    }
  </style>
</head>
<body>

  <!-- Screen 1 -->
  <div class="card active" id="screen1">
    <h2>Hey, can I borrow a minute?</h2>
    <p>I just want to share something. It's not random, promise.</p>
    <button class="btn btn-main" onclick="goTo('screen2')">Sure</button>
    <button class="btn btn-secondary" onclick="goTo('fake1')">No</button>
  </div>

  <!-- Screen 2 -->
  <div class="card" id="screen2">
    <button class="back-button" onclick="goTo('screen1')">← Back</button>
    <h2>This might sound random</h2>
    <p>But I’ve been meaning to say this for a while now.</p>
    <button class="btn btn-main" onclick="goTo('screen3')">Proceed</button>
    <button class="btn btn-secondary" onclick="goTo('fake2')">Not sure</button>
  </div>

  <!-- Screen 3 -->
  <div class="card" id="screen3">
    <button class="back-button" onclick="goTo('screen2')">← Back</button>
    <h2>I’ve been thinking</h2>
    <p>You’ve been on my mind a lot lately. Thought you should know.</p>
    <button class="btn btn-main" onclick="goTo('screen4')">Go on</button>
    <button class="btn btn-secondary" onclick="goTo('fake3')">Okay?</button>
  </div>

  <!-- Screen 4 -->
  <div class="card" id="screen4">
    <button class="back-button" onclick="goTo('screen3')">← Back</button>
    <h2>One last thing</h2>
    <p>Would you want to know what I honestly feel?</p>
    <button class="btn btn-main" onclick="goTo('screen5')">Yes</button>
    <button class="btn btn-secondary" onclick="goTo('fake4')">No</button>
  </div>

  <!-- Confession Message -->
  <div class="card" id="screen5">
    <button class="back-button" onclick="goTo('screen4')">← Back</button>
    <h2>Just being honest</h2>
    <p class="confession">
Hi,I’ve been holding this in for a while now, and I don’t really know how to say it properly. So I made this. I like you. Not just in a friendly way it’s something more than that. No pressure or anything. Just wanted to be real with you. You can take this as a Compliment.
    </p>
  </div>

  <!-- Fake Screens -->
  <div class="card" id="fake1">
    <button class="back-button" onclick="goTo('screen1')">← Back</button>
    <h2>Haha, it’s nothing shady</h2>
    <p>Just something I’ve been wanting to say. Try again?</p>
  </div>

  <div class="card" id="fake2">
    <button class="back-button" onclick="goTo('screen2')">← Back</button>
    <h2>Wait up</h2>
    <p>You might want to hear this after all.</p>
  </div>

  <div class="card" id="fake3">
    <button class="back-button" onclick="goTo('screen3')">← Back</button>
    <h2>For real</h2>
    <p>This is something I’ve been meaning to share, not just random talk.</p>
  </div>

  <div class="card" id="fake4">
    <button class="back-button" onclick="goTo('screen4')">← Back</button>
    <h2>No worries</h2>
    <p>If you're not ready, that’s okay. Just thought I’d try.</p>
  </div>

  <script>
    function goTo(id) {
      document.querySelectorAll('.card').forEach(c => c.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }
  </script>

</body>
</html># Websites
