# Panificadora Sagres · Belém/PA

Landing single page estática de captação de encomenda da Panificadora Sagres,
R. dos Caripunas, 1717, Batista Campos, Belém/PA.

Não tem carrinho, checkout nem backend. A conversão é o clique que abre o
WhatsApp da Sagres com a mensagem de pedido já montada no padrão que eles usam.

## Arquivos publicados

```
index.html   landing completa: CSS crítico inline, cardápio, formulário, JSON-LD
style.css    CSS não crítico (abaixo da dobra)
robots.txt   libera buscadores e motores de resposta de IA
llms.txt     resumo do negócio e cardápio inteiro em texto puro, para IA
img/         logo, foto de produto, fachada e QR de avaliação
.cpanel.yml  deploy do cPanel Git Version Control
```

Copy, cardápio de origem e decisões de projeto ficam fora do repo (ver `.gitignore`).

## Deploy

cPanel Git Version Control puxa deste repo por HTTPS. SSH desligado, sem push direto.

1. `git push` na branch `main`
2. No cPanel: **Update from Remote** e depois **Deploy HEAD Commit**

Versão nova é bump do `DEPLOYPATH` no `.cpanel.yml`. Publicar uma versão não a coloca
no ar: o redirect da rota de tráfego é uma decisão separada.

## Dados estruturados

Três blocos JSON-LD: `Bakery` no head, `Menu` com os 113 itens e `FAQPage`, os dois
últimos no fim do body. O `Menu` é gerado por script a partir da fonte do cardápio.
Não editar à mão.

Bravo Holding · ewertton.bravo@gmail.com
