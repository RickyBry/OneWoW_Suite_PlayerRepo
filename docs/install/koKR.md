# OneWoW Suite — 플레이어 설치 안내

**언어:** [English](../../README.md) · [Deutsch](deDE.md) · [Español (España)](esES.md) · [Español (México)](esMX.md) · [Français](frFR.md) · [Italiano](itIT.md) · 한국어 · [Português (Brasil)](ptBR.md) · [Русский](ruRU.md) · [简体中文](zhCN.md) · [繁體中文](zhTW.md)

이 저장소는 OneWoW의 **플레이어용** 복사본입니다. 월드 오브 워크래프트에 넣는 애드온 폴더만 들어 있습니다. [전체 Suite 저장소](https://github.com/kellewic/OneWoW_Suite)에서 최신 내용이 반영됩니다. 개발용 전체 저장소는 플레이에 필요하지 않습니다.

- **웹사이트:** [https://wow2.xyz/](https://wow2.xyz/)
- **플레이어 위키:** [설치](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [시작하기](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **지원:** [https://wow2.xyz/support/](https://wow2.xyz/support/)

여기는 미러입니다. 이슈나 풀 리퀘스트는 열지 마세요. Suite 저장소나 지원 페이지를 이용해 주세요.

**일반** 절차(GitHub Desktop)와 **고급** 절차(명령줄, 폴더를 다시 복사하지 않는 링크)가 같은 페이지에 있습니다.

---

## 필요한 것

- **월드 오브 워크래프트 리테일** (클래식용이 아닙니다)
- 이 저장소를 둘 폴더 (문서 폴더로 충분합니다)
- **GitHub Desktop** (권장) 또는 명령줄을 쓸 경우 **Git**

### 다운로드

| 항목 | 대상 | 링크 |
|------|------|------|
| **GitHub Desktop** | Windows 10/11 및 macOS — 가장 쉬운 방법 | [desktop.github.com](https://desktop.github.com/) |
| **Git** | 명령줄만 사용할 때 | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Windows용 Git** | Windows 명령줄 | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **macOS용 Git** | Mac 명령줄 (또는 Xcode Command Line Tools) | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

GitHub Desktop을 쓰면 Git을 **따로** 설치할 필요가 없습니다. Desktop에 포함되어 있습니다.

저장소 주소 (나중에 붙여 넣습니다):

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## AddOns 폴더 찾기

와우는 `Interface\AddOns` **바로 안**에 있는 애드온만 불러옵니다 (`OneWoW`, `OneWoW_Bags` 등).

**Windows (일반):**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS (일반):**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

경로가 다르면 게임이 다른 위치에 설치된 것입니다.

1. **Battle.net** 앱을 엽니다.
2. **월드 오브 워크래프트**를 선택합니다.
3. 플레이 버튼 옆 **톱니바퀴** / 옵션을 엽니다.
4. **게임 설정**에서 설치 위치를 찾거나 **폴더 표시** / **폴더 열기**를 사용합니다.

`_retail_`(리테일)이어야 합니다. `_classic_`나 `_classic_era_`가 아닙니다. `Interface`와 `AddOns`가 없으면 `_retail_` 안에 두 폴더를 만드세요.

---

## 일반 설치 — GitHub Desktop

명령을 입력하고 싶지 않다면 이 방법을 쓰세요.

### 1. GitHub Desktop 설치

1. [https://desktop.github.com/](https://desktop.github.com/) 을 엽니다.
2. **Windows** 또는 **macOS**용 설치 파일을 받습니다. 사이트가 맞는 파일을 고릅니다.
3. 설치 프로그램을 실행하고 설정을 마칩니다.
4. GitHub 계정으로 로그인할 수 있습니다. 이 **공개** 저장소는 로그인이 필수는 아닙니다. 계정 없이 복제할 수 있습니다.

### 2. 저장소 복제 (폴더에 저장)

「복제(Clone)」는 선택한 폴더로 저장소를 받고, 나중에 업데이트할 수 있도록 GitHub와 연결을 유지하는 것입니다.

1. **GitHub Desktop**을 엽니다.
2. **File → Clone repository** (파일 → 저장소 복제).
3. **URL** 탭을 엽니다.
4. 다음을 붙여 넣습니다.

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. **Local path**에 다시 찾기 쉬운 폴더를 지정합니다. 예:

   - Windows: `C:\Users\이름\Documents\OneWoW_Suite_PlayerRepo`
   - Mac: `/Users/이름/Documents/OneWoW_Suite_PlayerRepo`

   이 폴더는 와우 AddOns 폴더가 **아닙니다**. 작업용 복사본입니다. 다음 단계에서 여기부터 AddOns로 복사하거나 연결합니다.

6. **Clone**을 누르고 파일이 나타날 때까지 기다립니다.

끝나면 `OneWoW`, `OneWoW_Bags`, `OneWoW_QoL` 및 다른 `OneWoW_*` 폴더가 보여야 합니다.

### 3. 애드온을 게임에 넣기

1. 방금 저장한 복제 폴더를 엽니다.
2. `Interface\AddOns` 폴더를 엽니다 (위 참고).
3. 원하는 애드온 폴더를 `AddOns` **안으로** 복사합니다.

**필수:** `OneWoW` (허브). 없으면 나머지가 로드되지 않습니다.

**선택 기능:** `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit`.

**Catalog를 쓰면** `OneWoW_CatalogData_*` 폴더도 모두 복사하세요. 그렇지 않으면 해당 탭이 비어 보입니다.

**AltTracker를 쓰면** `OneWoW_AltTracker_*` 동반 폴더도 모두 복사하세요.

**DevTool** (`OneWoW_Utility_DevTool`)은 선택 사항입니다. 게임 안 검사기(`/1wdt`)이며 플레이에 필수는 아닙니다.

모든 폴더가 필요하지는 않습니다. 켤 것만 복사하세요.

저장소 전체를 `OneWoW_Suite_PlayerRepo`라는 **한 폴더**로 AddOns에 넣지 마세요. 한 단계 더 안에 있으면 와우가 `OneWoW`를 찾지 못합니다.

복사 후 `AddOns`는 이렇게 보여야 합니다.

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

이렇게가 아닙니다.

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. 와우에서 켜기

1. **캐릭터 선택** 화면에서 **애드온**을 클릭합니다.
2. **OneWoW**와 복사한 선택 모듈을 활성화합니다.
3. 접속합니다 (이미 접속 중이면 `/reload`).
4. `/1w`를 입력해 허브를 엽니다.
5. **Manage Features**에서 모듈을 켜거나 끕니다. 끄면 애드온이 **언로드**됩니다. 숨기기만 하는 것이 아닙니다.

### 5. 나중에 업데이트 (Desktop)

1. **GitHub Desktop**을 엽니다.
2. 위쪽에서 이 저장소가 선택되어 있는지 확인합니다.
3. **Fetch origin**을 클릭합니다. GitHub에 새 파일이 있는지 확인합니다.
4. **Pull origin**이 보이면 클릭합니다. 변경 사항이 복제 폴더로 내려옵니다.

AddOns에 폴더를 **복사**했다면, pull 후에 다시 복사하고 이전 파일을 덮어쓰세요. Windows와 macOS가 바꾸겠냐고 물으면 예를 선택합니다.

**정션/심볼릭 링크**를 썼다면 (아래 고급) Pull만으로 충분합니다. 게임이 이미 이 폴더를 가리킵니다.

게임이 켜져 있으면 파일을 바꾸기 전에 와우를 종료하세요. 더 안전합니다.

---

## 다른 간단한 방법 — ZIP (자동 업데이트 없음)

저장소 페이지에서 **Code → Download ZIP**, 압축을 푼 뒤 `OneWoW*` 폴더를 위와 같이 AddOns에 복사합니다.

ZIP은 매번 전체 스냅샷입니다. 스스로 업데이트되지 않습니다. 나중에 `pull`하려면 Desktop이나 Git을 쓰세요. Git을 쓰기 싫다면 **CurseForge**나 Discord 커뮤니티 ZIP도 괜찮습니다.

---

## 고급 — Git 명령줄

터미널이 편하다면 이 방법을 쓰세요. 먼저 [Git](https://git-scm.com/downloads)을 설치합니다 ([Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)). Mac에서는 `xcode-select --install`도 됩니다.

Windows는 **Git Bash** 또는 **PowerShell**, Mac은 **터미널**을 엽니다. 폴더를 만들 위치로 `cd`한 다음 (예: 문서):

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1`은 최신 파일만 받고 과거 기록은 받지 않습니다.

그다음 일반 설치와 같이 `OneWoW*` 폴더를 `Interface\AddOns`에 복사하거나 연결합니다.

### 나중에 업데이트 (명령줄)

```text
cd 경로\OneWoW_Suite_PlayerRepo
git pull
```

Mac에서는 `경로/OneWoW_Suite_PlayerRepo`를 사용합니다.

폴더를 복사했다면 AddOns에 다시 복사하세요. 연결했다면 `git pull`이 업데이트 전부입니다.

---

## 고급 — 정션과 심볼릭 링크 (다시 복사하지 않기)

**링크**는 `AddOns\OneWoW`가 `...\OneWoW_Suite_PlayerRepo\OneWoW`를 가리키게 합니다. 이후 Desktop Pull이나 `git pull`이 게임이 이미 쓰는 파일을 갱신합니다.

- 먼저 월드 오브 워크래프트를 종료하세요.
- 링크를 만들기 **전에** Desktop이나 Git으로 저장소를 복제하세요 (대상 폴더가 있어야 합니다).
- AddOns에 `OneWoW`를 이미 **복사**했다면 그 복사본을 삭제하거나 이름을 바꾸세요. 같은 이름의 실제 폴더가 있으면 링크를 만들 수 없습니다.
- 사용할 애드온 폴더마다 링크를 하나씩 만듭니다. `OneWoW`부터 시작하세요.
- AddOns에서 정션/심볼릭 링크를 삭제하면 **링크만** 사라지고 복제본은 남습니다.

### Windows — 정션 (관리자 권한 불필요)

정션(`mklink /J`)은 관리자 명령 프롬프트가 필요 없습니다. 심볼릭 링크(`mklink /D`)는 종종 필요합니다. `/J`를 쓰세요.

1. **명령 프롬프트**(cmd)를 엽니다.
2. 두 경로를 실제 와우 `AddOns`와 실제 복제 폴더에 맞게 고칩니다.
3. 애드온마다 한 줄씩 실행합니다.

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\이름\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Bags 예:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\이름\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

사용하는 모든 `OneWoW_*` 폴더에 반복하세요 (Catalog 데이터, AltTracker 동반 폴더 포함).

**PowerShell:**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\이름\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Windows가 경로가 이미 있다고 하면 AddOns에 폴더가 아직 있는 것입니다. 제거하거나 이름을 바꾼 뒤 다시 실행하세요.

### macOS — 심볼릭 링크

1. **터미널**을 엽니다.
2. 두 경로를 Mac에 맞게 고칩니다.
3. 실행합니다.

```text
ln -s "/Users/이름/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

각 애드온 폴더마다 반복하세요. `AddOns/OneWoW`가 실제 복사본으로 있으면 먼저 휴지통으로 옮기세요.

### 확인

`AddOns\OneWoW`(또는 Mac 경로)를 엽니다. 복제본과 같은 파일이 보여야 합니다. Pull 후에는 다시 복사하지 않아도 파일이 바뀝니다.

### 링크 해제

AddOns **안의** 연결된 폴더만 삭제하세요. `OneWoW_Suite_PlayerRepo` 복제본은 그대로입니다. 원하면 다시 복사 방식으로 돌아갈 수 있습니다.

---

## 이 저장소의 폴더

| 종류 | 폴더 |
|------|------|
| **필수** | `OneWoW` |
| **기능** | `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit` |
| **Catalog 데이터** | `OneWoW_CatalogData_Journal`, `OneWoW_CatalogData_Vendors`, `OneWoW_CatalogData_Tradeskills`, `OneWoW_CatalogData_Quests`, `OneWoW_CatalogData_Quests_Archive` |
| **AltTracker 데이터** | `OneWoW_AltTracker_Storage`, `OneWoW_AltTracker_Character`, `OneWoW_AltTracker_Professions`, `OneWoW_AltTracker_Collections`, `OneWoW_AltTracker_Endgame`, `OneWoW_AltTracker_Auctions`, `OneWoW_AltTracker_Accounting` |
| **선택** | `OneWoW_Utility_DevTool` (`/1wdt`) |

---

## 자주 있는 문제

| 증상 | 조치 |
|------|------|
| 캐릭터 선택에 OneWoW가 없음 | AddOns에 `OneWoW`가 없거나 다른 폴더 안에 있습니다. |
| 기능은 켜져 있지만 비어 있음 | Catalog 또는 AltTracker 데이터 폴더도 복사하고 활성화하세요. |
| Pull은 됐는데 게임이 예전처럼 보임 | 한 번만 복사했습니다. Pull 후 다시 복사하거나 정션/심볼릭 링크를 쓰세요. |
| `mklink` / `ln` 실패 | AddOns에 같은 이름의 실제 폴더가 있거나 경로가 잘못되었습니다. |
| 애드온이 로드되지 않음 | `_retail_`인지, 폴더가 `AddOns` 바로 아래인지 확인하세요. |

---

## 도움말

- 플레이어 위키: [https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- 지원: [https://wow2.xyz/support/](https://wow2.xyz/support/)
- 전체 소스 (기여): [https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**제작:** MichinMuggin / Ricky

**웹사이트:** https://wow2.xyz/

**All rights reserved.**
