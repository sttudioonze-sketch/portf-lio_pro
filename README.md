# Portfólio PRO — Landing Page

Landing page de alta performance para o Portfólio PRO, serviço de portfólios e CVs executivos para treinadores e profissionais do futebol.

Site estático (HTML puro, sem build), responsivo para mobile, tablet e desktop.

## Estrutura

```
.
├── index.html                  # página completa do site
├── favicon.ico
├── favicon-16x16.png
├── favicon-32x32.png
├── apple-touch-icon.png
├── android-chrome-192x192.png
├── android-chrome-512x512.png
├── site.webmanifest
├── og-image.jpg                 # imagem de compartilhamento (WhatsApp, redes sociais)
├── img/                         # imagens da página — cache de 1 ano via vercel.json
│   ├── hero-desktop.webp        # 1800×1250 — só baixa acima de 781px
│   ├── hero-mobile.webp         #  900×1600 — só baixa até 780px
│   ├── sobre-desktop.webp
│   ├── sobre-mobile.webp
│   ├── logo-pro.png             # usado em dois lugares, um arquivo só
│   └── logo-pro-lockup.png
├── robots.txt
└── vercel.json                  # cache de assets estáticos na Vercel
```

## Publicar no GitHub

```bash
git init
git add .
git commit -m "Primeira versão da landing page Portfólio PRO"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
git push -u origin main
```

(Crie antes o repositório vazio em https://github.com/new — sem README, sem .gitignore, para não gerar conflito.)

## Publicar na Vercel

**Opção A — pelo site da Vercel (mais simples):**
1. Acesse https://vercel.com/new
2. Importe o repositório do GitHub que você acabou de criar
3. Framework preset: **Other** (é um site estático puro, sem build necessário)
4. Build command: deixe em branco
5. Output directory: deixe em branco (raiz do projeto)
6. Clique em **Deploy**

**Opção B — pela CLI da Vercel:**
```bash
npm install -g vercel
vercel login
vercel --prod
```

Depois do deploy, a Vercel gera uma URL pública (ex: `seu-projeto.vercel.app`). Você pode depois conectar um domínio próprio em Settings → Domains, dentro do painel do projeto na Vercel.

## Editar o conteúdo

Todo o site está em um único arquivo `index.html` (HTML + CSS + JavaScript inline, sem dependências externas além da fonte do Google Fonts). Para editar textos, basta abrir esse arquivo em qualquer editor de texto e localizar a seção desejada pelo `id` (ex: `id="contato"`, `id="sobre"`, `id="faq"`).
