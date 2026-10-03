# 🚀 RydenScript: Linguagem de Programação Geral

O **RydenScript** é uma linguagem de programação rápida, fácil e declarativa, onde todos os comandos são baseados em tags (não usa comandos de outras linguagems!! use sempre os exemplos eles estão exatamente como vai funcionar corretamente no editor do RydenScript). Criada por **Daniel Saldanha** em julho de 2026, ela foi concebida para **revolucionar o desenvolvimento web, a criação de utilitários e aplicativos**, tornando a construção de sistemas complexos tão simples quanto uma brincadeira de criança.

Diferente de linguagens de marcação puras, o RydenScript é uma linguagem de **propósito geral** com motor de lógica, rede P2P e automação de sistemas integrados.

---

## 🛠️ Filosofia e Regras de Sintaxe

### 1. A Regra das Tags
O RydenScript utiliza `< >` para todos os comandos. Para garantir que o compilador entenda seu código e evitar que o GitHub esconda suas tags, utilize espaços claros ou blocos de código.

### 2. Estrutura de Páginas
Todo aplicativo ou site em RydenScript deve ser delimitado por tags de página. A `<page1>` é a tela principal carregada por padrão.
*   **Início:** `<page1>`
*   **Fim:** `<page1>`
*   *Nota:* Você pode criar páginas infinitas (`<page2>`, `<page3>`, etc.) e navegar entre elas instantaneamente, aviso: não escreva `<pagina1>` ta errado o certo e sempre page `<page1>` e assim com todas as outras de 1 a infinito , mais tirando a tag `<fundo>` e `<page>` os comandos basicos são apenas uma letra significativa que deve ser escrita do jeito pedido nas tabelas de exemplo , ex: `<t>` `<b>` `<p>`  .

### 3. Simplicidade Radical
Não utiliza chaves `{ }`, parênteses `( )` ou colchetes `[ ]` nem barras `/` nem palavras inteiras dentro , por exemplo `<button>` o certo e `<b>` e o titulo e `<t>` e a mesma coisa com o paragrafo que e `<p>` . A separação de parâmetros complexos é feita através do caractere pipe `|`.

---

## 📚 Progressão de Sintaxe: Do Básico ao Complexo

### Nível 1: Comandos Básicos de Estrutura
Estes são os blocos fundamentais para criar uma página web ou sistema simples.

| Tag | Função | Exemplo de como deve ser escrito|
| :--- | :--- | :--- |
| `<fundo>` | Define a cor de fundo da página (CSS ou Inglês). | `<fundo> red` |
| `<t>` | Cria um título ou cabeçalho. | `<t> Título <t>` |
| `<p>` | Cria um parágrafo ou bloco de texto descritivo. | `<p> Texto <p>` |
| `<b>` | Cria um botão interativo. | `<b> Clique <b>` |
| `<video>` | Roda um vídeo via URL. | `<video> url "link" <video>` |
| `<image>` | Exibe uma imagem via URL. | `<image> url "link" <image>` |

### Nível 2: Estilização e Design (v3.0.0+)
Adicione propriedades visuais avançadas aos elementos usando a sintaxe de parâmetros.

*   **Títulos (`<t>`) e Parágrafos (`<p>`)**:
    *   **Parâmetros:** `cor`, `tamanho`, `fonte`, `borda`, `x`, `y`.
    *   *Exemplo:* `<t> Título <t> cor: #00ffd5 | fonte: Arial | borda: 2px solid #00ffd5 | x: 50px | y: 20px`
*   **Botões (`<b>`)**:
    *   **Parâmetros:** `cor`, `fonte`, `x`, `y`, `ação`.
    *   *Exemplo:* `<b> Entrar <b> cor: #1a73e8 | fonte: sans-serif | page2`

### Nível 3: Navegação e Componentes de Interface
O RydenScript permite criar aplicações multipáginas e interfaces modernas.

*   **Navegação entre Páginas:** Use a tag `<f> pageN <f>` dentro de um botão para mudar de tela.
*   **Menu de Navegação:**
    *   `<f> menu | cor: [hex] | cormenu: [hex] | paginas: Nome:pageID, ... <f>`
