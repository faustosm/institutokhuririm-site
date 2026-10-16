# Instituto Khuririm · site institucional

Código do site [institutokhuririm.com.br](https://institutokhuririm.com.br): one-page estático em HTML, CSS e JavaScript puro, sem etapa de build, em português, inglês (`/en/`) e espanhol (`/es/`).

## Estrutura

```
instituto-khuririm-site/   # tudo o que vai ao ar
  index.html               # versão em português (padrão)
  en/index.html            # versão em inglês
  es/index.html            # versão em espanhol
  404.html                 # página de erro
  assets/css/style.css     # estilos (cores como variáveis no topo)
  assets/js/main.js        # menu do celular, copiar PIX, animações
  assets/img/              # fotos em WebP (1200 px e 600 px)
  _headers                 # cabeçalhos de segurança e cache
  sitemap.xml, robots.txt
src/worker.js              # redireciona http:// e www. para https://institutokhuririm.com.br
wrangler.jsonc             # configuração do Cloudflare Workers
```

## Rodar localmente

```bash
cd instituto-khuririm-site
python3 -m http.server 8080   # abrir http://localhost:8080
```

## Publicação

Hospedado no Cloudflare Workers com assets estáticos:

```bash
npx wrangler deploy
```
