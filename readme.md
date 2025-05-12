# Probabilidade e Estatística com R

Um trabalho de análise de qualidade do ar na Índia usando R e R Markdown, desenvolvido como parte da disciplina de Probabilidade e Estatística da UFF.

---

## 📖 Descrição

Este projeto explora dados diários de AQI (Air Quality Index) e medições de poluentes (PM2.5, PM10, NO₂ etc.) - [Air Quality Data in India (Kaggle)](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india) - para responder três perguntas principais:

1. **Quais cidades/estados têm a maior média de AQI** no período completo?  
2. **Quais cidades/estados que iniciaram acima da média geral conseguiram ficar abaixo** dessa média nos dois últimos anos?  
3. **O comportamento das medições de PM2.5 e PM10 é semelhante** em todas as cidades?

Além disso, demonstramos como o dataset atende a requisitos de EDA:
- Gráficos de dispersão (duas variáveis contínuas).  
- Gráficos de barras facetados (três variáveis categóricas).  
- Séries temporais (gráficos de linha).

---

## 📂 Estrutura do Repositório

```text
├── data/
│   ├── stations.csv
│   ├── station_day.csv
│   └── city_day.csv
├── scripts/
│   |── trabalho-prob-estatistica.
|   └── 
