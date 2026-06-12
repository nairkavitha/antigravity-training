# Sampark Dashboard Design System

This design system document provides a comprehensive reference of colors, typography, shadows, layouts, and custom dashboard components used in the **Sampark v2 Analytics Dashboard**. 

You can use this reference to copy CSS variables, typography imports, and styling blocks directly into your future web applications and dashboards.

---

## 🎨 Color Palette & Design Tokens

These variables are defined under the `:root` scope. They use a professional, curated HSL-balanced scheme based on the Jio Blue and Jio Red corporate identities, paired with functional accent colors for alerts and statuses.

### CSS Variables Declarations
```css
:root {
  /* Brand Colors */
  --jio-blue: #005AAC;
  --jio-blue-deep: #003D7A;
  --jio-blue-light: #1A6FBE;
  --jio-blue-pale: #E8F1FA;
  
  --jio-red: #E8001D;
  --jio-red-light: #FF4D62;
  --jio-red-pale: #FFF0F2;
  
  --jio-cyan: #00B4D8;
  --jio-cyan-pale: #E0F7FB;

  /* Neutrals & Surfaces */
  --white: #FFFFFF;
  --off-white: #F7F9FC;     /* Body background */
  --surface: #F0F4F9;       /* Inactive tracks, secondary sections */
  --surface-2: #E3EBF5;     /* Tags and borders */
  
  /* Borders */
  --border: #D0DFF0;
  --border-light: #EAF0F8;

  /* Typography Colors */
  --text-primary: #0A1628;
  --text-secondary: #3D5278;
  --text-muted: #7A93B8;
  --text-light: #A8BDD8;

  /* Accent & Status Colors */
  --green: #00875A;
  --green-pale: #E3F9F0;
  
  --amber: #E67E22;
  --amber-pale: #FEF5EC;
  
  --purple: #6C47BB;
  --purple-pale: #F0EBFB;

  /* Depth (Shadows) */
  --shadow-sm: 0 1px 3px rgba(0, 90, 172, 0.08), 0 1px 2px rgba(0, 0, 0, 0.04);
  --shadow-md: 0 4px 16px rgba(0, 90, 172, 0.10), 0 2px 6px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 12px 40px rgba(0, 90, 172, 0.14), 0 4px 12px rgba(0, 0, 0, 0.08);
  --shadow-xl: 0 24px 64px rgba(0, 90, 172, 0.18), 0 8px 24px rgba(0, 0, 0, 0.10);

  /* Border Radii */
  --radius: 16px;           /* Primary card & container radius */
  --radius-sm: 10px;        /* Secondary item radius */
  --radius-xs: 6px;         /* Small items & inline highlights */
}
```

---

## 🔤 Typography

The typography system uses Google Fonts, combining **Rajdhani** for high-impact metric values and section headers, **DM Sans** for readable body text, and **DM Mono** for technical labels and numbers.

### Google Fonts Link Imports
Place these in the `<head>` of your HTML document:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,300&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
```

### Font Configurations
```css
body {
  font-family: 'DM Sans', sans-serif;
  color: var(--text-primary);
  line-height: 1.6;
}

/* Metric text, large display fonts */
.metric-text, h1, h2, h3, .card-title, .kpi-number, .radar-legend-score {
  font-family: 'Rajdhani', sans-serif;
}

/* Code, tables, status tags, metadata counts */
.mono-text, .quote-tag, .tag, .quote-attr, .rec-priority {
  font-family: 'DM Mono', monospace;
}
```

---

## 💎 Custom Components

### 1. Hero Header
A high-end gradient hero section with an embedded grid pattern overlay and dynamic animations.

```html
<div class="hero">
  <div class="hero-grid-overlay"></div>
  <div class="hero-content animate">
    <div class="hero-badge">
      <span class="hero-badge-dot"></span>
      Reliance Jio · HR Intelligence · Sampark Programme
    </div>
    <h1>Shaping <span>Sampark v2</span><br>Voice of the Field</h1>
    <p class="hero-sub">Deep analytics and thematic intelligence from 54 HR & TM Leads across Jio.</p>
    <div class="hero-meta">
      <div class="hero-stat">
        <div class="hero-stat-num">54</div>
        <div class="hero-stat-label">Respondents</div>
      </div>
      <div class="hero-divider"></div>
      <div class="hero-stat">
        <div class="hero-stat-num">100%</div>
        <div class="hero-stat-label">Completion Rate</div>
      </div>
    </div>
  </div>
