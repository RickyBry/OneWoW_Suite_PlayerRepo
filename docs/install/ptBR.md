# OneWoW Suite — instalação para jogadores

**Idioma:** [English](../../README.md) · [Deutsch](deDE.md) · [Español (España)](esES.md) · [Español (México)](esMX.md) · [Français](frFR.md) · [Italiano](itIT.md) · [한국어](koKR.md) · Português (Brasil) · [Русский](ruRU.md) · [简体中文](zhCN.md) · [繁體中文](zhTW.md)

Este repositório é a cópia **para jogadores** do OneWoW: só as pastas de addons que vão no World of Warcraft. Ele é atualizado a partir do [repositório completo da Suite](https://github.com/kellewic/OneWoW_Suite). Você não precisa desse repo de desenvolvimento para jogar.

- **Site:** [https://wow2.xyz/](https://wow2.xyz/)
- **Wiki:** [Instalação](https://github.com/kellewic/OneWoW_Suite/wiki/Install) · [Primeiros passos](https://github.com/kellewic/OneWoW_Suite/wiki/Getting-Started)
- **Suporte:** [https://wow2.xyz/support/](https://wow2.xyz/support/)

Isto é um espelho. Não abra issues nem pull requests aqui. Use o repo da Suite ou a página de suporte.

Os passos **normais** (GitHub Desktop) e os **avançados** (linha de comando e atalhos para não copiar pastas de novo) estão nesta mesma página.

---

## O que você precisa

- **World of Warcraft Retail** (esta suite não é para Classic)
- Uma pasta no computador para guardar este repo (Documentos serve)
- **GitHub Desktop** (recomendado) ou **Git** se preferir o terminal

### Downloads

| O quê | Para quem | Link |
|-------|-----------|------|
| **GitHub Desktop** | Windows 10/11 e macOS — o jeito mais fácil | [desktop.github.com](https://desktop.github.com/) |
| **Git** | Só linha de comando | [git-scm.com/downloads](https://git-scm.com/downloads) |
| **Git para Windows** | Terminal no Windows | [git-scm.com/download/win](https://git-scm.com/download/win) |
| **Git para macOS** | Terminal no Mac (ou Xcode Command Line Tools) | [git-scm.com/download/mac](https://git-scm.com/download/mac) |

Se você usa GitHub Desktop, **não** precisa instalar o Git à parte. O Desktop já inclui o necessário.

Endereço do repositório (você vai colar depois):

```text
https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
```

---

## Encontrar a pasta AddOns

O WoW só carrega addons que estão **diretamente** em `Interface\AddOns` (cada pasta se chama `OneWoW`, `OneWoW_Bags`, e assim por diante).

**Windows (típico):**

```text
C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns
```

**macOS (típico):**

```text
/Applications/World of Warcraft/_retail_/Interface/AddOns
```

Se esses caminhos estiverem errados, o jogo está instalado em outro lugar:

1. Abra o aplicativo **Battle.net**.
2. Selecione **World of Warcraft**.
3. Abra a **engrenagem** / opções ao lado de Jogar.
4. Em **Configurações do jogo**, encontre a pasta de instalação ou use **Mostrar pasta** / **Abrir pasta**.

Você precisa de `_retail_` (Retail), não `_classic_` nem `_classic_era_`. Se `Interface` e `AddOns` não existirem, crie essas duas pastas dentro de `_retail_`.

---

## Instalação normal — GitHub Desktop

Use isto se você não quiser digitar comandos.

### 1. Instalar o GitHub Desktop

1. Abra [https://desktop.github.com/](https://desktop.github.com/).
2. Baixe o instalador para **Windows** ou **macOS**. O site escolhe o arquivo certo.
3. Execute o instalador e termine a configuração.
4. Você pode entrar com uma conta GitHub. Neste repo **público**, o login é opcional. Dá para clonar sem conta.

### 2. Clonar este repositório (salvar numa pasta)

«Clonar» significa: baixar o repo para uma pasta que você escolhe e manter o vínculo com o GitHub para atualizar depois.

1. Abra o **GitHub Desktop**.
2. **File → Clone repository** (Arquivo → Clonar repositório).
3. Abra a aba **URL**.
4. Cole:

   ```text
   https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
   ```

5. Em **Local path**, escolha uma pasta fácil de achar, por exemplo:

   - Windows: `C:\Users\SEUNOME\Documents\OneWoW_Suite_PlayerRepo`
   - Mac: `/Users/SEUNOME/Documents/OneWoW_Suite_PlayerRepo`

   Esta pasta **não** é a AddOns do WoW. É uma cópia de trabalho. No próximo passo você copia ou cria atalho daqui para a AddOns.

6. Clique em **Clone** e espere os arquivos aparecerem.

Quando terminar, você deve ver `OneWoW`, `OneWoW_Bags`, `OneWoW_QoL` e as outras pastas `OneWoW_*`.

### 3. Colocar os addons no jogo

1. Abra a pasta clonada.
2. Abra `Interface\AddOns` (veja acima).
3. Copie as pastas de addon que quiser **para dentro** de `AddOns`.

**Obrigatório:** `OneWoW` (o hub). Sem ele, o resto não carrega.

**Opcionais:** `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit`.

**Se você usa Catalog**, copie também todas as pastas `OneWoW_CatalogData_*` ou essas abas ficam vazias.

**Se você usa AltTracker**, copie também todas as pastas companheiras `OneWoW_AltTracker_*`.

**DevTool** (`OneWoW_Utility_DevTool`) é opcional. É um inspetor no jogo (`/1wdt`), não é necessário para jogar.

Você não precisa copiar tudo. Só o que for ativar.

**Não** jogue o repo inteiro na AddOns como uma pasta `OneWoW_Suite_PlayerRepo`. O WoW não vê o `OneWoW` se ele estiver um nível mais fundo.

Depois de copiar, a `AddOns` deve parecer assim:

```text
AddOns\OneWoW\
AddOns\OneWoW_Bags\
AddOns\OneWoW_QoL\
...
```

e não assim:

```text
AddOns\OneWoW_Suite_PlayerRepo\OneWoW\
```

### 4. Ligar no WoW

1. Na tela de **seleção de personagem**, clique em **Addons**.
2. Ative **OneWoW** e cada módulo opcional que você copiou.
3. Entre (ou digite `/reload` se já estava no mundo).
4. Digite `/1w` para abrir o hub.
5. Em **Manage Features**, ative ou desative módulos. Desativar **descarrega** o addon; não só esconde.

### 5. Atualizar depois (Desktop)

1. Abra o **GitHub Desktop**.
2. Confirme que este repositório está selecionado no topo.
3. Clique em **Fetch origin**. Isso consulta o GitHub por arquivos novos.
4. Se aparecer **Pull origin**, clique. As mudanças chegam na pasta clonada.

Se você **copiou** as pastas para a AddOns, copie de novo depois de cada pull e substitua as antigas. Windows e macOS pedem para substituir: aceite.

Se você usou **junções ou links simbólicos** (seção avançada), o Pull basta. O jogo já aponta para esta pasta.

Feche o WoW antes de substituir arquivos se o jogo estiver aberto. É mais seguro.

---

## Outra opção simples — ZIP (sem atualizações)

Na página do repo: **Code → Download ZIP**, extraia e copie as pastas `OneWoW*` para a AddOns do mesmo jeito.

Um ZIP é um retrato completo toda vez. Ele não se atualiza sozinho. Prefira Desktop ou Git se quiser `pull` depois. **CurseForge** e o ZIP do Discord também servem se você não quiser Git.

---

## Avançado — Git na linha de comando

Se você se sente à vontade no terminal. Instale o [Git](https://git-scm.com/downloads) primeiro ([Windows](https://git-scm.com/download/win) · [macOS](https://git-scm.com/download/mac)). No Mac também vale `xcode-select --install`.

Abra o **Git Bash** ou o **PowerShell** no Windows, ou o **Terminal** no Mac. Entre com `cd` onde a pasta deve ser criada (por exemplo Documentos) e:

```text
git clone --depth 1 https://github.com/MichinMigugin/OneWoW_Suite_PlayerRepo.git
cd OneWoW_Suite_PlayerRepo
```

`--depth 1` baixa só os arquivos atuais, não o histórico inteiro.

Depois copie (ou crie atalho) as pastas `OneWoW*` para `Interface\AddOns` como na instalação normal.

### Atualizar depois (linha de comando)

```text
cd caminho\para\OneWoW_Suite_PlayerRepo
git pull
```

No Mac use `caminho/para/OneWoW_Suite_PlayerRepo`.

Se você copiou pastas, copie de novo para a AddOns. Se criou atalhos, `git pull` é a atualização inteira.

---

## Avançado — junções e links simbólicos (sem copiar de novo)

Um **atalho** faz `AddOns\OneWoW` apontar para `...\OneWoW_Suite_PlayerRepo\OneWoW`. Depois, Pull no Desktop ou `git pull` atualiza os arquivos que o jogo já usa.

- Feche o World of Warcraft primeiro.
- Clone o repo com Desktop ou Git **antes** de criar os atalhos (as pastas de destino precisam existir).
- Se você já **copiou** `OneWoW` para a AddOns, apague ou renomeie essa cópia. Não dá para criar o atalho se já existe uma pasta de verdade com o mesmo nome.
- Um atalho por pasta de addon que você quiser. Comece por `OneWoW`.
- Apagar a junção ou o link na AddOns remove o **atalho**, não o seu clone.

### Windows — junção (sem Administrador)

Uma junção (`mklink /J`) não precisa do prompt como administrador. Um symlink (`mklink /D`) muitas vezes precisa: use `/J`.

1. Abra o **Prompt de Comando** (cmd).
2. Ajuste os dois caminhos: sua pasta `AddOns` real do WoW e sua pasta clonada real.
3. Uma linha por addon:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" "C:\Users\SEUNOME\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Exemplo Bags:

```text
mklink /J "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW_Bags" "C:\Users\SEUNOME\Documents\OneWoW_Suite_PlayerRepo\OneWoW_Bags"
```

Repita para cada pasta `OneWoW_*` que você usar (incluindo dados do Catalog e companheiros do AltTracker).

**PowerShell:**

```text
New-Item -ItemType Junction -Path "C:\Program Files (x86)\World of Warcraft\_retail_\Interface\AddOns\OneWoW" -Target "C:\Users\SEUNOME\Documents\OneWoW_Suite_PlayerRepo\OneWoW"
```

Se o Windows disser que o caminho já existe, ainda há uma pasta na AddOns. Remova ou renomeie e rode o comando de novo.

### macOS — link simbólico

1. Abra o **Terminal**.
2. Ajuste os dois caminhos ao seu Mac.
3. Execute:

```text
ln -s "/Users/SEUNOME/Documents/OneWoW_Suite_PlayerRepo/OneWoW" "/Applications/World of Warcraft/_retail_/Interface/AddOns/OneWoW"
```

Repita para cada pasta. Se `AddOns/OneWoW` já existe como cópia real, jogue no Lixo primeiro.

### Conferir se funcionou

Abra `AddOns\OneWoW` (ou o caminho do Mac). Você deve ver os mesmos arquivos do clone. Depois de um Pull, esses arquivos mudam sem outra cópia.

### Desfazer um atalho

Apague só a pasta vinculada **dentro da AddOns**. O clone `OneWoW_Suite_PlayerRepo` fica. Você pode voltar a copiar pastas se quiser.

---

## Pastas neste repo

| Tipo | Pastas |
|------|--------|
| **Obrigatório** | `OneWoW` |
| **Funções** | `OneWoW_Bags`, `OneWoW_QoL`, `OneWoW_AltTracker`, `OneWoW_Catalog`, `OneWoW_Trackers`, `OneWoW_Notes`, `OneWoW_ShoppingList`, `OneWoW_Mail`, `OneWoW_DirectDeposit` |
| **Dados do Catalog** | `OneWoW_CatalogData_Journal`, `OneWoW_CatalogData_Vendors`, `OneWoW_CatalogData_Tradeskills`, `OneWoW_CatalogData_Quests`, `OneWoW_CatalogData_Quests_Archive` |
| **Dados do AltTracker** | `OneWoW_AltTracker_Storage`, `OneWoW_AltTracker_Character`, `OneWoW_AltTracker_Professions`, `OneWoW_AltTracker_Collections`, `OneWoW_AltTracker_Endgame`, `OneWoW_AltTracker_Auctions`, `OneWoW_AltTracker_Accounting` |
| **Opcional** | `OneWoW_Utility_DevTool` (`/1wdt`) |

---

## Problemas comuns

| O que você vê | O que fazer |
|---------------|-------------|
| Sem OneWoW na seleção de personagem | Falta `OneWoW` na AddOns, ou ela está dentro de outra pasta. |
| Função ligada mas vazia | Copie também as pastas de dados do Catalog ou AltTracker e ative-as. |
| O Pull funcionou mas o jogo parece antigo | Você copiou uma vez. Copie de novo depois do Pull ou use junções/links. |
| `mklink` / `ln` falha | Já existe uma pasta real com esse nome na AddOns, ou o caminho está errado. |
| Os addons não carregam | Confirme `_retail_` e que as pastas estão direto na `AddOns`. |

---

## Ajuda

- Wiki: [https://github.com/kellewic/OneWoW_Suite/wiki](https://github.com/kellewic/OneWoW_Suite/wiki)
- Suporte: [https://wow2.xyz/support/](https://wow2.xyz/support/)
- Código completo (contribuir): [https://github.com/kellewic/OneWoW_Suite](https://github.com/kellewic/OneWoW_Suite)

---

**Autor:** MichinMuggin / Ricky

**Site:** https://wow2.xyz/

**Todos os direitos reservados.**
