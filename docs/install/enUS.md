# OneWoW Suite — player install

**Language:** English · [Deutsch](deDE.md) · [Español (España)](esES.md) · [Español (México)](esMX.md) · [Français](frFR.md) · [Italiano](itIT.md) · [한국어](koKR.md) · [Português (Brasil)](ptBR.md) · [Русский](ruRU.md) · [简体中文](zhCN.md) · [繁體中文](zhTW.md)

This page is the same English guide as the [repository README](../../README.md).

This repository is the **player** copy of OneWoW: only the addon folders you put in World of Warcraft. It is kept up to date from the full [Suite repo](https://github.com/kellewic/OneWoW_Suite). You do not need that full repo to play.

- **Website:** [https://wow2.xyz/](https://wow2.xyz/)
- **Player wiki:** [Install](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [Getting started](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **Support:** [https://wow2.xyz/support/](https://wow2.xyz/support/)

This is a mirror. Please do not open issues or pull requests here. Use the Suite repo or the support page.

The **normal** steps (GitHub Desktop) and the **advanced** steps (command line and links so you never copy folders again) are on this same page.

---

## What you need

- **World of Warcraft Retail** (this suite is not for Classic)
- A folder on your computer to keep this repo (Documents is fine)
- **GitHub Desktop** (recommended) or **Git** if you prefer the command line

### Downloads

| What | Who it is for | Link |
|------|----------------|------|
| **GitHub Desktop** | Windows 10/11 and macOS — easiest way | [desktop.github.com](https://desktop.github.com/) |
| **Git** | Command line only | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Git for Windows** | Windows command line | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **Git for macOS** | Mac command line (or install Xcode Command Line Tools) | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

You do **not** need Git installed if you use GitHub Desktop. Desktop includes what it needs.

Repository address (you will paste this later):

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## Find your AddOns folder

WoW only loads addons that sit **directly** inside `Interface\AddOns` (each folder named `OneWoW`, `OneWoW_Bags`, and so on).

**Windows (typical):**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS (typical):**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

If those paths are wrong, your game is installed somewhere else:

1. Open the **Battle.net** app.
2. Select **World of Warcraft**.
3. Open the **gear** / options next to the Play button.
4. Open **Game Settings** and find the install location, or use any **Show folder** / **Open folder** control.

You want `_retail_` (Retail), not `_classic_` or `_classic_era_`. If `Interface\AddOns` does not exist yet, create those two folders inside `_retail_`.

---

## Normal install — GitHub Desktop

Use this if you do not want to type commands.

### 1. Install GitHub Desktop

1. Open [https://desktop.github.com/](https://desktop.github.com/).
2. Download the installer for **Windows** or **macOS**. The site picks the right one for your computer.
3. Run the installer and finish the setup screens.
4. You may sign in with a GitHub account. For this **public** repo, sign-in is optional. You can clone without an account.

### 2. Clone this repository (save it to a folder)

"Clone" means: download the repo into a folder you choose, and keep a link to GitHub so you can update later.

1. Open **GitHub Desktop**.
2. **File → Clone repository**.
3. Open the **URL** tab.
4. Paste:

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. Set **Local path** to a simple folder you can find again, for example:

   - Windows: `C:\Users\YOURNAME\Documents\OneWoW_Suite_PlayerRepo`
   - Mac: `/Users/YOURNAME/Documents/OneWoW_Suite_PlayerRepo`

   This folder is **not** your WoW AddOns folder. It is a holding copy. You will copy or link from here into AddOns in the next step.

6. Click **Clone** and wait until the files appear.

When it is done, that folder should contain `OneWoW`, `OneWoW_Bags`, `OneWoW_QoL`, and the other `OneWoW_*` folders.

### 3. Put the addons into the game

1. Open the clone folder you just saved.
2. Open your `Interface\AddOns` folder (see above).
3. Copy the addon folders you want **into** `AddOns`.

**Required:** `OneWoW` (the hub). Without it, the rest will not load.

**Optional features:** `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit`.

**If you use Catalog**, also copy all `OneWoW_CatalogData_*` folders or those tabs will look empty.

**If you use AltTracker**, also copy all `OneWoW_AltTracker_*` companion folders.

**DevTool** (`OneWoW_Utility_DevTool`) is optional. It is an in-game inspector (`/1wdt`), not required to play.

You do not need every folder. Copy only what you will enable.

**Do not** drop the whole repo into AddOns as one folder named `OneWoW_Suite_PlayerRepo`. WoW will not see `OneWoW` if it is nested one level too deep.

After a copy, `AddOns` should look like:

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

not:

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. Turn them on in WoW

1. At the **character select** screen, click **AddOns**.
2. Enable **OneWoW** and every optional module you copied.
3. Log in (or type `/reload` if you were already in the world).
4. Type `/1w` to open the hub.
5. Use **Manage Features** to enable or disable modules. Disabling a feature unloads it; it is not only hidden.

### 5. Update later (Desktop)

1. Open **GitHub Desktop**.
2. Make sure this repository is selected at the top.
3. Click **Fetch origin**. That checks GitHub for new files.
4. If Desktop offers **Pull origin**, click it. That downloads the changes into your clone folder.

If you **copied** folders into AddOns, copy them again after each pull and overwrite the old ones. Windows and macOS will ask you to replace files — say yes.

If you used **junctions or symlinks** (advanced section below), Pull is enough. The game already points at this folder.

Close WoW before you replace files if the game is running. It is the safer habit.

---

## Other simple option — zip (no updates)

On the repo page, **Code → Download ZIP**, unpack it, then copy the `OneWoW*` folders into AddOns the same way.

A zip is a full snapshot every time. It will not update itself. Prefer Desktop or Git if you want `pull` later. **CurseForge** and the Discord community zip are also fine if you do not want Git at all.

---

## Advanced — Git command line

Use this if you are comfortable in a terminal. Install [Git](https://git-scm.com/downloads) first ([Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)). On a Mac you can also run `xcode-select --install` and use the Git that comes with the Command Line Tools.

Open **Git Bash** or **PowerShell** on Windows, or **Terminal** on a Mac. Choose where the folder should be created (`cd` into Documents if you like), then:

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` downloads only the latest files, not years of history.

Then copy (or link) the `OneWoW*` folders into `Interface\AddOns` exactly as in the normal install.

### Update later (command line)

```text
cd path\to\OneWoW_Suite_PlayerRepo
git pull
```

On a Mac use `path/to/OneWoW_Suite_PlayerRepo`.

If you copied folders, copy them into AddOns again. If you linked them, `git pull` is the whole update.

---

## Advanced — junctions and symlinks (no more copying)

A **link** makes `AddOns\OneWoW` point at `...\OneWoW_Suite_PlayerRepo\OneWoW`. After that, Desktop Pull or `git pull` updates the files the game already uses.

- Close World of Warcraft first.
- Clone the repo with Desktop or Git **before** you create links (the target folders must exist).
- If you already **copied** `OneWoW` into AddOns, delete or rename that copy first. A link cannot be created if a real folder with the same name is already there.
- Create one link per addon folder you want. Start with `OneWoW`.
- Deleting a junction or symlink in AddOns removes the **link**, not your clone.

### Windows — junction (no Administrator)

A junction (`mklink /J`) does not need an Administrator command prompt. A symlink (`mklink /D`) often does — use `/J`.

1. Open **Command Prompt** (cmd).
2. Adjust both paths: your real WoW `AddOns` folder, and your real clone folder.
3. Run one line per addon:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\YOURNAME\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Example for Bags:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\YOURNAME\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

Repeat for every `OneWoW_*` folder you use (including Catalog data and AltTracker companions).

**PowerShell** equivalent:

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\YOURNAME\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

If Windows says the path already exists, a folder is still in AddOns. Remove or rename it, then run the command again.

### macOS — symlink

1. Open **Terminal**.
2. Adjust both paths to match your Mac.
3. Run:

```text
ln -s "/Users/YOURNAME/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

Repeat for each addon folder. If `AddOns/OneWoW` already exists as a real copy, move it to the Trash first.

### Check that it worked

Open `AddOns\OneWoW` (or the Mac equivalent). You should see the same files as in your clone. After a Pull, those files should change without another copy.

### Undo a link

Delete the linked folder **inside AddOns** only. Your `OneWoW_Suite_PlayerRepo` clone stays on disk. You can go back to copying folders if you prefer.

---

## Folders in this repo

| Kind | Folders |
|------|---------|
| **Required** | `OneWoW` |
| **Features** | `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit` |
| **Catalog data** | `OneWoW_CatalogData_Journal`, `OneWoW_CatalogData_Vendors`, `OneWoW_CatalogData_Tradeskills`, `OneWoW_CatalogData_Quests`, `OneWoW_CatalogData_Quests_Archive` |
| **AltTracker data** | `OneWoW_AltTracker_Storage`, `OneWoW_AltTracker_Character`, `OneWoW_AltTracker_Professions`, `OneWoW_AltTracker_Collections`, `OneWoW_AltTracker_Endgame`, `OneWoW_AltTracker_Auctions`, `OneWoW_AltTracker_Accounting` |
| **Optional** | `OneWoW_Utility_DevTool` (`/1wdt`) |

---

## Common problems

| What you see | What to do |
|--------------|------------|
| No OneWoW at character select | The `OneWoW` folder is missing from AddOns, or it is nested inside another folder. |
| Feature enabled but empty | Copy the Catalog or AltTracker data folders too, and enable them. |
| Pull worked but the game looks old | You copied folders once. Copy again after Pull, or use junctions/symlinks. |
| `mklink` / `ln` fails | A real folder with that name already exists in AddOns, or a path is wrong. |
| Addons do not load | Confirm you are in `_retail_`, and that the folders sit directly in `AddOns`. |

---

## Help

- Player wiki: [https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- Support: [https://wow2.xyz/support/](https://wow2.xyz/support/)
- Full source (contributors): [https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**Author:** MichinMuggin / Ricky

**Website:** https://wow2.xyz/

**All rights reserved.**