*   **Componentes Visuais:**
    *   `<f> interface retangulo | cor:#1e293b | largura:100% | altura:60px <f>`
    *   `<f> grid [linhas] [colunas] <f>` (Ex: `<f> grid 3 3 <f>`)
    *   `<f> pagiamento | [palavra chave] [ pagina ] | ... infinito` (Ex: `<f> pagiamento | 123 page2 | `) 

---

## 🌐 Rede P2P Descentralizada
Crie chats e sistemas de comunicação em tempo real sem necessidade de um servidor central.

*   **`<P2P id>`**: Gera e exibe o ID exclusivo do usuário na rede.
*   **`<P2P chat>`**: Renderiza a janela de histórico de mensagens WebRTC em tempo real.
*   **`<P2P input>`**: Painel de comando para envio de mensagens e dados.
    *   *Exemplo:* `<P2P input> "dados.txt" | conteudo: "Olá" | id "XYZ"`

---

## ⚙️ Administract Coder (Automação de Sistemas)
Esta é a biblioteca de baixo nível para controle administrativo e gestão de arquivos.

| Comando | Descrição | Exemplo de Uso |
| :--- | :--- | :--- |
| `gerar` | Automatiza a criação de arquivos físicos. | `<f> administract>c> gerar main.js \| destino area_trabalho \| conteudo "..."` |
| `mensagem` | Dispara alertas automatizados do sistema. | `<f> administract>c> mensagem "Sistema Iniciado!"` |
| `abrir` | Abre programas ou URLs com delay programado. | `<f> abrir [url] \| espera [segundos]` |
| `pagiamento` | Sistema de senhas e redirecionamento. | `<f> pagiamento 1234 painelSecreto \| 970 page2` |
| `calculadora` | Instancia uma calculadora funcional. | `<f> calculadora <f>` |
| `cronometro` | Aciona um cronômetro de precisão. | `<f> cronometro <f>` |

---

## 🎮 Motores de Jogos (2D e 3D)
Embora focado em apps, o RydenScript possui motores potentes para entretenimento.

### Motor `bloco2D` (v4.0.0)
Utilizado para criar interfaces interativas ou jogos de plataforma.
*   **Comportamentos:** `normal`, `player`, `pagina`, `superpulo`, `elimina`, `clique_pagina`, `clique_mostrar`.
*   *Exemplo:* `<f> bloco2D 600 20 0 350 #444444 normal`

### Motor 3D e Outros
*   **3D:** `bloco3D [X] [Y] [Z] [L] [A] [P] [Textura] [Comportamento] [Mensagem]`
*   **Tetris:** `<f> tetrisFundo cor "black" <f>`, `<f> tetrisBloco "url" <f>`, `<f> tetris <f>`
*   **Estilo Mario:** `<f> marioCenario`, `<f> marioJogador`, `<f> mario <f>`

---

## 📝 Exemplo de Aplicação Real (Rede Social / App)

```rydenscript
<page1>
    <fundo> #18191a
    <f> menu | cor: #ff5722 | cormenu: #222 | paginas: Home:page1, Perfil:page2 <f>
    <t> 👤 Bem-vindo ao App <t> cor: "#e4e6eb" | x: "50px" | y: "50px"
    <p> Este é um sistema estruturado em RydenScript. <p> cor: "#b0b3b8" | x: "50px" | y: "100px"
    <b> Acessar Perfil <b> cor: "#2374e1" | x: "50px" | y: "160px" | page2
<page1>

<page2>
    <fundo> #0f172a
    <t> ⚙️ Seu Perfil <t> cor: "white"
    <P2P id>
    <P2P chat>
    <b> Voltar <b> <f> page1 <f>
<page2>
```

---

## 🛠️ Biblioteca Completa da Tag de Função `<f>`

A tag `<f>` (Função) é o coração do RydenScript, permitindo acessar bibliotecas de jogos, utilitários e sistema. Abaixo estão **todos** os comandos documentados:

