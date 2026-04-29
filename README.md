<svg width="900" height="200" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0d1117;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#161b22;stop-opacity:1" />
    </linearGradient>
    <linearGradient id="textGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#58a6ff;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#79c0ff;stop-opacity:1" />
    </linearGradient>
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <style>
      .title {
        font-family: 'Courier New', monospace;
        font-size: 52px;
        font-weight: 700;
        fill: url(#textGrad);
        filter: url(#glow);
        animation: fadeSlideIn 1.2s ease forwards;
        opacity: 0;
      }
      .subtitle {
        font-family: 'Courier New', monospace;
        font-size: 18px;
        fill: #8b949e;
        animation: fadeSlideIn 1.2s ease 0.4s forwards;
        opacity: 0;
      }
      .cursor {
        fill: #58a6ff;
        animation: blink 1s step-end infinite;
      }
      .dot1 { fill: #ff5f57; }
      .dot2 { fill: #febc2e; }
      .dot3 { fill: #28c840; }
      .bar { fill: #30363d; rx: 12; ry: 12; }
      @keyframes fadeSlideIn {
        0% { opacity: 0; transform: translateY(16px); }
        100% { opacity: 1; transform: translateY(0); }
      }
      @keyframes blink {
        0%, 100% { opacity: 1; }
        50% { opacity: 0; }
      }
      @keyframes scanline {
        0% { transform: translateY(-100%); }
        100% { transform: translateY(200px); }
      }
      .scanline {
        animation: scanline 3s linear infinite;
        opacity: 0.03;
      }
      .grid-line {
        stroke: #58a6ff;
        stroke-opacity: 0.06;
        stroke-width: 1;
      }
    </style>
  </defs>

  <!-- Background -->
  <rect width="900" height="200" fill="url(#bg)" rx="12"/>

  <!-- Subtle grid -->
  <line class="grid-line" x1="0" y1="50" x2="900" y2="50"/>
  <line class="grid-line" x1="0" y1="100" x2="900" y2="100"/>
  <line class="grid-line" x1="0" y1="150" x2="900" y2="150"/>
  <line class="grid-line" x1="150" y1="0" x2="150" y2="200"/>
  <line class="grid-line" x1="300" y1="0" x2="300" y2="200"/>
  <line class="grid-line" x1="450" y1="0" x2="450" y2="200"/>
  <line class="grid-line" x1="600" y1="0" x2="600" y2="200"/>
  <line class="grid-line" x1="750" y1="0" x2="750" y2="200"/>

  <!-- Scanline effect -->
  <rect class="scanline" x="0" y="0" width="900" height="4" fill="#58a6ff"/>

  <!-- Terminal window chrome -->
  <rect x="20" y="18" width="860" height="164" fill="#0d1117" rx="8" stroke="#30363d" stroke-width="1"/>
  <circle class="dot1" cx="40" cy="34" r="5"/>
  <circle class="dot2" cx="57" cy="34" r="5"/>
  <circle class="dot3" cx="74" cy="34" r="5"/>
  <line x1="20" y1="46" x2="880" y2="46" stroke="#30363d" stroke-width="1"/>

  <!-- Terminal prompt line -->
  <text x="38" y="78" font-family="'Courier New', monospace" font-size="13" fill="#28c840">agrim@dev</text>
  <text x="107" y="78" font-family="'Courier New', monospace" font-size="13" fill="#8b949e">:</text>
  <text x="115" y="78" font-family="'Courier New', monospace" font-size="13" fill="#58a6ff">~</text>
  <text x="127" y="78" font-family="'Courier New', monospace" font-size="13" fill="#8b949e">$</text>
  <text x="140" y="78" font-family="'Courier New', monospace" font-size="13" fill="#c9d1d9"> whoami</text>

  <!-- Name output -->
  <text class="title" x="38" y="138">Agrim Dubey</text>
  <rect class="cursor" x="330" y="116" width="3" height="28" rx="1"/>

  <!-- subtitle -->
  <text class="subtitle" x="38" y="168">CS Student · Backend Dev · Full-Stack · Always Building</text>
</svg>
