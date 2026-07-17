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

* **Visualização em Grelha (Grid):** ```text
  <f> grid 3 3 <f>
