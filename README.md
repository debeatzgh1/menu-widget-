<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DebeatzGH</title>

  <style>
    body {
      margin: 0;
      min-height: 200vh;
      font-family: Arial, sans-serif;
      background: #f5f5f5;
    }

    /* Heartbeat animation */
    @keyframes heartbeat {
      0%   { transform: translateX(-50%) scale(1); }
      20%  { transform: translateX(-50%) scale(1.12); }
      40%  { transform: translateX(-50%) scale(1); }
      60%  { transform: translateX(-50%) scale(1.12); }
      100% { transform: translateX(-50%) scale(1); }
    }

    /* Floating Milkshake Button */
    .milkshake-btn {
      position: fixed;
      top: 20px;
      left: 50%;
      transform: translateX(-50%);
      width: 64px;
      height: 64px;
      background: #16a34a;
      color: #fff;
      font-size: 26px;
      font-weight: bold;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      box-shadow: 0 6px 16px rgba(0,0,0,0.3);
      animation: heartbeat 2.6s infinite ease-in-out;
      z-index: 9999;
    }

    .milkshake-btn:hover {
      background: #15803d;
    }
  </style>
</head>

<body>

  <!-- SINGLE FLOATING BUTTON -->
  <a
    href="https://msha.ke/debeatzgh"
    class="milkshake-btn"
    title="Open Milkshake"
  >
    ☰
  </a>

</body>
</html>
