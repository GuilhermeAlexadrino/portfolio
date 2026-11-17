# Portfólio Acadêmico

Aluno: Guilherme Alexandrino
Curso: Técnico em Desenvolvimento de Sistemas (componente Desenvolvimento de Sistemas I)
Atividade: Agenda 15 - Portfólio: um projeto do início ao fim

## Descrição do portfólio

Este projeto é a minha página de portfólio pessoal. Ele apresenta quem eu sou, as tecnologias que estudo, os projetos que desenvolvi ao longo do curso e as formas de entrar em contato comigo.

A página é responsiva: o layout se adapta a computador, tablet e celular. Ela foi feita como atividade do curso e é a minha vitrine para mostrar o que já aprendi com HTML, Bootstrap e Git/GitHub.

## Link do site publicado

[COLE AQUI O LINK DO GITHUB PAGES]

## Tecnologias utilizadas

O site foi feito usando apenas HTML e Bootstrap, sem JavaScript próprio e sem arquivo de CSS separado.

- HTML5: estrutura da página
- Bootstrap 5.3.3 (CSS e JavaScript via CDN): grid, navbar, carousel, cards e botões

Alguns ajustes pequenos de estilo, incluindo o recurso novo, estão escritos em CSS dentro do próprio `index.html` (tag `<style>`).

Apoio ao projeto:

- Devicon: ícones das tecnologias
- Git e GitHub: controle de versão e repositório
- GitHub Pages: publicação do site

## Estrutura do projeto

```
portfolio/
├── index.html     página principal
├── README.md      este arquivo
└── *.png          imagens do site (slide1-3, perfil e p1-p3), na mesma pasta do index.html
```

## Como o projeto funciona

O site é uma página única, dividida em blocos que aparecem de cima para baixo:

1. Navbar: menu fixo no topo (`sticky-top`). Cada link aponta para o id de uma seção (`#perfil`, `#projetos` e `#contato`), então ao clicar a página rola até ela. Em telas pequenas, o menu vira um botão que abre e fecha (`navbar-toggler`).
2. Carousel: área de destaque com 3 slides, transição suave (`carousel-fade`), indicadores e botões de avançar e voltar. Um pequeno ajuste de estilo faz a altura acompanhar a proporção da imagem, então o slide aparece inteiro em qualquer tela.
3. Perfil: layout em duas colunas (`col-lg-4` e `col-lg-8`). À esquerda ficam a foto, o nome e a etiqueta; à direita, o texto de apresentação, os cards de informações (localização, área de interesse, formação e objetivo) e as tecnologias com ícones.
4. Projetos: três cards com imagem, título, descrição e um botão que abre o repositório de cada projeto no GitHub. Os cards têm a mesma altura (`h-100`) e o botão fica sempre no fim do card (`mt-auto`).
5. Contato: um card central com botões para e-mail, GitHub e LinkedIn, e a localização.
6. Rodapé: texto de direitos e as tecnologias usadas.

A responsividade vem do sistema de grid do Bootstrap, com a meta tag `viewport` no `<head>`. Por exemplo, os cards de projetos ocupam a largura inteira no celular, dois por linha no tablet e três por linha em telas grandes (`col-md-6 col-xl-4`).

## Recurso novo adicionado

Efeito hover com transição nos cards.

Ao passar o mouse sobre um card das seções Perfil e Projetos, ele sobe suavemente e ganha uma sombra mais forte. Isso dá um retorno visual ao usuário e deixa a página mais interativa e moderna. O recurso vai além do que foi feito em aula, onde os cards eram estáticos.

### Como foi implementado

O efeito usa apenas CSS, dentro da tag `<style>` do `index.html`:

```css
#perfil .card,
#projetos .card {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

#perfil .card:hover,
#projetos .card:hover {
    transform: translateY(-8px);
    box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.15) !important;
}
```

Explicação:

- `#perfil .card, #projetos .card` seleciona apenas os cards dessas duas seções, e o card de contato não é afetado.
- `transition` diz ao navegador para animar as propriedades `transform` e `box-shadow` em 0.3 segundo, com aceleração suave (`ease`). Sem ela, a mudança seria instantânea.
- `:hover` é a pseudo-classe que vale somente enquanto o mouse está sobre o elemento.
- `transform: translateY(-8px)` move o card 8 pixels para cima.
- `box-shadow` aumenta e escurece a sombra. O `!important` é necessário porque a classe `shadow-sm` do Bootstrap também usa `!important` na sombra, e sem ele a regra nova seria ignorada.

## Como executar localmente

1. Baixe ou clone o repositório.
2. Abra o arquivo `index.html` no navegador.

O site precisa de internet para carregar o Bootstrap e os ícones pelo CDN.

## Autor

Guilherme Alexandrino

- GitHub: https://github.com/GuilhermeAlexadrino
- LinkedIn: https://www.linkedin.com/in/guilherme-alexandrino-b95736432/
