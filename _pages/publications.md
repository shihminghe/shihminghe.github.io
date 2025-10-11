---
layout: single
permalink: /publications/
author_profile: true
---

---
layout: single
permalink: /publications/
author_profile: true
---

<div style="display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; margin-bottom: 40px;">
  <div style="flex: 1 1 48%; min-width: 300px;">
    <h3 style="text-align:center;">Citations per Year</h3>
    <canvas id="citationChart"></canvas>
  </div>
  <div style="flex: 1 1 48%; min-width: 300px;">
    <h3 style="text-align:center;">Publications per Year</h3>
    <canvas id="pubChart"></canvas>
  </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
document.addEventListener('DOMContentLoaded', function () {
  // === Citation Chart (Left) ===
  const citationCtx = document.getElementById('citationChart').getContext('2d');
  new Chart(citationCtx, {
    type: 'line',
    data: {
      labels: ['2015','2016','2017','2018','2019','2020','2021','2022','2023','2024','2025'],
      datasets: [{
        label: 'Citations',
        data: [0, 5, 12, 25, 40, 60, 95, 130, 180, 240, 300],
        borderColor: '#4A90E2',
        backgroundColor: 'rgba(74,144,226,0.15)',
        fill: true,
        tension: 0.25,
        pointRadius: 3
      }]
    },
    options: {
      scales: {
        y: { beginAtZero: true, title: { display: true, text: 'Citations' } },
        x: { title: { display: true, text: 'Year' } }
      },
      plugins: {
        legend: { display: false }
      }
    }
  });

  // === Publications Chart (Right) ===
  const pubCtx = document.getElementById('pubChart').getContext('2d');
  new Chart(pubCtx, {
    type: 'bar',
    data: {
      labels: ['2015','2016','2017','2018','2019','2020','2021','2022','2023','2024','2025'],
      datasets: [
        {
          label: 'Journal Papers',
          data: [0,2,0,0,2,1,1,2,0,1,2],
          backgroundColor: '#D6B89C'
        },
        {
          label: 'Conference Papers',
          data: [0,1,2,1,3,1,1,1,0,0,0],
          backgroundColor: '#A8B695'
        },
        {
          label: 'Technical Reports',
          data: [1,1,0,0,0,0,0,0,0,0,0],
          backgroundColor: '#8392A7'
        }
      ]
    },
    options: {
      responsive: true,
      scales: {
        y: { beginAtZero: true, title: { display: true, text: 'Publications' } },
        x: { title: { display: true, text: 'Year' } }
      },
      plugins: {
        legend: { position: 'bottom' }
      }
    }
  });
});
</script>

Publications
======

**2025**  
- <b>Beyond Seamless: Unexpected Defective Merging in Single-Orientation Graphene</b><br>
  <i><u>arXiv preprint arXiv:2509.21908</u></i> [cond-mat.mtrl-sci] (2025)<br>
  Zhien Wang, Jiangtao Wang&#42;, Diego Exposito, Andrey Krayev, <b>Shih-Ming He</b>, Xudong Zheng, Zachariah Hennighausen, Ivan Brihuega, Se-Young Jeong&#42;, Jing Kong&#42;<br>
  <a href="https://doi.org/10.48550/arXiv.2509.21908" target="_blank">https://doi.org/10.48550/arXiv.2509.21908</a>

- <b>A Novel Surface-Enhanced Raman Spectroscopy (SERS)-Based Strategy for Rapid and Sensitive Detection of NRR Products Using Janus WSSe/WS₂ Heterostructures</b><br>
  <i><u>Chemical Engineering Journal</u></i>, 522, 166830 (2025) <br>
  Yu-Ren Peng, Tianyi Zhang, Tilo H. Yang, Shin-Yi Tang, <b>Shih-Ming He</b>, Pei-Husan Wang, Tzi-Yi Yang, Hung-Ti Chen, Shih-Syuan Huang, Yuan-Chun Chen, Hao-Chung Kuo, Jing Kong&#42;, Yu-Lun Chueh&#42;<br>
  <a href="https://doi.org/10.1016/j.cej.2025.166830" target="_blank">https://doi.org/10.1016/j.cej.2025.166830</a>

