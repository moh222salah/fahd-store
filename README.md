herepython3 - << 'PYEOF'
remaining = '''-height:1;margin-bottom:16px">
        <span style="background:linear-gradient(135deg,var(--t1),var(--t2));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text">Gulf-Native.</span>
        <span style="font-family:var(--fi);background:linear-gradient(135deg,var(--g),var(--g2));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;font-size:1.15em"> Globally Ready.</span>
      </h2>
      <p style="font-size:17px;color:var(--t2);max-width:580px;margin:0 auto;line-height:1.9;font-weight:300">Engineered for Gulf culture. Deployed with international standards. Every payment method Gulf consumers trust — live and certified.</p>
    </div>

    <div class="marquee-wrap">
      <div class="marquee-track">
        <div class="m-pill">💳 Mada</div><div class="m-pill">📱 STC Pay</div><div class="m-pill">🍎 Apple Pay</div><div class="m-pill">🔄 Tabby</div><div class="m-pill">✨ Tamara</div><div class="m-pill">💰 Visa</div><div class="m-pill">💳 Mastercard</div><div class="m-pill">🌍 PayPal</div><div class="m-pill">📜 ZATCA e-Invoice</div><div class="m-pill">🏦 Bank Transfer</div>
        <div class="m-pill">💳 Mada</div><div class="m-pill">📱 STC Pay</div><div class="m-pill">🍎 Apple Pay</div><div class="m-pill">🔄 Tabby</div><div class="m-pill">✨ Tamara</div><div class="m-pill">💰 Visa</div><div class="m-pill">💳 Mastercard</div><div class="m-pill">🌍 PayPal</div><div class="m-pill">📜 ZATCA e-Invoice</div><div class="m-pill">🏦 Bank Transfer</div>
      </div>
    </div>

    <div class="market-map rv">
      <div class="mc"><div class="mc-flag">🇸🇦</div><div class="mc-name">Saudi Arabia</div><div class="mc-status live">● Primary Market</div></div>
      <div class="mc"><div class="mc-flag">🇦🇪</div><div class="mc-name">UAE</div><div class="mc-status exp">● Expanding</div></div>
      <div class="mc"><div class="mc-flag">🇰🇼</div><div class="mc-name">Kuwait</div><div class="mc-status road">● On Roadmap</div></div>
      <div class="mc"><div class="mc-flag">🇶🇦</div><div class="mc-name">Qatar</div><div class="mc-status road">● On Roadmap</div></div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════════════
     FINAL CTA
════════════════════════════════════════════════ -->
<section class="final">
  <div class="cta-box rv">
    <div class="cta-eyebrow">🤝 Let\'s Build Together</div>
    <h2>Ready to <span class="gc">Launch</span><br/>Your Gulf Platform?</h2>
    <p>From concept to full production in 45–60 days. Full-stack, mobile-first, AI-powered, ZATCA-compliant. Let\'s build something the Gulf has never seen.</p>
    <div class="cta-btns">
      <a href="https://moh222salah.github.io/cv" target="_blank" class="cta-gold" style="font-size:14px;padding:16px 36px">💼 View Full Portfolio →</a>
      <a href="https://wa.me/201113903070" target="_blank" class="cta-wa" style="font-size:14px;padding:16px 36px">💬 WhatsApp Direct →</a>
    </div>
    <div class="cta-contacts">
      <div class="cta-c">💼 <a href="https://moh222salah.github.io/cv" target="_blank">moh222salah.github.io/cv</a></div>
      <div class="cta-c">💬 <a href="https://wa.me/201113903070" target="_blank">wa.me/201113903070</a></div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer class="footer">
  <div class="foot-logo">Fahd Store</div>
  <div class="foot-txt">Luxury Gulf E-Commerce Platform — Built with Royal Precision</div>
  <div class="foot-v">v1.0.0 · 2025</div>
</footer>

</div><!-- /page -->

<script>
/* ─── CUSTOM CURSOR ─── */
const cur = document.getElementById('cur');
const cur2 = document.getElementById('cur2');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{
  mx=e.clientX; my=e.clientY;
  cur.style.left=mx+'px'; cur.style.top=my+'px';
});
(function ani(){
  rx+=(mx-rx)*.1; ry+=(my-ry)*.1;
  cur2.style.left=rx+'px'; cur2.style.top=ry+'px';
  requestAnimationFrame(ani);
})();

/* ─── PARTICLES CANVAS ─── */
(function(){
  const c=document.getElementById('particles');
  const ctx=c.getContext('2d');
  let W,H,pts=[];
  function resize(){W=c.width=innerWidth;H=c.height=innerHeight}
  resize(); window.addEventListener('resize',resize);
  function rand(a,b){return Math.random()*(b-a)+a}
  for(let i=0;i<55;i++){
    pts.push({
      x:rand(0,innerWidth),y:rand(0,innerHeight),
      vx:rand(-.18,.18),vy:rand(-.18,.18),
      r:rand(.6,2.2),
      o:rand(.06,.35),
      g:Math.random()>.6
    });
  }
  function draw(){
    ctx.clearRect(0,0,W,H);
    pts.forEach(p=>{
      p.x+=p.vx; p.y+=p.vy;
      if(p.x<-5)p.x=W+5; if(p.x>W+5)p.x=-5;
      if(p.y<-5)p.y=H+5; if(p.y>H+5)p.y=-5;
      ctx.beginPath();
      ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
      ctx.fillStyle=p.g?`rgba(201,168,76,${p.o})`:`rgba(240,230,200,${p.o*.5})`;
      ctx.fill();
    });
    // Draw delicate connecting lines between nearby gold particles
    const gpts=pts.filter(p=>p.g);
    for(let i=0;i<gpts.length;i++){
      for(let j=i+1;j<gpts.length;j++){
        const dx=gpts[i].x-gpts[j].x, dy=gpts[i].y-gpts[j].y;
        const dist=Math.sqrt(dx*dx+dy*dy);
        if(dist<140){
          ctx.beginPath();
          ctx.strokeStyle=`rgba(201,168,76,${.08*(1-dist/140)})`;
          ctx.lineWidth=.5;
          ctx.moveTo(gpts[i].x,gpts[i].y);
          ctx.lineTo(gpts[j].x,gpts[j].y);
          ctx.stroke();
        }
      }
    }
    requestAnimationFrame(draw);
  }
  draw();
})();

/* ─── SCROLL REVEAL ─── */
const obs = new IntersectionObserver(entries=>{
  entries.forEach((e,i)=>{
    if(e.isIntersecting){
      setTimeout(()=>e.target.classList.add('in'), i*70);
    }
  });
},{threshold:0.07});
document.querySelectorAll('.rv,.rvl,.rvr,.rv2').forEach(el=>obs.observe(el));

/* ─── ECOSYSTEM TABS ─── */
function switchEco(idx, el){
  document.querySelectorAll('.eco-tab').forEach(t=>t.classList.remove('on'));
  el.classList.add('on');
  document.querySelectorAll('.eco-panel').forEach((p,i)=>p.classList.toggle('on',i===idx));
  // Re-trigger reveal for new panel cards
  document.querySelectorAll('#ep'+idx+' .rv2').forEach((c,i)=>{
    c.classList.remove('in');
    setTimeout(()=>c.classList.add('in'),i*100+50);
  });
}

/* ─── COUNTER ANIMATION ─── */
const counterObs = new IntersectionObserver(entries=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      const el = e.target;
      const target = parseFloat(el.getAttribute('data-target'));
      const suffix = el.getAttribute('data-suffix')||'';
      let start=0; const dur=1800; const step=16;
      const inc = target/(dur/step);
      el.innerHTML='0<span class="stat-suf">'+suffix+'</span>';
      const timer = setInterval(()=>{
        start+=inc;
        if(start>=target){
          clearInterval(timer);
          el.innerHTML=target+'<span class="stat-suf">'+suffix+'</span>';
        } else {
          el.innerHTML=Math.floor(start)+'<span class="stat-suf">'+suffix+'</span>';
        }
      },step);
      counterObs.unobserve(el);
    }
  });
},{threshold:.5});
document.querySelectorAll('[data-target]').forEach(el=>counterObs.observe(el));

/* ─── BAR ANIMATION ─── */
document.querySelectorAll('.dbar-fill').forEach(bar=>{
  const w = bar.style.width;
  bar.style.width='0%';
  const barObs = new IntersectionObserver(entries=>{
    if(entries[0].isIntersecting){
      setTimeout(()=>bar.style.width=w, 300);
      barObs.unobserve(bar);
    }
  },{threshold:.3});
  barObs.observe(bar);
});

/* ─── ACTIVE NAV HIGHLIGHT ─── */
window.addEventListener('scroll',()=>{
  document.querySelectorAll('section[id]').forEach(sec=>{
    const rect=sec.getBoundingClientRect();
    if(rect.top<=150&&rect.bottom>=150){
      // could highlight nav if needed
    }
  });
});

/* ─── HOVER MAGIC on stat boxes ─── */
document.querySelectorAll('.stat-box').forEach(b=>{
  b.addEventListener('mouseenter',()=>b.style.background='rgba(201,168,76,.03)');
  b.addEventListener('mouseleave',()=>b.style.background='');
});
</script>
</body>
</html>'''

