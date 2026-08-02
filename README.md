# 🛡️ RydenScript Engine 👾

**RydenScript** Autor: Daniel Saldanha , RydenScript é uma linguagem rapida e facil e cujo todos os comandos são tags , o nome  RydenScript dando assim o o nome de arquivos.rs o RydenScript foi feito em 2026 de mes de julho o Logotipo foi inspirado no Render uma marca de hospedagem de servidor so mudou o nome para "Ryden" e botou o "Script" do lado dando assim "RydenScript" direto ao ponto o RydenScript tem motor de jogos simplificado concebido para transformar a complexidade do desenvolvimento web, de utilitários e de jogos (2D e 3D) numa autêntica brincadeira de crianças!

Ela traduz comandos extremamente intuitivos em código HTML5, CSS3, Canvas e WebGL (via Three.js), permitindo que qualquer pessoa — desde iniciantes a programadores experientes — crie aplicações completas e mundos interativos em segundos sem tocar numa única linha de código complexo a unica Regras inportante e que os comandos basicos nunca podem estar na mesma linha elas so podem estar uma em uma linha diferente não precisa de chaves colchetes ou qualquer outras coisa as tags podem ser uma de baixo da outra a unica coisa que precisa ser dividido em partes e o motor "jogo3D" e ele so precisa  de "#" sim so isso".

---

## 🚀 Visão Geral e Diferenciais

Ao contrário de interpretadores rígidos e focados apenas em texto administrativo, o **RydenScript** destaca-se por três pilares fundamentais:
* **Retrocompatibilidade Absoluta:** Atualizações massivas (como a injeção do motor 3D) rodam em perfeita harmonia com os comandos mais antigos, mantendo todas as funcionalidades intactas.
* **Hibridismo Poderoso:** Consegue renderizar utilitários de sistema dinâmicos, jogos 2D clássicos em Canvas e ambientes virtuais 3D no mesmo ecrã.
* **Zero Configuração:** Esquece setups complexos de câmara, renderizadores, loops de física ou buffers de colisão. O motor do RydenScript trata de tudo nos bastidores de forma invisível.

---

## 🧩 Sintaxe Básica (Tags Principais)

| Comando | Função | Exemplo |
| :--- | :--- | :--- |
| `<fundo>` | Define a cor de fundo da página | `<fundo> #16161a` |
| `<t>` | Cria um título estruturado com cor customizada | `<t> Meu Universo <t> #00ffd5` |
| `<p>` | Cria um parágrafo de texto com cor | `<p> Bem-vindo à nova era <p> #ffffff` |
| `<b>` | Cria um botão com eventos nativos de alerta e cores | `<b> Alerta <b> <f> alert Olá! <f> cor red` |
| `<image>` | Renderiza uma imagem responsiva | `<image> url "https://link.com/foto.png" <image>` |
| `<video>` | Cria um player de vídeo nativo | `<video> url "https://link.com/video.mp4" <video>` |
| `<iframe>` | Incorpora um site externo de forma isolada | `<iframe> url "https://exemplo.com" <iframe>` |

---

## ⚙️ Core de Funções Integradas (`<f>`)

O interpretador suporta 40 funções utilitárias que estendem o HTML padrão em ferramentas complexas de sistema: 

Desvio de meteoros
'<f> mapa cor "blue" <f>
'<f> jogador cor "yellow" '<f>
'<f> obstaculos cor "red" '<f>
'<f> jogo2D '<f>

jogo estilo dinossauro quando acaba a internet ou mario 
'<f> marioCenario "[https://link.com/fundo.png](https://link.com/fundo.png)" '<f>
'<f> marioJogador "[https://link.com/jogador.png](https://link.com/jogador.png)" '<f>
'<f> marioInimigo "[https://link.com/inimigo.png](https://link.com/inimigo.png)" '<f>
'<f> marioChao "[https://link.com/chao.png](https://link.com/chao.png)" '<f>
'<f> mario <f>

Tetris
'<f> tetrisFundo cor "black" <f>
'<f> tetrisBloco "[https://link.com/bloco.png](https://link.com/bloco.png)" '<f>
'<f> tetris <f>

