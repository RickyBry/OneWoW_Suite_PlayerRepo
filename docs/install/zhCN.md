# OneWoW Suite — 玩家安装说明

**语言：** [English](../../README.md) · [Deutsch](deDE.md) · [Español (España)](esES.md) · [Español (México)](esMX.md) · [Français](frFR.md) · [Italiano](itIT.md) · [한국어](koKR.md) · [Português (Brasil)](ptBR.md) · [Русский](ruRU.md) · 简体中文 · [繁體中文](zhTW.md)

本仓库是 OneWoW 的**玩家**副本：只有放进魔兽世界的插件文件夹。内容会从完整的 [Suite 仓库](https://github.com/kellewic/OneWoW_Suite)同步。玩游戏不需要那个开发用的完整仓库。

- **网站：** [https://wow2.xyz/](https://wow2.xyz/)
- **玩家维基：** [安装](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [入门](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **支持：** [https://wow2.xyz/support/](https://wow2.xyz/support/)

这里是镜像。请不要在此提交 issue 或 pull request。请到 Suite 仓库或支持页面。

**普通**步骤（GitHub Desktop）和**高级**步骤（命令行，以及不用再复制文件夹的链接）都在同一页。

---

## 你需要准备

- **魔兽世界正式服（Retail）**（本套件不适用于怀旧服）
- 电脑上一个用来保存本仓库的文件夹（「文档」即可）
- **GitHub Desktop**（推荐），或如果你习惯命令行则安装 **Git**

### 下载

| 内容 | 适用对象 | 链接 |
|------|----------|------|
| **GitHub Desktop** | Windows 10/11 和 macOS — 最简单 | [desktop.github.com](https://desktop.github.com/) |
| **Git** | 仅命令行 | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Windows 版 Git** | Windows 命令行 | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **macOS 版 Git** | Mac 命令行（或 Xcode Command Line Tools） | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

使用 GitHub Desktop 时**不必**再单独安装 Git。Desktop 已自带。

仓库地址（稍后粘贴）：

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## 找到 AddOns 文件夹

魔兽只会加载位于 `Interface\AddOns` **直接内部**的插件（文件夹名为 `OneWoW`、`OneWoW_Bags` 等）。

**Windows（常见）：**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS（常见）：**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

如果路径不对，说明游戏装在别处：

1. 打开 **Battle.net** 客户端。
2. 选择**魔兽世界**。
3. 打开「开始游戏」旁边的**齿轮** / 选项。
4. 在**游戏设置**里查看安装位置，或使用**显示文件夹** / **打开文件夹**。

必须是 `_retail_`（正式服），不是 `_classic_` 或 `_classic_era_`。如果还没有 `Interface` 和 `AddOns`，在 `_retail_` 里新建这两个文件夹。

---

## 普通安装 — GitHub Desktop

不想打命令就用这个。

### 1. 安装 GitHub Desktop

1. 打开 [https://desktop.github.com/](https://desktop.github.com/)。
2. 下载 **Windows** 或 **macOS** 安装包。网站会按你的电脑选择。
3. 运行安装程序并完成设置。
4. 可以用 GitHub 账号登录。对本**公开**仓库来说，登录是可选的。没有账号也能克隆。

### 2. 克隆本仓库（保存到一个文件夹）

「克隆」的意思是：把仓库下载到你指定的文件夹，并保持与 GitHub 的连接，方便以后更新。

1. 打开 **GitHub Desktop**。
2. **File → Clone repository**（文件 → 克隆仓库）。
3. 打开 **URL** 标签。
4. 粘贴：

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. 把 **Local path** 设成容易再找到的文件夹，例如：

   - Windows：`C:\Users\你的用户名\Documents\OneWoW_Suite_PlayerRepo`
   - Mac：`/Users/你的用户名/Documents/OneWoW_Suite_PlayerRepo`

   这个文件夹**不是**游戏的 AddOns。它只是一份工作副本。下一步再从这里复制或链接到 AddOns。

6. 点击 **Clone**，等到文件出现。

完成后应能看到 `OneWoW`、`OneWoW_Bags`、`OneWoW_QoL` 以及其他 `OneWoW_*` 文件夹。

### 3. 把插件放进游戏

1. 打开刚保存的克隆文件夹。
2. 打开 `Interface\AddOns`（见上文）。
3. 把需要的插件文件夹复制**进** `AddOns`。

**必须：** `OneWoW`（主界面）。没有它，其他插件不会加载。

**可选功能：** `OneWoW_Bags`、`OneWoW_QoL`、`OneWoW_AltTracker`、`OneWoW_Catalog`、`OneWoW_Trackers`、`OneWoW_Notes`、`OneWoW_ShoppingList`、`OneWoW_Mail`、`OneWoW_DirectDeposit`。

**如果使用 Catalog**，还要复制所有 `OneWoW_CatalogData_*` 文件夹，否则那些标签页会是空的。

**如果使用 AltTracker**，还要复制所有 `OneWoW_AltTracker_*` 配套文件夹。

**DevTool**（`OneWoW_Utility_DevTool`）是可选的。这是游戏内检查器（`/1wdt`），玩游戏不是必须。

不必复制全部。只复制你要启用的。

**不要**把整个仓库当成一个名为 `OneWoW_Suite_PlayerRepo` 的文件夹丢进 AddOns。如果 `OneWoW` 再套一层，游戏就找不到它。

复制后，`AddOns` 应类似：

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

### 4. 在游戏里启用

1. 在**角色选择**界面点击**插件**。
2. 启用 **OneWoW** 以及你复制的每个可选模块。
3. 进入游戏（如果已经在世界里，输入 `/reload`）。
4. 输入 `/1w` 打开主界面。
5. 在 **Manage Features** 中启用或停用模块。停用会**卸载**插件，不仅仅是隐藏。

### 5. 以后更新（Desktop）

1. 打开 **GitHub Desktop**。
2. 确认顶部选中的是本仓库。
3. 点击 **Fetch origin**，检查 GitHub 是否有新文件。
4. 如果出现 **Pull origin**，点它。更改会下载到克隆文件夹。

如果当初是把文件夹**复制**进 AddOns 的，每次 pull 之后再复制一遍并覆盖旧文件。Windows 和 macOS 会询问是否替换，选是。

如果用了**目录联接或符号链接**（下面高级部分），Pull 就够了。游戏已经指向这个文件夹。

游戏在运行时，替换文件前先关闭魔兽。更安全。

---

## 另一种简单做法 — ZIP（不会自动更新）

在仓库页面点 **Code → Download ZIP**，解压后按同样方式把 `OneWoW*` 文件夹复制到 AddOns。

ZIP 每次都是完整快照，不会自己更新。如果以后想 `pull`，请用 Desktop 或 Git。不想用 Git 也可以用 **CurseForge** 或 Discord 社区 ZIP。

---

## 高级 — Git 命令行

如果你习惯终端。先安装 [Git](https://git-scm.com/downloads)（[Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)）。Mac 上也可以运行 `xcode-select --install`。

Windows 打开 **Git Bash** 或 **PowerShell**，Mac 打开**终端**。用 `cd` 进入要创建文件夹的位置（例如「文档」），然后：

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` 只下载最新文件，不要多年历史。

然后像普通安装一样，把 `OneWoW*` 文件夹复制（或链接）到 `Interface\AddOns`。

### 以后更新（命令行）

```text
cd 路径\OneWoW_Suite_PlayerRepo
git pull
```

Mac 使用 `路径/OneWoW_Suite_PlayerRepo`。

如果是复制的文件夹，再复制到 AddOns。如果已链接，`git pull` 就是全部更新。

---

## 高级 — 目录联接与符号链接（不用再复制）

**链接**让 `AddOns\OneWoW` 指向 `...\OneWoW_Suite_PlayerRepo\OneWoW`。之后 Desktop 的 Pull 或 `git pull` 会直接更新游戏正在用的文件。

- 先关闭魔兽世界。
- 用 Desktop 或 Git **先克隆**仓库，再创建链接（目标文件夹必须已存在）。
- 如果已经把 `OneWoW` **复制**进 AddOns，先删除或重命名那份副本。已有同名真实文件夹时无法创建链接。
- 每个要用的插件文件夹建一条链接。从 `OneWoW` 开始。
- 在 AddOns 里删除联接或符号链接只会去掉**链接**，不会删除你的克隆。

### Windows — 目录联接（不需要管理员）

目录联接（`mklink /J`）不需要以管理员打开命令提示符。符号链接（`mklink /D`）常常需要，请用 `/J`。

1. 打开**命令提示符**（cmd）。
2. 把两条路径改成你真实的魔兽 `AddOns` 和真实的克隆文件夹。
3. 每个插件一行：

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\你的用户名\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Bags 示例：

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\你的用户名\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

对每个使用的 `OneWoW_*` 文件夹重复（包括 Catalog 数据和 AltTracker 配套文件夹）。

**PowerShell：**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\你的用户名\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

如果 Windows 提示路径已存在，说明 AddOns 里还有同名文件夹。删掉或改名后再运行命令。

### macOS — 符号链接

1. 打开**终端**。
2. 按你的 Mac 改两条路径。
3. 运行：

```text
ln -s "/Users/你的用户名/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

每个插件文件夹重复一次。如果 `AddOns/OneWoW` 已是真实副本，先把它移到废纸篓。

### 检查是否成功

打开 `AddOns\OneWoW`（或 Mac 上的对应路径）。应看到与克隆里相同的文件。Pull 之后这些文件会变，不必再复制。

### 撤销链接

只删除 **AddOns 里**的那个链接文件夹。克隆 `OneWoW_Suite_PlayerRepo` 还在。想改回复制也可以。

---

## 本仓库中的文件夹

| 类型 | 文件夹 |
|------|--------|
| **必须** | `OneWoW` |
| **功能** | `OneWoW_Bags`、`OneWoW_QoL`、`OneWoW_AltTracker`、`OneWoW_Catalog`、`OneWoW_Trackers`、`OneWoW_Notes`、`OneWoW_ShoppingList`、`OneWoW_Mail`、`OneWoW_DirectDeposit` |
| **Catalog 数据** | `OneWoW_CatalogData_Journal`、`OneWoW_CatalogData_Vendors`、`OneWoW_CatalogData_Tradeskills`、`OneWoW_CatalogData_Quests`、`OneWoW_CatalogData_Quests_Archive` |
| **AltTracker 数据** | `OneWoW_AltTracker_Storage`、`OneWoW_AltTracker_Character`、`OneWoW_AltTracker_Professions`、`OneWoW_AltTracker_Collections`、`OneWoW_AltTracker_Endgame`、`OneWoW_AltTracker_Auctions`、`OneWoW_AltTracker_Accounting` |
| **可选** | `OneWoW_Utility_DevTool`（`/1wdt`） |

---

## 常见问题

| 现象 | 处理 |
|------|------|
| 角色选择看不到 OneWoW | AddOns 里缺少 `OneWoW`，或它套在另一层文件夹里。 |
| 功能已开但是空的 | 同时复制 Catalog 或 AltTracker 的数据文件夹并启用。 |
| Pull 成功但游戏还是旧的 | 你只复制过一次。Pull 后再复制，或改用联接/符号链接。 |
| `mklink` / `ln` 失败 | AddOns 里已有同名真实文件夹，或路径写错。 |
| 插件不加载 | 确认是 `_retail_`，且文件夹直接位于 `AddOns` 下。 |

---

## 帮助

- 玩家维基：[https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- 支持：[https://wow2.xyz/support/](https://wow2.xyz/support/)
- 完整源码（参与开发）：[https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**作者：** MichinMuggin / Ricky

**网站：** https://wow2.xyz/

**版权所有。**
