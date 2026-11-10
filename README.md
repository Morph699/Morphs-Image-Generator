<img width="1280" height="1920" alt="1793188189117-01a18257-a80d-75ce-8a2d-2d77bb83de65" src="https://github.com/user-attachments/assets/ff32a7b2-5220-4832-9e53-6f456051ea85" />

# Morphs Image Generator — Architectural & Feature Specification

**Morphs Image Generator** is a cross-platform visual synthesis suite and neural rendering workstation engineered for Windows Desktop (PowerShell WinForms / compiled standalone binary) and Mobile/Web environments (Android WebView, PWA, and local container runtimes). 

Designed with an air-gapped UI philosophy, zero external dependencies, and resilient stream failover pipelines, the application delivers end-to-end generative workflows from prompt creation to ultra-high-resolution canvas post-processing.

---

### 1. Neural Generation Core & Multi-Engine Matrix
* **Multi-Engine Pipeline:** Integrates multiple neural diffusion backends, including Turbo Diffusion (instant 2s iterations), FLUX.1 Schnell, FLUX Kontext, FLUX.2 Klein, FLUX Realism, FLUX Anime, FLUX 3D Render, and Midjourney Master emulation.
* **Autonomous Stream Failover:** Multi-tier fallback routing chain automatically redirects interrupted generation requests to backup endpoints, preventing dropped passes or frozen worker threads.
* **Custom API Key Sentry:** Top-level persistent API Key HUD pill allows direct integration of custom Pollinations credentials (`pk_...` / `sk_...`), bypassing public IP pacing queues and unlocking rapid, unthrottled generation streams.

---

### 2. Multi-Ratio Geometry & Ultra-Resolution Resampling
* **Aspect Ratio Engine:** Real-time geometric clamping supporting standard and widescreen form factors:
  * `1:1` Square Studio (up to 8192×8192)
  * `9:16` Vertical Portrait & Story Formats (up to 4320×7680)
  * `4:3` Legacy / Monitor Viewports (up to 5760×4320)
  * `16:9` Cinematic Widescreen HD (up to 7680×4320)
  * `21:9` Ultrawide Panavision Cinema (up to 6880×2880)
* **High-Precision Resampling:** Built-in GDI+ / HTML5 canvas bicubic upscaling engine capable of generating crisp 2K QHD, 4K UHD, and 8K Cinema Master renders without artifacts or pixelization.
* **Optional Payload Compression:** Toggleable frame compression dynamically downsamples high-density canvas buffers for low-bandwidth mobile operations.

---

### 3. Contextual Img2Img & Smart Subject Ingestion
* **Intelligent Camera Snapshot Parsing:** Ingestion driver detects generic device capture prefixes (`IMG_`, `PXL_`, `DSC_`, `Screenshot_`) and prompts the user for a semantic subject descriptor, ensuring the neural engine understands the core focus of the image.
* **Prompt Harmonization:** Automatically wraps user instructions into structured image-to-image prompts: `[Reimagine, transform and stylize reference subject ({subject})]: {prompt}` to preserve subject contours while executing stylistic overhauls.

---

### 4. Creative Studios & Aesthetic Customization
* **AI Era / Style Transformation:** One-click contextual filter engine injecting specialized lighting, medium, and aesthetic tokens:
  * *Anime / Manga Cell-Shaded* (Clean line art and vibrant cel fills)
  * *1920s Daguerreotype* (Vintage monochrome grain and historic optics)
  * *Claymation Stop-Motion* (Tactile plasticine textures and miniature depth)
  * *80s Retro Synthwave* (Outrun neon gridlines and CRT glow)
  * *Dark Medieval Oil* (Chiaroscuro lighting and Rembrandt-style oil textures)
  * *Dark Knight Cinematic* (IMAX noir, dynamic rain reflections, and grit)
  * *Hyper Cyberpunk Metropolis* (Volumetric neon haze and futuristic architecture)
* **Die-Cut Sticker Studio:** Automatically isolates subjects against dark backdrops and calculates high-contrast vector white perimeter borders for physical decal generation.
* **Integrated Meme Canvas Studio:** In-engine typographic compositor featuring dynamic auto-fitting, multi-font support (Impact, Arial Black, Consolas, Georgia, Comic Sans), stroke-path outline rendering, and selectable neon accent colors.

---

### 5. Dual-Engine AI Arena Mode
* **Comparative Neural Staging:** Executes dual disparate models concurrently (e.g., *FLUX Realism* vs. *Midjourney Master*) using independent randomized seeds and automated inter-request cooldown pacing.
* **Automated Canvas Compositing:** Stitches both passes vertically onto a cohesive unified viewport divided by a 12px accent divider bar, replicating overlay captions across both viewports for direct side-by-side output evaluation.

---

### 6. Hardware Shielding & Artifact Elimination
* **Bicubic Anti-Watermark Inpainting Engine:** Post-process inspection module isolates the lower-right branding footprint (26% canvas width × 7.5% canvas height), samples a clean 6px slice directly above it, and redraws the buffer to eliminate corner watermarks and branding artifacts without external editors.
* **Rate-Limit Banner Interceptor:** Actively samples a 16×16 pixel matrix from incoming image streams. If yellow warning banner saturation exceeds 60%, the corrupt buffer is automatically discarded and an automatic cooldown sequence is triggered to keep the primary view unblemished.

---

### 7. Dual-Platform Runtime Ergonomics
* **Windows Desktop (WinForms / Compiled Binary):**
  * Console suppression on launch with high-DPI awareness (`SetProcessDpiAwareness(2)`).
  * Gothic sinusoidal breathing splash screen with in-memory PrivateFontCollection loading (`AmericanText.ttf` / fallback `Old English Text MT`).
  * Dual-path settings persistence surviving write-protected directories (`settings_paid.json` failover to `%LOCALAPPDATA%` and Registry).
  * Direct Windows Clipboard integration for instant image and log copying, paired with deep JSON and CSV log exports.
* **Android & Web Container Edition (HTML5 / PWA):**
  * **Zero Page-Reload Architecture:** Hot-reset workflows operate entirely within volatile RAM, completely eliminating white-screen stalls, route disconnects, and WebView container crashes.
  * **Universal Downloader Engine:** 4-tier download cascade utilizing Native Web Share, an ephemeral HTTPS bridge, direct Object URL anchors, and long-press gallery anchors to prevent `IllegalArgumentException` URI crashes on mobile wrappers.
  * **Network Radar Sentry:** Real-time connection supervisor adjusting image delivery dimensions based on Wi-Fi, cellular, or battery-saver telemetry.
* **Visual Palette & Typography Matrix:** Complete 10-theme high-contrast WCAG AAA engine (Soft Slate, Dark Stealth, Matrix Green, Cyber Yellow, Cyberpunk Pink, Dracula Purple, Blood Matrix, Nordic Frost, Solarized Ocean, Sunset Amber) paired with dynamic font scaling (Small, Medium, Large, Extra Large).
