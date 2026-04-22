# Escopo

A proposta não é criar algo original, mas **copiar fielmente um layout existente**, entendendo como ele foi construído. 

[Link de referencias](https://github.com/neoukunft/ozymandias/blob/main/references-landing-pages.md)

## Regra de ouro pra iniciante

Se fizer isso aqui, já está acima de 90% dos iniciantes:

- NÃO usar `div` pra tudo → usar `section`, `header`, `main`
- NÃO usar CSS inline
- NÃO misturar responsabilidade (HTML ≠ CSS)
- Nomear classes direito (`hero-title`, não `text1`)

## Etapas

1. **Estrutura (HTML)**
    - Criar o esqueleto da página
    - Usar tags semânticas (`header`, `main`, `section`, `footer`)
2. **Estilo (CSS)**
    - Aplicar cores, tipografia e espaçamento
    - Organizar o CSS em arquivos separados
3. **Responsividade**
    - Adaptar para mobile e tablet
    - Usar media queries
4. **SEO básico**
    - Meta tags no `<head>`
    - Uso correto de headings (`h1` até `h3`)
    - Estrutura limpa e legível

## 1. Criar repositório

- Nome: `landing-page-[algum-nome-aqui]` (simples, direto)
- README desde o começo (explicar o objetivo: reproduzir template)
- Ativar GitHub Pages depois

---

## 2. Estrutura básica de pastas

Usa isso aqui sem inventar moda:

```
landing-page-[algum-nome-aqui]/
│
├── index.html
├── README.md
├── .gitignore
│
├── assets/
│   ├── images/
│   ├── icons/
│   └── fonts/
│
├── css/
│   ├── reset.css
│   ├── variables.css (opcional)
│   ├── responsive.css
│   └── style.css
│
├── js/
│   └── main.js
│
└── seo/
    ├── sitemap.xml
    └── robots.txt
```

## 3. O porquê de cada coisa (sem enrolação)

### `/index.html`

- Estrutura da página (sem pensar em beleza ainda)
- Só semântica: header, section, footer

---

### `/assets`

- Tudo que é arquivo estático
- **Regra:** nunca misturar imagem com CSS/JS

---

### `/css`

- `reset.css` → zera bagunça dos navegadores
- `variables.css` → cores, fontes, espaçamentos (opcional)
- `style.css` → layout principal
- `responsive.css` → media queries separadas (iniciante entende melhor)

---

### `/js`

- Mesmo que não use agora, já cria
- Evita gambiarra depois

---

### `/seo`

- `robots.txt` → controle de indexação
- `sitemap.xml` → ajuda Google entender estrutura

---

## 4. Ordem de execução (o que ele deve fazer)

### PASSO 1 — HTML puro (esqueleto)

- Só marcação sem estilo
- Separar bem:
    - header
    - hero
    - features
    - footer

### PASSO 2 — Reset + Estilo

**Dica extra: Antes de começar, te indico ler esse site que explica [as diferenças e composição de Grid e Flex para Layout](https://dev.to/codecasts/grid-para-layout-flexbox-para-componentes-gb3)**

- Importa no HTML:
```
<link rel="stylesheet" href="css/reset.css">
<link rel="stylesheet" href="css/responsive.css">
<link rel="stylesheet" href="css/style.css">
```

1. Copiar o reset.css desse [link](https://meyerweb.com/eric/tools/css/reset/)
2. Em responsive.css, criar as classes de [Grid](https://www.origamid.com/projetos/css-grid-layout-guia-completo/) e [Flex](https://origamid.com/projetos/flexbox-guia-completo/) Containers
3. O style.css será os demais estilos do projeto


### PASSO 3 — Estilo base

- Primeiro desktop (mais fácil de copiar template)
- Depois refine para demais telas.

Links:

- [HTML Responsive Web Design](https://www.w3schools.com/html/html_responsive.asp)
- [Responsive Web Design](https://www.w3schools.com/css/css_rwd_intro.asp)
- [Responsive Web Design - Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)
- [W3.CSS Responsive Fluid Grid](https://www.w3schools.com/w3css/w3css_responsive.asp)


### PASSO 4 — Responsividade

- Começa pelo mobile depois ajusta (ou desktop-first se for cópia)

Links: 

- [Media Queries for Standard Devices](https://css-tricks.com/snippets/css/media-queries-for-standard-devices/)
- [CSS Media Queries Guide](https://css-tricks.com/a-complete-guide-to-css-media-queries/)


### PASSO 5 — SEO básico (obrigatório)

No `<head>`:

```
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Descrição da landing page">
<title>Título da página</title>
```

Links:

- [HTML Semantic Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)
- [HTML5: Aprenda o Básico Essencial de SEO com HTML](https://blog.codapp.com.br/html5-aprenda-o-basico-essencial-de-seo-com-html/)

### PASSO 6 — Publicar

- [Subir no GitHub](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository)
- [Ativar GitHub Pages](https://docs.github.com/pt/pages/quickstart)
- Validar no navegador real
