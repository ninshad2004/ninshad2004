<svg width="900" height="280" viewBox="0 0 900 280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <style>
      @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&amp;display=swap');
      .mono { font-family: 'JetBrains Mono', 'Courier New', monospace; }
      .key { fill: #7ee787; }
      .val { fill: #79c0ff; }
      .val-teal { fill: #3dd68c; }
      .val-amber { fill: #e3b341; }
      .val-pink { fill: #f778ba; }
      .sep { fill: #484f58; }
      .muted { fill: #6e7681; }
      .bright { fill: #e6edf3; }

      /* Typing animation for command */
      #cmd-text {
        font-family: 'JetBrains Mono', 'Courier New', monospace;
        font-size: 13px;
        fill: #e6edf3;
      }
      .cmd-chars { animation: reveal-cmd 1.2s steps(1) 0.3s both; }
      @keyframes reveal-cmd {
        0%  { clip-path: inset(0 100% 0 0); }
        100%{ clip-path: inset(0 0% 0 0); }
      }

      /* Cursor blink */
      #cursor { animation: blink 1s step-end infinite 1.6s; opacity:0; }
      @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

      /* Lines fade in sequentially */
      .line { opacity: 0; animation: fadein 0.3s ease forwards; }
      #l1 { animation-delay: 1.5s; }
      #l2 { animation-delay: 1.75s; }
      #l3 { animation-delay: 2.0s; }
      #l4 { animation-delay: 2.25s; }
      #l5 { animation-delay: 2.5s; }
      #l6 { animation-delay: 2.75s; }
      @keyframes fadein { to { opacity: 1; } }

      /* Badges */
      .badge { opacity: 0; animation: badge-in 0.4s ease forwards; }
      #b1{animation-delay:3.1s} #b2{animation-delay:3.2s} #b3{animation-delay:3.3s}
      #b4{animation-delay:3.4s} #b5{animation-delay:3.5s} #b6{animation-delay:3.6s}
      #b7{animation-delay:3.7s} #b8{animation-delay:3.8s} #b9{animation-delay:3.9s}
      #b10{animation-delay:4.0s}
      @keyframes badge-in { to { opacity: 1; } }

      /* Scan line */
      #scanline { animation: scan 4s linear infinite; }
      @keyframes scan { 0%{transform:translateY(0px)} 100%{transform:translateY(280px)} }

      /* Particles float */
      .p { animation: float linear infinite; }
      @keyframes float {
        0%{opacity:0.1} 50%{opacity:0.5} 100%{opacity:0.1}
      }
    </style>

    <!-- Grid pattern -->
    <pattern id="grid" width="32" height="32" patternUnits="userSpaceOnUse">
      <path d="M 32 0 L 0 0 0 32" fill="none" stroke="#1D9E75" stroke-width="0.3" opacity="0.15"/>
    </pattern>

    <!-- Clip for typing effect -->
    <clipPath id="cmd-clip">
      <rect x="0" y="0" width="900" height="280"/>
    </clipPath>
  </defs>

  <!-- Background -->
  <rect width="900" height="280" rx="12" fill="#0d1117"/>

  <!-- Grid overlay -->
  <rect width="900" height="280" rx="12" fill="url(#grid)" opacity="0.6"/>

  <!-- Scan line -->
  <rect id="scanline" x="0" y="0" width="900" height="2" fill="#1D9E75" opacity="0.12"/>

  <!-- Floating particles -->
  <circle class="p" cx="820" cy="40" r="1.5" fill="#1D9E75" opacity="0.3" style="animation-duration:3.1s;animation-delay:0.2s"/>
  <circle class="p" cx="760" cy="90" r="1" fill="#79c0ff" opacity="0.3" style="animation-duration:4.2s;animation-delay:1s"/>
  <circle class="p" cx="850" cy="160" r="2" fill="#1D9E75" opacity="0.2" style="animation-duration:3.7s;animation-delay:0.5s"/>
  <circle class="p" cx="780" cy="220" r="1.2" fill="#e3b341" opacity="0.25" style="animation-duration:5s;animation-delay:1.8s"/>
  <circle class="p" cx="870" cy="120" r="1" fill="#f778ba" opacity="0.2" style="animation-duration:4.5s;animation-delay:0.8s"/>
  <circle class="p" cx="30" cy="60" r="1.2" fill="#1D9E75" opacity="0.2" style="animation-duration:3.9s;animation-delay:1.2s"/>
  <circle class="p" cx="60" cy="240" r="1" fill="#79c0ff" opacity="0.2" style="animation-duration:4.1s;animation-delay:2s"/>
  <circle class="p" cx="840" cy="250" r="1.5" fill="#3dd68c" opacity="0.2" style="animation-duration:3.5s;animation-delay:0.4s"/>
  <circle class="p" cx="15" cy="150" r="1" fill="#79c0ff" opacity="0.15" style="animation-duration:4.8s;animation-delay:1.5s"/>
  <circle class="p" cx="890" cy="60" r="1.2" fill="#1D9E75" opacity="0.2" style="animation-duration:3.3s;animation-delay:0.9s"/>

  <!-- Corner brackets decoration -->
  <path d="M 16 16 L 16 36 M 16 16 L 36 16" stroke="#1D9E75" stroke-width="1.5" fill="none" opacity="0.5"/>
  <path d="M 884 16 L 884 36 M 884 16 L 864 16" stroke="#1D9E75" stroke-width="1.5" fill="none" opacity="0.5"/>
  <path d="M 16 264 L 16 244 M 16 264 L 36 264" stroke="#1D9E75" stroke-width="1.5" fill="none" opacity="0.5"/>
  <path d="M 884 264 L 884 244 M 884 264 L 864 264" stroke="#1D9E75" stroke-width="1.5" fill="none" opacity="0.5"/>

  <!-- Window dots -->
  <circle cx="44" cy="32" r="5" fill="#ff5f57"/>
  <circle cx="62" cy="32" r="5" fill="#febc2e"/>
  <circle cx="80" cy="32" r="5" fill="#28c840"/>
  <text x="100" y="37" class="mono muted" font-size="11">ninshad@kali ~ %</text>

  <!-- Divider line -->
  <line x1="24" y1="48" x2="876" y2="48" stroke="#21262d" stroke-width="0.5"/>

  <!-- Prompt -->
  <text x="32" y="76" class="mono val-teal" font-size="13">❯</text>
  <g class="cmd-chars">
    <text x="50" y="76" id="cmd-text">cat ninshad.json</text>
  </g>
  <rect id="cursor" x="214" y="63" width="7" height="14" fill="#3dd68c"/>

  <!-- Output lines -->
  <g class="mono" font-size="12.5">
    <g id="l1" class="line">
      <text x="32" y="104" class="sep">┌──</text>
      <text x="68" y="104" class="key">name</text>
      <text x="108" y="104" class="sep">──────────</text>
      <text x="210" y="104" class="bright">Ninshad KS</text>
    </g>
    <g id="l2" class="line">
      <text x="32" y="122" class="sep">│</text>
      <text x="46" y="122" class="key">role</text>
      <text x="86" y="122" class="sep">──────────</text>
      <text x="188" y="122" class="val-teal">Cybersecurity Practitioner · Tool Builder · Founder</text>
    </g>
    <g id="l3" class="line">
      <text x="32" y="140" class="sep">│</text>
      <text x="46" y="140" class="key">base</text>
      <text x="86" y="140" class="sep">──────────</text>
      <text x="188" y="140" class="val-amber">Kochi, Kerala, India  ·  Open to remote &amp; relocation</text>
    </g>
    <g id="l4" class="line">
      <text x="32" y="158" class="sep">│</text>
      <text x="46" y="158" class="key">cert</text>
      <text x="86" y="158" class="sep">──────────</text>
      <text x="188" y="158" class="val-pink">CEH v13 · CHFI · CSA  (EC-Council)</text>
    </g>
    <g id="l5" class="line">
      <text x="32" y="176" class="sep">│</text>
      <text x="46" y="176" class="key">focus</text>
      <text x="86" y="176" class="sep">─────────</text>
      <text x="188" y="176" class="val">Offensive Security · AI-powered Tools · Kerala SMBs</text>
    </g>
    <g id="l6" class="line">
      <text x="32" y="194" class="sep">└──</text>
      <text x="68" y="194" class="key">status</text>
      <text x="116" y="194" class="sep">────────</text>
      <text x="210" y="194" class="val-teal">Seeking SOC Analyst / Junior Pen Tester roles</text>
      <circle cx="670" cy="189" r="4" fill="#3dd68c">
        <animate attributeName="opacity" values="1;0.2;1" dur="2s" repeatCount="indefinite"/>
      </circle>
    </g>
  </g>

  <!-- Badge row -->
  <g class="mono" font-size="11">
    <!-- Metasploit -->
    <g id="b1" class="badge">
      <rect x="32" y="213" width="82" height="20" rx="10" fill="#0f6e5620" stroke="#1D9E75" stroke-width="0.8"/>
      <text x="73" y="227" text-anchor="middle" fill="#3dd68c">Metasploit</text>
    </g>
    <!-- Nmap -->
    <g id="b2" class="badge">
      <rect x="120" y="213" width="48" height="20" rx="10" fill="#185fa520" stroke="#388bfd" stroke-width="0.8"/>
      <text x="144" y="227" text-anchor="middle" fill="#79c0ff">Nmap</text>
    </g>
    <!-- Burp Suite -->
    <g id="b3" class="badge">
      <rect x="174" y="213" width="76" height="20" rx="10" fill="#185fa520" stroke="#388bfd" stroke-width="0.8"/>
      <text x="212" y="227" text-anchor="middle" fill="#79c0ff">Burp Suite</text>
    </g>
    <!-- Python -->
    <g id="b4" class="badge">
      <rect x="256" y="213" width="56" height="20" rx="10" fill="#85490b20" stroke="#d29922" stroke-width="0.8"/>
      <text x="284" y="227" text-anchor="middle" fill="#e3b341">Python</text>
    </g>
    <!-- Wazuh -->
    <g id="b5" class="badge">
      <rect x="318" y="213" width="56" height="20" rx="10" fill="#0f6e5620" stroke="#1D9E75" stroke-width="0.8"/>
      <text x="346" y="227" text-anchor="middle" fill="#3dd68c">Wazuh</text>
    </g>
    <!-- OSINT -->
    <g id="b6" class="badge">
      <rect x="380" y="213" width="54" height="20" rx="10" fill="#72243e20" stroke="#db61a2" stroke-width="0.8"/>
      <text x="407" y="227" text-anchor="middle" fill="#f778ba">OSINT</text>
    </g>
    <!-- MITRE ATT&CK -->
    <g id="b7" class="badge">
      <rect x="440" y="213" width="100" height="20" rx="10" fill="#185fa520" stroke="#388bfd" stroke-width="0.8"/>
      <text x="490" y="227" text-anchor="middle" fill="#79c0ff">MITRE ATT&amp;CK</text>
    </g>
    <!-- YARA -->
    <g id="b8" class="badge">
      <rect x="546" y="213" width="50" height="20" rx="10" fill="#85490b20" stroke="#d29922" stroke-width="0.8"/>
      <text x="571" y="227" text-anchor="middle" fill="#e3b341">YARA</text>
    </g>
    <!-- Kali Linux -->
    <g id="b9" class="badge">
      <rect x="602" y="213" width="76" height="20" rx="10" fill="#21262d" stroke="#484f58" stroke-width="0.8"/>
      <text x="640" y="227" text-anchor="middle" fill="#8b949e">Kali Linux</text>
    </g>
    <!-- FastAPI -->
    <g id="b10" class="badge">
      <rect x="684" y="213" width="62" height="20" rx="10" fill="#0f6e5620" stroke="#1D9E75" stroke-width="0.8"/>
      <text x="715" y="227" text-anchor="middle" fill="#3dd68c">FastAPI</text>
    </g>
  </g>

  <!-- Bottom link -->
  <text x="32" y="258" class="mono muted" font-size="11">ninshadks.netlify.app  ·  github.com/ninshad2004</text>
  <text x="868" y="258" text-anchor="end" class="mono" font-size="11" fill="#484f58">v2.0</text>
</svg>

# Hey, I'm Ninshad 👋

**Cybersecurity Practitioner · Tool Builder · Founder**  
📍 Kochi, Kerala → Open to remote & relocation worldwide  
🔍 Actively seeking SOC Analyst / Junior Pen Tester / Security Analyst roles

---

## 🛠️ What I've Built

| Project | What it does | Stack |
|---|---|---|
| [KUMARAN](https://github.com/ninshad2004/Kumaran) | CLI network security scanner — ethical recon & risk scoring | Python, Nmap |
| [Job Hunter Agent](https://job-hunter-agent-eight.vercel.app) | Live web app that automates job searching & filtering | HTML, JS, Vercel |
| UPI SafeScan | AI-powered UPI QR fraud detection before payment | Python, TensorFlow |
| Cyvron | Cybersecurity consultancy for SMBs in Kerala | FastAPI, Nuclei |

---

## ⚔️ Skills & Tools

**Offensive:** Metasploit · Nmap · Burp Suite · Nikto · SQLMap · OWASP ZAP  
**Defensive:** Wazuh · Splunk · Wireshark · Snort · ELK Stack · Sysmon  
**Intel & Forensics:** MITRE ATT&CK · OSINT · YARA · Digital Forensics · CVSS v3.1  
**Dev:** Python · Bash · PowerShell · Linux (Kali daily driver) · HTML/CSS/JS

---

## 📜 Certifications (In Progress)

- 🎯 CEH v13 — EC-Council · Expected Aug 2026  
- 🎯 CSA — EC-Council · Expected Oct 2026  
- 🎯 CHFI — EC-Council · Expected Dec 2026

---

## 📬 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-ninshad-blue?style=flat&logo=linkedin)](https://linkedin.com/in/ninshad)
[![Portfolio](https://img.shields.io/badge/Portfolio-ninshadks.netlify.app-green?style=flat)](https://ninshadks.netlify.app)
[![Email](https://img.shields.io/badge/Email-ninshadktl2004@gmail.com-red?style=flat&logo=gmail)](mailto:ninshadktl2004@gmail.com)

> 💡 *21 · Fresher · Building in public · Open to anywhere*
