# .NET 10 C# File-based Apps 繁體中文 Demo

這是一個不需建置流程的純靜態單頁網站，介紹如何使用 .NET 10 直接執行單一 C# 檔案。

## 線上展示

GitHub Pages：<https://yazelin.github.io/dotnet10-csharp-file-demo/>

## 本機預覽

直接開啟 `index.html`，或執行：

```bash
python3 -m http.server 8080
```

然後前往 `http://localhost:8080`。

## GitHub Pages 部署

此專案包含 `.github/workflows/deploy-pages.yml`，推送到 `main` 後會透過 GitHub Actions 部署。

若第一次部署尚未啟用，請到 **Settings → Pages**，將 **Source** 設為 **GitHub Actions**。

## 內容

- `dotnet hello.cs` 單檔執行
- 命令列參數
- `#:package` 引用 NuGet
- `#:sdk Microsoft.NET.Sdk.Web` 單檔 Web API
- Linux／macOS shebang
- C# File-based Apps 適合 AI Agent 的情境
- Microsoft 官方參考連結