### 1. Engine de Jogos 2D (Estilo Mario/Dinossauro)
Use estes comandos para configurar e iniciar um jogo de plataforma 2D.
*   `<f> marioCenario "url" <f>`: Define a imagem de fundo.
*   `<f> marioJogador "url" <f>`: Define a skin do personagem.
*   `<f> marioInimigo "url" <f>`: Define a imagem do inimigo.
*   `<f> marioChao "url" <f>`: Define a textura do chão.
*   `<f> mario <f>`: Inicializa o motor do jogo estilo Mario.
*   `<f> mapa cor "cor" <f>`: Define a cor do mapa no jogo de desvio.
*   `<f> jogador cor "cor" <f>`: Define a cor do jogador.
*   `<f> obstaculos cor "cor" <f>`: Define a cor dos obstáculos.
*   `<f> jogo2D <f>`: Inicializa o motor de jogo 2D de desvio.

### 2. Engine de Blocos 2D (v4.0.0)
Comando versátil para criar elementos com física ou interatividade.
*   **Sintaxe:** `<f> bloco2D [Largura] [Altura] [X] [Y] [Visual/link de imagem] [Comportamento] [Extra]`
*   **Comportamentos suportados:**
    *   `normal`: Bloco sólido.
    *   `player`: Personagem controlável.
    *   `pagina`: Portal para outra página apos encostar no bloco com esse comportamento (Ex: `pagina page2`).
    *   `superpulo`: Bloco que impulsiona o pulo.
    *   `elimina`: Reseta o player pra de onde ele veio (Ex: `elimina "Mensagem"`).
    *   `clique_pagina`: Botão que muda de página ao clicar no bloco (Ex: `clique_pagina page2`).
    *   `clique_mostrar`: Revela elementos ocultos ao clicar (quebrado).

### 3. Engine de Jogos 3D (Parkour e Exploração)
*   `<f> jogador3D "url_ou_path" <f>`: Define a skin/modelo do jogador 3D.
*   `<f> mapa3D "cor_ou_hex" <f>`: Define a textura padrão do chão 3D.
*   `<f> jogo3D <f>`: Inicializa a Engine 3D.
*   **Comando de Bloco 3D:** `bloco3D [X] [Y] [Z] [L] [A] [P] [Textura] [Comportamento] [Mensagem]`

### 4. Biblioteca Tetris
*   `<f> tetrisFundo cor "cor" <f>`: Define o fundo do Tetris.
*   `<f> tetrisBloco "url" <f>`: Define a textura dos blocos.
*   `<f> tetris <f>`: Inicializa o jogo Tetris.

### 5. Administract Coder (Sistema e Automação)
Comandos para gestão de arquivos e tarefas administrativas.
*   `<f> administract>c> gerar [arq] | destino [local] | conteudo "[texto]"`: Cria arquivos.
*   `<f> administract>c> mensagem "[texto]"`: Exibe alerta de sistema.
*   `<f> administract>c> abrir [app/url] | espera [segundos]`: Abre programas/sites.
*   `<f> pagiamento [senha] [painel] | [código] [página]`: Sistema de acesso e redirecionamento.

### 6. Utilitários e Interface
*   `<f> calculadora <f>`: Abre a interface de calculadora.
*   `<f> cronometro <f>`: Abre um cronômetro com controles.
*   `<f> alert "mensagem" <f>`: Exibe um alerta na tela (usado em botões).
*   `<f> pageN <f>`: Comando de navegação para a página N.
*   `<f> grid [linhas] [colunas] <f>`: Cria uma estrutura de grelha.
*   `<f> interface retangulo | cor:[c] | largura:[l] | altura:[a] <f>`: Cria um componente visual.
*   `<f> menu | cor:[c] | cormenu:[c] | paginas:Nome:pageID,... <f>`: Cria um menu de navegação entre paginas.
*   `<f> irpara "URL" <f>`
*   `<f> login | titulo: "seutitulo" | corFundo: #123 | corBotao: #145 | textoBotao | corTexto <f> `

---

## 🧩 Outras Tags Importantes

*   `<page1>` ... `<page1>`: Delimitador de páginas.
*   `<fundo> [cor]`: Define o fundo da página atual.
*   `<t> [texto] <t> [estilo]`: Título estilizado (cor, fonte, tamanho, x, y).
*   `<p> [texto] <p> [estilo]`: Parágrafo estilizado (cor, fonte, tamanho, x, y).
*   `<b> [texto] <b> [estilo]`: Botão estilizado com ações (alert, pageN).
*   `<P2P id>`, `<P2P input>`, `<P2P chat>`: Sistema de rede descentralizada.
*   `<video>`, `<image>`: Exibição de mídia.

