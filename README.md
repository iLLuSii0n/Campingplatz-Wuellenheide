<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Campingplatz Wüllenheide – Camping Club Bremen e.V.</title>
<meta name="description" content="Campingplatz Wüllenheide in Wilstedt bei Bremen: Zeltplätze, Stellplätze, Mietwohnwagen und Dauerplätze direkt neben dem Heidebad – betrieben vom Camping Club Bremen e.V.">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --green-deep: #1B4332;
    --green-mid: #2D6A4F;
    --green-light: #52B788;
    --sand: #F5EDD6;
    --sand-dark: #E8D9B4;
    --sky: #7EC8E3;
    --terracotta: #C17A44;
    --cream: #FDFAF4;
    --text-dark: #1A1A1A;
    --text-mid: #4A5568;
    --white: #ffffff;
    --radius: 4px;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--cream);
    color: var(--text-dark);
    font-size: 16px;
    line-height: 1.65;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(27,67,50,0.97);
    backdrop-filter: blur(8px);
    padding: 0 2rem;
    display: flex; align-items: center; justify-content: space-between;
    height: 64px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
  }

  .nav-logo {
    font-family: 'Playfair Display', serif;
    color: var(--sand);
    font-size: 1.1rem;
    line-height: 1.2;
    text-decoration: none;
    letter-spacing: 0.02em;
  }
  .nav-logo span { color: var(--sky); }

  .nav-links {
    display: flex; gap: 1.75rem; list-style: none;
  }
  .nav-links a {
    color: rgba(245,237,214,0.8);
    text-decoration: none;
    font-size: 0.85rem;
    font-weight: 500;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--sky); }

  .nav-cta {
    background: var(--terracotta);
    color: var(--white) !important;
    padding: 0.5rem 1.25rem;
    border-radius: 2px;
    transition: background 0.2s !important;
  }
  .nav-cta:hover { background: #a86538 !important; color: var(--white) !important; }

  /* HERO */
  .hero {
    min-height: 100vh;
    background: linear-gradient(160deg, var(--green-deep) 0%, #0d2b1f 60%, #071a12 100%);
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    position: relative; overflow: hidden;
    padding-top: 64px;
  }

  .lake-svg {
    position: absolute; bottom: 0; left: 0; right: 0;
    width: 100%; height: 280px;
    opacity: 0.35;
  }

  .hero-stars {
    position: absolute; top: 0; left: 0; right: 0; bottom: 0;
    background-image:
      radial-gradient(1px 1px at 15% 20%, rgba(255,255,255,0.6) 0%, transparent 100%),
      radial-gradient(1px 1px at 40% 8%, rgba(255,255,255,0.4) 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 70% 15%, rgba(255,255,255,0.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 85% 30%, rgba(255,255,255,0.3) 0%, transparent 100%),
      radial-gradient(1px 1px at 55% 25%, rgba(255,255,255,0.4) 0%, transparent 100%),
      radial-gradient(1px 1px at 25% 45%, rgba(255,255,255,0.2) 0%, transparent 100%);
  }

  .hero-content {
    position: relative; z-index: 2;
    text-align: center; padding: 2rem;
    max-width: 860px;
  }

  .hero-eyebrow {
    display: inline-block;
    color: var(--sky);
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    font-weight: 600;
    margin-bottom: 1.5rem;
    padding: 0.4rem 1rem;
    border: 1px solid rgba(126,200,227,0.3);
    border-radius: 2px;
  }

  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 7vw, 5.5rem);
    font-weight: 900;
    color: var(--sand);
    line-height: 1.1;
    margin-bottom: 1.5rem;
    letter-spacing: -0.02em;
  }
  .hero h1 em {
    font-style: italic;
    color: var(--sky);
  }

  .hero-sub {
    color: rgba(245,237,214,0.7);
    font-size: 1.1rem;
    max-width: 600px;
    margin: 0 auto 2.5rem;
    font-weight: 300;
  }

  .hero-badges {
    display: flex; gap: 1.5rem; justify-content: center; flex-wrap: wrap;
    margin-bottom: 3rem;
  }
  .badge {
    display: flex; align-items: center; gap: 0.5rem;
    color: rgba(245,237,214,0.8);
    font-size: 0.85rem;
    font-weight: 500;
  }
  .badge-icon { color: var(--green-light); font-size: 1.1rem; }

  .hero-ctas {
    display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;
  }

  .btn-primary {
    background: var(--terracotta);
    color: var(--white);
    padding: 1rem 2.25rem;
    border-radius: 2px;
    border: none;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.95rem;
    letter-spacing: 0.03em;
    transition: all 0.2s;
    display: inline-block;
    cursor: pointer;
    font-family: 'Inter', sans-serif;
  }
  .btn-primary:hover { background: #a86538; transform: translateY(-1px); }

  .btn-outline {
    background: transparent;
    color: var(--sand);
    border: 1.5px solid rgba(245,237,214,0.4);
    padding: 1rem 2.25rem;
    border-radius: 2px;
    text-decoration: none;
    font-weight: 500;
    font-size: 0.95rem;
    transition: all 0.2s;
    display: inline-block;
  }
  .btn-outline:hover { border-color: var(--sky); color: var(--sky); }

  /* SCROLL INDICATOR */
  .scroll-indicator {
    position: absolute; bottom: 2rem; left: 50%; transform: translateX(-50%);
    z-index: 2; display: flex; flex-direction: column; align-items: center; gap: 0.5rem;
    color: rgba(245,237,214,0.4); font-size: 0.7rem; letter-spacing: 0.1em;
    text-transform: uppercase;
    animation: bounce 2s infinite;
  }
  @keyframes bounce {
    0%, 100% { transform: translateX(-50%) translateY(0); }
    50% { transform: translateX(-50%) translateY(6px); }
  }

  /* SECTIONS */
  section { padding: 6rem 2rem; }

  .container { max-width: 1100px; margin: 0 auto; }

  .section-label {
    display: inline-block;
    color: var(--terracotta);
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    font-weight: 700;
    margin-bottom: 0.75rem;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 700;
    color: var(--green-deep);
    line-height: 1.2;
    margin-bottom: 1.25rem;
  }

  .section-lead {
    font-size: 1.05rem;
    color: var(--text-mid);
    max-width: 600px;
    margin-bottom: 3rem;
    line-height: 1.75;
  }

  /* ÜBER UNS / INTRO */
  .intro { background: var(--cream); }

  .intro-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: start;
  }

  .intro-visual { position: relative; }

  .intro-map-box {
    background: var(--green-deep);
    border-radius: 4px;
    padding: 2rem;
    color: var(--sand);
    position: relative;
    overflow: hidden;
  }

  .map-header {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    color: var(--sand);
    margin-bottom: 1rem;
    display: flex; align-items: center; gap: 0.5rem;
  }

  .map-embed {
    border-radius: 2px;
    overflow: hidden;
    height: 280px;
  }
  .map-embed iframe {
    width: 100%; height: 100%; border: none;
    filter: saturate(0.8);
  }

  .map-stats {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 1rem; margin-top: 1.25rem;
  }
  .map-stat {
    background: rgba(255,255,255,0.06);
    padding: 0.75rem 1rem;
    border-radius: 2px;
    border-left: 2px solid var(--sky);
  }
  .map-stat strong { display: block; color: var(--sky); font-size: 1.1rem; }
  .map-stat span { color: rgba(245,237,214,0.6); font-size: 0.8rem; }

  .info-cards {
    display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-top: 2rem;
  }
  .info-card {
    background: var(--white);
    border: 1px solid var(--sand-dark);
    padding: 1.25rem;
    border-radius: var(--radius);
    display: flex; gap: 0.75rem; align-items: flex-start;
  }
  .info-icon { font-size: 1.3rem; flex-shrink: 0; margin-top: 0.1rem; }
  .info-card h4 { font-size: 0.85rem; font-weight: 600; color: var(--green-deep); margin-bottom: 0.25rem; }
  .info-card p { font-size: 0.8rem; color: var(--text-mid); line-height: 1.5; }

  .intro-text-block {
    margin-top: 2rem; font-size: 0.95rem; color: var(--text-mid);
    line-height: 1.75; max-width: 540px;
  }

  /* UNTERKUNFT & AUSFLUGSZIELE (geteiltes Karten-Layout) */
  .unterkunft { background: var(--sand); }
  .ausflug { background: var(--cream); }

  .accommodation-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }

  .acc-card {
    background: var(--cream);
    border-radius: var(--radius);
    overflow: hidden;
    border: 1px solid var(--sand-dark);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .acc-card:hover { transform: translateY(-3px); box-shadow: 0 12px 30px rgba(0,0,0,0.1); }
  .ausflug .acc-card { background: var(--white); }

  .acc-header {
    background: var(--green-deep);
    padding: 1.5rem;
    position: relative;
  }
  .acc-icon { font-size: 2.5rem; margin-bottom: 0.5rem; display: block; }
  .acc-title {
    font-family: 'Playfair Display', serif;
    color: var(--sand);
    font-size: 1.2rem;
    font-weight: 700;
  }
  .acc-tag {
    position: absolute; top: 1rem; right: 1rem;
    background: var(--terracotta);
    color: white;
    font-size: 0.65rem;
    padding: 0.2rem 0.5rem;
    border-radius: 2px;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 600;
  }

  .acc-body { padding: 1.25rem; }
  .acc-price {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    color: var(--green-deep);
    font-weight: 700;
    margin-bottom: 0.25rem;
  }
  .acc-price-note { font-size: 0.75rem; color: var(--text-mid); margin-bottom: 1rem; }

  .acc-features { list-style: none; }
  .acc-features li {
    font-size: 0.83rem;
    color: var(--text-mid);
    padding: 0.3rem 0;
    border-bottom: 1px solid var(--sand-dark);
    display: flex; align-items: center; gap: 0.5rem;
  }
  .acc-features li:last-child { border-bottom: none; }
  .acc-features li::before { content: "✓"; color: var(--green-light); font-weight: 700; }

  .acc-text { font-size: 0.85rem; color: var(--text-mid); line-height: 1.6; margin-bottom: 0.75rem; }
  .acc-link { font-size: 0.8rem; color: var(--green-mid); font-weight: 600; text-decoration: none; }
  .acc-link:hover { color: var(--terracotta); }

  /* PREISE */
  .preise-section { background: var(--cream); }

  .price-table-wrap { overflow-x: auto; }
  .price-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.88rem;
  }
  .price-table th {
    background: var(--green-deep);
    color: var(--sand);
    padding: 0.9rem 1rem;
    text-align: left;
    font-weight: 600;
    font-size: 0.78rem;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }
  .price-table td {
    padding: 0.8rem 1rem;
    border-bottom: 1px solid var(--sand-dark);
    color: var(--text-dark);
    vertical-align: top;
  }
  .price-table tr:nth-child(even) td { background: var(--sand); }
  .price-table tr:hover td { background: rgba(82,183,136,0.06); }
  .price-highlight { color: var(--green-deep); font-weight: 700; font-size: 1rem; }
  .price-note-sm { font-size: 0.75rem; color: var(--text-mid); }

  .price-tabs {
    display: flex; gap: 0.5rem; flex-wrap: wrap; margin-bottom: 1.5rem;
  }
  .price-tab {
    padding: 0.5rem 1.1rem;
    border: 1.5px solid var(--sand-dark);
    background: transparent;
    border-radius: 2px;
    font-family: 'Inter', sans-serif;
    font-size: 0.8rem;
    font-weight: 600;
    cursor: pointer;
    color: var(--text-mid);
    transition: all 0.15s;
  }
  .price-tab.active { border-color: var(--green-deep); color: var(--green-deep); background: rgba(27,67,50,0.05); }

  .tab-content { display: none; }
  .tab-content.active { display: block; }

  .price-foot-note {
    margin-top: 1.25rem; font-size: 0.82rem; color: var(--text-mid);
    border-left: 3px solid var(--terracotta); padding-left: 1rem; line-height: 1.6;
  }

  /* FREIZEIT */
  .freizeit { background: var(--green-deep); color: var(--sand); }
  .freizeit .section-title { color: var(--sand); }
  .freizeit .section-label { color: var(--sky); }
  .freizeit .section-lead { color: rgba(245,237,214,0.7); }

  .activities-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;
  }

  .activity-card {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: var(--radius);
    padding: 1.5rem 1.25rem;
    transition: background 0.2s, transform 0.2s;
  }
  .activity-card:hover { background: rgba(255,255,255,0.1); transform: translateY(-2px); }

  .activity-emoji { font-size: 2rem; margin-bottom: 0.75rem; display: block; }
  .activity-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.05rem;
    color: var(--sand);
    margin-bottom: 0.4rem;
  }
  .activity-desc { font-size: 0.8rem; color: rgba(245,237,214,0.6); line-height: 1.55; }

  .highlight-strip {
    margin-top: 3rem; padding: 2rem;
    background: rgba(255,255,255,0.06);
    border-radius: var(--radius);
    border: 1px solid rgba(255,255,255,0.1);
  }
  .highlight-strip-inner { display: flex; gap: 1rem; align-items: flex-start; flex-wrap: wrap; }
  .highlight-item { flex: 1; min-width: 200px; }
  .highlight-label {
    color: var(--sky); font-size: 0.75rem; letter-spacing: 0.15em;
    text-transform: uppercase; font-weight: 600; margin-bottom: 0.4rem;
  }
  .highlight-text { font-size: 0.88rem; color: rgba(245,237,214,0.7); }

  /* KONTAKT */
  .kontakt { background: var(--sand); }

  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: start;
  }

  .contact-block { margin-bottom: 2rem; }
  .contact-label {
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--terracotta);
    font-weight: 700;
    margin-bottom: 0.5rem;
  }
  .contact-value {
    font-size: 1.05rem;
    color: var(--green-deep);
    font-weight: 500;
    line-height: 1.55;
  }
  .contact-value a { color: var(--green-deep); text-decoration: none; }
  .contact-value a:hover { color: var(--terracotta); }

  .opening-table { width: 100%; border-collapse: collapse; margin-top: 0.5rem; }
  .opening-table td { padding: 0.4rem 0; font-size: 0.9rem; color: var(--text-mid); }
  .opening-table td:first-child { color: var(--green-deep); font-weight: 600; width: 50%; }

  .anfahrt-box {
    background: var(--green-deep);
    border-radius: var(--radius);
    padding: 2rem;
    color: var(--sand);
  }
  .anfahrt-box h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    margin-bottom: 1rem;
    color: var(--sand);
  }
  .anfahrt-box p { font-size: 0.88rem; color: rgba(245,237,214,0.8); line-height: 1.65; margin-bottom: 0.9rem; }
  .anfahrt-box p:last-of-type { margin-bottom: 0; }

  .address-tag {
    background: rgba(255,255,255,0.07);
    border-left: 2px solid var(--sky);
    padding: 0.75rem 1rem;
    margin-top: 1.25rem;
    border-radius: 2px;
    font-size: 0.88rem;
    color: var(--sand);
  }
  .address-tag a { color: var(--sky); text-decoration: none; }

  /* BUCHUNGSFORMULAR */
  .booking-form-wrap {
    margin-top: 3rem; padding: 2rem;
    background: var(--white);
    border-radius: var(--radius);
    border: 1px solid var(--sand-dark);
  }
  .booking-form-wrap h3 {
    font-family: 'Playfair Display', serif;
    color: var(--green-deep);
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
  }
  .booking-form-note { font-size: 0.83rem; color: var(--text-mid); margin-bottom: 1.5rem; }
  .form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  .form-field { display: flex; flex-direction: column; gap: 0.35rem; }
  .form-field.full { grid-column: 1 / -1; }
  .form-field label {
    font-size: 0.72rem; letter-spacing: 0.08em; text-transform: uppercase;
    color: var(--green-deep); font-weight: 600;
  }
  .form-field input, .form-field textarea {
    font-family: 'Inter', sans-serif;
    font-size: 0.92rem;
    padding: 0.65rem 0.75rem;
    border: 1.5px solid var(--sand-dark);
    border-radius: 2px;
    background: var(--cream);
    color: var(--text-dark);
  }
  .form-field input:focus, .form-field textarea:focus {
    outline: none; border-color: var(--green-mid);
  }
  .form-field textarea { resize: vertical; min-height: 90px; }
  .form-submit-row { margin-top: 1.5rem; display: flex; align-items: center; gap: 1rem; flex-wrap: wrap; }
  .form-status { font-size: 0.83rem; color: var(--green-mid); }

  /* RESOURCE STRIP */
  .resource-strip {
    background: var(--green-mid);
    padding: 1.75rem 2rem;
    display: flex; align-items: center; justify-content: center;
    gap: 2rem; flex-wrap: wrap;
  }
  .resource-item {
    display: flex; align-items: center; gap: 0.6rem;
    color: var(--sand);
    text-decoration: none;
    font-size: 0.88rem;
    font-weight: 500;
    transition: color 0.2s;
  }
  .resource-item:hover { color: var(--sky); }
  .resource-icon { font-size: 1.2rem; }

  /* FOOTER */
  footer {
    background: var(--green-deep);
    color: rgba(245,237,214,0.6);
    padding: 3rem 2rem 2rem;
  }
  .footer-inner {
    max-width: 1100px; margin: 0 auto;
    display: grid; grid-template-columns: 2fr 1fr 1fr 1fr;
    gap: 3rem; margin-bottom: 2.5rem;
  }
  .footer-brand { }
  .footer-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    color: var(--sand);
    margin-bottom: 0.75rem;
  }
  .footer-logo span { color: var(--sky); }
  .footer-tagline { font-size: 0.83rem; line-height: 1.7; }

  .footer-col h4 {
    color: var(--sand);
    font-size: 0.75rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    font-weight: 700;
    margin-bottom: 1rem;
  }
  .footer-col a {
    display: block;
    color: rgba(245,237,214,0.55);
    text-decoration: none;
    font-size: 0.83rem;
    padding: 0.2rem 0;
    transition: color 0.15s;
  }
  .footer-col a:hover { color: var(--sky); }

  .footer-impressum {
    max-width: 1100px; margin: 0 auto 1.5rem;
    font-size: 0.78rem; line-height: 1.7;
    color: rgba(245,237,214,0.5);
    border-top: 1px solid rgba(255,255,255,0.08);
    padding-top: 1.5rem;
  }
  .footer-impressum strong { color: var(--sand); display: block; margin-bottom: 0.35rem; font-size: 0.72rem; letter-spacing: 0.1em; text-transform: uppercase; }
  .footer-impressum a { color: rgba(245,237,214,0.6); text-decoration: none; }

  .footer-bottom {
    max-width: 1100px; margin: 0 auto;
    border-top: 1px solid rgba(255,255,255,0.08);
    padding-top: 1.5rem;
    display: flex; justify-content: space-between; align-items: center;
    flex-wrap: wrap; gap: 1rem;
    font-size: 0.78rem;
  }
  .footer-bottom a { color: rgba(245,237,214,0.5); text-decoration: none; }
  .footer-bottom a:hover { color: var(--sky); }
  .footer-legal { display: flex; gap: 1.5rem; }

  /* WAVE ANIMATION */
  .wave-path {
    animation: wave 8s ease-in-out infinite;
    transform-origin: center bottom;
  }
  .wave-path2 {
    animation: wave 10s ease-in-out infinite reverse;
    transform-origin: center bottom;
    opacity: 0.6;
  }
  @keyframes wave {
    0%, 100% { d: path("M0,120 C200,60 400,180 600,100 C800,20 1000,140 1200,80 C1400,20 1600,120 1800,80 L1800,280 L0,280 Z"); }
    50% { d: path("M0,80 C200,140 400,60 600,120 C800,180 1000,60 1200,120 C1400,180 1600,80 1800,120 L1800,280 L0,280 Z"); }
  }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    .intro-grid, .contact-grid { grid-template-columns: 1fr; gap: 3rem; }
    .accommodation-grid { grid-template-columns: 1fr 1fr; }
    .activities-grid { grid-template-columns: 1fr 1fr; }
    .footer-inner { grid-template-columns: 1fr 1fr; }
    .nav-links { display: none; }
  }
  @media (max-width: 600px) {
    .accommodation-grid { grid-template-columns: 1fr; }
    .activities-grid { grid-template-columns: 1fr 1fr; }
    .footer-inner { grid-template-columns: 1fr; }
    section { padding: 4rem 1.25rem; }
    .info-cards, .form-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- NAVIGATION -->
<nav>
  <a href="#" class="nav-logo">Campingplatz<br><span>Wüllenheide</span></a>
  <ul class="nav-links">
    <li><a href="#unterkunft">Unterkunft</a></li>
    <li><a href="#preise">Preise</a></li>
    <li><a href="#freizeit">Freizeit</a></li>
    <li><a href="#ausflugsziele">Ausflugsziele</a></li>
    <li><a href="#kontakt">Kontakt</a></li>
    <li><a href="#kontakt" class="nav-cta">Buchungsanfrage</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-stars"></div>

  <svg class="lake-svg" viewBox="0 0 1800 280" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
    <path class="wave-path" d="M0,120 C200,60 400,180 600,100 C800,20 1000,140 1200,80 C1400,20 1600,120 1800,80 L1800,280 L0,280 Z" fill="#7EC8E3"/>
    <path class="wave-path2" d="M0,150 C300,90 500,200 800,130 C1100,60 1300,170 1800,110 L1800,280 L0,280 Z" fill="#2D6A4F"/>
  </svg>

  <div class="hero-content">
    <span class="hero-eyebrow">🏕️ Campingplatz Wüllenheide · Wilstedt bei Bremen</span>
    <h1>Mit Kind und Hund<br>mitten ins <em>Grüne</em></h1>
    <p class="hero-sub">Campingplatz Wüllenheide am östlichen Ortsrand von Wilstedt – rund 25 Kilometer vor den Toren Bremens, in der Nähe der Künstlerdörfer Fischerhude und Worpswede. Betrieben vom Camping Club Bremen e.V.</p>

    <div class="hero-badges">
      <span class="badge"><span class="badge-icon">🐾</span> Hunde willkommen</span>
      <span class="badge"><span class="badge-icon">🏊</span> Heidebad direkt nebenan</span>
      <span class="badge"><span class="badge-icon">🎣</span> Eigener Angelsee</span>
      <span class="badge"><span class="badge-icon">📶</span> Kostenloses WLAN</span>
    </div>

    <div class="hero-ctas">
      <a href="#kontakt" class="btn-primary">Buchungsanfrage senden</a>
      <a href="#unterkunft" class="btn-outline">Alle Unterkünfte</a>
    </div>
  </div>

  <div class="scroll-indicator">
    <span>Entdecken</span>
    <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
      <path d="M8 3v10M3 9l5 5 5-5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
    </svg>
  </div>
</section>

<!-- INTRO / ÜBER UNS -->
<section class="intro" id="info">
  <div class="container">
    <div class="intro-grid">
      <div>
        <span class="section-label">Unser Campingplatz</span>
        <h2 class="section-title">Herzlich willkommen auf dem Campingplatz Wüllenheide</h2>
        <p class="section-lead">Ruhig gelegen am östlichen Rand von Wilstedt, eingebettet in die Landschaft rund um die Künstlerdörfer Fischerhude und Worpswede – ideal für Familien, Senioren und alle, die Erholung im Grünen suchen.</p>

        <div class="info-cards">
          <div class="info-card">
            <span class="info-icon">📍</span>
            <div>
              <h4>Lage</h4>
              <p>An der Reitbahn 4, 27412 Wilstedt – ca. 25 km vor den Toren Bremens</p>
            </div>
          </div>
          <div class="info-card">
            <span class="info-icon">📞</span>
            <div>
              <h4>Kontakt</h4>
              <p><a href="tel:+4917665527411">0176 65 52 74 11</a><br><a href="mailto:1.vorsitzender@camping-club-bremen.de">1.vorsitzender@camping-club-bremen.de</a></p>
            </div>
          </div>
          <div class="info-card">
            <span class="info-icon">🗓️</span>
            <div>
              <h4>Saisonbetrieb</h4>
              <p>Geöffnet vom 01.04. bis 30.09.</p>
            </div>
          </div>
          <div class="info-card">
            <span class="info-icon">🕐</span>
            <div>
              <h4>Anreise</h4>
              <p>Täglich von 15:00 bis 20:00 Uhr</p>
            </div>
          </div>
        </div>

        <p class="intro-text-block">Direkt nebenan begrüßt Sie das beheizte Heidebad der Gemeinde mit Kinderbecken, Rutschen und Beachvolleyballfeld. Auf dem Platz selbst warten ein eigener Angelsee, ein Spielplatz und ein Aufenthaltsraum für Regentage – dazu kostenloses WLAN für alle Gäste. Einkaufsmöglichkeiten finden Sie in unmittelbarer Nähe, Rad- und Wanderwege, Reiterhöfe und ein Tennisplatz laden zu Ausflügen ein. Auch Bremen, Bremerhaven und Hamburg sind als Tagesausflugsziele gut zu erreichen. Im DCC-Campingführer finden Sie uns unter der Nummer 2280.</p>
      </div>

      <div class="intro-visual">
        <div class="intro-map-box">
          <div class="map-header">📍 So finden Sie uns</div>
          <div class="map-embed">
            <iframe
              src="https://www.google.com/maps?q=53.187562,9.104299&z=14&output=embed"
              allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade">
            </iframe>
          </div>
          <div class="map-stats">
            <div class="map-stat">
              <strong>DCC Nr. 2280</strong>
              <span>im Campingführer</span>
            </div>
            <div class="map-stat">
              <strong>~25 km</strong>
              <span>vor den Toren Bremens</span>
            </div>
            <div class="map-stat">
              <strong>&lt; 10 m</strong>
              <span>zum Heidebad</span>
            </div>
            <div class="map-stat">
              <strong>01.04.–30.09.</strong>
              <span>Saisonbetrieb</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- UNTERKUNFT -->
<section class="unterkunft" id="unterkunft">
  <div class="container">
    <span class="section-label">Campingangebot</span>
    <h2 class="section-title">Ihre Unterkunft in Wilstedt</h2>
    <p class="section-lead">Vom einfachen Zeltplatz bis zum eigenen Dauerplatz – passend für jeden Aufenthalt.</p>

    <div class="accommodation-grid">
      <!-- Zeltplatz -->
      <div class="acc-card">
        <div class="acc-header">
          <span class="acc-icon">⛺</span>
          <div class="acc-title">Zeltplatz</div>
        </div>
        <div class="acc-body">
          <div class="acc-price">8,00 €</div>
          <div class="acc-price-note">pro Nacht · zzgl. Personengebühr</div>
          <ul class="acc-features">
            <li>Stellplatzgebühr Zelt: 8,00 €/Nacht</li>
            <li>Personengebühr: 8,00 €/Person und Nacht</li>
            <li>Strom (ohne E-Bike/Kühlbox): 2,00 €/Nacht</li>
            <li>Hund: 2,00 € pro Nacht</li>
          </ul>
        </div>
      </div>

      <!-- Stellplatz Wohnwagen/Wohnmobil -->
      <div class="acc-card">
        <div class="acc-header">
          <span class="acc-icon">🚐</span>
          <div class="acc-title">Stellplatz Wohnwagen / Wohnmobil</div>
          <span class="acc-tag">Beliebt</span>
        </div>
        <div class="acc-body">
          <div class="acc-price">13,00 €</div>
          <div class="acc-price-note">pro Nacht · zzgl. Personengebühr</div>
          <ul class="acc-features">
            <li>Stellplatzgebühr: 13,00 €/Nacht</li>
            <li>Personengebühr: 8,00 €/Person und Nacht</li>
            <li>Strom: 4,00 €/Nacht</li>
            <li>Laden E-Auto: 0,70 €/kWh nach Verbrauch</li>
          </ul>
        </div>
      </div>

      <!-- Mietwohnwagen -->
      <div class="acc-card">
        <div class="acc-header">
          <span class="acc-icon">🛻</span>
          <div class="acc-title">Mietwohnwagen</div>
        </div>
        <div class="acc-body">
          <div class="acc-price">30,00 €</div>
          <div class="acc-price-note">pro Nacht, inkl. Strom · zzgl. Personengebühr</div>
          <ul class="acc-features">
            <li>Personengebühr Gäste: 8,00 €/Nacht</li>
            <li>Personengebühr DCC-Mitglieder: 5,00 €/Nacht</li>
            <li>Einmalige Endreinigung: 25,00 €</li>
            <li>Sanitäranlagen im zentralen Gebäude</li>
          </ul>
        </div>
      </div>

      <!-- Dauerplatz -->
      <div class="acc-card">
        <div class="acc-header">
          <span class="acc-icon">🏞️</span>
          <div class="acc-title">Dauerplatz</div>
          <span class="acc-tag">Auf Anfrage</span>
        </div>
        <div class="acc-body">
          <div class="acc-price">Preis auf Anfrage</div>
          <div class="acc-price-note">Verpachtung langfristiger Stellplätze</div>
          <ul class="acc-features">
            <li>Stellplatzgrößen von 95 bis 200 m²</li>
            <li>Inkl. 2 Erwachsene und eigene Kinder</li>
            <li>Inkl. Caravan und Auto</li>
            <li>Anfragen gern über das Kontaktformular</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PREISE -->
<section class="preise-section" id="preise">
  <div class="container">
    <span class="section-label">Übersicht</span>
    <h2 class="section-title">Preise 2026</h2>
    <p class="section-lead">Alle Preise auf einen Blick – transparent und fair.</p>

    <div class="price-tabs">
      <button class="price-tab active" onclick="setTab('standard', this)">Standardpreise</button>
      <button class="price-tab" onclick="setTab('dcc', this)">DCC-Vorteilsplatz</button>
      <button class="price-tab" onclick="setTab('mietwohnwagen', this)">Mietwohnwagen</button>
      <button class="price-tab" onclick="setTab('dauerplatz', this)">Dauerplätze</button>
    </div>

    <!-- STANDARDPREISE -->
    <div class="tab-content active" id="tab-standard">
      <div class="price-table-wrap">
        <table class="price-table">
          <thead>
            <tr><th>Leistung</th><th>Einheit</th><th>Preis</th></tr>
          </thead>
          <tbody>
            <tr><td>Stellplatzgebühr (Wohnwagen/Wohnmobil)</td><td>pro Nacht</td><td><span class="price-highlight">13,00 €</span></td></tr>
            <tr><td>Stellplatzgebühr Zelt</td><td>pro Nacht</td><td><span class="price-highlight">8,00 €</span></td></tr>
            <tr><td>Personengebühr</td><td>pro Person und Nacht</td><td><span class="price-highlight">8,00 €</span></td></tr>
            <tr><td>Strom Wohnwagen/Wohnmobil</td><td>pro Nacht</td><td><span class="price-highlight">4,00 €</span></td></tr>
            <tr><td>Strom Zelt (ohne E-Bike/Kühlbox)</td><td>pro Nacht</td><td><span class="price-highlight">2,00 €</span></td></tr>
            <tr><td>Hund</td><td>pro Hund und Nacht</td><td><span class="price-highlight">2,00 €</span></td></tr>
            <tr><td>Abfallbeutel</td><td>pro Stück</td><td><span class="price-highlight">2,00 €</span></td></tr>
            <tr><td>Laden E-Auto</td><td>nach Verbrauch je kWh</td><td><span class="price-highlight">0,70 €</span></td></tr>
          </tbody>
        </table>
      </div>
      <p class="price-foot-note">Rezeption geöffnet vom 01.04. bis 30.09. Anreise täglich von 15:00 bis 20:00 Uhr. Hunde sind bei uns herzlich willkommen – bitte auf dem gesamten Platz an der Leine führen und Hinterlassenschaften entfernen.</p>
    </div>

    <!-- DCC -->
    <div class="tab-content" id="tab-dcc">
      <p style="margin-bottom:1.25rem; font-size:0.92rem; color:var(--text-mid);">Mitglieder des Deutschen Camping-Clubs e.V. (DCC) profitieren auf unserem DCC-Vorteilsplatz-PLUS von Sonderkonditionen.</p>
      <div class="price-table-wrap">
        <table class="price-table">
          <thead>
            <tr><th>Zeitraum</th><th>Saison</th><th>Preis</th></tr>
          </thead>
          <tbody>
            <tr><td>01.04. – 15.06. &amp; 15.09. – 30.09.</td><td>Nebensaison</td><td><span class="price-highlight">19,00 €/Tag</span> <span class="price-note-sm">zzgl. Strom</span></td></tr>
            <tr><td>16.06. – 14.09.</td><td>Hauptsaison</td><td><span class="price-highlight">21,00 €/Tag</span> <span class="price-note-sm">zzgl. Strom</span></td></tr>
            <tr><td>Ganzjährig (ab 5 Einheiten/Tag)</td><td>Gruppenpreis</td><td><span class="price-highlight">17,00 €/Tag</span> <span class="price-note-sm">je Einheit, zzgl. Strom</span></td></tr>
          </tbody>
        </table>
      </div>
      <p class="price-foot-note">Die Preise gelten pro Nacht und pro Gespann / Wohnmobil / Zelt / Familie bzw. Großeltern mit Kindern bis 18 Jahre. Jede weitere volljährige Person wird mit 5,00 € berechnet. Die Legitimation erfolgt ausschließlich über eine gültige DCC-Karte bei Anreise – ohne Karte kann keine Vergünstigung gewährt werden.</p>
    </div>

    <!-- MIETWOHNWAGEN -->
    <div class="tab-content" id="tab-mietwohnwagen">
      <div class="price-table-wrap">
        <table class="price-table">
          <thead>
            <tr><th>Leistung</th><th>Preis</th></tr>
          </thead>
          <tbody>
            <tr><td>Wohnwagenmiete, inkl. Strom</td><td><span class="price-highlight">30,00 €</span> <span class="price-note-sm">pro Nacht, zzgl. Personengebühr</span></td></tr>
            <tr><td>Personengebühr Gäste</td><td><span class="price-highlight">8,00 €</span> <span class="price-note-sm">pro Nacht</span></td></tr>
            <tr><td>Personengebühr DCC-Mitglieder</td><td><span class="price-highlight">5,00 €</span> <span class="price-note-sm">pro Nacht</span></td></tr>
            <tr><td>Endreinigung</td><td><span class="price-highlight">25,00 €</span> <span class="price-note-sm">einmalig</span></td></tr>
            <tr><td>Abfallbeutel</td><td><span class="price-highlight">2,00 €</span> <span class="price-note-sm">pro Stück</span></td></tr>
          </tbody>
        </table>
      </div>
      <p class="price-foot-note">Für die Toilettennutzung steht das Sanitärgebäude zur Verfügung, davor finden Sie ein Abwaschbecken. Am Abreisetag bitten wir, den Wohnwagen bis 14:00 Uhr zu räumen und Bettlaken sowie Bezüge ins Bad zu legen.</p>
    </div>

    <!-- DAUERPLÄTZE -->
    <div class="tab-content" id="tab-dauerplatz">
      <div class="price-table-wrap">
        <table class="price-table">
          <thead>
            <tr><th>Leistung</th><th>Details</th></tr>
          </thead>
          <tbody>
            <tr><td>Stellplatzgröße</td><td>95 – 200 m²</td></tr>
            <tr><td>Inklusive</td><td>2 Erwachsene, eigene Kinder, Caravan und Auto</td></tr>
            <tr><td>Preis</td><td><span class="price-highlight">auf Anfrage</span></td></tr>
          </tbody>
        </table>
      </div>
      <p class="price-foot-note">Bei Interesse an einem Dauerplatz melden Sie sich gerne über unser <a href="#kontakt" style="color:var(--green-deep); font-weight:600;">Kontaktformular</a> – wir finden den passenden Stellplatz für Sie.</p>
    </div>
  </div>
</section>

<!-- FREIZEIT -->
<section class="freizeit" id="freizeit">
  <div class="container">
    <span class="section-label">Vor Ort &amp; in der Umgebung</span>
    <h2 class="section-title">Freizeit für die ganze Familie</h2>
    <p class="section-lead">Vom Schwimmbad direkt nebenan bis zum eigenen Angelsee – bei uns wird es nicht langweilig.</p>

    <div class="activities-grid">
      <div class="activity-card">
        <span class="activity-emoji">🏊</span>
        <div class="activity-name">Heidebad nebenan</div>
        <div class="activity-desc">Keine 10 Meter vom Eingang entfernt: Schwimmbecken, Babybecken, Rutschen und Beachvolleyballfeld.</div>
      </div>
      <div class="activity-card">
        <span class="activity-emoji">🎣</span>
        <div class="activity-name">Angelsee</div>
        <div class="activity-desc">Eigener Angelsee direkt auf dem Gelände für entspannte Stunden am Wasser.</div>
      </div>
      <div class="activity-card">
        <span class="activity-emoji">🛝</span>
        <div class="activity-name">Spielplatz</div>
        <div class="activity-desc">Gut ausgestatteter Spielplatz auf dem Campingplatz für die jüngsten Gäste.</div>
      </div>
      <div class="activity-card">
        <span class="activity-emoji">🏠</span>
        <div class="activity-name">Aufenthaltsraum</div>
        <div class="activity-desc">Überdachter Rückzugsort, in dem Kinder auch an Regentagen spielen können.</div>
      </div>
      <div class="activity-card">
        <span class="activity-emoji">📶</span>
        <div class="activity-name">Kostenloses WLAN</div>
        <div class="activity-desc">Für alle Gäste auf dem gesamten Platz verfügbar.</div>
      </div>
      <div class="activity-card">
        <span class="activity-emoji">🏓</span>
        <div class="activity-name">Sport &amp; Spiel</div>
        <div class="activity-desc">Gartenschach, Basketballkörbe und Tischtennisplatten im Bereich des Heidebads.</div>
      </div>
      <div class="activity-card">
        <span class="activity-emoji">🚴</span>
        <div class="activity-name">Rad- &amp; Wanderwege</div>
        <div class="activity-desc">Schöne Strecken ab dem Platz, dazu Reiterhöfe und ein Tennisplatz in der Nähe.</div>
      </div>
      <div class="activity-card">
        <span class="activity-emoji">⛪</span>
        <div class="activity-name">Pilgerkapelle</div>
        <div class="activity-desc">Gemeinsam mit der Kirchengemeinde eingeweihte Kapelle am Mönchsweg – offen für Mitglieder, Dauercamper und Tagesgäste.</div>
      </div>
    </div>

    <div class="highlight-strip">
      <div class="highlight-strip-inner">
        <div class="highlight-item">
          <div class="highlight-label">DCC-Vorteilsplatz-PLUS</div>
          <p class="highlight-text">Mitglieder des Deutschen Camping-Clubs profitieren je Saison von Sonderpreisen.</p>
        </div>
        <div class="highlight-item">
          <div class="highlight-label">Hunde willkommen</div>
          <p class="highlight-text">Anleinpflicht auf dem gesamten Platz – bitte Hinterlassenschaften entfernen.</p>
        </div>
        <div class="highlight-item">
          <div class="highlight-label">Einkaufen &amp; Versorgung</div>
          <p class="highlight-text">Einkaufsmöglichkeiten befinden sich in unmittelbarer Nähe zum Platz.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- AUSFLUGSZIELE -->
<section class="ausflug" id="ausflugsziele">
  <div class="container">
    <span class="section-label">In der Region</span>
    <h2 class="section-title">Ausflugsziele rund um Wilstedt</h2>
    <p class="section-lead">Von Künstlerdörfern bis zum Wissenschaftszentrum – eine Auswahl an Zielen, deren Besuch sich lohnt.</p>

    <div class="accommodation-grid">
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🦌</span><div class="acc-title">Tiergarten Ludwigslust</div></div>
        <div class="acc-body">
          <p class="acc-text">Kompakter Tierpark auf rund 4 Hektar mit etwa 200 Tieren aus 50 Arten – von Flamingos und Lamas bis zu Kranichen.</p>
          <a href="http://www.tiergarten-ludwigslust.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🎨</span><div class="acc-title">Künstlerdorf Worpswede</div></div>
        <div class="acc-body">
          <p class="acc-text">Seit mehr als 120 Jahren Künstlerkolonie, geprägt vom Weyerberg und der weiten norddeutschen Landschaft.</p>
          <a href="http://www.worpswede.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🖌️</span><div class="acc-title">Künstlerdorf Fischerhude</div></div>
        <div class="acc-body">
          <p class="acc-text">Heimat von Malern, Bildhauern und Musikern seit 1895 – unter anderem mit dem Otto-Modersohn-Museum.</p>
          <a href="http://www.fischerhude.com/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🌾</span><div class="acc-title">Teufelsmoor</div></div>
        <div class="acc-body">
          <p class="acc-text">Die einst karge Moorlandschaft rund um Worpswede lädt heute zu weiten Wanderungen durch die Kulturlandschaft ein.</p>
          <a href="http://www.kulturland-teufelsmoor.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🚣</span><div class="acc-title">Torfkahnfahrt</div></div>
        <div class="acc-body">
          <p class="acc-text">Geführte Bootstour mit unterhaltsamen Einblicken in die Geschichte der Moorlandschaft von der Eiszeit bis heute.</p>
          <a href="http://www.torfkahnfahrt.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🔬</span><div class="acc-title">Universum Bremen</div></div>
        <div class="acc-body">
          <p class="acc-text">Wissenschafts-Erlebniszentrum mit über 300 Mitmach-Stationen zu Mensch, Erde und Kosmos.</p>
          <a href="http://universum-bremen.de/de/startseite.html" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🌺</span><div class="acc-title">Rhododendronpark Bremen</div></div>
        <div class="acc-body">
          <p class="acc-text">46 Hektar Botanischer Garten mit einer der größten Rhododendron-Sammlungen weltweit und dem Science Center botanika.</p>
          <a href="http://rhododendronpark-bremen.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🦜</span><div class="acc-title">Weltvogelpark Walsrode</div></div>
        <div class="acc-body">
          <p class="acc-text">Der weltweit größte Vogelpark mit über 4.000 Vögeln aus 650 Arten auf 24 Hektar Erlebnislandschaft.</p>
          <a href="http://www.weltvogelpark.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🔭</span><div class="acc-title">Olbers-Planetarium Bremen</div></div>
        <div class="acc-body">
          <p class="acc-text">Seit 1952 in Betrieb und das meistbesuchte 6-Meter-Planetarium Deutschlands mit rund 1.400 Veranstaltungen im Jahr.</p>
          <a href="http://planetarium.hs-bremen.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🏛️</span><div class="acc-title">Samtgemeinde Zeven</div></div>
        <div class="acc-body">
          <p class="acc-text">Zwischen Hamburg und Bremen an der A1 gelegen, mit einer einladenden Fußgängerzone und Parklandschaft.</p>
          <a href="http://www.zeven.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
      <div class="acc-card">
        <div class="acc-header"><span class="acc-icon">🌴</span><div class="acc-title">Erlebnisbad Ronolulu</div></div>
        <div class="acc-body">
          <p class="acc-text">Badespaß und Sauna-Oase bei jedem Wetter – einmal zahlen, den ganzen Tag genießen.</p>
          <a href="http://www.ronolulu.de/" target="_blank" class="acc-link">→ Mehr erfahren</a>
        </div>
      </div>
    </div>

    <p style="margin-top:2rem; font-size:0.88rem; color:var(--text-mid);">Allgemeine Informationen zur Gemeinde Wilstedt und zur Hansestadt Bremen finden Sie unter <a href="http://wilstedt.de/" target="_blank" style="color:var(--green-mid); font-weight:600;">wilstedt.de</a> und <a href="http://bremen.de/" target="_blank" style="color:var(--green-mid); font-weight:600;">bremen.de</a>.</p>
  </div>
</section>

<!-- KONTAKT -->
<section class="kontakt" id="kontakt">
  <div class="container">
    <span class="section-label">So erreichen Sie uns</span>
    <h2 class="section-title">Kontakt &amp; Anfahrt</h2>

    <div class="contact-grid">
      <div>
        <div class="contact-block">
          <div class="contact-label">Adresse</div>
          <div class="contact-value">
            Campingplatz Wüllenheide<br>
            Camping Club Bremen e.V.<br>
            An der Reitbahn 4<br>
            27412 Wilstedt
          </div>
        </div>

        <div class="contact-block">
          <div class="contact-label">Telefon &amp; E-Mail</div>
          <div class="contact-value">
            <a href="tel:+4917665527411">Für Rückfragen: 0176 65 52 74 11</a><br>
            <a href="mailto:1.vorsitzender@camping-club-bremen.de">1.vorsitzender@camping-club-bremen.de</a>
          </div>
        </div>

        <div class="contact-block">
          <div class="contact-label">Saison &amp; Anreise</div>
          <table class="opening-table">
            <tr><td>Saisonbetrieb</td><td>01.04. – 30.09.</td></tr>
            <tr><td>Anreise</td><td>Täglich 15:00 – 20:00 Uhr</td></tr>
          </table>
        </div>
      </div>

      <div>
        <div class="anfahrt-box">
          <h3>🗺️ So erreichen Sie uns</h3>
          <p>Wilstedt liegt rund 25 Kilometer nordöstlich von Bremen, in der Nähe der Künstlerdörfer Fischerhude und Worpswede – gut über die Autobahn A1 und die B75 zu erreichen.</p>
          <p>Der Campingplatz liegt am östlichen Ortsrand von Wilstedt, direkt neben dem Heidebad. Für die genaue Anfahrt empfehlen wir die Navigation zur Adresse An der Reitbahn 4.</p>
          <div class="address-tag">
            📍 An der Reitbahn 4, 27412 Wilstedt<br>
            <a href="https://www.google.com/maps/search/?api=1&query=53.187562,9.104299" target="_blank">In Google Maps öffnen →</a>
          </div>
        </div>

        <div style="margin-top:1.5rem; padding:1.5rem; background:var(--white); border-radius:var(--radius); border:1px solid var(--sand-dark);">
          <h4 style="font-family:'Playfair Display',serif; font-size:1rem; color:var(--green-deep); margin-bottom:0.75rem;">📄 Links &amp; Dokumente</h4>
          <div style="display:flex; gap:0.75rem; flex-direction:column;">
            <a href="https://www.campingplatz-wuellenheide.de/app/download/5793768809/2013_Lageplan_01.pdf" target="_blank" style="color:var(--green-mid); text-decoration:none; font-size:0.85rem;">→ Lageplan (PDF)</a>
            <a href="http://www.heidebad-wilstedt.de/" target="_blank" style="color:var(--green-mid); text-decoration:none; font-size:0.85rem;">→ Heidebad Wilstedt</a>
            <a href="https://www.camping-club.de/" target="_blank" style="color:var(--green-mid); text-decoration:none; font-size:0.85rem;">→ Deutscher Camping-Club e.V. (Dachverband)</a>
          </div>
        </div>
      </div>
    </div>

    <!-- BUCHUNGSFORMULAR -->
    <div class="booking-form-wrap">
      <h3>Buchungsanfrage</h3>
      <p class="booking-form-note">Füllen Sie das Formular aus – beim Absenden öffnet sich Ihr E-Mail-Programm mit einer vorausgefüllten Nachricht an uns.</p>
      <form id="buchungsformular" onsubmit="return sendBooking(event)">
        <div class="form-grid">
          <div class="form-field">
            <label for="vorname">Vorname *</label>
            <input type="text" id="vorname" required>
          </div>
          <div class="form-field">
            <label for="nachname">Name *</label>
            <input type="text" id="nachname" required>
          </div>
          <div class="form-field full">
            <label for="email">E-Mail-Adresse *</label>
            <input type="email" id="email" required>
          </div>
          <div class="form-field">
            <label for="unterkunftsart">Wohnwagen / Zelt / Mobile Home</label>
            <input type="text" id="unterkunftsart" placeholder="z. B. Wohnwagen">
          </div>
          <div class="form-field">
            <label for="dauerplatz-interesse">Interesse an Dauerplatz?</label>
            <input type="text" id="dauerplatz-interesse" placeholder="Ja / Nein">
          </div>
          <div class="form-field">
            <label for="anreise">Anreise *</label>
            <input type="date" id="anreise" required>
          </div>
          <div class="form-field">
            <label for="abreise">Abreise *</label>
            <input type="date" id="abreise" required>
          </div>
          <div class="form-field">
            <label for="personen">Anzahl Personen über 18</label>
            <input type="number" id="personen" min="0">
          </div>
          <div class="form-field">
            <label for="kinder">Anzahl Kinder</label>
            <input type="number" id="kinder" min="0">
          </div>
          <div class="form-field full">
            <label for="nachricht">Nachricht</label>
            <textarea id="nachricht" placeholder="Ihre Anfrage oder besonderen Wünsche..."></textarea>
          </div>
        </div>
        <div class="form-submit-row">
          <button type="submit" class="btn-primary">Buchungsanfrage senden</button>
          <span class="form-status" id="form-status"></span>
        </div>
      </form>
    </div>
  </div>
</section>

<!-- RESOURCE STRIP -->
<div class="resource-strip">
  <a href="http://www.heidebad-wilstedt.de/" class="resource-item" target="_blank">
    <span class="resource-icon">🏊</span> Heidebad Wilstedt
  </a>
  <a href="https://www.camping-club.de/" class="resource-item" target="_blank">
    <span class="resource-icon">🎪</span> Deutscher Camping-Club
  </a>
  <a href="http://wilstedt.de/" class="resource-item" target="_blank">
    <span class="resource-icon">🏘️</span> Gemeinde Wilstedt
  </a>
  <a href="mailto:1.vorsitzender@camping-club-bremen.de" class="resource-item" target="_blank">
    <span class="resource-icon">✉️</span> E-Mail schreiben
  </a>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-brand">
      <div class="footer-logo">Campingplatz<br><span>Wüllenheide</span></div>
      <p class="footer-tagline">Mit Kind und Hund mitten ins Grüne. Geöffnet vom 01.04. bis 30.09. am östlichen Ortsrand von Wilstedt, direkt neben dem Heidebad.<br><br>An der Reitbahn 4 · 27412 Wilstedt<br>Camping Club Bremen e.V.</p>
    </div>
    <div class="footer-col">
      <h4>Unterkunft</h4>
      <a href="#unterkunft">Zeltplatz</a>
      <a href="#unterkunft">Stellplätze</a>
      <a href="#unterkunft">Mietwohnwagen</a>
      <a href="#unterkunft">Dauerplätze</a>
    </div>
    <div class="footer-col">
      <h4>Freizeit &amp; Region</h4>
      <a href="#freizeit">Heidebad</a>
      <a href="#freizeit">Angelsee &amp; Spielplatz</a>
      <a href="#freizeit">Pilgerkapelle</a>
      <a href="#ausflugsziele">Ausflugsziele</a>
    </div>
    <div class="footer-col">
      <h4>Informationen</h4>
      <a href="#preise">Preise</a>
      <a href="#kontakt">Kontakt &amp; Anfahrt</a>
      <a href="#kontakt">Buchungsanfrage</a>
      <a href="https://www.campingplatz-wuellenheide.de/app/download/5793768809/2013_Lageplan_01.pdf" target="_blank">Lageplan (PDF)</a>
    </div>
  </div>

  <div class="footer-impressum" id="impressum">
    <strong>Impressum</strong>
    Verantwortlich: Camping Club Bremen e.V., 1. Vorsitzender Michael Woltmann · Föhrenstr. 65 · 28207 Bremen · E-Mail: <a href="mailto:1.vorsitzender@camping-club-bremen.de">1.vorsitzender@camping-club-bremen.de</a>
  </div>

  <div class="footer-bottom">
    <span>© 2026 Campingplatz Wüllenheide · Camping Club Bremen e.V.</span>
    <div class="footer-legal">
      <a href="#impressum">Impressum</a>
    </div>
  </div>
</footer>

<script>
  // Price tabs
  function setTab(tab, btn) {
    document.querySelectorAll('.price-tab').forEach(b => b.classList.remove('active'));
    document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
    btn.classList.add('active');
    document.getElementById('tab-' + tab).classList.add('active');
  }

  // Buchungsformular -> mailto
  function sendBooking(e) {
    e.preventDefault();
    const vorname = document.getElementById('vorname').value;
    const nachname = document.getElementById('nachname').value;
    const email = document.getElementById('email').value;
    const unterkunftsart = document.getElementById('unterkunftsart').value;
    const dauerplatz = document.getElementById('dauerplatz-interesse').value;
    const anreise = document.getElementById('anreise').value;
    const abreise = document.getElementById('abreise').value;
    const personen = document.getElementById('personen').value;
    const kinder = document.getElementById('kinder').value;
    const nachricht = document.getElementById('nachricht').value;

    const body =
      'Vorname: ' + vorname + '\n' +
      'Name: ' + nachname + '\n' +
      'E-Mail: ' + email + '\n' +
      'Wohnwagen/Zelt/Mobile Home: ' + unterkunftsart + '\n' +
      'Interesse an Dauerplatz: ' + dauerplatz + '\n' +
      'Anreise: ' + anreise + '\n' +
      'Abreise: ' + abreise + '\n' +
      'Personen über 18: ' + personen + '\n' +
      'Kinder: ' + kinder + '\n\n' +
      'Nachricht:\n' + nachricht;

    const mailtoLink = 'mailto:1.vorsitzender@camping-club-bremen.de?subject=' +
      encodeURIComponent('Buchungsanfrage Campingplatz Wüllenheide') +
      '&body=' + encodeURIComponent(body);

    window.location.href = mailtoLink;
    document.getElementById('form-status').textContent = 'Ihr E-Mail-Programm wird geöffnet …';
    return false;
  }

  // Smooth nav highlight
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a');
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(s => {
      if (window.scrollY >= s.offsetTop - 100) current = s.id;
    });
    navLinks.forEach(a => {
      a.style.color = a.getAttribute('href') === '#' + current
        ? 'var(--sky)' : '';
    });
  });
</script>
</body>
</html>
