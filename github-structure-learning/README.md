<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">

  <!-- ========== DEFINITIONS ========== -->
  <defs>
    <!-- Subtle glow -->
    <filter id="softGlow">
      <feGaussianBlur stdDeviation="6" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Gradient Accent -->
    <linearGradient id="accentGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#F05032"/>
      <stop offset="100%" stop-color="#ff7b54"/>
    </linearGradient>

    <linearGradient id="blueGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#58a6ff"/>
      <stop offset="100%" stop-color="#79c0ff"/>
    </linearGradient>
  </defs>

  <!-- ========== MAIN DARK TILE ========== -->
  <rect x="56" y="56" width="400" height="400" rx="90"
        fill="#0d1117"/>

  <!-- Subtle border -->
  <rect x="56" y="56" width="400" height="400" rx="90"
        fill="none" stroke="#1f2933" stroke-width="3"/>

  <!-- ========== REPOSITORY FOLDER ========== -->
  <rect x="150" y="185" width="212" height="140" rx="18"
        fill="#161b22" stroke="#30363d" stroke-width="2"/>

  <rect x="150" y="165" width="120" height="40" rx="12"
        fill="#161b22" stroke="#30363d" stroke-width="2"/>

  <!-- ========== GIT BRANCH STRUCTURE ========== -->

  <!-- Main vertical branch -->
  <line x1="256" y1="140" x2="256" y2="310"
        stroke="url(#accentGrad)"
        stroke-width="6"
        stroke-linecap="round"
        filter="url(#softGlow)"/>

  <!-- Left feature branch -->
  <path d="M256 210 Q210 210 210 245"
        fill="none"
        stroke="url(#blueGrad)"
        stroke-width="5"
        stroke-linecap="round"/>

  <!-- Right merge branch -->
  <path d="M256 245 Q300 245 300 210"
        fill="none"
        stroke="url(#blueGrad)"
        stroke-width="5"
        stroke-linecap="round"/>

  <!-- Commit Nodes -->
  <circle cx="256" cy="150" r="10" fill="url(#accentGrad)" filter="url(#softGlow)"/>
  <circle cx="256" cy="210" r="10" fill="url(#accentGrad)" filter="url(#softGlow)"/>
  <circle cx="256" cy="270" r="10" fill="url(#accentGrad)" filter="url(#softGlow)"/>

  <circle cx="210" cy="245" r="8" fill="#58a6ff"/>
  <circle cx="300" cy="210" r="8" fill="#58a6ff"/>

  <!-- Merge arrow indicator -->
  <polygon points="290,200 315,210 290,220"
           fill="#58a6ff"/>

  <!-- ========== TERMINAL ACCENT ========== -->
  <rect x="180" y="340" width="152" height="36" rx="10"
        fill="#11161c" stroke="#30363d" stroke-width="1.5"/>

  <text x="195" y="363"
        font-family="monospace"
        font-size="16"
        fill="#F05032">$</text>

  <text x="215" y="363"
        font-family="monospace"
        font-size="14"
        fill="#58a6ff">git push</text>

  <!-- ========== TITLE TEXT ========== -->
  <text x="256" y="120"
        font-family="Arial Black, sans-serif"
        font-size="34"
        text-anchor="middle"
        fill="#ffffff"
        letter-spacing="4">
    GIT
  </text>

</svg>