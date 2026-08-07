# 🎮 RydenScript

**RydenScript** é uma linguagem de programação rápida, intuitiva e totalmente baseada em tags, desenvolvida para simplificar a criação de aplicações web, utilitários e jogos (2D e 3D). Criada por **Daniel Saldanha** em julho de 2026, a linguagem foi concebida para transformar a complexidade do desenvolvimento em uma experiência acessível e divertida.

---

## 🚀 Visão Geral

Ao contrário de interpretadores rígidos, o **RydenScript** foca na agilidade e na experiência do desenvolvedor ("Developer Experience"). Seus principais pilares são:

*   **Leveza Extrema:** O interpretador ocupa apenas alguns kilobytes, garantindo performance mesmo em hardwares limitados.
*   **Sintaxe Amigável:** Utiliza tags (`< >`) em vez de estruturas complexas como chaves `{ }` ou parênteses `( )`.
*   **Zero Configuração:** Esqueça setups complexos de câmera, renderizadores ou loops de física. O motor do RydenScript gerencia tudo automaticamente.
*   **Multifuncional:** Capaz de criar desde interfaces administrativas simples até jogos 3D complexos com física e colisão.

---

## 🧩 Sintaxe Básica

A estrutura fundamental do RydenScript é baseada em **Páginas**. Cada aplicação começa com uma definição de página.

### Comandos Essenciais

| Tag | Descrição | Exemplo |
| :--- | :--- | :--- |
| `<pageN>` | Define o início e o fim de uma página (ex: `<page1>`). | `<page1> ... <page1>` |
| `<fundo>` | Define a cor de fundo da página (CSS ou nome em inglês). | `<fundo> #16161a` |
| `<t>` | Cria um título estilizado. | `<t> Meu Projeto <t>` |
| `<p>` | Cria um parágrafo de texto. | `<p> Bem-vindo ao sistema. <p>` |
| `<b>` | Cria um botão interativo. | `<b> Clique Aqui <b>` |

> **Dica de Formatação:** Para evitar que o GitHub oculte suas tags, sempre utilize blocos de código ou garanta espaços entre os sinais de menor/maior quando documentar.

---

## 🎨 Estilização e Posicionamento (v3.0+)

A partir da versão 3.0, o RydenScript introduziu controle total sobre o design dos elementos através de parâmetros separados por pipe (`|`).

### Parâmetros Suportados:
*   `cor`: Hexadecimal ou nome da cor.
*   `tamanho`: Tamanho da fonte (ex: `24px`).
*   `fonte`: Família da fonte (ex: `Arial`, `Courier New`).
*   `x` / `y`: Coordenadas para posicionamento absoluto.

**Exemplo:**
```rydenscript
<t> Título Customizado <t> cor: "#ff5722" | tamanho: "32px" | x: "50px" | y: "20px"
```

---

## 🕹️ Motor de Jogos (2D e 3D)

O RydenScript possui um motor integrado potente para criação de jogos de forma declarativa.

### Blocos 2D (`bloco2D`)
O comando `bloco2D` aceita: `largura`, `altura`, `posição X`, `posição Y`, `visual` e `comportamento`.

| Comportamento | Descrição |
| :--- | :--- |
| `normal` | Bloco sólido com colisão. |
| `player` | Personagem controlável com física e gravidade. |
| `pagina` | Portal que transporta o jogador para outra página. |
| `elimina` | Obstáculo que reseta a posição do jogador. |

### Exemplo de Jogo 3D
```rydenscript
<fundo> #16161a
<f> jogador3D "https://link-da-skin.png" <f>
<f> mapa3D "#55aa55" <f>

// bloco3D [X] [Y] [Z] [L] [A] [P] [Textura] [Comportamento]
bloco3D 0 0 0 5 1 5 "#55aa55" normal
<f> jogo3D <f>
```

---

## 🌐 Comunicação P2P

Crie aplicações descentralizadas e chats em tempo real com facilidade.

*   `<P2P id>`: Exibe o ID exclusivo do usuário.
*   `<P2P input>`: Painel para inserir ID de destino e enviar mensagens.
*   `<P2P chat>`: Renderiza o histórico de mensagens em tempo real.

---

## ⚙️ Automação (Administract Coder)

Para tarefas de sistema e automação, utilize o prefixo `<f> administract>c>`.

*   **Gerar Arquivos:** `<f> administract>c> gerar main.js | destino area_trabalho | conteudo "..." `
*   **Alertas de Sistema:** `<f> administract>c> mensagem "Sistema Iniciado" `
*   **Executar Programas:** `<f> administract>c> abrir notepad.exe | espera 3`

---

## 📝 Exemplo Completo (App Multi-páginas)

```rydenscript
<page1>
    <fundo> #18191a
    <t> Painel de Entrada <t> cor: "#ffffff"
    <p> Escolha uma opção abaixo: <p>
    <b> Iniciar App <b> <f> page2 <f> cor: "#2374e1"
<page1>

<page2>
    <fundo> #0f172a
    <t> Bem-vindo à Página 2 <t>
    <b> Voltar <b> <f> page1 <f>
<page2>
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
