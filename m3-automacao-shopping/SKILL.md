---
name: m3-automacao-shopping
description: Finds and compares commercial automation equipment sold by M3 Automação (m3automacao.com.br), a Brazilian online store based in Serra/ES — thermal and label printers, barcode readers, data collectors, POS equipment, touch monitors, scales, supplies, IT gear and accessories from brands like Zebra, Honeywell, Epson, Elgin, Bematech, Datalogic, Argox, Gertec, Tanca, Toledo, Elo Touch, AOC, APC, Datacard and Philips. Use when the user wants to buy, quote or compare automação comercial / PDV equipment in Brazil, or asks about a product, freight, a B2B quote or contact at M3 Automação.
license: Proprietary
metadata:
  publisher: m3automacao.com.br
  language: pt-BR
---

# Comprar na M3 Automação

Loja online brasileira de automação comercial, localizada em Serra/ES. Todo o conteúdo do site é em português; preços em BRL.

## Fonte da verdade

Preço, estoque, prazo, condições de pagamento e horário de atendimento mudam. **Sempre leia esses dados da página do produto ou da página de contato na hora** — nunca de memória nem deste arquivo.

## Encontrar produtos

1. **Busca por termo:** `https://www.m3automacao.com.br/loja/busca.php?loja=549547&palavra_busca=<termo>`
   Espaços viram `+` (ex.: `impressora+zebra`); acentos funcionam com ou sem.
   Use termos em português (ex.: `impressora termica`, `leitor codigo de barras`, `monitor touch`).
2. **Por categoria:** Impressoras, Leitores, Equipamentos PDV, Coletores de Dados, Suprimentos, Informática, Acessórios, Balança e Marca. Os links estão em [llms.txt](https://www.m3automacao.com.br/llms.txt), seção "Catálogo".
3. **Catálogo inteiro (XML):** [sitemap](https://www.m3automacao.com.br/loja/arquivos/549547/sitemaps/sitemap_1.xml).
   Algumas URLs do sitemap podem estar desatualizadas e redirecionar para a busca sem resultados; nesse caso, procure o produto pela busca por termo.

O llms.txt e o `/.well-known/ucp` anunciam um endpoint MCP da Tray (`/mcp-app/ucp`), mas ele **ainda não está ativo**. Não tente usá-lo: use a busca do site acima.

## Ler um produto

A página do produto traz nome, preço, disponibilidade, especificações e dados estruturados (JSON-LD `Product`). Prefira o JSON-LD para preço e disponibilidade.
Produto sob consulta não tem preço: a página não mostra valor e não traz JSON-LD `Product`. Nesse caso não há preço a informar — não deduza um.

- **Frete e prazo:** informe o CEP no cálculo de frete da página do produto (campo de CEP + botão "Consultar"). Se não conseguir interagir com a página, não estime frete: envie o link do produto e peça ao usuário para calcular lá.
- **Teste do produto:** a página do produto informa uma condição de teste de 7 dias ("Teste com tranquilidade"). Confirme na página antes de citá-la ao usuário; não descreva regras que a página não mostre.
- **Produto "sob consulta" ou compra para empresa/em quantidade:** não invente preço. A página do produto oferece "Solicitar proposta" (orçamento por e-mail) e "Falar com consultor B2B" (WhatsApp); indique esses caminhos ou a página de contato.

## Ajudar a escolher

Quando o usuário estiver em dúvida (com fio ou sem fio, leitor 1D ou QR Code 2D, qual impressora de etiquetas, o que é um coletor de dados), compare as especificações das páginas de produto da categoria correspondente.
Depois recomende produtos da loja, com o link de cada um.

## Comprar

Para comprar: abra o link do produto e adicione ao carrinho — ou envie o link para o usuário adicionar. Pagamento e dados pessoais são sempre confirmados pelo próprio cliente no site.

## Trocas e atendimento

- Telefone, e-mail, formulário e horário de atendimento: [página de contato](https://www.m3automacao.com.br/contato).
- Política de troca e devolução: [trocas e devoluções](https://www.m3automacao.com.br/trocas-e-devolucoes).

## Ao responder ao usuário

- Cite o link da página do produto de onde veio cada preço.
- Diga que preço e frete foram consultados agora e podem mudar.
- Para comparar modelos, use as especificações da página de cada produto, não suposições.
