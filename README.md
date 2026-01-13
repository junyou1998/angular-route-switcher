<div align="center">

# 🚀 Angular Route Switcher

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/junyou1998/angular-route-switcher/blob/main/LICENSE)
[![GreasyFork](https://img.shields.io/badge/GreasyFork-Install-red.svg)](https://greasyfork.org/scripts/562323-angular-route-switcher)
![Version](https://img.shields.io/badge/version-1.3-green.svg)

**Angular Route Switcher** is a UserScript tool designed for Angular developers.<br>It automatically detects your application's routes and provides a floating, draggable UI to quickly switch between them.

**Angular Route Switcher** 是一個專為 Angular 開發者設計的 UserScript 工具。<br>它能自動偵測應用程式中的路由，並提供一個可拖曳的懸浮介面，讓您快速切換頁面。

</div>

---

### ✨ Features / 核心功能

-   **Auto-Detection**: Automatically extracts routes from the Angular router configuration (requires `window.ng` in Dev Mode).
    <br> **自動偵測**：自動從 Angular 路由器配置中提取路由（需要在開發模式下使用，依賴 `window.ng`）。
-   **Floating & Draggable**: A floating action button that can be dragged and automatically snaps to screen edges.
    <br> **懸浮拖曳**：提供可拖曳的懸浮按鈕，並支援自動吸附至螢幕邊緣。
-   **Route Titles**: Displays route titles alongside paths for better clarity.
    <br> **路由標題**：在此清單中同時顯示路由路徑與標題，方便識別。
-   **Search**: Built-in search bar to filter routes by path or title.
    <br> **快速搜尋**：內建搜尋功能，可透過路徑或標題篩選路由。

### 📦 Installation / 安裝方式

1.  Install a UserScript manager like **[Tampermonkey](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=zh-TW)** or **Violentmonkey**.
    <br> 請先安裝 UserScript 管理器，例如 **[Tampermonkey](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=zh-TW)** 或 **Violentmonkey**。
2.  Install the script using the link below:
    <br> 點擊下方連結安裝腳本：
    <br> [Install from GreasyFork / 前往 GreasyFork 安裝](https://greasyfork.org/scripts/562323-angular-route-switcher)
3.  Open your local Angular application (e.g., `http://localhost:4200`).
    <br> 開啟您的本機 Angular 應用程式（例如 `http://localhost:4200`）。

### 🎮 Usage / 使用說明

1.  Ensure your Angular app is running in **Development Mode**.
    <br> 確保您的 Angular 應用程式正運行於 **開發模式 (Development Mode)**。
2.  Click the floating "Explore" icon to open the route list.
    <br> 點擊畫面上的懸浮「探索」圖示以開啟路由清單。
3.  Click any item to navigate to that route.
    <br> 點擊任一項目即可跳轉至該路由。

### 🛠️ How It Works / 原理與實作

This tool leverages the debugging APIs exposed by Angular in **Development Mode**.
<br> 本工具利用了 Angular 在 **開發模式** 下暴露的除錯 API 來運作。

1.  **Accessing Angular Context / 取得 Angular Context**:
    It looks for the `window.ng` object and uses `ng.getComponent()` to retrieve the root component instance of your application.
    <br> 腳本會尋找 `window.ng` 物件，並使用 `ng.getComponent()` 來取得應用程式的根元件實例。

2.  **Extracting Routes / 提取路由**:
    Once the root component (or the Router instance) is found, it traverses the `router.config` to build a flat list of all available routes.
    <br> 找到根元件（或 Router 實例）後，它會遍歷 `router.config` 來建構一個完整的可用路由清單。

3.  **Navigation / 路由切換**:
    When you click a route, it calls the Angular Router's `navigateByUrl()` method directly. This ensures a seamless page transition without triggering a full page reload, just like a native Angular navigation.
    <br> 當您點擊路由時，它會直接呼叫 Angular Router 的 `navigateByUrl()` 方法。這能確保頁面切換順暢且不需重新載入整頁，就如同原生的 Angular 導航一樣。