</div>
```

```css
.hero {
  background: linear-gradient(135deg, var(--jio-blue-deep) 0%, var(--jio-blue) 45%, var(--jio-blue-light) 100%);
  position: relative;
  overflow: hidden;
  padding: 56px 64px 80px;
}

.hero::before {
  content: '';
  position: absolute;
  top: -80px; right: -80px;
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(255,255,255,0.06) 0%, transparent 70%);
  border-radius: 50%;
}

.hero::after {
  content: '';
  position: absolute;
  bottom: -120px; left: -60px;
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(0,180,216,0.12) 0%, transparent 70%);
  border-radius: 50%;
}

.hero-grid-overlay {
  position: absolute; inset: 0;
  background-image: linear-gradient(rgba(255,255,255,0.04) 1px, transparent 1px),
                    linear-gradient(90deg, rgba(255,255,255,0.04) 1px, transparent 1px);
  background-size: 40px 40px;
  pointer-events: none;
}

.hero-content { position: relative; z-index: 2; }

.hero-badge {
  display: inline-flex; align-items: center; gap: 8px;
  background: rgba(255,255,255,0.12);
  border: 1px solid rgba(255,255,255,0.2);
  border-radius: 100px;
  padding: 6px 16px;
  font-family: 'DM Mono', monospace;
  font-size: 11px;
  color: rgba(255,255,255,0.85);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-bottom: 24px;
  backdrop-filter: blur(8px);
}

.hero-badge-dot {
  width: 6px; height: 6px;
  background: #4DFFB4;
  border-radius: 50%;
  animation: pulse-green 2s infinite;
}

@keyframes pulse-green {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.5; transform: scale(0.8); }
}

.hero h1 {
  font-family: 'Rajdhani', sans-serif;
  font-size: 52px;
  font-weight: 700;
  color: white;
  line-height: 1.08;
  letter-spacing: -0.01em;
  margin-bottom: 16px;
}

.hero h1 span { color: var(--jio-cyan); }

.hero-sub {
  font-size: 17px;
  color: rgba(255,255,255,0.72);
  font-weight: 300;
  max-width: 520px;
  line-height: 1.6;
  margin-bottom: 40px;
}

.hero-meta {
  display: flex; align-items: center; gap: 32px;
  flex-wrap: wrap;
}

.hero-stat { display: flex; flex-direction: column; gap: 2px; }

.hero-stat-num {
  font-family: 'Rajdhani', sans-serif;
  font-size: 32px;
  font-weight: 700;
  color: white;
  line-height: 1;
}

