# OneWoW Suite — установка для игроков

**Язык:** [English](../../README.md) · [Deutsch](deDE.md) · [Español (España)](esES.md) · [Español (México)](esMX.md) · [Français](frFR.md) · [Italiano](itIT.md) · [한국어](koKR.md) · [Português (Brasil)](ptBR.md) · Русский · [简体中文](zhCN.md) · [繁體中文](zhTW.md)

Этот репозиторий — **игровая** копия OneWoW: только папки аддонов для World of Warcraft. Он обновляется из полного [репозитория Suite](https://github.com/kellewic/OneWoW_Suite). Большой репозиторий разработчиков для игры не нужен.

- **Сайт:** [https://wow2.xyz/](https://wow2.xyz/)
- **Вики:** [Установка](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [С чего начать](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **Поддержка:** [https://wow2.xyz/support/](https://wow2.xyz/support/)

Это зеркало. Не открывайте здесь issues и pull request. Пишите в репозиторий Suite или на страницу поддержки.

**Обычные** шаги (GitHub Desktop) и **расширенные** (командная строка и ссылки, чтобы больше не копировать папки) собраны на этой же странице.

---

## Что нужно

- **World of Warcraft Retail** (эта сюита не для Classic)
- Папка на компьютере для этого репозитория (Документы подойдут)
- **GitHub Desktop** (рекомендуется) или **Git**, если удобнее терминал

### Загрузки

| Что | Для кого | Ссылка |
|-----|----------|--------|
| **GitHub Desktop** | Windows 10/11 и macOS — самый простой способ | [desktop.github.com](https://desktop.github.com/) |
| **Git** | Только командная строка | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Git для Windows** | Терминал Windows | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **Git для macOS** | Терминал Mac (или Xcode Command Line Tools) | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

Если вы используете GitHub Desktop, Git **отдельно** ставить не нужно. Desktop уже всё содержит.

Адрес репозитория (вставите позже):

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## Как найти папку AddOns

WoW загружает только аддоны, которые лежат **сразу** в `Interface\AddOns` (папки `OneWoW`, `OneWoW_Bags` и так далее).

**Windows (обычно):**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS (обычно):**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

Если пути другие, игра установлена в другом месте:

1. Откройте приложение **Battle.net**.
2. Выберите **World of Warcraft**.
3. Откройте **шестерёнку** / параметры рядом с «Играть».
4. В **настройках игры** найдите папку установки или нажмите **Показать папку** / **Открыть папку**.

Нужна папка `_retail_` (Retail), не `_classic_` и не `_classic_era_`. Если нет `Interface` и `AddOns`, создайте их внутри `_retail_`.

---

## Обычная установка — GitHub Desktop

Если не хотите вводить команды, используйте этот способ.

### 1. Установите GitHub Desktop

1. Откройте [https://desktop.github.com/](https://desktop.github.com/).
2. Скачайте установщик для **Windows** или **macOS**. Сайт сам выберет нужный файл.
3. Запустите установщик и завершите настройку.
4. Можно войти в аккаунт GitHub. Для этого **публичного** репозитория вход необязателен. Клонировать можно без аккаунта.

### 2. Клонируйте репозиторий (сохраните в папку)

«Клонировать» значит: скачать репозиторий в выбранную папку и сохранить связь с GitHub, чтобы потом обновлять.

1. Откройте **GitHub Desktop**.
2. **File → Clone repository** (Файл → Клонировать репозиторий).
3. Откройте вкладку **URL**.
4. Вставьте:

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. В **Local path** укажите простую папку, которую легко найти, например:

   - Windows: `C:\Users\ВАШЕИМЯ\Documents\OneWoW_Suite_PlayerRepo`
   - Mac: `/Users/ВАШЕИМЯ/Documents/OneWoW_Suite_PlayerRepo`

   Это **не** папка AddOns игры. Это рабочая копия. На следующем шаге вы скопируете или свяжете её с AddOns.

6. Нажмите **Clone** и дождитесь появления файлов.

Когда закончится, должны быть видны `OneWoW`, `OneWoW_Bags`, `OneWoW_QoL` и остальные папки `OneWoW_*`.

### 3. Положите аддоны в игру

1. Откройте только что сохранённую папку клона.
2. Откройте `Interface\AddOns` (см. выше).
3. Скопируйте нужные папки аддонов **внутрь** `AddOns`.

**Обязательно:** `OneWoW` (хаб). Без него остальное не загрузится.

**По желанию:** `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit`.

**Если используете Catalog**, скопируйте также все папки `OneWoW_CatalogData_*`, иначе вкладки будут пустыми.

**Если используете AltTracker**, скопируйте также все сопутствующие папки `OneWoW_AltTracker_*`.

**DevTool** (`OneWoW_Utility_DevTool`) необязателен. Это внутриигровой инспектор (`/1wdt`), для игры не нужен.

Не обязательно копировать всё. Только то, что включите.

**Не** кладите весь репозиторий в AddOns одной папкой `OneWoW_Suite_PlayerRepo`. WoW не увидит `OneWoW`, если он лежит на уровень глубже.

После копирования `AddOns` должен выглядеть так:

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

а не так:

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. Включите в WoW

1. На экране **выбора персонажа** нажмите **Модификации**.
2. Включите **OneWoW** и каждый скопированный необязательный модуль.
3. Войдите в игру (или введите `/reload`, если уже в мире).
4. Введите `/1w`, чтобы открыть хаб.
5. В **Manage Features** включайте и выключайте модули. Выключение **выгружает** аддон, а не только скрывает его.

### 5. Обновление позже (Desktop)

1. Откройте **GitHub Desktop**.
2. Убедитесь, что сверху выбран этот репозиторий.
3. Нажмите **Fetch origin**. Проверка GitHub на новые файлы.
4. Если появится **Pull origin**, нажмите. Изменения попадут в папку клона.

Если вы **копировали** папки в AddOns, после каждого pull скопируйте их снова и замените старые. Windows и macOS спросят про замену — согласитесь.

Если вы сделали **junction или символические ссылки** (раздел ниже), достаточно Pull. Игра уже смотрит в эту папку.

Если игра запущена, закройте WoW перед заменой файлов. Так безопаснее.

---

## Другой простой вариант — ZIP (без обновлений)

На странице репозитория: **Code → Download ZIP**, распакуйте и скопируйте папки `OneWoW*` в AddOns так же, как выше.

ZIP — полный снимок каждый раз. Сам он не обновится. Для `pull` лучше Desktop или Git. **CurseForge** и ZIP из Discord тоже подойдут, если Git не нужен.

---

## Расширенно — Git в командной строке

Если вам удобен терминал. Сначала установите [Git](https://git-scm.com/downloads) ([Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)). На Mac можно выполнить `xcode-select --install`.

Откройте **Git Bash** или **PowerShell** в Windows либо **Терминал** на Mac. Перейдите через `cd` туда, где создать папку (например Документы), затем:

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` скачивает только актуальные файлы, без всей истории.

Затем скопируйте (или свяжите) папки `OneWoW*` в `Interface\AddOns` как при обычной установке.

### Обновление позже (командная строка)

```text
cd путь\к\OneWoW_Suite_PlayerRepo
git pull
```

На Mac: `путь/к/OneWoW_Suite_PlayerRepo`.

Если копировали папки — скопируйте снова в AddOns. Если связали — весь апдейт это `git pull`.

---

## Расширенно — junction и символические ссылки (без повторного копирования)

**Ссылка** делает так, что `AddOns\OneWoW` указывает на `...\OneWoW_Suite_PlayerRepo\OneWoW`. После этого Pull в Desktop или `git pull` обновляет файлы, которые игра уже использует.

- Сначала закройте World of Warcraft.
- Клонируйте репозиторий через Desktop или Git **до** создания ссылок (целевые папки должны существовать).
- Если `OneWoW` уже **скопирован** в AddOns, удалите или переименуйте эту копию. Ссылку нельзя создать, если папка с таким именем уже есть.
- Одна ссылка на каждую нужную папку аддона. Начните с `OneWoW`.
- Удаление junction или symlink в AddOns снимает только **ссылку**, клон остаётся.

### Windows — junction (без прав администратора)

Junction (`mklink /J`) не требует командной строки от администратора. Символическая ссылка (`mklink /D`) часто требует — используйте `/J`.

1. Откройте **командную строку** (cmd).
2. Подставьте свои пути: настоящая папка `AddOns` WoW и настоящая папка клона.
3. По одной строке на аддон:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\ВАШЕИМЯ\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Пример для Bags:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\ВАШЕИМЯ\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

Повторите для каждой используемой папки `OneWoW_*` (включая данные Catalog и компаньоны AltTracker).

**PowerShell:**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\ВАШЕИМЯ\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Если Windows пишет, что путь уже существует, в AddOns ещё лежит папка. Удалите или переименуйте её и повторите команду.

### macOS — символическая ссылка

1. Откройте **Терминал**.
2. Подставьте пути вашего Mac.
3. Выполните:

```text
ln -s "/Users/ВАШЕИМЯ/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

Повторите для каждой папки. Если `AddOns/OneWoW` уже существует как обычная копия, сначала перетащите её в Корзину.

### Проверка

Откройте `AddOns\OneWoW` (или путь на Mac). Должны быть те же файлы, что в клоне. После Pull они изменятся без повторного копирования.

### Отменить ссылку

Удалите только связанную папку **внутри AddOns**. Клон `OneWoW_Suite_PlayerRepo` останется. Можно снова копировать папки вручную.

---

## Папки в этом репозитории

| Тип | Папки |
|-----|-------|
| **Обязательно** | `OneWoW` |
| **Функции** | `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit` |
| **Данные Catalog** | `OneWoW_CatalogData_Journal`, `OneWoW_CatalogData_Vendors`, `OneWoW_CatalogData_Tradeskills`, `OneWoW_CatalogData_Quests`, `OneWoW_CatalogData_Quests_Archive` |
| **Данные AltTracker** | `OneWoW_AltTracker_Storage`, `OneWoW_AltTracker_Character`, `OneWoW_AltTracker_Professions`, `OneWoW_AltTracker_Collections`, `OneWoW_AltTracker_Endgame`, `OneWoW_AltTracker_Auctions`, `OneWoW_AltTracker_Accounting` |
| **По желанию** | `OneWoW_Utility_DevTool` (`/1wdt`) |

---

## Частые проблемы

| Что видно | Что делать |
|-----------|------------|
| Нет OneWoW на выборе персонажа | Папки `OneWoW` нет в AddOns или она вложена в другую папку. |
| Функция включена, но пусто | Скопируйте также папки данных Catalog или AltTracker и включите их. |
| Pull прошёл, а игра выглядит старой | Вы копировали один раз. Скопируйте снова после Pull или сделайте junction/symlink. |
| Не работают `mklink` / `ln` | В AddOns уже есть настоящая папка с таким именем или путь указан неверно. |
| Аддоны не загружаются | Проверьте `_retail_` и что папки лежат сразу в `AddOns`. |

---

## Помощь

- Вики: [https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- Поддержка: [https://wow2.xyz/support/](https://wow2.xyz/support/)
- Полный исходный код (вклад): [https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**Автор:** MichinMuggin / Ricky

**Сайт:** https://wow2.xyz/

**Все права защищены.**
