[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

<div align="center">

## Deno: 改善Node.js十大技術債的新JavaScript runtime(JS執行環境)

<a href="https://deno.com/blog/v1" target="blank"><img align="center" src="https://deno.com/blog/v1/cover_wide.jpg" alt="Deno"></a>

</div>

---

### 主要非常非常地簡單介紹一下Deno這個JS Runtime。


> 前言: JS執行環境除了常聽到的Node.js(2009 年推出)之外，還有後來的Bun(2022年推出，同樣也是要改善Node.js的缺點所誕生Runtime + 多合一工具包)，以及要來討論的主角: Deno(2018年推出) 😍😍😍😍😍(冷靜...。


<details open>
  <summary>
	關於Bun的相關資訊
  </summary>

  - [官網](https://bun.sh/)
  - [Github](https://github.com/oven-sh/bun)
  - 開發者: [Jarred Sumner](https://github.com/Jarred-Sumner)
  - [原生支援 TypeScript](https://bun.sh/docs/runtime/typescript)
	> 以往Node.js使用TS需使用其他套件(如: [ts-node](https://github.com/TypeStrong/ts-node) )，或編譯器(如: [tsc](https://nodejs.org/en/learn/getting-started/nodejs-with-typescript#examples ))去轉成JS執行
  - [使用Safari的JavaScriptCore引擎](https://developer.apple.com/documentation/javascriptcore)
  - 2023年9月份終於推出1.0正式版本:
    - [官方Blog](https://bun.sh/blog/bun-v1.0)
    - [Github Releases](https://github.com/oven-sh/bun/releases/tag/bun-v1.0.0)
    - [JavaScript執行環境Bun 1.0推出，可達Node.js的5倍速](https://www.ithome.com.tw/news/158705)
    - [A Quick Look at Bun 1.0 – The Node.js Alternative](https://www.freecodecamp.org/news/a-quick-look-at-bun-js/)
 - [Bun 是什麼? 為什麼要用 Bun? 它解決了哪些 Node.js 的問題?](https://www.explainthis.io/zh-hant/swe/what-is-bun)
 - [Bun vs Node.js](https://123davidbill.medium.com/%E7%AD%86%E8%A8%98-bun-vs-node-js-632b3a87e6a7)

 </details>

<details open>
  <summary>
	Deno是什麼?
  </summary>

  - [官網](https://deno.com/)
  - [Github](https://github.com/denoland/deno)
  - 與Node.js同開發者: [Ryan Dahl](https://tinyclouds.org/)
  - [原生支援 TypeScript](https://docs.deno.com/runtime/manual/advanced/typescript/overview)
  - [與Node.js一樣使用[V8引擎](https://v8.dev/ )、以及[Rust語言](https://www.rust-lang.org/zh-TW )所構建的執行環境(Node.js使用C++)]
  - Deno Land(Deno的雲端Library、Modules)
    - Deno最大的特點就是引入模組不再過度依賴npm下載套件然後建立又肥又複雜的node_module目錄了，可使用CDN從雲端函式庫去引入，當然要[使用npm](https://docs.deno.com/runtime/manual/node) 還是可以的。
    - [Deno Standard Modules](https://deno.land/std): 標準函式庫
    - [Deno Third Party Modules](https://deno.land/x): 第三方函式庫
  - [Deno Deploy](https://deno.com/deploy): JavaScript應用的全球分散式serverless雲端平台，我自己的[網站](https://rexfox.deno.dev/ )也是架設在上面，速度非常快
    - [文檔](https://docs.deno.com/deploy/manual)
  - [Deno KV](https://docs.deno.com/kv/manual): Key-Value資料庫(NoSQL)
  - ✨ : JSConf EU 2018 歐洲大會演講(6月初): [我爲Node.js感到後悔的十件事](https://www.youtube.com/watch?v=M3BM9TB-8yA)
    - [演講簡報](https://tinyclouds.org/jsconf2018.pdf)
  - ✨ : 來台演講JSDC 2018(11月，富邦人壽大樓國際會議中心): [Deno，A New Server-Side Runtime By Ryan Dahl](https://www.youtube.com/watch?v=FlTG0UXRAkE&list=PL8dIIwCMF-SP9LpiqVypGKHLaGNm8vQ29)
  - [演講筆記](https://hackmd.io/c/JSDC2018/%2FYByw2CjTTeyRNXIbONNrcg)
  - Deno如何償還Node.js十大技術債:
    - [（上）](https://www.ithome.com.tw/news/128189)
    - [（下）](https://www.ithome.com.tw/news/128190)
  - 😂 : [求不要更新了，老子学不动了](https://github.com/denoland/deno/issues/25)
  - [Deno 入門指南](https://ianchen0119.gitbook.io/deno/)
    - [Deno 跟 Node.js 的主要差異](https://ianchen0119.gitbook.io/deno/an-zhuang-bing-shi-yong-deno/deno-gen-node.js-de-zhu-yao-cha-yi)
  - [初探 Deno — 與 Node.js 的淺比較(IT鐵人賽)](https://ithelp.ithome.com.tw/articles/10250363)

</details>

<details open>
  <summary>
	✨ : 讓Ryan Dahl懊悔不已的Node.js十大技術債[ [取自Deno如何償還Node.js十大技術債（上）](https://www.ithome.com.tw/news/128189) ]
  </summary>

  - 沒用JavaScript非同步處理的Promise物件。
  - 低估安全的重要。
  - 採用gyp來設計Build系統。
  - 沒有聽大家建議提供FFI而繼續用gyp。
  - 過度依賴npm（內建package.json支援）。
  - 太容易可require("任意模組")。
  - package.json建立錯誤的模組概念（在同一目錄下的檔案就是同一模組）。
  - 又肥又複雜的node_module設計和下載黑洞（往往下載npm得花上非常久的時間）。
  - require("module")時沒有強制加上.js附加檔名。
  - 無用的index.js設計。

</details>

---

## License
**[MIT](https://github.com/Lin-Rexter/AI_Hub_Discord-Bot/blob/1902f8e112c3e682ab041c39864d8bb8c7f78a24/LICENSE)**