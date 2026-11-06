# 東京 2026 行程網頁：給 Claude 的規則

靜態網頁 `index.html`，用 GitHub Pages 發布（https://axde954e6.github.io/2026-TOKYO/）。
風格參考神戶網頁：https://github.com/axde954e6/2026-KOBE

## 內容寫法：簡短為主
- 每張行程卡 `.note` 一到兩句就好，寫重點（交通幾分、營業時間、要不要預約），不寫導覽細節、不寫長段說明。
- 一個大景點只用一張卡；底下小景點用 `.stop-list`，最多 3–4 項，每項一句。
- 不要把景點內部的參觀路線逐項列出。
- 重要提醒（公休、需預約、末班車）用 `<mark class="hl">…</mark>` 標一句，不另開長段落。
- 可有可無的景點標「⭐ 有空再去」或寫「沒預約就跳過」，不要硬排。
- 交通只寫最省事的一種，必要時再補一種。
- 不確定的資訊寫「以官網為準」，不要寫成長篇推測。

## 流程
- 使用者要求修改時：改完 commit、push 到指定分支、開 PR、直接 squash merge 到 main，不用再問。
- merge 後確認 Pages 部署（`pages build and deployment`）成功；deploy 卡住超過 10 分鐘，就推一個不影響內容的小 commit 重新觸發。
