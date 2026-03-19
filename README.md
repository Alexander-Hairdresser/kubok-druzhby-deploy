[kubok-druzhby-github.html](https://github.com/user-attachments/files/26128714/kubok-druzhby-github.html)
<!DOCTYPE html>
<!-- v3.2 -->
<html lang="ru">
<head>
<!--
   ______                            __
  / ____/___  ____ ___  ____  __  __/ /____  _____
 / /   / __ \/ __ `__ \/ __ \/ / / / __/ _ \/ ___/
/ /___/ /_/ / / / / / / /_/ / /_/ / /_/  __/ /
\____/\____/_/ /_/ /_/ .___/\__,_/\__/\___/_/
                    /_/
        Официальный цифровой проект турнира
        Разработка: Alexander Rum
        Креативная команда: "Темная лошадка", Смоленск
-->
<meta name="generator" content="Alexander Rum">
<meta name="author" content="Разработка: Alexander Rum; Креативная команда: Темная лошадка, Смоленск">

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>КУБОК ДРУЖБЫ 2026 — Официальный турнирный портал</title>
<meta name="description" content="Официальный сайт турнира КУБОК ДРУЖБЫ 2026. Расписание матчей, турнирная таблица, информация о командах.">

<!-- Fonts -->
<link rel="preconnect" href="https://api.fontshare.com" crossorigin>
<link href="https://api.fontshare.com/v2/css?f[]=clash-display@200,300,400,500,600,700&f[]=general-sans@200,300,400,500,600,700&display=swap" rel="stylesheet">

<style>
/* ========== CSS RESET & BASE ========== */
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; -webkit-text-size-adjust: 100%; }

:root {
  /* Primary Palette */
  --navy-900: #070e1a;
  --navy-800: #0a1628;
  --navy-700: #0f2347;
  --navy-600: #152d5a;
  --navy-500: #1a3a6e;
  --navy-400: #234b8a;
  --navy-300: #3366aa;

  /* Orange Accents (replacing gold) */
  --orange-500: #e87a3a;
  --orange-400: #f08c50;
  --orange-300: #f5a070;
  --orange-200: #fbb990;
  --orange-100: #fdd4b8;

  /* Neutrals */
  --white: #ffffff;
  --gray-100: #f0f2f5;
  --gray-200: #d8dce5;
  --gray-300: #b0b8c8;
  --gray-400: #8892a6;
  --gray-500: #606b82;
  --gray-600: #3d4660;

  /* Semantic */
  --success: #2ecc71;
  --warning: #f39c12;
  --danger: #e74c3c;
  --info: #3498db;

  /* Glassmorphism */
  --glass-bg: rgba(15, 35, 71, 0.6);
  --glass-border: rgba(232, 122, 58, 0.15);
  --glass-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);

  /* Typography */
  --font-display: 'Clash Display', sans-serif;
  --font-body: 'General Sans', sans-serif;

  /* Spacing */
  --section-pad: clamp(3rem, 8vw, 6rem);
  --content-max: 1200px;
  --card-radius: 16px;
  --card-radius-sm: 10px;
}

body {
  font-family: var(--font-body);
  background: var(--navy-900);
  color: var(--white);
  line-height: 1.6;
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
}

/* ========== UTILITY ========== */
.container {
  max-width: var(--content-max);
  margin: 0 auto;
  padding: 0 clamp(1rem, 4vw, 2rem);
}

.section-title {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: clamp(1.75rem, 5vw, 2.5rem);
  color: var(--orange-400);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: 0.25em;
}

.section-subtitle {
  font-size: clamp(0.9rem, 2.5vw, 1.05rem);
  color: var(--gray-400);
  margin-bottom: 2.5rem;
}

.orange-line {
  width: 60px;
  height: 3px;
  background: linear-gradient(90deg, var(--orange-500), var(--orange-300));
  border-radius: 2px;
  margin-bottom: 1rem;
}

/* ========== FLOATING BALL MENU ========== */
.menu-ball {
  position: fixed;
  bottom: 1.5rem;
  right: 1.5rem;
  z-index: 2000;
  width: 62px;
  height: 62px;
  border-radius: 50%;
  background: radial-gradient(circle at 38% 32%, #c8956a, #a06b3e 40%, #7a4f2a 70%, #5a3a1e);
  border: 2px solid rgba(160, 107, 62, 0.6);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 20px rgba(90, 58, 30, 0.5), inset 0 2px 4px rgba(255,220,180,0.25), inset 0 -2px 4px rgba(0,0,0,0.3);
  transition: transform 0.2s, box-shadow 0.2s;
  animation: ballPulse 3s ease-in-out infinite;
  -webkit-tap-highlight-color: transparent;
  user-select: none;
}

.menu-ball::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  background: radial-gradient(circle at 30% 22%, rgba(255,220,180,0.3), transparent 45%);
  pointer-events: none;
}

/* Retro ball stitching line */
.menu-ball::after {
  content: '';
  position: absolute;
  width: 44px;
  height: 44px;
  border-radius: 50%;
  border: 1.5px dashed rgba(90, 58, 30, 0.5);
  pointer-events: none;
}

.menu-ball-svg {
  position: absolute;
  width: 100%;
  height: 100%;
  pointer-events: none;
  z-index: 1;
}

.menu-ball-text {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 0.5rem;
  color: rgba(255,240,220,0.9);
  text-transform: uppercase;
  letter-spacing: 0.1em;
  z-index: 2;
  pointer-events: none;
  text-shadow: 0 1px 2px rgba(0,0,0,0.4);
}

.menu-ball:active {
  transform: scale(0.92);
}

.menu-ball.open {
  animation: none;
  transform: scale(1.05);
  box-shadow: 0 4px 28px rgba(160, 107, 62, 0.6), inset 0 2px 4px rgba(255,220,180,0.3), inset 0 -2px 4px rgba(0,0,0,0.3);
  border-color: rgba(200, 149, 106, 0.8);
}

@keyframes ballPulse {
  0%, 100% { box-shadow: 0 4px 20px rgba(90, 58, 30, 0.5), inset 0 2px 4px rgba(255,220,180,0.25), inset 0 -2px 4px rgba(0,0,0,0.3); }
  50% { box-shadow: 0 4px 28px rgba(160, 107, 62, 0.6), inset 0 2px 4px rgba(255,220,180,0.35), inset 0 -2px 4px rgba(0,0,0,0.25); }
}

/* Floating menu panel */
.menu-panel {
  position: fixed;
  bottom: 5.5rem;
  right: 1.5rem;
  z-index: 1999;
  background: rgba(10, 22, 40, 0.95);
  border: 1px solid rgba(232, 122, 58, 0.2);
  border-radius: 16px;
  padding: 0.75rem 0;
  backdrop-filter: blur(24px);
  -webkit-backdrop-filter: blur(24px);
  box-shadow: 0 8px 40px rgba(0,0,0,0.5);
  min-width: 180px;
  transform: scale(0.8) translateY(10px);
  opacity: 0;
  pointer-events: none;
  transition: transform 0.25s cubic-bezier(0.34, 1.56, 0.64, 1), opacity 0.2s;
  transform-origin: bottom right;
}

.menu-panel.open {
  transform: scale(1) translateY(0);
  opacity: 1;
  pointer-events: auto;
}

.menu-panel a {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  padding: 0.65rem 1.25rem;
  font-family: var(--font-display);
  font-weight: 500;
  font-size: 0.82rem;
  color: var(--gray-300);
  text-decoration: none;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  transition: background 0.15s, color 0.15s;
}

.menu-panel a:hover,
.menu-panel a:active {
  background: rgba(232, 122, 58, 0.1);
  color: var(--orange-400);
}

.menu-panel a .menu-icon {
  font-size: 1rem;
  width: 1.2rem;
  text-align: center;
}

/* ========== HERO ========== */
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
  text-align: center;
  padding: 2rem 1rem;
}

.hero-bg {
  position: absolute;
  inset: 0;
  z-index: 0;
}

.hero-bg svg {
  width: 100%;
  height: 100%;
}

.hero-cosmos {
  position: absolute;
  inset: 0;
  overflow: hidden;
  pointer-events: none;
}

.hero-stars {
  position: absolute;
  inset: -10%;
  opacity: 0.8;
  will-change: transform, opacity;
}

.hero-stars-1 {
  background-image:
    radial-gradient(circle at 8% 22%, rgba(255,255,255,0.9) 0 1px, transparent 1.6px),
    radial-gradient(circle at 17% 68%, rgba(255,255,255,0.7) 0 1.2px, transparent 1.8px),
    radial-gradient(circle at 28% 16%, rgba(251,185,144,0.95) 0 1.4px, transparent 2px),
    radial-gradient(circle at 37% 58%, rgba(255,255,255,0.8) 0 1px, transparent 1.7px),
    radial-gradient(circle at 46% 28%, rgba(255,255,255,0.65) 0 1.2px, transparent 1.8px),
    radial-gradient(circle at 61% 18%, rgba(255,255,255,0.9) 0 1.3px, transparent 1.9px),
    radial-gradient(circle at 74% 66%, rgba(240,140,80,0.7) 0 1.5px, transparent 2.1px),
    radial-gradient(circle at 87% 24%, rgba(255,255,255,0.75) 0 1.1px, transparent 1.8px),
    radial-gradient(circle at 92% 78%, rgba(255,255,255,0.8) 0 1.3px, transparent 2px);
  animation: starPulseSlow 8s ease-in-out infinite;
}

.hero-stars-2 {
  background-image:
    radial-gradient(circle at 12% 44%, rgba(255,255,255,0.6) 0 0.9px, transparent 1.5px),
    radial-gradient(circle at 22% 84%, rgba(255,255,255,0.65) 0 1px, transparent 1.6px),
    radial-gradient(circle at 33% 34%, rgba(251,185,144,0.7) 0 1px, transparent 1.7px),
    radial-gradient(circle at 49% 78%, rgba(255,255,255,0.55) 0 1px, transparent 1.6px),
    radial-gradient(circle at 58% 47%, rgba(255,255,255,0.65) 0 0.8px, transparent 1.4px),
    radial-gradient(circle at 69% 88%, rgba(255,255,255,0.7) 0 1px, transparent 1.7px),
    radial-gradient(circle at 83% 38%, rgba(240,140,80,0.55) 0 1.2px, transparent 1.8px),
    radial-gradient(circle at 94% 52%, rgba(255,255,255,0.75) 0 0.9px, transparent 1.5px);
  animation: starPulseSlow 12s ease-in-out infinite reverse;
}

.hero-nebula {
  position: absolute;
  border-radius: 50%;
  filter: blur(26px);
  opacity: 0.22;
  mix-blend-mode: screen;
}

.hero-nebula-1 {
  width: 32vw;
  height: 22vw;
  min-width: 280px;
  min-height: 180px;
  top: 12%;
  left: -4%;
  background: radial-gradient(circle at 40% 50%, rgba(72,125,255,0.45), rgba(72,125,255,0.05) 60%, transparent 78%);
  animation: nebulaFloat 28s ease-in-out infinite;
}

.hero-nebula-2 {
  width: 26vw;
  height: 18vw;
  min-width: 220px;
  min-height: 150px;
  right: 2%;
  top: 8%;
  background: radial-gradient(circle at 50% 50%, rgba(232,122,58,0.35), rgba(232,122,58,0.06) 58%, transparent 76%);
  animation: nebulaFloat 34s ease-in-out infinite reverse;
}

.hero-comet {
  position: absolute;
  top: 18%;
  left: -30%;
  width: 22vw;
  min-width: 180px;
  max-width: 360px;
  height: 2px;
  background: linear-gradient(90deg, rgba(255,255,255,0), rgba(255,255,255,0.15), rgba(251,185,144,0.5), rgba(255,255,255,0.95));
  border-radius: 999px;
  filter: drop-shadow(0 0 10px rgba(255,255,255,0.4));
  opacity: 0;
  transform: rotate(18deg);
  animation: cometFly 18s linear infinite;
}

.hero-comet::after {
  content: '';
  position: absolute;
  right: -6px;
  top: 50%;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  transform: translateY(-50%);
  background: radial-gradient(circle, rgba(255,255,255,1) 0%, rgba(251,185,144,0.95) 45%, rgba(232,122,58,0.2) 75%, transparent 100%);
  box-shadow: 0 0 18px rgba(255,255,255,0.45);
}

.hero-satellite {
  position: absolute;
  top: 24%;
  right: -10%;
  width: 132px;
  height: 48px;
  opacity: 0.55;
  transform: rotate(-14deg);
  animation: satelliteFly 40s linear infinite;
}

.hero-satellite .sat-core {
  position: absolute;
  left: 42px;
  top: 12px;
  width: 32px;
  height: 24px;
  border-radius: 12px;
  background: linear-gradient(180deg, rgba(212,222,246,0.95), rgba(117,139,179,0.85));
  box-shadow: 0 0 10px rgba(255,255,255,0.12);
}

.hero-satellite .sat-core::before,
.hero-satellite .sat-core::after {
  content: '';
  position: absolute;
  top: 50%;
  width: 42px;
  height: 1.5px;
  background: linear-gradient(90deg, rgba(255,255,255,0.9), rgba(255,255,255,0.12));
}

.hero-satellite .sat-core::before {
  right: 100%;
  transform: translateY(-50%) rotate(14deg);
  transform-origin: right center;
}

.hero-satellite .sat-core::after {
  left: 100%;
  transform: translateY(-50%) rotate(-14deg);
  transform-origin: left center;
}

.hero-satellite .sat-dish {
  position: absolute;
  left: 55px;
  top: 2px;
  width: 8px;
  height: 8px;
  border: 1.5px solid rgba(251,185,144,0.7);
  border-radius: 50%;
  box-shadow: 0 0 12px rgba(251,185,144,0.14);
}

.hero-satellite .sat-dish::after {
  content: '';
  position: absolute;
  left: 50%;
  top: -8px;
  width: 1.5px;
  height: 8px;
  background: rgba(251,185,144,0.7);
  transform: translateX(-50%);
}

.hero-satellite .sat-panel {
  position: absolute;
  top: 10px;
  width: 28px;
  height: 16px;
  border: 1px solid rgba(163,196,255,0.45);
  background:
    linear-gradient(180deg, rgba(32,58,110,0.75), rgba(16,30,65,0.92)),
    repeating-linear-gradient(90deg, transparent 0 4px, rgba(113,153,255,0.2) 4px 5px);
  box-shadow: inset 0 0 10px rgba(113,153,255,0.16);
}

.hero-satellite .sat-panel.left {
  left: 8px;
}

.hero-satellite .sat-panel.right {
  right: 8px;
}

.hero-planet {
  position: absolute;
  left: -10vw;
  bottom: -20vw;
  width: clamp(260px, 34vw, 520px);
  aspect-ratio: 1;
  border-radius: 50%;
  background:
    radial-gradient(circle at 36% 34%, rgba(164,214,255,0.9), rgba(54,88,150,0.92) 42%, rgba(18,31,58,0.98) 72%, rgba(6,10,22,0) 78%),
    radial-gradient(circle at 66% 70%, rgba(255,255,255,0.14), transparent 44%);
  opacity: 0.32;
  filter: blur(0.2px);
  box-shadow:
    0 0 80px rgba(52,90,180,0.16),
    inset -24px -18px 40px rgba(5,10,24,0.55);
  animation: planetDrift 120s linear infinite;
}

.hero-planet::before {
  content: '';
  position: absolute;
  inset: 18% -12%;
  border-radius: 50%;
  border: 1.5px solid rgba(255,255,255,0.16);
  transform: rotate(-16deg);
  opacity: 0.7;
}

.hero-planet::after {
  content: '';
  position: absolute;
  inset: 22% -18%;
  border-radius: 50%;
  border: 8px solid rgba(125,160,230,0.09);
  transform: rotate(-16deg);
  opacity: 0.35;
}

@keyframes starPulseSlow {
  0%, 100% { opacity: 0.42; transform: translate3d(0, 0, 0) scale(1); }
  50% { opacity: 0.95; transform: translate3d(0, -6px, 0) scale(1.015); }
}

@keyframes nebulaFloat {
  0%, 100% { transform: translate3d(0, 0, 0) scale(1); }
  50% { transform: translate3d(18px, -10px, 0) scale(1.08); }
}

@keyframes cometFly {
  0%, 82% { opacity: 0; transform: translate3d(0, 0, 0) rotate(18deg); }
  84% { opacity: 0.95; }
  100% { opacity: 0; transform: translate3d(145vw, 36vh, 0) rotate(18deg); }
}

@keyframes satelliteFly {
  0% { transform: translate3d(0, 0, 0) rotate(-14deg); opacity: 0; }
  10% { opacity: 0.5; }
  60% { opacity: 0.58; }
  100% { transform: translate3d(-150vw, 18vh, 0) rotate(8deg); opacity: 0; }
}

@keyframes planetDrift {
  0% { transform: translate3d(0, 0, 0); }
  100% { transform: translate3d(18vw, -6vh, 0); }
}

.hero-gradient {
  position: absolute;
  inset: 0;
  background:
    radial-gradient(ellipse 80% 60% at 50% 40%, rgba(15, 35, 71, 0.3) 0%, transparent 70%),
    radial-gradient(ellipse 60% 50% at 50% 50%, rgba(232, 122, 58, 0.06) 0%, transparent 60%),
    linear-gradient(180deg, rgba(7, 14, 26, 0.2) 0%, rgba(7, 14, 26, 0.8) 100%);
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 800px;
}

.hero-emblem {
  width: clamp(120px, 25vw, 180px);
  height: auto;
  margin-bottom: 1.5rem;
  filter: drop-shadow(0 0 40px rgba(232, 122, 58, 0.3));
  animation: emblemFloat 6s ease-in-out infinite;
}

.hero-emblem-wrap {
  position: relative;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
}

.hero-emblem-wrap::before {
  content: '';
  position: absolute;
  inset: 8% 12%;
  border-radius: 42%;
  background: radial-gradient(circle, rgba(232, 122, 58, 0.34) 0%, rgba(232, 122, 58, 0.14) 38%, rgba(232, 122, 58, 0.05) 58%, transparent 76%);
  filter: blur(22px);
  z-index: 0;
}

.hero-emblem-wrap::after {
  content: '';
  position: absolute;
  top: -8%;
  bottom: -8%;
  left: -35%;
  width: 32%;
  background: linear-gradient(115deg, transparent 0%, rgba(255,255,255,0.04) 35%, rgba(255,244,214,0.45) 50%, rgba(255,255,255,0.04) 65%, transparent 100%);
  transform: translateX(-220%) skewX(-18deg);
  animation: emblemShine 5.8s ease-in-out infinite;
  pointer-events: none;
  z-index: 2;
  mix-blend-mode: screen;
}

.hero-emblem-image {
  position: relative;
  z-index: 1;
  width: clamp(180px, 28vw, 300px);
  height: auto;
  display: block;
  filter: drop-shadow(0 0 18px rgba(255, 223, 174, 0.22)) drop-shadow(0 0 30px rgba(232, 122, 58, 0.30)) drop-shadow(0 10px 28px rgba(0, 0, 0, 0.32));
  animation: emblemFloat 7.2s ease-in-out infinite;
}

@keyframes emblemFloat {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

@keyframes emblemShine {
  0%, 58% { transform: translateX(-220%) skewX(-18deg); opacity: 0; }
  64% { opacity: 1; }
  82%, 100% { transform: translateX(360%) skewX(-18deg); opacity: 0; }
}

.hero-pretitle {
  font-family: var(--font-display);
  font-weight: 500;
  font-size: clamp(0.75rem, 2vw, 0.9rem);
  color: var(--orange-300);
  letter-spacing: 0.3em;
  text-transform: uppercase;
  margin-bottom: 0.75rem;
}

.hero-title {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: clamp(2.5rem, 8vw, 5rem);
  line-height: 1.05;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  background: linear-gradient(180deg, var(--orange-100) 0%, var(--orange-400) 50%, var(--orange-500) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 0.5rem;
}

.hero-year {
  font-family: 'Century Gothic', 'General Sans', 'Roboto', sans-serif;
  font-weight: 300;
  font-size: clamp(1.3rem, 4vw, 2.2rem);
  color: var(--white);
  opacity: 0.55;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  margin-bottom: 1.5rem;
}

.hero-meta {
  display: flex;
  gap: 2rem;
  justify-content: center;
  flex-wrap: wrap;
  margin-bottom: 2rem;
}

.hero-meta-item {
  font-family: var(--font-body);
  font-size: 0.85rem;
  color: var(--gray-300);
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.hero-meta-item svg {
  width: 16px;
  height: 16px;
  color: var(--orange-400);
}

.hero-scroll {
  position: absolute;
  bottom: 2rem;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
  animation: scrollBounce 2s ease-in-out infinite;
}

.hero-scroll svg {
  width: 24px;
  height: 24px;
  color: var(--orange-400);
  opacity: 0.6;
}

@keyframes scrollBounce {
  0%, 100% { transform: translateX(-50%) translateY(0); }
  50% { transform: translateX(-50%) translateY(8px); }
}

/* ========== SECTIONS ========== */
section {
  padding: var(--section-pad) 0;
}

.section-header {
  margin-bottom: 2.5rem;
}

/* ========== LIGHT BEAM HOVER EFFECT ========== */
.light-beam {
  position: relative;
  overflow: hidden;
  cursor: pointer;
}

.light-beam::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(120deg, transparent 0%, transparent 30%, rgba(255,255,255,0.15) 45%, rgba(255,255,255,0.3) 50%, rgba(255,255,255,0.15) 55%, transparent 70%, transparent 100%);
  transform: translateX(-100%);
  transition: none;
  pointer-events: none;
  z-index: 5;
}

.light-beam:hover::after {
  animation: lightBeamSweep 0.6s ease-in-out forwards;
}

@keyframes lightBeamSweep {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

/* ========== REGULATIONS BUTTONS ========== */
.regulations-row {
  display: flex;
  gap: 1rem;
  margin-bottom: 2rem;
}

.reg-btn {
  flex: 1;
  position: relative;
  overflow: hidden;
  cursor: pointer;
  background: linear-gradient(135deg, rgba(34, 120, 70, 0.25), rgba(46, 160, 90, 0.15));
  border: 1.5px solid rgba(46, 180, 90, 0.35);
  border-radius: var(--card-radius);
  padding: 1rem 1.25rem;
  display: flex;
  align-items: center;
  gap: 0.75rem;
  transition: border-color 0.3s, box-shadow 0.3s, background 0.3s;
  -webkit-tap-highlight-color: transparent;
}

.reg-btn:hover {
  border-color: rgba(46, 200, 100, 0.6);
  box-shadow: 0 4px 24px rgba(46, 180, 90, 0.2);
  background: linear-gradient(135deg, rgba(34, 120, 70, 0.35), rgba(46, 160, 90, 0.25));
}

/* Green light beam effect */
.reg-btn::after {
  content: '';
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: linear-gradient(120deg, transparent 0%, transparent 30%, rgba(120,255,160,0.2) 45%, rgba(150,255,180,0.35) 50%, rgba(120,255,160,0.2) 55%, transparent 70%, transparent 100%);
  transform: translateX(-100%);
  transition: none;
  pointer-events: none;
  z-index: 5;
}

.reg-btn:hover::after {
  animation: lightBeamSweep 0.6s ease-in-out forwards;
}

.reg-btn-icon {
  font-size: 1.3rem;
  flex-shrink: 0;
}

.reg-btn-text {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 0.85rem;
  color: rgba(150, 255, 180, 0.9);
  text-transform: uppercase;
  letter-spacing: 0.08em;
  line-height: 1.3;
}

.reg-btn .chevron {
  width: 16px; height: 16px;
  margin-left: auto;
  color: rgba(150, 255, 180, 0.5);
  flex-shrink: 0;
  transition: transform 0.3s;
}

.reg-btn.open .chevron {
  transform: rotate(180deg);
}

/* Regulation content panel */
.reg-content {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.4s ease, margin 0.3s;
  margin-top: 0;
}

.reg-content.open {
  max-height: 2000px;
  margin-top: 1rem;
}

.reg-content-inner {
  background: linear-gradient(135deg, rgba(34, 120, 70, 0.12), rgba(15, 35, 71, 0.4));
  border: 1px solid rgba(46, 180, 90, 0.2);
  border-radius: var(--card-radius);
  padding: 1.5rem;
  font-family: var(--font-body);
  font-size: 0.9rem;
  line-height: 1.7;
  color: var(--gray-200);
}

.reg-content-inner h4 {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 1rem;
  color: rgba(150, 255, 180, 0.9);
  margin-bottom: 0.75rem;
}

.reg-content-inner p {
  margin-bottom: 0.75rem;
}

.reg-content-inner ul, .reg-content-inner ol {
  margin-left: 1.25rem;
  margin-bottom: 0.75rem;
}

.reg-content-inner li {
  margin-bottom: 0.35rem;
}

@media (max-width: 480px) {
  .regulations-row {
    flex-direction: column;
    gap: 0.75rem;
  }
  .reg-btn {
    padding: 0.85rem 1rem;
  }
  .reg-content.open {
    max-height: 5000px;
  }
}

/* ========== STANDINGS TABLE ========== */
.standings-wrapper {
  overflow-x: auto;
  border-radius: var(--card-radius);
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  box-shadow: var(--glass-shadow);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
}

.standings-table {
  width: 100%;
  border-collapse: collapse;
  min-width: 640px;
  font-variant-numeric: tabular-nums;
}

.standings-table thead {
  background: rgba(232, 122, 58, 0.1);
}

.standings-table th {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--orange-400);
  padding: 1rem 0.75rem;
  text-align: center;
  white-space: nowrap;
}

.standings-table th:nth-child(2) {
  text-align: left;
}

.standings-table td {
  padding: 0.85rem 0.75rem;
  text-align: center;
  font-size: 0.9rem;
  border-bottom: 1px solid rgba(255, 255, 255, 0.04);
  color: var(--gray-200);
}

.standings-table td:nth-child(2) {
  text-align: left;
  font-weight: 600;
  color: var(--white);
}

.standings-table tbody tr {
  transition: background 0.2s;
}

.standings-table tbody tr:hover {
  background: rgba(232, 122, 58, 0.05);
}

.standings-table tbody tr:nth-child(1) td:first-child,
.standings-table tbody tr:nth-child(2) td:first-child,
.standings-table tbody tr:nth-child(3) td:first-child {
  position: relative;
}

.standings-table tbody tr:nth-child(1) td:first-child::before,
.standings-table tbody tr:nth-child(2) td:first-child::before,
.standings-table tbody tr:nth-child(3) td:first-child::before {
  content: '';
  position: absolute;
  left: 0;
  top: 15%;
  height: 70%;
  width: 3px;
  border-radius: 0 3px 3px 0;
}

.standings-table tbody tr:nth-child(1) td:first-child::before {
  background: var(--orange-400);
}
.standings-table tbody tr:nth-child(2) td:first-child::before {
  background: var(--orange-500);
}
.standings-table tbody tr:nth-child(3) td:first-child::before {
  background: rgba(232, 122, 58, 0.4);
}

.standings-table .rank {
  font-family: var(--font-display);
  font-weight: 700;
  color: var(--orange-300);
}

.standings-table .points {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 1rem;
  color: var(--orange-400);
}

/* ========== SCHEDULE ========== */
.schedule-grid {
  display: grid;
  gap: 0.75rem;
}

.match-card {
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  border-radius: var(--card-radius-sm);
  padding: 0.85rem 1.25rem;
  display: grid;
  grid-template-columns: auto 1fr auto auto;
  align-items: center;
  gap: 0.75rem;
  transition: transform 0.2s, border-color 0.2s;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
}

.match-card:hover {
  transform: translateY(-1px);
  border-color: rgba(232, 122, 58, 0.3);
}

.match-number {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 0.7rem;
  color: var(--navy-800);
  background: var(--orange-400);
  width: 30px;
  height: 30px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.match-body {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.match-team {
  flex: 1;
  min-width: 0;
}

.match-team .team-name {
  font-weight: 600;
  font-size: 0.88rem;
  color: var(--white);
  display: block;
}

.match-team.away {
  text-align: right;
}

/* Score area */
.match-score {
  display: flex;
  align-items: center;
  gap: 0.2rem;
  flex-shrink: 0;
  position: relative;
  z-index: 10;
}

.score-input {
  width: 28px;
  height: 28px;
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 5px;
  text-align: center;
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 0.85rem;
  color: rgba(255,255,255,0.25);
  cursor: pointer;
  transition: all 0.2s;
  -moz-appearance: textfield;
  padding: 0;
}

.score-input::-webkit-outer-spin-button,
.score-input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

.score-input:focus {
  outline: none;
  border-color: var(--orange-400);
  background: rgba(232, 122, 58, 0.1);
  color: var(--orange-300);
  box-shadow: 0 0 8px rgba(232, 122, 58, 0.2);
}

.score-input.has-value {
  color: var(--white);
  background: rgba(232, 122, 58, 0.12);
  border-color: rgba(232, 122, 58, 0.25);
}

.score-divider {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 0.8rem;
  color: rgba(255,255,255,0.2);
  user-select: none;
}

.match-time {
  text-align: right;
}

.match-time .time {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 0.9rem;
  color: var(--orange-300);
}

.match-time .status {
  font-size: 0.6rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--gray-400);
  margin-top: 0.1rem;
}

.round-header {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 0.8rem;
  color: var(--orange-400);
  text-transform: uppercase;
  letter-spacing: 0.15em;
  padding: 1.5rem 0 0.5rem;
  border-bottom: 1px solid rgba(232, 122, 58, 0.15);
  margin-bottom: 0.25rem;
}

.round-header:first-child {
  padding-top: 0;
}

@media (max-width: 640px) {
  .match-card {
    grid-template-columns: auto 1fr;
    gap: 0.5rem 0.75rem;
    padding: 0.75rem 1rem;
  }
  .match-body {
    gap: 0.35rem;
  }
  .match-team .team-name {
    font-size: 0.78rem;
  }
  .score-input {
    width: 24px;
    height: 24px;
    font-size: 0.75rem;
  }
  .match-time {
    grid-column: 1 / -1;
    text-align: left;
    display: flex;
    align-items: center;
    gap: 0.75rem;
    padding-top: 0.5rem;
    border-top: 1px solid rgba(255,255,255,0.05);
  }
}

/* ========== TEAMS ========== */
.teams-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1rem;
}

.team-card {
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  border-radius: var(--card-radius);
  padding: 1.5rem;
  text-align: center;
  transition: transform 0.25s, border-color 0.25s, box-shadow 0.25s;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  position: relative;
  overflow: hidden;
}

.team-card-top {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  border-radius: var(--card-radius) var(--card-radius) 0 0;
}

.team-card:hover {
  transform: translateY(-3px);
  border-color: rgba(232, 122, 58, 0.3);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.3);
}

.team-badge {
  width: 56px;
  height: 56px;
  margin: 0 auto 1rem;
  display: block;
}

.team-card .team-name {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 1.1rem;
  color: var(--white);
  margin-bottom: 0.25rem;
}

.team-card .team-city {
  font-size: 0.8rem;
  color: var(--gray-400);
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-bottom: 0.5rem;
}

.team-expand-hint {
  font-size: 0.7rem;
  color: var(--gray-500);
  transition: color 0.2s;
}

.team-card:hover .team-expand-hint {
  color: var(--orange-300);
}

/* Team roster expansion */
.team-roster {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.4s ease, padding 0.4s ease;
  padding: 0;
}

.team-card.expanded .team-roster {
  max-height: 600px;
  padding-top: 1rem;
}

.team-card.expanded .team-expand-hint {
  display: none;
}

.roster-section-title {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  margin-bottom: 0.5rem;
  margin-top: 0.75rem;
  padding-top: 0.75rem;
  border-top: 1px solid rgba(255,255,255,0.06);
}

.roster-section-title.field {
  color: var(--orange-400);
}

.roster-section-title.bench {
  color: var(--gray-500);
}

.roster-player {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.35rem 0;
  font-size: 0.82rem;
}

.player-frame {
  width: 28px;
  height: 28px;
  border-radius: 50%;
  border: 2px solid;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 0.6rem;
  flex-shrink: 0;
}

.player-frame.field-frame {
  border-color: var(--orange-400);
  color: var(--orange-300);
  background: rgba(232, 122, 58, 0.1);
}

.player-frame.bench-frame {
  border-color: var(--gray-600);
  color: var(--gray-500);
  background: rgba(61, 70, 96, 0.2);
}

.player-role {
  color: var(--gray-400);
  font-size: 0.75rem;
  font-style: italic;
}

.player-name-empty {
  color: var(--gray-600);
  font-size: 0.78rem;
}

.player-name-input {
  flex: 1;
  min-width: 0;
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(255,255,255,0.06);
  border-radius: 4px;
  padding: 0.25rem 0.5rem;
  font-family: var(--font-body);
  font-size: 0.8rem;
  color: rgba(255,255,255,0.2);
  cursor: pointer;
  transition: all 0.2s;
  outline: none;
}

.player-name-input::placeholder {
  color: rgba(255,255,255,0.15);
}

.player-name-input:focus {
  border-color: var(--orange-400);
  background: rgba(232, 122, 58, 0.08);
  color: var(--orange-300);
  box-shadow: 0 0 8px rgba(232, 122, 58, 0.15);
}

.player-name-input.has-name {
  color: var(--white);
  background: rgba(255,255,255,0.05);
  border-color: rgba(255,255,255,0.1);
}

/* ========== JUDGES SECTION ========== */
.judges-list {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  max-width: 700px;
}

.judge-panel {
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  border-radius: var(--card-radius-sm);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  position: relative;
  overflow: hidden;
  cursor: pointer;
}

.judge-panel-header {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 1rem 1.25rem;
  transition: background 0.2s;
}

.judge-panel-header:hover {
  background: rgba(232, 122, 58, 0.05);
}

.judge-panel-icon {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: rgba(232, 122, 58, 0.12);
  border: 1.5px solid rgba(232, 122, 58, 0.3);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.judge-panel-icon svg {
  width: 18px;
  height: 18px;
  color: var(--orange-400);
}

.judge-panel-title {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 0.95rem;
  color: var(--white);
  flex: 1;
}

.judge-panel-status {
  font-size: 0.75rem;
  color: var(--gray-500);
  font-style: italic;
}

.judge-panel .chevron {
  width: 18px;
  height: 18px;
  color: var(--gray-500);
  transition: transform 0.3s ease;
  flex-shrink: 0;
}

.judge-panel.open .chevron {
  transform: rotate(180deg);
}

.judge-panel-body {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.35s ease;
}

.judge-panel.open .judge-panel-body {
  max-height: 500px;
}

.judge-panel-content {
  padding: 0 1.25rem 1rem;
}

.judge-person {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.5rem 0;
  border-bottom: 1px solid rgba(255,255,255,0.04);
}

.judge-person:last-child {
  border-bottom: none;
}

.judge-person-num {
  width: 28px;
  height: 28px;
  border-radius: 50%;
  background: rgba(232, 122, 58, 0.12);
  border: 1.5px solid rgba(232, 122, 58, 0.25);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--orange-400);
  flex-shrink: 0;
}

.judge-person-num.muted {
  background: rgba(255,255,255,0.04);
  border-color: rgba(255,255,255,0.1);
  color: var(--gray-500);
}

.judge-person-role {
  font-size: 0.8rem;
  color: var(--gray-400);
}

.judge-person-name {
  font-size: 0.8rem;
  color: var(--gray-600);
  margin-left: auto;
  font-style: italic;
}

.judge-name-input {
  flex: 1;
  min-width: 0;
  max-width: 160px;
  margin-left: auto;
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(255,255,255,0.06);
  border-radius: 4px;
  padding: 0.25rem 0.5rem;
  font-family: var(--font-body);
  font-size: 0.8rem;
  color: rgba(255,255,255,0.2);
  cursor: pointer;
  transition: all 0.2s;
  outline: none;
}

.judge-name-input::placeholder {
  color: rgba(255,255,255,0.15);
}

.judge-name-input:focus {
  border-color: var(--orange-400);
  background: rgba(232, 122, 58, 0.08);
  color: var(--orange-300);
  box-shadow: 0 0 8px rgba(232, 122, 58, 0.15);
}

.judge-name-input.has-name {
  color: var(--white);
  background: rgba(255,255,255,0.05);
  border-color: rgba(255,255,255,0.1);
  font-style: normal;
}

/* ========== ORGANIZATION ========== */
.org-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 1rem;
}

.org-card {
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  border-radius: var(--card-radius-sm);
  overflow: hidden;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
}

.org-card-header {
  padding: 1rem 1.25rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  cursor: pointer;
  user-select: none;
  transition: background 0.2s;
}

.org-card-header:hover {
  background: rgba(232, 122, 58, 0.05);
}

.org-card-header h3 {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 0.9rem;
  color: var(--orange-300);
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.org-card-header .chevron {
  width: 20px;
  height: 20px;
  color: var(--gray-400);
  transition: transform 0.3s;
}

.org-card.open .chevron {
  transform: rotate(180deg);
}

.org-card-body {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.4s ease;
}

.org-card.open .org-card-body {
  max-height: 500px;
}

.org-task {
  padding: 0.6rem 1.25rem;
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
  border-top: 1px solid rgba(255, 255, 255, 0.03);
  font-size: 0.85rem;
}

.org-task .checkbox {
  width: 18px;
  height: 18px;
  border-radius: 4px;
  border: 2px solid var(--gray-500);
  flex-shrink: 0;
  margin-top: 2px;
  cursor: pointer;
  transition: 0.2s;
  display: flex;
  align-items: center;
  justify-content: center;
}

.org-task .checkbox.checked {
  background: var(--orange-500);
  border-color: var(--orange-500);
}

.org-task .checkbox.checked::after {
  content: '✓';
  color: var(--navy-800);
  font-size: 0.7rem;
  font-weight: 700;
}

.org-task .task-text {
  flex: 1;
  color: var(--gray-200);
}

.org-task .task-person {
  font-size: 0.75rem;
  color: var(--orange-400);
  font-weight: 600;
  white-space: nowrap;
}

/* ========== BUDGET ========== */
.budget-card {
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  border-radius: var(--card-radius);
  overflow: hidden;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  margin-top: 2rem;
}

.budget-card-title {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 1rem;
  color: var(--orange-300);
  padding: 1.25rem 1.5rem;
  border-bottom: 1px solid var(--glass-border);
}

.budget-table {
  width: 100%;
  border-collapse: collapse;
}

.budget-table th {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--orange-400);
  padding: 0.75rem 1.5rem;
  text-align: left;
  background: rgba(232, 122, 58, 0.05);
}

.budget-table th:not(:first-child) {
  text-align: center;
}

.budget-table td {
  padding: 0.7rem 1.5rem;
  font-size: 0.85rem;
  color: var(--gray-200);
  border-bottom: 1px solid rgba(255, 255, 255, 0.03);
}

.budget-table td:not(:first-child) {
  text-align: center;
  color: var(--gray-400);
}

.budget-input {
  background: transparent;
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 6px;
  color: var(--gray-300);
  font-family: var(--font-body);
  font-size: 0.85rem;
  padding: 0.4rem 0.5rem;
  width: 90px;
  text-align: center;
  outline: none;
  transition: border-color 0.2s, background 0.2s, box-shadow 0.2s;
  cursor: pointer;
}
.budget-input::placeholder {
  color: var(--gray-600);
  font-size: 0.8rem;
}
.budget-input:hover {
  border-color: rgba(232, 122, 58, 0.3);
  background: rgba(232, 122, 58, 0.04);
}
.budget-input:focus {
  border-color: var(--orange-500);
  background: rgba(232, 122, 58, 0.08);
  box-shadow: 0 0 0 2px rgba(232, 122, 58, 0.15);
}
.budget-input.has-value {
  color: var(--orange-300);
  border-color: rgba(232, 122, 58, 0.25);
}
.budget-total-row td {
  font-weight: 700;
  font-family: var(--font-display);
  color: var(--orange-400) !important;
  border-top: 2px solid rgba(232, 122, 58, 0.2);
  padding-top: 0.9rem;
}

/* ========== VENUE WIDGET ========== */
.venue-card {
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  border-radius: var(--card-radius);
  overflow: hidden;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  margin-top: 2rem;
}
.venue-card-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.25rem 1.5rem;
  border-bottom: 1px solid var(--glass-border);
}
.venue-icon {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  background: rgba(232, 122, 58, 0.12);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  flex-shrink: 0;
}
.venue-info h3 {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: 1rem;
  color: var(--orange-300);
  margin-bottom: 0.2rem;
}
.venue-info p {
  font-size: 0.82rem;
  color: var(--gray-400);
  line-height: 1.4;
}
.venue-map-container {
  position: relative;
  width: 100%;
  height: 250px;
  border-top: 1px solid var(--glass-border);
}
.venue-map-container iframe {
  width: 100%;
  height: 100%;
  border: none;
  filter: saturate(0.7) brightness(0.85) contrast(1.1);
}
.venue-link-row {
  padding: 0.8rem 1.5rem;
  border-top: 1px solid var(--glass-border);
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.venue-link-row a {
  font-family: var(--font-display);
  font-size: 0.8rem;
  font-weight: 600;
  color: var(--orange-400);
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  transition: color 0.2s;
}
.venue-link-row a:hover {
  color: var(--orange-300);
}

/* ========== INFO SECTION ========== */
.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
  gap: 1rem;
  margin-bottom: 2rem;
}

.info-card {
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  border-radius: var(--card-radius-sm);
  padding: 1.25rem;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  text-align: center;
}

.info-card .info-value {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 1.5rem;
  color: var(--orange-400);
  margin-bottom: 0.25rem;
}

.info-card .info-label {
  font-size: 0.8rem;
  color: var(--gray-400);
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

/* ========== FOOTER ========== */
.footer {
  padding: 2.5rem 0;
  border-top: 1px solid var(--glass-border);
  text-align: center;
}

.footer-brand {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 1rem;
  color: var(--orange-400);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}

.footer-text {
  font-size: 0.8rem;
  color: var(--gray-500);
  margin-bottom: 0.75rem;
}

.footer-credits {
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
  margin-bottom: 1rem;
}

.footer-credit-line {
  font-size: 0.78rem;
  color: var(--gray-400);
  letter-spacing: 0.04em;
}

.footer-credit-line strong {
  color: var(--orange-300);
  font-weight: 600;
}

.footer a {
  color: var(--gray-400);
  text-decoration: none;
  font-size: 0.75rem;
  transition: color 0.2s;
}

.footer a:hover {
  color: var(--orange-400);
}

/* ========== SCROLLBAR ========== */
::-webkit-scrollbar { width: 8px; height: 8px; }
::-webkit-scrollbar-track { background: var(--navy-900); }
::-webkit-scrollbar-thumb { background: var(--navy-600); border-radius: 4px; }
::-webkit-scrollbar-thumb:hover { background: var(--navy-500); }

/* ========== RESPONSIVE TWEAKS ========== */
@media (max-width: 480px) {
  .teams-grid { grid-template-columns: 1fr 1fr; }
  .org-grid { grid-template-columns: 1fr; }
  .info-grid { grid-template-columns: 1fr 1fr; }
  .judges-grid { grid-template-columns: 1fr 1fr; }
  .hero-meta { gap: 1rem; }
  .footer-credit-line {
    font-size: 0.72rem;
    line-height: 1.5;
  }
  .hero-comet {
    width: 42vw;
    top: 15%;
    animation-duration: 14s;
  }
  .hero-satellite {
    width: 96px;
    height: 38px;
    top: 14%;
    opacity: 0.38;
  }
  .hero-planet {
    left: -28vw;
    bottom: -28vw;
    width: 72vw;
    opacity: 0.22;
  }
  .hero-nebula-1,
  .hero-nebula-2 {
    opacity: 0.14;
  }
}

@media (max-width: 360px) {
  .teams-grid { grid-template-columns: 1fr; }
  .info-grid { grid-template-columns: 1fr; }
  .judges-grid { grid-template-columns: 1fr; }
}

/* Mobile expanded team card — full width */
@media (max-width: 768px) {
  .team-card.expanded {
    grid-column: 1 / -1;
  }
  .team-card.expanded .player-name-input {
    min-width: 100px;
  }
}
</style>
</head>
<body>

<!-- ====== FLOATING BALL MENU ====== -->
<div class="menu-ball" id="menuBall" onclick="toggleBallMenu()">
  <svg class="menu-ball-svg" viewBox="0 0 62 62" xmlns="http://www.w3.org/2000/svg">
    <!-- Retro stitching seam (vertical) -->
    <path d="M31 6 Q33 15 31 22 Q29 29 31 36 Q33 43 31 50 Q29 54 31 56" fill="none" stroke="rgba(90,58,30,0.45)" stroke-width="1.2" stroke-dasharray="3 2"/>
    <!-- Cross stitch marks along seam -->
    <line x1="29" y1="12" x2="33" y2="14" stroke="rgba(90,58,30,0.35)" stroke-width="0.8"/>
    <line x1="33" y1="18" x2="29" y2="20" stroke="rgba(90,58,30,0.35)" stroke-width="0.8"/>
    <line x1="29" y1="26" x2="33" y2="28" stroke="rgba(90,58,30,0.35)" stroke-width="0.8"/>
    <line x1="33" y1="34" x2="29" y2="36" stroke="rgba(90,58,30,0.35)" stroke-width="0.8"/>
    <line x1="29" y1="42" x2="33" y2="44" stroke="rgba(90,58,30,0.35)" stroke-width="0.8"/>
    <line x1="33" y1="48" x2="29" y2="50" stroke="rgba(90,58,30,0.35)" stroke-width="0.8"/>
    <!-- Valve circle -->
    <circle cx="44" cy="20" r="3" fill="none" stroke="rgba(90,58,30,0.4)" stroke-width="0.8"/>
    <circle cx="44" cy="20" r="1" fill="rgba(90,58,30,0.3)"/>
  </svg>
  <span class="menu-ball-text">меню</span>
</div>
<div class="menu-panel" id="menuPanel">
  <a href="#standings" onclick="closeBallMenu()"><span class="menu-icon">📊</span> Таблица</a>
  <a href="#regulations" onclick="closeBallMenu()"><span class="menu-icon">📜</span> Регламент</a>
  <a href="#schedule" onclick="closeBallMenu()"><span class="menu-icon">📅</span> Расписание</a>
  <a href="#teams" onclick="closeBallMenu()"><span class="menu-icon">👥</span> Команды</a>
  <a href="#judges" onclick="closeBallMenu()"><span class="menu-icon">⚖️</span> Судьи</a>
  <a href="#organization" onclick="closeBallMenu()"><span class="menu-icon">📋</span> Организация</a>
  <a href="javascript:void(0)" onclick="closeBallMenu();openMiniGame()"><span class="menu-icon">🎮</span> Мини-игра</a>
</div>

<!-- ====== HERO ====== -->
<section class="hero" id="hero">
  <div class="hero-bg">
    <svg viewBox="0 0 1440 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
      <defs>
        <radialGradient id="heroGlow" cx="50%" cy="40%" r="60%">
          <stop offset="0%" style="stop-color:#152d5a;stop-opacity:0.6"/>
          <stop offset="100%" style="stop-color:#070e1a;stop-opacity:1"/>
        </radialGradient>
        <pattern id="hexGrid" x="0" y="0" width="60" height="52" patternUnits="userSpaceOnUse" patternTransform="rotate(15)">
          <polygon points="30,2 54,15 54,37 30,50 6,37 6,15" fill="none" stroke="rgba(232,122,58,0.04)" stroke-width="0.5"/>
        </pattern>
        <linearGradient id="lineGrad" x1="0%" y1="0%" x2="100%" y2="0%">
          <stop offset="0%" style="stop-color:rgba(232,122,58,0);"/>
          <stop offset="50%" style="stop-color:rgba(232,122,58,0.15);"/>
          <stop offset="100%" style="stop-color:rgba(232,122,58,0);"/>
        </linearGradient>
      </defs>
      <rect fill="url(#heroGlow)" width="1440" height="900"/>
      <rect fill="url(#hexGrid)" width="1440" height="900"/>
      <line x1="0" y1="300" x2="1440" y2="300" stroke="url(#lineGrad)" stroke-width="0.5"/>
      <line x1="0" y1="600" x2="1440" y2="600" stroke="url(#lineGrad)" stroke-width="0.5"/>
      <line x1="200" y1="0" x2="500" y2="900" stroke="rgba(232,122,58,0.03)" stroke-width="1"/>
      <line x1="940" y1="0" x2="1240" y2="900" stroke="rgba(232,122,58,0.03)" stroke-width="1"/>
      <circle cx="720" cy="450" r="200" fill="none" stroke="rgba(232,122,58,0.04)" stroke-width="0.5"/>
      <circle cx="720" cy="450" r="300" fill="none" stroke="rgba(232,122,58,0.025)" stroke-width="0.5"/>
      <circle cx="720" cy="450" r="400" fill="none" stroke="rgba(232,122,58,0.015)" stroke-width="0.5"/>
    </svg>
    <div class="hero-cosmos" aria-hidden="true">
      <div class="hero-stars hero-stars-1"></div>
      <div class="hero-stars hero-stars-2"></div>
      <div class="hero-nebula hero-nebula-1"></div>
      <div class="hero-nebula hero-nebula-2"></div>
      <div class="hero-comet"></div>
      <div class="hero-satellite">
        <span class="sat-panel left"></span>
        <span class="sat-core"></span>
        <span class="sat-dish"></span>
        <span class="sat-panel right"></span>
      </div>
      <div class="hero-planet"></div>
    </div>
  </div>
  <div class="hero-gradient"></div>

  <div class="hero-content">
    <div class="hero-emblem-wrap">
      <img class="hero-emblem-image" src="data:image/webp;base64,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" alt="Логотип турнира Кубок Дружбы Смоленск 2026" onerror="this.style.display='none'; var fallback = this.parentElement.querySelector('.hero-emblem'); if (fallback) fallback.style.display='block';">
    </div>

    <!-- Tournament Emblem SVG -->
    <svg class="hero-emblem" viewBox="0 0 200 240" xmlns="http://www.w3.org/2000/svg" aria-label="Эмблема турнира Кубок Дружбы 2026 — Смоленск" style="display:none;">
      <defs>
        <linearGradient id="shieldGrad" x1="0%" y1="0%" x2="0%" y2="100%">
          <stop offset="0%" style="stop-color:#f5a070"/>
          <stop offset="100%" style="stop-color:#e87a3a"/>
        </linearGradient>
        <linearGradient id="shieldInner" x1="0%" y1="0%" x2="0%" y2="100%">
          <stop offset="0%" style="stop-color:#0f2347"/>
          <stop offset="100%" style="stop-color:#0a1628"/>
        </linearGradient>
        <linearGradient id="ballGrad" x1="0%" y1="0%" x2="100%" y2="100%">
          <stop offset="0%" style="stop-color:#fbb990"/>
          <stop offset="100%" style="stop-color:#e87a3a"/>
        </linearGradient>
      </defs>
      <!-- Shield outer -->
      <path d="M100 8 L185 50 L185 140 Q185 195 100 232 Q15 195 15 140 L15 50 Z" fill="url(#shieldGrad)" stroke="none"/>
      <!-- Shield inner -->
      <path d="M100 18 L177 56 L177 140 Q177 190 100 224 Q23 190 23 140 L23 56 Z" fill="url(#shieldInner)" stroke="none"/>
      <!-- Orange inner border -->
      <path d="M100 26 L170 61 L170 140 Q170 185 100 217 Q30 185 30 140 L30 61 Z" fill="none" stroke="url(#shieldGrad)" stroke-width="0.8" opacity="0.35"/>

      <!-- === Smolensk Fortress Wall silhouette === -->
      <g stroke="url(#ballGrad)" fill="none" stroke-linecap="round" stroke-linejoin="round">
        <!-- Main wall base line -->
        <path d="M42 130 L42 108 L50 108 L50 100 L56 100 L56 108 L64 108 L64 130" stroke-width="1.5" opacity="0.6"/>
        <!-- Left wall crenellations (merlons) -->
        <path d="M42 130 L42 125 M46 125 L46 130 M50 130 L50 125 M54 125 L54 130 M58 130 L58 125 M62 125 L62 130" stroke-width="1" opacity="0.35"/>
        
        <!-- CENTER TOWER (taller, prominent) -->
        <path d="M82 130 L82 78 L88 78 L88 70 L94 70 L94 65 L100 62 L106 65 L106 70 L112 70 L112 78 L118 78 L118 130" stroke-width="1.8"/>
        <!-- Tower pointed roof tip -->
        <path d="M100 62 L100 55" stroke-width="1.5"/>
        <circle cx="100" cy="53" r="2" fill="#e87a3a" opacity="0.8"/>
        <!-- Tower brick pattern (horizontal lines) -->
        <path d="M86 85 L114 85 M84 92 L116 92 M83 100 L117 100 M82 108 L118 108 M82 116 L118 116 M82 124 L118 124" stroke-width="0.6" opacity="0.25"/>
        <!-- Tower vertical brick joints -->
        <path d="M92 78 L92 130 M100 70 L100 130 M108 78 L108 130" stroke-width="0.4" opacity="0.15"/>
        <!-- Tower arch window -->
        <path d="M95 88 Q100 82 105 88 L105 96 L95 96 Z" fill="none" stroke-width="1.2" opacity="0.7"/>

        <!-- Right wall section -->
        <path d="M136 130 L136 108 L144 108 L144 100 L150 100 L150 108 L158 108 L158 130" stroke-width="1.5" opacity="0.6"/>
        <!-- Right wall crenellations -->
        <path d="M138 130 L138 125 M142 125 L142 130 M146 130 L146 125 M150 125 L150 130 M154 130 L154 125 M158 125 L158 130" stroke-width="1" opacity="0.35"/>

        <!-- Connecting walls -->
        <path d="M64 130 L64 120 L82 120 L82 130" stroke-width="1" opacity="0.4"/>
        <path d="M118 130 L118 120 L136 120 L136 130" stroke-width="1" opacity="0.4"/>
      </g>

      <!-- === Football (soccer ball) — inside tower arch area === -->
      <g transform="translate(100, 148)">
        <circle cx="0" cy="0" r="14" fill="none" stroke="url(#ballGrad)" stroke-width="1.5"/>
        <polygon points="0,-6 5.7,-1.8 3.5,4.8 -3.5,4.8 -5.7,-1.8" fill="none" stroke="url(#ballGrad)" stroke-width="0.8" opacity="0.7"/>
        <!-- Ball panel lines -->
        <path d="M0,-14 L0,-6 M-13.3,4.3 L-5.7,-1.8 M13.3,4.3 L5.7,-1.8 M-8.2,11.3 L-3.5,4.8 M8.2,11.3 L3.5,4.8" stroke="url(#ballGrad)" stroke-width="0.7" opacity="0.5"/>
      </g>

      <!-- === Ground line === -->
      <line x1="35" y1="170" x2="165" y2="170" stroke="url(#shieldGrad)" stroke-width="0.6" opacity="0.3"/>

      <!-- === Year 2026 === -->
      <text x="100" y="190" text-anchor="middle" font-family="'Clash Display', sans-serif" font-weight="700" font-size="16" fill="#e87a3a" letter-spacing="0.2em">2026</text>

      <!-- === Subtle stars flanking the tower top === -->
      <g fill="#e87a3a" opacity="0.5">
        <polygon points="65,68 67,73 72,73 68,76 69,81 65,78 61,81 62,76 58,73 63,73"/>
        <polygon points="135,68 137,73 142,73 138,76 139,81 135,78 131,81 132,76 128,73 133,73"/>
      </g>
    </svg>

    <div class="hero-pretitle">Братский футбол</div>
    <h1 class="hero-title">Кубок Дружбы</h1>
    <div class="hero-year">Смоленск 2026</div>

    <div class="hero-meta">
      <div class="hero-meta-item">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="4" width="18" height="18" rx="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/></svg>
        Апрель 2026
      </div>
      <div class="hero-meta-item">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
        6 команд
      </div>
      <div class="hero-meta-item">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
        15 матчей
      </div>
      <div class="hero-meta-item">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
        Круговой турнир
      </div>
    </div>
  </div>

  <div class="hero-scroll">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><polyline points="6 9 12 15 18 9"/></svg>
  </div>
</section>

<!-- ====== STANDINGS ====== -->
<section id="standings">
  <div class="container">

    <!-- Regulation Buttons -->
    <div class="regulations-row" id="regulations">
      <div class="reg-btn" onclick="toggleReg('tournament')">
        <span class="reg-btn-icon">🏆</span>
        <span class="reg-btn-text">Регламент Турнира</span>
        <svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><polyline points="6 9 12 15 18 9"/></svg>
      </div>
      <div class="reg-btn" onclick="toggleReg('judges')">
        <span class="reg-btn-icon">📜</span>
        <span class="reg-btn-text">Регламент Судейства</span>
        <svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><polyline points="6 9 12 15 18 9"/></svg>
      </div>
    </div>

    <!-- Tournament Regulation Content -->
    <div class="reg-content" id="regTournament">
      <div class="reg-content-inner">
        <h4>🏆 Регламент Турнира</h4>
        <p>Текст регламента турнира будет добавлен позже.</p>
      </div>
    </div>

    <!-- Judging Regulation Content -->
    <div class="reg-content" id="regJudges">
      <div class="reg-content-inner">
        <h4>📜 Регламент Судейства</h4>
        <p>Текст регламента судейства будет добавлен позже.</p>
      </div>
    </div>

    <div class="info-grid">
      <div class="info-card">
        <div class="info-value">6</div>
        <div class="info-label">Команд</div>
      </div>
      <div class="info-card">
        <div class="info-value">15</div>
        <div class="info-label">Матчей</div>
      </div>
      <div class="info-card">
        <div class="info-value">12 мин</div>
        <div class="info-label">Длительность</div>
      </div>
      <div class="info-card">
        <div class="info-value">14:00</div>
        <div class="info-label">Начало</div>
      </div>
    </div>

    <div class="section-header">
      <div class="orange-line"></div>
      <h2 class="section-title">Турнирная таблица</h2>
      <p class="section-subtitle">Текущее положение команд в турнире</p>
    </div>

    <div class="standings-wrapper" id="standingsTable">
      <!-- Filled by JS -->
    </div>
  </div>
</section>

<!-- ====== SCHEDULE ====== -->
<section id="schedule">
  <div class="container">
    <div class="section-header">
      <div class="orange-line"></div>
      <h2 class="section-title">Расписание матчей</h2>
      <p class="section-subtitle">Полное расписание всех 15 матчей кругового турнира</p>
    </div>
    <div class="schedule-grid" id="scheduleGrid">
      <!-- Filled by JS -->
    </div>
  </div>
</section>

<!-- ====== TEAMS ====== -->
<section id="teams">
  <div class="container">
    <div class="section-header">
      <div class="orange-line"></div>
      <h2 class="section-title">Команды</h2>
      <p class="section-subtitle">6 команд-участниц турнира · Нажмите на карточку для просмотра состава</p>
    </div>
    <div class="teams-grid" id="teamsGrid">
      <!-- Filled by JS -->
    </div>
  </div>
</section>

<!-- ====== JUDGES ====== -->
<section id="judges">
  <div class="container">
    <div class="section-header">
      <div class="orange-line"></div>
      <h2 class="section-title">Судьи</h2>
      <p class="section-subtitle">Судейская бригада турнира</p>
    </div>
    <div class="judges-list" id="judgesGrid">
      <!-- Filled by JS -->
    </div>
  </div>
</section>

<!-- ====== ORGANIZATION ====== -->
<section id="organization">
  <div class="container">
    <div class="section-header">
      <div class="orange-line"></div>
      <h2 class="section-title">Организация</h2>
      <p class="section-subtitle">Задачи и ответственные за подготовку турнира</p>
    </div>
    <div class="org-grid" id="orgGrid">
      <!-- Filled by JS -->
    </div>

    <!-- Budget -->
    <div class="budget-card">
      <div class="budget-card-title">💰 Бюджет турнира</div>
      <table class="budget-table">
        <thead>
          <tr>
            <th>Категория</th>
            <th>Планируемо</th>
            <th>Факт</th>
          </tr>
        </thead>
        <tbody id="budgetBody">
          <!-- Filled by JS -->
        </tbody>
        <tfoot>
          <tr class="budget-total-row">
            <td>ИТОГО</td>
            <td id="budgetTotalPlan">0 ₽</td>
            <td id="budgetTotalFact">0 ₽</td>
          </tr>
        </tfoot>
      </table>
    </div>

    <!-- Venue -->
    <div class="venue-card">
      <div class="venue-card-header">
        <div class="venue-icon">🏟️</div>
        <div class="venue-info">
          <h3>Место проведения</h3>
          <p>Манеж № 1 · ул. Посёлок Тихвинка, 19Е · Смоленск</p>
        </div>
      </div>
      <div class="venue-map-container">
        <iframe src="https://yandex.ru/map-widget/v1/?ll=32.076261%2C54.755986&z=16&pt=32.076261%2C54.755986%2Cpm2orl&mode=search&text=%D0%9C%D0%B0%D0%BD%D0%B5%D0%B6%20%E2%84%96%201%20%D0%A2%D0%B8%D1%85%D0%B2%D0%B8%D0%BD%D0%BA%D0%B0%2019%D0%95" allowfullscreen loading="lazy"></iframe>
      </div>
      <div class="venue-link-row">
        <a href="https://yandex.ru/maps/org/manezh_1/15496579209" target="_blank" rel="noopener noreferrer">
          📍 Открыть в Яндекс Картах →
        </a>
      </div>
    </div>
  </div>
</section>

<!-- ====== FOOTER ====== -->
<footer class="footer">
  <div class="container">
    <div class="footer-brand">Кубок Дружбы 2026</div>
    <p class="footer-text">Официальный турнирный портал · Апрель 2026</p>
    <div class="footer-credits">
      <div class="footer-credit-line"><strong>Разработка:</strong> Alexander Rum</div>
      <div class="footer-credit-line"><strong>Креативная команда:</strong> "Темная лошадка", Смоленск</div>
    </div>
    <a href="#hero">Вернуться наверх ↑</a>
  </div>
</footer>

<script>
// ============================================================
// TOURNAMENT DATA
// ============================================================

const teams = [
  { id: 1, name: 'Тёмная Лошадка', abbr: 'ТЛ', city: 'Смоленск', color: '#7c3aed' },
  { id: 2, name: 'Альтернатива', abbr: 'АЛ', city: 'Смоленск', color: '#2563eb' },
  { id: 3, name: 'Брянск', abbr: 'БР', city: 'Брянск', color: '#dc2626' },
  { id: 4, name: 'Орёл', abbr: 'ОР', city: 'Орёл', color: '#16a34a' },
  { id: 5, name: 'Орша', abbr: 'ОШ', city: 'Орша', color: '#0891b2' },
  { id: 6, name: 'Витебск', abbr: 'ВТБ', city: 'Витебск', color: '#4a90d9' },
];

const matches = [
  { num: 1, round: 1, home: 'Тёмная Лошадка', away: 'Витебск', time: '14:00-14:12' },
  { num: 2, round: 1, home: 'Альтернатива', away: 'Орша', time: '14:15-14:27' },
  { num: 3, round: 1, home: 'Брянск', away: 'Орёл', time: '14:30-14:42' },
  { num: 4, round: 2, home: 'Тёмная Лошадка', away: 'Орша', time: '14:45-14:57' },
  { num: 5, round: 2, home: 'Витебск', away: 'Орёл', time: '15:00-15:12' },
  { num: 6, round: 2, home: 'Альтернатива', away: 'Брянск', time: '15:15-15:27' },
  { num: 7, round: 3, home: 'Тёмная Лошадка', away: 'Орёл', time: '15:30-15:42' },
  { num: 8, round: 3, home: 'Орша', away: 'Брянск', time: '15:45-15:57' },
  { num: 9, round: 3, home: 'Витебск', away: 'Альтернатива', time: '16:00-16:12' },
  { num: 10, round: 4, home: 'Тёмная Лошадка', away: 'Брянск', time: '16:15-16:27' },
  { num: 11, round: 4, home: 'Орёл', away: 'Альтернатива', time: '16:30-16:42' },
  { num: 12, round: 4, home: 'Орша', away: 'Витебск', time: '16:45-16:57' },
  { num: 13, round: 5, home: 'Тёмная Лошадка', away: 'Альтернатива', time: '17:00-17:12' },
  { num: 14, round: 5, home: 'Брянск', away: 'Витебск', time: '17:15-17:27' },
  { num: 15, round: 5, home: 'Орёл', away: 'Орша', time: '17:30-17:42' },
];

const judgesData = {
  main: { role: 'Главный судья', name: '' },
  assistants: [
    { role: 'Помощник судьи 1', name: '' },
    { role: 'Помощник судьи 2', name: '' },
    { role: 'Помощник судьи 3', name: '' },
    { role: 'Помощник судьи 4', name: '' },
    { role: 'Помощник судьи 5', name: '' },
  ]
};

const orgData = [
  { category: 'Площадка', icon: '🏟️', tasks: [
    { text: 'Подтвердить бронь зала', person: 'Юра' },
    { text: 'Уточнить время открытия зала', person: 'Юра' },
    { text: 'Уточнить время закрытия зала', person: 'Юра' },
  ]},
  { category: 'Расписание', icon: '📋', tasks: [
    { text: 'Составить таблицу матчей', person: 'Кэп' },
    { text: 'Утвердить длительность тайма', person: 'Кэп' },
  ]},
  { category: 'Команды', icon: '👥', tasks: [
    { text: 'Подтвердить 6 команд', person: 'Анд' },
    { text: 'Получить окончательные составы', person: 'Анд' },
  ]},
  { category: 'Финансы', icon: '💰', tasks: [
    { text: 'Определить размер взноса', person: 'Юра' },
    { text: 'Собрать взносы', person: 'Юра' },
  ]},
  { category: 'Вода', icon: '💧', tasks: [
    { text: 'Организовать бутыли с водой', person: 'Витя' },
  ]},
  { category: 'Перекусы', icon: '🍎', tasks: [
    { text: 'Определить формат перекусов', person: 'Витя' },
  ]},
  { category: 'Медицина', icon: '🏥', tasks: [
    { text: 'Собрать аптечку', person: 'Витя' },
    { text: 'Купить спортивную заморозку', person: 'Анд' },
  ]},
  { category: 'Судейство', icon: '⚖️', tasks: [
    { text: 'Назначить судью', person: 'Кэп' },
  ]},
  { category: 'Коммуникация', icon: '📢', tasks: [
    { text: 'Опубликовать регламент', person: 'Ром' },
    { text: 'Опубликовать расписание', person: 'Ром' },
  ]},
  { category: 'Финал', icon: '📸', tasks: [
    { text: 'Организовать фотосессию', person: 'Ром' },
  ]},
  { category: 'Инвентарь', icon: '⚽', tasks: [
    { text: 'Организовать мячи, свистки и др.', person: 'Анд' },
  ]},
  { category: 'Сувениры', icon: '🎁', tasks: [
    { text: 'Организация сувениров и подарков', person: 'Ром' },
  ]},
  { category: 'Размещение', icon: '🏨', tasks: [
    { text: 'Организовать ночлег для игроков', person: '?' },
  ]},
];

const budgetItems = [
  'Аренда зала',
  'Вода',
  'Перекусы',
  'Аптечка',
  'Печать материалов (Ром)',
  'Прочие расходы',
];

// ============================================================
// SVG BADGE GENERATOR
// ============================================================

function createTeamBadge(abbr, color, size = 56) {
  const lighterColor = color + '33'; // ~20% opacity for background
  return `<svg width="${size}" height="${size}" viewBox="0 0 ${size} ${size}" xmlns="http://www.w3.org/2000/svg">
    <circle cx="${size/2}" cy="${size/2}" r="${size/2 - 2}" fill="${lighterColor}" stroke="${color}" stroke-width="2.5"/>
    <text x="${size/2}" y="${size/2}" text-anchor="middle" dominant-baseline="central" font-family="'Clash Display', sans-serif" font-weight="700" font-size="${size * 0.32}" fill="${color}">${abbr}</text>
  </svg>`;
}

// ============================================================
// RENDER FUNCTIONS
// ============================================================

function calcStandings() {
  // Calculate standings from current score inputs
  const stats = {};
  teams.forEach(t => {
    stats[t.name] = { played: 0, won: 0, drawn: 0, lost: 0, gf: 0, ga: 0, pts: 0 };
  });

  matches.forEach(m => {
    const homeInput = document.querySelector(`.score-input[data-match="${m.num}"][data-side="home"]`);
    const awayInput = document.querySelector(`.score-input[data-match="${m.num}"][data-side="away"]`);
    if (!homeInput || !awayInput) return;
    const hg = parseInt(homeInput.value) || 0;
    const ag = parseInt(awayInput.value) || 0;

    // Only count if at least one goal entered or match is played
    const homeEl = homeInput;
    const awayEl = awayInput;
    const hasData = homeEl.classList.contains('has-value') || awayEl.classList.contains('has-value') || (hg > 0 || ag > 0);
    if (!hasData && hg === 0 && ag === 0) return;

    if (stats[m.home]) {
      stats[m.home].played++;
      stats[m.home].gf += hg;
      stats[m.home].ga += ag;
      if (hg > ag) { stats[m.home].won++; stats[m.home].pts += 3; }
      else if (hg === ag) { stats[m.home].drawn++; stats[m.home].pts += 1; }
      else { stats[m.home].lost++; }
    }
    if (stats[m.away]) {
      stats[m.away].played++;
      stats[m.away].gf += ag;
      stats[m.away].ga += hg;
      if (ag > hg) { stats[m.away].won++; stats[m.away].pts += 3; }
      else if (ag === hg) { stats[m.away].drawn++; stats[m.away].pts += 1; }
      else { stats[m.away].lost++; }
    }
  });

  return stats;
}

function renderStandings() {
  const el = document.getElementById('standingsTable');
  const stats = calcStandings();

  // Sort: points desc, then goal diff desc, then goals scored desc
  const sorted = teams.slice().sort((a, b) => {
    const sa = stats[a.name] || {};
    const sb = stats[b.name] || {};
    if ((sb.pts || 0) !== (sa.pts || 0)) return (sb.pts || 0) - (sa.pts || 0);
    const diffA = (sa.gf || 0) - (sa.ga || 0);
    const diffB = (sb.gf || 0) - (sb.ga || 0);
    if (diffB !== diffA) return diffB - diffA;
    return (sb.gf || 0) - (sa.gf || 0);
  });

  let html = `<table class="standings-table">
    <thead>
      <tr>
        <th>#</th>
        <th>Команда</th>
        <th>И</th>
        <th>В</th>
        <th>Н</th>
        <th>П</th>
        <th>ГЗ</th>
        <th>ГП</th>
        <th>РГ</th>
        <th>О</th>
      </tr>
    </thead>
    <tbody>`;

  sorted.forEach((team, i) => {
    const s = stats[team.name] || {};
    const diff = (s.gf || 0) - (s.ga || 0);
    const diffStr = diff > 0 ? '+' + diff : diff.toString();
    html += `<tr>
      <td class="rank">${i + 1}</td>
      <td>${team.name}</td>
      <td>${s.played || 0}</td>
      <td>${s.won || 0}</td>
      <td>${s.drawn || 0}</td>
      <td>${s.lost || 0}</td>
      <td>${s.gf || 0}</td>
      <td>${s.ga || 0}</td>
      <td>${diffStr}</td>
      <td class="points">${s.pts || 0}</td>
    </tr>`;
  });

  html += '</tbody></table>';
  el.innerHTML = html;
}

function renderSchedule() {
  const el = document.getElementById('scheduleGrid');
  let html = '';
  let currentRound = 0;

  const roundLabels = {
    1: 'Круг 1 — Стартовые матчи',
    2: 'Круг 2',
    3: 'Круг 3',
    4: 'Круг 4',
    5: 'Круг 5 — Финальные матчи',
  };

  matches.forEach(m => {
    if (m.round !== currentRound) {
      currentRound = m.round;
      html += `<div class="round-header">${roundLabels[currentRound] || 'Круг ' + currentRound}</div>`;
    }

    html += `<div class="match-card light-beam">
      <div class="match-number">${m.num}</div>
      <div class="match-body">
        <div class="match-team home">
          <span class="team-name">${m.home}</span>
        </div>
        <div class="match-score">
          <input type="number" class="score-input" min="0" max="99" value="0" data-match="${m.num}" data-side="home" onclick="this.select()">
          <span class="score-divider">:</span>
          <input type="number" class="score-input" min="0" max="99" value="0" data-match="${m.num}" data-side="away" onclick="this.select()">
        </div>
        <div class="match-team away">
          <span class="team-name">${m.away}</span>
        </div>
      </div>
      <div class="match-time">
        <div class="time">${m.time}</div>
        <div class="status">Предстоящий</div>
      </div>
    </div>`;
  });

  el.innerHTML = html;
}

function renderTeams() {
  const el = document.getElementById('teamsGrid');
  let html = '';

  teams.forEach((team, idx) => {
    // Build roster HTML
    const playerRoles = [
      { num: 1, role: 'Вратарь', type: 'field' },
      { num: 2, role: 'Полевой', type: 'field' },
      { num: 3, role: 'Полевой', type: 'field' },
      { num: 4, role: 'Полевой', type: 'field' },
      { num: 5, role: 'Полевой', type: 'field' },
      { num: 6, role: 'Полевой', type: 'field' },
      { num: 7, role: 'Замена', type: 'bench' },
      { num: 8, role: 'Замена', type: 'bench' },
      { num: 9, role: 'Замена', type: 'bench' },
      { num: 10, role: 'Замена', type: 'bench' },
    ];

    let rosterHTML = '';
    rosterHTML += '<div class="roster-section-title field">В поле — 6 игроков</div>';
    playerRoles.filter(p => p.type === 'field').forEach(p => {
      rosterHTML += `<div class="roster-player">
        <div class="player-frame field-frame">${p.num}</div>
        <span class="player-role">${p.role}</span>
        <input type="text" class="player-name-input" placeholder="Никнейм" data-team="${idx}" data-num="${p.num}" onclick="event.stopPropagation(); this.select();">
      </div>`;
    });
    rosterHTML += '<div class="roster-section-title bench">На замене — 4 игрока</div>';
    playerRoles.filter(p => p.type === 'bench').forEach(p => {
      rosterHTML += `<div class="roster-player">
        <div class="player-frame bench-frame">${p.num}</div>
        <span class="player-role">${p.role}</span>
        <input type="text" class="player-name-input" placeholder="Никнейм" data-team="${idx}" data-num="${p.num}" onclick="event.stopPropagation(); this.select();">
      </div>`;
    });

    html += `<div class="team-card light-beam" data-team="${idx}" onclick="toggleTeamRoster(${idx})">
      <div class="team-card-top" style="background: linear-gradient(90deg, ${team.color}, ${team.color}88);"></div>
      ${createTeamBadge(team.abbr, team.color)}
      <div class="team-name">${team.name}</div>
      <div class="team-city">${team.city}</div>
      <div class="team-expand-hint">▼ Состав</div>
      <div class="team-roster">${rosterHTML}</div>
    </div>`;
  });

  el.innerHTML = html;
}

function renderJudges() {
  const el = document.getElementById('judgesGrid');
  const whistleIcon = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><circle cx="12" cy="12" r="10"/><path d="M12 8v4l3 3"/></svg>';
  const groupIcon = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>';
  const chevronSvg = '<svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><polyline points="6 9 12 15 18 9"/></svg>';

  const mainName = judgesData.main.name || 'Не утверждён';

  let html = `
    <div class="judge-panel light-beam" onclick="this.classList.toggle('open')">
      <div class="judge-panel-header">
        <div class="judge-panel-icon">${whistleIcon}</div>
        <div class="judge-panel-title">Главный судья</div>
        <div class="judge-panel-status">${mainName}</div>
        ${chevronSvg}
      </div>
      <div class="judge-panel-body">
        <div class="judge-panel-content">
          <div class="judge-person">
            <div class="judge-person-num">1</div>
            <div class="judge-person-role">Главный судья</div>
            <input type="text" class="judge-name-input" placeholder="Никнейм" data-judge="main" onclick="event.stopPropagation(); this.select();">
          </div>
        </div>
      </div>
    </div>
    <div class="judge-panel light-beam" onclick="this.classList.toggle('open')">
      <div class="judge-panel-header">
        <div class="judge-panel-icon">${groupIcon}</div>
        <div class="judge-panel-title">Помощники судьи</div>
        <div class="judge-panel-status">5 человек</div>
        ${chevronSvg}
      </div>
      <div class="judge-panel-body">
        <div class="judge-panel-content">`;

  judgesData.assistants.forEach((a, i) => {
    html += `
          <div class="judge-person">
            <div class="judge-person-num muted">${i + 1}</div>
            <div class="judge-person-role">${a.role}</div>
            <input type="text" class="judge-name-input" placeholder="Никнейм" data-judge="assistant_${i}" onclick="event.stopPropagation(); this.select();">
          </div>`;
  });

  html += `
        </div>
      </div>
    </div>`;

  el.innerHTML = html;
}

function renderOrg() {
  const el = document.getElementById('orgGrid');
  let html = '';

  orgData.forEach((cat, i) => {
    html += `<div class="org-card${i < 3 ? ' open' : ''}" data-org="${i}">
      <div class="org-card-header" onclick="toggleOrg(${i})">
        <h3>${cat.icon} ${cat.category}</h3>
        <svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><polyline points="6 9 12 15 18 9"/></svg>
      </div>
      <div class="org-card-body">`;

    cat.tasks.forEach((task, j) => {
      html += `<div class="org-task">
        <div class="checkbox" onclick="event.stopPropagation(); toggleCheck(this)" data-cat="${i}" data-task="${j}"></div>
        <span class="task-text">${task.text}</span>
        <span class="task-person">${task.person}</span>
      </div>`;
    });

    html += '</div></div>';
  });

  el.innerHTML = html;
}

function renderBudget() {
  const el = document.getElementById('budgetBody');
  let html = '';

  budgetItems.forEach((item, i) => {
    html += `<tr>
      <td>${item}</td>
      <td><input type="text" inputmode="numeric" class="budget-input" data-budget="${i}" data-type="plan" placeholder="0 \u20bd"></td>
      <td><input type="text" inputmode="numeric" class="budget-input" data-budget="${i}" data-type="fact" placeholder="0 \u20bd"></td>
    </tr>`;
  });

  el.innerHTML = html;

  // Attach handlers
  document.querySelectorAll('.budget-input').forEach(input => {
    input.addEventListener('input', function() {
      // Allow only digits
      this.value = this.value.replace(/[^\d]/g, '');
      if (this.value) {
        this.classList.add('has-value');
      } else {
        this.classList.remove('has-value');
      }
      updateBudgetTotals();
      scheduleSave();
    });
    input.addEventListener('focus', function() {
      this.select();
    });
  });

  // Restore budget from localStorage
  try {
    const saved = JSON.parse(localStorage.getItem('kubokBudget') || '{}');
    document.querySelectorAll('.budget-input').forEach(input => {
      input.value = '';
      input.classList.remove('has-value');
    });
    Object.keys(saved).forEach(key => {
      const input = document.querySelector(`.budget-input[data-budget="${key.split('_')[0]}"][data-type="${key.split('_')[1]}"]`);
      if (input && saved[key] !== undefined && saved[key] !== null) {
        input.value = saved[key];
        input.classList.toggle('has-value', Boolean(saved[key]));
      }
    });
    updateBudgetTotals();
  } catch(e) {}
}

function updateBudgetTotals() {
  let totalPlan = 0, totalFact = 0;
  document.querySelectorAll('.budget-input[data-type="plan"]').forEach(input => {
    totalPlan += parseInt(input.value) || 0;
  });
  document.querySelectorAll('.budget-input[data-type="fact"]').forEach(input => {
    totalFact += parseInt(input.value) || 0;
  });
  const planEl = document.getElementById('budgetTotalPlan');
  const factEl = document.getElementById('budgetTotalFact');
  if (planEl) planEl.textContent = totalPlan.toLocaleString('ru-RU') + ' \u20bd';
  if (factEl) factEl.textContent = totalFact.toLocaleString('ru-RU') + ' \u20bd';
}

// ============================================================
// INTERACTIONS
// ============================================================

function toggleTeamRoster(idx) {
  const card = document.querySelector(`[data-team="${idx}"]`);
  const wasExpanded = card.classList.contains('expanded');
  
  // Close all other cards
  document.querySelectorAll('.team-card.expanded').forEach(c => {
    if (c !== card) c.classList.remove('expanded');
  });
  
  card.classList.toggle('expanded');
  
  // On mobile, scroll the opened card into view
  if (!wasExpanded && window.innerWidth <= 768) {
    setTimeout(() => {
      card.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }, 100);
  }
}

function toggleReg(type) {
  const id = type === 'tournament' ? 'regTournament' : 'regJudges';
  const otherId = type === 'tournament' ? 'regJudges' : 'regTournament';
  const panel = document.getElementById(id);
  const otherPanel = document.getElementById(otherId);
  const isOpen = panel.classList.contains('open');

  // Close the other one
  otherPanel.classList.remove('open');
  document.querySelectorAll('.reg-btn').forEach(btn => {
    const btnType = btn.onclick.toString().includes('tournament') ? 'tournament' : 'judges';
    if (btnType !== type) btn.classList.remove('open');
  });

  // Toggle this one
  panel.classList.toggle('open');
  // Toggle button state
  const btns = document.querySelectorAll('.reg-btn');
  btns.forEach(btn => {
    if (btn.querySelector('.reg-btn-text').textContent.includes(type === 'tournament' ? 'Турнир' : 'Судей')) {
      btn.classList.toggle('open', !isOpen);
    }
  });

  // On mobile, scroll into view
  if (!isOpen && window.innerWidth <= 768) {
    setTimeout(() => panel.scrollIntoView({ behavior: 'smooth', block: 'start' }), 100);
  }
}

function toggleOrg(idx) {
  const card = document.querySelector(`[data-org="${idx}"]`);
  card.classList.toggle('open');
}

function toggleCheck(el) {
  el.classList.toggle('checked');
  scheduleSave();
}

// Ball menu toggle
function toggleBallMenu() {
  const ball = document.getElementById('menuBall');
  const panel = document.getElementById('menuPanel');
  ball.classList.toggle('open');
  panel.classList.toggle('open');
}

function closeBallMenu() {
  document.getElementById('menuBall').classList.remove('open');
  document.getElementById('menuPanel').classList.remove('open');
}

// Close menu when clicking outside
document.addEventListener('click', (e) => {
  if (!e.target.closest('#menuBall') && !e.target.closest('#menuPanel')) {
    closeBallMenu();
  }
});

// ============================================================
// GOOGLE APPS SCRIPT API
// ============================================================
const API_URL = localStorage.getItem('kubokApiUrl') || 'https://script.google.com/macros/s/AKfycbyyYyHEb7Uba6BZOpdmU18Ge_DzGs0xjb_LVVvC9qmXOuEq3xVA9zh0cd2ZEyUQwuNg/exec';

let saveTimeout = null;

function collectAllData() {
  const scores = {};
  document.querySelectorAll('.score-input[data-side="home"]').forEach(input => {
    const num = input.dataset.match;
    const awayInput = document.querySelector(`.score-input[data-match="${num}"][data-side="away"]`);
    scores[num] = {
      home: parseInt(input.value) || 0,
      away: parseInt(awayInput?.value) || 0
    };
  });

  const players = {};
  document.querySelectorAll('.player-name-input').forEach(input => {
    const key = input.dataset.team + '_' + input.dataset.num;
    if (input.value.trim()) {
      players[key] = input.value.trim();
    }
  });

  const judges = {};
  document.querySelectorAll('.judge-name-input').forEach(input => {
    if (input.value.trim()) {
      judges[input.dataset.judge] = input.value.trim();
    }
  });

  const checkboxes = {};
  document.querySelectorAll('.checkbox').forEach(el => {
    const key = el.dataset.cat + '_' + el.dataset.task;
    checkboxes[key] = el.classList.contains('checked');
  });

  const budget = {};
  document.querySelectorAll('.budget-input').forEach(input => {
    const key = input.dataset.budget + '_' + input.dataset.type;
    budget[key] = input.value.trim();
  });

  return { scores, players, judges, checkboxes, budget };
}

function persistLocalSnapshot(snapshot) {
  localStorage.setItem('kubokPlayers', JSON.stringify(snapshot.players));
  localStorage.setItem('kubokJudges', JSON.stringify(snapshot.judges));
  localStorage.setItem('kubokCheckboxes', JSON.stringify(snapshot.checkboxes));
  localStorage.setItem('kubokBudget', JSON.stringify(snapshot.budget));
}

async function postApi(payload, keepalive = false) {
  const res = await fetch(API_URL, {
    method: 'POST',
    body: JSON.stringify(payload),
    headers: { 'Content-Type': 'text/plain;charset=utf-8' },
    redirect: 'follow',
    mode: 'cors',
    keepalive
  });

  if (res.type === 'opaque') return true;
  if (!res.ok) {
    throw new Error(`HTTP ${res.status}`);
  }
  return true;
}

// ---- RESTORE: localStorage first (instant), then API overwrites ----
async function loadData() {
  restoreFromLocalStorage();
  
  if (!API_URL) return;
  try {
    const res = await fetch(API_URL + '?action=getAll', { redirect: 'follow' });
    const data = await res.json();
    
    // Restore scores from API
    if (data.scores) {
      Object.keys(data.scores).forEach(matchNum => {
        const homeInput = document.querySelector(`.score-input[data-match="${matchNum}"][data-side="home"]`);
        const awayInput = document.querySelector(`.score-input[data-match="${matchNum}"][data-side="away"]`);
        if (homeInput && data.scores[matchNum].home != null) {
          homeInput.value = data.scores[matchNum].home;
          if (parseInt(homeInput.value) > 0) homeInput.classList.add('has-value');
        }
        if (awayInput && data.scores[matchNum].away != null) {
          awayInput.value = data.scores[matchNum].away;
          if (parseInt(awayInput.value) > 0) awayInput.classList.add('has-value');
        }
      });
    }
    
    // Restore players from API
    if (data.players && Object.keys(data.players).length > 0) {
      Object.keys(data.players).forEach(key => {
        const [teamIdx, playerNum] = key.split('_');
        const input = document.querySelector(`.player-name-input[data-team="${teamIdx}"][data-num="${playerNum}"]`);
        if (input && data.players[key]) {
          input.value = data.players[key];
          input.classList.add('has-name');
        }
      });
      localStorage.setItem('kubokPlayers', JSON.stringify(data.players));
    }
    
    // Restore judges from API
    if (data.judges && Object.keys(data.judges).length > 0) {
      Object.keys(data.judges).forEach(key => {
        const input = document.querySelector(`.judge-name-input[data-judge="${key}"]`);
        if (input && data.judges[key]) {
          input.value = data.judges[key];
          input.classList.add('has-name');
        }
      });
      localStorage.setItem('kubokJudges', JSON.stringify(data.judges));
    }
    
    // Restore checkboxes from API
    if (data.checkboxes && Object.keys(data.checkboxes).length > 0) {
      document.querySelectorAll('.checkbox.checked').forEach(el => el.classList.remove('checked'));
      Object.keys(data.checkboxes).forEach(key => {
        const [cat, task] = key.split('_');
        const el = document.querySelector(`.checkbox[data-cat="${cat}"][data-task="${task}"]`);
        if (el && data.checkboxes[key]) el.classList.add('checked');
      });
      localStorage.setItem('kubokCheckboxes', JSON.stringify(data.checkboxes));
    }
    
    // Restore budget from API
    if (data.budget && Object.keys(data.budget).length > 0) {
      document.querySelectorAll('.budget-input').forEach(input => {
        input.value = '';
        input.classList.remove('has-value');
      });
      Object.keys(data.budget).forEach(key => {
        const [idx, type] = key.split('_');
        const input = document.querySelector(`.budget-input[data-budget="${idx}"][data-type="${type}"]`);
        if (input && data.budget[key] !== undefined && data.budget[key] !== null) {
          input.value = data.budget[key];
          input.classList.toggle('has-value', Boolean(data.budget[key]));
        }
      });
      localStorage.setItem('kubokBudget', JSON.stringify(data.budget));
      updateBudgetTotals();
    }
    
    renderStandings();
    console.log('Данные загружены из API');
  } catch (e) {
    console.error('Ошибка загрузки API (используются локальные данные):', e);
  }
}

function restoreFromLocalStorage() {
  // Players from localStorage
  try {
    const players = JSON.parse(localStorage.getItem('kubokPlayers') || '{}');
    Object.keys(players).forEach(key => {
      const [teamIdx, playerNum] = key.split('_');
      const input = document.querySelector(`.player-name-input[data-team="${teamIdx}"][data-num="${playerNum}"]`);
      if (input && players[key]) {
        input.value = players[key];
        input.classList.add('has-name');
      }
    });
  } catch(e) {}
  
  // Judges from localStorage
  try {
    const judges = JSON.parse(localStorage.getItem('kubokJudges') || '{}');
    Object.keys(judges).forEach(key => {
      const input = document.querySelector(`.judge-name-input[data-judge="${key}"]`);
      if (input && judges[key]) {
        input.value = judges[key];
        input.classList.add('has-name');
      }
    });
  } catch(e) {}
  
  // Checkboxes from localStorage
  try {
    const checks = JSON.parse(localStorage.getItem('kubokCheckboxes') || '{}');
    document.querySelectorAll('.checkbox.checked').forEach(el => el.classList.remove('checked'));
    Object.keys(checks).forEach(key => {
      const [cat, task] = key.split('_');
      const el = document.querySelector(`.checkbox[data-cat="${cat}"][data-task="${task}"]`);
      if (el && checks[key]) el.classList.add('checked');
    });
  } catch(e) {}
  
  // Budget from localStorage
  try {
    const budget = JSON.parse(localStorage.getItem('kubokBudget') || '{}');
    document.querySelectorAll('.budget-input').forEach(input => {
      input.value = '';
      input.classList.remove('has-value');
    });
    Object.keys(budget).forEach(key => {
      const [idx, type] = key.split('_');
      const input = document.querySelector(`.budget-input[data-budget="${idx}"][data-type="${type}"]`);
      if (input && budget[key] !== undefined && budget[key] !== null) {
        input.value = budget[key];
        input.classList.toggle('has-value', Boolean(budget[key]));
      }
    });
    updateBudgetTotals();
  } catch(e) {}
}

// ---- SAVE: always to localStorage + API ----
function scheduleSave() {
  const snapshot = collectAllData();
  persistLocalSnapshot(snapshot);
  clearTimeout(saveTimeout);
  saveTimeout = setTimeout(() => saveAllData(snapshot), 1200);
}

async function saveAllData(snapshot = null, keepalive = false) {
  try {
    const data = snapshot || collectAllData();
    persistLocalSnapshot(data);

    if (!API_URL) return;

    try {
      await postApi({ action: 'saveAllData', ...data }, keepalive);
    } catch (unifiedError) {
      await postApi({ action: 'saveAllScores', scores: data.scores }, keepalive);
      await postApi({
        action: 'saveAllPlayers',
        players: data.players,
        judges: data.judges,
        checkboxes: data.checkboxes,
        budget: data.budget
      }, keepalive);
      console.warn('saveAllData недоступен, использован запасной режим:', unifiedError);
    }

    console.log('Сохранено (localStorage + API)');
  } catch (e) {
    console.error('Ошибка сохранения в API (локально сохранено):', e);
  }
}

function flushSaveOnExit() {
  clearTimeout(saveTimeout);
  saveAllData(collectAllData(), true);
}

// API URL setup via menu
function setupApi() {
  const current = localStorage.getItem('kubokApiUrl') || '';
  const url = prompt('Вставьте URL вашего Google Apps Script \u0432еб-приложения:', current);
  if (url !== null) {
    localStorage.setItem('kubokApiUrl', url.trim());
    location.reload();
  }
}

// ============================================================
// INIT
// ============================================================
renderSchedule();
renderTeams();
renderJudges();
renderOrg();
renderBudget();
renderStandings();

// Score input handlers
document.querySelectorAll('.score-input').forEach(input => {
  input.addEventListener('input', function() {
    const val = parseInt(this.value) || 0;
    if (val > 0) {
      this.classList.add('has-value');
    } else {
      this.classList.remove('has-value');
    }
    if (this.value !== '' && val > 99) this.value = 99;
    if (this.value !== '' && val < 0) this.value = 0;
    // Recalculate standings live
    renderStandings();
    // Auto-save
    scheduleSave();
  });
  input.addEventListener('focus', function() {
    this.select();
  });
});

// Player name input handlers
document.querySelectorAll('.player-name-input').forEach(input => {
  input.addEventListener('input', function() {
    if (this.value.trim()) {
      this.classList.add('has-name');
    } else {
      this.classList.remove('has-name');
    }
    // Auto-save
    scheduleSave();
  });
  input.addEventListener('focus', function(e) {
    e.stopPropagation();
    this.select();
  });
});

// Judge name input handlers
document.querySelectorAll('.judge-name-input').forEach(input => {
  input.addEventListener('input', function() {
    if (this.value.trim()) {
      this.classList.add('has-name');
    } else {
      this.classList.remove('has-name');
    }
    scheduleSave();
  });
  input.addEventListener('focus', function(e) {
    e.stopPropagation();
    this.select();
  });
});

window.addEventListener('pagehide', flushSaveOnExit);
window.addEventListener('beforeunload', flushSaveOnExit);
document.addEventListener('visibilitychange', () => {
  if (document.visibilityState === 'hidden') {
    flushSaveOnExit();
  }
});

// Load data from Google Sheets on startup
loadData();

// ============================================================
// MINI-GAME: Удар по воротам
// ============================================================
let gameActive = false;
let gameRAF = null;
let gameCleanup = null;

const gameAssets = {
  goal: Object.assign(new Image(), { src: 'ворота 2.png' }),
  keeper: {
    low: Object.assign(new Image(), { src: 'ловлю.PNG' }),
    save: Object.assign(new Image(), { src: 'отбито.png' }),
    miss: Object.assign(new Image(), { src: 'мимо.PNG' }),
    goal: Object.assign(new Image(), { src: 'гол.PNG' }),
  },
  ball: {
    idle: Object.assign(new Image(), { src: 'мяч.PNG' }),
  },
};

function imageReady(img) {
  return img && img.complete && img.naturalWidth > 0;
}

function drawImageCover(ctx, img, x, y, w, h) {
  if (!imageReady(img)) return false;
  const srcW = img.naturalWidth;
  const srcH = img.naturalHeight;
  const srcRatio = srcW / srcH;
  const dstRatio = w / h;
  let cropW = srcW;
  let cropH = srcH;
  let cropX = 0;
  let cropY = 0;

  if (srcRatio > dstRatio) {
    cropW = srcH * dstRatio;
    cropX = (srcW - cropW) / 2;
  } else {
    cropH = srcW / dstRatio;
    cropY = (srcH - cropH) / 2;
  }

  ctx.drawImage(img, cropX, cropY, cropW, cropH, x, y, w, h);
  return true;
}

function drawImageContain(ctx, img, x, y, w, h) {
  if (!imageReady(img)) return false;
  const scale = Math.min(w / img.naturalWidth, h / img.naturalHeight);
  const drawW = img.naturalWidth * scale;
  const drawH = img.naturalHeight * scale;
  const drawX = x + (w - drawW) / 2;
  const drawY = y + (h - drawH) / 2;
  ctx.drawImage(img, drawX, drawY, drawW, drawH);
  return true;
}

function openMiniGame() {
  document.getElementById('gameOverlay').style.display = 'flex';
  document.body.style.overflow = 'hidden';
  if (gameCleanup) gameCleanup();
  initGame();
}

function closeMiniGame() {
  document.getElementById('gameOverlay').style.display = 'none';
  document.body.style.overflow = '';
  gameActive = false;
  if (gameRAF) cancelAnimationFrame(gameRAF);
  if (gameCleanup) {
    gameCleanup();
    gameCleanup = null;
  }
}

function initGame() {
  const canvas = document.getElementById('gameCanvas');
  const ctx = canvas.getContext('2d');
  const overlay = document.getElementById('gameOverlay');
  let viewportWidth = 0;
  let viewportHeight = 0;
  
  function resizeCanvas() {
    const dpr = Math.max(1, Math.min(window.devicePixelRatio || 1, 3));
    viewportWidth = overlay.clientWidth;
    viewportHeight = overlay.clientHeight;
    canvas.width = Math.round(viewportWidth * dpr);
    canvas.height = Math.round(viewportHeight * dpr);
    canvas.style.width = viewportWidth + 'px';
    canvas.style.height = viewportHeight + 'px';
    ctx.setTransform(dpr, 0, 0, dpr, 0, 0);
    ctx.imageSmoothingEnabled = true;
    ctx.imageSmoothingQuality = 'high';
  }
  resizeCanvas();
  window.addEventListener('resize', resizeCanvas);

  // Game state
  let score = 0;
  let lives = 5;
  let level = 1;
  let shotFired = false;
  let showResult = false;
  let resultText = '';
  let resultTimer = 0;
  let highScore = parseInt(localStorage.getItem('kubokGameHigh') || '0');
  let gameOver = false;
  let stars = [];
  let keeperReaction = '';
  gameActive = true;

  // Generate retro stars background
  for (let i = 0; i < 60; i++) {
    stars.push({
      x: Math.random(),
      y: Math.random(),
      size: Math.random() * 2 + 0.5,
      speed: Math.random() * 0.0003 + 0.0001,
      brightness: Math.random() * 0.5 + 0.3
    });
  }

  // Goal (moves left-right)
  const goal = {
    w: 0, h: 0, x: 0, y: 0,
    speed: 1.5, dir: 1,
    postW: 0,
    reset() {
      const W = viewportWidth, H = viewportHeight;
      this.w = W * 0.5;
      this.h = H * 0.085;
      this.postW = Math.max(4, W * 0.008);
      this.x = W / 2 - this.w / 2;
      this.y = H * 0.06;
      this.speed = 1.5 + level * 0.5;
    }
  };

  // Goalkeeper
  const keeper = {
    w: 0, h: 0, x: 0, y: 0,
    speed: 0, dir: 1,
    reset() {
      const W = viewportWidth, H = viewportHeight;
      this.w = Math.max(26, W * 0.055);
      this.h = Math.max(34, H * 0.07);
      this.y = goal.y + goal.h + 2;
      this.x = goal.x + goal.w / 2 - this.w / 2;
      this.speed = 1 + level * 0.4;
    }
  };

  // Ball
  const ball = {
    x: 0, y: 0, r: 0,
    vx: 0, vy: 0,
    active: false,
    reset() {
      const W = viewportWidth, H = viewportHeight;
      this.r = Math.max(13, W * 0.022);
      this.x = W / 2;
      this.y = H * 0.8;
      this.vx = 0;
      this.vy = 0;
      this.active = false;
    }
  };

  // Aiming
  let aimX = viewportWidth / 2;
  let aimDir = 1;
  let aimSpeed = 2 + level * 0.3;

  // Touch / mouse
  function handleShoot(e) {
    e.preventDefault();
    if (gameOver) {
      // Restart
      score = 0;
      lives = 5;
      level = 1;
      gameOver = false;
      ball.reset();
      goal.reset();
      keeper.reset();
      shotFired = false;
      aimSpeed = 2 + level * 0.3;
      return;
    }
    if (!shotFired && !showResult && ball.active === false) {
      shotFired = true;
      ball.active = true;
      const W = viewportWidth, H = viewportHeight;
      const targetX = aimX;
      const targetY = goal.y + goal.h / 2;
      const dx = targetX - ball.x;
      const dy = targetY - ball.y;
      const dist = Math.sqrt(dx * dx + dy * dy);
      const speed = Math.max(6, H * 0.012);
      ball.vx = (dx / dist) * speed;
      ball.vy = (dy / dist) * speed;
    }
  }

  canvas.addEventListener('click', handleShoot);
  canvas.addEventListener('touchstart', handleShoot, { passive: false });
  gameCleanup = () => {
    window.removeEventListener('resize', resizeCanvas);
    canvas.removeEventListener('click', handleShoot);
    canvas.removeEventListener('touchstart', handleShoot);
  };

  goal.reset();
  keeper.reset();
  ball.reset();

  function drawField(W, H) {
    ctx.clearRect(0, 0, W, H);
    // Dark green pitch gradient
    const grad = ctx.createLinearGradient(0, 0, 0, H);
    grad.addColorStop(0, '#0a2e0a');
    grad.addColorStop(0.5, '#0d3b0d');
    grad.addColorStop(1, '#0a2e0a');
    ctx.fillStyle = grad;
    ctx.fillRect(0, 0, W, H);

    // Retro scanlines
    ctx.fillStyle = 'rgba(0,0,0,0.08)';
    for (let i = 0; i < H; i += 3) {
      ctx.fillRect(0, i, W, 1);
    }

    // Stars
    stars.forEach(s => {
      s.y += s.speed;
      if (s.y > 1) s.y = 0;
      ctx.fillStyle = `rgba(255,255,255,${s.brightness})`;
      ctx.fillRect(s.x * W, s.y * H, s.size, s.size);
    });

    // Pitch lines
    ctx.strokeStyle = 'rgba(255,255,255,0.1)';
    ctx.lineWidth = 1;
    ctx.beginPath();
    ctx.moveTo(0, H * 0.5);
    ctx.lineTo(W, H * 0.5);
    ctx.stroke();
    ctx.beginPath();
    ctx.arc(W / 2, H * 0.5, W * 0.1, 0, Math.PI * 2);
    ctx.stroke();
  }

  function drawGoal(W, H) {
    const g = goal;
    if (drawImageContain(ctx, gameAssets.goal, g.x - g.postW * 12, g.y - g.h * 0.65, g.w + g.postW * 24, g.h * 3.2)) {
      return;
    }
    // Net
    ctx.fillStyle = 'rgba(255,255,255,0.06)';
    ctx.fillRect(g.x, g.y, g.w, g.h);
    // Net lines
    ctx.strokeStyle = 'rgba(255,255,255,0.12)';
    ctx.lineWidth = 0.5;
    for (let i = g.x; i < g.x + g.w; i += 12) {
      ctx.beginPath();
      ctx.moveTo(i, g.y);
      ctx.lineTo(i, g.y + g.h);
      ctx.stroke();
    }
    for (let j = g.y; j < g.y + g.h; j += 10) {
      ctx.beginPath();
      ctx.moveTo(g.x, j);
      ctx.lineTo(g.x + g.w, j);
      ctx.stroke();
    }
    // Posts
    ctx.fillStyle = '#ffffff';
    ctx.fillRect(g.x - g.postW, g.y, g.postW, g.h + 4);
    ctx.fillRect(g.x + g.w, g.y, g.postW, g.h + 4);
    // Crossbar
    ctx.fillRect(g.x - g.postW, g.y - 3, g.w + g.postW * 2, 4);
  }

  function drawKeeper(W, H) {
    const k = keeper;
    let sprite = gameAssets.keeper.low;
    if (keeperReaction === 'miss') {
      sprite = gameAssets.keeper.miss;
    } else if (keeperReaction === 'goal') {
      sprite = gameAssets.keeper.goal;
    } else if (keeperReaction === 'save') {
      sprite = gameAssets.keeper.save;
    }
    if (drawImageContain(ctx, sprite, k.x - k.w * 1.7, k.y - k.h * 1.6, k.w * 3.8, k.h * 3.6)) {
      return;
    }
    // Body
    ctx.fillStyle = '#e87a3a';
    ctx.fillRect(k.x, k.y, k.w, k.h);
    // Head
    const headR = k.w * 0.35;
    ctx.beginPath();
    ctx.arc(k.x + k.w / 2, k.y - headR * 0.5, headR, 0, Math.PI * 2);
    ctx.fillStyle = '#f5c89a';
    ctx.fill();
    // Arms
    ctx.strokeStyle = '#e87a3a';
    ctx.lineWidth = Math.max(3, k.w * 0.15);
    ctx.lineCap = 'round';
    ctx.beginPath();
    ctx.moveTo(k.x, k.y + k.h * 0.2);
    ctx.lineTo(k.x - k.w * 0.5, k.y - k.h * 0.1);
    ctx.stroke();
    ctx.beginPath();
    ctx.moveTo(k.x + k.w, k.y + k.h * 0.2);
    ctx.lineTo(k.x + k.w + k.w * 0.5, k.y - k.h * 0.1);
    ctx.stroke();
    // Gloves
    ctx.fillStyle = '#22c55e';
    ctx.beginPath();
    ctx.arc(k.x - k.w * 0.5, k.y - k.h * 0.1, k.w * 0.2, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(k.x + k.w + k.w * 0.5, k.y - k.h * 0.1, k.w * 0.2, 0, Math.PI * 2);
    ctx.fill();
  }

  function drawBall(W, H) {
    const b = ball;
    const sprite = gameAssets.ball.idle;
    if (drawImageContain(ctx, sprite, b.x - b.r * 1.35, b.y - b.r * 1.35, b.r * 2.7, b.r * 2.7)) {
      return;
    }
    ctx.beginPath();
    ctx.arc(b.x, b.y, b.r, 0, Math.PI * 2);
    ctx.fillStyle = '#fff';
    ctx.fill();
    ctx.strokeStyle = '#333';
    ctx.lineWidth = 1.5;
    ctx.stroke();
    // Pentagon pattern
    ctx.fillStyle = '#333';
    ctx.beginPath();
    ctx.arc(b.x, b.y, b.r * 0.4, 0, Math.PI * 2);
    ctx.fill();
  }

  function drawAim(W, H) {
    if (shotFired || showResult || gameOver) return;
    // Crosshair at aim position
    ctx.strokeStyle = 'rgba(232, 122, 58, 0.8)';
    ctx.lineWidth = 2;
    const sz = 12;
    const ay = goal.y + goal.h / 2;
    ctx.beginPath();
    ctx.moveTo(aimX - sz, ay);
    ctx.lineTo(aimX + sz, ay);
    ctx.stroke();
    ctx.beginPath();
    ctx.moveTo(aimX, ay - sz);
    ctx.lineTo(aimX, ay + sz);
    ctx.stroke();
    ctx.beginPath();
    ctx.arc(aimX, ay, sz * 0.8, 0, Math.PI * 2);
    ctx.stroke();
    // Dotted line from ball to aim
    ctx.setLineDash([4, 4]);
    ctx.strokeStyle = 'rgba(232, 122, 58, 0.3)';
    ctx.beginPath();
    ctx.moveTo(ball.x, ball.y);
    ctx.lineTo(aimX, ay);
    ctx.stroke();
    ctx.setLineDash([]);
  }

  function drawHUD(W, H) {
    const fontSize = Math.max(14, W * 0.025);
    ctx.font = `bold ${fontSize}px "Clash Display", sans-serif`;
    ctx.textAlign = 'left';
    ctx.fillStyle = '#e87a3a';
    ctx.fillText(`ГОЛЫ: ${score}`, 16, fontSize + 10);
    ctx.textAlign = 'right';
    ctx.fillStyle = '#ffffff';
    ctx.fillText('⚽'.repeat(lives), W - 16, fontSize + 10);
    ctx.textAlign = 'center';
    ctx.fillStyle = 'rgba(255,255,255,0.4)';
    const smallFont = Math.max(11, W * 0.017);
    ctx.font = `${smallFont}px "General Sans", sans-serif`;
    ctx.fillText(`Уровень ${level} · Рекорд: ${highScore}`, W / 2, fontSize + 10);
  }

  function drawMessage(W, H, text, sub) {
    ctx.fillStyle = 'rgba(0,0,0,0.5)';
    ctx.fillRect(0, H * 0.35, W, H * 0.3);
    const fontSize = Math.max(20, W * 0.045);
    ctx.font = `bold ${fontSize}px "Clash Display", sans-serif`;
    ctx.textAlign = 'center';
    ctx.fillStyle = '#e87a3a';
    ctx.fillText(text, W / 2, H * 0.48);
    if (sub) {
      const subFont = Math.max(13, W * 0.022);
      ctx.font = `${subFont}px "General Sans", sans-serif`;
      ctx.fillStyle = 'rgba(255,255,255,0.6)';
      ctx.fillText(sub, W / 2, H * 0.55);
    }
  }

  function drawStartScreen(W, H) {
    drawField(W, H);
    drawGoal(W, H);
    drawKeeper(W, H);
    drawBall(W, H);
    drawHUD(W, H);
    drawAim(W, H);
    const fontSize = Math.max(14, W * 0.022);
    ctx.font = `${fontSize}px "General Sans", sans-serif`;
    ctx.textAlign = 'center';
    ctx.fillStyle = 'rgba(255,255,255,0.5)';
    ctx.fillText('Нажмите чтобы ударить по воротам', W / 2, H * 0.92);
  }

  function checkCollision() {
    const b = ball;
    const g = goal;
    const k = keeper;

    // Ball reached goal area
    if (b.y - b.r <= g.y + g.h) {
      // Check if ball is within goal posts
      if (b.x > g.x && b.x < g.x + g.w) {
        // Check if keeper catches it
        if (b.x > k.x - k.w * 0.5 && b.x < k.x + k.w + k.w * 0.5 &&
            b.y > k.y - k.h * 0.3 && b.y < k.y + k.h) {
          // Saved!
          resultText = 'ОТБИТО!';
          keeperReaction = 'save';
          lives--;
        } else {
          // GOAL!
          resultText = 'ГОООЛ!!!';
          keeperReaction = 'goal';
          score++;
          if (score > highScore) {
            highScore = score;
            localStorage.setItem('kubokGameHigh', highScore.toString());
          }
          if (score % 3 === 0) level++;
        }
      } else {
        // Missed the goal entirely
        resultText = 'МИМО!';
        keeperReaction = 'miss';
        lives--;
      }
      b.active = false;
      showResult = true;
      resultTimer = 60;
      return true;
    }
    // Ball went off screen
    if (b.y < -20 || b.x < -20 || b.x > viewportWidth + 20) {
      resultText = 'МИМО!';
      keeperReaction = 'miss';
      lives--;
      b.active = false;
      showResult = true;
      resultTimer = 60;
      return true;
    }
    return false;
  }

  function gameLoop() {
    if (!gameActive) return;
    const W = viewportWidth;
    const H = viewportHeight;

    // Recalc sizes on every frame (handles resize)
    goal.w = W * 0.35;
    goal.h = H * 0.085;
    goal.postW = Math.max(4, W * 0.008);
    goal.w = W * 0.5;
    goal.y = H * 0.06;
    keeper.w = Math.max(26, W * 0.055);
    keeper.h = Math.max(34, H * 0.07);
    keeper.y = goal.y + goal.h + 2;
    ball.r = Math.max(13, W * 0.022);

    // Draw field
    drawField(W, H);

    if (gameOver) {
      drawGoal(W, H);
      drawMessage(W, H, `ИГРА ОКОНЧЕНА · ${score} голов`, 'Нажмите чтобы начать заново');
      drawHUD(W, H);
      gameRAF = requestAnimationFrame(gameLoop);
      return;
    }

    // Move goal
    goal.x += goal.speed * goal.dir;
    if (goal.x + goal.w > W - 20) goal.dir = -1;
    if (goal.x < 20) goal.dir = 1;

    // Move keeper (slightly offset from goal center)
    const goalCenterX = goal.x + goal.w / 2;
    const keeperTarget = goalCenterX - keeper.w / 2 + Math.sin(Date.now() / 400) * goal.w * 0.3;
    keeper.x += (keeperTarget - keeper.x) * 0.05;

    // Move aim crosshair
    if (!shotFired && !showResult) {
      aimSpeed = 2 + level * 0.4;
      aimX += aimSpeed * aimDir;
      if (aimX > W - 30) aimDir = -1;
      if (aimX < 30) aimDir = 1;
      keeperReaction = '';
    }

    // Move ball
    if (ball.active) {
      ball.x += ball.vx;
      ball.y += ball.vy;
      // Shrink ball as it goes up (perspective)
      const progress = 1 - (ball.y / (H * 0.82));
      ball.r = Math.max(4, W * 0.015 * (1 - progress * 0.5));
      checkCollision();
    }

    // Result display
    if (showResult) {
      resultTimer--;
      if (resultTimer <= 0) {
        showResult = false;
        shotFired = false;
        keeperReaction = '';
        if (lives <= 0) {
          gameOver = true;
        } else {
          ball.reset();
          ball.x = W / 2;
          ball.y = H * 0.8;
        }
      }
    }

    // Draw everything
    drawGoal(W, H);
    drawKeeper(W, H);
    drawBall(W, H);
    drawAim(W, H);
    drawHUD(W, H);

    if (showResult) {
      const isGoal = resultText.includes('ГО');
      const col = isGoal ? '#22c55e' : '#ef4444';
      const fontSize = Math.max(24, W * 0.06);
      ctx.font = `bold ${fontSize}px "Clash Display", sans-serif`;
      ctx.textAlign = 'center';
      ctx.fillStyle = col;
      ctx.fillText(resultText, W / 2, H * 0.5);
    }

    if (!shotFired && !showResult && !gameOver) {
      const fontSize = Math.max(12, W * 0.018);
      ctx.font = `${fontSize}px "General Sans", sans-serif`;
      ctx.textAlign = 'center';
      ctx.fillStyle = 'rgba(255,255,255,0.4)';
      ctx.fillText('Нажмите чтобы ударить', W / 2, H * 0.93);
    }

    gameRAF = requestAnimationFrame(gameLoop);
  }

  gameLoop();
}
</script>

<!-- Game Overlay -->
<div id="gameOverlay" style="display:none; position:fixed; inset:0; z-index:10000; background:#0a1628; flex-direction:column; align-items:center; justify-content:center;">
  <button onclick="closeMiniGame()" style="position:absolute; right:14px; bottom:14px; z-index:10001; background:rgba(180,20,20,0.92); border:1px solid rgba(255,255,255,0.18); color:#fff; font-size:0.95rem; padding:0.45rem 0.85rem; border-radius:999px; cursor:pointer; font-family:'General Sans',sans-serif; box-shadow:0 8px 24px rgba(0,0,0,0.35);">Выйти</button>
  <canvas id="gameCanvas" style="width:100%; height:100%; display:block; touch-action:none;"></canvas>
</div>

</body>
</html>
