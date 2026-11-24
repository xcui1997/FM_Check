# FM_Check — 3D Focal Mechanism & Stereographic Projection Lab
# FM_Check — 三维震源机制与赤平投影交互可视化实验室

[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-0ea5e9?style=flat-square)](https://xcui1997.github.io/FM_Check/)
[![Bilingual](https://img.shields.io/badge/Language-EN%20%2F%20%E4%B8%AD%E6%96%87-10b981?style=flat-square)](#)

> **Co-created by [xcui1997](https://github.com/xcui1997) & Gemini.**  
> **由 [xcui1997](https://github.com/xcui1997) 与 Gemini 共同创建。**

---

## English Overview

**FM_Check** is an interactive, zero-dependency, browser-based 3D seismological laboratory designed to inspect, verify, and visualize earthquake **focal mechanisms (beachballs)**, **conjugate nodal planes**, **P/T principal stress axes**, and **stereographic projections** in real time.

### Key Features
* **Synchronized 3-Column 3D Observatory**:
  1. **3D Fault Kinematics & Nodal Planes**: Interactive fault-block slip animation, green fault plane (`NP1`), violet auxiliary plane (`NP2`), `P` (compressional) / `T` (extensional) axes, horizontal map-cut ring (blue), and vertical cross-section ring (yellow).
  2. **Map View (Lower-Hemisphere Cutaway)**: Horizontal equatorial slice projecting the lower-hemisphere bowl onto a standard `N / E / S / W` stereographic map disc.
  3. **Cross-Section View (Back-Hemisphere Cutaway)**: GMT `pscoupe`-style vertical slice along profile `A → A'` projecting the back hemisphere onto a vertical depth section (`Surface` / `Depth ↓`) to reveal true subsurface dip angles.
* **Multi-Format Seismological Query Parser**:
  * `Strike / Dip / Rake` (e.g., `210 / 32 / 90` or `Strike=135 Dip=60 Rake=40`)
  * USGS `NP1` strings (`NP1: strike=180, dip=55, rake=-90`)
  * 6-component **Global CMT / USGS Moment Tensors** (`Mrr, Mtt, Mpp, Mrt, Mrp, Mtp`)
  * `P / T` axis trend & plunge pairs (`P: 135/05, T: 225/05`)
* **Lossless Conjugate Plane Toggle (`Swap NP1 / NP2`)**: Instantly swaps the fault plane and auxiliary plane while preserving P/T stress axes and far-field radiation patterns.
* **Bilingual UI (`EN / 中文`)**: One-click switching between English and Chinese interfaces.

### Quick Start
* **Online**: Visit [`https://xcui1997.github.io/FM_Check/`](https://xcui1997.github.io/FM_Check/)
* **Local**: Simply open `index.html` in any modern WebGL-enabled browser (no build step or server required).

---

## 中文说明

**FM_Check** 是一个无需安装任何依赖、打开浏览器即可使用的**三维震源机制（沙滩球）与赤平投影交互可视化实验室**，用于快速查看、核验与教学演示地震双力偶震源机制、共轭双节面、P/T 主应力轴以及不同视角下的投影几何关系。

### 核心功能
* **三栏联动三维震源观测台**：
  1. **三维断层运动学与双节面模型**：实时演示断层两盘错动动画，同步显示发震断层面（`NP1`，绿色）、共轭辅助面（`NP2`，紫色）、`P` 轴（压应力）与 `T` 轴（张应力）、蓝色水平切割圈以及黄色垂直剖面切割圈。
  2. **地图俯视投影（下半球切割）**：沿水平赤道面切去上半球，将下半球碗壳投影至 `N / E / S / W` 水平地理圆盘（常规地图视角沙滩球）。
  3. **剖面视角投影（后半球切割）**：采用地震学软件 GMT `pscoupe` 标准算法，沿垂直剖面 `A → A'` 切去前半球，将后半球投影至竖直深度剖面屏（`Surface` / `Depth ↓`），直观呈现地下断层或俯冲板片的真实倾角。
* **多格式震源参数快速解析**：
  * 走向 / 倾角 / 滑动角（如 `210 / 32 / 90` 或 `Strike=135 Dip=60 Rake=40`）
  * USGS 节面字符串（`NP1: strike=180, dip=55, rake=-90`）
  * **Global CMT / USGS 六分量地震矩张量**（`Mrr, Mtt, Mpp, Mrt, Mrp, Mtp`）
  * `P / T` 主应力轴方位角与倾伏角（`P: 135/05, T: 225/05`）
* **无损共轭节面切换（`Swap NP1 / NP2`）**：一键互换假设断层面（NP1）与辅助面（NP2），直观验证共轭断层面具有完全相同的远场 P/T 轴与沙滩球辐射花样。
* **中英文双语界面（`EN / 中文`）**：页面右上角支持一键实时切换中英文。

### 使用方式
* **在线访问**：打开 [`https://xcui1997.github.io/FM_Check/`](https://xcui1997.github.io/FM_Check/)
* **本地运行**：直接双击 `index.html` 即可在任意支持 WebGL 的现代浏览器中运行。

---

### Credits / 致谢
Created collaboratively by **xcui1997** and **Gemini**.  
本工具由 **xcui1997** 与 **Gemini** 共同设计并构建。

