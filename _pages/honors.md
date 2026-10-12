---
layout: page
title: Honors
permalink: /honors/
nav: true
nav_order: 3
_styles: |
  .honors-list .honor-entry {
    display: grid;
    grid-template-columns: 190px minmax(0, 1fr);
    align-items: center;
    gap: 28px;
    padding: 28px 0;
    border-bottom: 1px solid var(--global-divider-color);
  }
  .honors-list .honor-entry:first-child { padding-top: 8px; }
  .honors-list .honor-entry:last-child { border-bottom: 0; }
  .honors-list .honor-preview { display: block; }
  .honors-list .honor-preview img {
    display: block;
    width: 100%;
    height: auto;
    border: 1px solid var(--global-divider-color);
    border-radius: 4px;
  }
  .honors-list .honor-entry h2 { font-size: 1.3rem; line-height: 1.4; margin: 0 0 10px; }
  .honors-list .honor-conference { color: var(--global-text-color-light); margin-bottom: 12px; }
  .honors-list .honor-description { font-style: italic; margin-bottom: 14px; }
  .honors-list .honor-description q { quotes: none; }
  .honors-list .honor-preview:focus-visible { outline: 2px solid var(--global-theme-color); outline-offset: 4px; }
  @media (max-width: 575px) {
    .honors-list .honor-entry { grid-template-columns: minmax(0, 1fr); gap: 20px; }
    .honors-list .honor-preview { width: 170px; }
  }
---

<div class="honors-list">
  <section class="honor-entry" aria-labelledby="icig-honor">
    <a class="honor-preview" href="{{ '/assets/pdf/honors/icig-2026.pdf' | relative_url }}" aria-label="View ICIG 2026 award certificate (PDF)">
      <img src="{{ '/assets/img/honors/icig-2026.png' | relative_url }}" alt="ICIG 2026 Best Student Paper Honorable Mention certificate" width="1273" height="1800" loading="lazy">
    </a>
    <div>
      <h2 id="icig-honor">Best Student Paper Honorable Mention</h2>
      <p class="honor-conference">The 14th International Conference on Image and Graphics (ICIG), 2026</p>
      <p class="honor-description">MVFM-3DAD: Multi-view Flow Matching for 3D Anomaly Detection via Density Proxy Estimation</p>
      <a href="{{ '/assets/pdf/honors/icig-2026.pdf' | relative_url }}">View certificate (PDF)</a>
    </div>
  </section>
  <section class="honor-entry" aria-labelledby="neurips-honor">
    <a class="honor-preview" href="{{ '/assets/pdf/honors/neurips-2026.pdf' | relative_url }}" aria-label="View NeurIPS 2026 reviewer recognition letter (PDF)">
      <img src="{{ '/assets/img/honors/neurips-2026.png' | relative_url }}" alt="NeurIPS 2026 letter recognizing Hanzhe Liang as Top Reviewer" width="1391" height="1800" loading="lazy">
    </a>
    <div>
      <h2 id="neurips-honor">Top Reviewer</h2>
      <p class="honor-conference">Conference on Neural Information Processing Systems (NeurIPS), 2026</p>
      <p class="honor-description"><q>Their reviews were instrumental in maintaining the scholarly standards of the conference</q></p>
      <a href="{{ '/assets/pdf/honors/neurips-2026.pdf' | relative_url }}">View certificate (PDF)</a>
    </div>
  </section>
</div>
