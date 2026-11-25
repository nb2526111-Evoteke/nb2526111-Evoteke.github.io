# Rinaldo — Portfólio & Palavra Viva

Site estático publicado no GitHub Pages.

- **Home:** apresentação, projetos e últimos artigos.
- **Portfólio:** sobre o trabalho, habilidades e princípios.
- **Projetos:** cards dos projetos públicos.
- **Blog:** prévia estática dos artigos publicados do Palavra Viva.

## URLs

- https://nb2526111-evoteke.github.io/
- https://nb2526111-evoteke.github.io/portfolio.html
- https://nb2526111-evoteke.github.io/projetos.html
- https://nb2526111-evoteke.github.io/blog/

## Como o blog é gerado

O conteúdo vem do banco SQLite do projeto `palavra-viva`. O script
`scripts/export-portal-blog.ts`, no repositório do blog, lê os artigos publicados e
gera as páginas em `blog/`, atualiza os cards da home e o `sitemap.xml`.

```bash
# no repositório palavra-viva
npx tsx scripts/export-portal-blog.ts
```

O blog completo (Bíblia interativa, biblioteca, planos e painel) roda no
GitHub Codespaces:

https://codespaces.new/nb2526111-Evoteke/palavra-viva

## Estrutura

```text
.
├─ index.html
├─ portfolio.html
├─ projetos.html
├─ 404.html
├─ blog/                 # gerado a partir do banco do blog
├─ assets/
│  ├─ style.css
│  ├─ app.js
│  ├─ favicon.svg
│  └─ images/temas/
├─ .github/workflows/pages.yml
└─ README.md
```

## Desenvolvimento

Não há build. Basta abrir `index.html` no navegador ou servir a pasta:

```bash
npx serve .
```

## Publicação

Cada push em `main` dispara o workflow do GitHub Pages. O site é publicado em
`https://nb2526111-evoteke.github.io/`.

## Licença

Código sob MIT. Conteúdo editorial e textos bíblicos têm licenças próprias:
Bíblia Livre (BLIVRE), CC BY 4.0 BR; fotos Unsplash; ícones e fontes conforme
o projeto Palavra Viva.
