# ASP.NET Core

-  -  -  -  -

# ASP.NET Core
- ASP.NET Core 是一種跨平台且高效能的開放原始碼架構，用於建置現代化、雲端式、網際網路連線的應用程式。 利用 ASP.NET Core，可以：
  1. 建置 Web 應用程式和服務、IoT 應用程式，以及行動後端。
  2. 在 Windows、macOS 和 Linux 上使用您最愛的開發工具。
  3. 部署到雲端或在內部部署。
  4. 在 .NET Core 或 .NET Framework 上執行。

-  -  -  -  -

# 為什麼要重新設計 ASP.NET Core
- 數百萬的開發人員已使用 (並持續使用) ASP.NET 4.x 來建立 Web 應用程式。ASP.NET Core 是 ASP.NET 4.x 的重新設計，其架構變更可產生更為精簡且更加模組化的架構。

-  -  -  -  -

# ASP.NET Core 的優點（一）
- 能夠在 Windows、macOS 和 Linux 上開發並執行。
- 輕量型、高效能且模組化的 HTTP 要求管線。
- 開放原始碼和社群導向。
- 內建的相依性注入。
- 可測試性架構。
- 可簡化現代網頁程式開發的工具。
- 並存版本控制。
- 整合現代化用戶端架構和開發工作流程。
- 支援使用gRPC裝載遠端程序呼叫（RPC）服務。

-  -  -  -  -

# ASP.NET Core 的優點（二）
- 雲端就緒、以環境為基礎的組態系統。
- 能夠裝載于下列各項：
  - Kestrel
  - IIS
  - HTTP.sys
  - Nginx
  - Apache
  - Docker
- 用於建置 Web UI 和 Web API 的統一劇本。
- Razor Pages 更容易撰寫以頁面為焦點的案例程式碼，也更具生產力。
- Blazor 可讓您在瀏覽器中使用 C# 與 JavaScript。 共用伺服器端與用戶端應用程式邏輯都是以 .NET 撰寫。

-  -  -  -  -

# ASP.NET Core 或 ASP.NET？
- 下表將比較 ASP.NET Core 與 ASP.NET 4.x。
<escape>
    <table>
        <thead>
            <tr><th>ASP.NET Core</th><th>ASP.NET 4.x</th></tr>           
        </thead>
        <tbody>
            <tr><td>為 Windows、macOS 或 Linux 建置</td><td>為 Windows 建置</td></tr><tr><td>從 ASP.NET Core 2.x 開始，Razor 頁面是建立 Web UI 的建議方法。 另請參閱MVC、 Web API和SignalR。</td><td>使用Web Forms、 SignalR、 MVC、 web API、 webhook或Web Pages</td></tr><tr><td>每部電腦多個版本</td><td>每部電腦一個版本</td></tr><tr><td>在 Visual Studio、Visual Studio for Mac 或 Visual Studio Code 中使用 C# 或 F# 進行開發</td><td>在 Visual Studio 中使用 C#、VB 或 F# 進行開發</td></tr><tr><td>效能比 ASP.NET 4.x 更高</td><td>效能良好</td></tr><tr><td>使用 .NET Core 執行階段</td><td>使用 .NET Framework 執行階段</td></tr>
        </tbody>
    </table><!-- .element style="font-size: 0.5em;" -->
</escape>