**2024**  
- <b>Plasma-Driven Selenization for Electrical Property Enhancement in Janus 2D Materials</b><br>
  <i><u>Small Methods</u></i>, 8, 2400150 (2024) <br>
  <b>Shih-Ming He</b>, Jia-Yung Zhuang, Ciao-Fen Chen, Ren-Kuei Liao, Shun-Tsung Lo, Yen-Fu Lin&#42;, Ching-Yuan Su&#42;<br>
  <span style="color:#e67e22; font-weight:600">&#9733; Selected as Front Cover</span><br>
  <a href="https://doi.org/10.1002/smtd.202400150" target="_blank">https://doi.org/10.1002/smtd.202400150</a><br>
  <img src="/images/sm.jpg" alt="Front Cover" style="max-width:250px; margin-top:6px;">

**2022**  
- <b>Wrinkle-Free Graphene Films on Fluorinated Self-Assembled Monolayer-Modified Substrates for Enhancing the Electrical Performance of Transistors</b><br>
  <i><u>ACS Applied Nano Materials</u></i>, 5 (4), 5793–5802 (2022)<br>
  <b>Shih-Ming He</b>, Hsin-Yin Lin, Chia-Jou Shen, Ching-Yuan Su&#42;<br>
  <a href="https://doi.org/10.1021/acsanm.2c00918" target="_blank">https://doi.org/10.1021/acsanm.2c00918</a>

- <b>Robustness of large-area suspended graphene under interaction with intense laser</b><br>
  <i><u>Scientific Reports</u></i>, 12 (1), 2346 (2022) <br>
  Y. Kuramitsu&#42;, T. Minami, T. Hihara, K. Sakai, T. Nishimoto, S. Isayama, Y. T. Liao, K. T. Wu, W. Y. Woon&#42;, S. H. Chen, Y. L. Liu, <b>S. M. He</b>, C. Y. Su, D. Farley, C. Baird, W. Trickey, C. Murphy, K. Lancaster, J. Green, J. Pasley, N. Booth, C. Spindloe, A. Hughes, R. Heathcote, T. Nishimoto, H. Habara, M. Ota, S. Egashira, A. Morace, Y. Sakawa, R. Kodama, M. Koenig, M. Kanasaki, K. Morii, T. Asai, K. Sakamoto, K. Shimizu, T. Yamauchi, K. Oda, K. Kondo, H. Kiriyama, Y. Fukuda, and N. Woolsey<br>
  <span style="color:#e67e22; font-weight:600">&#9733; Collection of "Top 100 in Physics in 2022" (Rank: 11/100)</span><br>
  <a href="https://doi.org/10.1038/s41598-022-06055-4" target="_blank">https://doi.org/10.1038/s41598-022-06055-4</a>

**2021**  
- <b>Toward large-scale CVD graphene growth by enhancing reaction kinetics via an efficient interdiffusion mediator and mechanism study utilizing CFD simulations</b><br>
  <i><u>Journal of the Taiwan Institute of Chemical Engineers</u></i>, 128, 400–408 (2021)<br>
  <b>Shih-Ming He</b>, Zhi-Long Lin, Wei-Jie Lin, Kai-Xiang Xu, Yi-Hsien Chen, Jyh-Chen Chen, Ching-Yuan Su&#42;<br>
  <a href="https://doi.org/10.1016/j.jtice.2021.08.035" target="_blank">https://doi.org/10.1016/j.jtice.2021.08.035</a>

- <b>Graphene under extreme electromagnetic field: energetic ion acceleration by direct irradiation of ultra intense laser on few layer suspended graphene</b><br>
  <i><u>Research Square, Preprint, Version 1, posted 17 Jun.</u></i> (2021)<br>
  Yasuhiro Kuramitsu, Takumi Minami, Takamasa Hihara, Kentaro Sakai, Takahiro Nishimoto, Shogo Isayama, Yu-Tzu Liao, Kuan-Ting Wu, Wei-Yen Woon, Shih-Hung Chen, Yao-Li Liu, <b>Shih-Ming He</b>, Ching-Yuan Su, Masato Ota, Shunsuke Egashira, Alessio Morace, Youichi Sakawa, Hideaki Habara, Ryosuke Kodama, Leonard Dohl, Nigel Woolsey, Michel Koenig, Masato Kanasaki, Takafumi Asai, Tomoya Yamauchi, Keiji Oda, Kotaro Kondo, Hiromitsu Kiriyama, Yuji Fukuda<br>
  <a href="https://doi.org/10.21203/rs.3.rs-373515/v1" target="_blank">https://doi.org/10.21203/rs.3.rs-373515/v1</a>
  

