<div align="center">

<svg width="860" height="130" viewBox="0 0 860 130" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Drift smoke gradient -->
    <radialGradient id="smoke1" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#888888" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#888888" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="smoke2" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#aaaaaa" stop-opacity="0.4"/>
      <stop offset="100%" stop-color="#aaaaaa" stop-opacity="0"/>
    </radialGradient>
    <!-- Speed line gradient -->
    <linearGradient id="speedLine" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#FF1801" stop-opacity="0"/>
      <stop offset="40%" stop-color="#FF1801" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#FF1801" stop-opacity="0"/>
    </linearGradient>
    <linearGradient id="trackLine" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#333" stop-opacity="0"/>
      <stop offset="50%" stop-color="#555" stop-opacity="1"/>
      <stop offset="100%" stop-color="#333" stop-opacity="0"/>
    </linearGradient>
    <style>
      .f1-car { animation: raceDrift 4s cubic-bezier(0.25, 0.46, 0.45, 0.94) infinite; }
      .smoke-trail { animation: smokeTrail 4s cubic-bezier(0.25, 0.46, 0.45, 0.94) infinite; }
      .spark1 { animation: spark 4s ease-in-out infinite; }
      .spark2 { animation: spark 4s ease-in-out 0.15s infinite; }
      .spark3 { animation: spark 4s ease-in-out 0.3s infinite; }

      @keyframes raceDrift {
        0%   { transform: translateX(-140px) rotate(0deg); opacity: 0; }
        5%   { opacity: 1; }
        30%  { transform: translateX(260px) rotate(-12deg); }
        50%  { transform: translateX(430px) rotate(8deg); }
        70%  { transform: translateX(620px) rotate(-6deg); }
        90%  { transform: translateX(820px) rotate(0deg); opacity: 1; }
        100% { transform: translateX(980px) rotate(0deg); opacity: 0; }
      }

      @keyframes smokeTrail {
        0%   { transform: translateX(-200px); opacity: 0; }
        5%   { opacity: 1; }
        30%  { transform: translateX(180px) scaleX(2) scaleY(1.5); opacity: 0.7; }
        50%  { transform: translateX(340px) scaleX(3) scaleY(2); opacity: 0.4; }
        70%  { transform: translateX(520px) scaleX(4) scaleY(2.5); opacity: 0.2; }
        100% { transform: translateX(900px) scaleX(5); opacity: 0; }
      }

      @keyframes spark {
        0%   { transform: translateX(-140px); opacity: 0; }
        28%  { opacity: 0; }
        30%  { opacity: 1; }
        35%  { opacity: 0; }
        100% { transform: translateX(980px); opacity: 0; }
      }
    </style>
  </defs>

  <!-- Track surface -->
  <rect x="0" y="98" width="860" height="18" fill="#111111" rx="2"/>
  <rect x="0" y="104" width="860" height="2" fill="url(#trackLine)"/>
  <!-- Track dashes -->
  <rect x="80" y="106" width="40" height="2" fill="#FFD700" opacity="0.5"/>
  <rect x="200" y="106" width="40" height="2" fill="#FFD700" opacity="0.5"/>
  <rect x="320" y="106" width="40" height="2" fill="#FFD700" opacity="0.5"/>
  <rect x="440" y="106" width="40" height="2" fill="#FFD700" opacity="0.5"/>
  <rect x="560" y="106" width="40" height="2" fill="#FFD700" opacity="0.5"/>
  <rect x="680" y="106" width="40" height="2" fill="#FFD700" opacity="0.5"/>
  <rect x="780" y="106" width="40" height="2" fill="#FFD700" opacity="0.5"/>

  <!-- Drift smoke cloud -->
  <g class="smoke-trail">
    <ellipse cx="60" cy="90" rx="30" ry="14" fill="url(#smoke1)"/>
    <ellipse cx="30" cy="85" rx="22" ry="10" fill="url(#smoke2)"/>
    <ellipse cx="10" cy="82" rx="14" ry="8" fill="url(#smoke1)" opacity="0.5"/>
  </g>

  <!-- Sparks during drift -->
  <circle class="spark1" cx="260" cy="94" r="2.5" fill="#FFD700"/>
  <circle class="spark2" cx="255" cy="90" r="1.5" fill="#FF6B00"/>
  <circle class="spark3" cx="265" cy="92" r="2" fill="#FF1801"/>

  <!-- Speed lines -->
  <rect x="0" y="75" width="860" height="1.5" fill="url(#speedLine)" opacity="0.5"/>
  <rect x="0" y="80" width="860" height="1" fill="url(#speedLine)" opacity="0.3"/>

  <!-- ═══ F1 CAR ═══ -->
  <g class="f1-car">
    <!-- Shadow -->
    <ellipse cx="0" cy="100" rx="58" ry="5" fill="#000" opacity="0.3"/>

    <!-- Rear diffuser -->
    <polygon points="-52,95 -42,88 -42,96" fill="#990000"/>

    <!-- Main body — low, sleek sidepods -->
    <path d="M -55,93 L -42,83 L 30,81 L 48,85 L 52,93 Z" fill="#CC1100"/>
    <!-- Top body highlight -->
    <path d="M -42,83 L 30,81 L 40,84 L -30,85 Z" fill="#FF2200" opacity="0.6"/>

    <!-- Cockpit / monocoque -->
    <path d="M -15,81 Q -5,68 15,68 Q 25,68 30,75 L 28,81 Z" fill="#1a1a2e"/>
    <!-- Cockpit rim highlight -->
    <path d="M -12,80 Q 0,70 14,70 Q 22,70 26,75" stroke="#FF1801" stroke-width="1" fill="none" opacity="0.8"/>

    <!-- Halo -->
    <path d="M -8,76 Q 8,62 22,70" stroke="#C8A000" stroke-width="2.5" fill="none" stroke-linecap="round"/>
    <rect x="-2" y="68" width="3" height="8" fill="#C8A000" rx="1"/>

    <!-- Nose cone — long and pointed -->
    <polygon points="-55,90 -55,95 -85,92" fill="#AA0000"/>
    <polygon points="-55,90 -70,91 -85,92" fill="#FF2200" opacity="0.4"/>

    <!-- Front wing -->
    <rect x="-90" y="92" width="38" height="3" fill="#CC1100" rx="1"/>
    <rect x="-82" y="89" width="22" height="3" fill="#FF1801" rx="1"/>
    <!-- Front wing endplates -->
    <rect x="-90" y="89" width="3" height="6" fill="#880000" rx="1"/>
    <rect x="-53" y="89" width="3" height="6" fill="#880000" rx="1"/>

    <!-- Rear wing -->
    <rect x="42" y="74" width="22" height="3.5" fill="#FF1801" rx="1"/>
    <rect x="44" y="77" width="18" height="3" fill="#CC1100" rx="1"/>
    <!-- DRS flap line -->
    <line x1="42" y1="75.5" x2="64" y2="75.5" stroke="#FFD700" stroke-width="0.8" opacity="0.7"/>
    <!-- Rear wing endplates -->
    <rect x="42" y="74" width="3" height="15" fill="#880000" rx="1"/>
    <rect x="61" y="74" width="3" height="15" fill="#880000" rx="1"/>

    <!-- Rear wheel + tire -->
    <circle cx="38" cy="95" r="11" fill="#1a1a1a"/>
    <circle cx="38" cy="95" r="8" fill="#111"/>
    <circle cx="38" cy="95" r="4" fill="#333"/>
    <!-- Rim detail -->
    <line x1="34" y1="95" x2="42" y2="95" stroke="#555" stroke-width="1"/>
    <line x1="38" y1="91" x2="38" y2="99" stroke="#555" stroke-width="1"/>

    <!-- Front wheel + tire -->
    <circle cx="-40" cy="95" r="10" fill="#1a1a1a"/>
    <circle cx="-40" cy="95" r="7" fill="#111"/>
    <circle cx="-40" cy="95" r="3.5" fill="#333"/>
    <line x1="-44" y1="95" x2="-36" y2="95" stroke="#555" stroke-width="1"/>
    <line x1="-40" y1="91" x2="-40" y2="99" stroke="#555" stroke-width="1"/>

    <!-- Suspension arms -->
    <line x1="-20" y1="87" x2="-40" y2="92" stroke="#444" stroke-width="1.5"/>
    <line x1="-10" y1="89" x2="-40" y2="94" stroke="#444" stroke-width="1.5"/>
    <line x1="18" y1="87" x2="38" y2="90" stroke="#444" stroke-width="1.5"/>
    <line x1="10" y1="89" x2="38" y2="94" stroke="#444" stroke-width="1.5"/>

    <!-- Sidepod vents -->
    <line x1="-35" y1="84" x2="-30" y2="84" stroke="#FF4400" stroke-width="1" opacity="0.7"/>
    <line x1="-35" y1="86" x2="-30" y2="86" stroke="#FF4400" stroke-width="1" opacity="0.7"/>

    <!-- Exhaust glow -->
    <ellipse cx="-48" cy="88" rx="5" ry="3" fill="#FF6600" opacity="0.6"/>
    <ellipse cx="-50" cy="88" rx="3" ry="2" fill="#FFAA00" opacity="0.8"/>

    <!-- Race number -->
    <text x="0" y="80" font-family="monospace" font-size="7" font-weight="bold" fill="#FFD700" text-anchor="middle">4.0</text>
  </g>