---

## 📝 Exemplo de Código (v4.0.0)

```rydenscript
<page1>
    <fundo> #0f172a
    <f> menu | cor: #ff5722 | cormenu: #222 | paginas: Home:page1, Jogo:page2 <f>
    <t> Bem-vindo ao RydenScript <t> cor: "white" | x: "50px" | y: "20px"
    <b> Iniciar Jogo <b> <f> page2 <f> cor: "green" | x: "50px" | y: "100px"
<page1>

<page2>
    <fundo> #111
    <f> jogador3D "https://img.icons8.com/emoji/96/dog-emoji.png" <f>
    <f> mapa3D "#55aa55" <f>
    bloco3D 0 0 0 5 1 5 "#55aa55" normal
    <f> jogo3D <f>
<page2>
```
## RydenScript v5.0.0 Documentação
# Mudanças do RydenScript — `<RS>` e PowerShell

## 1. `<RS>`

O `<RS>` é um bloco do RydenScript criado para concentrar a saída de código PowerShell.

A lógica continua sendo escrita em RydenScript. O PowerShell é apenas o resultado da compilação.

---

## 2. Variáveis no `<RS>`

```rydenscript
Ry Variavel "Ola RydenScript"
```

Gera no PowerShell:

```powershell
$Variavel = "Ola RydenScript"
```

---

## 3. Mostrar Variável

```rydenscript
Mostr Ry Variavel
```

Gera:

```powershell
Write-Output $Variavel
```

---

## 4. Um Único Arquivo PowerShell

Os comandos colocados dentro do `<RS>` podem contribuir para o mesmo arquivo `.ps1`.

Exemplos:
- `powershell>c> mensagem`
- `Administract>c> mensagem`
- `abrir`

Assim, em vez de cada recurso gerar um arquivo separado, o `<RS>` pode reunir os códigos em uma única saída PowerShell.

---

## 5. Download

O editor do RydenScript pode mostrar um botão para baixar o PowerShell compilado.

* **Nome do arquivo:** `rydenscript_rs.ps1`

---

## 6. Objetivo

A ideia é permitir que o RydenScript tenha recursos além da Web através da compilação para PowerShell.

* O programador continua escrevendo RydenScript.
* O PowerShell fica responsável pelo código gerado para recursos que precisam dele.

> **Frase da Ideia:**
> *"Você programa em RydenScript.*
> *O RydenScript programa o PowerShell."*

**RS - RydenScript → PowerShell**

---

### Exemplos de Estrutura e Comandos

* **Estrutura:**
  ```rydenscript
  <RS>
  ...
  <RS>
  ```

* **Variáveis:**
  ```rydenscript
  Ry Variavel "Ola RydenScript"
  Mostr Ry Variavel
  ```

* **PowerShell:**
  ```rydenscript
  powershell>c> mensagem "Ola"
  ```

* **Administract:**
  ```rydenscript
  Administract>c> mensagem "Ola PowerShell"
  ```

* **Abrir:**
  ```rydenscript
  abrir programa.exe
  abrir programa.exe espera 5
  ```

* **Janela:**
  ```rydenscript
  Create Janel
  ```

* **Switch:**
  ```rydenscript
  Switch Ry opcao

  Caso 1
      Mostr "Um"
  FimCaso

  Caso 2
      Mostr "Dois"
  FimCaso

  Padrao
      Mostr "Outra opcao"
  FimCaso

  FimSwitch
  ```

---

<hr style="border: 1px solid #ccc;">

# Novas Atualizações do `<RS>`

<hr style="border: 1px solid #ccc;">

## 8. Create Button

O `<RS>` agora possui criação de botões para `JanelRS`.

* **Sintaxe:**
  ```rydenscript
  Create Button | id: salvar | texto: "Salvar" | largura: 100 | altura: 40 | x: 25 | y: 400
  ```

* **Propriedades disponíveis:**
  - `id`
  - `texto`
  - `largura`
  - `altura`
  - `x`
  - `y`
  - `cor`
  - `cortexto`
  - `borda`
  - `add_click`
  - `add_tick`

