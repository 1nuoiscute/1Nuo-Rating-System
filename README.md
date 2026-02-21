# 1Nuo-Rating-System
[![Live Demo](https://img.shields.io/badge/Live%20Demo-在线演示-blue?style=for-the-badge&logo=googlechrome&logoColor=white)](https://www.1nuo.me/rate/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://github.com/1nuoiscute/1Nuo-Rating-System/blob/main/LICENSE)

一个静态博客专用的量化评测管理工具。通过可视化后台直接驱动 GitHub API 更新 JSON 数据，实现零服务器成本的云端同步。内置加权评分引擎与 ECharts 可视化看板，专为追求量化评测、轻代码维护的博主打造。

<p align="center">
<img src="https://img.1nuo.me/blog/2026/02/21/QQ_1771685190048.webp" width="48%" />
<img src="https://img.1nuo.me/blog/2026/02/21/QQ_1771685210856.webp" width="48%" />
</p>

## 💡 为什么做这个？
本主页将结构化的数据转化为多维的可视化看板，通过交互式图表与按地域或评分筛选和搜索系统，让原本琐碎的记录具备逻辑深度与直观表现。

在维护静态博客（如 Hexo/Hugo）的评测页面时，手动修改成百上千行的 `.json` 数据库极易出错且效率低下。本工具将“数据输入”与“代码维护”分离，让你在网页里即可更新内容。

## 🛠️ 核心功能

### 🎨 呈现端 (Frontend / `index.md`)
* **评分看板 (ECharts)**：基于 **ECharts** 自动提取全局数据，生成各维度的平均分看板，直观展示评价走势。
* **多维过滤系统**：支持按地区、关键词进行实时检索，并可根据综合得分或游玩时间进行动态排序。
* **标准化量化卡片**：清晰展示 **S/A/B/C** 评级、单项维度得分条及标签，实现评价结果的标准化呈现。
* **景点对撞机 (PK Mode)**：支持在不同项目间开启“对撞”模式，在同一坐标系下进行多维度数据对比与博弈。
* **深/浅评价跳转**：支持从量化卡片直接跳转至深度评测页面或交互式简评弹窗，实现信息获取的无缝衔接。

### ⚙️ 管理端 (Backend / `index.html`)
* **可视化管理中心**：提供完整的 GUI 表单界面，支持通过 **File System Access API** 直接读写本地 `.json` 文件。
* **GitHub API 云端同步**：集成 GitHub API 逻辑，填表即可直接将数据更新推送至远端仓库，实现零服务器维护。
* **自动化加权引擎**：内置四维度加权评分模型，只需填入基准分即可自动计算最终分值与等级。
* **智能文本处理**：自动清洗粘贴进入的 Markdown 图片链接格式，并为简评心得自动添加格式化缩进。

## 📐 评价模型

系统采用加权算法生成最终得分，确保评价标准的严谨性：

$$Final\ Score = \sum (Score_i \times Weight_i) + Bonus_{tags}$$

目前的 **“景点模式”** 权重分配如下：
* **建筑视觉 (25%)**：衡量建筑美学与视觉冲击力。
* **文化共鸣 (30%)**：挖掘历史积淀与情感权重。
* **游览体验 (25%)**：量化服务流程与现场感受。
* **质价比 (20%)**：基于项目体量与成本的评估。

当然，你可以根据你的喜好自行调节权重名称与占比，也不仅仅局限于旅游景点测评。
## 🚀 快速上手

1. **关联本地**：点击“关联本地”，选中你的 `rate_data.json` 文件。
2. **配置云端**：展开“云端同步设置”，填入 GitHub 用户名、仓库名及 **Personal Access Token**。
3. **开始评测**：填入数据后点击“本地写入”或“云端同步”即可。

## 📄 开源协议
基于 **MIT License** 开源。
