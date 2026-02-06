# 初學者資料科學課程大綱

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=344191198)

[![GitHub license](https://img.shields.io/github/license/microsoft/Data-Science-For-Beginners.svg)](https://github.com/microsoft/Data-Science-For-Beginners/blob/master/LICENSE)
[![GitHub contributors](https://img.shields.io/github/contributors/microsoft/Data-Science-For-Beginners.svg)](https://GitHub.com/microsoft/Data-Science-For-Beginners/graphs/contributors/)
[![GitHub issues](https://img.shields.io/github/issues/microsoft/Data-Science-For-Beginners.svg)](https://GitHub.com/microsoft/Data-Science-For-Beginners/issues/)
[![GitHub pull-requests](https://img.shields.io/github/issues-pr/microsoft/Data-Science-For-Beginners.svg)](https://GitHub.com/microsoft/Data-Science-For-Beginners/pulls/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

[![GitHub watchers](https://img.shields.io/github/watchers/microsoft/Data-Science-For-Beginners.svg?style=social&label=Watch)](https://GitHub.com/microsoft/Data-Science-For-Beginners/watchers/)
[![GitHub forks](https://img.shields.io/github/forks/microsoft/Data-Science-For-Beginners.svg?style=social&label=Fork)](https://GitHub.com/microsoft/Data-Science-For-Beginners/network/)
[![GitHub stars](https://img.shields.io/github/stars/microsoft/Data-Science-For-Beginners.svg?style=social&label=Star)](https://GitHub.com/microsoft/Data-Science-For-Beginners/stargazers/)


[![Microsoft Foundry Discord](https://dcbadge.limes.pink/api/server/nTYy5BXMWG)](https://discord.gg/nTYy5BXMWG)

[![Microsoft Foundry Developer Forum](https://img.shields.io/badge/GitHub-Microsoft_Foundry_Developer_Forum-blue?style=for-the-badge&logo=github&color=000000&logoColor=fff)](https://aka.ms/foundry/forum)

微軟 Azure 雲端倡導者很高興提供一個為期 10 週、共 20 節的資料科學課程。每堂課包含課前和課後測驗、完成課程的書面指南、解答以及作業。我們採用以專案為基礎的教學法，讓你在實作中學習，這是一種讓新技能穩固吸收的有效方式。

**衷心感謝我們的作者們：** [Jasmine Greenaway](https://www.twitter.com/paladique)、[Dmitry Soshnikov](http://soshnikov.com)、[Nitya Narasimhan](https://twitter.com/nitya)、[Jalen McGee](https://twitter.com/JalenMcG)、[Jen Looper](https://twitter.com/jenlooper)、[Maud Levy](https://twitter.com/maudstweets)、[Tiffany Souterre](https://twitter.com/TiffanySouterre)、[Christopher Harrison](https://www.twitter.com/geektrainer)。

**🙏 特別感謝 🙏 我們的 [Microsoft 學生大使](https://studentambassadors.microsoft.com/) 作者、審查員與內容貢獻者，** 主要包括 Aaryan Arora、[Aditya Garg](https://github.com/AdityaGarg00)、[Alondra Sanchez](https://www.linkedin.com/in/alondra-sanchez-molina/)、[Ankita Singh](https://www.linkedin.com/in/ankitasingh007)、[Anupam Mishra](https://www.linkedin.com/in/anupam--mishra/)、[Arpita Das](https://www.linkedin.com/in/arpitadas01/)、ChhailBihari Dubey、[Dibri Nsofor](https://www.linkedin.com/in/dibrinsofor)、[Dishita Bhasin](https://www.linkedin.com/in/dishita-bhasin-7065281bb)、[Majd Safi](https://www.linkedin.com/in/majd-s/)、[Max Blum](https://www.linkedin.com/in/max-blum-6036a1186/)、[Miguel Correa](https://www.linkedin.com/in/miguelmque/)、[Mohamma Iftekher (Iftu) Ebne Jalal](https://twitter.com/iftu119)、[Nawrin Tabassum](https://www.linkedin.com/in/nawrin-tabassum)、[Raymond Wangsa Putra](https://www.linkedin.com/in/raymond-wp/)、[Rohit Yadav](https://www.linkedin.com/in/rty2423)、Samridhi Sharma、[Sanya Sinha](https://www.linkedin.com/mwlite/in/sanya-sinha-13aab1200)、[Sheena Narula](https://www.linkedin.com/in/sheena-narua-n/)、[Tauqeer Ahmad](https://www.linkedin.com/in/tauqeerahmad5201/)、Yogendrasingh Pawar、[Vidushi Gupta](https://www.linkedin.com/in/vidushi-gupta07/)、[Jasleen Sondhi](https://www.linkedin.com/in/jasleen-sondhi/)

|![Sketchnote by @sketchthedocs https://sketchthedocs.dev](../../translated_images/zh-TW/00-Title.8af36cd35da1ac55.webp)|
|:---:|
| 初學者資料科學 - _圖解筆記由 [@nitya](https://twitter.com/nitya) 製作_ |

### 🌐 多語系支援

#### 透過 GitHub Action 支援（自動且隨時更新）

<!-- CO-OP TRANSLATOR LANGUAGES TABLE START -->
[Arabic](../ar/README.md) | [Bengali](../bn/README.md) | [Bulgarian](../bg/README.md) | [Burmese (Myanmar)](../my/README.md) | [Chinese (Simplified)](../zh-CN/README.md) | [Chinese (Traditional, Hong Kong)](../zh-HK/README.md) | [Chinese (Traditional, Macau)](../zh-MO/README.md) | [Chinese (Traditional, Taiwan)](./README.md) | [Croatian](../hr/README.md) | [Czech](../cs/README.md) | [Danish](../da/README.md) | [Dutch](../nl/README.md) | [Estonian](../et/README.md) | [Finnish](../fi/README.md) | [French](../fr/README.md) | [German](../de/README.md) | [Greek](../el/README.md) | [Hebrew](../he/README.md) | [Hindi](../hi/README.md) | [Hungarian](../hu/README.md) | [Indonesian](../id/README.md) | [Italian](../it/README.md) | [Japanese](../ja/README.md) | [Kannada](../kn/README.md) | [Korean](../ko/README.md) | [Lithuanian](../lt/README.md) | [Malay](../ms/README.md) | [Malayalam](../ml/README.md) | [Marathi](../mr/README.md) | [Nepali](../ne/README.md) | [Nigerian Pidgin](../pcm/README.md) | [Norwegian](../no/README.md) | [Persian (Farsi)](../fa/README.md) | [Polish](../pl/README.md) | [Portuguese (Brazil)](../pt-BR/README.md) | [Portuguese (Portugal)](../pt-PT/README.md) | [Punjabi (Gurmukhi)](../pa/README.md) | [Romanian](../ro/README.md) | [Russian](../ru/README.md) | [Serbian (Cyrillic)](../sr/README.md) | [Slovak](../sk/README.md) | [Slovenian](../sl/README.md) | [Spanish](../es/README.md) | [Swahili](../sw/README.md) | [Swedish](../sv/README.md) | [Tagalog (Filipino)](../tl/README.md) | [Tamil](../ta/README.md) | [Telugu](../te/README.md) | [Thai](../th/README.md) | [Turkish](../tr/README.md) | [Ukrainian](../uk/README.md) | [Urdu](../ur/README.md) | [Vietnamese](../vi/README.md)

> **偏好本機複製？**

> 本儲存庫包含超過 50 種語言翻譯，會大幅增加下載大小。若要在沒有翻譯的情況下複製，請使用稀疏檢出：
> ```bash
> git clone --filter=blob:none --sparse https://github.com/microsoft/Data-Science-For-Beginners.git
> cd Data-Science-For-Beginners
> git sparse-checkout set --no-cone '/*' '!translations' '!translated_images'
> ```
> 這樣你會以更快的速度獲得完成課程所需的一切。
<!-- CO-OP TRANSLATOR LANGUAGES TABLE END -->

**如果你希望支援其他翻譯語言，清單列於[這裡](https://github.com/Azure/co-op-translator/blob/main/getting_started/supported-languages.md)**

#### 加入我們的社群  
[![Microsoft Foundry Discord](https://dcbadge.limes.pink/api/server/nTYy5BXMWG)](https://discord.gg/nTYy5BXMWG)

我們持續進行 Discord 上的 AI 學習系列，詳情請參閱並加入 [Learn with AI Series](https://aka.ms/learnwithai/discord)，活動期間為 2025 年 9 月 18 日至 30 日。你將獲得使用 GitHub Copilot 進行資料科學的技巧與秘訣。

![Learn with AI series](../../translated_images/zh-TW/1.2b28cdc6205e26fe.webp)

# 你是學生嗎？

請使用以下資源開始：

- [學生中心頁面](https://docs.microsoft.com/en-gb/learn/student-hub?WT.mc_id=academic-77958-bethanycheum) 在這頁你可以找到初學者資源、學生套件，甚至有方式取得免費認證憑證。這是一個你應該收藏並常回訪的網頁，因為我們至少每月更新一次內容。
- [Microsoft Learn 學生大使](https://studentambassadors.microsoft.com?WT.mc_id=academic-77958-bethanycheum) 加入全球學生大使社群，這可能是你進入微軟的門路。

# 入門指南

## 📚 文件資源

- **[安裝指南](INSTALLATION.md)** - 初學者逐步安裝說明
- **[使用指南](USAGE.md)** - 範例與常見工作流程
- **[故障排除](TROUBLESHOOTING.md)** - 常見問題解決方案
- **[貢獻指南](CONTRIBUTING.md)** - 如何為此專案做出貢獻
- **[教師專用](for-teachers.md)** - 教學指引和課堂資源

## 👨‍🎓 對學生

> **完全初學者**：對資料科學不熟悉？從我們的[初學者範例](examples/README.md)開始吧！這些簡單且註解完整的範例，能幫助你先了解基礎，再投入完整課程。
> **[學生](https://aka.ms/student-page)**：想自行使用本課程，請將整個儲存庫 fork 一份，自行完成課程活動，從課前測驗開始。然後閱讀課程內容，完成後續練習。嘗試理解課程內容自行建立專案，不要直接複製解答程式碼；不過這些程式碼會放在每個以專案為導向課程的 /solutions 目錄下。另一個想法是與朋友組成學習小組，一起研讀課程內容。進一步學習，建議參考 [Microsoft Learn](https://docs.microsoft.com/en-us/users/jenlooper-2911/collections/qprpajyoy3x0g7?WT.mc_id=academic-77958-bethanycheum)。

**快速開始：**
1. 參考[安裝指南](INSTALLATION.md)設定你的開發環境
2. 閱讀[使用指南](USAGE.md)了解如何操作課程內容
3. 從第一課開始，依序完成各課
4. 加入我們的[Discord 社群](https://aka.ms/ds4beginners/discord)尋求支援

## 👩‍🏫 對教師

> **教師們**：我們在[此處](for-teachers.md)提供了一些使用本課程的建議。歡迎你在[討論論壇](https://github.com/microsoft/Data-Science-For-Beginners/discussions)提供回饋！
## 認識團隊

[![宣傳影片](../../ds-for-beginners.gif)](https://youtu.be/8mzavjQSMM4 "宣傳影片")

**Gif 製作者** [Mohit Jaisal](https://www.linkedin.com/in/mohitjaisal)

> 🎥 點擊上方圖片觀看關於此專案及創作者的影片！

## 教學法

我們在建構此課程時選擇了兩個教學原則：確保它是以專案為基礎，並包括頻繁的小測驗。到本系列結束時，學生將學會資料科學的基本原理，包括倫理概念、資料準備、不同的資料處理方式、資料視覺化、資料分析、資料科學的實際案例等。

此外，課前的低壓測驗能設定學生學習主題的意圖，而課後的第二次測驗則確保進一步的記憶鞏固。此課程設計靈活且有趣，可全部或部分學習。專案由簡入深，隨著10週週期的結束逐漸變得複雜。

> 請參閱我們的[行為準則](CODE_OF_CONDUCT.md)、[貢獻指南](CONTRIBUTING.md)、[翻譯指南](TRANSLATIONS.md)。我們歡迎您的建設性回饋！

## 每堂課包含：

- 可選擇的手繪筆記
- 可選擇的補充影片
- 課前暖身小測驗
- 書面課程內容
- 以專案為基礎的課程，包含如何逐步構建專案的指南
- 知識檢查
- 挑戰任務
- 補充閱讀
- 作業
- [課後小測驗](https://ff-quizzes.netlify.app/en/)

> **關於測驗的說明**：所有測驗存放於 Quiz-App 資料夾中，共40個小測驗，每個含三個問題。它們從課程內部連結，但該測驗應用也可以在本地執行或部署到 Azure；請參考 `quiz-app` 資料夾中的指示。正逐步進行在地化。

## 🎓 初學者友善範例

**資料科學新手？** 我們建立了一個特別的[範例目錄](examples/README.md)，提供簡單且詳細註解的程式碼，幫助你快速上手：

- 🌟 **Hello World** - 你的第一個資料科學程式
- 📂 **載入資料** - 學習讀取與探索資料集
- 📊 **簡單分析** - 計算統計與尋找模式
- 📈 **基本視覺化** - 製作圖表
- 🔬 **真實專案** - 完整流程從頭到尾

每個範例皆附詳細註解說明每一步，適合完全初學者！

👉 **[從範例開始學習](examples/README.md)** 👈

## 課程列表


|![ 由 @sketchthedocs 製作的手繪筆記 https://sketchthedocs.dev](../../translated_images/zh-TW/00-Roadmap.4905d6567dff4753.webp)|
|:---:|
| 初學資料科學：路線圖 - _手繪筆記由 [@nitya](https://twitter.com/nitya) 製作_ |


| 課程編號 | 主題 | 課程群組 | 學習目標 | 連結課程 | 作者 |
| :-------: | :----------------------------------------: | :--------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------: | :----: |
| 01 | 定義資料科學 | [介紹](1-Introduction/README.md) | 了解資料科學的基本概念及其與人工智慧、機器學習和大數據的關係。 | [課程](1-Introduction/01-defining-data-science/README.md) [影片](https://youtu.be/beZ7Mb_oz9I) | [Dmitry](http://soshnikov.com) |
| 02 | 資料科學倫理 | [介紹](1-Introduction/README.md) | 資料倫理的概念、挑戰與架構。 | [課程](1-Introduction/02-ethics/README.md) | [Nitya](https://twitter.com/nitya) |
| 03 | 定義資料 | [介紹](1-Introduction/README.md) | 資料如何分類及常見來源。 | [課程](1-Introduction/03-defining-data/README.md) | [Jasmine](https://www.twitter.com/paladique) |
| 04 | 統計與機率入門 | [介紹](1-Introduction/README.md) | 運用機率與統計的數學技術理解資料。 | [課程](1-Introduction/04-stats-and-probability/README.md) [影片](https://youtu.be/Z5Zy85g4Yjw) | [Dmitry](http://soshnikov.com) |
| 05 | 處理關聯型資料 | [處理資料](2-Working-With-Data/README.md) | 介紹關聯型資料及使用結構化查詢語言（SQL，讀作「see-quell」）探索與分析關聯資料的基礎。 | [課程](2-Working-With-Data/05-relational-databases/README.md) | [Christopher](https://www.twitter.com/geektrainer) |
| 06 | 處理 NoSQL 資料 | [處理資料](2-Working-With-Data/README.md) | 介紹非關聯資料及其類型，及探索與分析文件型資料庫的基礎。 | [課程](2-Working-With-Data/06-non-relational/README.md) | [Jasmine](https://twitter.com/paladique) |
| 07 | 使用 Python | [處理資料](2-Working-With-Data/README.md) | 使用 Python 與 Pandas 等函式庫進行資料探索的基礎。建議具備 Python 程式設計基礎。 | [課程](2-Working-With-Data/07-python/README.md) [影片](https://youtu.be/dZjWOGbsN4Y) | [Dmitry](http://soshnikov.com) |
| 08 | 資料準備 | [處理資料](2-Working-With-Data/README.md) | 資料清理與轉換技術，應對缺失、不準確或不完整資料的挑戰。 | [課程](2-Working-With-Data/08-data-preparation/README.md) | [Jasmine](https://www.twitter.com/paladique) |
| 09 | 數量視覺化 | [資料視覺化](3-Data-Visualization/README.md) | 學習用 Matplotlib 來視覺化鳥類資料 🦆 | [課程](3-Data-Visualization/09-visualization-quantities/README.md) | [Jen](https://twitter.com/jenlooper) |
| 10 | 資料分布視覺化 | [資料視覺化](3-Data-Visualization/README.md) | 視覺化區間內的觀測與趨勢。 | [課程](3-Data-Visualization/10-visualization-distributions/README.md) | [Jen](https://twitter.com/jenlooper) |
| 11 | 比例視覺化 | [資料視覺化](3-Data-Visualization/README.md) | 視覺化離散與分組百分比。 | [課程](3-Data-Visualization/11-visualization-proportions/README.md) | [Jen](https://twitter.com/jenlooper) |
| 12 | 關係視覺化 | [資料視覺化](3-Data-Visualization/README.md) | 視覺化資料集及其變數間的連結與關聯。 | [課程](3-Data-Visualization/12-visualization-relationships/README.md) | [Jen](https://twitter.com/jenlooper) |
| 13 | 有意義的視覺化 | [資料視覺化](3-Data-Visualization/README.md) | 製作具價值且有助於有效問題解決與洞察的視覺化技術與指導。 | [課程](3-Data-Visualization/13-meaningful-visualizations/README.md) | [Jen](https://twitter.com/jenlooper) |
| 14 | 資料科學生命週期入門 | [生命週期](4-Data-Science-Lifecycle/README.md) | 介紹資料科學生命週期及其第一步：獲取與萃取資料。 | [課程](4-Data-Science-Lifecycle/14-Introduction/README.md) | [Jasmine](https://twitter.com/paladique) |
| 15 | 資料分析 | [生命週期](4-Data-Science-Lifecycle/README.md) | 資料科學生命週期中專注於資料分析技術的階段。 | [課程](4-Data-Science-Lifecycle/15-analyzing/README.md) | [Jasmine](https://twitter.com/paladique) |
| 16 | 溝通 | [生命週期](4-Data-Science-Lifecycle/README.md) | 資料科學生命週期中著重於以便於決策者理解的方式呈現資料洞察的階段。 | [課程](4-Data-Science-Lifecycle/16-communication/README.md) | [Jalen](https://twitter.com/JalenMcG) |
| 17 | 雲端中的資料科學 | [雲端資料](5-Data-Science-In-Cloud/README.md) | 系列課程介紹雲端資料科學及其優點。 | [課程](5-Data-Science-In-Cloud/17-Introduction/README.md) | [Tiffany](https://twitter.com/TiffanySouterre) 和 [Maud](https://twitter.com/maudstweets) |
| 18 | 雲端中的資料科學 | [雲端資料](5-Data-Science-In-Cloud/README.md) | 使用低代碼工具訓練模型。 |[課程](5-Data-Science-In-Cloud/18-Low-Code/README.md) | [Tiffany](https://twitter.com/TiffanySouterre) 和 [Maud](https://twitter.com/maudstweets) |
| 19 | 雲端中的資料科學 | [雲端資料](5-Data-Science-In-Cloud/README.md) | 使用 Azure Machine Learning Studio 部署模型。 | [課程](5-Data-Science-In-Cloud/19-Azure/README.md) | [Tiffany](https://twitter.com/TiffanySouterre) 和 [Maud](https://twitter.com/maudstweets) |
| 20 | 實務中的資料科學 | [實務應用](6-Data-Science-In-Wild/README.md) | 實務中由資料科學驅動的專案。 | [課程](6-Data-Science-In-Wild/20-Real-World-Examples/README.md) | [Nitya](https://twitter.com/nitya) |

## GitHub Codespaces

請依照以下步驟打開此範例於 Codespace：
1. 點擊 Code 下拉選單，選擇「Open with Codespaces」。
2. 在窗格底部選擇「+ New codespace」。
更多資訊請參考 [GitHub 文件](https://docs.github.com/en/codespaces/developing-in-codespaces/creating-a-codespace-for-a-repository#creating-a-codespace)。

## VSCode 遠端容器

請依照下列步驟使用 VS Code Remote - Containers 擴充套件，在你的本機和 VSCode 中於容器中開啟此倉庫：

1. 若是首次使用開發容器，請確保你的系統已符合前置需求（例如安裝 Docker），詳見[入門文件](https://code.visualstudio.com/docs/devcontainers/containers#_getting-started)。

使用此倉庫時，可以選擇在隔離的 Docker 卷中開啟：

**注意**：底層會使用 Remote-Containers 的 **Clone Repository in Container Volume...** 指令，將原始碼克隆到 Docker 卷，而非本地檔案系統。[卷](https://docs.docker.com/storage/volumes/) 是持續保存容器資料的首選方式。

或是開啟本地克隆或下載的倉庫版本：

- 將此倉庫克隆到本地檔案系統。
- 按 F1 鍵並選擇 **Remote-Containers: Open Folder in Container...** 指令。
- 選擇剛克隆的資料夾，等待容器啟動後即可開始使用。

## 離線使用

可用 [Docsify](https://docsify.js.org/#/) 離線運行此文件。請 fork 此倉庫，[在本機安裝 Docsify](https://docsify.js.org/#/quickstart)，然後於此倉庫根目錄輸入 `docsify serve`。網站將於本地主機的 3000 埠執行：`localhost:3000`。

> 注意，筆記本無法經由 Docsify 渲染，需時請另行在 VS Code 中使用 Python 核心運行。

## 其他課程

我們團隊也製作其他課程！歡迎查看：

<!-- CO-OP TRANSLATOR OTHER COURSES START -->
### LangChain
[![LangChain4j 初學者](https://img.shields.io/badge/LangChain4j%20for%20Beginners-22C55E?style=for-the-badge&&labelColor=E5E7EB&color=0553D6)](https://aka.ms/langchain4j-for-beginners)
[![LangChain.js for Beginners](https://img.shields.io/badge/LangChain.js%20for%20Beginners-22C55E?style=for-the-badge&labelColor=E5E7EB&color=0553D6)](https://aka.ms/langchainjs-for-beginners?WT.mc_id=m365-94501-dwahlin)

---

### Azure / Edge / MCP / Agents
[![AZD for Beginners](https://img.shields.io/badge/AZD%20for%20Beginners-0078D4?style=for-the-badge&labelColor=E5E7EB&color=0078D4)](https://github.com/microsoft/AZD-for-beginners?WT.mc_id=academic-105485-koreyst)
[![Edge AI for Beginners](https://img.shields.io/badge/Edge%20AI%20for%20Beginners-00B8E4?style=for-the-badge&labelColor=E5E7EB&color=00B8E4)](https://github.com/microsoft/edgeai-for-beginners?WT.mc_id=academic-105485-koreyst)
[![MCP for Beginners](https://img.shields.io/badge/MCP%20for%20Beginners-009688?style=for-the-badge&labelColor=E5E7EB&color=009688)](https://github.com/microsoft/mcp-for-beginners?WT.mc_id=academic-105485-koreyst)
[![AI Agents for Beginners](https://img.shields.io/badge/AI%20Agents%20for%20Beginners-00C49A?style=for-the-badge&labelColor=E5E7EB&color=00C49A)](https://github.com/microsoft/ai-agents-for-beginners?WT.mc_id=academic-105485-koreyst)

---
 
### 生成式 AI 系列
[![Generative AI for Beginners](https://img.shields.io/badge/Generative%20AI%20for%20Beginners-8B5CF6?style=for-the-badge&labelColor=E5E7EB&color=8B5CF6)](https://github.com/microsoft/generative-ai-for-beginners?WT.mc_id=academic-105485-koreyst)
[![Generative AI (.NET)](https://img.shields.io/badge/Generative%20AI%20(.NET)-9333EA?style=for-the-badge&labelColor=E5E7EB&color=9333EA)](https://github.com/microsoft/Generative-AI-for-beginners-dotnet?WT.mc_id=academic-105485-koreyst)
[![Generative AI (Java)](https://img.shields.io/badge/Generative%20AI%20(Java)-C084FC?style=for-the-badge&labelColor=E5E7EB&color=C084FC)](https://github.com/microsoft/generative-ai-for-beginners-java?WT.mc_id=academic-105485-koreyst)
[![Generative AI (JavaScript)](https://img.shields.io/badge/Generative%20AI%20(JavaScript)-E879F9?style=for-the-badge&labelColor=E5E7EB&color=E879F9)](https://github.com/microsoft/generative-ai-with-javascript?WT.mc_id=academic-105485-koreyst)

---
 
### 核心學習
[![ML for Beginners](https://img.shields.io/badge/ML%20for%20Beginners-22C55E?style=for-the-badge&labelColor=E5E7EB&color=22C55E)](https://aka.ms/ml-beginners?WT.mc_id=academic-105485-koreyst)
[![Data Science for Beginners](https://img.shields.io/badge/Data%20Science%20for%20Beginners-84CC16?style=for-the-badge&labelColor=E5E7EB&color=84CC16)](https://aka.ms/datascience-beginners?WT.mc_id=academic-105485-koreyst)
[![AI for Beginners](https://img.shields.io/badge/AI%20for%20Beginners-A3E635?style=for-the-badge&labelColor=E5E7EB&color=A3E635)](https://aka.ms/ai-beginners?WT.mc_id=academic-105485-koreyst)
[![Cybersecurity for Beginners](https://img.shields.io/badge/Cybersecurity%20for%20Beginners-F97316?style=for-the-badge&labelColor=E5E7EB&color=F97316)](https://github.com/microsoft/Security-101?WT.mc_id=academic-96948-sayoung)
[![Web Dev for Beginners](https://img.shields.io/badge/Web%20Dev%20for%20Beginners-EC4899?style=for-the-badge&labelColor=E5E7EB&color=EC4899)](https://aka.ms/webdev-beginners?WT.mc_id=academic-105485-koreyst)
[![IoT for Beginners](https://img.shields.io/badge/IoT%20for%20Beginners-14B8A6?style=for-the-badge&labelColor=E5E7EB&color=14B8A6)](https://aka.ms/iot-beginners?WT.mc_id=academic-105485-koreyst)
[![XR Development for Beginners](https://img.shields.io/badge/XR%20Development%20for%20Beginners-38BDF8?style=for-the-badge&labelColor=E5E7EB&color=38BDF8)](https://github.com/microsoft/xr-development-for-beginners?WT.mc_id=academic-105485-koreyst)

---
 
### Copilot 系列
[![Copilot for AI Paired Programming](https://img.shields.io/badge/Copilot%20for%20AI%20Paired%20Programming-FACC15?style=for-the-badge&labelColor=E5E7EB&color=FACC15)](https://aka.ms/GitHubCopilotAI?WT.mc_id=academic-105485-koreyst)
[![Copilot for C#/.NET](https://img.shields.io/badge/Copilot%20for%20C%23/.NET-FBBF24?style=for-the-badge&labelColor=E5E7EB&color=FBBF24)](https://github.com/microsoft/mastering-github-copilot-for-dotnet-csharp-developers?WT.mc_id=academic-105485-koreyst)
[![Copilot Adventure](https://img.shields.io/badge/Copilot%20Adventure-FDE68A?style=for-the-badge&labelColor=E5E7EB&color=FDE68A)](https://github.com/microsoft/CopilotAdventures?WT.mc_id=academic-105485-koreyst)
<!-- CO-OP TRANSLATOR OTHER COURSES END -->

## 獲取幫助

**遇到問題嗎？** 查看我們的[故障排除指南](TROUBLESHOOTING.md)，獲得常見問題的解決方案。

如果您卡住或對建立 AI 應用有任何疑問，請加入學習者及資深開發人員的 MCP 討論社群。這是一個支持性強的社群，歡迎提問且自由分享知識。

[![Microsoft Foundry Discord](https://dcbadge.limes.pink/api/server/nTYy5BXMWG)](https://discord.gg/nTYy5BXMWG)

如果您在開發過程中有產品反饋或錯誤，請訪問：

[![Microsoft Foundry Developer Forum](https://img.shields.io/badge/GitHub-Microsoft_Foundry_Developer_Forum-blue?style=for-the-badge&logo=github&color=000000&logoColor=fff)](https://aka.ms/foundry/forum)

---

<!-- CO-OP TRANSLATOR DISCLAIMER START -->
**免責聲明**：  
本文件係使用 AI 翻譯服務 [Co-op Translator](https://github.com/Azure/co-op-translator) 所翻譯而成。雖然我們致力於確保翻譯的準確性，但請注意自動翻譯可能包含錯誤或不準確之處。原始語言版本應視為權威且具法律效力的文件。對於關鍵資訊，建議聘請專業人工翻譯。我們不對因使用本翻譯內容而產生的任何誤解或誤譯負責。
<!-- CO-OP TRANSLATOR DISCLAIMER END -->