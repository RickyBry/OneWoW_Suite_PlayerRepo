# OneWoW Suite — instalación para jugadores

**Idioma:** [English](../../README.md) · [Deutsch](deDE.md) · [Español (España)](esES.md) · Español (México) · [Français](frFR.md) · [Italiano](itIT.md) · [한국어](koKR.md) · [Português (Brasil)](ptBR.md) · [Русский](ruRU.md) · [简体中文](zhCN.md) · [繁體中文](zhTW.md)

Este repositorio es la copia **para jugadores** de OneWoW: solo las carpetas de addons que van en World of Warcraft. Se actualiza desde el [repositorio completo de la Suite](https://github.com/kellewic/OneWoW_Suite). No necesitas ese repo de desarrollo para jugar.

- **Sitio:** [https://wow2.xyz/](https://wow2.xyz/)
- **Wiki:** [Instalación](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [Primeros pasos](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **Soporte:** [https://wow2.xyz/support/](https://wow2.xyz/support/)

Esto es un espejo. No abras issues ni pull requests aquí. Usa el repo de la Suite o la página de soporte.

Los pasos **normales** (GitHub Desktop) y los **avanzados** (línea de comandos y vínculos para no volver a copiar carpetas) están en esta misma página.

---

## Qué necesitas

- **World of Warcraft Retail** (esta suite no es para Classic)
- Una carpeta en la computadora para guardar este repo (Documentos está bien)
- **GitHub Desktop** (recomendado) o **Git** si prefieres la terminal

### Descargas

| Qué | Para quién | Enlace |
|-----|------------|--------|
| **GitHub Desktop** | Windows 10/11 y macOS — la forma más fácil | [desktop.github.com](https://desktop.github.com/) |
| **Git** | Solo línea de comandos | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Git para Windows** | Terminal en Windows | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **Git para macOS** | Terminal en Mac (o Xcode Command Line Tools) | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

Si usas GitHub Desktop, **no** hace falta instalar Git por separado. Desktop ya lo trae.

Dirección del repositorio (la vas a pegar después):

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## Encontrar la carpeta AddOns

WoW solo carga addons que estén **directamente** dentro de `Interface\AddOns` (cada carpeta se llama `OneWoW`, `OneWoW_Bags`, etc.).

**Windows (típico):**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS (típico):**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

Si esas rutas no existen, el juego está instalado en otro lado:

1. Abre la app **Battle.net**.
2. Selecciona **World of Warcraft**.
3. Abre el **engrane** / opciones junto a Jugar.
4. En **Configuración del juego** busca la carpeta de instalación, o usa **Mostrar carpeta** / **Abrir carpeta**.

Necesitas `_retail_` (Retail), no `_classic_` ni `_classic_era_`. Si no existen `Interface` y `AddOns`, créalas dentro de `_retail_`.

---

## Instalación normal — GitHub Desktop

Usa esto si no quieres escribir comandos.

### 1. Instalar GitHub Desktop

1. Abre [https://desktop.github.com/](https://desktop.github.com/).
2. Descarga el instalador para **Windows** o **macOS**. El sitio elige el correcto.
3. Ejecuta el instalador y termina la configuración.
4. Puedes iniciar sesión con una cuenta de GitHub. En este repo **público** es opcional. Puedes clonar sin cuenta.

### 2. Clonar este repositorio (guardarlo en una carpeta)

«Clonar» significa: descargar el repo a una carpeta que elijas y mantener el vínculo con GitHub para actualizar después.

1. Abre **GitHub Desktop**.
2. **File → Clone repository** (Archivo → Clonar repositorio).
3. Abre la pestaña **URL**.
4. Pega:

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. En **Local path** elige una carpeta fácil de encontrar, por ejemplo:

   - Windows: `C:\Users\TUNOMBRE\Documents\OneWoW_Suite_PlayerRepo`
   - Mac: `/Users/TUNOMBRE/Documents/OneWoW_Suite_PlayerRepo`

   Esta carpeta **no** es AddOns de WoW. Es una copia de trabajo. En el siguiente paso copias o vinculas desde aquí hacia AddOns.

6. Haz clic en **Clone** y espera a que aparezcan los archivos.

Cuando termine, debes ver `OneWoW`, `OneWoW_Bags`, `OneWoW_QoL` y el resto de carpetas `OneWoW_*`.

### 3. Poner los addons en el juego

1. Abre la carpeta clonada.
2. Abre `Interface\AddOns` (más arriba).
3. Copia las carpetas que quieras **dentro** de `AddOns`.

**Obligatorio:** `OneWoW` (el hub). Sin él, el resto no carga.

**Opcionales:** `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit`.

**Si usas Catalog**, copia también todas las carpetas `OneWoW_CatalogData_*` o esas pestañas se verán vacías.

**Si usas AltTracker**, copia también todas las carpetas compañeras `OneWoW_AltTracker_*`.

**DevTool** (`OneWoW_Utility_DevTool`) es opcional. Es un inspector dentro del juego (`/1wdt`), no hace falta para jugar.

No tienes que copiarlo todo. Solo lo que vayas a activar.

**No** metas el repo entero en AddOns como una carpeta `OneWoW_Suite_PlayerRepo`. WoW no verá `OneWoW` si está un nivel más adentro.

Después de copiar, `AddOns` debe verse así:

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

no así:

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. Activarlos en WoW

1. En la **selección de personaje**, haz clic en **Addons**.
2. Activa **OneWoW** y cada módulo opcional que hayas copiado.
3. Entra (o escribe `/reload` si ya estabas en el mundo).
4. Escribe `/1w` para abrir el hub.
5. En **Manage Features** activa o desactiva módulos. Desactivar **descarga** el addon; no solo lo oculta.

### 5. Actualizar después (Desktop)

1. Abre **GitHub Desktop**.
2. Asegúrate de que este repositorio esté seleccionado arriba.
3. Haz clic en **Fetch origin**. Revisa GitHub por archivos nuevos.
4. Si aparece **Pull origin**, haz clic. Los cambios llegan a tu carpeta clonada.

Si **copiaste** las carpetas a AddOns, vuelve a copiarlas después de cada pull y reemplaza las viejas. Windows y macOS pedirán reemplazar: acepta.

Si usaste **uniones o enlaces simbólicos** (sección avanzada), el Pull alcanza. El juego ya apunta a esta carpeta.

Cierra WoW antes de reemplazar archivos si el juego está abierto. Es lo más seguro.

---

## Otra opción sencilla — ZIP (sin actualizaciones)

En la página del repo: **Code → Download ZIP**, descomprime y copia las carpetas `OneWoW*` a AddOns igual que arriba.

Un ZIP es una foto completa cada vez. No se actualiza solo. Mejor Desktop o Git si quieres hacer `pull`. **CurseForge** y el ZIP de Discord también sirven si no quieres Git.

---

## Avanzado — Git en la terminal

Si te sientes cómodo en una terminal. Instala [Git](https://git-scm.com/downloads) primero ([Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)). En Mac también puedes usar `xcode-select --install`.

Abre **Git Bash** o **PowerShell** en Windows, o **Terminal** en Mac. Entra con `cd` donde quieras crear la carpeta (por ejemplo Documentos) y:

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` descarga solo los archivos actuales, no todo el historial.

Luego copia (o vincula) las carpetas `OneWoW*` en `Interface\AddOns` como en la instalación normal.

### Actualizar después (terminal)

```text
cd ruta\a\OneWoW_Suite_PlayerRepo
git pull
```

En Mac usa `ruta/a/OneWoW_Suite_PlayerRepo`.

Si copiaste carpetas, vuelve a copiarlas a AddOns. Si las vinculaste, `git pull` es toda la actualización.

---

## Avanzado — uniones y enlaces simbólicos (sin volver a copiar)

Un **vínculo** hace que `AddOns\OneWoW` apunte a `...\OneWoW_Suite_PlayerRepo\OneWoW`. Después, Pull en Desktop o `git pull` actualiza los archivos que el juego ya usa.

- Cierra World of Warcraft primero.
- Clona el repo con Desktop o Git **antes** de crear vínculos (las carpetas de destino deben existir).
- Si ya **copiaste** `OneWoW` a AddOns, borra o renombra esa copia. No se puede crear el vínculo si ya hay una carpeta real con el mismo nombre.
- Un vínculo por cada carpeta de addon que quieras. Empieza por `OneWoW`.
- Borrar la unión o el enlace en AddOns quita el **vínculo**, no tu clon.

### Windows — unión (sin Administrador)

Una unión (`mklink /J`) no necesita el símbolo del sistema como administrador. Un symlink (`mklink /D`) suele necesitarlo: usa `/J`.

1. Abre el **símbolo del sistema** (cmd).
2. Ajusta las dos rutas: tu `AddOns` real de WoW y tu carpeta clonada real.
3. Una línea por addon:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\TUNOMBRE\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Ejemplo para Bags:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\TUNOMBRE\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

Repite por cada carpeta `OneWoW_*` que uses (incluidos datos de Catalog y compañeros de AltTracker).

**PowerShell:**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\TUNOMBRE\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Si Windows dice que la ruta ya existe, todavía hay una carpeta en AddOns. Quítala o renuómbrala y vuelve a ejecutar el comando.

### macOS — enlace simbólico

1. Abre **Terminal**.
2. Ajusta las dos rutas a tu Mac.
3. Ejecuta:

```text
ln -s "/Users/TUNOMBRE/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

Repite por cada carpeta. Si `AddOns/OneWoW` ya existe como copia real, muévela a la Papelera primero.

### Comprobar que funciona

Abre `AddOns\OneWoW` (o la ruta del Mac). Debes ver los mismos archivos que en el clon. Tras un Pull, esos archivos cambian sin copiar otra vez.

### Deshacer un vínculo

Borra solo la carpeta vinculada **dentro de AddOns**. El clon `OneWoW_Suite_PlayerRepo` se queda. Puedes volver a copiar carpetas si quieres.

---

## Carpetas de este repo

| Tipo | Carpetas |
|------|----------|
| **Obligatorio** | `OneWoW` |
| **Funciones** | `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit` |
| **Datos de Catalog** | `OneWoW_CatalogData_Journal`, `OneWoW_CatalogData_Vendors`, `OneWoW_CatalogData_Tradeskills`, `OneWoW_CatalogData_Quests`, `OneWoW_CatalogData_Quests_Archive` |
| **Datos de AltTracker** | `OneWoW_AltTracker_Storage`, `OneWoW_AltTracker_Character`, `OneWoW_AltTracker_Professions`, `OneWoW_AltTracker_Collections`, `OneWoW_AltTracker_Endgame`, `OneWoW_AltTracker_Auctions`, `OneWoW_AltTracker_Accounting` |
| **Opcional** | `OneWoW_Utility_DevTool` (`/1wdt`) |

---

## Problemas frecuentes

| Qué ves | Qué hacer |
|---------|-----------|
| No aparece OneWoW en la selección de personaje | Falta `OneWoW` en AddOns o está dentro de otra carpeta. |
| Función activa pero vacía | Copia también las carpetas de datos de Catalog o AltTracker y actívalas. |
| El Pull va bien pero el juego se ve viejo | Copiaste una vez. Vuelve a copiar después del Pull o usa uniones/enlaces. |
| Fallan `mklink` / `ln` | Ya hay una carpeta real con ese nombre en AddOns, o la ruta está mal. |
| Los addons no cargan | Confirma `_retail_` y que las carpetas están directo en `AddOns`. |

---

## Ayuda

- Wiki: [https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- Soporte: [https://wow2.xyz/support/](https://wow2.xyz/support/)
- Código completo (colaborar): [https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**Autor:** MichinMuggin / Ricky

**Sitio:** https://wow2.xyz/

**Todos los derechos reservados.**
