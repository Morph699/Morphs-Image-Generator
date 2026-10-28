<img width="1280" height="1920" alt="1793188189117-01a18257-a80d-75ce-8a2d-2d77bb83de65" src="https://github.com/user-attachments/assets/ff32a7b2-5220-4832-9e53-6f456051ea85" />

# Morphs Image Gen 

The **Morphs Image Generator** is a lightweight, ultra-responsive digital creation suite designed for artists, designers, and content creators. Powered by a flexible multi-engine neural pipeline, it delivers instantaneous concept rendering, photo re-imagining, die-cut vector sticker styling, and complete meme typography directly on your device with zero cloud lock-in.

With the **update**, Morphs Image Gen integrates a dedicated **Personal API Key Engine**, allowing creators to hook directly into Pollinations VIP infrastructure to bypass public IP concurrency bottlenecks and rate-limit cooldowns entirely.

### What’s New in v4.5

* **🔑 Personal API Key Sentry:**  
  Direct integration with `enter.pollinations.ai` credentials (`pk_...` / `sk_...`). The application dynamically injects keys as query tokens and bearer headers, bypassing public 45-second IP cooldowns and priority throttling.
* **⚡ Live Header Key Status:**  
  A recalibrated, space-efficient header houses the new `🔑 API Key` trigger (which dynamically lights up as `🔑 Key ✓` in neon green once authenticated).
* **🛡️ 16×16 Pixel Yellow Rate-Limit Interceptor:**  
  An automated raster guard samples incoming image buffers at runtime. If a public rate-limit banner is detected (yellow matrix saturation $\ge 60\%$), the buffer is automatically diverted and re-routed across backup engine nodes rather than rendering an error graphic.
* **📐 Streamlined Compact Header:**  
  The 10-theme selector has been compacted down to 185px, neatly aligning the API Key manager, font scaler, and Pro status drawer without UI crowding.

### Core Studio Capabilities

#### 1. Multi-Engine Neural Core
Switch dynamically between discrete diffusion pipelines tailored for specific aesthetic styles:
* **Turbo Diffusion:** 2-second ultra-fast iteration engine.
* **FLUX.1 Schnell & FLUX.2 Klein:** High-fidelity photorealism and quick contextual passes.
* **FLUX Kontext:** Dedicated reference-guided transformation pipeline.
* **Aesthetic Modes:** Anime/Manga Cell-Shaded, FLUX 3D Octane Render, and Midjourney Masterwork emulation.

#### 2. Img2Img Reference Studio
* **Drag-and-Drop Ingestion:** Drop local photos (`.png`, `.jpg`, `.jpeg`, `.webp`) straight onto the studio dock.
* **Subject-Preserving Context Injection:** Automatically scans image filenames to isolate subjects and injects structured context wrappers (`[Reimagine, transform and stylize reference subject ({subject})]: {prompt}`), preserving the core silhouette while transforming the environment.

#### 3. AI Meme Canvas & Die-Cut Sticker Studio
* **Auto-Fitted Typography:** Draw classic meme captions (Impact, Arial Black, Comic Sans, Trebuchet, etc.) dynamically rendered with balanced black outline strokes. Text automatically calculates line length and downscales to eliminate boundary clipping.
* **Color Customization:** Switch between High-Contrast White, Cyber Yellow, Cyan, Hot Pink, Gold, and Neon Green captions.
* **Die-Cut Sticker Maker:** One-click sticker filter injecting bold white contour outlines and isolated contrast backgrounds ready for icon clipping.

#### 4. Master Resolution & Frame Scaling
* **Flexible Aspect Ratios:** 1:1 (Square), 9:16 (Mobile Story/Reel), 4:3 (Classic Display), 16:9 (Widescreen HD), and 21:9 (Ultrawide Cinema).
* **Multi-Tier Quality Engine:** SD Base, 1080p Full HD, 2K QHD, 4K UHD, and 8K Cinema Master with hardware bicubic GDI+ resampling.

#### 5. AI Arena Dual-Model Comparison (Pro Premium)
* Pits two disparate diffusion engines against each other using an identical seed.
* Executes passes with an automated 2.6-second inter-request cooldown to protect pipeline throughput.
* Automatically stitches both results vertically into an ultrawide/stacked comparison board separated by a `#38BDF8` divider, replicating meme captions across both frames simultaneously.

#### 6. Anti-Watermark Inpainting Engine
* Real-time clean recreation engine. Automatically samples an unblemished 6px horizontal strip directly above the bottom-right branding zone (26% width $\times$ 7.5% height) and bicubically interpolates it across the watermark boundary for clean visual exports.

### Ergonomics, Layout & Persistence

* **10 High-Contrast Themes (WCAG AAA):** Soft Slate (Light Default), Dark Stealth (OLED), Matrix Green, Cyber Yellow, Cyberpunk Pink, Dracula Purple (Pro Exclusive), Blood Matrix, Nordic Frost, Solarized Ocean, and Sunset Amber.
* **Dynamic Typography Scaling:** Small (8pt), Medium (9pt Free Default), Large (11pt Standard+), and Extra Large (12.5pt Pro).
* **Dual-Path Settings Persistence:** Retains your API key, preferred model, theme, font scaling, aspect ratio, window location, and splitter layout in portable mode (`Engineimagegen\settings_paid.json`) with automated failover to `%LOCALAPPDATA%` and the Windows Registry.
* **Export Utilities:** Instant Windows Clipboard copying, single-click PNG/JPG saving, and session logging with deep JSON/CSV telemetry exports.

### Tier Licensing Matrix

| Feature / Quota | Free Edition | Supporter Tier (`'D'`) | Standard Tier (`'S'`) | Pro Premium Tier (`'P'`) |
| : | :: | :: | :: | :: |
| **Generations** | 5 Passes | 5 Passes | 10 Passes | **Unlimited (9,999+)** |
| **Max Resolution** | 1080p HD | 1080p HD | 2K QHD Studio | **4K UHD & 8K Master** |
| **Aspect Ratios** | 1:1, 9:16, 4:3 | 1:1, 9:16, 4:3 | + 16:9 Widescreen | **+ 21:9 Ultrawide Cinema** |
| **AI Models** | Turbo, Schnell, Kontext | Turbo, Schnell, Kontext | + FLUX Realism / Anime | **+ FLUX 3D & Midjourney** |
| **AI Arena Mode** | ✕ | ✕ | ✕ | **✓ Dual Engine Compare** |
| **API Key Bypass** | ✓ Supported | ✓ Supported | ✓ Supported | **✓ Supported** |
| **Themes** | Slate, Stealth | + Matrix Green | + Cyber Yellow / Pink | **All 10 Themes Unlocked** |
| **Log Exports** | Clipboard / View | Clipboard / View | Clipboard / View | **Deep JSON & CSV Logs** |
