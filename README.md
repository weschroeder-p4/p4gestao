# Planilha Inteligente de Precificação — Landing Page

Página de vendas lowticket do produto **Planilha Inteligente de Precificação™**.

- **Domínio:** `p4gestao.com.br`
- **Checkout:** `https://payfast.greenn.com.br/4uus7j2` (Greenn/Payfast)
- **Preço:** R$ 67 à vista ou 8x de R$ 9,70
- **Meta Pixel:** `3103391829973250` (já instalado)
- **Microsoft Clarity:** `sn3gbc8rkb` (já instalado)

## Como publicar no GitHub Pages com o domínio p4gestao.com.br

### 1. Criar o repositório no GitHub

1. Acesse [github.com/new](https://github.com/new)
2. Nomeie como `p4gestao` (ou outro nome de sua escolha) e marque como **Public**
3. Crie **sem** README/`.gitignore` (já temos os arquivos)

### 2. Subir os arquivos

Faça upload de **todo o conteúdo desta pasta `site/`** (não a pasta em si — os arquivos de dentro):

```
index.html
CNAME
.nojekyll
robots.txt
sitemap.xml
site.webmanifest
favicon.ico
favicon-16x16.png
favicon-32x32.png
favicon-48x48.png
apple-touch-icon.png
android-chrome-192x192.png
android-chrome-512x512.png
og-image.jpg
README.md
assets/  (pasta inteira, com todas as imagens)
```

Pelo navegador: no repositório, clique em **Add file → Upload files**, arraste tudo, e faça **Commit changes**.

### 3. Ativar o GitHub Pages

1. No repositório, vá em **Settings → Pages**
2. Em **Source**, escolha a branch `main` e a pasta `/ (root)`
3. Clique em **Save**
4. Em 1-2 minutos a página estará no ar em `https://SEU-USUARIO.github.io/p4gestao/`

### 4. Configurar o domínio próprio `p4gestao.com.br`

**No GitHub:**

1. Em **Settings → Pages → Custom domain**, digite `p4gestao.com.br` e clique em **Save**
2. Aguarde a verificação do DNS (pode levar de 10 minutos a algumas horas)
3. Marque **Enforce HTTPS** assim que a opção ficar disponível

**No Registro.br (ou onde o domínio está registrado):**

Você quer usar o **domínio raiz** (`p4gestao.com.br`), então adicione 4 registros do tipo **A** apontando o host `@` (ou deixe o campo vazio, dependendo do painel) para os IPs do GitHub Pages:

| Tipo | Nome | Valor |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

Opcional — adicione também os registros **AAAA** para IPv6:

| Tipo | Nome | Valor |
|------|------|-------|
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |

**Bônus — para que `www.p4gestao.com.br` também funcione**, adicione um registro CNAME:

| Tipo | Nome | Valor |
|------|------|-------|
| CNAME | www | SEU-USUARIO.github.io |

(substitua `SEU-USUARIO` pelo seu nome de usuário do GitHub).

A propagação DNS pode levar de 10 minutos a algumas horas. Para acompanhar, use [dnschecker.org](https://dnschecker.org).

## Estrutura de arquivos

```
site/
├── index.html                          # página principal
├── CNAME                                # p4gestao.com.br
├── .nojekyll                            # não processar com Jekyll
├── robots.txt                           # diretivas para buscadores
├── sitemap.xml                          # mapa do site
├── site.webmanifest                     # PWA manifest
├── favicon.ico                          # favicon multi-resolução
├── favicon-{16,32,48}x{16,32,48}.png    # favicons modernos
├── apple-touch-icon.png                 # iOS home screen
├── android-chrome-{192,512}.png         # Android/PWA
├── og-image.jpg                         # preview WhatsApp/Facebook
├── README.md                            # este arquivo
└── assets/
    ├── empresario-preocupado.jpg
    ├── solucao-planilha.png
    ├── mockup-oferta.png
    ├── conversa-seria.jpg
    ├── wesley.jpg
    └── lucro-verdade.png
```

## Tracking instalado

- **Meta Pixel** (ID `3103391829973250`) — dispara `PageView` automaticamente em cada visita
- **Microsoft Clarity** (ID `sn3gbc8rkb`) — grava sessões e gera heatmap
- **API de Conversões da Meta** — configurada **no painel da Greenn**, não na página (evento `Purchase` enviado server-side direto pela Greenn)

## Edições rápidas (no `index.html`)

- **Preço**: procure por `8x de R$ 9,70` e `R$ 67 à vista` (aparece em 2 ofertas)
- **Link do checkout**: procure por `payfast.greenn.com.br/4uus7j2` (3 botões)
- **Depoimentos**: bloco `<!-- DEPOIMENTOS -->`, edite os 4 cards
- **FAQ**: bloco `<!-- FAQ -->`, cada `<details>` é uma pergunta
- **Cores**: variáveis CSS no `:root` no topo do `<style>`
