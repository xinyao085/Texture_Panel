# China Map Texture Panel  
中国地图纹理设计面板

A **D3.js + SVG Pattern** based interactive map tool for designing and previewing texture fills on Chinese provincial maps.  
一个基于 **D3.js + SVG Pattern** 的中国省级地图纹理设计与交互示例项目。

---

## ✨ Features | 功能特性

### English
- 🗺️ Interactive map of Chinese provinces (including Hong Kong, Macao, Taiwan)
- 🎨 Two rendering modes: Color Mode & Pattern Mode
- 🧩 Multiple texture types: Dot, Line, Grid
- 🔄 Real-time pattern rotation
- 📜 Scrollable province list with map synchronization
- 🧹 Clear selection with one click

### 中文
- 🗺️ 中国省级行政区交互式地图（含港澳台）
- 🎨 支持颜色模式与纹理模式切换
- 🧩 多种纹理类型：点阵 / 线条 / 网格
- 🔄 支持纹理实时旋转
- 📜 省份列表与地图高亮联动
- 🧹 一键清除当前选择状态

---

## 📁 Project Structure | 项目结构

```text
.
├── Texture_Panel.html          # Entry HTML, DOM structure & UI logic
│                              # 项目入口，页面结构与事件监听
├── style.css                   # Layout & interaction styles
│                              # 页面布局、地图与交互样式
├── texturePatten.js            # Core logic: SVG patterns & map interaction
│                              # 核心逻辑：纹理定义、更新与地图交互
└── json/
    └── china_topo_quantized.json  # China provincial TopoJSON data
                                   # 中国省级 TopoJSON 数据（压缩）
