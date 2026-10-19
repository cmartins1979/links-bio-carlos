# Página de links do Carlos

Página em React + Vite, com animações em Motion (`motion/react`). Mesmo visual e mesma base da página de vendas do livro.

No ar para aprovação: https://pagina-links-carlos.vercel.app

## O que falta preencher

Todos os links ficam em `src/config.js`. Enquanto um link estiver `"#"`, o botão aparece, mas clicar não faz nada.

- `LIVRO_URL`: link do checkout do livro. **Falta.**
- `MENTORIA_URL`: WhatsApp da mentoria, no formato `https://wa.me/55DDDNUMERO`. **Falta.**
- `SUBSTACK_URL`: https://mentordelogistica.substack.com
- `LOGICHECK_URL`: https://mentordelogistica.com.br/logicheck
- `INSTAGRAM_URL`: https://instagram.com/carlosermartins
- `LINKEDIN_URL`: https://www.linkedin.com/in/carlos-eduardo-ro-martins/

## Como publicar depois de trocar um link

Os links ficam dentro do código compilado. Por isso, depois de editar `src/config.js`, é preciso gerar a página de novo. Não dá para trocar só no `dist/`.

**Pela Vercel (mais simples):** dentro desta pasta, rode `vercel --prod`. A Vercel instala, compila e publica sozinha. Não precisa rodar `npm install` na máquina.

**Em outra hospedagem:** precisa do Node 18 ou mais novo.

```
npm install
npm run build    # gera a pasta dist/
```

Depois é só enviar o conteúdo de `dist/` para a hospedagem. Funciona em qualquer servidor estático. Para publicar numa subpasta (por exemplo, site.com/links), compile com `npx vite build --base=/links/`.

A pasta `dist/` deste pacote é a versão que está no ar hoje, ainda sem os links do livro e da mentoria.

## Onde fica cada coisa

- Textos e ordem dos cards: `src/App.jsx`
- Cores e layout: `src/styles.css`
- Imagens: `public/img/`

## Fontes

Outfit (títulos) e Manrope (texto), ambas do Google Fonts, com licença livre, embutidas pelo pacote `@fontsource`.
