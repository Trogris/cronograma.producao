# Cronograma de Produção — Fiscaltech 2026

Ferramenta interativa de planejamento de produção (Gantt, Análise de Capacidade e
Previsto x Realizado), com sincronização opcional para uma planilha Google Sheets.

- **Arquivo único:** `index.html` — não tem build, nem dependências externas de CSS/JS.
- Abrir localmente: dê duplo clique no `index.html`.
- Para publicar num link, veja as opções no final deste arquivo.

## Aviso — dados sensíveis

Este arquivo contém dados reais de contratos, clientes e prazos da Fiscaltech.
**Não deixe o link acessível publicamente sem controle de acesso.**

## Publicar com acesso restrito (grátis)

O GitHub Pages sozinho não tem como exigir login em contas gratuitas/Pro — o link fica
acessível pra qualquer pessoa que o receba. Duas formas reais de restringir o acesso:

### Opção A — Cloudflare Pages + Cloudflare Access (recomendado)
1. Suba este repositório no GitHub (pode ficar privado).
2. Crie uma conta grátis em https://dash.cloudflare.com → Workers & Pages → Create → Pages
   → conecte ao repositório do GitHub → deploy (raiz do projeto, sem build command).
3. No mesmo painel, vá em **Zero Trust → Access → Applications → Add an application**
   → tipo "Self-hosted" → aponte pro domínio que o Cloudflare Pages gerou.
4. Configure uma política de acesso (ex: "permitir só e-mails @fiscaltech.com.br", ou uma
   lista específica de e-mails). Grátis para até 50 usuários.
5. Resultado: quem acessar o link precisa confirmar o e-mail (código enviado por e-mail)
   antes de ver a página.

### Opção B — Netlify/Vercel (link "não listado", sem login de verdade)
1. Suba este repositório no GitHub (pode ficar privado).
2. Crie uma conta grátis em https://netlify.com ou https://vercel.com → "New site/project
   from Git" → conecte o repositório → deploy (sem build command, publish directory = raiz).
3. Você recebe um link tipo `nome-do-projeto.netlify.app`. Ele **não pede login** — qualquer
   pessoa com o link acessa. Só não é público "descoberto" (não aparece em buscas), mas não
   é controle de acesso de verdade.

## Sincronização com Google Sheets

O botão "Salvar no Sheets" só funciona quando o arquivo está hospedado normalmente na web
(GitHub Pages, Cloudflare Pages, Netlify, Vercel etc.) — **não funciona se publicado como
Artifact do Claude**, porque a sandbox do Artifact bloqueia chamadas para fora.
