## 跟你朋友介紹 Git
首先你已經知道 Git 的重要功能就是版本控制，而這類的版本控制系統，簡單來說是用來幫助我們記錄檔案的各種變更，包含新增、編輯、修改等，使我們除了能夠保存這些歷史紀錄外，還可以顯示不同版本間的差異，並可將檔案復原到某一版本。這在個人使用或單一檔案時可能尚感覺不出它究竟有多便利與強大，但當遇到多人協作或多檔案時，Git 的優勢便相當明顯，大家可以各自開發或維護專案而不用互相傷害，也無須擔心版本的衝突或主機出問題。當遇到問題時，我們可以透過  Git 保留的歷史紀錄來找出兇手與證據，也可以隨意回到喜歡的版本，不怕找不到檔案或被覆蓋掉。

它的另一大優點是，作為分散式版本控制系統，它可以在自己、同事、公司或任何有需要的電腦上，建立起本地端的**「數據庫/檔案庫（Repository）」**，每個數據庫得各自進行開發，並依需求上傳或下載檔案到遠端數據庫上。

為了操作 Git，我們需要使用指令來進行，接著就來介紹一些基本但超級實用的指令吧！
打開你的終端機視窗，我們第一步需要先建立一個 **Git 目錄**，所以在進入想建立目錄的資料夾後使用 `git init` 指令建立起一個**.git**目錄，讓 Git 開始對它進行版本控制；接著使用 `git add <檔名>` 指令把想要進行版本控制的檔案放進目錄，如果想一次拉資料夾內全部的檔案，可以使用 `git add .` 指令喔！
當編輯過檔案想要好好留記錄、即新建版本的時候，則輸入 `git commit` 指令，進入編輯器 vim 裡面記錄下想寫的 commit，vim 的用法你自己去查！而想確認目前的版本控制的狀況時，可以使用 `git status` 指令查詢；若是要看歷史紀錄，則輸入 `git log` 來看，如果嫌 `git log` 的資訊又臭又長，也可輸入 `git log --oneline` 取得比較簡短的資訊。
另外，也可在目錄下建立一個 **.gitignore** 檔案，在裡面用 vim 列出所有**不想**加入版本控制、即要忽略的檔案檔名，不過 .gitignore 本身需要加入版本控制。

在使用 Git 的時候，還可以建立**分支（branch）**（相對於分支的是 **master**），在不影響原本的檔案的情況下，在分支上進行新的操作或開發，並視需求也可以將分支合併回去 master，分支的用法我們就先談到這裡，有機會再繼續 XDD

另外還要介紹一個 Git 的平台叫做 **GitHub**，它提供大家在上面建立數據庫，因此我們可以它為遠端數據庫。我們可以執行 `git pull origin` 指令，把東西從 GitHub 上抓下來使用，並用 `git push origin master` 指令把本地端的 master 相關分支內容推到 GitHub 上相對應的數據庫。

以上就是簡單的 Git 介紹啦。