# Mapa Interativo — Base Produtiva Rural da Bacia do Rio Doce

Mapa interativo (Leaflet) com indicadores da base produtiva rural dos municípios da bacia do rio Doce, desenvolvido como parte do estudo sobre os impactos do rompimento da barragem do Fundão (Mariana, MG).

## 🔗 Acesso

**[Abrir o mapa](https://liviomiguelds.github.io/projeto-recuperacao-rural-rio-doce/)**

> Substitua o link acima pela URL do GitHub Pages depois de publicar.

## O que o mapa mostra

**Fundo (seletor de rádio, 1 por vez):**
- % de ocupados na agropecuária
- % população rural
- % VAB agropecuário/PIB (2021)
- Valor da Produção Animal (per capita)
- Valor da Produção Vegetal (per capita)
- Valor da Produção Silvicultura (per capita)

**Produtos (checkboxes, qualquer combinação):** Bovino, Suíno, Galináceos, Café, Milho, Feijão, Cana-de-açúcar, Outros (vegetal) e Silvicultura — tamanho e opacidade das bolinhas refletem o Quociente Locacional (QL) de cada município em relação à média da bacia.

**Outros elementos:**
- Calha do Rio Doce e limites de macrorregião (Alto/Médio/Baixo Rio Doce) em destaque
- Busca por nome de município
- Tooltip (passar o mouse) com o detalhamento completo por município

## Fontes dos dados

Elaboração própria, com base em dados do IBGE:
- Censo Demográfico (2022)
- Pesquisa da Pecuária Municipal – PPM (2024)
- Produção Agrícola Municipal – PAM (2024)
- Produção da Extração Vegetal e da Silvicultura – PEVS (2024)
- Produto Interno Bruto dos Municípios (2021)

Valores monetários são per capita e deflacionados para R$ de 2025 (IPCA).

## Estrutura dos arquivos

```
index.html                              # o mapa
mapa_interativo_base_produtiva_files/    # dependências (leaflet, leaflet.extras, jquery, bootstrap)
```

Os dois precisam ficar juntos — o HTML **não é autocontido**, ele referencia os arquivos dessa pasta.

## Como atualizar

Este mapa é gerado pelo script `_MAPA_INTERATIVO.R`, parte do projeto de pesquisa sobre a Barragem do Fundão. Para atualizar:

1. Rodar o `_FIGURAS.R` (seção 25 — Base Produtiva Rural) se algum dado de origem mudou.
2. Rodar o `_MAPA_INTERATIVO.R`, que regenera o `.html` e a pasta de dependências aqui mesmo, em `Resultados/25. Base Produtiva Rural/Figuras/`.
3. Dar commit/push nos dois (`.html` + pasta de dependências).
