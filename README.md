# 🛡️ RydenScript

**RydenScript** é uma linguagem de marcação simplificada criada para facilitar o desenvolvimento de páginas web sem precisar escrever diretamente em HTML.  
Ela traduz comandos intuitivos em código HTML e CSS, permitindo que qualquer pessoa construa interfaces rapidamente.

---

## 🚀 Visão Geral

RydenScript foi projetada para ser **fácil, rápida e visual**.  
Com uma sintaxe minimalista, você pode criar páginas completas usando comandos simples como `<t>`, `<p>`, `<b>`, `<fundo>`, `<image>`, `<video>` e `<iframe>`.

---

## 🧩 Sintaxe Básica

| Comando | Função | Exemplo |
|----------|--------|----------|
| `<fundo>` | Define a cor de fundo da página | `<fundo> lightblue` |
| `<t>` | Cria um título colorido | `<t> Minha Página <t> red` |
| `<p>` | Cria um parágrafo colorido | `<p> Texto azul <p> blue` |
| `<b>` | Cria um botão com ação | `<b> Botão <b> <f> alert Você clicou! <f> cor green` |
| `<f>` | Define funções internas | `<f> grid 2 2 <f>` |
| `<image>` | Insere uma imagem | `<image> url "https://via.placeholder.com/150" <image>` |
| `<video>` | Insere um vídeo | `<video> url "https://www.w3schools.com/html/mov_bbb.mp4" <video>` |
| `<iframe>` | Insere um iframe | `<iframe> url "https://www.example.com" <iframe>` |

---

## 🧠 Como Funciona

O compilador RydenScript lê cada linha e converte os comandos em HTML.  
Por exemplo:

```ryden
<fundo> lightblue
<t> Minha Página <t> red
<p> Texto azul <p> blue
<video> url "https://www.w3schools.com/html/mov_bbb.mp4" <video>
