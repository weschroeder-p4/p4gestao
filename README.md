# Planilha Inteligente de Precificação — Landing Page

Página de vendas lowticket do produto **Planilha Inteligente de Precificação™**.

- **URL final:** `https://lp.p4gestao.com.br/pip/`
- **Subdomínio:** `lp.p4gestao.com.br` (reservado para landing pages — o domínio raiz `p4gestao.com.br` fica livre para uso institucional)
- **Checkout:** `https://payfast.greenn.com.br/4uus7j2` (Greenn/Payfast)
- **Preço:** R$ 67 à vista ou 8x de R$ 9,70
- **Meta Pixel:** `3103391829973250` (já instalado)
- **Microsoft Clarity:** `sn3gbc8rkb` (já instalado)

## Estrutura do repositório

```
repositorio/                        ← raiz do repo no GitHub
├── CNAME                            (lp.p4gestao.com.br)
├── .nojekyll
├── README.md
├── robots.txt
├── sitemap.xml
└── pip/                             ← subpasta servida em /pip/
    ├── index.html
    ├── favicon.ico
    ├── favicon-{16,32,48}x{16,32,48}.png
    ├── apple-touch-icon.png
    ├── android-chrome-{192,512}.png
    ├── og-image.jpg
    ├── site.webmanifest
    └── assets/
        ├── conversa-seria.jpg
        ├── empresario-preocupado.jpg
        ├── lucro-verdade.png
        ├── mockup-oferta.png
        ├── solucao-planilha.png
        └── wesley.jpg
```

## DNS no Cloudflare

| Type | Name | Target | Proxy status |
|------|------|--------|--------------|
| CNAME | lp | `SEU-USUARIO.github.io` | DNS only (nuvem cinza) |

**IMPORTANTE:** mantenha a nuvem **cinza** (DNS only) na configuração inicial. Após o GitHub Pages emitir o certificado HTTPS automaticamente (até 24h), você pode ativar a nuvem laranja (Proxied) se quiser as features de CDN/segurança do Cloudflare — mas precisa configurar SSL como "Full" ou "Full (strict)" para evitar loops de redirecionamento.

## GitHub Pages

- Settings → Pages → Source: branch `main` / pasta `/ (root)`
- Custom domain: `lp.p4gestao.com.br` (preenchido automaticamente pelo arquivo CNAME)
- Enforce HTTPS: marque após GitHub emitir o certificado

## Tracking instalado

- **Meta Pixel** (`3103391829973250`) — dispara `PageView` automaticamente
- **Microsoft Clarity** (`sn3gbc8rkb`) — grava sessões e gera heatmap
- **API de Conversões da Meta** — configurada **no painel da Greenn**, não na página

## Edições rápidas no `pip/index.html`

- **Preço**: procure por `8x de R$ 9,70` e `R$ 67 à vista` (aparece em 2 ofertas)
- **Link do checkout**: procure por `payfast.greenn.com.br/4uus7j2` (3 botões)
- **Depoimentos**: bloco `<!-- DEPOIMENTOS -->`, edite os 4 cards
- **FAQ**: bloco `<!-- FAQ -->`, cada `<details>` é uma pergunta
- **Cores**: variáveis CSS no `:root` no topo do `<style>`
- **URL canônica**: aparece em 5 lugares (canonical, og:url, og:image, twitter:image, JSON-LD)
