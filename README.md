# Portfólio · Josué Mbele

Portfólio de página única (single page) de **Josué Mbele**, estudante de Engenharia de Software. Feito só com **HTML5, CSS3 e JavaScript puro**, sem frameworks e sem dependências externas. O visual é minimalista, com a cor principal **#4060F5**.

## Estrutura de arquivos

```
portfolio/
├── index.html        # estrutura da página + JavaScript (no final do arquivo)
├── style.css         # todos os estilos
├── README.md
├── imagens/
│   └── infografico.png
├── video/
│   └── video.mp4
├── audio/
│   └── audio.mp3
├── animacao/
│   └── animacao.mp4
└── musica/
    └── musica.mp3
```

> O `index.html` carrega o estilo com `<link rel="stylesheet" href="style.css">`. Os dois arquivos precisam ficar **na mesma pasta**.

As pastas de mídia (`video`, `audio`, `animacao`, `musica` e `imagens/infografico.png`) **não vêm prontas**. Crie as pastas e coloque seus arquivos com exatamente esses nomes, ou ajuste o caminho no HTML.

## Como abrir

1. Baixe `index.html` e `style.css` e deixe na mesma pasta.
2. Dê dois cliques em `index.html` para abrir no navegador.

Não precisa instalar nada nem rodar servidor. Para testar localmente com servidor, qualquer um serve, por exemplo `python -m http.server`.

## Seções da página

| # | Seção | Âncora | O que tem |
|---|-------|--------|-----------|
| 1 | Início (hero) | `#inicio` | Nome, profissão, texto curto, foto de perfil e o botão **MEUS PROJETOS** |
| 2 | Sobre mim | `#sobre` | Habilidades (tags) e texto de apresentação |
| – | Projetos | `#projetos` | Destino do botão do hero |
| 3 | Vídeo | `#video` | Player de vídeo (`video/video.mp4`) |
| 4 | Áudio | `#audio` | Card com player de áudio (`audio/audio.mp3`) |
| 5 | Imagem | `#imagem` | Imagem de destaque com zoom ao passar o mouse e legenda |
| 6 | Infográfico | `#infografico` | Imagem que abre ampliada ao clicar; rola para os lados no celular |
| 7 | Animação | `#animacao` | Player de vídeo (`animacao/animacao.mp4`) |
| 8 | Música | `#musica` | Player de áudio com disco girando e equalizador animado |
| 9 | Rodapé | – | Nome, frase, ano automático e 5 links de redes sociais |

## O que o JavaScript faz

- Mostra o **ano atual** no rodapé automaticamente.
- Muda o fundo do **cabeçalho** quando a página é rolada.
- **Menu mobile** (abre e fecha pelo botão ou com `Esc`, e fecha ao tocar num link).
- Animação de **entrada suave** das seções ao rolar (`IntersectionObserver`).
- **Item ativo no menu** conforme a seção visível.
- A **foto do hero** acompanha o movimento do mouse (apenas em telas com mouse).
- **Lightbox** do infográfico (usa o elemento `<dialog>`; clique fora para fechar).
- **Equalizador** da música: as barras são criadas por JS e animam enquanto o áudio toca.
- **Só uma mídia toca por vez**: ao dar play em um áudio ou vídeo, os outros pausam.
- Respeita `prefers-reduced-motion` (efeito de mouse desligado para quem prefere menos animação).

## Como personalizar

**Textos.** Edite direto no `index.html`: nome, profissão, parágrafos da seção "Sobre mim", frase do rodapé. Os pontos editáveis têm comentários como `<!-- EDITE O TEXTO DE INTRODUÇÃO -->`.

**Habilidades.** Estão na lista `<ul class="tags">`. Existe um `<li></li>` vazio no final; preencha com uma habilidade ou apague.

**Redes sociais.** No rodapé, troque cada `href="#"` pelo seu link (Instagram, LinkedIn, GitHub, YouTube e outra rede).

**Cor principal.** Altere o valor `#4060F5` no `style.css`. Se a cor estiver definida como variável no início do arquivo, basta mudar ali.

**Mídias.** Troque os arquivos nas pastas mantendo o mesmo nome, ou altere o `src` no HTML:

```html
<source src="video/video.mp4" type="video/mp4">
<source src="audio/audio.mp3" type="audio/mpeg">
```

**Fotos embutidas.** A foto de perfil e a imagem da seção "Imagem" estão embutidas no HTML como **base64** (`src="data:image/jpeg;base64,..."`), para funcionarem mesmo sem a pasta `imagens/`. Para trocar, substitua o `src` por um caminho normal:

```html
<img src="imagens/perfil.jpg" alt="Foto de perfil de Josué Mbele">
<img src="imagens/imagem.jpg" alt="...">
```

Isso também deixa o `index.html` bem mais leve (hoje ele passa de 800 KB).

## Acessibilidade e responsividade

- Layout adaptável a celular, tablet e desktop, com `meta viewport`.
- `lang="pt-BR"`, textos alternativos (`alt`) nas imagens, `aria-label` nos botões e na navegação.
- Players com controles nativos do navegador e texto alternativo para navegadores sem suporte.

## Publicar online

Por ser um site estático, funciona em qualquer hospedagem gratuita: **GitHub Pages**, **Netlify** ou **Vercel**. Envie a pasta inteira (HTML, CSS e as pastas de mídia) e use o `index.html` como página inicial.

## Tecnologias

HTML5 · CSS3 · JavaScript (ES5, sem bibliotecas)

## Autor

**Josué Mbele**, estudante de Engenharia de Software (Anhembi Morumbi). © Todos os direitos reservados.