Codificação pra jogo 3D
bloco3D [X] [Y] [Z] [Largura] [Altura] [Profundidade] "Cor_ou_Link_Textura" [Comportamento] ["Mensagem_Opcional"]

Jogo de parkur exemplo 3D
<fundo> #16161a
'<t> 🛠️ Meu Jogo de Parkour 3D 🛠️ '<t> #00e1ff

# Configuração da skin do Jogador (Suporta upload de arquivo local também!)
'<f> jogador3D "[https://img.icons8.com/emoji/96/dog-emoji.png](https://img.icons8.com/emoji/96/dog-emoji.png)" <f>

# Textura padrão do chão
'<f> mapa3D "#55aa55" <f>

# Construção das plataformas do mapa
bloco3D 0 0 0 5 1 5 "#55aa55" normal
bloco3D 0 1.5 -7 3 1 3 "[https://img.icons8.com/color/48/minecraft-grass-block.png](https://img.icons8.com/color/48/minecraft-grass-block.png)" normal
bloco3D 0 -2 -14 8 1 8 "#ff3300" elimina "🔥 A lava derreteu-te! Voltaste ao início!"
bloco3D 4 3 -21 3 1 3 "#00ffd5" notifica "📢 Checkpoint Secreto Ativado!"
bloco3D 0 5 -28 4 1 4 "#ffd700" notifica "🏆 PARABÉNS! Completaste o Parkour!"

# Inicialização da Engine 3D
'<f> jogo3D '<f>

