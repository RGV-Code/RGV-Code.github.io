<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rocco Given Visagie</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --navy:#0a1628;--navy2:#0f1f3d;--navy3:#1a2f54;
  --orange:#ff6b00;--orange2:#ff8c33;
  --orange-dim:rgba(255,107,0,0.12);--orange-dim2:rgba(255,107,0,0.06);
  --black:#07090f;--white:#f4f4f0;--muted:#8a9bbf;--muted2:#b8c6e0;
  --border:rgba(255,107,0,0.18);--border2:rgba(255,255,255,0.08);
  --fh:'Bebas Neue',sans-serif;--fm:'JetBrains Mono',monospace;--fb:'Inter',sans-serif;
}
body{background:var(--black);color:var(--white);font-family:var(--fb);line-height:1.65;overflow-x:hidden}
.wrap{max-width:880px;margin:0 auto;padding:64px 36px}
.hero{display:grid;grid-template-columns:1fr 180px;gap:40px;align-items:center;margin-bottom:72px;opacity:0;transform:translateY(24px);animation:up 0.7s ease forwards}
.hero-eyebrow{font-family:var(--fm);font-size:11px;color:var(--orange);letter-spacing:0.2em;text-transform:uppercase;margin-bottom:16px;display:flex;align-items:center;gap:10px}
.hero-eyebrow::before{content:'';width:28px;height:1px;background:var(--orange)}
.hero h1{font-family:var(--fh);font-size:clamp(52px,8vw,88px);line-height:0.92;letter-spacing:0.02em;color:var(--white);margin-bottom:20px}
.hero h1 em{color:var(--orange);font-style:normal}
.bio{font-size:15px;color:var(--muted2);max-width:460px;line-height:1.8;margin-bottom:28px;font-style:italic}
.pills{display:flex;flex-wrap:wrap;gap:10px}
.pill{display:flex;align-items:center;gap:7px;padding:7px 14px;background:var(--navy2);border:1px solid var(--border);border-radius:100px;font-family:var(--fm);font-size:11px;color:var(--muted2);text-decoration:none;transition:all 0.2s}
.pill:hover{border-color:var(--orange);color:var(--orange)}
.pill-dot{width:5px;height:5px;border-radius:50%;background:var(--orange);flex-shrink:0}
.pill-li{display:flex;align-items:center;gap:7px;padding:7px 14px;background:#0a66c2;border:1px solid #0a66c2;border-radius:100px;font-family:var(--fm);font-size:11px;color:#fff;text-decoration:none;transition:all 0.2s}
.pill-li:hover{background:#0856a0;border-color:#0856a0}
.pill-li svg{width:12px;height:12px;fill:#fff;flex-shrink:0}
.av-wrap{width:160px;height:160px;border-radius:50%;padding:3px;background:conic-gradient(var(--orange),var(--navy3),var(--orange));flex-shrink:0}
.av-inner{width:100%;height:100%;border-radius:50%;background:var(--navy2);border:2px solid var(--navy);display:flex;align-items:center;justify-content:center;font-family:var(--fh);font-size:40px;letter-spacing:0.04em;color:var(--orange)}
.banner{display:flex;align-items:center;gap:10px;padding:14px 20px;background:var(--orange-dim2);border:1px solid var(--border);border-radius:10px;margin-bottom:72px;font-family:var(--fm);font-size:12px;color:var(--orange2)}
.blink{width:8px;height:8px;border-radius:50%;background:var(--orange);animation:blink 2s ease infinite;flex-shrink:0}
.sec{margin-bottom:68px;opacity:0;transform:translateY(16px)}
.sec.vis{animation:up 0.55s ease forwards}
.sec-head{font-family:var(--fm);font-size:10px;color:var(--orange);letter-spacing:0.22em;text-transform:uppercase;margin-bottom:28px;display:flex;align-items:center;gap:14px}
.sec-head::after{content:'';flex:1;height:1px;background:linear-gradient(to right,var(--border),transparent)}
.sk-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:14px}
.sk{background:var(--navy2);border:1px solid var(--border2);border-radius:12px;padding:18px;transition:border-color 0.2s,transform 0.2s}
.sk:hover{border-color:var(--border);transform:translateY(-2px)}
.sk-cat{font-family:var(--fm);font-size:10px;color:var(--orange);letter-spacing:0.12em;text-transform:uppercase;margin-bottom:6px}
.sk-name{font-family:var(--fb);font-size:15px;font-weight:600;color:var(--white);margin-bottom:4px}
.sk-desc{font-size:12px;color:var(--muted)}
.bar-track{height:2px;background:rgba(255,255,255,0.08);border-radius:2px;margin-top:14px;overflow:hidden}
.bar-fill{height:100%;border-radius:2px;background:linear-gradient(90deg,var(--orange),var(--orange2));width:0;transition:width 1.3s cubic-bezier(0.4,0,0.2,1)}
.tl{padding-left:24px;border-left:2px solid var(--navy3);position:relative}
.tl-item{position:relative;margin-bottom:36px}
.tl-item::before{content:'';position:absolute;left:-30px;top:5px;width:10px;height:10px;border-radius:50%;background:var(--orange);border:2px solid var(--black)}
.tl-item:first-child::before{box-shadow:0 0 0 4px rgba(255,107,0,0.15)}
.tl-co{font-family:var(--fb);font-size:17px;font-weight:600;color:var(--white)}
.tl-role{font-size:13px;color:var(--muted2);font-style:italic;margin:2px 0 5px}
.tl-date{font-family:var(--fm);font-size:11px;color:var(--orange);letter-spacing:0.06em}
.edu-grid{display:grid;grid-template-columns:1fr 1fr;gap:18px}
.edu{background:var(--navy2);border:1px solid var(--border2);border-radius:14px;padding:26px;position:relative;overflow:hidden;transition:border-color 0.2s}
.edu:hover{border-color:var(--border)}
.edu-accent{position:absolute;top:0;left:0;right:0;height:3px;background:var(--orange)}
.edu-accent.navy{background:var(--navy3)}
.edu-inst{font-family:var(--fb);font-size:15px;font-weight:600;color:var(--white);margin-bottom:6px}
.edu-deg{font-size:13px;color:var(--muted2);font-style:italic;margin-bottom:14px}
.edu-badge{display:inline-block;padding:4px 12px;border-radius:100px;font-family:var(--fm);font-size:10px;letter-spacing:0.07em;background:var(--orange-dim);border:1px solid var(--border);color:var(--orange2)}
.edu-badge.done{background:rgba(10,22,40,0.6);border-color:rgba(255,255,255,0.12);color:var(--muted2)}
.loc-box{background:var(--navy2);border:1px solid var(--border2);border-left:3px solid var(--orange);border-radius:0 12px 12px 0;padding:24px 28px;font-family:var(--fm);font-size:13px;color:var(--muted2);line-height:2.1}
.ref-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}
.ref{background:var(--navy2);border:1px solid var(--border2);border-radius:12px;padding:20px;transition:border-color 0.2s}
.ref:hover{border-color:var(--border)}
.ref-av{width:42px;height:42px;border-radius:50%;background:var(--navy3);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-family:var(--fh);font-size:15px;color:var(--orange);margin-bottom:12px}
.ref-name{font-family:var(--fb);font-size:14px;font-weight:600;color:var(--white);margin-bottom:4px}
.ref-ph{font-family:var(--fm);font-size:11px;color:var(--muted)}
.li-banner{display:flex;align-items:center;justify-content:space-between;gap:16px;padding:18px 24px;background:#0a1f3d;border:1px solid #0a66c2;border-radius:12px;margin-top:28px}
.li-banner-left{display:flex;align-items:center;gap:12px}
.li-banner-left svg{width:24px;height:24px;fill:#0a66c2;flex-shrink:0}
.li-banner-text{font-family:var(--fm);font-size:12px;color:var(--muted2)}
.li-banner-text strong{color:var(--white);display:block;margin-bottom:2px;font-size:13px}
.li-btn{display:inline-flex;align-items:center;gap:7px;padding:9px 18px;background:#0a66c2;border-radius:100px;font-family:var(--fm);font-size:11px;color:#fff;text-decoration:none;white-space:nowrap;transition:background 0.2s}
.li-btn:hover{background:#0856a0}
.li-btn svg{width:11px;height:11px;fill:#fff}
.footer{border-top:1px solid var(--border2);padding-top:40px;text-align:center}
.footer-q{font-size:14px;font-style:italic;color:var(--muted);margin-bottom:14px}
.footer-m{font-family:var(--fm);font-size:10px;color:var(--muted);letter-spacing:0.16em}
.footer-o{color:var(--orange)}
@keyframes up{to{opacity:1;transform:translateY(0)}}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0.4}}
@media(max-width:600px){
  .hero{grid-template-columns:1fr}.av-wrap{display:none}
  .edu-grid{grid-template-columns:1fr}.ref-grid{grid-template-columns:1fr}
  .wrap{padding:36px 18px}
  .li-banner{flex-direction:column;align-items:flex-start}
}
</style>
</head>
<body>
<div class="wrap">

  <div class="hero">
    <div>
      <div class="hero-eyebrow">Full Stack Developer</div>
      <h1>ROCCO GIVEN<br><em>VISAGIE</em></h1>
      <p class="bio">Passionate about building digital experiences that are visually compelling, intuitive, and a joy to use — bridging design and development, one clean line of code at a time.</p>
      <div class="pills">
        <a href="mailto:220343527@mycput.ac.za" class="pill"><span class="pill-dot"></span>220343527@mycput.ac.za</a>
        <a href="tel:+27609208354" class="pill"><span class="pill-dot"></span>060 920 8354</a>
        <div class="pill"><span class="pill-dot"></span>Cape Town, ZA</div>
        <a href="https://www.linkedin.com/in/rocco-given-visagie-597717312/" target="_blank" class="pill-li">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          LinkedIn
        </a>
      </div>
    </div>
    <div class="av-wrap"><div class="av-inner">RGV</div></div>
  </div>

  <div class="banner">
    <div class="blink"></div>
    Final Year · Diploma: ICT in Applications Development · CPUT, District Six · Open to Opportunities
  </div>

  <div class="sec" id="s1">
    <div class="sec-head">Technical Skills</div>
    <div class="sk-grid">
      <div class="sk"><div class="sk-cat">Backend</div><div class="sk-name">Java</div><div class="sk-desc">Scalable, clean OOP code</div><div class="bar-track"><div class="bar-fill" data-w="85"></div></div></div>
      <div class="sk"><div class="sk-cat">Frontend</div><div class="sk-name">JavaScript</div><div class="sk-desc">Dynamic, interactive UIs</div><div class="bar-track"><div class="bar-fill" data-w="78"></div></div></div>
      <div class="sk"><div class="sk-cat">Design</div><div class="sk-name">UX / UI Design</div><div class="sk-desc">User-centred experiences</div><div class="bar-track"><div class="bar-fill" data-w="80"></div></div></div>
      <div class="sk"><div class="sk-cat">QA</div><div class="sk-name">Debugging</div><div class="sk-desc">Systematic diagnostics</div><div class="bar-track"><div class="bar-fill" data-w="75"></div></div></div>
      <div class="sk"><div class="sk-cat">Research</div><div class="sk-name">Usability Testing</div><div class="sk-desc">Evidence-based decisions</div><div class="bar-track"><div class="bar-fill" data-w="72"></div></div></div>
      <div class="sk"><div class="sk-cat">Planning</div><div class="sk-name">Project Management</div><div class="sk-desc">On-time delivery</div><div class="bar-track"><div class="bar-fill" data-w="70"></div></div></div>
    </div>
  </div>

  <div class="sec" id="s2">
    <div class="sec-head">Work Experience</div>
    <div class="tl">
      <div class="tl-item"><div class="tl-co">Capita Call Centre</div><div class="tl-role">Customer Experience Advisor — Marks &amp; Spencer Campaign</div><div class="tl-date">June 2022 – January 2024</div></div>
      <div class="tl-item"><div class="tl-co">Deli Den Urban Farmhouse</div><div class="tl-role">Cashier / Merchandiser / Sales Assistant</div><div class="tl-date">2022</div></div>
      <div class="tl-item"><div class="tl-co">Footgear – Access Park</div><div class="tl-role">Sales Associate</div><div class="tl-date">2021</div></div>
      <div class="tl-item"><div class="tl-co">Dis-Chem</div><div class="tl-role">Cashier / Merchandiser</div><div class="tl-date">2019</div></div>
      <div class="tl-item"><div class="tl-co">Ignite Events Company</div><div class="tl-role">Bartender / Waiter</div><div class="tl-date">2016</div></div>
      <div class="tl-item" style="margin-bottom:0"><div class="tl-co">Spur Steak Ranches</div><div class="tl-role">Waiter</div><div class="tl-date">2015</div></div>
    </div>
  </div>

  <div class="sec" id="s3">
    <div class="sec-head">Education</div>
    <div class="edu-grid">
      <div class="edu"><div class="edu-accent"></div><div class="edu-inst">Cape Peninsula University of Technology</div><div class="edu-deg">Diploma: ICT in Applications Development · District Six Campus</div><span class="edu-badge">Final Year · Current</span></div>
      <div class="edu"><div class="edu-accent navy"></div><div class="edu-inst">De Kuilen High School</div><div class="edu-deg">National Senior Certificate — Bachelor's Pass</div><span class="edu-badge done">Completed 2015</span></div>
    </div>
  </div>

  <div class="sec" id="s4">
    <div class="sec-head">Location</div>
    <div class="loc-box">26 Kameeldoring Street<br>Rouxville, Kuilsriver<br>Cape Town, 7580<br>South Africa</div>
  </div>

  <div class="sec" id="s5">
    <div class="sec-head">References</div>
    <div class="ref-grid">
      <div class="ref"><div class="ref-av">PH</div><div class="ref-name">Phillip Human</div><div class="ref-ph">083 395 8662</div></div>
      <div class="ref"><div class="ref-av">RH</div><div class="ref-name">Ronisha Hendricks</div><div class="ref-ph">064 032 2039</div></div>
    </div>
  </div>

  <div class="sec" id="s6">
    <div class="sec-head">Connect</div>
    <div class="li-banner">
      <div class="li-banner-left">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        <div class="li-banner-text">
          <strong>Rocco Given Visagie</strong>
          linkedin.com/in/rocco-given-visagie-597717312
        </div>
      </div>
      <a href="https://www.linkedin.com/in/rocco-given-visagie-597717312/" target="_blank" class="li-btn">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        View Profile
      </a>
    </div>
  </div>

  <div class="footer">
    <p class="footer-q">"Crafting seamless end-to-end solutions that balance aesthetic detail with technical integrity."</p>
    <div class="footer-m">ROCCO GIVEN VISAGIE <span class="footer-o">·</span> CAPE TOWN <span class="footer-o">·</span> OPEN TO OPPORTUNITIES</div>
  </div>

</div>
<script>
const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.classList.add('vis');
      e.target.querySelectorAll('.bar-fill').forEach(b=>{
        setTimeout(()=>{b.style.width=b.dataset.w+'%'},250);
      });
      obs.unobserve(e.target);
    }
  });
},{threshold:0.1});
document.querySelectorAll('.sec').forEach(s=>obs.observe(s));
</script>
</body>
<video width="640" height="360" controls>
  <source src="InterviewProjectPresentationFinalVideoCompress.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
