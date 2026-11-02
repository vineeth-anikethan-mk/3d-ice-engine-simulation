# Interactive 3D Internal Combustion Engine Digital Twins

> High-fidelity, real-time cutaway 3D simulations of modern internal combustion engines built with **Three.js (WebGL)** and **JavaScript (ES Modules)**. Self-contained, zero-dependency, and interactive across desktop and mobile browsers.

Developed as part of the **BSERC Gen AI Internship** project, demonstrating how structured generative AI workflows can design, model, and simulate complex mechanical systems.

---

## Overview

This repository contains three interactive, photorealistic 3D simulations of advanced automotive powertrain architectures:

1. **2.0L 4-Cylinder Turbocharged Direct-Injection (TDI) Diesel Engine**
2. **Mercedes-AMG G63 4.0L M177 "Hot-Inside-V" Bi-Turbo V8 Engine**
3. **Bugatti Chiron Super Sport 8.0L Quad-Turbo W16 Engine**

Each model features exact mathematical slider-crank kinematics, reciprocating pistons with wrist pins and rings, dual/quad overhead camshafts driving angled valves with dynamic compressing helical springs, rotating toothed timing gears with traveling belt/chain links, realistic turbocharger and manifold plumbing, and real-time thermodynamic HUD telemetry.

---

## Featured Engine Simulations

### 1. 2.0L I4 Turbocharged Diesel Engine (`diesel_engine_3d.html`)
* **Architecture**: Inline-4, 16.5:1 compression ratio, 180° flat-plane forged steel crankshaft (`1-3-4-2` 720° firing order).
* **Combustion & Fueling**: Toroidal omega bowl-in-piston crowns, 2,000-bar common-rail with central piezo injectors, multi-plume atomization sprays near TDC, and adiabatic compression auto-ignition flashes.
* **Valvetrain**: DOHC 16-valve setup with helical coil springs, bucket tappets, bronze guides, valve seat rings, and internal head port ducts.
* **Forced Induction**: Variable Geometry Turbocharger (VGT) with cast block support bracket, braided stainless oil feed and return lines, overhead charge pipe with silicone couplers, front finned intercooler, electronic throttle body, rear EGR cooler crossover loop, and pipe-aligned intake/exhaust particle streams.
* **Timing & Rotating Assembly**: CNC-machined toothed timing gears (crankshaft, twin cams, CP4 HPFP, water pump, and idler), traveling timing belt cleats, and a 36-tooth dual-mass flywheel with clutch friction face and damper packs.

---

### 2. Mercedes-AMG G63 4.0L "Hot-V" Bi-Turbo V8 (`mercedes_g63_amg_v8_biturbo_3d.html`)
* **Architecture**: 90° V8 closed-deck block with Nanoslide cylinder sleeves, cross-plane crankshaft (`0°, 90°, 270°, 180°` throws; `1-5-4-2-6-3-7-8` firing order at 90° intervals) with shared side-by-side H-beam connecting rods.
* **"Hot-Inside-V" Turbocharging**: Twin-scroll turbochargers positioned directly inside the 90° cylinder valley on a heavy cast mounting pedestal, eliminating turbo lag. Includes exhaust manifold port flanges, electronic wastegate actuators with linkage rods, twin downpipes with V-band clamps, and CHRA oil/water plumbing.
* **Charge-Air Induction**: Outer carbon-fiber intake plenums with AMG red branding strips, dual front water-to-air charge-air coolers, electronic throttle bodies, and flanged intake runners.
* **Valvetrain**: Quad overhead camshafts with 32 angled valves, compressing helical springs, anodized retainers, hydraulic tappets, and internal head ducts.
* **Timing Drive**: Dual-bank timing drive with CNC-machined cam-phaser sprockets, center V-valley transfer gear, traveling duplex chain links, front Poly-V serpentine belt, and a 38-tooth AMG flywheel.
* **Live Telemetry**: Dyno output (577 HP, 850 N·m torque curve), boost pressure (up to 1.50 bar), 200-bar rail pressure, Hot-V valley EGT, and an 8-cylinder firing monitor.

---

### 3. Bugatti Chiron Super Sport 8.0L Quad-Turbo W16 (`bugatti_chiron_supersport_w16_3d.html`)
* **Architecture**: 8.0L W-configuration composed of two narrow-angle 15° VR8 cylinder banks set at a 90° main V-angle (4 staggered cylinder rows at `-52.5°, -37.5°, +37.5°, +52.5°`).
* **Cranktrain**: 8-throw forged titanium crankshaft firing every 45° across all 16 cylinders, titanium connecting rods, forged alloy pistons, and a 40-tooth dual-clutch transmission (DSG) flywheel with radial torsion dampers.
* **2-Stage Sequential Quad-Turbocharging**: 4 giant turbochargers (2 primary active from idle + 2 secondary Stage-2 engaging above 3,800 RPM) fed by 16 individual bolted Inconel exhaust headers (four 4-into-1 collectors) with sequential balance bridges and block brackets.
* **Valvetrain & Induction**: 64 complete valves with compressing helical springs, roller followers, 64 machined cam lobes, 32 sequential fuel injectors fed by 4 anodized fuel rails, top carbon-fiber "16.4" intake plenums with 16 downward runners, dual throttle bodies, and rear liquid charge coolers.
* **Live Telemetry**: 1,600 PS power, 1,600 N·m torque, 2/4 vs 4/4 active turbo indicator, 1.85 bar boost, titanium EGT, and a 16-cylinder 4-stroke matrix.