* **Visualização em Grelha (Grid):** ```text
  <f> grid 3 3 <f>
📄 Sistema de Páginas e Navegação (<page>)O RydenScript permite criar aplicações multipáginas e redes de telas de forma declarativa e instantânea, sem a necessidade de escrever scripts adicionais para roteamento ou controle de exibição.📌 Como Funciona:Use a tag <pageN> para definir o início de uma nova tela (onde N é o número da página, ex: <page1>, <page2>, etc.).A <page1> é sempre carregada por padrão como a tela principal.Para navegar entre as páginas, basta indicar o destino no botão usando a instrução <f> pageN.🛠️ Sintaxe dos ComandosTag / InstruçãoDescriçãoExemplo<page1>, <page2>, ...Delimita um novo bloco de página/tela.<page1><b> Texto <b> <f> pageNCria um botão interativo que esconde a tela atual e exibe a página N.<b> Ir para o Feed <b> <f> page2💻 Exemplo Prático (Rede Social / App Multi-telas)Plaintext<page1>
<fundo> #18191a
<t> 👤 Login / Entrada <t> #e4e6eb
<p> Bem-vindo à rede em RydenScript! <p> #b0b3b8
<b> Entrar no Feed <b> <f> page2 cor #2374e1
<b> Ver Perfil <b> <f> page3 cor #3a3b3c

<page2>
<fundo> #18191a
<t> 📰 Feed Principal <t> #e4e6eb
<p> O que você está pensando hoje? <p> #b0b3b8
<b> Ir para Notificações <b> <f> page4 cor #3a3b3c
<b> Voltar para Entrada <b> <f> page1 cor #e41e3f

<page3>
<fundo> #18191a
<t> ⚙️ Seu Perfil <t> #e4e6eb
<p> Nome do Usuário: DevRyden <p> #b0b3b8
<b> Voltar ao Feed <b> <f> page2 cor #2374e1

<page4>
<fundo> #18191a
<t> 🔔 Notificações <t> #e4e6eb
<p> Você não possui novas notificações no momento. <p> #b0b3b8
<b> Voltar ao Feed <b> <f> page2 cor #2374e1
✨ Destaques do Recurso:Páginas Infinitas: Crie quantas telas precisar (<page1> até <page999>).Navegação Limpa: A transição é instantânea e oculta automaticamente os elementos das outras telas.Suporte a Componentes: Cada página pode conter gráficos 3D (<f> jogo3D <f>), botões, vídeos, imagens ou qualquer outro comando da linguagem!

## 🧩 Sintaxe Básica mais explicadamente (Tags explicadas)
vamos la eu primeiro vou falar as regras não precisa de parenteses colchetes ou qualquer outra coisa so <> e sempre coloque as tags em linhas proprias so a tag <f>, que não precisa se ela ter que ser a configuração de alguma coisa mais eu sempre recomendo quando começar o codigo sempre coloca a tag <page1> porque ela vai ser a sua primeira pagina em seguida a tag <fundo> ela define a cor de fundo da sua pagina por exemplo "<fundo> blue" vc esta definindo que ela sera azul o fundo azul mais pode ser qualquer cor em ingles, e a tag "<t>" e basicamente o seu titulo e vc tambem pode mudar a cor dele por exemplo "<t> meu titulo <t> red" ou seja seu titulo e vermelho agora a tag <b> ela e simplesmente um botão e vc pode usar ela pra dar um alerta na tela ou passar pra sua pagina 2 ou seja pra <page2> mais vou mostrar como da um alert na tela e tambem a de mudar a cor do botão por exemplo um pouco complexo porque vc precisa usar a tag <f> mais pra explicar rapidamente oque a tag <f> faz, ela vem de função ela e a função de alguma coisa e assim como <b> e botão <fundo> e obviamente o fundo da pagina mais com a tag <f> vc pode escolher oque vai acontecer quando clicar em um botão ou em outros comandos aqui vai o exemplo de um botão verde que apos ser apertado lança um alerta na tela "<b> botão <b> <f> alert "ei vc clicou no botão" <f>", basicamente eu acabei de programar um botão chamado botão que quando clica nele lança uma mensagem alerta na tela dizendo vc clicou no botão , e passar pra pagina 2 tambem e facil aqui vai o exemplo "<b> passar pra pagina 2 <b> <f> page2 <f>", e apos clicado passa pra pagina dois, mais aqui vai oque e a pagina dois e que agora quando eu disse no inicio sempre tem que começar com pagina um a "<page1>" e o botão que ia pra pagina 2 ta la agora e so fechar a tag digitando mais um "<page1>" vc fechou essa base agora vc vai escolher oque tem na pagina 2 e vc pode definir ela do jeito que quiser que nem na pagina 1 e sim vc pode fazer paginas infinitas , aqui eu expliquei o basico de RydenScript obrigado por ler ate aqui.
## Novos comandos (Tags mais novas)
Calculdora adicionada : <f> calculadora <f>
pagiamento adicionado exemplo: <page1>
'<t> pesquise "970" para descobrir '<t> gray
'<fundo> black
'<f> pagiamento 1234 painelSecreto | 970 page2 |
'<page1>
'<page2>
'<t> ola vc descobriu essa pagina '<t> gray
'<page2>

interface adicionada exemplo : '<page1>
'<fundo> #0f172a

'<f> interface retangulo | cor:#1e293b | largura:100% | altura:60px <f>
'<t> RydenScript <t> white

'<p> Bem-vindo à página principal estruturada com componentes visuais! <p> #94a3b8

'<f> interface retangulo | cor:#334155 | largura:300px | altura:180px <f>
'<f> interface retangulo | cor:#334155 | largura:300px | altura:180px <f>
'<f> interface retangulo | cor:#334155 | largura:300px | altura:180px <f>


# Criação complexa e maioria das tags explicadas
# Vamos gerar um arquivo README.md real e estruturado para o projeto RydenScript
readme_content = """# 🎮 RydenScript

Uma engine de jogos autoral e interpretador leve baseado em texto, desenhado para criar páginas interativas, menus e jogos 2D estilo plataforma de forma totalmente simples e intuitiva.

---

## 🚀 Como Funciona a Sintaxe

O RydenScript utiliza gatilhos simples com o prefixo `<f>` para executar comandos visuais, criar textos, botões de navegação e instanciar o motor de blocos 2D.

### Guia Rápido de Comandos

| Comando / Tag | Descrição | Exemplo de Uso |
| :--- | :--- | :--- |
| **`<pageX>`** | Define o início de uma nova página/cenário independente. | `<page1>` |
| **`<fundo>`** | Define a cor de fundo exclusiva da página atual (ex: `#111111`). | `<fundo> #111111` |
| **`<t>`** | Cria um título estilizado com cor personalizada. | `<t> #fff Meu Jogo` |
| **`<p>`** | Cria um parágrafo de texto com cor personalizada. | `<p> #ccc Bem-vindo ao jogo!` |
| **`<b>`** | Cria um botão interativo de navegação ou ação. | `<b> Ir para a Fase 2 <f> page2` |

