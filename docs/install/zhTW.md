# OneWoW Suite — 玩家安裝說明

**語言：** [English](../../README.md) · [Deutsch](deDE.md) · [Español (España)](esES.md) · [Español (México)](esMX.md) · [Français](frFR.md) · [Italiano](itIT.md) · [한국어](koKR.md) · [Português (Brasil)](ptBR.md) · [Русский](ruRU.md) · [简体中文](zhCN.md) · 繁體中文

本儲存庫是 OneWoW 的**玩家**副本：只有放進魔獸世界的插件資料夾。內容會從完整的 [Suite 儲存庫](https://github.com/kellewic/OneWoW_Suite)同步。玩遊戲不需要那個開發用的完整儲存庫。

- **網站：** [https://wow2.xyz/](https://wow2.xyz/)
- **玩家 Wiki：** [安裝](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [入門](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **支援：** [https://wow2.xyz/support/](https://wow2.xyz/support/)

這裡是鏡像。請不要在此開 issue 或 pull request。請到 Suite 儲存庫或支援頁面。

**一般**步驟（GitHub Desktop）與**進階**步驟（命令列，以及不用再複製資料夾的連結）都在同一頁。

---

## 你需要準備

- **魔獸世界正式服（Retail）**（本套件不適用於經典版）
- 電腦上一個用來保存本儲存庫的資料夾（「文件」即可）
- **GitHub Desktop**（建議），或如果你習慣命令列則安裝 **Git**

### 下載

| 內容 | 適用對象 | 連結 |
|------|----------|------|
| **GitHub Desktop** | Windows 10/11 與 macOS — 最簡單 | [desktop.github.com](https://desktop.github.com/) |
| **Git** | 僅命令列 | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Windows 版 Git** | Windows 命令列 | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **macOS 版 Git** | Mac 命令列（或 Xcode Command Line Tools） | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

使用 GitHub Desktop 時**不必**再另外安裝 Git。Desktop 已內建。

儲存庫位址（稍後貼上）：

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## 找到 AddOns 資料夾

魔獸只會載入位於 `Interface\AddOns` **直接內部**的插件（資料夾名稱為 `OneWoW`、`OneWoW_Bags` 等）。

**Windows（常見）：**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS（常見）：**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

如果路徑不對，表示遊戲裝在別處：

1. 開啟 **Battle.net** 用戶端。
2. 選擇**魔獸世界**。
3. 開啟「開始遊戲」旁邊的**齒輪** / 選項。
4. 在**遊戲設定**裡查看安裝位置，或使用**顯示資料夾** / **開啟資料夾**。

必須是 `_retail_`（正式服），不是 `_classic_` 或 `_classic_era_`。如果還沒有 `Interface` 與 `AddOns`，在 `_retail_` 裡新建這兩個資料夾。

---

## 一般安裝 — GitHub Desktop

不想打指令就用這個。

### 1. 安裝 GitHub Desktop

1. 開啟 [https://desktop.github.com/](https://desktop.github.com/)。
2. 下載 **Windows** 或 **macOS** 安裝檔。網站會依你的電腦選擇。
3. 執行安裝程式並完成設定。
4. 可以用 GitHub 帳號登入。對本**公開**儲存庫來說，登入是選用的。沒有帳號也能複製。

### 2. 複製本儲存庫（儲存到一個資料夾）

「Clone」的意思是：把儲存庫下載到你指定的資料夾，並維持與 GitHub 的連線，方便以後更新。

1. 開啟 **GitHub Desktop**。
2. **File → Clone repository**（檔案 → 複製儲存庫）。
3. 開啟 **URL** 分頁。
4. 貼上：

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. 把 **Local path** 設成容易再找到的資料夾，例如：

   - Windows：`C:\Users\你的使用者名稱\Documents\OneWoW_Suite_PlayerRepo`
   - Mac：`/Users/你的使用者名稱/Documents/OneWoW_Suite_PlayerRepo`

   這個資料夾**不是**遊戲的 AddOns。它只是一份工作副本。下一步再從這裡複製或連結到 AddOns。

6. 按 **Clone**，等到檔案出現。

完成後應能看到 `OneWoW`、`OneWoW_Bags`、`OneWoW_QoL` 以及其他 `OneWoW_*` 資料夾。

### 3. 把插件放進遊戲

1. 開啟剛儲存的複製資料夾。
2. 開啟 `Interface\AddOns`（見上文）。
3. 把需要的插件資料夾複製**進** `AddOns`。

**必須：** `OneWoW`（主介面）。沒有它，其他插件不會載入。

**選用功能：** `OneWoW_Bags`、`OneWoW_QoL`、`OneWoW_AltTracker`、`OneWoW_Catalog`、`OneWoW_Trackers`、`OneWoW_Notes`、`OneWoW_ShoppingList`、`OneWoW_Mail`、`OneWoW_DirectDeposit`。

**如果使用 Catalog**，還要複製所有 `OneWoW_CatalogData_*` 資料夾，否則那些分頁會是空的。

**如果使用 AltTracker**，還要複製所有 `OneWoW_AltTracker_*` 配套資料夾。

**DevTool**（`OneWoW_Utility_DevTool`）是選用的。這是遊戲內檢查器（`/1wdt`），玩遊戲不是必須。

不必複製全部。只複製你要啟用的。

**不要**把整個儲存庫當成一個名為 `OneWoW_Suite_PlayerRepo` 的資料夾丟進 AddOns。如果 `OneWoW` 再套一層，遊戲就找不到它。

複製後，`AddOns` 應類似：

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

而不是：

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. 在遊戲裡啟用

1. 在**角色選擇**畫面點擊**插件**。
2. 啟用 **OneWoW** 以及你複製的每個選用模組。
3. 進入遊戲（如果已經在世界裡，輸入 `/reload`）。
4. 輸入 `/1w` 開啟主介面。
5. 在 **Manage Features** 中啟用或停用模組。停用會**卸載**插件，不僅僅是隱藏。

### 5. 以後更新（Desktop）

1. 開啟 **GitHub Desktop**。
2. 確認頂部選中的是本儲存庫。
3. 點擊 **Fetch origin**，檢查 GitHub 是否有新檔案。
4. 如果出現 **Pull origin**，點它。變更會下載到複製資料夾。

如果當初是把資料夾**複製**進 AddOns 的，每次 pull 之後再複製一遍並覆蓋舊檔。Windows 與 macOS 會詢問是否取代，選是。

如果用了**目錄聯結或符號連結**（下面進階部分），Pull 就夠了。遊戲已經指向這個資料夾。

遊戲在執行時，取代檔案前先關閉魔獸。更安全。

---

## 另一種簡單做法 — ZIP（不會自動更新）

在儲存庫頁面點 **Code → Download ZIP**，解壓後用同樣方式把 `OneWoW*` 資料夾複製到 AddOns。

ZIP 每次都是完整快照，不會自己更新。如果以後想 `pull`，請用 Desktop 或 Git。不想用 Git 也可以用 **CurseForge** 或 Discord 社群 ZIP。

---

## 進階 — Git 命令列

如果你習慣終端機。先安裝 [Git](https://git-scm.com/downloads)（[Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)）。Mac 上也可以執行 `xcode-select --install`。

Windows 開啟 **Git Bash** 或 **PowerShell**，Mac 開啟**終端機**。用 `cd` 進入要建立資料夾的位置（例如「文件」），然後：

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` 只下載最新檔案，不要多年歷史。

然後像一般安裝一樣，把 `OneWoW*` 資料夾複製（或連結）到 `Interface\AddOns`。

### 以後更新（命令列）

```text
cd 路徑\OneWoW_Suite_PlayerRepo
git pull
```

Mac 使用 `路徑/OneWoW_Suite_PlayerRepo`。

如果是複製的資料夾，再複製到 AddOns。如果已連結，`git pull` 就是全部更新。

---

## 進階 — 目錄聯結與符號連結（不用再複製）

**連結**讓 `AddOns\OneWoW` 指向 `...\OneWoW_Suite_PlayerRepo\OneWoW`。之後 Desktop 的 Pull 或 `git pull` 會直接更新遊戲正在用的檔案。

- 先關閉魔獸世界。
- 用 Desktop 或 Git **先複製**儲存庫，再建立連結（目標資料夾必須已存在）。
- 如果已經把 `OneWoW` **複製**進 AddOns，先刪除或重新命名那份副本。已有同名真實資料夾時無法建立連結。
- 每個要用的插件資料夾建一條連結。從 `OneWoW` 開始。
- 在 AddOns 裡刪除聯結或符號連結只會去掉**連結**，不會刪除你的複製本。

### Windows — 目錄聯結（不需要系統管理員）

目錄聯結（`mklink /J`）不需要以系統管理員開啟命令提示字元。符號連結（`mklink /D`）常常需要，請用 `/J`。

1. 開啟**命令提示字元**（cmd）。
2. 把兩條路徑改成你真實的魔獸 `AddOns` 與真實的複製資料夾。
3. 每個插件一行：

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\你的使用者名稱\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Bags 範例：

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\你的使用者名稱\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

對每個使用的 `OneWoW_*` 資料夾重複（包括 Catalog 資料與 AltTracker 配套資料夾）。

**PowerShell：**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\你的使用者名稱\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

如果 Windows 提示路徑已存在，表示 AddOns 裡還有同名資料夾。刪掉或改名後再執行命令。

### macOS — 符號連結

1. 開啟**終端機**。
2. 依你的 Mac 改兩條路徑。
3. 執行：

```text
ln -s "/Users/你的使用者名稱/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

每個插件資料夾重複一次。如果 `AddOns/OneWoW` 已是真實副本，先把它移到垃圾桶。

### 檢查是否成功

開啟 `AddOns\OneWoW`（或 Mac 上的對應路徑）。應看到與複製本裡相同的檔案。Pull 之後這些檔案會變，不必再複製。

### 撤銷連結

只刪除 **AddOns 裡**的那個連結資料夾。複製本 `OneWoW_Suite_PlayerRepo` 還在。想改回複製也可以。

---

## 本儲存庫中的資料夾

| 類型 | 資料夾 |
|------|--------|
| **必須** | `OneWoW` |
| **功能** | `OneWoW_Bags`、`OneWoW_QoL`、`OneWoW_AltTracker`、`OneWoW_Catalog`、`OneWoW_Trackers`、`OneWoW_Notes`、`OneWoW_ShoppingList`、`OneWoW_Mail`、`OneWoW_DirectDeposit` |
| **Catalog 資料** | `OneWoW_CatalogData_Journal`、`OneWoW_CatalogData_Vendors`、`OneWoW_CatalogData_Tradeskills`、`OneWoW_CatalogData_Quests`、`OneWoW_CatalogData_Quests_Archive` |
| **AltTracker 資料** | `OneWoW_AltTracker_Storage`、`OneWoW_AltTracker_Character`、`OneWoW_AltTracker_Professions`、`OneWoW_AltTracker_Collections`、`OneWoW_AltTracker_Endgame`、`OneWoW_AltTracker_Auctions`、`OneWoW_AltTracker_Accounting` |
| **選用** | `OneWoW_Utility_DevTool`（`/1wdt`） |

---

## 常見問題

| 現象 | 處理 |
|------|------|
| 角色選擇看不到 OneWoW | AddOns 裡缺少 `OneWoW`，或它套在另一層資料夾裡。 |
| 功能已開但是空的 | 同時複製 Catalog 或 AltTracker 的資料資料夾並啟用。 |
| Pull 成功但遊戲還是舊的 | 你只複製過一次。Pull 後再複製，或改用聯結／符號連結。 |
| `mklink` / `ln` 失敗 | AddOns 裡已有同名真實資料夾，或路徑寫錯。 |
| 插件不載入 | 確認是 `_retail_`，且資料夾直接位於 `AddOns` 下。 |

---

## 說明

- 玩家 Wiki：[https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- 支援：[https://wow2.xyz/support/](https://wow2.xyz/support/)
- 完整原始碼（參與開發）：[https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**作者：** MichinMuggin / Ricky

**網站：** https://wow2.xyz/

**版權所有。**
