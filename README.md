<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Aleah — Maintenance</title>
  <meta name="description" content="The website is currently under maintenance. Please check back shortly." />

  <style>
    :root{
      --bg-dark: #0b0c10;
      --text: #e7eef5;
      --muted: #aab7c4;
      --accent1: #ff64a6;  /* pink from logo */
      --accent2: #48c6ef;  /* teal/blue from logo */
      --card: rgba(255,255,255,0.05);
      --shadow: 0 8px 30px rgba(0,0,0,0.35);
      --radius: 20px;
    }

    @media (prefers-color-scheme: light){
      :root{
        --bg-dark: #f7fafc;
        --text: #111827;
        --muted: #4b5563;
        --card: #ffffff;
        --shadow: 0 8px 25px rgba(17,24,39,0.08);
      }
    }

    *{box-sizing:border-box;}
    html,body{height:100%;margin:0;padding:0;font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;}
    body{
      background: radial-gradient(900px 600px at 10% 20%, rgba(255,100,166,0.08), transparent 60%),
                  radial-gradient(900px 600px at 90% 80%, rgba(72,198,239,0.08), transparent 60%),
                  var(--bg-dark);
      color:var(--text);
      display:grid;
      place-items:center;
      text-align:center;
      padding:2rem;
    }

    .card{
      background:var(--card);
      backdrop-filter: blur(10px);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
      padding:40px 32px 50px;
      max-width:640px;
      width:100%;
      animation: fadeIn 1s ease-in-out both;
    }
    @keyframes fadeIn{
      from{opacity:0; transform:translateY(10px);}
      to{opacity:1; transform:translateY(0);}
    }

    .logo-img{
      width:180px;
      height:auto;
      margin-bottom:16px;
      animation: float 3s ease-in-out infinite;
    }
    @keyframes float{
      0%,100%{transform:translateY(0);}
      50%{transform:translateY(-6px);}
    }

    h1{
      font-size:clamp(1.6rem,3vw,2rem);
      margin:10px 0 6px;
    }
    p{
      color:var(--muted);
      font-size:1rem;
      line-height:1.6;
      margin:0.5rem 0;
    }

    .progress{
      width:100%;
      height:8px;
      border-radius:999px;
      background:rgba(255,255,255,0.15);
      margin:24px 0 8px;
      overflow:hidden;
    }
    .progress span{
      display:block;
      height:100%;
      width:40%;
      background:linear-gradient(90deg,var(--accent2),var(--accent1));
      animation:slide 2.8s ease-in-out infinite;
    }
    @keyframes slide{
      0%{transform:translateX(-110%);}
      50%{transform:translateX(40%);}
      100%{transform:translateX(110%);}
    }

    .dots{display:inline-flex;gap:6px;margin-left:4px;}
    .dot{
      width:6px;height:6px;border-radius:50%;
      background:var(--accent2);
      opacity:.8;
      animation:bounce 1.2s infinite;
    }
    .dot:nth-child(2){animation-delay:.15s;}
    .dot:nth-child(3){animation-delay:.3s;}
    @keyframes bounce{
      0%,80%,100%{transform:translateY(0);}
      40%{transform:translateY(-6px);}
    }

    .contact{
      margin-top:18px;
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding:10px 14px;
      border-radius:12px;
      border:1px dashed rgba(255,255,255,0.18);
      background:rgba(255,255,255,0.06);
      color:var(--text);
      text-decoration:none;
      font-weight:600;
      transition:all .2s;
    }
    .contact:hover{
      border-color:var(--accent1);
      background:rgba(255,255,255,0.1);
      text-decoration:none;
    }

    footer{
      margin-top:20px;
      font-size:13px;
      color:var(--muted);
    }
  </style>
</head>
<body>
  <main class="card">
    <img src="logo-als.png" alt="Aleah logo" class="logo-img" />

    <h1>We’re improving things behind the scenes</h1>
    <p>
      The website is currently under maintenance. Please come back shortly
      <span class="dots"><span class="dot"></span><span class="dot"></span><span class="dot"></span></span>
    </p>

    <div class="progress"><span></span></div>
    <p style="margin-top:0;">Thank you for your patience.</p>

    <a class="contact" href="mailto:info@aleah.tech">
      ✉️ info@aleah.tech
    </a>

    <footer>© <span id="year"></span> Aleah. All rights reserved.</footer>
  </main>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
