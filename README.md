# 🛡️ RydenScript Engine 👾

**RydenScript** é uma linguagem de marcação e motor de jogos simplificado concebido para transformar a complexidade do desenvolvimento web, de utilitários e de jogos (2D e 3D) numa autêntica brincadeira de crianças!

Ela traduz comandos extremamente intuitivos em código HTML5, CSS3, Canvas e WebGL (via Three.js), permitindo que qualquer pessoa — desde iniciantes a programadores experientes — crie aplicações completas e mundos interativos em segundos sem tocar numa única linha de código complexo.

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
<f> mapa cor "blue" <f>
<f> jogador cor "yellow" <f>
<f> obstaculos cor "red" <f>
<f> jogo2D <f>

jogo estilo dinossauro quando acaba a internet ou mario 
<f> marioCenario "[https://link.com/fundo.png](https://link.com/fundo.png)" <f>
<f> marioJogador "[https://link.com/jogador.png](https://link.com/jogador.png)" <f>
<f> marioInimigo "[https://link.com/inimigo.png](https://link.com/inimigo.png)" <f>
<f> marioChao "[https://link.com/chao.png](https://link.com/chao.png)" <f>
<f> mario <f>

Tetris
<f> tetrisFundo cor "black" <f>
<f> tetrisBloco "[https://link.com/bloco.png](https://link.com/bloco.png)" <f>
<f> tetris <f>

Codificação pra jogo 3D
bloco3D [X] [Y] [Z] [Largura] [Altura] [Profundidade] "Cor_ou_Link_Textura" [Comportamento] ["Mensagem_Opcional"]

Jogo de parkur exemplo 3D
<fundo> #16161a
<t> 🛠️ Meu Jogo de Parkour 3D 🛠️ <t> #00e1ff

# Configuração da skin do Jogador (Suporta upload de arquivo local também!)
<f> jogador3D "[https://img.icons8.com/emoji/96/dog-emoji.png](https://img.icons8.com/emoji/96/dog-emoji.png)" <f>

# Textura padrão do chão
<f> mapa3D "#55aa55" <f>

# Construção das plataformas do mapa
bloco3D 0 0 0 5 1 5 "#55aa55" normal
bloco3D 0 1.5 -7 3 1 3 "[https://img.icons8.com/color/48/minecraft-grass-block.png](https://img.icons8.com/color/48/minecraft-grass-block.png)" normal
bloco3D 0 -2 -14 8 1 8 "#ff3300" elimina "🔥 A lava derreteu-te! Voltaste ao início!"
bloco3D 4 3 -21 3 1 3 "#00ffd5" notifica "📢 Checkpoint Secreto Ativado!"
bloco3D 0 5 -28 4 1 4 "#ffd700" notifica "🏆 PARABÉNS! Completaste o Parkour!"

# Inicialização da Engine 3D
<f> jogo3D <f>

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