---

## 9. Add_Click

O `Create Button` pode receber um evento de clique.

* **Exemplo:**
  ```rydenscript
  Create Button | id: botao | texto: "Clique" | add_click: código PowerShell
  ```

* O compilador transforma isso em um evento PowerShell:
  ```powershell
  $botao.Add_Click({
      código PowerShell
  })
  ```

---

## 10. Add_Tick

O `Create Button` também pode receber um evento periódico.

* **Exemplo:**
  ```rydenscript
  Create Button | id: botao | texto: "Loop" | add_tick: código PowerShell
  ```

* O compilador cria um `System.Windows.Forms.Timer` e executa o código no evento `Tick`.

---

## 11. Create Textbox

Foi adicionada a base para criação de caixas de texto dentro de `JanelRS`.

* **Exemplo:**
  ```rydenscript
  Create Textbox | id: editor | largura: 640 | altura: 350 | x: 25 | y: 25
  ```

---

## 12. JanelRS

`Create Janel` cria uma janela PowerShell usando Windows Forms.

* **Exemplo:**
  ```rydenscript
  Create Janel
  ```

A janela é preparada antes dos componentes e somente depois é aberta com `ShowDialog()`.

---

## 13. Bloco de Notas

Com `JanelRS`, `Textbox` e `Button`, o `<RS>` pode montar aplicações como um bloco de notas.

* **Exemplo de estrutura:**
  ```rydenscript
  <RS>

  Create Janel | titulo: "Bloco de Notas RydenScript" | largura: 700 | altura: 500

  Create Textbox | id: editor | largura: 640 | altura: 350 | x: 25 | y: 25

  Create Button | id: salvar | texto: "Salvar" | x: 25 | y: 400

  Create Button | id: limpar | texto: "Limpar" | x: 140 | y: 400

  Create Button | id: sair | texto: "Sair" | x: 255 | y: 400

  <RS>
  ```

---

## 14. Compilação

* Os novos componentes continuam sendo escritos em RydenScript.
* O compilador do RydenScript transforma os componentes em código PowerShell.

> RydenScript continua sendo a linguagem usada pelo programador.  
> PowerShell continua sendo o alvo gerado pelo `<RS>`.

---

## 15. Objetivo da Atualização

Expandir o `<RS>` para permitir criação de interfaces desktop e automações usando PowerShell sem retirar as bibliotecas e recursos já existentes do RydenScript.

> **Frase:**
> *"Você programa em RydenScript.*
> *O RydenScript programa o PowerShell."*


---

## 📈 Histórico de Versões

| Versão | Principais Novidades |
| :--- | :--- |
| **v1.0.0** | Lançamento inicial, foco em tags básicas e leveza extrema. |
| **v2.0.0** | Introdução do sistema P2P e menus de navegação dinâmicos. |
| **v3.0.0** | Suporte a posicionamento absoluto (X/Y) e estilização avançada. |
| **v4.0.0** | Evolução do motor `bloco2D`, interatividade por clique e ecossistema self-hosted. |
| **v5.0.0** |RydenScript virou um magico , trazendo mais automação com a sua cartola e utilizando PowerShell. |
| **v6.0.0** |RydenScript Resolveu melhorar seu proprio visual , Trazendo mais Leveza e Otimização. |
| **v7.0.0** |RydenScript Trouxe mais Bibliotecas ao `<f>` e mais Comandos ao `<RS>`  |

dicas: use sua criatividade e genialidade para conseguir fazer coisas complexas de jeito facil com os recursos existentes, 
exemplo1: alterne em paginas para diferentes estados, 
exemplo2: preocure ser mais curioso e testando diferentes bibliotecas
exemplo3: use a sua criatividade e tente fazer gambiarras para fazer oque você deseja mesmo não tento comando especifico, assim como no Bloco2D.

---

## 👨‍💻 Autor

Desenvolvido com ☕ e dedicação por **Daniel Saldanha**.
Inspirado na simplicidade e no poder da web moderna.

---
*RydenScript - Transformando código em brincadeira de criança.*

#RydenScript #programinglanguage #programação #tecnologia
