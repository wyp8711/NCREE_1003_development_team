
## 為什麼 Commit Message 很重要？

Git 在每次 Commit 時，需要寫下 Git Commit Message（提交說明），用來記錄提交版本更動的摘要。

&gt; 任何專案都至少由兩個以上的開發者共同合作開發

除了專案開發者，任何專案都會是跟其他開發者和、未來的自己共同開發維護的。當不同開發者接手專案時，能藉由瀏覽 Commit Message 內容快速進入狀況，瞭解程式異動的原因，如此也利於後續的維護。

### 何謂好的 Commit Message？

一個好的 Git Commit Message 必須兼具 What &amp; Why &amp; How，能幫助開發者瞭解這個提交版本：

1. 做了什麼事情（What）
2. 為什麼要做這件事情（Why）
3. 用什麼方法做到的（How）

## Commit Message 的規範與準則

在團隊之間，撰寫 commit log 的方式應一致，也就是定義風格與內容，可透過遵守現有的慣例來實現。

一個 Commit Message 主要由 Header + Body + Footer 組成：

```htmlmixed=
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```
### Message Header: 
 - type（必要）：commit 的類別
   - 如：feat, fix, docs, style, refactor, test, chore
 - scope（可選）：commit 影響的範圍
   - 如：資料庫、控制層、模板層等，視專案不同改變
 - subject（必要）：commit 的簡短描述
   - 不超過 50 個字元
   - 結尾不加句號
   - 盡量讓 Commit 單一化，一次只更動一個主題

### Message Body
 * 對本次 Commit 的詳細描述，解釋 What & Why & How
 * 可以分成多行，每一行不超過 72 個字元
 * 說明程式碼變動的項目與原因，還有與先前行為的對比

### Message Footer
 - 填寫任務編號 `issue #1246`
 - BREAKING CHANGE（可略），記錄不兼容的變動，後面是對變動的描述、以及變動原因和遷移方法

## Header： 類別規範

type 代表提交 Commit 的類別，以下為使用慣例：

* feat：新增或修改功能（feature）
* fix：修補 bug（bug fix）
* docs：文件（documentation）
* style：格式
  * 不影響程式碼運行的變動，例如：white-space, formatting, missing semi colons
* refactor：重構 
  * 不是新增功能，也非修補 bug 的程式碼變動
* perf：改善效能（improves performance）
* test：增加測試（when adding missing tests）
* chore：maintain
  * 不影響程式碼運行，建構程序或輔助工具的變動，例如修改 config、Grunt Task 任務管理工具
* revert：撤銷回覆先前的 commit
  * 例如：`revert：type(scope):subject`
### Commit Message 範例

以下舉幾個範例：

```
feat: message 新增信件通知功能
feat(優惠券): 加入搜尋按鈕，調整畫面

fix: 圓餅圖圖例跑版
fix: 意見反應，信件看不到圖片問題

style: 統一換行符號 CRLF to LF

docs: 更新 README 相關資訊
docs: 修正型別註解

chore(submoudle): 變更 git url
chore: 調整單元測試環境

refactor(每日通知信件): 重構程式結構
```
# Reference
https://codeewander.github.io/docs/git-commit
https://sparkful.app/zh-TW/blog/craft-meaningful-git-commit-messages
https://codeewander.github.io/docs/git-commit
