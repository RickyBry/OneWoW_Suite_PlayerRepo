# OneWoW Suite — installazione per i giocatori

**Lingua:** [English](../../README.md) · [Deutsch](deDE.md) · [Español (España)](esES.md) · [Español (México)](esMX.md) · [Français](frFR.md) · Italiano · [한국어](koKR.md) · [Português (Brasil)](ptBR.md) · [Русский](ruRU.md) · [简体中文](zhCN.md) · [繁體中文](zhTW.md)

Questo repository è la copia **per i giocatori** di OneWoW: solo le cartelle addon da mettere in World of Warcraft. Viene aggiornato dal [repository Suite completo](https://github.com/kellewic/OneWoW_Suite). Non ti serve quel repo di sviluppo per giocare.

- **Sito:** [https://wow2.xyz/](https://wow2.xyz/)
- **Wiki:** [Installazione](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [Per iniziare](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **Supporto:** [https://wow2.xyz/support/](https://wow2.xyz/support/)

Questo è uno specchio. Non aprire issue o pull request qui. Usa il repo Suite o la pagina di supporto.

I passi **normali** (GitHub Desktop) e quelli **avanzati** (riga di comando e collegamenti per non ricopiare le cartelle) sono sulla stessa pagina.

---

## Cosa ti serve

- **World of Warcraft Retail** (questa suite non è per Classic)
- Una cartella sul computer per tenere questo repo (Documenti va bene)
- **GitHub Desktop** (consigliato) oppure **Git** se preferisci il terminale

### Download

| Cosa | Per chi | Link |
|------|---------|------|
| **GitHub Desktop** | Windows 10/11 e macOS — il modo più semplice | [desktop.github.com](https://desktop.github.com/) |
| **Git** | Solo riga di comando | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Git per Windows** | Terminale Windows | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **Git per macOS** | Terminale Mac (o Xcode Command Line Tools) | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

Se usi GitHub Desktop **non** devi installare Git a parte. Desktop lo include già.

Indirizzo del repository (lo incollerai dopo):

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## Trovare la cartella AddOns

WoW carica solo gli addon che stanno **direttamente** in `Interface\AddOns` (ogni cartella si chiama `OneWoW`, `OneWoW_Bags`, e così via).

**Windows (tipico):**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS (tipico):**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

Se quei percorsi sono sbagliati, il gioco è installato altrove:

1. Apri l'app **Battle.net**.
2. Seleziona **World of Warcraft**.
3. Apri l'**ingranaggio** / le opzioni accanto a Gioca.
4. In **Impostazioni di gioco** trova la cartella di installazione, oppure usa **Mostra cartella** / **Apri cartella**.

Ti serve `_retail_` (Retail), non `_classic_` o `_classic_era_`. Se `Interface` e `AddOns` non esistono, creale dentro `_retail_`.

---

## Installazione normale — GitHub Desktop

Usa questa se non vuoi scrivere comandi.

### 1. Installa GitHub Desktop

1. Apri [https://desktop.github.com/](https://desktop.github.com/).
2. Scarica l'installer per **Windows** o **macOS**. Il sito sceglie quello giusto.
3. Avvia l'installer e completa la configurazione.
4. Puoi accedere con un account GitHub. Per questo repo **pubblico** è facoltativo. Puoi clonare senza account.

### 2. Clona questo repository (salvalo in una cartella)

«Clonare» significa: scaricare il repo in una cartella che scegli e tenere il collegamento a GitHub per aggiornare dopo.

1. Apri **GitHub Desktop**.
2. **File → Clone repository** (File → Clona repository).
3. Apri la scheda **URL**.
4. Incolla:

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. In **Local path** scegli una cartella facile da ritrovare, ad esempio:

   - Windows: `C:\Users\TUONOME\Documents\OneWoW_Suite_PlayerRepo`
   - Mac: `/Users/TUONOME/Documents/OneWoW_Suite_PlayerRepo`

   Questa cartella **non** è AddOns di WoW. È una copia di lavoro. Nel passo successivo copi o colleghi da qui verso AddOns.

6. Clicca **Clone** e aspetta che compaiano i file.

Quando ha finito dovresti vedere `OneWoW`, `OneWoW_Bags`, `OneWoW_QoL` e le altre cartelle `OneWoW_*`.

### 3. Metti gli addon nel gioco

1. Apri la cartella clonata.
2. Apri `Interface\AddOns` (vedi sopra).
3. Copia le cartelle addon che vuoi **dentro** `AddOns`.

**Obbligatorio:** `OneWoW` (l'hub). Senza di esso il resto non si carica.

**Opzionali:** `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit`.

**Se usi Catalog**, copia anche tutte le cartelle `OneWoW_CatalogData_*` o quelle schede resteranno vuote.

**Se usi AltTracker**, copia anche tutte le cartelle companion `OneWoW_AltTracker_*`.

**DevTool** (`OneWoW_Utility_DevTool`) è opzionale. È un ispettore in gioco (`/1wdt`), non serve per giocare.

Non devi copiare tutto. Solo ciò che attiverai.

**Non** mettere l'intero repo in AddOns come una sola cartella `OneWoW_Suite_PlayerRepo`. WoW non vede `OneWoW` se è un livello troppo in profondità.

Dopo la copia, `AddOns` deve assomigliare a:

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

non a:

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. Attivali in WoW

1. Nella schermata di **selezione personaggio**, clicca **Addons**.
2. Attiva **OneWoW** e ogni modulo opzionale che hai copiato.
3. Entra (o scrivi `/reload` se eri già nel mondo).
4. Digita `/1w` per aprire l'hub.
5. In **Manage Features** attiva o disattiva i moduli. Disattivare **scarica** l'addon; non lo nasconde soltanto.

### 5. Aggiornare dopo (Desktop)

1. Apri **GitHub Desktop**.
2. Controlla che questo repository sia selezionato in alto.
3. Clicca **Fetch origin**. Controlla su GitHub se ci sono file nuovi.
4. Se compare **Pull origin**, cliccalo. Le modifiche arrivano nella cartella clonata.

Se hai **copiato** le cartelle in AddOns, copiale di nuovo dopo ogni pull e sovrascrivi le vecchie. Windows e macOS chiedono di sostituire: accetta.

Se hai usato **junction o symlink** (sezione avanzata), il Pull basta. Il gioco punta già a questa cartella.

Chiudi WoW prima di sostituire i file se il gioco è aperto. È più sicuro.

---

## Altra opzione semplice — ZIP (niente aggiornamenti)

Nella pagina del repo: **Code → Download ZIP**, estrai e copia le cartelle `OneWoW*` in AddOns come sopra.

Uno ZIP è un'istantanea completa ogni volta. Non si aggiorna da solo. Meglio Desktop o Git se vuoi fare `pull`. **CurseForge** e lo ZIP Discord vanno bene se non vuoi Git.

---

## Avanzato — Git da riga di comando

Se sei a tuo agio nel terminale. Installa prima [Git](https://git-scm.com/downloads) ([Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)). Su Mac puoi anche usare `xcode-select --install`.

Apri **Git Bash** o **PowerShell** su Windows, o **Terminal** su Mac. Vai con `cd` dove vuoi creare la cartella (ad esempio Documenti), poi:

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` scarica solo i file attuali, non tutta la cronologia.

Poi copia (o collega) le cartelle `OneWoW*` in `Interface\AddOns` come nell'installazione normale.

### Aggiornare dopo (riga di comando)

```text
cd percorso\a\OneWoW_Suite_PlayerRepo
git pull
```

Su Mac usa `percorso/a/OneWoW_Suite_PlayerRepo`.

Se hai copiato le cartelle, copiale di nuovo in AddOns. Se le hai collegate, `git pull` è tutto l'aggiornamento.

---

## Avanzato — junction e symlink (niente più copie)

Un **collegamento** fa puntare `AddOns\OneWoW` a `...\OneWoW_Suite_PlayerRepo\OneWoW`. Dopo, Pull in Desktop o `git pull` aggiorna i file che il gioco usa già.

- Chiudi prima World of Warcraft.
- Clona il repo con Desktop o Git **prima** di creare i collegamenti (le cartelle di destinazione devono esistere).
- Se hai già **copiato** `OneWoW` in AddOns, elimina o rinomina quella copia. Non si può creare il collegamento se esiste già una cartella vera con lo stesso nome.
- Un collegamento per ogni cartella addon che vuoi. Inizia da `OneWoW`.
- Eliminare junction o symlink in AddOns toglie il **collegamento**, non il clone.

### Windows — junction (senza Amministratore)

Una junction (`mklink /J`) non richiede il prompt dei comandi come amministratore. Un symlink (`mklink /D`) spesso sì: usa `/J`.

1. Apri il **Prompt dei comandi** (cmd).
2. Adatta entrambi i percorsi: la vera cartella `AddOns` di WoW e la vera cartella clonata.
3. Una riga per addon:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\TUONOME\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Esempio Bags:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\TUONOME\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

Ripeti per ogni cartella `OneWoW_*` che usi (inclusi i dati Catalog e i companion AltTracker).

**PowerShell:**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\TUONOME\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Se Windows dice che il percorso esiste già, c'è ancora una cartella in AddOns. Rimuovila o rinominala, poi rilancia il comando.

### macOS — symlink

1. Apri **Terminal**.
2. Adatta entrambi i percorsi al tuo Mac.
3. Esegui:

```text
ln -s "/Users/TUONOME/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

Ripeti per ogni cartella. Se `AddOns/OneWoW` esiste già come copia reale, spostala prima nel Cestino.

### Controllare che funzioni

Apri `AddOns\OneWoW` (o il percorso Mac). Devi vedere gli stessi file del clone. Dopo un Pull quei file cambiano senza un'altra copia.

### Annullare un collegamento

Elimina solo la cartella collegata **dentro AddOns**. Il clone `OneWoW_Suite_PlayerRepo` resta. Puoi tornare a copiare le cartelle se preferisci.

---

## Cartelle in questo repo

| Tipo | Cartelle |
|------|----------|
| **Obbligatorio** | `OneWoW` |
| **Funzioni** | `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit` |
| **Dati Catalog** | `OneWoW_CatalogData_Journal`, `OneWoW_CatalogData_Vendors`, `OneWoW_CatalogData_Tradeskills`, `OneWoW_CatalogData_Quests`, `OneWoW_CatalogData_Quests_Archive` |
| **Dati AltTracker** | `OneWoW_AltTracker_Storage`, `OneWoW_AltTracker_Character`, `OneWoW_AltTracker_Professions`, `OneWoW_AltTracker_Collections`, `OneWoW_AltTracker_Endgame`, `OneWoW_AltTracker_Auctions`, `OneWoW_AltTracker_Accounting` |
| **Facoltativo** | `OneWoW_Utility_DevTool` (`/1wdt`) |

---

## Problemi comuni

| Cosa vedi | Cosa fare |
|-----------|-----------|
| Nessun OneWoW alla selezione personaggio | Manca `OneWoW` in AddOns, oppure è dentro un'altra cartella. |
| Funzione attiva ma vuota | Copia anche le cartelle dati di Catalog o AltTracker e attivale. |
| Il Pull funziona ma il gioco sembra vecchio | Hai copiato una volta. Copia di nuovo dopo il Pull, oppure usa junction/symlink. |
| `mklink` / `ln` fallisce | Esiste già una cartella vera con quel nome in AddOns, o un percorso è sbagliato. |
| Gli addon non si caricano | Controlla `_retail_` e che le cartelle siano direttamente in `AddOns`. |

---

## Aiuto

- Wiki: [https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- Supporto: [https://wow2.xyz/support/](https://wow2.xyz/support/)
- Codice completo (contribuire): [https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**Autore:** MichinMuggin / Ricky

**Sito:** https://wow2.xyz/

**Tutti i diritti riservati.**