---

## 📦 Biblioteca: `bloco2D`

O comando `bloco2D` é o coração da criação de mapas, plataformas e interações no RydenScript. Ele aceita parâmetros de largura, altura, posição X/Y, visual (cor hexadecimal ou link direto de imagem) e o tipo de comportamento.

> **⚠️ Nota importante sobre formatação no GitHub:** No Markdown padrão, algumas tags angulares como `<page>` ou `<f>` podem ser ocultadas pelo renderizador se colarem com texto puro. Por isso, utilize sempre blocos de código (` ```
```text?code_stdout&code_event_index=2
README.md gerado com sucesso!

```text `) ou mantenha espaçamentos claros para garantir que a documentação exiba os caracteres perfeitamente!

### Tabela de Tipos de Blocos 2D

| Tipo (`tipo`) | Descrição e Comportamento | Parâmetro Extra (`extra`) | Exemplo de Código |
| :--- | :--- | :--- | :--- |
| **`normal`** | Cria um bloco sólido de colisão (chão, paredes ou plataformas). Suporta cor em HEX ou link de imagem. | *Nenhum* | `<f> bloco2D 600 20 0 350 #444444 normal` |
| **`player`** | Cria o personagem principal controlável com física de gravidade, pulo (Espaço/W) e movimentação (A/D). | *Nenhum* | `<f> bloco2D 40 40 50 300 #00ffcc player` |
| **`pagina`** | Funciona como um portal. Se o player colidir com ele, muda instantaneamente para outra página do projeto. | ID de destino (ex: `page2`) | `<f> bloco2D 50 50 200 300 https://site.com/img.png pagina page2` |
| **`superpulo`** | Bloco especial que aumenta temporariamente a força do pulo do player ao ser tocado. | *Nenhum* | `<f> bloco2D 50 20 400 250 #ffff00 superpulo` |
| **`elimina`** | Obstáculo ou armadilha perigosa que reseta a posição do player ao encostar. | *Nenhum* | `<f> bloco2D 50 20 150 280 #ff3300 elimina` |

---

## 📝 Exemplo Completo de Jogo no RydenScript

Cole o código abaixo no seu interpretador ou arquivo `.rds` para testar um cenário completo com menu, física e transição de páginas:

```text
<page1>
<fundo> #0f172a
<t> #38bdf8 Menu Principal - RydenScript
<p> #94a3b8 Escolha uma opção para começar:
<b> Iniciar Aventura <f> page2

<page2>
<fundo> #111111
<t> #fff Fase 1: O Labirinto
<p> #ccc Use A e D para andar e W/Espaço para pular.

<f> bloco2D 600 20 0 350 #444444 normal
<f> bloco2D 50 50 200 300 https://upload.wikimedia.org/wikipedia/commons/4/47/React.svg pagina page1
<f> bloco2D 40 40 50 300 #00ffcc player

# ⚙️ Administract Coder — Documentação Oficial & Comandos de Automação

O **Administract Coder** é a linguagem de automação, painéis e controle administrativo do ecossistema Maiom Corp. Integrada diretamente ao motor do RydenScript, ela capacita o desenvolvedor a estruturar sistemas de acesso, fluxos de dados, criação de arquivos, painéis de gerenciamento e ferramentas utilitárias avançadas.

---

## 📋 Tabela de Comandos de Administração e Automação

| Comando / Sintaxe | Descrição / Função no Sistema | Exemplo de Uso |
| :--- | :--- | :--- |
| `<fundo> [cor]` | Define a cor de fundo padrão da página ou painel atual. | `<fundo> #f4f6f9` |
| `<t> [texto] <t> [cor]` | Cria um título formatado com a cor personalizada. | `<t> Central <t> #333` |
| `<p> [texto] <p> [cor]` | Cria um parágrafo de texto descritivo. | `<p> Descrição <p> #666` |
| `<f> administract>c> gerar [arquivo] \| destino [local] \| conteudo "[texto]"` | Automatiza a criação e geração instantânea de arquivos físicos de diferentes estruturas. | `<f> administract>c> gerar main.js \| destino area_trabalho \| conteudo "console.log('Online!');"` |
| `<f> administract>c> mensagem "[texto]"` | Dispara mensagens e alertas automatizados do sistema do Administract Coder. | `<f> administract>c> mensagem "Sistema iniciado!"` |
| `<f> administract>c> abrir [aplicativo/url] \| espera [segundos]` | Automatiza a abertura de programas executáveis ou páginas web com tempo de espera programado. | `<f> administract>c> abrir notepad.exe \| espera 3` |
| `<f> pagiamento [senha] [pagina]` | Cria códigos de acesso rápidos para redirecionar o fluxo e proteger áreas do sistema. | `<f> pagiamento 1234 painelSecreto` |
| `<f> salvarLocal "[chave]"` | Gerencia o armazenamento local (`localStorage`) salvando e carregando dados direto na interface. | `<f> salvarLocal "usuarioConfig"` |
| `<f> cronometro` | Aciona um cronômetro completo de precisão com controles de iniciar, pausar e resetar. | `<f> cronometro` |

---

## 🚀 Exemplo Completo de Script com o Administract Coder

```html
<fundo> #f4f6f9
<page1>
<t> Central de Automação Avançada - Maiom Corp <t> #333
<p> Crie diferentes estruturas de arquivos instantaneamente: <p> #666

<f> administract>c> gerar main.js | destino area_trabalho | conteudo "console.log('Sistema Maiom Corp Online!');"
<f> administract>c> gerar notas.txt | destino documentos | conteudo "Lista de tarefas pendentes do projeto."
<f> administract>c> gerar config.json | destino pasta_atual | conteudo "{\n  \"versao\": \"2.0\",\n  \"status\": \"ativo\"\n}"

<f> administract>c> mensagem "Olá Daniel! Sistema da Maiom Corp iniciado com sucesso."
<f> administract>c> abrir notepad.exe | espera 3
<f> administract>c> abrir [https://www.google.com](https://www.google.com) | espera 5

# 🌐 RydenScript - Documentação de Recursos (v2.0)

Bem-vindo à documentação oficial dos recursos do **RydenScript**. Abaixo estão detalhadas as especificações, sintaxes e descrições da nova tag de rede **P2P** e da função de navegação do **menu**.

## 📋 sistema de comunicação P2P e menu lateral

| Recurso / Componente | Sintaxe no Código | Descrição / Comportamento |
| :--- | :--- | :--- |
| **P2P (ID do Nó)** | `<P2P id>` | Gera e exibe na tela o ID aleatório exclusivo do usuário na rede descentralizada. |
| **P2P (Painel de Envio)** | `<P2P input>` | Insere o painel interativo de comando para digitar o ID do destino, mensagem e enviar. |
| **P2P (Histórico/Chat)** | `<P2P chat>` | Renderiza a janela de histórico onde as mensagens trocadas via WebRTC aparecem em tempo real. |
| **Função Menu** | `<f> menu \| cor: [hex] \| cormenu: [hex] \| paginas: Nome:pageID,...` | Cria dinamicamente a barra de navegação superior customizada, permitindo alternar entre as páginas do script. |

---

### 💡 Exemplo de Uso Prático (RydenScript com Menu e P2P)

```text
<page1>
<f> menu | cor: #ff5722 | cormenu: #222 | paginas: Home:page1, Creditos:page2, Videos:page3
<t> Olá mundo! <t>
<p> Compartilhe seu ID P2P: <p>
<P2P id>
<P2P input>
<P2P chat>
