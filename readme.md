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

## Check-list do Trabalho de AQI na Índia

### 1. Leitura e limpeza dos dados
- [x] Ler dados com função `read_...` do **tidyverse** para uma tibble
- [x] Usar `glimpse()` para inspecionar a tibble
- [ ] (Se necessário) Refazer leitura especificando tipos de colunas em `read_...`
- [x] (Se necessário) Aplicar `janitor::clean_names()`
- [x] Usar `summarytools::dfSummary()` para sumário da tibble
- [x] Verificar **NAs** e valores obviamente errados
- [x] (Se necessário) Corrigir valores óbvios na tibble
- [x] (Se necessário) Transformar a tibble para facilitar manipulações:
  - [x] `pivot_wider()` ou `pivot_longer()`
  - [x] Funções do **lubridate** para converter datas/horários
  - [x] Funções do **stringr** + `mutate()` para extrair partes de strings
  - [x] `mutate()` para converter unidades (e.g. µg/m³ para outra escala)

### 2. Análise exploratória (EDA)
- [x] Verificar contagem de valores diferentes em colunas de interesse
- [x] Verificar contagem de **NAs** em colunas de interesse
- [x] Agregar dados com `group_by()` + `summarise()` para estatísticas descritivas
- [x] Formular perguntas (além das 3 principais) e respondê-las via EDA

### 3. Visualização (ggplot2)
#### Requisitos gerais
- [x] Todos os gráficos com **ggplot2**
- [x] Cada gráfico com título, rótulos de eixos, legendas e elementos de interpretação
- [x] Incluir texto comentando conclusões de cada gráfico

#### 3.1 Scatter plots
- [x] Scatter plot(s) entre variáveis contínuas
- [x] Usar cores/formas/tamanhos para adicionar informação
- [x] (Se fizer sentido) transformar escalas (e.g., log)
- [x] Adicionar `geom_smooth()` para reta de regressão

#### 3.2 Histogramas
- [x] Histograma(s) de variáveis contínuas
- [x] (Se fizer sentido) facetar múltiplos histogramas
- [x] (Se fizer sentido) transformar escalas

#### 3.3 Boxplots
- [x] Boxplot(s) de variáveis contínuas
- [x] (Se fizer sentido) boxplots lado a lado
- [x] (Se fizer sentido) transformar escalas

#### 3.4 Barras e colunas
- [x] Gráfico(s) de barra/coluna de variáveis categóricas
- [x] Usar cores de preenchimento para informação adicional
- [x] Experimentar paletas de cores
- [x] (Se fizer sentido) facetar gráficos de barra/coluna
- [ ] (Se fizer sentido) usar proporções em vez de contagens
- [ ] (Se fizer sentido) gráficos stacked
- [x] (Se fizer sentido) gráficos dodged
- [x] (Se fizer sentido) ordenar barras/colunas por valor
- [ ] (Se fizer sentido) transformar escalas

#### 3.5 Gráficos de linha
- [x] Gráfico(s) de linha ao longo do tempo (ou outra variável contínua)
- [x] Se não for possível, explicar por quê
- [ ] (Se fizer sentido) transformar escalas

---

## 📂 Estrutura do Repositório

```text
├── data/
│   ├── stations.csv
│   ├── station_day.csv
│   └── city_day.csv
├── scripts/
│   |── trabalho-probabilidade-e-estatistica-com-R---outra-versao.Rmd
|   └── trabalho-probabilidade-e-estatistica-com-R---outra-versao.html
