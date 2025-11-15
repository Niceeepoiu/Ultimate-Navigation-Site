# 🧭 极致导航站 (Ultimate Navigation Site)

<a id="chinese-version"></a>
## 🇨🇳 中文版

[**English Version**](#english-version)

### 简介

这是一个基于 HTML、Tailwind CSS 和原生 JavaScript 构建的极简主义导航网站。它旨在提供一个快速、清晰、响应式的资源链接管理和搜索平台，特别优化了侧边栏分类的交互体验和移动端适配。

### ✨ 主要功能

* **动态侧边栏分类**:
    * 根据 `data.json` 动态生成无限级分类导航树。
    * **独立箭头点击**: 分类名称旁的箭头可独立点击，仅用于展开/收起子分类，不会触发资源筛选。
    * **独立分类点击**: 点击分类名称区域，只会筛选并显示该分类及其子分类下的资源，不会自动展开子分类。
    * **无子分类不显示箭头**：如果分类下没有子分类，则不显示展开箭头，保持界面简洁。
* **移动端优化**:
    * 通过汉堡菜单（<i class="fas fa-bars"></i>）控制侧边栏的收展。
    * 侧边栏展开时，背景变暗并添加遮罩，用户可点击遮罩层或切换分类后自动隐藏侧边栏。
* **资源搜索**: 顶部集成快速搜索框，支持对资源标题和描述进行实时过滤。
* **动态内容加载**: 资源数据与页面结构分离，通过 `data.json` 文件管理所有链接。

### ⚙️ 技术栈

* **HTML5**: 基础结构
* **Tailwind CSS**: 快速构建响应式界面的原子化 CSS 框架
* **JavaScript (ES6+)**: 处理动态加载、分类筛选和交互逻辑
* **Font Awesome**: 图标库

### 🚀 安装与运行

本项目是一个纯前端应用，无需任何后端环境即可运行。

1.  **准备数据文件 (`data.json`)**

    确保您的 `data.json` 文件位于项目根目录，并遵循资源配置结构。

    ```json
    [
      {
        "name": "分类A",
        "type": "category",
        "icon": "fa-solid fa-star", 
        "children": [
          {
            "title": "资源标题",
            "url": "[https://example.com](https://example.com)",
            "description": "这是资源的描述信息。",
            "type": "resource"
          }
        ]
      }
    ]
    ```

2.  **运行**

    直接使用浏览器打开 `index.html` 文件即可。

    > ⚠️ **注意**: 推荐使用 VS Code 的 **Live Server** 扩展或任何本地 Web 服务器（如 `http-server`）来运行项目，以避免本地文件访问的跨域问题。

***

<a id="english-version"></a>
## 🇬🇧 English Version

[**中文版**](#chinese-version)

### Introduction

This is a minimalist navigation website built purely with HTML, Tailwind CSS, and native JavaScript. It is designed to offer a fast, clean, and responsive platform for managing and searching resource links, with a focus on optimizing the interactive experience of the sidebar categories and mobile adaptability.

### ✨ Key Features

* **Dynamic Sidebar Categories**:
    * Generates an infinite-level category navigation tree dynamically from `data.json`.
    * **Independent Arrow Click**: The arrow next to the category name can be clicked independently to only expand/collapse subcategories without triggering resource filtering.
    * **Independent Category Click**: Clicking the category name area will only filter and display resources under that category and its subcategories, without automatically expanding the subcategories.
    * **No Arrow for No Children**: If a category has no subcategories, the expand arrow is not displayed, ensuring a clean interface.
* **Mobile Optimization**:
    * Sidebar visibility is controlled by a hamburger menu button (<i class="fas fa-bars"></i>).
    * When the sidebar is open, a darkened backdrop is shown, and the user can click the backdrop or select a category to automatically hide the sidebar.
* **Resource Search**: A quick search box is integrated at the top, supporting real-time filtering of resource titles and descriptions.
* **Dynamic Content Loading**: Resource data is separated from the page structure and managed via the `data.json` file for easy maintenance and updates.

### ⚙️ Technology Stack

* **HTML5**: Base structure
* **Tailwind CSS**: Atomic CSS framework for rapid and responsive UI development
* **JavaScript (ES6+)**: Handles dynamic loading, category filtering, and interaction logic
* **Font Awesome**: Icon library

### 🚀 Setup and Running

This project is a pure frontend application and requires no backend environment to run.

1.  **Prepare the Data File (`data.json`)**

    Ensure your `data.json` file is in the root directory of the project and follows the resource configuration structure:

    ```json
    [
      {
        "name": "Category A",
        "type": "category",
        "icon": "fa-solid fa-star", 
        "children": [
          {
            "title": "Resource Title",
            "url": "[https://example.com](https://example.com)",
            "description": "This is the description of the resource.",
            "type": "resource"
          }
        ]
      }
    ]
    ```

2.  **Running the Project**

    You can open the `index.html` file directly in your web browser.

    > ⚠️ **Note**: It is highly recommended to run the project using the **Live Server** extension in VS Code or any local web server (e.g., `http-server`) to avoid cross-origin issues with local file access (CORS).