---

## Interactive Controls & Features

Across all three engine simulations, the user interface provides:

| Control | Description |
| :--- | :--- |
| **Throttle / RPM Slider** | Continuously sweep engine speed from idle to redline with dynamic torque/power scaling and thermal glow. |
| **Simulation Time Scale** | Smoothly slow down the cycle (down to 0.01x) to analyze stroke-by-stroke kinematics and valve overlap. |
| **Block Cutaway Opacity** | Adjust engine block and cylinder head transparency (0%–100%) to view internal components. |
| **Cycle Pause / Resume** | Freeze kinematics at any point in the 720° 4-stroke cycle while preserving full 3D camera navigation. |
| **Exploded Assembly View** | Smoothly expand engine sub-assemblies (block, heads, valvetrain, turbos, intake, fuel, timing) along exploded vectors. |
| **Component Toggles** | Isolate or hide individual subsystems (Block, Heads, Turbos, Valvetrain, Fuel, Timing Belt/Chains, 3D Labels). |
| **10 Camera Presets** | Instant, smoothed camera choreographies targeting specific subsystems (Isometric, Turbos, Timing Drive, Flywheel, Banks, etc.). |
| **3D Floating Callouts** | Screen-space projected engineering annotation tags with sub-labels attached to key components. |

---

## Project Structure

```text
.
├── README.md                                    # Project documentation & GitHub overview
├── diesel_engine_3d.html                        # 2.0L I4 Turbocharged Diesel Engine simulation
├── mercedes_g63_amg_v8_biturbo_3d.html          # Mercedes-AMG G63 4.0L Bi-Turbo V8 simulation
├── bugatti_chiron_supersport_w16_3d.html        # Bugatti Chiron Super Sport 8.0L W16 simulation
└── 3D_Engine_Simulation_Prompts_4_Part_Format.docx # Structured 4-part prompts documentation
```

---

## Getting Started

### Direct Browser Launch (No Build or Installation Required)
All simulations are standalone single-file HTML applications. You do not need to install Node.js, Webpack, or external libraries:

1. Clone or download this repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```
2. Double-click any of the HTML files to open it directly in your web browser:
   * `diesel_engine_3d.html`
   * `mercedes_g63_amg_v8_biturbo_3d.html`
   * `bugatti_chiron_supersport_w16_3d.html`

### Deploying via GitHub Pages
To host these interactive simulations live on GitHub Pages:
1. Go to your repository settings on GitHub (`Settings` > `Pages`).
2. Under **Build and deployment**, select `Deploy from a branch` and choose `main` / `root`.
3. Open the published URL in your browser and append the HTML filename (e.g., `https://<username>.github.io/<repo>/mercedes_g63_amg_v8_biturbo_3d.html`).

---

## Technical Stack

* **Graphics Engine**: [Three.js](https://threejs.org/) (r160) loaded via modern ES Module Import Maps
* **Rendering & Shading**: WebGLRenderer with Physically Based Rendering (PBR `MeshStandardMaterial` & `MeshPhysicalMaterial`), ACESFilmic Tone Mapping, and PCFSoftShadowMap
* **Interaction**: `OrbitControls` with inertial damping, smooth camera interpolation, and raycasting
* **Styling**: Responsive HTML5 / CSS3 HUD overlays with frosted-glass backdrop filters (`backdrop-filter: blur(...)`)
* **Kinematic Solver**: Analytical slider-crank trigonometry ($y = r\cos\theta + \sqrt{L^2 - (r\sin\theta)^2}$) evaluated per cylinder per frame

---

## Prompt Engineering Framework

All models were generated and iterated using the structured **4-Part Prompt Engineering Methodology** (**Who • What • Do • Rules**):

* **Who**: Defines the user persona, context, and engineering depth.
* **What**: Specifies the powertrain architecture, cylinder layout, firing order, and subsystem fidelity.
* **Do**: Itemizes 5+ interactive controls (sliders, toggles, buttons, camera presets).
* **Rules**: Enforces single-file delivery, responsive viewports, realistic telemetry formulas, and strict component synchronization.

Refer to `3D_Engine_Simulation_Prompts_4_Part_Format.docx` for the prompt templates and guidelines.

---

## License

This project is licensed under the [MIT License](LICENSE).
