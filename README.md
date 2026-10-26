# Canon Picture Styles & 3D LUTs Library (.pf2 & .pf3)

[![Canon](https://img.shields.io/badge/Canon-EOS%20M%20%7C%20EOS%20R%20%7C%20DSLR-red.svg)](https://canon.com)
[![Presets](https://img.shields.io/badge/Presets-550%20Profiles-blue.svg)](.)
[![Formats](https://img.shields.io/badge/Formats-.pf2%20%7C%20.pf3%20%7C%20.bin%20%7C%20Hald%20PNG-success.svg)](.)
[![Live Demo](https://img.shields.io/badge/Demo-Interactive%20Web%20Catalog-brightgreen.svg)](https://mercurydcd.github.io/canon-picture-styles-pf3-catalog/)
[![Technical Catalog](https://img.shields.io/badge/Documentation-Sources%20%26%20History-purple.svg)](CATALOG_SOURCES_AND_HISTORY.md)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-Support%20Project-FF5E5B?logo=ko-fi&logoColor=white)](https://ko-fi.com/dcorral)
[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-GitHub-EA4AAA?logo=github-sponsors&logoColor=white)](https://github.com/sponsors/MercuryDCD)
[![License](https://img.shields.io/badge/License-Community%20%2F%20Free-orange.svg)](LICENSE)

A comprehensively curated, categorized, and standardized collection of **550 Picture Styles (`.pf2` & `.pf3`) and 3D LUTs** for Canon EOS cameras, Digital Photo Professional (DPP 4), and post-production workflows.

This library consolidates community classics, discontinued Canon styles, iconic analog film simulations (**Fujifilm**, **Kodak**, **Ilford**, **Agfa**, **Polaroid**, **Rollei**), cinematic Log curves (**Technicolor CineStyle**, **Marvels Cine**, **Flaat**), and modern digital color profiles (**Fujifilm X-Trans III**, **Pixelmator Pro**, **PictureFX**), unified into **7 semantic macro-categories** based on photographic aesthetics.

---

## 🌐 Interactive Web Catalog & Triage Suite (`index.html`)

You can explore, filter, compare, and triage all **550 Picture Styles live in your browser** with zero external dependencies and 100% client-side GPU acceleration.

> 🚀 **[Try the Live Web Catalog on GitHub Pages](https://mercurydcd.github.io/canon-picture-styles-pf3-catalog/)**

The platform features two synchronized operational modes (toggle with **`V`** or the top-left switcher):

### 1. 🗂️ Mosaico (550 Matrix Grid)
* **Instant Visual Matrix:** See all 550 profiles rendered in real time on any photograph using WebGL 2.0 trilinear 3D LUT interpolation ($< 0.2\text{ ms}$ per preset).
* **2D Spatial Keyboard Navigation:** Seamless directional navigation across cards (`↑`, `↓`, `←`, `→`) using roving tabindex and visual proximity calculation.
* **11 Pattern Test Scenes:** Instant evaluation on curated high-resolution scenes (Portrait & Skin, High-Contrast Portrait, Outdoor Portrait, Landscape & Sky, Foliage & Nature, Urban Architecture, Street, High Dynamic Range, Golden Hour Sunset, Indoor Ambient, Textures & Detail).
* **Universal RAW & JPG Loader:** Drag & drop any **JPG, PNG, WebP**, or **Canon RAW (`.CR3` / `.CR2` / `.CRW`)** — embedded full-resolution previews are extracted directly in-browser in $< 20\text{ ms}$.
* **Realtime Filtering:** Instant predictive search by name, film emulsion, or creator (*"Velvia"*, *"Portra"*, *"Tri-X"*, *"CineStyle"*, *"Classic Chrome"*), macro-category selector, and ⭐ Favorites toggle.
* **A/B Split Curtain Modal:** Press **`Enter`** on any card (or click) to open a full-screen Top Layer inspection modal (`<dialog>`) with an interactive 60 fps split curtain, detailed metadata sheet, and $0\dots 100\%$ intensity slider.
* **Direct File Downloads:** Download camera-ready `.pf3` or `.pf2` files directly from each card.

### 2. ⚡ Carrusel (Fast 1-by-1 Triage View)
A high-efficiency workflow designed for rapid criba and curating your personal presets:
* **Full-Screen GPU Viewport:** Evaluates the active preset at maximum resolution on your chosen photograph with zero latency.
* **Continuous Queue Loop:** Automatically filters out already saved or discarded styles so you only evaluate pending profiles.
* **Floating Metadata HUD:** Displays Tonal Profile (Look), Recommended Usage, Historical Emulsion Heritage, and Creator in an unobtrusive translucent panel.
* **Multi-Scene Evaluation (`G`):** Toggle between single large photo view and an 11-scene simultaneous evaluation grid.
* **Favorites & Discarded Drawer:** Slide-in management panel (`<dialog>`) to review selections, copy slot assignments formatted for **Canon EOS Utility 3** (User Defined 1, 2, 3), and export your collection to JSON.

---

## ⌨️ Unified Keyboard Hotkeys Matrix

| Key | Context | Action |
| :--- | :--- | :--- |
| **`V`** | Global | Toggle between Matrix Grid (Mosaico) and Carousel (Carrusel) mode via View Transitions. |
| **`H`** | Global | Toggle top navigation bar visibility for distraction-free full-screen viewing (100vh). |
| **`↑ / ↓ / ← / →`** | Matrix Grid | 2D Spatial navigation between preset cards with automatic scroll-into-view. |
| **`Enter`** | Matrix Grid | Open full-screen A/B inspection modal for the currently focused card. |
| **`Space`** | Matrix / Carousel / Modal | Hold in Matrix to peek original / Toggle Before & After in Carousel and Modal. |
| **`K` / `Enter`** | Carousel | **Keep (Mantener)** — Save active preset to favorites and advance immediately. |
| **`D`** | Carousel | **Discard (Descartar)** — Exclude active preset from triage queue and advance. |
| **`S`** | Carousel | **Skip (Saltar)** — Postpone active preset to the end of the queue without discarding. |
| **`←` (Left Arrow)** | Carousel | Step back to the previous preset in the triage queue. |
| **`M`** | Global | Toggle **⭐ Real Favorite** status (synced across Matrix, Carousel, and Modal). |
| **`G`** | Carousel | Toggle between 11-Scene Multi-Grid and Single Large Photo view. |
| **`F`** | Carousel / Modal | Toggle image framing between **Fit** (complete image) and **Cover** (edge-to-edge fill). |
| **`R`** | Carousel | **Restart Loop** — Restore discarded and skipped presets to queue, preserving favorites. |
| **`Esc`** | Modal / Popovers / Drawer | Close active inspection modal, sample photo picker, or triage drawer. |

---

## 💻 Running Locally (Offline)

If you clone or download this repository, launch the included local server runner:

1. Double-click **`START_CATALOG.bat`** (or execute `python -m http.server 8080` in the repository directory).
2. Visit:
   ```text
   http://localhost:8080/index.html
   ```

---

## 📂 Repository Structure & 7 Macro-Categories

The repository is organized into 7 semantic categories. Each folder contains camera-ready profiles directly in its root (**authentic native `.pf2` / `.pf3` files** for PSE profiles, or **high-precision Hald PNG Level 12 LUTs** for film simulations), alongside hardware-accelerated binary matrices in `luts_bin/`:

```text
├── 01_Fujifilm/              # 103 profiles: Provia, Velvia, Astia, Classic Chrome, Superia, Pro Neg, X-Trans III
├── 02_Kodak/                 #  58 profiles: Portra, Kodachrome, Ektachrome, Ektar, Royal Gold, Ultramax
├── 03_Black_and_White/       #  95 profiles: Ilford HP5/FP4/Delta, Fuji Acros, Kodak Tri-X/T-Max, Rollei IR
├── 04_Cinema_and_Log/        #  40 profiles: Technicolor CineStyle, Marvels Cine, Flaat 1-4, Panalog
├── 05_Vintage_and_Instant/   #  94 profiles: Polaroid PX/600/Time-Zero, Agfa Ultra/Vista, Lomography
├── 06_Portraits_and_Brands/  #  26 profiles: Leica, Nikon D2X, Olympus Blue, Canon Studio, 5D Classic
├── 07_Creative_and_Artistic/ # 134 profiles: Pixelmator Pro, PictureFX, Kevin Wang Anime, Infrared
├── Favorites/                # Curated favorites collection with EOS Utility slot assignments (.pf3, .pf2, .png)
├── samples/                  # 11 reference pattern scenes for color science evaluation
├── CATALOG_SOURCES_AND_HISTORY.md # Complete technical catalog with emulsion histories and sensitivities
├── build_catalog.py          # Automated metadata generator for presets_data.js
├── index.html                # Zero-dependency, client-side WebGL 2.0 catalog & triage platform
├── lut_engine.js             # High-performance WebGL 2.0 3D LUT engine & RAW extractor
├── presets_data.js           # Pre-compiled JSON index of all 550 profiles
└── START_CATALOG.bat         # One-click local HTTP server launcher
```

| Category | Profiles | Formats Included | Description & Iconic Looks |
| :--- | :---: | :---: | :--- |
| [**`01_Fujifilm`**](./01_Fujifilm) | 103 | `.pf2`, `.pf3`, `.png`, `.bin` | All Fuji simulations united: Provia, Velvia (50, 100, 100F), Astia, Classic Chrome, Superia (100–1600), Pro Neg (Hi/Std), Reala, Pro 160S/160C/400H/800Z, Fortia, Sensia, Natura 1600, X-Trans III sensor emulations. |
| [**`02_Kodak`**](./02_Kodak) | 58 | `.pf2`, `.pf3`, `.png`, `.bin` | All Kodak color films: Portra (160, 400, 800, NC, VC, UC), Kodachrome (25, 64, 200), Ektachrome (E100G, E100VS, E200, 64), Crowdak V3, Elite Chrome Extra Color, Royal Gold, Ultramax, Gold 100/200/400. |
| [**`03_Black_and_White`**](./03_Black_and_White) | 95 | `.pf2`, `.pf3`, `.png`, `.bin` | Complete monochrome catalog: Ilford (HP5 Plus, FP4, Delta 100/400/3200, Pan F Plus, XP2), Fuji Acros (Standard, +G, +R, +Ye) & Neopan, Kodak (Tri-X 320/400, T-Max 100/400/3200, Plus-X, Panatomic-X, BW400CN), Rollei (IR 400, Ortho 25, Retro), Polaroid 665/667/672, Agfa APX, ZilverFX (01–10, InfraRed), Sepia. |
| [**`04_Cinema_and_Log`**](./04_Cinema_and_Log) | 40 | `.pf2`, `.pf3`, `.bin` | Video & cinema grading: Technicolor CineStyle, Similaar Flaat (1–4 Maximum DR), Kodak 2393 Print Film, Marvels Cine (1.2, 2.1 Panalog, 3.3, 3.4), Panavision Genesis Panalog, Bleach Bypass, Teal & Orange, Futuristic Bleak, CandleLight. |
| [**`05_Vintage_and_Instant`**](./05_Vintage_and_Instant) | 94 | `.pf2`, `.pf3`, `.png`, `.bin` | Instant and retro films: Polaroid color (PX-70, PX-680, Time-Zero, 600, 669, 690, Polachrome, Spectra), Agfa (Ultra 100, Vista, Optima, RSX II 100 Color Slide), Lomography (Redscale 100, Color Tiger, X-Pro, Toy Camera, Holga). |
| [**`06_Portraits_and_Brands`**](./06_Portraits_and_Brands) | 26 | `.pf2`, `.pf3`, `.bin` | Classic camera sensors & dedicated skin tones: Leica, Nikon D2X, Olympus Deep Blue, Canon Studio & Snapshot, Canon 5D Classic Mint/Neutral, Canon 1Ds Mark II, BeautyShot, Fair Skin, Bridal Hanayome, LightFace. |
| [**`07_Creative_and_Artistic`**](./07_Creative_and_Artistic) | 134 | `.pf2`, `.pf3`, `.png`, `.bin` | Contemporary & artistic looks: Pixelmator Pro suite (Bright, Calm, Dramatic, Flamboyant, Intense, Vintage, Warm), PictureFX (GoldFX Summer Heat/Sunset, AnalogFX Old Style), Kevin Wang Japanese Pastel Anime, Infrared Fake/Half/IR, Wagokoro, CreativePack film looks. |
| [**`Favorites`**](./Favorites) | 30 | `.pf2`, `.pf3`, `.png` | Curated top selections and camera User 1, 2 & 3 slot configurations. |

---

## 📖 Technical Documentation & Provenance

For detailed sensitometric curve behaviors, historical film emulsion backgrounds, and original creator provenance for each of the 550 profiles, consult:

👉 **[`CATALOG_SOURCES_AND_HISTORY.md`](CATALOG_SOURCES_AND_HISTORY.md)**

---

## 📷 Camera Compatibility

These Picture Style profiles (`.pf2` and `.pf3`) are compatible with all modern and classic Canon EOS cameras:

* **Canon EOS R Series (Mirrorless):** EOS R, RP, R3, R5, R5 Mark II, R6, R6 Mark II, R7, R8, R10, R50, R100.
* **Canon EOS M Series:** EOS M, M2, M3, M5, M6, M6 Mark II, M10, M50, M50 Mark II, M100, M200.
* **Canon EOS DSLRs:** 1D series, 5D series (Classic, Mk II, Mk III, Mk IV), 6D series, 7D series, 80D, 90D, Rebel / xxxD / xxxxD series.
* **Canon Cinema EOS:** C100, C200, C300 (supporting standard Picture Style files).

> [!IMPORTANT]
> **JPEG vs RAW Shooters & DPP 4 Limitations:**
> * **JPEG Shooting (In-Camera):** When installed into the camera's hardware slots via **Canon Style Studio**, the style's 3D LUT, tone curve, and color matrix are permanently baked directly into the in-camera JPEG by the camera's DIGIC image processor (*SOOC* — Straight Out Of Camera) and visible in Live View.
> * **RAW Shooting & Canon DPP 4:** Canon Digital Photo Professional (DPP 4) on PC **only processes 1D tone curves and 6-axis HSL matrices; it ignores third-party 3D LUT tables**. Consequently, RAW files shot with LUT-based profiles will appear Neutral in DPP 4. To develop RAW files with the full 3D look on PC, use the included WebGL 2.0 Web Suite (`index.html`) or apply the original `.cube` / Hald PNG LUT in Lightroom, Capture One, or Photoshop.

---

## 🛠 How to Register Styles Onto Your Camera

Canon EOS cameras allow registering up to **3 custom Picture Styles** simultaneously into the internal hardware memory slots (**User Defined 1**, **User Defined 2**, and **User Defined 3**).

### 🎯 Tool & Format Compatibility Matrix

| Format in Catalog | Type & Origin | Recommended Tool | Why this tool? |
| :--- | :--- | :--- | :--- |
| **`.pf3` / `.pf2`** | **Native Canon Styles** (Picture Style Editor) | **Canon EOS Utility 3** | Contains authentic mathematical 1D tone curves, 3x3 matrices, and selective color tables (`0x1023`). EOS Utility compiles these cleanly. *Do not load into Canon Style Studio's base or it will throw `Unsupported PF3 property size: 0x40001023`.* |
| **`.png` (Hald L12) / `.cube`** | **Analog Film Simulation 3D LUTs** | **Canon Style Studio** | Contains full 3D volumetric color transformations ($33^3$ / 35,937 colors). Stock EOS Utility normalizes third-party 3D tables to flat Neutral. Canon Style Studio synthesizes the exact hardware DIGIC carrier directly. |

---

### 📷 Hardware Camera Prerequisites (DIGIC 7 & DIGIC 8 — M100, M6 Mark II, R Series)

Before connecting your camera via USB:
1. **Camera Mode Dial:** Set the physical dial to **P, Tv, Av, or M**. In Auto (`A+`), SCN, Creative Filters, or Movie mode, Canon camera firmware locks the Picture Style PTP register.
2. **Disable Wireless:** Set **Wi-Fi and Bluetooth to Disable [Off]** in the yellow camera setup menu (wrench). Active wireless locks the USB remote control bus.
3. **Close Background Software:** Completely exit EOS Utility before launching Canon Style Studio (or vice versa). Only one tool can talk to the camera at a time.

---

### Method 1: Film Simulation LUTs (.png Hald Level 12) via Canon Style Studio

Use this method for all film simulations downloaded as `.png`:

1. Download the `.png` LUT file from the Web Catalog or locate it in the category folders.
2. Ensure **EOS Utility 3 is completely closed** (including from the Windows system tray).
3. Connect the camera via USB and turn it on (Mode Dial in P/Tv/Av/M).
4. Launch **`START_CANON_STYLE_STUDIO.bat`** (or `CanonStyleStudio.exe`).
5. **Keep Base Picture Style on `Neutral`** (or `Standard`).
6. Click **`Add LUT…`** and select your downloaded **Hald Level 12 `.png`** (or `.cube`).
7. Adjust the opacity slider (0–100%) or sharpness if desired.
8. Click **`SEND TO CAMERA`** in the top toolbar.
9. Select your camera model and destination slot (**`User Def. 1`**, **`User Def. 2`**, or **`User Def. 3`**).
10. Enter a custom display name (max 31 chars, e.g. `FUJI 400H`, `PORTRA 160`) and click **`Install independently…`**.
11. Disconnect the USB cable, select the configured User Defined Picture Style on the camera, and shoot!

---

### Method 2: Native Canon Picture Styles (.pf3 / .pf2) via EOS Utility 3

Use official Canon EOS Utility 3 for native styles (`.pf3` / `.pf2`):

1. Download the `.pf3` or `.pf2` file.
2. Connect your camera via USB and launch **Canon EOS Utility 3**.
3. Select **`Camera settings`** $\rightarrow$ **`Register Picture Style File`**.
4. Select the target slot (**User Defined 1, 2, or 3**), open the `.pf3` / `.pf2` file, and click **`OK`**.

---

### ⚡ Hardware Troubleshooting & Solutions (Proven on Hardware)

#### 1. Error: `Slot style envelope is disabled or inconsistent`
* **Root Cause:** The target slot (`User Def 1/2/3`) in camera NVRAM is unformatted or in a reset state (flag `0`). Canon Style Studio expects an active carrier envelope.
* **The Golden Solution:**
  1. Close Canon Style Studio.
  2. Open **Canon EOS Utility 3**.
  3. Register any valid `.pf3` (any style from the catalog or Canon official) into the problematic slot. This formats the camera's internal 16,712-byte carrier and activates the slot flag to enabled (`1`).
  4. Exit EOS Utility completely.
  5. Reopen **Canon Style Studio** and flash your `.png` LUT. It will now succeed immediately.

#### 2. Error: `Slot Basic controls differ` (`SlotControlMismatch`)
* **Root Cause:** The camera slot currently has non-zero slider adjustments (e.g. Contrast: -3, Saturation: -2, Color Tone: -1), while Canon Style Studio has them set to 0.
* **Solution:** Look at the numbers in the error report and adjust the 4 basic control sliders (Contrast, Saturation, Color Tone, Sharpness Threshold) in Canon Style Studio's sidebar to match the camera's values before clicking install.

#### 3. Error: `ValueError: Unsupported PF3 property size: 0x40001023`
* **Root Cause:** Trying to load a native Canon `.pf3` with selective color tables (`0x1023`) into Canon Style Studio's base.
* **Solution:** Keep the base in Canon Style Studio set to stock **`Neutral`** when using LUTs. For native `.pf3` files, install them directly with **EOS Utility 3**.

---

## 🔬 Color Science & WebGL 2.0 Engine Architecture

This platform leverages high-precision mathematical transformations:
* **Hardware-Accelerated WebGL 2.0:** Employs 3D volumetric textures (`sampler3D`) with native GPU trilinear interpolation for instantaneous grading ($< 0.2\text{ ms}$ per frame).
* **12-bit Quantization:** Downsamples LUT matrices to Canon's official $33^3$ format (`0x40001070` and `0x40001071`) preserving highlight linearity and shadow fidelity.
* **Firmware Validation:** Validated with Canon's official `EdsCFParse.dll` runtime from Picture Style Editor, ensuring 100% valid CRC checksums and camera firmware compliance.
* **Client-Side RAW Decoding:** Custom binary parser reads the TIFF/IFD structure of Canon RAW files (`.CR3`, `.CR2`, `.CRW`) and streams the embedded preview JPEG in $< 20\text{ ms}$ without server-side processing.

---

## ☕ Support & Donations

If this curated catalog, the real-time WebGL 2.0 triage engine, or the camera-ready Picture Style profiles bring value to your photography or filmmaking workflow, you can support ongoing maintenance, color science profiling, and continuous platform development:

| Platform | Channel | Description |
| :--- | :--- | :--- |
| **Ko-fi** | [ko-fi.com/dcorral](https://ko-fi.com/dcorral) | One-time tips or regular coffees with zero friction. |
| **GitHub Sponsors** | [github.com/sponsors/MercuryDCD](https://github.com/sponsors/MercuryDCD) | Open-source project sponsorship and developer support. |

[![Ko-fi](https://img.shields.io/badge/Ko--fi-Tip%20or%20Coffee-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/dcorral)
&nbsp;
[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-GitHub%20Sponsors-EA4AAA?style=for-the-badge&logo=github-sponsors&logoColor=white)](https://github.com/sponsors/MercuryDCD)

---

## 📜 Credits & Acknowledgments

Honoring the color scientists and photographers who developed these looks over two decades:
* **Thomas Fransson:** Creator of native `.pf3` film simulations (*Astia Pack*, *Portra EDR/STD*, *California Cowboy*, *T-Rex B&W*, *Crowdak*, *Filmic*).
* **Vision Wrangler (Cinescopophilia):** Curator of the legendary 158-style community archive.
* **Kevin Wang:** Author of the celebrated *Japanese Style* pastel and *LOMO* color palettes.
* **Martin Beek (Marvels Film):** Pioneer of independent cinema profiles (*Marvels Cine*).
* **Similaar:** Creator of the *Flaat* dynamic range Log series.
* **LvClFER:** Developer of *Canon Style Studio* and independent serializer research.
* **Canon Inc.:** Creator of the Picture Style architecture and DPP/PSE image engines.

---

## ⚖ Disclaimer

*Canon*, *EOS*, and *Picture Style* are registered trademarks of Canon Inc. This repository is non-commercial, created for educational, creative, and historical preservation purposes.