.hero-stat-label {
  font-size: 11px;
  color: rgba(255,255,255,0.55);
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

.hero-divider {
  width: 1px; height: 40px;
  background: rgba(255,255,255,0.2);
}
```

---

### 2. Sticky Navigation Bar
A compact, sticky navbar that tracks layout categories using Intersection Observers.

```html
<div class="nav">
  <div class="nav-inner">
    <a class="nav-item active" href="#overview"><span class="nav-icon">⬡</span>Overview</a>
    <a class="nav-item" href="#effectiveness"><span class="nav-icon">📡</span>Effectiveness</a>
    <a class="nav-item" href="#domains"><span class="nav-icon">🔥</span>Issue Domains</a>
  </div>
</div>
```

```css
.nav {
  background: white;
  border-bottom: 1px solid var(--border);
  position: sticky; top: 0; z-index: 100;
  box-shadow: var(--shadow-sm);
}

.nav-inner {
  display: flex; align-items: center; gap: 4px;
  padding: 0 64px;
  overflow-x: auto;
}

.nav-item {
  display: flex; align-items: center; gap: 8px;
  padding: 16px 20px;
  font-size: 13px;
  font-weight: 500;
  color: var(--text-secondary);
  cursor: pointer;
  border-bottom: 2px solid transparent;
  white-space: nowrap;
  transition: all 0.2s;
  text-decoration: none;
}

.nav-item:hover { color: var(--jio-blue); }
.nav-item.active { color: var(--jio-blue); border-bottom-color: var(--jio-blue); }
.nav-icon { font-size: 15px; }
```

---

### 3. KPI Cards
Responsive metric containers configured with accent-colored top headers.

```html
<div class="kpi-grid">
  <!-- Blue Variant -->
  <div class="kpi-card blue">
    <div class="kpi-icon">🧭</div>
    <div class="kpi-number">3.8</div>
    <div class="kpi-label">Avg. Perceived Structure</div>
    <div class="kpi-sub">Scale 1–5 · 54 responses</div>
  </div>

  <!-- Red Variant -->
  <div class="kpi-card red">
    <div class="kpi-icon">🚨</div>
    <div class="kpi-number">67%</div>
    <div class="kpi-label">Primary Friction</div>
    <div class="kpi-sub">Field availability issues</div>
  </div>

  <!-- Green Variant -->
  <div class="kpi-card green">
    <div class="kpi-icon">✅</div>
    <div class="kpi-number">4.49</div>
    <div class="kpi-label">Avg. Effectiveness Score</div>
    <div class="kpi-sub">Scale 1-5</div>
  </div>
</div>
```

```css
.kpi-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 16px;
  margin-bottom: 24px;
}

.kpi-card {
  background: white;
  border-radius: var(--radius);
  padding: 24px;
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--border-light);
  position: relative;
  overflow: hidden;
  transition: box-shadow 0.3s, transform 0.3s;
}

.kpi-card:hover {
  box-shadow: var(--shadow-md);
  transform: translateY(-2px);
}

.kpi-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
}

