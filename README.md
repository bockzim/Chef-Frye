# Chef Frye · Página de vendas (receitas para air fryer)

Página de vendas estática, pensada primeiro para celular, feita com HTML + Tailwind CSS + JavaScript puro. Não precisa de instalação: abra o `index.html` no navegador.

## Estrutura

```
chef-frye/
├── index.html                 Estrutura da página (seções e textos fixos)
├── README.md
└── assets/
    ├── css/styles.css         Cores do tema, modo escuro e ajustes finos
    ├── js/
    │   ├── config.js          ← EDITE AQUI: checkout, nome, e-mail de suporte, tempo da promoção
    │   ├── data.js            Conteúdo: bônus, depoimentos, perguntas (FAQ), fotos das receitas
    │   ├── main.js            Monta as seções, cronômetro, curtidas/comentários, botão fixo
    │   └── tailwind.config.js Cores e animações do Tailwind
    └── img/                   hero, showcase, receitas/, bonus/, depoimentos/
```

## O que editar

| Quero mudar… | Onde |
|---|---|
| Links de pagamento dos 2 planos | `assets/js/config.js` → `CHECKOUT` |
| Nome do projeto (rodapé) | `assets/js/config.js` → `BRAND` |
| E-mail do botão "Suporte" | `assets/js/config.js` → `SUPPORT_EMAIL` |
| Tempo do cronômetro | `assets/js/config.js` → `PROMO_MINUTES` |
| Bônus, preços dos bônus, depoimentos, FAQ | `assets/js/data.js` |
| Textos do topo, preços dos planos, garantia | `index.html` |
| Cores da marca | `assets/css/styles.css` (variáveis `--heat`, `--gold`, `--leaf`...) |
| Trocar uma foto | Substitua o arquivo em `assets/img/` mantendo o nome |

## Publicar

Envie a pasta inteira para qualquer hospedagem estática (Netlify, Vercel, Cloudflare Pages, Hostinger...). Para testar localmente: `python3 -m http.server` dentro da pasta.

## Observações

- O Tailwind é carregado pelo CDN, o que dispensa instalação. Para produção, o ideal é gerar o CSS com o Tailwind CLI (mais leve e rápido). Dá para fazer essa troca depois.
- O cronômetro fica salvo no aparelho de cada visitante (`localStorage`) e não reinicia ao atualizar a página.
- Rastreamento (pixel/analytics) ainda não está incluso.
