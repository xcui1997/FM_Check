# FM_Check — Interactive Seismology Labs / 地震学交互实验室

## Live demos / 在线演示

- [3D Focal Mechanism & Stereographic Projection Lab / 三维震源机制与赤平投影实验室](https://xcui1997.github.io/FM_Check/)
- [Section 9.1 — Green’s Functions & the Moment Tensor / 第 9.1 节：格林函数与地震矩张量](https://xcui1997.github.io/FM_Check/section_9_1_green_s_functions_the_moment_tensor_interactive_lab.html)

Use the page header to switch labs. Both support **EN / 中文**.

可通过页首导航切换实验，两个页面均支持 **EN / 中文**。

---

## English Overview

### 3D Focal Mechanism & Stereographic Projection

Inspect earthquake **focal mechanisms (beachballs)**, conjugate nodal planes, **P/T axes**, and stereographic projections in three synchronized views.

- **3D Fault Kinematics & Nodal Planes** shows animated fault slip, green fault plane (`NP1`), violet auxiliary plane (`NP2`), `P` (compressional) and `T` (extensional) axes, and cut rings for the horizontal map (blue) and vertical section (yellow).
- **Map View (Lower-Hemisphere Cutaway)** projects the lower hemisphere onto an `N / E / S / W` stereographic map disc.
- **Cross-Section View (Back-Hemisphere Cutaway)** projects the back hemisphere onto a GMT `pscoupe`-style vertical depth section along profile `A → A'`.
- **Parse & Plot** accepts the following inputs.
  * `Strike / Dip / Rake` (e.g., `210 / 32 / 90` or `Strike=135 Dip=60 Rake=40`)
  * USGS `NP1` strings (`NP1: strike=180, dip=55, rake=-90`)
  * 6-component **Global CMT / USGS Moment Tensors** (`Mrr, Mtt, Mpp, Mrt, Mrp, Mtp`)
  * `P / T` axis trend & plunge pairs (`P: 135/05, T: 225/05`)
- **Swap NP1 / NP2** exchanges the fault plane and auxiliary plane while preserving the P/T axes and far-field radiation pattern.
- **Interactive controls** let you choose a faulting preset, adjust strike, dip, rake, and section azimuth, or start an automatic sweep.

### Section 9.1 — Green’s Functions & the Moment Tensor

Explore how source forces and the response of the Earth combine to produce a seismogram. The lab follows Section 9.1 of Peter M. Shearer’s *Introduction to Seismology* (2nd ed.). [Textbook contents](https://assets.cambridge.org/97805218/82101/toc/9780521882101_toc.pdf)

- **Visual guide** to point-force impulse responses, spatial derivatives, double couples, and convolution with a source time function.
- **Moment tensor** presets, clickable matrix cells, and six component sliders update a 3D force diagram, lower-hemisphere beachball, and physical diagnostics.
- **Wavefield** controls let you launch a pulse, compare point forces and force couples, and vary source separation and station azimuth to see their effects on the schematic traces.
- **Seismogram synthesis** shows six weighted elementary responses and their synthetic sum. Adjust station azimuth, takeoff angle, source pulse width, and vertical, radial, or transverse component.

The wavefield and synthetic traces use simplified teaching models to illustrate how source geometry and receiver position affect the signal.

---

## 中文说明

### 三维震源机制与赤平投影

通过三个联动视图，观察地震**震源机制（沙滩球）**、共轭节面、**P/T 轴**以及不同视角下的投影几何关系。

- **三维断层运动学与双节面模型**演示断层两盘错动，显示断层面（`NP1`，绿色）、共轭辅助面（`NP2`，紫色）、`P` 轴（压缩方向）与 `T` 轴（伸展方向），以及蓝色水平切割圈和黄色垂直切割圈。
- **地图俯视投影**将下半球投影至带有 `N / E / S / W` 方向标记的水平沙滩球圆盘。
- **剖面视角投影**采用 GMT `pscoupe` 风格，沿剖面 `A → A'` 将后半球投影到垂直深度剖面。
- **解析并绘图**支持以下输入。
  * 走向 / 倾角 / 滑动角（如 `210 / 32 / 90` 或 `Strike=135 Dip=60 Rake=40`）
  * USGS 节面字符串（`NP1: strike=180, dip=55, rake=-90`）
  * **Global CMT / USGS 六分量地震矩张量**（`Mrr, Mtt, Mpp, Mrt, Mrp, Mtp`）
  * `P / T` 轴方位角与倾伏角（`P: 135/05, T: 225/05`）
- **切换共轭节面（`Swap NP1 / NP2`）**可互换断层面与辅助面，同时保持 P/T 轴和远场沙滩球辐射图样。
- **交互控制**支持选择典型断层预设、调整走向、倾角、滑动角和剖面方位角，以及启动自动演示。

### 第 9.1 节：格林函数与地震矩张量

结合 Peter M. Shearer 的《Introduction to Seismology》（第 2 版）第 9.1 节，探索震源作用和介质响应如何共同生成地震图。[教材目录](https://assets.cambridge.org/97805218/82101/toc/9780521882101_toc.pdf)

- **物理图解**介绍点力脉冲响应、空间导数、双力偶，以及格林函数与震源时间函数的卷积。
- **矩张量实验**可选择震源预设、点击矩阵元素或调整六个独立分量，联动查看三维力学图、下半球沙滩球和物理诊断。
- **波场实验**可激发脉冲、比较点力与力偶，调整力源间距和台站方位角，观察示意波形的变化。
- **地震图合成**显示六个加权基本响应及其总和，可调整台站方位角、离源角、震源脉冲宽度，并切换竖直、径向或横向分量。

波场和合成波形使用简化的教学模型，用于观察震源几何和接收台站位置如何影响记录。

## Local use and publishing / 本地运行与发布

Open `index.html` or `section_9_1_green_s_functions_the_moment_tensor_interactive_lab.html` directly in a modern browser. Keep an internet connection for CDN assets and use a WebGL-enabled browser for the focal-mechanism views.

在现代浏览器中打开对应的 HTML 文件即可运行，无需构建。外部资源通过 CDN 加载，需要联网。震源机制实验的三维视图需要浏览器支持 WebGL。

GitHub Pages publishes from the root of `main`. The site homepage serves the focal-mechanism lab, and the Section 9.1 lab is available at its own URL.

GitHub Pages 从 `main` 分支的根目录发布。网站首页展示震源机制实验，第 9.1 节实验使用独立网址。

## Credits / 致谢

The 3D focal-mechanism lab was co-created by [xcui1997](https://github.com/xcui1997) and Gemini.

三维震源机制实验由 [xcui1997](https://github.com/xcui1997) 与 Gemini 共同设计并构建。

