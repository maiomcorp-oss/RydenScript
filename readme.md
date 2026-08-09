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
*   *Nota:* Você pode criar páginas infinitas (`<page2>`, `<page3>`, etc.) e navegar entre elas instantaneamente.

### 3. Simplicidade Radical
Não utiliza chaves `{ }`, parênteses `( )` ou colchetes `[ ]` nem barras `/` nem palavras inteiras dentro por exemplo `<button>` o certo e `<b>` e o titulo e '<t>' e a mesma coisa com o paragrafo que e `<p>` . A separação de parâmetros complexos é feita através do caractere pipe `|`.

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

```

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
*   **Sintaxe:** `<f> bloco2D [Largura] [Altura] [X] [Y] [Visual] [Comportamento] [Extra]`
*   **Comportamentos suportados:**
    *   `normal`: Bloco sólido.
    *   `player`: Personagem controlável.
    *   `pagina`: Portal para outra página (Ex: `pagina page2`).
    *   `superpulo`: Bloco que impulsiona o pulo.
    *   `elimina`: Reseta o player (Ex: `elimina "Mensagem"`).
    *   `clique_pagina`: Botão que muda de página ao clicar.
    *   `clique_mostrar`: Revela elementos ocultos ao clicar.

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
*   `<f> menu | cor:[c] | cormenu:[c] | paginas:Nome:pageID,... <f>`: Cria barra de navegação.

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

---

## 📈 Histórico de Versões

| Versão | Principais Novidades |
| :--- | :--- |
| **v1.0.0** | Lançamento inicial, foco em tags básicas e leveza extrema. |
| **v2.0.0** | Introdução do sistema P2P e menus de navegação dinâmicos. |
| **v3.0.0** | Suporte a posicionamento absoluto (X/Y) e estilização avançada. |
| **v4.0.0** | Evolução do motor `bloco2D`, interatividade por clique e ecossistema self-hosted. |

---

## 👨‍💻 Autor

Desenvolvido com ☕ e dedicação por **Daniel Saldanha**.
Inspirado na simplicidade e no poder da web moderna.

---
*RydenScript - Transformando código em brincadeira de criança.*
