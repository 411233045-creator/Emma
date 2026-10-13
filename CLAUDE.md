# Emma

不用登入的匿名網頁聊天室：輸入代號就能進房間收發訊息，前端放在 GitHub Pages，後端使用 Supabase。

## 開始工作前

開始任何工作前，先讀 [docs/architecture.md](docs/architecture.md)。畫面、資料格式、資料夾結構、驗證清單都以它為準。

## 目前階段

目前在**階段一**：還沒接 Supabase，前端使用瀏覽器裡的假後端（`VITE_BACKEND=mock`）。階段一的範圍與完成條件見架構文件第 4.1 節與第 13.1 節。

## 金鑰

不可以把金鑰檔案 commit 進 git。

- `.env`、`.env.local`、`.env.*.local` 不可以 commit；只有 `.env.example`（值留空）可以。
- Supabase 的秘密金鑰（Secret key，舊名 service_role key）、資料庫密碼、站長密碼，不可以出現在 repo 的任何檔案裡，也不可以放進任何 `VITE_` 開頭的設定。
- commit 前先確認變更清單裡沒有 `.env` 開頭的檔案。詳細規則見架構文件第 8 節。
