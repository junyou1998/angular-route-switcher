# Angular Route Switcher

**Angular Route Switcher** is a UserScript tool designed for Angular developers. It automatically detects your application's routes and provides a floating, draggable UI to quickly switch between them.
<br>
**Angular Route Switcher** 是一個專為 Angular 開發者設計的 UserScript 工具。它能自動偵測應用程式中的路由，並提供一個可拖曳的懸浮介面，讓您快速切換頁面。

### Features / 核心功能

-   **Auto-Detection**: Automatically extracts routes from the Angular router configuration (requires `window.ng` in Dev Mode).
    <br> **自動偵測**：自動從 Angular 路由器配置中提取路由（需要在開發模式下使用，依賴 `window.ng`）。
-   **Floating & Draggable**: A floating action button that can be dragged and automatically snaps to screen edges.
    <br> **懸浮拖曳**：提供可拖曳的懸浮按鈕，並支援自動吸附至螢幕邊緣。
-   **Route Titles**: Displays route titles alongside paths for better clarity.
    <br> **路由標題**：在此清單中同時顯示路由路徑與標題，方便識別。
-   **Search**: Built-in search bar to filter routes by path or title.
    <br> **快速搜尋**：內建搜尋功能，可透過路徑或標題篩選路由。

### Installation / 安裝方式

1.  Install a UserScript manager like **Tampermonkey** or **Violentmonkey**.
    <br> 請先安裝 UserScript 管理器，例如 **Tampermonkey** 或 **Violentmonkey**。
2.  Install the script using the link below:
    <br> 點擊下方連結安裝腳本：
    <br> [Install from GreasyFork / 前往 GreasyFork 安裝](https://greasyfork.org/scripts/562323-angular-route-switcher)
3.  Open your local Angular application (e.g., `http://localhost:4200`).
    <br> 開啟您的本機 Angular 應用程式（例如 `http://localhost:4200`）。

### Usage / 使用說明

1.  Ensure your Angular app is running in **Development Mode**.
    <br> 確保您的 Angular 應用程式正運行於 **開發模式 (Development Mode)**。
2.  Click the floating "Explore" icon to open the route list.
    <br> 點擊畫面上的懸浮「探索」圖示以開啟路由清單。
3.  Click any item to navigate to that route.
    <br> 點擊任一項目即可跳轉至該路由。
