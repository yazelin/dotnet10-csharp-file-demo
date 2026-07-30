# C#，終於可以從一個檔案開始

.NET 10 少掉的不是一個專案檔，而是一道讓很多人懶得開始的門檻。

我第一次看到 File-based Apps 時，想到的不是教學，而是那些原本會用 Python 隨手寫掉的小工具。C# 終於也能進入那個位置。

## 一個小改動，改的是使用習慣

過去要寫一小段 C#，你通常先建立專案、看見資料夾、處理專案檔。這些步驟沒有錯，只是對一個五分鐘就能寫完的工具來說，顯得太正式。

.NET 10 的 File-based Apps 把這段儀式拿掉了。你可以直接建立 `hello.cs`，寫下一行程式，再用 `dotnet hello.cs` 執行。

它仍然是編譯過的 .NET 程式，不是把 C# 變成另一種 Python。差別在於，使用者不必先感受到「我正在開一個專案」。

> 真正的改變不是少打一個指令，而是 C# 開始適合那些不值得建立專案的工作。

## 先跑起來，再決定要不要長大

1. 安裝 .NET 10 SDK。
2. 建立 `hello.cs`。
3. 執行 `dotnet hello.cs`。

```csharp
Console.WriteLine("Hello from C# File-based Apps!");
```

```bash
dotnet hello.cs
# Hello from C# File-based Apps!
```

## 它不是只有 Hello World

### 直接引用 NuGet

```csharp
#:package Spectre.Console@*
using Spectre.Console;

AnsiConsole.MarkupLine("[green]Ready![/]");
```

### 單檔 Web API

```csharp
#:sdk Microsoft.NET.Sdk.Web

var app = WebApplication.Create(args);
app.MapGet("/", () => "Hello API");
app.Run();
```

## 給 AI Agent 的 C# 入口

Agent 常常只需要生成一個小工具：讀 JSON、整理 CSV、打一個 API，或重用公司既有的 .NET 類別庫。這些工作不需要一個宏大的專案。

適合的情境包括資料轉換、CLI、一次性維運工具、REST API 整合，以及企業內部 .NET 系統周邊工具。

它不會取代 Python。Notebook、資料科學、PyTorch 與研究生態仍是 Python 的主場。C# 的優勢比較明確：既有 .NET 系統、強型別與企業整合。

## 官方資料

- [檔案型應用程式](https://learn.microsoft.com/zh-tw/dotnet/core/sdk/file-based-apps)
- [File-based programs 教學](https://learn.microsoft.com/zh-tw/dotnet/csharp/fundamentals/tutorials/file-based-programs)
- [官方公告](https://devblogs.microsoft.com/dotnet/announcing-dotnet-run-app/)

## Sitemap

- [HTML 文章](https://yazelin.github.io/dotnet10-csharp-file-demo/)
- [原始碼](https://github.com/yazelin/dotnet10-csharp-file-demo)
