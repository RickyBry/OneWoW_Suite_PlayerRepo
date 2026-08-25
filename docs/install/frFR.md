# OneWoW Suite — installation joueur

**Langue :** [English](../../README.md) · [Deutsch](deDE.md) · [Español (España)](esES.md) · [Español (México)](esMX.md) · Français · [Italiano](itIT.md) · [한국어](koKR.md) · [Português (Brasil)](ptBR.md) · [Русский](ruRU.md) · [简体中文](zhCN.md) · [繁體中文](zhTW.md)

Ce dépôt est la copie **joueur** de OneWoW : uniquement les dossiers d'addons à placer dans World of Warcraft. Il est mis à jour depuis le [dépôt Suite complet](https://github.com/kellewic/OneWoW_Suite). Vous n'avez pas besoin de ce grand dépôt de développement pour jouer.

- **Site :** [https://wow2.xyz/](https://wow2.xyz/)
- **Wiki joueur :** [Installation](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [Prise en main](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **Support :** [https://wow2.xyz/support/](https://wow2.xyz/support/)

C'est un miroir. N'ouvrez pas d'issues ni de pull requests ici. Utilisez le dépôt Suite ou la page de support.

Les étapes **normales** (GitHub Desktop) et les étapes **avancées** (ligne de commande et liens pour ne plus copier les dossiers) sont sur cette même page.

---

## Ce qu'il vous faut

- **World of Warcraft Retail** (cette suite n'est pas pour Classic)
- Un dossier sur l'ordinateur pour garder ce dépôt (Documents convient)
- **GitHub Desktop** (recommandé) ou **Git** si vous préférez le terminal

### Téléchargements

| Quoi | Pour qui | Lien |
|------|----------|------|
| **GitHub Desktop** | Windows 10/11 et macOS — le plus simple | [desktop.github.com](https://desktop.github.com/) |
| **Git** | Ligne de commande uniquement | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Git pour Windows** | Terminal Windows | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **Git pour macOS** | Terminal Mac (ou Xcode Command Line Tools) | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

Si vous utilisez GitHub Desktop, vous n'avez **pas** besoin d'installer Git à part. Desktop l'inclut.

Adresse du dépôt (à coller plus tard) :

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## Trouver le dossier AddOns

WoW ne charge que les addons placés **directement** dans `Interface\AddOns` (chaque dossier s'appelle `OneWoW`, `OneWoW_Bags`, etc.).

**Windows (typique) :**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS (typique) :**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

Si ces chemins sont faux, le jeu est installé ailleurs :

1. Ouvrez l'application **Battle.net**.
2. Sélectionnez **World of Warcraft**.
3. Ouvrez l'**engrenage** / les options à côté de Jouer.
4. Dans **Paramètres du jeu**, trouvez le dossier d'installation, ou utilisez **Afficher le dossier** / **Ouvrir le dossier**.

Il faut `_retail_` (Retail), pas `_classic_` ni `_classic_era_`. Si `Interface` et `AddOns` n'existent pas, créez-les dans `_retail_`.

---

## Installation normale — GitHub Desktop

Utilisez ceci si vous ne voulez pas taper de commandes.

### 1. Installer GitHub Desktop

1. Ouvrez [https://desktop.github.com/](https://desktop.github.com/).
2. Téléchargez l'installateur **Windows** ou **macOS**. Le site choisit le bon fichier.
3. Lancez l'installateur et terminez la configuration.
4. Vous pouvez vous connecter avec un compte GitHub. Pour ce dépôt **public**, c'est facultatif. Vous pouvez cloner sans compte.

### 2. Cloner ce dépôt (l'enregistrer dans un dossier)

« Cloner » signifie : télécharger le dépôt dans un dossier de votre choix, et garder le lien vers GitHub pour mettre à jour plus tard.

1. Ouvrez **GitHub Desktop**.
2. **File → Clone repository** (Fichier → Cloner le dépôt).
3. Ouvrez l'onglet **URL**.
4. Collez :

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. Dans **Local path**, choisissez un dossier facile à retrouver, par exemple :

   - Windows : `C:\Users\VOTRENOM\Documents\OneWoW_Suite_PlayerRepo`
   - Mac : `/Users/VOTRENOM/Documents/OneWoW_Suite_PlayerRepo`

   Ce dossier n'est **pas** le dossier AddOns de WoW. C'est une copie de travail. Ensuite, vous copiez ou liez depuis ici vers AddOns.

6. Cliquez sur **Clone** et attendez que les fichiers apparaissent.

Une fois terminé, vous devez voir `OneWoW`, `OneWoW_Bags`, `OneWoW_QoL` et les autres dossiers `OneWoW_*`.

### 3. Mettre les addons dans le jeu

1. Ouvrez le dossier cloné.
2. Ouvrez `Interface\AddOns` (voir plus haut).
3. Copiez les dossiers d'addons voulus **dans** `AddOns`.

**Obligatoire :** `OneWoW` (le hub). Sans lui, le reste ne se charge pas.

**Optionnels :** `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit`.

**Si vous utilisez Catalog**, copiez aussi tous les dossiers `OneWoW_CatalogData_*` sinon ces onglets seront vides.

**Si vous utilisez AltTracker**, copiez aussi tous les dossiers compagnons `OneWoW_AltTracker_*`.

**DevTool** (`OneWoW_Utility_DevTool`) est facultatif. C'est un inspecteur en jeu (`/1wdt`), pas nécessaire pour jouer.

Vous n'avez pas besoin de tout copier. Seulement ce que vous activerez.

**Ne** placez pas tout le dépôt dans AddOns comme un seul dossier `OneWoW_Suite_PlayerRepo`. WoW ne verra pas `OneWoW` s'il est un niveau trop bas.

Après la copie, `AddOns` doit ressembler à :

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

et non :

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. Les activer dans WoW

1. À l'écran de **sélection de personnage**, cliquez sur **Addons**.
2. Activez **OneWoW** et chaque module optionnel copié.
3. Connectez-vous (ou tapez `/reload` si vous étiez déjà en jeu).
4. Tapez `/1w` pour ouvrir le hub.
5. Dans **Manage Features**, activez ou désactivez les modules. Désactiver **décharge** l'addon ; il n'est pas seulement masqué.

### 5. Mettre à jour plus tard (Desktop)

1. Ouvrez **GitHub Desktop**.
2. Vérifiez que ce dépôt est sélectionné en haut.
3. Cliquez sur **Fetch origin**. Cela interroge GitHub pour de nouveaux fichiers.
4. Si **Pull origin** apparaît, cliquez. Les changements arrivent dans votre dossier cloné.

Si vous avez **copié** les dossiers vers AddOns, recopiez-les après chaque pull et remplacez les anciens. Windows et macOS demandent de remplacer : acceptez.

Si vous avez utilisé des **jonctions ou liens symboliques** (section avancée), le Pull suffit. Le jeu pointe déjà vers ce dossier.

Fermez WoW avant de remplacer des fichiers si le jeu tourne. C'est plus sûr.

---

## Autre option simple — ZIP (pas de mises à jour)

Sur la page du dépôt : **Code → Download ZIP**, décompressez, puis copiez les dossiers `OneWoW*` dans AddOns comme ci-dessus.

Un ZIP est une photo complète à chaque fois. Il ne se met pas à jour tout seul. Préférez Desktop ou Git pour un `pull` plus tard. **CurseForge** et le ZIP Discord conviennent si vous ne voulez pas de Git.

---

## Avancé — Git en ligne de commande

Si vous êtes à l'aise dans un terminal. Installez d'abord [Git](https://git-scm.com/downloads) ([Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)). Sur Mac, `xcode-select --install` fonctionne aussi.

Ouvrez **Git Bash** ou **PowerShell** sous Windows, ou **Terminal** sur Mac. Placez-vous avec `cd` où le dossier doit être créé (Documents par exemple), puis :

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` ne télécharge que les fichiers actuels, pas tout l'historique.

Ensuite, copiez (ou liez) les dossiers `OneWoW*` dans `Interface\AddOns` comme pour l'installation normale.

### Mettre à jour plus tard (ligne de commande)

```text
cd chemin\vers\OneWoW_Suite_PlayerRepo
git pull
```

Sur Mac : `chemin/vers/OneWoW_Suite_PlayerRepo`.

Si vous avez copié les dossiers, recopiez-les dans AddOns. Si vous les avez liés, `git pull` est toute la mise à jour.

---

## Avancé — jonctions et liens symboliques (plus de copies)

Un **lien** fait pointer `AddOns\OneWoW` vers `...\OneWoW_Suite_PlayerRepo\OneWoW`. Ensuite, Pull dans Desktop ou `git pull` met à jour les fichiers que le jeu utilise déjà.

- Fermez World of Warcraft d'abord.
- Clonez le dépôt avec Desktop ou Git **avant** de créer des liens (les dossiers cibles doivent exister).
- Si vous avez déjà **copié** `OneWoW` dans AddOns, supprimez ou renommez cette copie. Un lien ne peut pas être créé si un vrai dossier du même nom est déjà là.
- Un lien par dossier d'addon voulu. Commencez par `OneWoW`.
- Supprimer une jonction ou un lien dans AddOns enlève le **lien**, pas votre clone.

### Windows — jonction (sans Administrateur)

Une jonction (`mklink /J`) n'a pas besoin d'une invite de commandes administrateur. Un symlink (`mklink /D`) en a souvent besoin : utilisez `/J`.

1. Ouvrez l'**invite de commandes** (cmd).
2. Adaptez les deux chemins : votre vrai dossier `AddOns` WoW, et votre vrai dossier cloné.
3. Une ligne par addon :

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\VOTRENOM\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Exemple Bags :

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\VOTRENOM\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

Répétez pour chaque dossier `OneWoW_*` utilisé (données Catalog et compagnons AltTracker inclus).

**PowerShell :**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\VOTRENOM\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Si Windows dit que le chemin existe déjà, un dossier est encore dans AddOns. Retirez-le ou renommez-le, puis relancez la commande.

### macOS — lien symbolique

1. Ouvrez **Terminal**.
2. Adaptez les deux chemins à votre Mac.
3. Exécutez :

```text
ln -s "/Users/VOTRENOM/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

Répétez pour chaque dossier. Si `AddOns/OneWoW` existe déjà en vraie copie, mettez-le d'abord à la Corbeille.

### Vérifier

Ouvrez `AddOns\OneWoW` (ou le chemin Mac). Vous devez voir les mêmes fichiers que dans le clone. Après un Pull, ces fichiers changent sans nouvelle copie.

### Annuler un lien

Supprimez uniquement le dossier lié **dans AddOns**. Le clone `OneWoW_Suite_PlayerRepo` reste. Vous pouvez revenir à la copie classique.

---

## Dossiers de ce dépôt

| Type | Dossiers |
|------|----------|
| **Obligatoire** | `OneWoW` |
| **Fonctions** | `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit` |
| **Données Catalog** | `OneWoW_CatalogData_Journal`, `OneWoW_CatalogData_Vendors`, `OneWoW_CatalogData_Tradeskills`, `OneWoW_CatalogData_Quests`, `OneWoW_CatalogData_Quests_Archive` |
| **Données AltTracker** | `OneWoW_AltTracker_Storage`, `OneWoW_AltTracker_Character`, `OneWoW_AltTracker_Professions`, `OneWoW_AltTracker_Collections`, `OneWoW_AltTracker_Endgame`, `OneWoW_AltTracker_Auctions`, `OneWoW_AltTracker_Accounting` |
| **Facultatif** | `OneWoW_Utility_DevTool` (`/1wdt`) |

---

## Problèmes fréquents

| Ce que vous voyez | Que faire |
|-------------------|-----------|
| Pas de OneWoW à la sélection de personnage | `OneWoW` manque dans AddOns, ou il est dans un sous-dossier. |
| Fonction activée mais vide | Copiez aussi les dossiers de données Catalog ou AltTracker et activez-les. |
| Le Pull a marché mais le jeu semble ancien | Vous avez copié une fois. Recopiez après le Pull, ou utilisez jonctions/liens. |
| `mklink` / `ln` échoue | Un vrai dossier de ce nom existe encore dans AddOns, ou un chemin est faux. |
| Les addons ne se chargent pas | Vérifiez `_retail_` et que les dossiers sont directement dans `AddOns`. |

---

## Aide

- Wiki joueur : [https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- Support : [https://wow2.xyz/support/](https://wow2.xyz/support/)
- Code complet (contribuer) : [https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**Auteur :** MichinMuggin / Ricky

**Site :** https://wow2.xyz/

**Tous droits réservés.**
