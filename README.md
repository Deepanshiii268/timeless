# timeless
# 🕰️ TIMELESS — Pinterest Aesthetic Digital & Analog Clock Dashboard

[![License: MIT](https://img.shields.io/badge/License-MIT-A8B5A2.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Vanilla JS](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-0-D8A7A7?style=for-the-badge)](#)

> A cozy, editorial, Pinterest-inspired digital and analog clock dashboard. Built ground-up with semantic HTML5, pure CSS3, and vanilla JavaScript—combining soft glassmorphic depth, physical dial mechanics, and fluid responsive design without a single external library or framework.

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Design Philosophy & Aesthetic Direction](#-design-philosophy--aesthetic-direction)
- [Color Palette & Tokens](#-color-palette--tokens)
- [Core Features](#-core-features)
- [Mathematics & Physics Behind the Hands](#-mathematics--physics-behind-the-hands)
  - [Second Hand Formula](#second-hand-formula)
  - [Minute Hand Continuous Drift](#minute-hand-continuous-drift)
  - [Hour Hand Multi-Tier Drift](#hour-hand-multi-tier-drift)
  - [The 360-Degree Rollover Glitch Solution](#the-360-degree-rollover-glitch-solution)
- [Directory Architecture](#-directory-architecture)
- [Getting Started & Installation](#-getting-started--installation)
- [Code Deep Dive & Engineering Highlights](#-code-deep-dive--engineering-highlights)
  - [Neumorphic & Glassmorphic Elevation](#neumorphic--glassmorphic-elevation)
  - [Defensive DOM Architecture](#defensive-dom-architecture)
  - [Accessibility (a11y) Consideration](#accessibility-a11y-consideration)
- [Customization Guide](#-customization-guide)
  - [Switching to 24-Hour Military Format](#1-switching-to-24-hour-military-format)
  - [Switching Color Schemes](#2-switching-color-schemes)
  - [Enabling Smooth Continuous Sweeping Hands](#3-enabling-smooth-continuous-sweeping-hands)
- [Browser Compatibility](#-browser-compatibility)
- [Roadmap & Enhancements](#-roadmap--enhancements)
- [Author & Acknowledgments](#-author--acknowledgments)
- [License](#-license)

---

## 🌿 Overview

Most beginner-to-intermediate JavaScript clock tutorials produce raw, developer-centric interfaces: high-contrast dark modes, flat borders, or rigid monospaced digital timers. 

**Timeless** was created to demonstrate how basic web technologies (`HTML/CSS/JS`) can produce a **high-end, editorial user interface**. Taking direct cues from Japanese interior decor, Scandinavian minimalism, and Pinterest cozy dashboard boards, this project marries functional real-time timekeeping with elevated UI craftsmanship.

---

## 🎨 Design Philosophy & Aesthetic Direction

The design bridges two modern CSS rendering patterns:
1. **Glassmorphism**: Translucent card layering, background blur filters (`backdrop-filter: blur(14px)`), and semi-transparent white border highlights simulating real glass edges.
2. **Soft Neumorphism**: Multi-stop positive and negative drop shadows that simulate an ambient light source shining from the top-left corner, giving elements an extruded, organic feel rather than a flat digital presence.

Ambient background shapes float with varying timing delays (`12s`, `14s`, `16s`) across non-linear paths, creating an interface that feels alive without distracting from the time display.

---

## 🪞 Color Palette & Tokens

All core styles utilize strict CSS custom properties for uniform theming:

```css
:root {
  --warm-cream:  #F8F3EA; /* Root page canvas */
  --soft-beige:  #EDE3D2; /* Analog face radial highlight */
  --dusty-rose:  #D8A7A7; /* Second hand & visual focal points */
  --muted-sage:  #A8B5A2; /* Badges, secondary accents, star icons */
  --deep-brown:  #4A3F35; /* Primary headings, hour hand, marker pins */
  --soft-white:  #FFFDF8; /* Glass card fill & rim illumination */
  --muted-gray:  #8F8275; /* Subtitles, minute hand, secondary data */
}
