# Fio Condutor Tecnologia

Site institucional conceitual para portfólio, feito com SvelteKit, TypeScript e CSS. O projeto gera páginas estáticas para publicação na Netlify.

## Rodar localmente

```powershell
npm install
npm run dev
```

Abra o endereço local exibido pelo Vite. Para validar a tipagem e gerar a versão estática:

```powershell
npm run check
npm run build
```

## Páginas

- `/` — início
- `/solucoes` — serviços
- `/demonstracoes` — exemplos conceituais
- `/processo` — etapas de trabalho
- `/insights` — conteúdo editorial demonstrativo
- `/contato` — formulário que prepara a mensagem no WhatsApp informado

## Antes de publicar

- O nome da empresa e as telas demonstrativas são conceituais.
- O formulário não envia nem armazena dados: abre o WhatsApp com a mensagem preenchida.
- O WhatsApp usa o número informado `83998739712`.
- Atualize o host de demonstração em `static/sitemap.xml` e `static/robots.txt` quando definir o endereço final. Não há dados estruturados de empresa porque nome, endereço e operação são fictícios.
- Revise os artigos conceituais antes de tratá-los como conteúdo editorial publicado.
- Tipografias Syne, DM Sans e IBM Plex Mono carregam via Google Fonts; há fallbacks locais.

## Ativos visuais

A imagem editorial gerada para o projeto está em `static/images/fio-condutor-editorial.webp`. Logos vetoriais editáveis e PNGs transparentes estão em `static/logos/`; o favicon usa o mesmo símbolo.