/* Variant Border Gradients */
.kpi-card.blue::before { background: linear-gradient(90deg, var(--jio-blue), var(--jio-cyan)); }
.kpi-card.red::before { background: linear-gradient(90deg, var(--jio-red), #FF4D62); }
.kpi-card.green::before { background: linear-gradient(90deg, var(--green), #4ECCA3); }
.kpi-card.amber::before { background: linear-gradient(90deg, var(--amber), #F0C040); }
.kpi-card.purple::before { background: linear-gradient(90deg, var(--purple), var(--jio-cyan)); }

.kpi-icon {
  width: 40px; height: 40px;
  border-radius: var(--radius-xs);
  display: flex; align-items: center; justify-content: center;
  font-size: 20px;
  margin-bottom: 16px;
}

.kpi-card.blue .kpi-icon { background: var(--jio-blue-pale); }
.kpi-card.red .kpi-icon { background: var(--jio-red-pale); }
.kpi-card.green .kpi-icon { background: var(--green-pale); }
.kpi-card.amber .kpi-icon { background: var(--amber-pale); }
.kpi-card.purple .kpi-icon { background: var(--purple-pale); }

.kpi-number {
  font-family: 'Rajdhani', sans-serif;
  font-size: 40px;
  font-weight: 700;
  line-height: 1;
  margin-bottom: 4px;
}

.kpi-card.blue .kpi-number { color: var(--jio-blue); }
.kpi-card.red .kpi-number { color: var(--jio-red); }
.kpi-card.green .kpi-number { color: var(--green); }
.kpi-card.amber .kpi-number { color: var(--amber); }
.kpi-card.purple .kpi-number { color: var(--purple); }

.kpi-label {
  font-size: 12px;
  font-weight: 500;
  color: var(--text-secondary);
  line-height: 1.4;
}

.kpi-sub {
  font-size: 11px;
  color: var(--text-muted);
  margin-top: 6px;
}
```

---

### 4. Progress / Performance Bar Charts
Linear tracking bars utilizing smooth transitions for data fill width.

```html
<div class="bar-chart">
  <div class="bar-row">
    <div class="bar-labels">
      <span class="bar-label">Regular JC Health Review</span>
      <span class="bar-value">67%</span>
    </div>
    <div class="bar-track">
      <div class="bar-fill" style="width: 67%; background: linear-gradient(90deg, var(--green), #4ECCA3);"></div>
    </div>
  </div>
</div>
```

```css
.bar-chart { display: flex; flex-direction: column; gap: 10px; }
.bar-row { display: flex; flex-direction: column; gap: 4px; }
.bar-labels { display: flex; justify-content: space-between; align-items: center; }
.bar-label { font-size: 12px; color: var(--text-secondary); }

.bar-value {
  font-family: 'DM Mono', monospace;
  font-size: 12px;
  font-weight: 500;
  color: var(--text-primary);
}

.bar-track {
  height: 8px;
  background: var(--surface);
  border-radius: 4px;
  overflow: hidden;
}

.bar-fill {
  height: 100%;
  border-radius: 4px;
  transition: width 1.2s cubic-bezier(0.4, 0, 0.2, 1);
}
```

---

### 5. Insight Cards (Alert Indicators)
Informative list panels styled with left-bordered status alerts.

```html
<div class="insight-grid">
  <!-- Critical Alert -->
  <div class="insight-card critical">
    <div class="insight-icon">📭</div>
    <div class="insight-title">No Formal Tracking Mechanism</div>
    <div class="insight-text">Issues are logged but lack formal closure verification processes.</div>
    <div class="insight-stat">22 respondents</div>
  </div>

  <!-- Warning Alert -->
  <div class="insight-card warning">
    <div class="insight-icon">⏳</div>
    <div class="insight-title">Pending Regional Upgrades</div>
    <div class="insight-text">Resolution pipelines exceed standard state SLAs.</div>
    <div class="insight-stat">15 respondents</div>
  </div>
</div>
```

```css
.insight-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.insight-card {
  background: white;
  border-radius: var(--radius-sm);
  padding: 20px;
  border-left: 4px solid;
  box-shadow: var(--shadow-sm);
}

.insight-card.critical { border-left-color: var(--jio-red); }
.insight-card.warning { border-left-color: var(--amber); }
.insight-card.positive { border-left-color: var(--green); }
.insight-card.info { border-left-color: var(--jio-blue); }

.insight-icon { font-size: 22px; margin-bottom: 8px; }
.insight-title { font-size: 13px; font-weight: 600; color: var(--text-primary); margin-bottom: 6px; }
.insight-text { font-size: 12px; color: var(--text-secondary); line-height: 1.6; }

.insight-stat {
  font-family: 'Rajdhani', sans-serif;
  font-size: 24px;
  font-weight: 700;
  margin-top: 8px;
}

.insight-card.critical .insight-stat { color: var(--jio-red); }
.insight-card.warning .insight-stat { color: var(--amber); }
.insight-card.positive .insight-stat { color: var(--green); }
.insight-card.info .insight-stat { color: var(--jio-blue); }
```

---

### 6. Interactive Heatmap Grid
Matrix block component for displaying variable density metrics (e.g., categories vs frequencies).

```html
<div class="heatmap-header">
  <div class="heatmap-header-spacer"></div>
  <div class="heatmap-col-header">Very well</div>
  <div class="heatmap-col-header">Mostly</div>
  <div class="heatmap-col-header">Somewhat</div>
  <div class="heatmap-col-header">Not really</div>
</div>

<div class="heatmap-grid">
  <div class="heatmap-row">
    <div class="heatmap-row-label">👔 Manager Behaviour</div>
    <div class="heatmap-cells">
      <div class="heatmap-cell" style="background: var(--jio-blue); opacity: 0.45;">15%</div>
      <div class="heatmap-cell" style="background: var(--jio-blue); opacity: 0.42;">28%</div>
      <div class="heatmap-cell" style="background: var(--amber); opacity: 0.9;">33%</div>
      <div class="heatmap-cell" style="background: var(--jio-red); opacity: 0.65;">19%</div>
    </div>
  </div>
</div>
```

```css
.heatmap-grid { display: flex; flex-direction: column; gap: 10px; }
.heatmap-row { display: flex; align-items: center; gap: 12px; }
.heatmap-row-label {
  font-size: 12px; color: var(--text-secondary);
  width: 220px; flex-shrink: 0; line-height: 1.3;
}

.heatmap-cells { display: flex; gap: 4px; flex: 1; }

.heatmap-cell {
  flex: 1; height: 32px;
  border-radius: var(--radius-xs);
  display: flex; align-items: center; justify-content: center;
  font-size: 11px;
  font-weight: 500;
  color: white;
  position: relative;
  cursor: default;
  transition: transform 0.2s;
}

.heatmap-cell:hover { transform: scale(1.04); z-index: 2; }

.heatmap-header { display: flex; align-items: center; gap: 4px; margin-bottom: 4px; }
.heatmap-header-spacer { width: 220px; flex-shrink: 0; }
.heatmap-col-header { flex: 1; text-align: center; font-size: 10px; color: var(--text-muted); font-weight: 500; }
```

---

### 7. Quote Card
A stylized card block designed for testimonials, qualitative feedback, or user reviews.

```html
<div class="quote-card">
  <div class="quote-text">"Despite prior communication, field-role employees are often unavailable due to target runs."</div>
  <div class="quote-tag">Availability · Compensation</div>
</div>
```

```css
.quote-card {
  background: var(--off-white);
  border-radius: var(--radius-xs);
  padding: 14px 16px 14px 20px;
  border-left: 3px solid var(--border);
  position: relative;
  transition: all 0.2s;
}

.quote-card:hover {
  background: var(--jio-blue-pale);
  border-left-color: var(--jio-blue);
}

.quote-text {
  font-size: 13px;
  color: var(--text-primary);
  line-height: 1.7;
  font-style: italic;
}

.quote-tag {
  display: inline-flex;
  align-items: center;
  padding: 2px 10px;
  border-radius: 100px;
  font-size: 10px;
  font-weight: 500;
  background: var(--surface-2);
  color: var(--text-secondary);
  margin-top: 6px;
  font-family: 'DM Mono', monospace;
}
```

---

## 🛠️ Utility Styles & Animations

Use these classes to add polished micro-animations and structure page grids dynamically.

```css
/* Fade-In Up entrance animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate { animation: fadeInUp 0.6s ease both; }
.delay-1 { animation-delay: 0.1s; }
.delay-2 { animation-delay: 0.2s; }
.delay-3 { animation-delay: 0.3s; }
.delay-4 { animation-delay: 0.4s; }

/* Grid Layouts */
.grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
.grid-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 20px; }
.grid-3-2 { display: grid; grid-template-columns: 3fr 2fr; gap: 20px; }
.grid-2-3 { display: grid; grid-template-columns: 2fr 3fr; gap: 20px; }

/* Modern Styled Scrollbar */
::-webkit-scrollbar { width: 6px; height: 6px; }
::-webkit-scrollbar-track { background: var(--surface); }
::-webkit-scrollbar-thumb { background: var(--jio-blue); border-radius: 3px; }
```

---

## ⚙️ JavaScript Observers (Interactive Enhancements)

This script manages active states inside the header navigation based on viewport intersections, and handles smooth scrolling.

```javascript
// Smooth nav scroll + active state toggles
document.querySelectorAll('.nav-item').forEach(item => {
  item.addEventListener('click', function(e) {
    document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
    this.classList.add('active');
  });
});

// Intersection observer for section tracking active state
const sections = document.querySelectorAll('.section[id]');
const navItems = document.querySelectorAll('.nav-item');
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const id = entry.target.id;
      navItems.forEach(item => {
        item.classList.toggle('active', item.getAttribute('href') === '#' + id);
      });
    }
  });
}, { rootMargin: '-30% 0px -60% 0px' });
sections.forEach(s => observer.observe(s));
```
