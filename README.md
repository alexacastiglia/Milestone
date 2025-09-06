<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Change Lives with Clean Water</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400&display=swap" rel="stylesheet">
  <style>
    :root{
      --ink:#1a1a1a; --ink-dim:#333; --cw-blue:#003366; --cw-yellow:#ffc907; --cw-yellow-d:#e6b800; 
      --bg:#FFF7E1; --surface:#ffffff; --radius:12px; --shadow:0 8px 24px rgba(0,0,0,.12);
    }
    *{box-sizing:border-box}
    html, body{height:100%}
    body{margin:0;font-family:"Proxima Nova", system-ui, -apple-system, "Segoe UI", Roboto, Arial, sans-serif;font-weight:400;color:var(--ink);background:var(--bg)}

    .navbar{position:sticky;top:0;z-index:10;display:flex;justify-content:space-between;align-items:center;gap:1rem;padding:1rem 2rem;background:var(--surface);border-bottom:1px solid rgba(0,0,0,.06)}
    .logo{display:flex;align-items:center;gap:.5rem;font-family:"Proxima Nova", sans-serif;font-weight:400;color:var(--ink);letter-spacing:.2px}
    .logo img{height:32px;width:auto;display:block}
    .nav-links{list-style:none;display:flex;gap:1.25rem;margin:0;padding:0}
    .nav-links li{position:relative}
    .nav-links a{display:flex;align-items:center;gap:.35rem;color:var(--ink);text-decoration:none;font-family:"Proxima Nova", sans-serif;font-weight:400}
    .nav-links a svg{width:16px;height:16px;stroke:var(--ink);fill:none;stroke-width:2;transition:transform .2s}
    .nav-links li:hover > a svg{transform:rotate(180deg)}
    .signup-btn{background:var(--cw-yellow);color:var(--ink);padding:.55rem 1rem;border-radius:8px;text-decoration:none;font-family:"Proxima Nova", sans-serif;font-weight:400;box-shadow:0 0 0 0 rgba(255,201,7,.6);transition:box-shadow .25s, transform .2s, background .25s}
    .signup-btn:hover{background:var(--cw-yellow-d);box-shadow:0 0 24px 6px rgba(255,201,7,.35);transform:translateY(-1px)}

    .dropdown{display:none;position:absolute;top:100%;left:0;background:var(--surface);padding:.5rem 0;border-radius:8px;box-shadow:0 4px 12px rgba(0,0,0,.15)}
    .dropdown a{padding:.5rem 1rem;display:block;white-space:nowrap;font-family:"Proxima Nova", sans-serif;font-weight:400}
    .nav-links li:hover .dropdown{display:block}

    .hero{display:grid;grid-template-columns:1.1fr .9fr;align-items:center;gap:2rem;padding:2.5rem clamp(1rem, 3vw, 2rem)}
    .hero h1{font-size:clamp(1.9rem, 4vw, 2.8rem);line-height:1.15;margin:.2rem 0 1rem;font-weight:400;font-family:"Proxima Nova", sans-serif}
    .hero p{margin:0 0 1.25rem;color:var(--ink-dim);max-width:60ch;font-family:"Proxima Nova", sans-serif;font-weight:400}
    .hero-buttons{display:flex;flex-wrap:wrap;gap:.75rem}
    .btn{display:inline-block;padding:.8rem 1.4rem;border-radius:10px;text-decoration:none;font-family:"Proxima Nova", sans-serif;font-weight:400;transition:box-shadow .25s, transform .2s, background .25s}
    .btn-primary{background:var(--cw-yellow);color:var(--ink)}
    .btn-primary:hover{background:var(--cw-yellow-d);transform:translateY(-1px)}
    .btn-secondary{background:#bf6c46;color:#fff}
    .btn-secondary:hover{background:#994f34;transform:translateY(-1px)}
    .hero-figure img{width:min(400px, 80vw);height:auto;border-radius:16px;box-shadow:var(--shadow)}

    .impact-section{background:rgba(255,255,255,.9);padding:3rem 1rem;text-align:center}
    .impact-items{display:flex;justify-content:center;gap:1rem;flex-wrap:wrap;margin:0 auto 1.75rem;max-width:1000px}
    .impact-item{background:#fff;padding:1rem 1.25rem;border-radius:10px;box-shadow:0 2px 6px rgba(0,0,0,.08);min-width:140px;font-family:"Proxima Nova", sans-serif;font-weight:400}
    .impact-media img{width:60%;height:auto;border-radius:14px;box-shadow:var(--shadow)}

    .image-section{background:#FFF7E1;padding:3rem 1rem;text-align:center;display:none}

    footer{text-align:center;padding:1.5rem;background:var(--cw-blue);color:#fff;margin-top:2rem;font-family:"Proxima Nova", sans-serif;font-weight:400}
    @media (max-width: 860px){.hero{grid-template-columns:1fr;gap:1.5rem;text-align:center}}
  </style>
</head>
<body>
  <nav class="navbar">
    <div class="logo">
      <img src="img/cw_logo-2.png" alt="charity: water logo">
    </div>
    <ul class="nav-links">
      <li>
        <a href="#action">Take Action
          <svg viewBox="0 0 24 24"><path d="M6 9l6 6 6-6"/></svg>
        </a>
        <div class="dropdown">
          <a href="#donate">Donate</a>
          <a href="#fundraise">Fundraise</a>
          <a href="#campaigns">Campaigns</a>
        </div>
      </li>
      <li>
        <a href="#about">About Us
          <svg viewBox="0 0 24 24"><path d="M6 9l6 6 6-6"/></svg>
        </a>
        <div class="dropdown">
          <a href="#our-story">Our Story</a>
          <a href="#team">Team</a>
          <a href="#financials">Financials</a>
        </div>
      </li>
      <li><a href="#why">Why Water?</a></li>
    </ul>
    <a href="#signup" class="signup-btn">Sign Up</a>
  </nav>

  <header class="hero">
    <div class="hero-text">
      <h1>Change lives with clean water—and watch it happen</h1>
      <p>We make giving easy and transparent, with 100% of your donation funding real projects you can follow from start to finish.</p>
      <div class="hero-buttons">
        <a href="#donate" class="btn btn-primary">Donate Today!</a>
        <a href="#impact" class="btn btn-secondary">See Your Impact</a>
      </div>
    </div>
    <figure class="hero-figure">
      <img src="img/gallery1.png" alt="Community celebrating access to clean water" />
    </figure>
  </header>

  <section class="impact-section" id="impact">
    <h2 style="font-weight:400;font-family:'Proxima Nova', sans-serif;">Water impacts every area of life</h2>
    <div class="impact-items">
      <div class="impact-item">Health</div>
      <div class="impact-item">Education</div>
      <div class="impact-item">Women</div>
      <div class="impact-item">Economic Growth</div>
    </div>
    <div class="impact-media">
      <img src="img/gallery2.png" alt="Children collecting safe water together" />
    </div>
  </section>

  <footer>
    <p>&copy; 2025 charity: water. All rights reserved.</p>
  </footer>
</body>
</html>