with open('/home/claude/fahd-store/README.html','a',encoding='utf-8') as f:
    f.write(remaining)

content = open('/home/claude/fahd-store/README.html',encoding='utf-8').read()
checks = {
  'Has DOCTYPE': '<!DOCTYPE html>' in content,
  'Closes HTML': '</html>' in content,
  'Has hero section': 'hero-main' in content,
  'Has overview section': 'overview-head' in content,
  'Has features bento': 'feat-bento' in content,
  'Has ecosystem tabs': 'eco-tabs' in content,
  'Has journey section': 'journey-grid' in content,
  'Has marquee': 'marquee-track' in content,
  'Has final CTA': 'cta-box' in content,
  'Has particles canvas': 'particles' in content,
  'Has counter animation': 'data-target' in content,
  'Has scroll reveal': 'IntersectionObserver' in content,
  'Has custom cursor': "id='cur'" in content,
  'Has WhatsApp link': 'wa.me/201113903070' in content,
  'Has portfolio link': 'moh222salah.github.io/cv' in content,
  'Has Arabic text': 'فهد ستور' in content,
  'Has delivery bars': 'dbar-fill' in content,
  'Has payment stack': 'pay-stack' in content,
  'Has loyalty tiers': 'tier-name' in content,
  'Has AI visual': 'ai-visual' in content,
}
ok = True
for k,v in checks.items():
    status = '✅' if v else '❌'
    if not v: ok = False
    print(f"{status} {k}")
print(f"\n{'All passed!' if ok else 'SOME FAILED'}")
print(f"Size: {len(content)} bytes ({len(content)//1024} KB)")
PYEOF
