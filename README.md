# 🌡️ Clima nas maiores economias do Brasil — Dashboard Power BI

Dashboard em Power BI que analisa **dados climáticos diários de 2015 a 2025** das **5 capitais com maior PIB** do Brasil (São Paulo, Rio de Janeiro, Brasília, Belo Horizonte e Manaus) e dos **5 estados mais ricos** (SP, RJ, MG, PR e RS), em um ano marcado por um El Niño forte.

🎥 **Demonstração:** veja o vídeo [clima_dashboard_linkedin.mp4](clima_dashboard_linkedin.mp4)

## 📊 Páginas

| Página | O que mostra |
|---|---|
| **Visão Geral** | KPIs, mapa dos 27 pontos analisados, temperatura média por ano e matriz de anomalia térmica (mês × ano) |
| **Capitais** | Série mensal de temperatura, chuva média anual, ciclo sazonal e ranking das capitais |
| **Estados** | Temperatura por estação do ano, comparação capital × interior e evolução anual por estado |
| **Extremos** | Dias de calor (≥30°C) e dias frios (≤10°C) por ano, Top 10 dias mais quentes e chuvas mais intensas |

## 🔎 Principais achados

- **2024** foi o ano mais quente da série.
- O El Niño de 2023-24 aparece claramente na matriz de anomalias, com meses até **+1,8°C** acima da média.
- Maior máxima registrada: **43,9°C** em Governador Valadares (MG), em novembro de 2023.
- **Manaus** é a capital mais quente (27,5°C de média) e a mais chuvosa (~1.900 mm/ano).

## 🛠️ Como foi feito

- **Fonte de dados:** API da [NASA POWER](https://power.larc.nasa.gov/) (reanálise MERRA-2), consumida diretamente via **Power Query**
- **Seleção por PIB:** IBGE — PIB dos Municípios e Contas Regionais 2023
- **Modelagem:** esquema estrela — `fClima` (fato diário) + `dCidade` e `dCalendario` (dimensões)
- **DAX:** anomalia térmica, variação ano a ano, dias de calor/frio por ano, chuva média anual, Top N
- **Design:** layout no estilo Figma com fundos de página customizados, tema JSON próprio e navegação por botões

## 📁 Arquivos

- `Clima Brasil.pbix` — relatório do Power BI
- `clima_dashboard_linkedin.mp4` — vídeo de demonstração

## ▶️ Como abrir

1. Baixe o arquivo `Clima Brasil.pbix`
2. Abra no [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (gratuito)
3. Para atualizar os dados, clique em **Atualizar** e escolha acesso **Anônimo** à API da NASA POWER

---

📬 Projeto de portfólio — conecte-se comigo no LinkedIn!
