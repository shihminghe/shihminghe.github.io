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

<!--Citation Chart starts here-->

<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.3/dist/chart.umd.min.js"></script>
<script>
  // 資料
  const years = ['2016','2017','2018','2019','2020','2021','2022','2023','2024','2025'];
  const citesPerYear = [4,24,19,20,31,34,43,48,37,39];
  const cumulative = citesPerYear.reduce((a,v,i)=>{ a.push((a[i-1]||0)+v); return a; }, []);

  // 自訂：在柱上方（與可選的折線點）畫數字
  const valueLabelPlugin = {
    id: 'valueLabel',
    afterDatasetsDraw(chart, args, opts) {
      const {ctx} = chart;
      ctx.save();
      ctx.textAlign = 'center';
      ctx.textBaseline = 'bottom';
      ctx.fillStyle = opts.color || '#475569';
      ctx.font = `${opts.fontSize || 12}px system-ui, -apple-system, Segoe UI, Arial`;

      chart.data.datasets.forEach((ds, dsIndex) => {
        const meta = chart.getDatasetMeta(dsIndex);
        // 只在柱子上方顯示；若也要線上顯示，把條件拿掉並在下面判斷
        meta.data.forEach((elem, i) => {
          if (!elem) return;
          // bar
          if ((ds.type || chart.config.type) === 'bar' && opts.showBarLabels !== false) {
            const val = ds.data[i];
            ctx.fillText(val, elem.x, elem.y - 4);
          }
          // line（可選）
          if ((ds.type || chart.config.type) === 'line' && opts.showLineLabels) {
            const val = ds.data[i];
            ctx.fillText(val, elem.x, elem.y - 8);
          }
        });
      });
      ctx.restore();
    }
  };

  Chart.register(valueLabelPlugin);

  // 畫圖
  const ctx = document.getElementById('citationsCombo').getContext('2d');
  new Chart(ctx, {
    data: {
      labels: years,
      datasets: [
        {
          type: 'bar',
          label: 'Citations / Year',
          data: citesPerYear,
          backgroundColor: '#d9e3ff',
          borderColor: '#9ab4ff'
        },
        {
          type: 'line',
          label: 'Cumulative',
          data: cumulative,
          borderColor: '#3b82f6',
          backgroundColor: 'rgba(59,130,246,0.12)',
          fill: true,
          tension: 0.4,
          pointRadius: 3,
          borderWidth: 2
        }
      ]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,   // ← 讓高度跟著外層 div
      interaction: { mode: 'index', intersect: false },
      datasets: { bar: { borderRadius: 8, barThickness: 'flex' } }, // 圓角＆自適應寬
      scales: {
        y: { beginAtZero: true, title: { display: true, text: 'Citations' },
             grid: { color: 'rgba(0,0,0,0.06)' } },
        x: { title: { display: true, text: 'Year' }, ticks: { maxRotation: 0 } }
      },
      plugins: {
        legend: { position: 'bottom' },
        // 啟用我們的數字插件並可調樣式
        valueLabel: { color: '#334155', fontSize: 12, showBarLabels: true, showLineLabels: false }
      }
    }
  });
</script>

<!--Citation Chart ends here-->

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
