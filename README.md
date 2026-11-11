# AE Message Bubble Generator (v1.0)

[![Live Browser Simulator](https://img.shields.io/badge/Live%20Demo-AE%20ScriptUI%20Simulator-2c8cff?style=for-the-badge&logo=javascript)](https://work2survive.github.io/AE_JS_builder/?jsx=message_bubble.jsx)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Adobe After Effects](https://img.shields.io/badge/Adobe%20After%20Effects-CS6%20--%20CC%202026%2B-9999FF?style=for-the-badge&logo=adobeaftereffects)](https://www.adobe.com/products/aftereffects.html)
[![Built with Antigravity](https://img.shields.io/badge/Built%20With-Antigravity-4285F4?style=for-the-badge&logo=google)](https://deepmind.google/)

**Live Demo**: [https://work2survive.github.io/AE_JS_builder/?jsx=message_bubble.jsx](https://work2survive.github.io/AE_JS_builder/?jsx=message_bubble.jsx)

A powerful, expression-rigged Adobe After Effects ScriptUI panel for generating authentic, animated chat and text message bubbles imitating modern messaging platforms (**iOS Messages**, **Android RCS**, **WhatsApp**, **Instagram Direct**, **Facebook Messenger**, and **Custom** themes).

> **Live Browser Simulator**: Test and preview this tool interactively in the [AE JS & ScriptUI Simulator](https://work2survive.github.io/AE_JS_builder/?jsx=message_bubble.jsx) directly in your browser without launching After Effects!

---

## ✨ Features

### 1. Platform Presets & Color Themes
- **iOS Messages**: Apple iMessage signature blue `#007AFF` sent bubbles, neutral `#E9E9EB` received bubbles, and dark mode variants.
- **Android RCS**: Google Messages Material You pastel blue `#C2E7FF` / `#2B4459` styling with circled checkmarks.
- **WhatsApp**: Classic WhatsApp green `#D9FDD3` / `#005C4B` sent bubbles and clean white/dark gray received cards.
- **Instagram Direct**: Signature vibrant violet/purple `#8134AF` / `#3797F0` capsules.
- **Facebook Messenger**: Electric Messenger blue `#0084FF` and soft gray cards.
- **Custom Style**: Direct hex inputs and color pickers for custom branding.
- **Light & Dark Themes**: One-click switching with platform-accurate palette adaptation.

### 2. Message Types & Bubble Tail Control
- **Sent (Right)**: Right-aligned message bubble with bottom-right directional pointer.
- **Received (Left)**: Left-aligned message bubble with bottom-left directional pointer.
- **Bubble Tail Toggle**: Easily hide the pointer/tail (`Show Tail / Pointer` checkbox) for chained multi-message conversations.

### 3. Delivery Status Icons & Timing Simulation
- **Two Icon Styles**:
  - **RCS Circled Checks**: Single circle outline for Sent (`○✓`), double overlapping circles for Delivered (`○○✓✓`), and solid filled circles with inverted checkmarks for Read (`●●✓✓`).
  - **Standard Checks**: Classic single checkmark (`✓`) and double checkmarks (`✓✓`) transitioning to read receipt blue.
- **Timing Simulation (`Auto` Mode)**:
  - Dynamically calculates reading duration based on character count and word density (`0.8s + readingDuration`).
  - Animates status transitions from Sent $\rightarrow$ Delivered $\rightarrow$ Read with a celebratory micro-interaction pop.
- **Intelligent Default**: Automatically sets status icon to `None` when switching to Received messages.

### 4. Layout & Typography Engine
- **Font Family Selector**: Quickly switch between mobile system typefaces:
  - `SF Pro` (Apple / iOS)
  - `Roboto` (Google / Android)
  - `Segoe UI` (Windows / Messenger)
  - `Helvetica Neue` (WhatsApp)
  - `Arial`, `Inter`, `Open Sans`, `System Default`
- **Responsive Screen Width**: Slider from $300\text{ to }1920\text{ px}$ (default: $420\text{ px}$) driving automatic word wrapping so lines split naturally within realistic mobile phone widths.
- **Text Size**: Slider from $12\text{ to }60\text{ px}$.
- **Inner Padding**: Slider from $-10\text{ to }+10\text{ px}$ for compact or spacious layouts.
- **Leading / Line Height**: Slider from $50\%\text{ to }150\%$ (default: $100\%$) for fine typography control.

### 5. Entrance & Text Animation
- **Bubble Grow Duration**: Slider from $0\text{ to }20\text{ frames}$ (default: $5$). The bubble expands outward from its tail corner with a snappy overshoot bounce (`easeOutBack`). Set to $0$ for instant appearance.
- **Typewriter Reveal Duration**: Slider from $0\text{ to }20\text{ frames}$ (default: $5$). Text appears character-by-character immediately after the bubble expands.
- **Fade-in Timestamp**: Timestamps and status icons smoothly fade in upon typewriter completion.
- **iOS 18 Animated Text Effects**: 8 continuous loop effects:
  - **Big** (Enlarge Pulse)
  - **Small** (Contract Scale)
  - **Shake** (Horizontal Wobble)
  - **Nod** (Vertical Bobbing)
  - **Explode** (Burst & Decay)
  - **Ripple** (Wave Float)
  - **Bloom** (Radiant Glow)
  - **Jitter** (Chaotic Glitch)
  - Speed ($50\%\text{--}200\%$) and Intensity ($20\%\text{--}200\%$) sliders.

### 6. Procedural Rigging in After Effects
- **Native Shape Layers**: Built with After Effects vector Bézier shapes—sharp at any resolution, no raster pixelation.
- **Master Controller**: Creates `Bubble_Master_Controller` with intuitive Slider, Color, and Checkbox Effect Controls allowing full post-generation keyframing and Essential Graphics / MOGRT export.

---

## 🚀 Installation

### Option 1: Dockable ScriptUI Panel (Recommended)
1. Download or clone this repository.
2. Copy `Message_Bubble_Generator.jsx` into your After Effects `ScriptUI Panels` directory:
   - **Windows**:
     ```text
     C:\Program Files\Adobe\Adobe After Effects <Version>\Support Files\Scripts\ScriptUI Panels\
     ```
   - **macOS**:
     ```text
     /Applications/Adobe After Effects <Version>/Scripts/ScriptUI Panels/
     ```
3. Restart After Effects (if open).
4. Launch the panel from the top menu: **Window > Message_Bubble_Generator.jsx**.

### Option 2: Run Without Installing
1. In After Effects, navigate to **File > Scripts > Run Script File...**
2. Select `Message_Bubble_Generator.jsx` (or `message_bubble.jsx`).

---

## 🛠️ Usage

1. Open or select an active composition in After Effects.
2. Open the **Message Bubble Generator** panel.
3. Type or paste your message (up to 250 characters; emojis supported).
4. Select your **Style Preset** (iOS, Android RCS, WhatsApp, Instagram, Messenger, or Custom).
5. Choose **Message Type** (`Sent` or `Received`) and **Color Theme** (`Light` or `Dark`).
6. Navigate between tabs:
   - **Appearance Tab**:
     - *Layout & Typography*: Font family, screen width, text size, inner padding, and leading.
     - *Colors & Appearance*: Bubble and text color pickers.
     - *Status & Timestamp*: Icon style (RCS vs Standard), status mode (Auto/Read/Delivered/Sent/None), and randomized time re-roller.
   - **Animation Tab**:
     - *Text Effects & Animation*: Select an iOS 18 animated effect, set speed & intensity, enable entrance animations, and dial in the exact Bubble Grow and Typewriter frame durations ($0\text{--}20\text{ frames}$).
7. Click **Create Message Bubble**.
8. A complete, rigged layer group is automatically generated in your composition!

---

## 📁 Repository Structure

```
AE_message_bubble/
├── Message_Bubble_Generator.jsx   # Primary ScriptUI panel for After Effects
├── message_bubble.jsx             # Alias for compatibility with web simulator
├── README.md                      # Documentation & user guide
├── LICENSE                        # MIT License
└── .gitignore                     # Git ignore rules
```

---

## 🔗 Related Projects

- **[AE JS & ScriptUI Simulator](https://github.com/work2survive/AE_JS_builder)**: Agnostic browser-based emulator for developing and testing After Effects ScriptUI panels and 2D/3D shape layers.
- **[AE Pie Slice Tool](https://github.com/work2survive/AE-Pie-Slice-Tool)**: Procedural circular sectors, arcs, and pie slices for After Effects.
- **[AECustomRoundedRect](https://github.com/work2survive/AECustomRoundedRect)**: Independent 4-corner rounded rectangle generator for After Effects.

---

---

## 🤖 Acknowledgments

Engineered, architected, and co-developed using **[Google DeepMind Antigravity](https://deepmind.google/)** agentic coding assistant.

## 📄 License

This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details.