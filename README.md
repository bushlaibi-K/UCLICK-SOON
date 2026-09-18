<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>U Click — Coming Soon</title>
<meta name="description" content="U Click — custom 3D-printed keychains, fidget clickers, and more. Designed on screen, printed to order in Bahrain.">
<meta property="og:title" content="U Click — Coming Soon">
<meta property="og:description" content="Custom 3D-printed pieces, designed on screen, printed to order in Bahrain.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://uclick.bh">
<link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🎨</text></svg>">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@600;700;800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#FFF9EF;--ink:#1A1A2E;--ink-soft:#4A4A5A;--ink-faint:#8E8E9A;
    --blue:#2D5FE5;--blue-deep:#1B3FA0;--blue-tint:#E0EAFF;
    --orange:#F5922A;--orange-tint:#FFF0DC;
    --teal:#22B8C9;--teal-tint:#D8F6FA;
    --red:#E04545;--yellow:#FFD23F;--green:#4BB462;
    --line:#E9E0C9;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html,body{height:100%;}
  body{
    background:var(--paper);color:var(--ink);
    font-family:'Inter',-apple-system,sans-serif;
    -webkit-font-smoothing:antialiased;
    display:flex;flex-direction:column;align-items:center;justify-content:center;
    min-height:100vh;padding:32px 24px;text-align:center;
    position:relative;overflow:hidden;
  }
  h1,h2,h3{font-family:'Baloo 2',sans-serif;font-weight:700;letter-spacing:-0.01em;}
  body::before,body::after{
    content:"";position:fixed;border-radius:50%;opacity:.12;pointer-events:none;z-index:0;
  }
  body::before{width:420px;height:420px;background:var(--blue);top:-120px;right:-100px;}
  body::after{width:340px;height:340px;background:var(--orange);bottom:-80px;left:-80px;}
  .bg-teal{
    position:fixed;width:260px;height:260px;border-radius:50%;background:var(--teal);
    opacity:.08;top:50%;left:60%;pointer-events:none;z-index:0;
  }
  .content{position:relative;z-index:1;max-width:520px;}
  .logo-wrap{margin-bottom:28px;}
  .logo-wrap img{height:140px;width:auto;margin:0 auto;display:block;filter:drop-shadow(0 8px 24px rgba(0,0,0,0.08));}
  h1{font-size:clamp(28px,5vw,42px);line-height:1.1;margin-bottom:10px;}
  h1 .blue{color:var(--blue);}
  h1 .orange{color:var(--orange);}
  .tagline{font-size:clamp(15px,2.5vw,17px);color:var(--ink-soft);line-height:1.6;max-width:40ch;margin:0 auto 32px;}
  .dots{display:flex;justify-content:center;gap:8px;margin-bottom:32px;}
  .dot{width:14px;height:14px;border-radius:50%;animation:pulse 2.4s ease-in-out infinite;}
  .dot:nth-child(1){background:var(--blue);animation-delay:0s;}
  .dot:nth-child(2){background:var(--orange);animation-delay:0.3s;}
  .dot:nth-child(3){background:var(--teal);animation-delay:0.6s;}
  .dot:nth-child(4){background:var(--red);animation-delay:0.9s;}
  .dot:nth-child(5){background:var(--yellow);animation-delay:1.2s;}
  .dot:nth-child(6){background:var(--green);animation-delay:1.5s;}
  @keyframes pulse{
    0%,100%{transform:scale(1);opacity:1;}
    50%{transform:scale(1.4);opacity:.7;}
  }
  .cta-row{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-bottom:28px;}
  .btn{
    display:inline-flex;align-items:center;gap:9px;
    padding:14px 24px;border-radius:14px;font-weight:700;font-size:15px;
    border:none;text-decoration:none;
  }
  .btn-wa{background:#25D366;color:#fff;box-shadow:0 4px 0 #1DA851;}
  .btn-wa:hover{background:#20c05c;}
  .btn-ig{background:var(--ink);color:var(--paper);box-shadow:0 4px 0 var(--blue-deep);}
  .btn-ig:hover{background:#2a2a42;}
  .btn svg{width:18px;height:18px;flex-shrink:0;}
  .notify{margin-bottom:32px;}
  .notify p{font-size:13.5px;color:var(--ink-soft);margin-bottom:10px;font-weight:600;}
  .notify-form{display:flex;gap:8px;max-width:380px;margin:0 auto;}
  .notify-form input{
    flex:1;padding:12px 14px;border-radius:12px;border:1.5px solid var(--line);
    background:var(--paper);font-family:inherit;font-size:14px;color:var(--ink);min-width:0;
  }
  .notify-form input:focus{outline:none;border-color:var(--blue);}
  .notify-form button{
    padding:12px 20px;border-radius:12px;background:var(--blue);color:#fff;
    font-weight:700;font-size:14px;border:none;white-space:nowrap;
    box-shadow:0 3px 0 var(--blue-deep);
  }
  .notify-form button:hover{background:#2450CC;}
  .thankyou{display:none;font-size:14px;color:var(--green);font-weight:700;margin-top:8px;}
  .cards{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-bottom:32px;}
  .card{
    background:rgba(255,255,255,0.7);border:1px solid var(--line);border-radius:14px;
    padding:14px 18px;font-size:13px;color:var(--ink-soft);line-height:1.5;
    display:flex;align-items:center;gap:10px;
  }
  .card .ic{font-size:20px;flex-shrink:0;}
  .foot{font-size:12px;color:var(--ink-faint);margin-top:8px;}
  .foot a{color:var(--blue);font-weight:600;}
  .lang{
    position:absolute;top:20px;right:24px;z-index:2;
    display:flex;border:1.5px solid var(--line);border-radius:999px;overflow:hidden;
    font-size:12.5px;font-weight:700;
  }
  .lang span{padding:6px 12px;cursor:pointer;}
  .lang .active{background:var(--ink);color:var(--paper);}
  .ar{display:none;direction:rtl;text-align:center;}
  body.rtl .ar{display:block;}
  body.rtl .en{display:none;}
  body.rtl{direction:rtl;}
  body.rtl .lang{left:24px;right:auto;}
  @media(max-width:480px){
    .notify-form{flex-direction:column;}
    .cards{flex-direction:column;align-items:center;}
    .cta-row{flex-direction:column;align-items:center;}
  }
  @media(prefers-reduced-motion:reduce){.dot{animation:none!important;}}
</style>
</head>
<body>
<div class="bg-teal"></div>
<div class="lang" id="langToggle">
  <span class="active" data-lang="en">EN</span>
  <span data-lang="ar">عربي</span>
</div>
<div class="content">
  <div class="logo-wrap">
    <img src="/logo.png" alt="U Click logo" onerror="this.outerHTML='<div style=\'font-family:Baloo 2;font-size:48px;font-weight:800;color:#2D5FE5;margin-bottom:8px;\'>U Click</div>'">
  </div>
  <div class="en">
    <h1>Something <span class="orange">colorful</span> is <span class="blue">coming</span></h1>
    <p class="tagline">Custom 3D-printed keychains, fidget clickers, and more — designed on your screen, printed to order, delivered to your door in Bahrain.</p>
  </div>
  <div class="ar">
    <h1>شي <span class="orange">ملوّن</span> <span class="blue">يجيكم</span> قريب</h1>
    <p class="tagline">ميداليات وألعاب فيدجيت مطبوعة بتقنية ثلاثية الأبعاد — صمّمها على شاشتك، ونطبعها ونوصّلها لعندك في البحرين.</p>
  </div>
  <div class="dots">
    <div class="dot"></div><div class="dot"></div><div class="dot"></div>
    <div class="dot"></div><div class="dot"></div><div class="dot"></div>
  </div>
  <div class="cta-row">
    <a href="https://wa.me/97333XXXXXX" class="btn btn-wa" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.118.553 4.108 1.519 5.838L0 24l6.336-1.652A11.95 11.95 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.75c-1.97 0-3.837-.53-5.445-1.453l-.39-.226-3.766.983.999-3.657-.25-.397A9.72 9.72 0 012.25 12 9.75 9.75 0 0112 2.25 9.75 9.75 0 0121.75 12 9.75 9.75 0 0112 21.75z"/></svg>
      <span class="en">WhatsApp us</span><span class="ar">تواصل معانا</span>
    </a>
    <a href="https://instagram.com/uclick.bh" class="btn btn-ig" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="5"/><circle cx="17.5" cy="6.5" r="1.5" fill="currentColor" stroke="none"/></svg>
      <span class="en">@uclick.bh</span><span class="ar">@uclick.bh</span>
    </a>
  </div>
  <div class="notify">
    <p class="en">Get notified when we launch:</p>
    <p class="ar">خلنا نعلمك يوم نفتح:</p>
    <form class="notify-form" id="notifyForm">
      <input type="email" placeholder="your@email.com" required id="emailInput" aria-label="Email address">
      <button type="submit"><span class="en">Notify me</span><span class="ar">عَلّمني</span></button>
    </form>
    <div class="thankyou" id="thankyou">
      <span class="en">✓ You're on the list — we'll email you launch day.</span>
      <span class="ar">✓ سجّلناك — بنرسلك إيميل يوم الإطلاق.</span>
    </div>
  </div>
  <div class="cards">
    <div class="card"><span class="ic">🎨</span><span class="en">Live 3D customizer</span><span class="ar">صمّم بالـ 3D مباشر</span></div>
    <div class="card"><span class="ic">🧵</span><span class="en">Real filament colors</span><span class="ar">ألوان فيلامنت حقيقية</span></div>
    <div class="card"><span class="ic">🚚</span><span class="en">Delivered across Bahrain</span><span class="ar">توصيل لكل البحرين</span></div>
  </div>
  <div class="foot">
    <span class="en">© 2026 U Click · Bahrain · <a href="mailto:info@uclick.bh">info@uclick.bh</a></span>
    <span class="ar">© 2026 U Click · البحرين · <a href="mailto:info@uclick.bh">info@uclick.bh</a></span>
  </div>
</div>
<script>
  document.getElementById('langToggle').addEventListener('click', function(e){
    var t = e.target.closest('[data-lang]');
    if (!t) return;
    var lang = t.dataset.lang;
    this.querySelectorAll('span').forEach(function(s){ s.classList.toggle('active', s.dataset.lang === lang); });
    document.body.classList.toggle('rtl', lang === 'ar');
  });
  document.getElementById('notifyForm').addEventListener('submit', function(e){
    e.preventDefault();
    var email = document.getElementById('emailInput').value;
    console.log('Notify signup:', email);
    this.style.display = 'none';
    document.getElementById('thankyou').style.display = 'block';
  });
</script>
</body>
</html>
uclick-coming-soon.html)
