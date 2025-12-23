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


## 📘 User Guide | 使用指南

### 1️⃣ Select a Province | 选择省份

**English**

- Click a province directly on the map  
  **OR**
- Click a province name from the scrollable list on the left
- The selected province will be highlighted and displayed at the top

**中文**

- 可直接点击地图上的省份  
  **或**
- 从左侧省份列表中点击选择
- 当前选中省份会在地图中高亮，并显示在顶部提示栏

---

### 2️⃣ Switch Map Mode | 切换地图模式

**English**

- `Color Mode`: Province is filled with solid color
- `Pattern Mode`: Province is filled with SVG texture

**中文**

- `Color Mode`：使用纯色填充省份
- `Pattern Mode`：使用 SVG 纹理填充省份

---

### 3️⃣ Choose Texture Type | 选择纹理类型（Pattern Mode）

**Available Types | 可选类型**

- **Dot**：点阵纹理
- **Line**：线条纹理
- **Grid**：网格纹理

**English**

- Select a texture type using radio buttons
- The selected province updates immediately

**中文**

- 通过单选按钮选择纹理类型
- 当前省份纹理会实时更新

---

### 4️⃣ Rotate Texture | 旋转纹理

**English**

- Use the **Rotation slider (0–180°)** to rotate the texture
- Rotation only applies to the currently selected province

**中文**

- 使用 **Rotation 滑块（0–180°）** 调整纹理角度
- 仅作用于当前选中省份

---

### 5️⃣ Clear Selection | 清除选择

**English**

- Click **Clear Choice** to reset:
  - Selected province
  - Applied texture or color

**中文**

- 点击 **Clear Choice**
- 重置：
  - 当前选中省份
  - 所有纹理 / 颜色设置

---

## 🧠 Implementation Overview | 实现原理简述

### English

- Uses **D3.js** to render provinces from TopoJSON
- Each province has its own SVG `<pattern>` definition
- Patterns are dynamically updated (type & rotation)
- `patternTransform: rotate(angle)` controls rotation

### 中文

- 使用 **D3.js** 渲染 TopoJSON 省级地图
- 为每个省份生成独立 SVG `<pattern>`
- 通过动态更新 pattern 内容切换纹理类型
- 使用 `patternTransform: rotate(angle)` 实现旋转

---

## 🗺️ Map Data | 地图数据

**Source | 数据来源**

- Natural Earth

**Processing Pipeline | 处理流程**

1. Shapefile → NDJSON
2. Filter China provinces
3. Merge GeoJSON
4. Convert to TopoJSON
5. Quantize for file size reduction

**Final File | 最终文件**

```text
china_topo_quantized.json
