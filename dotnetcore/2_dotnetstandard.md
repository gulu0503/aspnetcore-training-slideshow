# .NET Standard

-  -  -  -  -

# .NET Standard（一）
- .NET Standard 是計劃在所有 .NET 實作提供的 .NET API 型式規格。 
- .NET Standard 背後的動機是在 .NET 生態系統中建立更高的一致性。

> 可攜式的程式庫（PCL）在最新版本的 Visual Studio 中視為已被取代。新的專案應該直接使用 .NET Standard 程式庫來存取較大的 API 介面區。

-  -  -  -  -

# .NET Standard（二）
- .NET Standard 支援下列重要案例：
  1. 定義一致的 BCL API 集合，以供所有 .NET 實作來實作，而不論工作負載為何。
  2. 可讓開發人員使用這組相同的 API，產生可跨 .NET 實作使用的可攜式程式庫。
  3. 減少或甚至排除因 .NET API 而必須對共用原始檔進行的條件式編譯，僅適用於 OS API。

-  -  -  -  -

<!-- .slide: class="fortable" -->
# .NET 實作支援
下表列出支援每個 .NET Standard 版本的最低平台版本：
<escape>
<table>
<thead>
<tr>
<th>.NET 標準</th>
<th>1</th>
<th>1.1</th>
<th>1.2</th>
<th>1.3</th>
<th>1.4</th>
<th>1.5</th>
<th>1.6</th>
<th>2</th>
<th>2.1</th>
</tr>
</thead>
<tbody><tr>
<td>.NET Core</td>
<td>1</td>
<td>1</td>
<td>1</td>
<td>1</td>
<td>1</td>
<td>1</td>
<td>1</td>
<td>2</td>
<td>3</td>
</tr>
<tr>
<td>.NET Framework</td>
<td>4.5</td>
<td>4.5</td>
<td>4.5.1</td>
<td>4.6</td>
<td>4.6.1</td>
<td>4.6.1</td>
<td>4.6.1</td>
<td>4.6.1</td>
<td>不適用</td>
</tr>
<tr>
<td>Mono</td>
<td>4.6</td>
<td>4.6</td>
<td>4.6</td>
<td>4.6</td>
<td>4.6</td>
<td>4.6</td>
<td>4.6</td>
<td>5.4</td>
<td>6.4</td>
</tr>
<tr>
<td>Xamarin.iOS</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>10.14</td>
<td>12.16</td>
</tr>
<tr>
<td>Xamarin.Mac</td>
<td>3</td>
<td>3</td>
<td>3</td>
<td>3</td>
<td>3</td>
<td>3</td>
<td>3</td>
<td>3.8</td>
<td>5.16</td>
</tr>
<tr>
<td>Xamarin.Android</td>
<td>7</td>
<td>7</td>
<td>7</td>
<td>7</td>
<td>7</td>
<td>7</td>
<td>7</td>
<td>8</td>
<td>10</td>
</tr>
<tr>
<td>通用 Windows 平台</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>10.0.16299</td>
<td>10.0.16299</td>
<td>10.0.16299</td>
<td>TBD</td>
</tr>
<tr>
<td>Unity</td>
<td>2018.1</td>
<td>2018.1</td>
<td>2018.1</td>
<td>2018.1</td>
<td>2018.1</td>
<td>2018.1</td>
<td>2018.1</td>
<td>2018.1</td>
<td>TBD</td>
</tr>
</tbody></table>
</escape>