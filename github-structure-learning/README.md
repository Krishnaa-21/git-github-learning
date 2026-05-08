<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 400" width="1200" height="400">

  <!-- ── Background ── -->
  <defs>
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%"   stop-color="#0d1117"/>
      <stop offset="50%"  stop-color="#0d1117"/>
      <stop offset="100%" stop-color="#161b22"/>
    </linearGradient>

    <linearGradient id="orangeGlow" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#F05032" stop-opacity="0"/>
      <stop offset="50%"  stop-color="#F05032" stop-opacity="0.15"/>
      <stop offset="100%" stop-color="#F05032" stop-opacity="0"/>
    </linearGradient>

    <linearGradient id="blueGlow" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#58a6ff" stop-opacity="0"/>
      <stop offset="50%"  stop-color="#58a6ff" stop-opacity="0.1"/>
      <stop offset="100%" stop-color="#58a6ff" stop-opacity="0"/>
    </linearGradient>

    <linearGradient id="lineGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#F05032" stop-opacity="0"/>
      <stop offset="40%"  stop-color="#F05032" stop-opacity="1"/>
      <stop offset="70%"  stop-color="#58a6ff" stop-opacity="1"/>
      <stop offset="100%" stop-color="#58a6ff" stop-opacity="0"/>
    </linearGradient>

    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="softGlow">
      <feGaussianBlur stdDeviation="8" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <!-- Base background -->
  <rect width="1200" height="400" fill="url(#bgGrad)"/>

  <!-- Ambient glow overlays -->
  <ellipse cx="300" cy="200" rx="350" ry="180" fill="url(#orangeGlow)" opacity="0.6"/>
  <ellipse cx="900" cy="200" rx="350" ry="180" fill="url(#blueGlow)"   opacity="0.6"/>

  <!-- Grid lines horizontal -->
  <line x1="0" y1="100" x2="1200" y2="100" stroke="#ffffff" stroke-width="0.3" opacity="0.05"/>
  <line x1="0" y1="200" x2="1200" y2="200" stroke="#ffffff" stroke-width="0.3" opacity="0.05"/>
  <line x1="0" y1="300" x2="1200" y2="300" stroke="#ffffff" stroke-width="0.3" opacity="0.05"/>

  <!-- Grid lines vertical -->
  <line x1="200"  y1="0" x2="200"  y2="400" stroke="#ffffff" stroke-width="0.3" opacity="0.04"/>
  <line x1="400"  y1="0" x2="400"  y2="400" stroke="#ffffff" stroke-width="0.3" opacity="0.04"/>
  <line x1="600"  y1="0" x2="600"  y2="400" stroke="#ffffff" stroke-width="0.3" opacity="0.04"/>
  <line x1="800"  y1="0" x2="800"  y2="400" stroke="#ffffff" stroke-width="0.3" opacity="0.04"/>
  <line x1="1000" y1="0" x2="1000" y2="400" stroke="#ffffff" stroke-width="0.3" opacity="0.04"/>

  <!-- ── LEFT: Git Branch Graph ── -->

  <!-- Main branch line (vertical) -->
  <line x1="80" y1="60" x2="80" y2="340"
        stroke="#F05032" stroke-width="2.5" stroke-linecap="round" opacity="0.9"/>

  <!-- Feature branch line -->
  <path d="M 80 140 Q 130 140 130 180 L 130 260 Q 130 300 80 300"
        fill="none" stroke="#58a6ff" stroke-width="2" stroke-linecap="round" opacity="0.8"/>

  <!-- Hotfix branch -->
  <path d="M 80 100 Q 155 100 155 130 L 155 170 Q 155 200 80 200"
        fill="none" stroke="#3fb950" stroke-width="1.8" stroke-linecap="round" opacity="0.7"/>

  <!-- Commit nodes on main -->
  <circle cx="80" cy="80"  r="7" fill="#F05032" filter="url(#glow)"/>
  <circle cx="80" cy="140" r="7" fill="#F05032" filter="url(#glow)"/>
  <circle cx="80" cy="200" r="7" fill="#F05032" filter="url(#glow)"/>
  <circle cx="80" cy="260" r="7" fill="#F05032" filter="url(#glow)"/>
  <circle cx="80" cy="300" r="6" fill="#F05032" filter="url(#glow)"/>
  <circle cx="80" cy="340" r="7" fill="#F05032" filter="url(#glow)"/>

  <!-- Commit nodes on feature branch -->
  <circle cx="130" cy="200" r="6" fill="#58a6ff" filter="url(#glow)"/>
  <circle cx="130" cy="240" r="6" fill="#58a6ff" filter="url(#glow)"/>

  <!-- Commit nodes on hotfix -->
  <circle cx="155" cy="150" r="5" fill="#3fb950" filter="url(#glow)"/>

  <!-- Commit labels -->
  <text x="95"  y="84"  font-family="monospace" font-size="9" fill="#8b949e">main</text>
  <text x="143" y="204" font-family="monospace" font-size="9" fill="#58a6ff">feat</text>
  <text x="163" y="154" font-family="monospace" font-size="9" fill="#3fb950">fix</text>

  <!-- Merge label -->
  <rect x="52" y="325" width="56" height="18" rx="4" fill="#F05032" opacity="0.15"/>
  <text x="80" y="337" font-family="monospace" font-size="9" fill="#F05032"
        text-anchor="middle">MERGE</text>

  <!-- ── CENTER: Main Text Block ── -->

  <!-- Top accent line -->
  <rect x="320" y="105" width="560" height="1.5" rx="1"
        fill="url(#lineGrad)" opacity="0.8"/>

  <!-- Pre-title badge -->
  <rect x="530" y="120" width="140" height="22" rx="11"
        fill="#F05032" opacity="0.12" stroke="#F05032" stroke-width="1" stroke-opacity="0.4"/>
  <text x="600" y="135" font-family="Arial, sans-serif" font-size="10"
        fill="#F05032" text-anchor="middle" letter-spacing="3" font-weight="bold">
    DEVELOPER ROADMAP
  </text>

  <!-- Main Title -->
  <text x="600" y="195"
        font-family="Arial Black, Impact, sans-serif"
        font-size="46"
        fill="#ffffff"
        text-anchor="middle"
        font-weight="900"
        letter-spacing="-1"
        filter="url(#softGlow)">
    Git &amp; GitHub
  </text>

  <text x="600" y="248"
        font-family="Arial Black, Impact, sans-serif"
        font-size="36"
        text-anchor="middle"
        font-weight="900"
        letter-spacing="2">
    <tspan fill="#F05032">Structure </tspan>
    <tspan fill="#58a6ff">Learning</tspan>
  </text>

  <!-- Subtitle -->
  <text x="600" y="285"
        font-family="Arial, sans-serif"
        font-size="14"
        fill="#8b949e"
        text-anchor="middle"
        letter-spacing="1">
    Beginner to Advanced  ·  Professional Learning Roadmap
  </text>

  <!-- Bottom accent line -->
  <rect x="320" y="300" width="560" height="1.5" rx="1"
        fill="url(#lineGrad)" opacity="0.8"/>

  <!-- Skill badges row -->
  <!-- Badge 1 -->
  <rect x="352" y="316" width="80" height="22" rx="11"
        fill="#161b22" stroke="#30363d" stroke-width="1"/>
  <circle cx="368" cy="327" r="4" fill="#F05032"/>
  <text x="378" y="331" font-family="monospace" font-size="9"
        fill="#c9d1d9" letter-spacing="0.5">git init</text>

  <!-- Badge 2 -->
  <rect x="444" y="316" width="96" height="22" rx="11"
        fill="#161b22" stroke="#30363d" stroke-width="1"/>
  <circle cx="460" cy="327" r="4" fill="#58a6ff"/>
  <text x="470" y="331" font-family="monospace" font-size="9"
        fill="#c9d1d9" letter-spacing="0.5">git commit</text>

  <!-- Badge 3 -->
  <rect x="552" y="316" width="86" height="22" rx="11"
        fill="#161b22" stroke="#30363d" stroke-width="1"/>
  <circle cx="568" cy="327" r="4" fill="#3fb950"/>
  <text x="578" y="331" font-family="monospace" font-size="9"
        fill="#c9d1d9" letter-spacing="0.5">git merge</text>

  <!-- Badge 4 -->
  <rect x="650" y="316" width="82" height="22" rx="11"
        fill="#161b22" stroke="#30363d" stroke-width="1"/>
  <circle cx="666" cy="327" r="4" fill="#d2a8ff"/>
  <text x="676" y="331" font-family="monospace" font-size="9"
        fill="#c9d1d9" letter-spacing="0.5">git rebase</text>

  <!-- Badge 5 -->
  <rect x="744" y="316" width="84" height="22" rx="11"
        fill="#161b22" stroke="#30363d" stroke-width="1"/>
  <circle cx="760" cy="327" r="4" fill="#ffa657"/>
  <text x="770" y="331" font-family="monospace" font-size="9"
        fill="#c9d1d9" letter-spacing="0.5">git push</text>

  <!-- ── RIGHT: Terminal Panel ── -->

  <!-- Terminal window frame -->
  <rect x="960" y="70" width="215" height="255" rx="10"
        fill="#161b22" stroke="#30363d" stroke-width="1.5"/>

  <!-- Terminal title bar -->
  <rect x="960" y="70" width="215" height="30" rx="10"
        fill="#21262d"/>
  <rect x="960" y="88" width="215" height="12" fill="#21262d"/>

  <!-- Traffic lights -->
  <circle cx="982" cy="85" r="5" fill="#ff5f57"/>
  <circle cx="998" cy="85" r="5" fill="#febc2e"/>
  <circle cx="1014" cy="85" r="5" fill="#28c840"/>

  <!-- Terminal label -->
  <text x="1067" y="90" font-family="monospace" font-size="10"
        fill="#8b949e" text-anchor="middle">bash — terminal</text>

  <!-- Terminal content -->
  <text x="978" y="122" font-family="monospace" font-size="10.5" fill="#3fb950">
    ~/project
  </text>
  <text x="978" y="122" font-family="monospace" font-size="10.5" fill="#8b949e">
    <tspan dx="60">$</tspan>
  </text>
  <text x="1052" y="122" font-family="monospace" font-size="10.5" fill="#c9d1d9">
    git init
  </text>

  <text x="978" y="143" font-family="monospace" font-size="9.5" fill="#8b949e">
    Initialized empty repo ✓
  </text>

  <text x="978" y="165" font-family="monospace" font-size="10.5" fill="#3fb950">
    ~/project
  </text>
  <text x="1038" y="165" font-family="monospace" font-size="10.5" fill="#8b949e">$</text>
  <text x="1052" y="165" font-family="monospace" font-size="10.5" fill="#c9d1d9">
    git add .
  </text>

  <text x="978" y="186" font-family="monospace" font-size="10.5" fill="#3fb950">
    ~/project
  </text>
  <text x="1038" y="186" font-family="monospace" font-size="10.5" fill="#8b949e">$</text>
  <text x="1052" y="186" font-family="monospace" font-size="10.5" fill="#c9d1d9">
    git commit
  </text>

  <text x="978" y="207" font-family="monospace" font-size="9.5" fill="#58a6ff">
    [main] initial commit
  </text>

  <text x="978" y="228" font-family="monospace" font-size="10.5" fill="#3fb950">
    ~/project
  </text>
  <text x="1038" y="228" font-family="monospace" font-size="10.5" fill="#8b949e">$</text>
  <text x="1052" y="228" font-family="monospace" font-size="10.5" fill="#c9d1d9">
    git push
  </text>

  <text x="978" y="249" font-family="monospace" font-size="9.5" fill="#3fb950">
    → origin/main ✓
  </text>

  <!-- Blinking cursor -->
  <rect x="978" y="263" width="7" height="12" rx="1" fill="#F05032" opacity="0.9">
    <animate attributeName="opacity" values="0.9;0;0.9" dur="1.2s" repeatCount="indefinite"/>
  </rect>

  <!-- ── Decorative Corner Dots ── -->
  <circle cx="30"   cy="30"  r="2" fill="#F05032" opacity="0.4"/>
  <circle cx="50"   cy="30"  r="1" fill="#F05032" opacity="0.2"/>
  <circle cx="30"   cy="50"  r="1" fill="#F05032" opacity="0.2"/>

  <circle cx="1170" cy="370" r="2" fill="#58a6ff" opacity="0.4"/>
  <circle cx="1150" cy="370" r="1" fill="#58a6ff" opacity="0.2"/>
  <circle cx="1170" cy="350" r="1" fill="#58a6ff" opacity="0.2"/>

  <!-- Bottom strip -->
  <rect x="0" y="390" width="1200" height="10" rx="0"
        fill="url(#lineGrad)" opacity="0.5"/>

</svg>