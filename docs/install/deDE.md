# OneWoW Suite — Installation für Spieler

**Sprache:** [English](../../README.md) · Deutsch · [Español (España)](esES.md) · [Español (México)](esMX.md) · [Français](frFR.md) · [Italiano](itIT.md) · [한국어](koKR.md) · [Português (Brasil)](ptBR.md) · [Русский](ruRU.md) · [简体中文](zhCN.md) · [繁體中文](zhTW.md)

Dieses Repository ist die **Spieler**-Kopie von OneWoW: nur die Addon-Ordner, die ins Spiel gehören. Es wird aus dem vollständigen [Suite-Repository](https://github.com/kellewic/OneWoW_Suite) aktuell gehalten. Das große Entwickler-Repo brauchen Sie zum Spielen nicht.

- **Website:** [https://wow2.xyz/](https://wow2.xyz/)
- **Spieler-Wiki:** [Installation](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [Erste Schritte](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **Support:** [https://wow2.xyz/support/](https://wow2.xyz/support/)

Dies ist ein Spiegel. Bitte keine Issues oder Pull Requests hier öffnen. Nutzen Sie das Suite-Repo oder die Support-Seite.

Die **normalen** Schritte (GitHub Desktop) und die **erweiterten** Schritte (Kommandozeile und Verknüpfungen, damit Sie Ordner nicht erneut kopieren müssen) stehen auf derselben Seite.

---

## Was Sie brauchen

- **World of Warcraft Retail** (nicht Classic)
- Einen Ordner auf dem Rechner für dieses Repo (Dokumente sind in Ordnung)
- **GitHub Desktop** (empfohlen) oder **Git**, wenn Sie die Kommandozeile bevorzugen

### Downloads

| Was | Für wen | Link |
|-----|---------|------|
| **GitHub Desktop** | Windows 10/11 und macOS — der einfachste Weg | [desktop.github.com](https://desktop.github.com/) |
| **Git** | Nur Kommandozeile | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Git für Windows** | Windows-Kommandozeile | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **Git für macOS** | Mac-Kommandozeile (oder Xcode Command Line Tools) | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

Wenn Sie GitHub Desktop nutzen, müssen Sie Git **nicht** extra installieren. Desktop bringt alles mit.

Adresse des Repositories (später einfügen):

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## Den AddOns-Ordner finden

WoW lädt nur Addons, die **direkt** in `Interface\AddOns` liegen (Ordner namens `OneWoW`, `OneWoW_Bags` usw.).

**Windows (typisch):**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS (typisch):**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

Wenn der Pfad nicht stimmt, ist das Spiel woanders installiert:

1. **Battle.net**-App öffnen.
2. **World of Warcraft** wählen.
3. Das **Zahnrad** / die Optionen neben Play öffnen.
4. Unter **Spieleinstellungen** den Installationsordner suchen oder **Ordner anzeigen** / **Ordner öffnen** nutzen.

Wichtig ist `_retail_` (Retail), nicht `_classic_` oder `_classic_era_`. Fehlen `Interface` und `AddOns`, legen Sie diese zwei Ordner in `_retail_` an.

---

## Normale Installation — GitHub Desktop

Nutzen Sie das, wenn Sie keine Befehle tippen möchten.

### 1. GitHub Desktop installieren

1. [https://desktop.github.com/](https://desktop.github.com/) öffnen.
2. Den Installer für **Windows** oder **macOS** herunterladen. Die Seite wählt die passende Datei.
3. Installer starten und die Einrichtung abschließen.
4. Eine Anmeldung bei GitHub ist möglich. Für dieses **öffentliche** Repo ist sie optional. Klonen geht ohne Konto.

### 2. Repository klonen (in einen Ordner speichern)

„Klonen“ heißt: Das Repo in einen Ordner Ihrer Wahl laden und die Verbindung zu GitHub behalten, damit Sie später aktualisieren können.

1. **GitHub Desktop** öffnen.
2. **File → Clone repository** (Datei → Repository klonen).
3. Den Tab **URL** öffnen.
4. Einfügen:

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. Unter **Local path** einen einfachen Ordner wählen, den Sie wiederfinden, zum Beispiel:

   - Windows: `C:\Users\IHRNAME\Documents\OneWoW_Suite_PlayerRepo`
   - Mac: `/Users/IHRNAME/Documents/OneWoW_Suite_PlayerRepo`

   Das ist **nicht** der WoW-AddOns-Ordner, sondern eine Zwischenkopie. Im nächsten Schritt kopieren oder verknüpfen Sie von hier nach AddOns.

6. **Clone** klicken und warten, bis die Dateien da sind.

Danach sollten `OneWoW`, `OneWoW_Bags`, `OneWoW_QoL` und die anderen `OneWoW_*`-Ordner sichtbar sein.

### 3. Addons ins Spiel legen

1. Den gerade gespeicherten Klon-Ordner öffnen.
2. Den Ordner `Interface\AddOns` öffnen (siehe oben).
3. Die gewünschten Addon-Ordner **nach** `AddOns` kopieren.

**Pflicht:** `OneWoW` (die Zentrale). Ohne diesen Ordner laden die anderen nicht.

**Optionale Features:** `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit`.

**Wenn Sie Catalog nutzen**, kopieren Sie auch alle Ordner `OneWoW_CatalogData_*`, sonst bleiben die Reiter leer.

**Wenn Sie AltTracker nutzen**, kopieren Sie auch alle Begleitordner `OneWoW_AltTracker_*`.

**DevTool** (`OneWoW_Utility_DevTool`) ist optional. Es ist ein Inspektor im Spiel (`/1wdt`), zum Spielen nicht nötig.

Sie müssen nicht jeden Ordner kopieren. Nur das, was Sie einschalten wollen.

**Nicht** das ganze Repo als einen Ordner `OneWoW_Suite_PlayerRepo` nach AddOns legen. WoW findet `OneWoW` nicht, wenn es eine Ebene zu tief liegt.

Nach dem Kopieren sollte `AddOns` so aussehen:

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

nicht:

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. Im Spiel einschalten

1. Auf dem **Charakterauswahl**-Bildschirm auf **Addons** klicken.
2. **OneWoW** und jedes kopierte optionale Modul aktivieren.
3. Einloggen (oder `/reload`, wenn Sie schon in der Welt sind).
4. `/1w` tippen, um die Zentrale zu öffnen.
5. Unter **Manage Features** Module ein- oder ausschalten. Ausschalten **entlädt** das Addon, es wird nicht nur versteckt.

### 5. Später aktualisieren (Desktop)

1. **GitHub Desktop** öffnen.
2. Oben dieses Repository auswählen.
3. **Fetch origin** klicken. Das prüft GitHub auf neue Dateien.
4. Wenn **Pull origin** angeboten wird, darauf klicken. Die Änderungen landen im Klon-Ordner.

Wenn Sie Ordner nach AddOns **kopiert** haben: nach jedem Pull erneut kopieren und ersetzen. Windows und macOS fragen nach dem Ersetzen — mit Ja bestätigen.

Wenn Sie **Junctions oder Symlinks** nutzen (Abschnitt unten), reicht Pull. Das Spiel zeigt bereits auf diesen Ordner.

WoW vor dem Ersetzen schließen, wenn das Spiel läuft. Das ist die sichere Variante.

---

## Andere einfache Option — ZIP (keine Updates)

Auf der Repo-Seite **Code → Download ZIP**, entpacken, dann die Ordner `OneWoW*` wie oben nach AddOns kopieren.

Ein ZIP ist jedes Mal ein voller Schnappschuss. Es aktualisiert sich nicht selbst. Desktop oder Git sind besser, wenn Sie später `pull` wollen. **CurseForge** und das Discord-Community-ZIP sind in Ordnung, wenn Sie gar kein Git wollen.

---

## Erweitert — Git auf der Kommandozeile

Für alle, die ein Terminal gewohnt sind. Zuerst [Git](https://git-scm.com/downloads) installieren ([Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)). Auf dem Mac geht auch `xcode-select --install` (Git der Command Line Tools).

**Git Bash** oder **PowerShell** unter Windows öffnen, auf dem Mac **Terminal**. Mit `cd` in den Zielordner wechseln (z. B. Dokumente), dann:

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` holt nur die neuesten Dateien, nicht die ganze Historie.

Danach die Ordner `OneWoW*` wie bei der normalen Installation nach `Interface\AddOns` kopieren oder verknüpfen.

### Später aktualisieren (Kommandozeile)

```text
cd pfad\zu\OneWoW_Suite_PlayerRepo
git pull
```

Auf dem Mac: `pfad/zu/OneWoW_Suite_PlayerRepo`.

Nach dem Kopieren erneut nach AddOns kopieren. Bei Verknüpfungen ist `git pull` das gesamte Update.

---

## Erweitert — Junctions und Symlinks (nicht mehr kopieren)

Eine **Verknüpfung** lässt `AddOns\OneWoW` auf `...\OneWoW_Suite_PlayerRepo\OneWoW` zeigen. Danach aktualisiert Desktop-Pull oder `git pull` genau die Dateien, die das Spiel schon nutzt.

- World of Warcraft zuerst schließen.
- Das Repo mit Desktop oder Git **klonen**, bevor Sie Links anlegen (die Zielordner müssen existieren).
- Wenn `OneWoW` schon nach AddOns **kopiert** wurde: Kopie löschen oder umbenennen. Ein Link geht nicht, wenn ein echter Ordner gleichen Namens schon da ist.
- Einen Link pro gewünschtem Addon-Ordner. Beginnen Sie mit `OneWoW`.
- Das Löschen einer Junction/eines Symlinks in AddOns entfernt nur den **Link**, nicht Ihren Klon.

### Windows — Junction (kein Administrator)

Eine Junction (`mklink /J`) braucht keine Eingabeaufforderung als Administrator. Ein Symlink (`mklink /D`) oft schon — nutzen Sie `/J`.

1. **Eingabeaufforderung** (cmd) öffnen.
2. Beide Pfade anpassen: echter WoW-`AddOns`-Ordner und echter Klon-Ordner.
3. Eine Zeile pro Addon:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\IHRNAME\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Beispiel Bags:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\IHRNAME\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

Für jeden genutzten Ordner `OneWoW_*` wiederholen (inkl. Catalog-Daten und AltTracker-Begleiter).

**PowerShell:**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\IHRNAME\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Meldet Windows, der Pfad existiere bereits, liegt noch ein Ordner in AddOns. Entfernen oder umbenennen, dann den Befehl erneut ausführen.

### macOS — Symlink

1. **Terminal** öffnen.
2. Beide Pfade an Ihren Mac anpassen.
3. Ausführen:

```text
ln -s "/Users/IHRNAME/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

Pro Addon-Ordner wiederholen. Existiert `AddOns/OneWoW` schon als echte Kopie, zuerst in den Papierkorb legen.

### Prüfen

`AddOns\OneWoW` (bzw. den Mac-Pfad) öffnen. Sie sollten dieselben Dateien sehen wie im Klon. Nach einem Pull ändern sich die Dateien ohne erneutes Kopieren.

### Link rückgängig machen

Nur den verknüpften Ordner **in AddOns** löschen. Der Klon `OneWoW_Suite_PlayerRepo` bleibt. Sie können wieder ganz normal kopieren.

---

## Ordner in diesem Repo

| Art | Ordner |
|-----|--------|
| **Pflicht** | `OneWoW` |
| **Features** | `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit` |
| **Catalog-Daten** | `OneWoW_CatalogData_Journal`, `OneWoW_CatalogData_Vendors`, `OneWoW_CatalogData_Tradeskills`, `OneWoW_CatalogData_Quests`, `OneWoW_CatalogData_Quests_Archive` |
| **AltTracker-Daten** | `OneWoW_AltTracker_Storage`, `OneWoW_AltTracker_Character`, `OneWoW_AltTracker_Professions`, `OneWoW_AltTracker_Collections`, `OneWoW_AltTracker_Endgame`, `OneWoW_AltTracker_Auctions`, `OneWoW_AltTracker_Accounting` |
| **Optional** | `OneWoW_Utility_DevTool` (`/1wdt`) |

---

## Häufige Probleme

| Symptom | Lösung |
|---------|--------|
| Kein OneWoW in der Charakterauswahl | `OneWoW` fehlt in AddOns oder liegt in einem Unterordner. |
| Feature an, aber leer | Catalog- oder AltTracker-Datenordner mitkopieren und aktivieren. |
| Pull ok, Spiel wirkt alt | Sie haben einmal kopiert. Nach dem Pull erneut kopieren oder Junctions/Symlinks nutzen. |
| `mklink` / `ln` schlägt fehl | Ein echter Ordner gleichen Namens ist noch in AddOns, oder ein Pfad ist falsch. |
| Addons laden nicht | `_retail_` prüfen; die Ordner müssen direkt in `AddOns` liegen. |

---

## Hilfe

- Spieler-Wiki: [https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- Support: [https://wow2.xyz/support/](https://wow2.xyz/support/)
- Vollständiger Quellcode (Mitwirken): [https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**Autor:** MichinMuggin / Ricky

**Website:** https://wow2.xyz/

**Alle Rechte vorbehalten.**
