<style>
*{box-sizing:border-box;margin:0;padding:0}
@keyframes fadeUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}
@keyframes pulse{0%,100%{transform:scale(1)}50%{transform:scale(1.15)}}

.wrap{max-width:640px;margin:1.5rem auto;display:flex;flex-direction:column;gap:12px}

.hero{
  background:var(--color-background-primary);
  border:0.5px solid var(--color-border-tertiary);
  border-radius:16px;
  padding:1.75rem 1.75rem 1.5rem;
  animation:fadeUp .5s ease both;
  position:relative;
  overflow:hidden;
}
.hero-accent{
  position:absolute;top:0;left:0;right:0;height:4px;
  background:linear-gradient(90deg,#7F77DD,#5DCAA5,#EF9F27);
}
.hero-top{display:flex;align-items:center;gap:1.25rem;margin-bottom:1.25rem}
.avatar{
  width:72px;height:72px;border-radius:50%;
  background:#EEEDFE;
  border:2px solid #AFA9EC;
  display:flex;align-items:center;justify-content:center;
  font-size:24px;font-weight:500;color:#3C3489;
  flex-shrink:0;
}
.hero-name{
  font-size:22px;font-weight:500;
  color:var(--color-text-primary);
  margin-bottom:2px;
}
.type-line{
  display:flex;align-items:center;gap:6px;
  font-size:13px;color:var(--color-text-secondary);
  height:20px;overflow:hidden;
}
.typer{display:inline-block;min-width:160px}
.cursor{display:inline-block;width:2px;height:13px;background:#7F77DD;border-radius:1px;animation:blink 1s step-end infinite;vertical-align:middle}
.flag-pill{
  display:inline-flex;align-items:center;gap:5px;
  font-size:11px;font-weight:500;
  padding:2px 10px;border-radius:99px;
  background:#E1F5EE;color:#085041;border:0.5px solid #5DCAA5;
  margin-left:auto;
}
.divider{height:0.5px;background:var(--color-border-tertiary);margin:.25rem 0 1rem}

.stat-row{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:1rem}
.stat{
  background:var(--color-background-secondary);
  border-radius:var(--border-radius-md);
  padding:12px 14px;text-align:center;
}
.stat-num{font-size:20px;font-weight:500;color:var(--color-text-primary)}
.stat-lbl{font-size:11px;color:var(--color-text-tertiary);margin-top:2px}

.section-lbl{font-size:11px;font-weight:500;letter-spacing:.06em;text-transform:uppercase;color:var(--color-text-tertiary);margin-bottom:10px}

.badge-row{display:flex;flex-wrap:wrap;gap:7px;margin-bottom:1rem}
.badge{display:inline-flex;align-items:center;gap:5px;font-size:12px;font-weight:500;padding:4px 12px;border-radius:99px;border:0.5px solid}
.b-java{background:#FAEEDA;color:#633806;border-color:#EF9F27}
.b-spring{background:#EAF3DE;color:#27500A;border-color:#97C459}
.b-html{background:#FAECE7;color:#712B13;border-color:#D85A30}
.b-css{background:#E6F1FB;color:#0C447C;border-color:#85B7EB}
.b-js{background:#FAEEDA;color:#854F0B;border-color:#FAC775}
.b-c{background:#EEEDFE;color:#3C3489;border-color:#AFA9EC}

.proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(0,1fr));gap:10px;margin-bottom:1rem}
.proj{
  background:var(--color-background-primary);
  border:0.5px solid var(--color-border-tertiary);
  border-radius:var(--border-radius-md);
  padding:14px;
  text-decoration:none;
  display:block;
  transition:border-color .15s,background .15s;
  cursor:pointer;
}
.proj:hover{border-color:var(--color-border-secondary);background:var(--color-background-secondary)}
.proj-icon{
  width:32px;height:32px;border-radius:8px;
  display:flex;align-items:center;justify-content:center;
  font-size:15px;margin-bottom:10px;
  border:0.5px solid;
}
.pi-purple{background:#EEEDFE;color:#534AB7;border-color:#AFA9EC}
.pi-teal{background:#E1F5EE;color:#0F6E56;border-color:#5DCAA5}
.pi-amber{background:#FAEEDA;color:#854F0B;border-color:#EF9F27}
.pi-coral{background:#FAECE7;color:#993C1D;border-color:#F0997B}
.proj-name{font-size:13px;font-weight:500;color:var(--color-text-primary);margin-bottom:3px}
.proj-desc{font-size:12px;color:var(--color-text-secondary);margin-bottom:8px}
.proj-tag{font-size:11px;padding:2px 8px;border-radius:99px;background:#EEEDFE;color:#3C3489;border:0.5px solid #AFA9EC}
.live-badge{display:inline-flex;align-items:center;gap:4px;font-size:11px;padding:2px 8px;border-radius:99px;background:#EAF3DE;color:#27500A;border:0.5px solid #97C459}
.live-dot{width:6px;height:6px;border-radius:50%;background:#639922;animation:pulse 2s ease-in-out infinite}

.link-row{display:flex;gap:8px;flex-wrap:wrap}
.link-btn{
  display:inline-flex;align-items:center;gap:6px;
  font-size:13px;font-weight:500;
  padding:7px 16px;border-radius:var(--border-radius-md);
  border:0.5px solid var(--color-border-secondary);
  background:transparent;
  color:var(--color-text-primary);
  text-decoration:none;cursor:pointer;
  transition:background .14s;
}
.link-btn:hover{background:var(--color-background-secondary)}
.link-btn i{font-size:15px;color:var(--color-text-secondary)}
.link-btn.primary{background:#EEEDFE;border-color:#AFA9EC;color:#3C3489}
.link-btn.primary i{color:#534AB7}
.link-btn.primary:hover{background:#CECBF6}
</style>

<h2 class="sr-only" style="position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0,0,0,0)">Chand Mandol — CSE student and aspiring software developer profile</h2>

<div class="wrap">

  <div class="hero">
    <div class="hero-accent"></div>

    <div class="hero-top">
      <div class="avatar">CM</div>
      <div style="flex:1;min-width:0">
        <div class="hero-name">Chand Mandol</div>
        <div class="type-line">
          <span class="typer" id="typer"></span>
          <span class="cursor"></span>
          <span class="flag-pill"><i class="ti ti-map-pin" style="font-size:11px" aria-hidden="true"></i>Bangladesh</span>
        </div>
      </div>
    </div>

    <div class="stat-row">
      <div class="stat">
        <div class="stat-num">4</div>
        <div class="stat-lbl">Projects</div>
      </div>
      <div class="stat">
        <div class="stat-num">6+</div>
        <div class="stat-lbl">Tech stack</div>
      </div>
      <div class="stat">
        <div class="stat-num">1</div>
        <div class="stat-lbl">Live app</div>
      </div>
    </div>

    <div class="divider"></div>
    <div class="section-lbl">Tech stack</div>
    <div class="badge-row">
      <span class="badge b-java"><i class="ti ti-coffee" aria-hidden="true"></i>Java</span>
      <span class="badge b-spring"><i class="ti ti-leaf" aria-hidden="true"></i>Spring Boot</span>
      <span class="badge b-html"><i class="ti ti-code" aria-hidden="true"></i>HTML5</span>
      <span class="badge b-css"><i class="ti ti-palette" aria-hidden="true"></i>CSS3</span>
      <span class="badge b-js"><i class="ti ti-brand-javascript" aria-hidden="true"></i>JavaScript</span>
      <span class="badge b-c"><i class="ti ti-cpu" aria-hidden="true"></i>C / C++</span>
    </div>

    <div class="divider"></div>
    <div class="section-lbl">Featured projects</div>
    <div class="proj-grid">

      <a class="proj" href="https://github.com/Chand241/CalculatorChand241" target="_blank">
        <div class="proj-icon pi-amber"><i class="ti ti-calculator" aria-hidden="true"></i></div>
        <div class="proj-name">Calculator</div>
        <div class="proj-desc">Web-based calculator</div>
        <span class="proj-tag">HTML · JS</span>
      </a>

      <a class="proj" href="https://github.com/Chand241/portfolio" target="_blank">
        <div class="proj-icon pi-purple"><i class="ti ti-user" aria-hidden="true"></i></div>
        <div class="proj-name">Portfolio</div>
        <div class="proj-desc">Personal portfolio site</div>
        <span class="proj-tag">HTML · CSS</span>
      </a>

      <a class="proj" href="https://github.com/Chand241/OOP_Spring25" target="_blank">
        <div class="proj-icon pi-coral"><i class="ti ti-school" aria-hidden="true"></i></div>
        <div class="proj-name">OOP Practice</div>
        <div class="proj-desc">Java OOP assignments</div>
        <span class="proj-tag">Java</span>
      </a>

      <a class="proj" href="https://library-management-system-0ksw.onrender.com/" target="_blank" style="border-color:#5DCAA5">
        <div class="proj-icon pi-teal"><i class="ti ti-books" aria-hidden="true"></i></div>
        <div class="proj-name">Smart Library</div>
        <div class="proj-desc">Full-stack LMS</div>
        <span class="live-badge"><span class="live-dot"></span>Live</span>
      </a>

    </div>

    <div class="divider"></div>
    <div class="link-row">
      <a class="link-btn primary" href="https://www.linkedin.com/in/chand-cse/" target="_blank">
        <i class="ti ti-brand-linkedin" aria-hidden="true"></i>LinkedIn
      </a>
      <a class="link-btn" href="https://github.com/Chand241" target="_blank">
        <i class="ti ti-brand-github" aria-hidden="true"></i>GitHub
      </a>
      <a class="link-btn" href="https://library-management-system-0ksw.onrender.com/" target="_blank">
        <i class="ti ti-external-link" aria-hidden="true"></i>Live app
      </a>
    </div>
  </div>

</div>

<script>
const roles = [
  "CSE Student",
  "Java Developer",
  "Web Explorer",
  "Spring Boot Learner",
  "Aspiring Engineer"
];
let ri = 0, ci = 0, deleting = false;
const el = document.getElementById('typer');

function tick() {
  const word = roles[ri];
  if (!deleting) {
    el.textContent = word.slice(0, ++ci);
    if (ci === word.length) { deleting = true; setTimeout(tick, 1400); return; }
    setTimeout(tick, 70);
  } else {
    el.textContent = word.slice(0, --ci);
    if (ci === 0) { deleting = false; ri = (ri + 1) % roles.length; setTimeout(tick, 300); return; }
    setTimeout(tick, 38);
  }
}
tick();
</script>
