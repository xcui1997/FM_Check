# FM_Check — Interactive Seismology Labs

[![Live demos on GitHub Pages](https://img.shields.io/badge/GitHub_Pages-Live_Demo-0969da?style=flat-square)](https://xcui1997.github.io/FM_Check/)

**English** | [简体中文](README.zh-CN.md) | [Source code](https://github.com/xcui1997/FM_Check) | [Live demos](#live-demos) | [Quick start](#quick-start)

---

FM_Check is a set of four browser-based labs for teaching and exploring earthquake focal mechanisms and source physics. Use the interactive views to connect fault geometry, moment tensors, and rupture models with the radiation patterns, seismograms, and spectra they produce.

## Live demos

| Lab | What to explore | Source |
| --- | --- | --- |
| [3D Focal Mechanism & Stereographic Projection](https://xcui1997.github.io/FM_Check/) | Rotate a fault model and compare the map and vertical-section beachballs. | [HTML](index.html) |
| [§9.1 · Green’s Functions & the Moment Tensor](https://xcui1997.github.io/FM_Check/section_9_1_green_s_functions_the_moment_tensor_interactive_lab.html) | Build a moment tensor from force couples and see how their contributions add up to a seismogram. | [HTML](section_9_1_green_s_functions_the_moment_tensor_interactive_lab.html) |
| [Chapter 9 · Source Theory](https://xcui1997.github.io/FM_Check/chapter_9_source_theory_interactive_lab.html) | Compare rupture directivity, source spectra, non-double-couple sources, scaling, and empirical Green’s function deconvolution. | [HTML](chapter_9_source_theory_interactive_lab.html) |
| [§§9.4.2, 9.5.1 & 9.7 · Magnitude Saturation & Source Spectra](https://xcui1997.github.io/FM_Check/section_9_4_9_7_magnitude_saturation_source_spectra_lab.html) | Compare body-wave, surface-wave, and moment magnitudes as earthquake size and source spectrum change. | [HTML](section_9_4_9_7_magnitude_saturation_source_spectra_lab.html) |

The page header links to the other labs and lets you switch between **English** and **中文**.

## Key features

### 3D Focal Mechanism & Stereographic Projection

- Three synchronized views show animated fault slip, the `NP1` and `NP2` nodal planes, P/T axes, a lower-hemisphere map projection, and a GMT `pscoupe`-style vertical section along a selectable azimuth.
- **Parse & Plot** accepts strike/dip/rake, USGS nodal-plane strings, six-component Global CMT or USGS tensors, and P/T trends and plunges.
- Use faulting presets, angle sliders, or **Auto-Sweep** to explore different mechanisms. **Swap NP1 / NP2** exchanges the nodal planes while preserving the far-field radiation pattern and P/T axes.

### §9.1 · Green’s Functions & the Moment Tensor

- Visual guides introduce point-force impulse responses, spatial derivatives, double couples, and convolution with a source time function.
- Presets, clickable tensor cells, and six component sliders update the force diagram, lower-hemisphere beachball, and physical diagnostics.
- Launch a pulse and adjust force separation or station azimuth to compare schematic waveforms. The synthesis tab displays six weighted elementary responses and their sum, with controls for takeoff angle, pulse width, and the vertical, radial, and transverse components.

### Chapter 9 · Earthquakes & Source Theory

- Compare unilateral and bilateral rupture, sub-shear and supershear propagation, and the resulting displacement pulses at four azimuths.
- Explore Brune spectra and magnitude saturation, then vary moment magnitude, stress drop, and rigidity in the self-similar scaling module.
- Vary isotropic, double-couple, and compensated linear vector dipole (CLVD) components and see how the beachball and Hudson source-type plot respond.
- Apply empirical Green’s function (EGF) deconvolution to synthetic traces and see how event location, mechanism mismatch, noise, and water-level regularization affect the recovered source pulse.

### §§9.4.2, 9.5.1 & 9.7 · Magnitude Saturation & Source Spectra

- Linked plots compare the far-field displacement spectrum and the $m_b$, $M_S$, and $M_W$ curves as you vary $M_W$ from 4.0 to 9.5, adjust stress drop, or switch between the Brune and Boatwright models.
- Compare the 1 s and 20 s measurement periods with the rupture pulse duration to see how the fixed measurement bands contribute to magnitude saturation. A separate tab illustrates Aki’s self-similar scaling and shows how the corner frequency falls as seismic moment increases at fixed stress drop.
- Load examples such as the 1960 Chile, 1964 Alaska, 2004 Sumatra, 2008 Wenchuan, and 1992 Landers earthquakes from the event table based on Shearer’s Table 9.1.

## Quick start

1. **Focal mechanisms.** Enter `210 / 32 / 90` and select **Parse & Plot**. Use **Swap NP1 / NP2** to see how the nodal planes exchange roles while the radiation pattern stays the same.
2. **Green’s functions.** Open **Nine Force Couples & Moment Tensor**, select **Pure Strike-Slip**, and adjust one tensor component to see how the beachball changes.
3. **Source theory.** Open **9.4.1 Directivity**, choose **Unilateral**, and select **Trigger Quake**. Compare the displacement pulses at 0° and 180°.
4. **Magnitude saturation.** Compare the $M_W = 4.5$ preset with **1960 Chile**. Watch the corner frequency move relative to the 1 Hz and 0.05 Hz measurement bands.

## Run locally

Open the corresponding HTML file directly in a modern browser. `index.html` opens the focal-mechanism lab. The pages load fonts and libraries from CDNs, and the focal-mechanism lab uses WebGL for its 3D views.

GitHub Pages publishes these files from the root of the `main` branch.

## References and credits

The source-theory labs follow topics in Chapter 9 of Peter M. Shearer’s *Introduction to Seismology* (2nd ed.). The wavefield and synthetic traces use simplified teaching models. [Textbook contents](https://assets.cambridge.org/97805218/82101/toc/9780521882101_toc.pdf)

The 3D focal-mechanism lab was co-created by xcui1997 and Gemini. [xcui1997 on GitHub](https://github.com/xcui1997)