</svg>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=13&duration=50&pause=2000&color=FF1801&center=true&vCenter=true&width=860&lines=🏎️+%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA)](https://git.io/typing-svg)

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=72&duration=1000&pause=99999&color=FF1801&center=true&vCenter=true&width=900&height=120&lines=HACKX+4.0)](https://git.io/typing-svg)

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Orbitron&weight=600&size=16&duration=1000&pause=99999&color=FFD700&center=true&vCenter=true&width=700&height=35&lines=BUILD.+RACE.+WIN.+——+NMIMS+NAVI+MUMBAI)](https://git.io/typing-svg)

<br/>

![](https://img.shields.io/badge/FORMAT-OFFLINE-FF1801?style=for-the-badge&labelColor=0d0d0d)
![](https://img.shields.io/badge/DURATION-24%20HOURS-FFD700?style=for-the-badge&labelColor=0d0d0d)
![](https://img.shields.io/badge/TEAM-2–4%20MEMBERS-FF6B35?style=for-the-badge&labelColor=0d0d0d)
![](https://img.shields.io/badge/PRIZE%20POOL-₹75%2C000-00D4FF?style=for-the-badge&labelColor=0d0d0d)

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=13&duration=50&pause=2000&color=FF1801&center=true&vCenter=true&width=860&lines=🏎️+%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%ba%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA%E2%80%BA)](https://git.io/typing-svg)

</div>

---

## ⚡ IGNITION

**HackX 4.0** is a **24-hour offline flagship hackathon** at **NMIMS, Navi Mumbai** — where the sharpest student developers, designers, and problem-solvers strap in and race to build real-world solutions at full throttle.

Teams of **2–4** sprint from concept to deployment in one relentless session of critical thinking, fast coding, and bold innovation. With **₹75,000** on the line, **Logitech gear**, **internship opportunities**, and goodies + certificates for every racer — this is your Grand Prix moment.

> *"Lights out. And away we go."*

---

## 🏆 PRIZE GARAGE

<div align="center">

| 🥇 P1 — Grand Prix | 🥈 P2 — Runner Up | 🥉 P3 — Second Runner Up | 🎖️ All Finishers |
|:------------------:|:-----------------:|:------------------------:|:----------------:|
| **₹35,000** | **₹25,000** | **₹15,000** | Certificates + Internship Opps |

### 🎁 All winners receive: Logitech Goodies + Swag Pack
### 💰 Total Prize Pool: ₹75,000

</div>

---

## 🔩 PROBLEM STATEMENTS — PICK YOUR CIRCUIT

<br/>

### `PS-01` &nbsp; AI / DevSecOps
**The Vibe-Audit** — *Production-Ready Gatekeeper*

Build an automated gatekeeper that scans AI-generated *(vibe-coded)* repos and produces a structured **Go/No-Go production readiness report** — covering secrets detection, compliance checks, and dependency auditing.

<br/>

### `PS-02` &nbsp; AI / Agents
**Curvet AI** — *The SME-Plug · Hot-Swappable Expert Plugin*

Design a universal skill plugin that injects **specialized domain knowledge and structured reasoning** into any AI agent framework — enforcing source-of-truth citations and domain-specific decision trees.

<br/>

### `PS-03` &nbsp; SaaS / Ops
**Prasad Food Divine** — *Banquet Management · End-to-End Event Platform*

Build a centralized multi-branch banquet management platform covering **lead tracking, real-time booking, event coordination, vendor management, billing automation**, and analytics dashboards.

<br/>

### `PS-04` &nbsp; Analytics / CX
**Prasad Food Divine** — *Review Management · Centralized Feedback Intelligence*

Develop a platform that **aggregates reviews from Google, Zomato, and internal forms**, auto-categorizes feedback, generates AI-assisted responses, and delivers branch & staff performance insights.

<br/>

### `PS-05` &nbsp; Distributed Systems
**Cosmeon** — *FS-Lite · Orbital File System Simulation*

Build a lightweight distributed file system that **splits files into chunks and distributes them across simulated satellite nodes** — with on-demand reconstruction, integrity checks, and failure simulation.

<br/>

### `PS-06` &nbsp; ML / Geo
**Cosmeon** — *Satellite Insight Engine · Climate Risk from Orbital Data*

Build a pipeline that ingests open satellite imagery *(Sentinel/Landsat)*, performs **automated flood detection and environmental risk analysis using ML**, and outputs structured, decision-ready climate risk insights.

---

## 🏎️ PIT LANE TIMELINE

> *The race is 24 hours. Every sector counts. Here's your strategy board.*

<br/>

<div align="center">

**— — — — — — — — — FEB 28 — — — — — — — — —**

</div>

| 🕐 Time | Pit Stop | Status |
|:-------:|:--------:|:-------|
| **8:30 AM** | 🔴 CHECK-IN | Reporting — scrutineering & paddock entry |
| **9:00 AM** | 📋 OFFICIALS | Registrations open — driver livery collection |
| **10:30 AM** | 🟡 FORMATION LAP | Opening Ceremony — system diagnostics complete |
| **12:00 PM** | 🟢 **RACE START** | **Green flag! 24-hour clock begins. ERS enabled.** |
| **5:00 PM** | ☕ REFRESH | High Tea — fuel & tire management |
| **7:00 PM** | 🛠️ PIT STOP I | Mentorship Round I — mid-race strategy tuning |
| **8:00 PM** | 🍽️ DINNER | Evening fuel stop |

<div align="center">

**— — — — — — — — — MAR 1 — — — — — — — — —**

</div>

| 🕐 Time | Pit Stop | Status |
|:-------:|:--------:|:-------|
| **8:30 AM** | 🌅 BREAKFAST | Morning boost — fresh tires, new strategy |
| **9:00 AM** | 🏎️ FINAL STINT | Mentorship Round II — push for fastest lap |
| **12:00 PM** | 🏁 **RACE END** | **Chequered flag — submissions closed. Cool down lap.** |
| **12:15 PM** | 🥗 LUNCH | Post-race recovery mode |
| **1:00 PM** | ⚖️ JUDGING | Technical inspection — stewards review begins |
| **4:00 PM** | 🏆 **PODIUM** | **Results & Closing Ceremony — Victory lap!** |

---

## 🧑‍💻 DRIVER SPECS

```
TEAM SIZE   →  2 – 4 members
ELIGIBILITY →  Students only  
FORMAT      →  Offline · On-site
VENUE       →  NMIMS, Navi Mumbai
DURATION    →  24 Hours non-stop
```

---

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=20&duration=2500&pause=800&color=FF1801&center=true&vCenter=true&width=700&lines=LIGHTS+OUT.+AWAY+WE+GO.;YOUR+TRACK+AWAITS.;HACKX+4.0+—+RACE+DAY+IS+HERE.)](https://git.io/typing-svg)

<br/>

*Made with ❤️ and full throttle by the HackX Team · NMIMS Navi Mumbai*

</div>
