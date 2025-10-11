---
layout: single
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<h1>About Me</h1>
<p>
I’m <strong>Shih-Ming He</strong>, an Assistant Professor in the <strong>Department of Electronic Engineering</strong>, Chung Yuan Christian University (CYCU), Taiwan, where I lead the <strong>2D Semiconductor Materials with AI-driven Research &amp; Transfer (2SMART) Lab</strong>.
</p>
<p>
My work bridges <strong>2D semiconductor materials</strong>, <strong>scalable CVD/MOCVD process development</strong>, and <strong>large-area transfer techniques</strong> toward reliable device integration.
</p>

<hr>

<h1>At a glance</h1>
<ul>
  <li>Built and tuned <strong>CVD/MOCVD</strong> platforms for <strong>wafer-scale 2D materials</strong></li>
  <li>Focus on <strong>transfer reliability</strong> &amp; <strong>process reproducibility</strong> for manufacturing</li>
  <li>Interested in <strong>AI-driven synthesis</strong> and <strong>autonomous process optimization</strong></li>
</ul>
<blockquote>
  Caring about turning lab-scale breakthroughs into <strong>robust, scalable processes</strong> that teams can actually build on.
</blockquote>

<hr>

<div style="margin:28px 0;">
  <div style="background:#fafafa;border:1px solid #eee;border-radius:12px;padding:16px;box-shadow:0 1px 4px rgba(0,0,0,0.05);">
    <h3 style="text-align:center;margin-top:0;">Citations: Yearly (bars) + Cumulative (line)</h3>
    <canvas id="citationsCombo" style="width:100%;height:360px;"></canvas>
  </div>
</div>

<script>
  // 實際數據（2016–2025）
  const years = ['2016','2017','2018','2019','2020','2021','2022','2023','2024','2025'];
  const citesPerYear = [4, 24, 19, 20, 31, 34, 43, 48, 37, 39];
  const cumulative = citesPerYear.reduce((a,v,i)=>{ a.push((a[i-1]||0)+v); return a; },[]);

  function renderCitationCombo() {
    const el = document.getElementById('citationsCombo');
    if (!el || !window.Chart) return;
    const ctx = el.getContext('2d');
    new Chart(ctx, {
      data: {
        labels: years,
        datasets: [
          {
            type: 'bar',
            label: 'Citations / Year',
            data: citesPerYear,
            backgroundColor: '#cfd9f2',
            borderColor: '#9bb4ea'
          },
          {
            type: 'line',
            label: 'Cumulative Citations',
            data: cumulative,
            borderColor: '#4A90E2',
            backgroundColor: 'rgba(74,144,226,0.10)',
            fill: true,
            tension: 0.3,
            pointRadius: 3
          }
        ]
      },
      options: {
        responsive: true,
        interaction: { mode: 'index', intersect: false },
        scales: {
          y: { beginAtZero: true, title: { display: true, text: 'Citations' } },
          x: { title: { display: true, text: 'Year' } }
        },
        plugins: { legend: { position: 'bottom' } }
      }
    });
  }
</script>

<!-- 關鍵：載 UMD 版（非 ESM），載入完成後再呼叫 render -->
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.3/dist/chart.umd.min.js"
        onload="renderCitationCombo()"></script>

<h1>Life Timeline</h1>
<div class="timeline">
  <div class="tl-item">
    <div class="tl-date">2025.08.01</div>
    <div class="tl-content">Joined the Department of Electronic Engineering, Chung Yuan Christian University, Taiwan, as Assistant Professor</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2025.05.01</div>
    <div class="tl-content">Left the Research Laboratory of Electronics (RLE), Massachusetts Institute of Technology, USA</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2024.12.01</div>
    <div class="tl-content">Awarded Postdoctoral Research Abroad Fellowship from National Science and Technology Council, Taiwan</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2023.10.01</div>
    <div class="tl-content">Joined the Research Laboratory of Electronics (RLE), Massachusetts Institute of Technology, USA, as a Postdoctoral Associate</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2023.09.01</div>
    <div class="tl-content">Left the Optical Sciences Center, National Central University, Taiwan</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2023.04.27</div>
    <div class="tl-content">Joined the Optical Sciences Center, National Central University, Taiwan, as Postdoctoral Research Fellow</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2022.12.06</div>
    <div class="tl-content">Completed one-year alternative military service at Tainan Education and Nursing Institute, Taiwan</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2022.01.03</div>
    <div class="tl-content">Began one-year alternative military service at Tainan Education and Nursing Institute, Taiwan</div>
  </div>
  
  <div class="tl-item">
    <div class="tl-date">2021.11.27</div>
    <div class="tl-content">Earned Ph.D. in Energy Engineering, National Central University, Taiwan</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2019.12.01</div>
    <div class="tl-content">Awarded Graduate Students Study Abroad Fellowship from Ministry of Science and Technology, Taiwan; hosted by the Department of Electrical Engineering and Computer Science, Massachusetts Institute of Technology</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2017.07.17</div>
    <div class="tl-content">Visited Rutherford Appleton Laboratory (UK) for a two-week collaboration</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2016.11.15</div>
    <div class="tl-content">Visited Shizuoka University, Japan, for a one-week academic exchange</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2016.09.01</div>
    <div class="tl-content">Admitted to direct Ph.D. program in Energy Engineering, National Central University, Taiwan</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2015.07.13</div>
    <div class="tl-content">Participated in a two-week academic exchange program at Hiroshima University, Japan</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2014.09.01</div>
    <div class="tl-content">Began M.S. studies in Energy Engineering at National Central University, Taiwan</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2014.07.24</div>
    <div class="tl-content">Completed an 18-day round-island cycling trip in Taiwan</div>
  </div>
  
  <div class="tl-item">
    <div class="tl-date">2014.07.07</div>
    <div class="tl-content">Began round-island cycling trip in Taiwan</div>
  </div>

  <div class="tl-item">
    <div class="tl-date">2014.06.30</div>
    <div class="tl-content">Graduated with B.S. in Physics, Fu Jen Catholic University, Taiwan</div>
  </div>
  
  <div class="tl-item">
    <div class="tl-date">2010.09.01</div>
    <div class="tl-content">Began undergraduate studies in Physics at Fu Jen Catholic University, Taiwan</div>
  </div>
</div>

<!-- Style -->
<style>
/* Timeline */
.timeline { border-left: 3px solid #9aa0a6; margin: 24px 0; padding-left: 20px; }
.tl-item { margin: 16px 0; position: relative; }
.tl-item::before {
  content: ""; width: 12px; height: 12px; background: #9aa0a6; border-radius: 50%;
  position: absolute; left: -27px; top: 6px;
}
.tl-date { font-weight: 700; color: #e67e22; margin-bottom: 4px; }
.tl-content { line-height: 1.7; }

/* Spacing & mobile tweaks */
blockquote { margin: 12px 0 0 0; }
@media (max-width: 640px) {
  .timeline { padding-left: 16px; }
  .tl-item::before { left: -24px; }
  .tl-date { display: block; margin-bottom: 2px; }
}
</style>

<hr>

<blockquote><em>Never say never. Everything happened with meaning.</em></blockquote>

<hr>
