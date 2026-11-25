# FM_Check — 地震学交互实验室

[![GitHub Pages 在线演示](https://img.shields.io/badge/GitHub_Pages-Live_Demo-0969da?style=flat-square)](https://xcui1997.github.io/FM_Check/)

[English](README.md) | **简体中文** | [源代码](https://github.com/xcui1997/FM_Check) | [在线演示](#在线演示) | [快速上手](#快速上手)

---

FM_Check 包含四个可在浏览器中使用的地震学实验，适合课堂演示和自学。通过交互图形，可以观察断层几何、地震矩张量和破裂模型如何影响辐射图样、地震图与震源谱。

## 在线演示

| 实验 | 可以探索什么 | 源文件 |
| --- | --- | --- |
| [三维震源机制与赤平投影](https://xcui1997.github.io/FM_Check/) | 旋转断层模型，对比地图和垂直剖面中的沙滩球。 | [HTML](index.html) |
| [第 9.1 节 · 格林函数与地震矩张量](https://xcui1997.github.io/FM_Check/section_9_1_green_s_functions_the_moment_tensor_interactive_lab.html) | 用力偶构建矩张量，观察各项响应如何叠加成地震图。 | [HTML](section_9_1_green_s_functions_the_moment_tensor_interactive_lab.html) |
| [第 9 章 · 震源理论](https://xcui1997.github.io/FM_Check/chapter_9_source_theory_interactive_lab.html) | 探索破裂方向性、震源谱、非双力偶震源、标度律及经验格林函数反褶积。 | [HTML](chapter_9_source_theory_interactive_lab.html) |
| [第 9.4.2、9.5.1 与 9.7 节 · 震级饱和与震源谱](https://xcui1997.github.io/FM_Check/section_9_4_9_7_magnitude_saturation_source_spectra_lab.html) | 随震源规模和震源谱变化，对比体波震级、面波震级和矩震级。 | [HTML](section_9_4_9_7_magnitude_saturation_source_spectra_lab.html) |

每个页面的页首都可以切换实验，也可以选择 **中文** 或 **English**。

## 主要功能

### 三维震源机制与赤平投影

- 三个联动视图显示断层错动、`NP1` 与 `NP2` 节面、P/T 轴、下半球地图投影，以及沿可选方位角绘制的 GMT `pscoupe` 风格垂直剖面。
- **解析并绘图**支持走向／倾角／滑动角、USGS 节面字符串、Global CMT 或 USGS 六分量矩张量，以及 P/T 轴方位角与倾伏角。
- 可选择断层预设、拖动角度滑块或启动**慢速自动演示**。**切换共轭节面**会互换两个节面，同时保持远场辐射图样和 P/T 轴。

### 第 9.1 节 · 格林函数与地震矩张量

- 通过图解了解点力脉冲响应、空间导数、双力偶，以及格林函数与震源时间函数的卷积。
- 选择预设、点击矩阵元素或调整六个独立分量，可联动观察力学图、下半球沙滩球和物理诊断。
- 激发脉冲并调整力源间距或台站方位角，可以比较示意波形。合成页显示六个加权基本响应及其总和，可调节离源角和脉冲宽度，并切换竖直、径向或横向分量。

### 第 9 章 · 地震与震源理论

- 对比单侧与双侧破裂、亚剪切与超剪切传播，观察四个方位上的位移脉冲。
- 查看 Brune 震源谱和震级饱和曲线，并在自相似标度模块中改变矩震级、应力降和介质刚度。
- 调整各向同性、双力偶及补偿线性矢量偶极（CLVD）分量，观察沙滩球和 Hudson 震源类型图的变化。
- 使用合成波形演示经验格林函数（EGF）反褶积，观察事件位置偏差、机制差异、噪声及水位正则化对恢复震源脉冲的影响。

### 第 9.4.2、9.5.1 与 9.7 节 · 震级饱和与震源谱

- 双图联动显示远场位移谱和 $m_b$、$M_S$、$M_W$ 曲线，可在 4.0 到 9.5 之间调整 $M_W$，并改变应力降或切换 Brune 与 Boatwright 模型。
- 对比 1 秒、20 秒的测量周期与破裂脉冲宽度，观察固定测量频带如何影响震级饱和。自相似标度页演示 Aki 标度律，以及在应力降固定时，拐角频率如何随地震矩增大而降低。
- 在根据 Shearer 教材表 9.1 编制的震例表中，可载入 1960 年智利、1964 年阿拉斯加、2004 年苏门答腊、2008 年汶川和 1992 年兰德斯地震，查看对应的震级和震源谱。

## 快速上手

1. **震源机制。** 输入 `210 / 32 / 90` 并点击**解析并绘图**，再点击**切换共轭节面**，观察两个节面互换后辐射图样是否变化。
2. **格林函数。** 在**九个基本力偶与矩张量**页选择**纯走滑断层**，然后调整一个矩张量分量，观察沙滩球如何变化。
3. **震源理论。** 在 **9.4.1 破裂方向性**页选择**单侧破裂**，用**点击发震演示**启动模拟，对比 0° 和 180° 方位的位移脉冲。
4. **震级饱和。** 对比 $M_W = 4.5$ 和 **1960 智利**预设，观察拐角频率相对 1 Hz 和 0.05 Hz 测量频带的位置。

## 本地运行

在现代浏览器中直接打开对应的 HTML 文件。`index.html` 对应震源机制实验。页面从 CDN 加载字体和库，震源机制实验的三维视图使用 WebGL。

GitHub Pages 从 `main` 分支的根目录发布上述 HTML 文件。

## 参考资料与致谢

震源理论相关实验参考 Peter M. Shearer 的《Introduction to Seismology》（第 2 版）第 9 章。波场和合成波形使用简化的教学模型。[教材目录](https://assets.cambridge.org/97805218/82101/toc/9780521882101_toc.pdf)

三维震源机制实验由 xcui1997 与 Gemini 共同设计并构建。[xcui1997 的 GitHub 主页](https://github.com/xcui1997)