**2020**  
- <b>Designed catalytic protocol for enhancing HER performance of P, N-co-doped graphene: The correlation of manipulating the dopants allocations and heteroatomic structure</b><br>
  <i><u>Journal of Physical Chemistry C</u></i>, 124 (47), 25701–25711 (2020)<br>
  Wei-Ting Chen, Dipak Dutta, Yu-Han Hung, Yu-Yu Sin, <b>Shih-Ming He</b>, Jeng-Kuei Chang, Ching-Yuan Su&#42;<br>
  <a href="https://doi.org/10.1021/acs.jpcc.0c07467" target="_blank">https://doi.org/10.1021/acs.jpcc.0c07467</a>

**2019**  
- <b>Spectroscopic and electrical characterizations of low-damage phosphorous-doped graphene via ion implantation</b><br>
  <i><u>ACS Applied Materials & Interfaces</u></i>, 11 (50), 47289–47298 (2019)<br>
  <b>Shih-Ming He</b>, Cheng-Chun Huang, Jhe-Wei Liou, Wei-Yen Woon&#42;, Chin-Yuan Su&#42;<br>
  <a href="https://doi.org/10.1021/acsami.9b18479" target="_blank">https://doi.org/10.1021/acsami.9b18479</a>

- <b>Nano-Catalyst Assisted Pore-structure Fine Tailoring of Holey-graphene for High Performance Energy Storage</b><br>
  <i><u>ACS Applied Materials & Interfaces</u></i>, 11 (40), 36560–36570 (2019)<br>
  Dipak Dutta, Jian-Yong Jiang, Anif Jamaluddin, <b>Shih-Ming He</b>, Yu-Han Hung, Fuming Chen, Jeng-Kuei Chang, Ching-Yuan Su&#42;<br>
  <a href="https://doi.org/10.1021/acsami.9b09927" target="_blank">https://doi.org/10.1021/acsami.9b09927</a>

**2016**  
- <b>Ultra-large suspended graphene as highly elastic membrane for capacitive pressure sensor</b><br>
  <i><u>Nanoscale</u></i>, 8 (6), 3555–3564 (2016)<br>
  Yu-Min Chen, <b>Shih-Ming He</b>, Chi-Hsien Huang, Cheng-Chun Huang, Wen-Pin Shih, Chun-Lin Chu, Jing Kong, Ju Li, Ching-Yuan Su&#42;<br>
  <a href="https://doi.org/10.1039/C5NR08668J" target="_blank">https://doi.org/10.1039/C5NR08668J</a>

- <b>Wide-range work-function tuning of active graphene transparent electrodes via hole doping</b><br>
  <i><u>RSC Advances</u></i>, 6 (39), 32746–32756 (2016)<br>
  Jheng-Yuan Syu, Yu-Min Chen, Kai-Xiang Xu, <b>Shih-Ming He</b>, Wu-Ching Hung, Chien-Liang Chang, Ching-Yuan Su&#42;<br>
  <a href="https://doi.org/10.1039/C6RA04449B" target="_blank">https://doi.org/10.1039/C6RA04449B</a>

<hr class="bold">

Conference Paper
======
**2022**  
- <b>Heteroepitaxy of III-nitrides on polycrystalline and amorphous substrates</b><br>
  <i><u>Proceedings Volume PC12001, Gallium Nitride Materials and Devices XVII</u></i>; PC1200108 (2022)<br>
  <i>Event: SPIE OPTO, 2022, San Francisco, California, USA</i><br>
  Muzafar Rather, Loganathan Ravi, <b>Shih-Ming He</b>, Chao-Chia Cheng, Ching-Yuan Su, Jen-Inn Chyi<br>
  <a href="https://doi.org/10.1117/12.2608062" target="_blank">https://doi.org/10.1117/12.2608062</a>

<hr class="bold">

Technical Reports
======
**2016**  
- <b>Application and Prospect of Graphene Nanoribbon</b><br>
  <i><u>NDL Communications</u></i><br>
  <b>Shih-Ming He</b>, Ching-Yuan Su  

**2015**  
- <b>The Synthesis Technology for Large-Area and High-Quality Graphene Film</b><br>
  <i><u>Journal of the Vacuum Society of the R.O.C.</u></i><br>
  <b>Shih-Ming He</b>, Ching-Yuan Su  

<hr class="bold">
