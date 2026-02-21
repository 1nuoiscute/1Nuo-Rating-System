# 1Nuo-Rating-System 🧭

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Online-blue?style=for-the-badge&logo=googlechrome&logoColor=white)](https://www.1nuo.me/rate/)
[![简体中文](https://img.shields.io/badge/Language-简体中文-red?style=for-the-badge)](README.md)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://github.com/1nuoiscute/1Nuo-Rating-System/blob/main/LICENSE)

A dedicated quantitative evaluation tool for static blogs. It leverages a visual management backend to drive the GitHub API for real-time JSON updates, achieving seamless cloud synchronization with zero server overhead. Equipped with a weighted scoring engine and interactive ECharts visualization, it is tailor-made for bloggers seeking professional auditing and low-maintenance workflows.

<p align="center">
<img src="https://img.1nuo.me/blog/2026/02/21/QQ_1771685190048.webp" width="48%" />
<img src="https://img.1nuo.me/blog/2026/02/21/QQ_1771685210856.webp" width="48%" />
</p>

## 💡 Why this project?
This project transforms structured data into multi-dimensional visual dashboards. Through interactive charts and a robust filtering/search system by region or rating, it provides logical depth and intuitive presentation for otherwise fragmented records.

For static blog users (Hexo/Hugo/Jekyll), manually editing thousands of lines in `.json` databases is error-prone and inefficient. This tool decouples "Data Entry" from "Code Maintenance," allowing you to update content directly through a web-based GUI.

## 🛠️ Key Features

### 🎨 Frontend (Display / `index.md`)
* **Data Dashboard (ECharts)**: Automatically aggregates global data via **ECharts** to generate average score boards and visualize rating trends.
* **Multi-dimensional Filtering**: Real-time search by region or keyword, with dynamic sorting by comprehensive score or visitation time.
* **Standardized Rating Cards**: Clear presentation of **S/A/B/C** grades, individual dimension score bars, and tags.
* **Attraction Collider (PK Mode)**: Side-by-side comparison of two projects in the same coordinate system for visual data "battles."
* **Deep/Shallow Linkage**: Seamlessly jump from rating cards to in-depth review pages or interactive summary popups.

### ⚙️ Backend (Management / `index.html`)
* **Visual Management Center**: A complete GUI form interface supporting the **File System Access API** for direct local `.json` read/write.
* **GitHub API Cloud Sync**: Integrated GitHub API logic to push data updates directly to remote repositories for zero-server maintenance.
* **Automated Weighting Engine**: A built-in 4-dimensional weighting model that automatically calculates final scores and grades based on base inputs.
* **Smart Text Processing**: Automatic cleaning of Markdown image links and formatting of indentation for reviews.

## 📐 Evaluation Model

The system utilizes a weighted algorithm to ensure the rigor of evaluation standards:

$$Final\ Score = \sum (Score_i \times Weight_i) + Bonus_{tags}$$

**Current weights for "Attractions":**
* **Architectural Impact (25%)**: Measuring aesthetics and visual power.
* **Cultural Resonance (30%)**: Evaluating historical depth and emotional weight.
* **Visitation Experience (25%)**: Quantifying service flow and on-site atmosphere.
* **Price-to-Value (20%)**: ROI assessment based on scale vs. cost.

Of course, you can customize the weights and dimension names according to your preferences beyond just travel attractions.

## 🚀 Quick Start

1.  **Link Local**: Click "Link Local" and select your `rate_data.json` file.
2.  **Config Cloud**: Expand "Cloud Sync Settings," enter your GitHub Username, Repo name, and **Personal Access Token**.
3.  **Start Rating**: Fill in the data and click "Local Write" or "Cloud Sync".

## 📄 License
Licensed under the **MIT License**.
