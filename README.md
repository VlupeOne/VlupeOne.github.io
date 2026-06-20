# Thiago Pimentel — Portfólio

Site de portfólio pessoal publicado via GitHub Pages.

🌐 **[vlupeone.github.io](https://vlupeone.github.io/)**

---

## Sobre o projeto

Portfólio profissional focado em apresentar projetos, serviços e forma de trabalho para
potenciais clientes e recrutadores na área de desenvolvimento full stack.

O site foi construído intencionalmente com HTML, CSS e JavaScript puros — sem framework,
sem build obrigatório, sem dependências externas — para garantir desempenho máximo,
manutenção simples e funcionamento direto no GitHub Pages.

---

## Estrutura

```
VlupeOne.github.io/
├── index.html      Página principal (todo o conteúdo, CSS e JS)
├── 404.html        Página de erro personalizada
├── design/         Conceitos visuais usados no redesign da landing page
├── robots.txt      Diretivas para indexadores
├── sitemap.xml     Mapa do site para SEO
├── og-cover.png    Imagem de compartilhamento (Open Graph)
└── README.md       Este arquivo
```

---

## Como editar os dados de contato

Todos os dados configuráveis estão no bloco `CONFIG` no início do `<script>` em `index.html`:

```js
const CONFIG = {
  WHATSAPP: '5511XXXXXXXXX',   // somente dígitos (55 = Brasil)
  EMAIL:    'SEU@EMAIL.COM',
  LINKEDIN: 'https://linkedin.com/in/SEU-USUARIO-AQUI',
};
```

Substitua os valores pelos seus dados reais. O formulário e os botões de contato passam
a funcionar automaticamente após a configuração.

---

## Como adicionar um projeto ao showcase

Dentro de `#projetos` em `index.html`, duplique um `<article class="project-card">` e edite:

- `.project-status` — texto e classe visual (`wip` para projeto em evolução)
- `<h3>` — título do projeto
- `<p>` — descrição do problema/solução
- `.project-visual` — mockup ou visual ilustrativo em HTML/CSS
- `.tag-row .tag` — tecnologias
- `.project-link href` — link para o repositório

Se adicionar mais cards, ajuste o `project-count` para refletir a quantidade destacada.

---

## Como executar localmente

Não há build. Basta abrir o `index.html` diretamente no navegador ou usar um servidor local simples:

```bash
# Python 3
python -m http.server 8000

# Node.js (com npx)
npx serve .
```

Acesse `http://localhost:8000`.

---

## Como publicar no GitHub Pages

1. Faça commit e push de todos os arquivos para a branch `main` do repositório `VlupeOne/VlupeOne.github.io`
2. O GitHub Pages publica automaticamente em `https://vlupeone.github.io/`
3. A publicação leva entre 30 segundos e 2 minutos

Verifique em **Settings → Pages** se a fonte está configurada como `Deploy from a branch → main → / (root)`.

---

## Recursos de acessibilidade implementados

- Link "Pular para o conteúdo" visível ao receber foco
- HTML semântico com `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<nav>`
- Hierarquia de headings correta (h1 → h2 → h3)
- `aria-label` em todos os botões e ícones sem texto visível
- Carrossel com `role="region"`, `aria-label`, `role="group"` por slide, `aria-live` e navegação por teclado
- Formulário com `<label>` vinculados, `aria-required`, `aria-invalid` e mensagens de erro com `role="alert"`
- Foco visível em todos os elementos interativos
- `prefers-reduced-motion` aplicado no CSS
- Contraste seguindo WCAG 2.2 AA
- Menu mobile acessível por teclado com `aria-expanded`

---

## Decisões de design

- **Fundo escuro com seções claras**: cria contraste visual entre blocos e guia o olhar
- **Azul e vermelho como destaques**: consistentes em todo o site (gradientes, tags, botões)
- **Tipografia sem serifa**: legibilidade em telas de todos os tamanhos
- **Mockups em HTML/CSS/SVG inline**: ilustrações dos projetos sem dependência de imagens externas
- **Showcase de projetos**: cards maiores com contexto, stack e link direto para repositório
- **Sem scroll-snap por cenas**: removido em favor de scroll contínuo para melhor UX mobile
- **Formulário sem servidor**: prepara mensagem para WhatsApp ou e-mail — transparente para o usuário

---

## SEO implementado

- `<title>` e `<meta description>` com nome completo e especialidade
- Open Graph completo com URL absoluta na imagem
- Twitter Card
- `<link rel="canonical">`
- `robots.txt` e `sitemap.xml`
- JSON-LD com `schema:Person` e `schema:WebSite`

---

## Projetos apresentados

| Projeto | Repositório | Status |
|---|---|---|
| Ticketeria | [ticketeria-mvp](https://github.com/VlupeOne/ticketeria-mvp) | Concluído |
| Preço Confirmado | [preco-confirmado-mvp](https://github.com/VlupeOne/preco-confirmado-mvp) | Backend concluído / Frontend em desenvolvimento |

---

## Stack do site

- HTML5 semântico
- CSS3 com variáveis custom
- JavaScript vanilla (sem dependências)
- SVG inline para ilustrações e ícones
- GitHub Pages (hospedagem)
