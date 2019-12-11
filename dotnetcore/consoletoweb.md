# 將.NET Core Console專案轉為ASP.NET Core專案

-  -  -  -  -

![](../images/MdMsAvvJIG_S1vvSjhd5xkyiiwmOKlzLmHu-g5h7voM.jpg)
- 在 .NET Core 中，無論是主控台應用程式、 ASP.NET Core 應用程式或是 .NET Core 3.0 才導入的WinForm和WPF程式的進入點都是Program類別的Main方法。

-  -  -  -  -

- 為了能夠更加理解什麼是ASP.NET Core，我們先來把剛剛建立的Console程式，轉換為ASP.NET Core程式...

![](../images/5TnUrAU.gif)

-  -  -  -  -

# 修改.csproj
- 將.csproj中的 `Microsoft.NET.Sdk` 改為 `Microsoft.NET.Sdk.Web` 。
```xml
<Project Sdk="Microsoft.NET.Sdk.Web">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.1</TargetFramework>
    <RootNamespace>dotnetcore_firstapp_training</RootNamespace>
  </PropertyGroup>
</Project>
```

-  -  -  -  -

# 修改Program.cs
- 將Program修改為連到網站，會回應Hello World!字樣。

```csharp
using System;
using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Hosting;
using Microsoft.AspNetCore.Http;
using Microsoft.Extensions.DependencyInjection;
using Microsoft.Extensions.Hosting;

namespace dotnetcore_firstapp_training
{
    public class Program
    {
        public static void Main(string[] args)
        {
            CreateHostBuilder(args).Build().Run();
        }

        public static IHostBuilder CreateHostBuilder(string[] args) =>
            Host.CreateDefaultBuilder(args)
                .ConfigureWebHostDefaults(webBuilder =>
                {
                    webBuilder.Configure(app => app.Run(context => context.Response.WriteAsync("Hello World!")));
                });
    }
}
```

-  -  -  -  -

# 試試Web版的Hello World程式

- 下指令 `dotnet run` 執行應用程式。
- 未特別設定時，預設網址是http://localhost:5000/ 和 https://localhost:5001/ ，連結到這兩個網址看看是否成功。

![](../images/Cg35dbl.gif)

-  -  -  -  -

# 新增Startup.cs檔案

- 在ASP.NET Core中，我們一般會把一些服務的注冊和要求處理管線的程式寫在Startup.cs。
- 現在先新增Startup.cs檔案在根目錄，並把剛剛回應Hello World!的程式碼移植到這個cs檔裡面。

-  -  -  -  -

- Startup.cs

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Hosting;
using Microsoft.AspNetCore.Http;
using Microsoft.Extensions.DependencyInjection;
using Microsoft.Extensions.Hosting;

namespace dotnetcore_firstapp_training
{
    public class Startup
    {
        public void ConfigureServices(IServiceCollection services)
        {
        }

        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            app.Run(context => context.Response.WriteAsync("Hello World!"));
        }
    }
}
```

- 修改Program中CreateHostBuilder方法，改為使用Startup

```csharp
        public static IHostBuilder CreateHostBuilder(string[] args) =>
            Host.CreateDefaultBuilder(args)
                .ConfigureWebHostDefaults(webBuilder =>
                {
                    webBuilder.UseStartup<Startup>();
                });
```

-  -  -  -  -

# 使用Routing和Endpoints Middleware

- 剛剛的寫法只要網址是在 http://localhost:5000 下，不管是 http://localhost:5000 或  http://localhost:5000/123 又或是 http://localhost:5000/123/abcd ，都會回傳Hello World!字樣，現在我們希望能夠改為：
  1. 當瀏覽 http://localhost:5000 時回傳Hello World!字樣。
  2. 瀏覽 http://localhost:5000 下的其他網址回傳404。

- 修改Startup的Configure方法

``` csharp
        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            app.UseRouting();
            app.UseEndpoints(endpoints =>
            {
                endpoints.MapGet("/", async context =>
                {
                    await context.Response.WriteAsync("Hello World!");
                });
            });
        }
```

-  -  -  -  -

