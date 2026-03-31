# data_fuel_python
Análise de dados do preço da gasolina
# ⛽ Análise Global de Preços de Combustíveis com Python e Machine Learning

Projeto de análise de dados focado na evolução do preço da gasolina em diversos países, com destaque para o **Brasil**, utilizando **Python, Pandas, Matplotlib e Scikit-learn**.

O objetivo é realizar uma análise exploratória, identificar padrões globais, prever tendências do preço da gasolina no Brasil e agrupar países com comportamentos semelhantes.

---

## 📌 Objetivos do projeto

Este projeto tem como foco responder perguntas como:

* Quais países possuem a gasolina mais cara no cenário global?
* Como o preço da gasolina evoluiu ao longo do tempo?
* Como o Brasil se posiciona em relação ao restante do mundo?
* Quais países apresentam comportamento semelhante ao Brasil?
* É possível estimar a tendência do preço da gasolina no Brasil para 2026?
* Existem grupos de países com perfis semelhantes de preço e volatilidade?

---

## 📂 Fonte dos dados

Base utilizada:

**Global Fuel Prices Database**

A base contém séries históricas mensais com preços de combustíveis em diversos países desde **2015**, incluindo:

* gasolina regular
* diesel
* GLP
* querosene
* derivados em moeda local e USD

Neste projeto foi utilizada a aba de **Gasolina em USD por litro**.

---

## 🛠️ Tecnologias utilizadas

* Python 3
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab

---

## 📊 Etapas desenvolvidas

### 1. Limpeza e transformação dos dados

A base original estava em formato Excel com múltiplas abas e estrutura wide.

Foi realizado:

* leitura das abas
* transformação para formato long
* padronização de datas
* tratamento de valores nulos
* filtragem de outliers

---

### 2. Análise exploratória

Foram desenvolvidas análises como:

* ranking dos países com gasolina mais cara
* comparação do Brasil com a média mundial
* evolução histórica do preço por país
* comparação por continentes e potências globais

---

### 3. Conversão do preço do Brasil para Real (R$)

Foi criada uma série histórica do Brasil em **R$/litro**, utilizando câmbio médio anual.

Exemplo:

```python
CAMBIO_ANUAL = {
    2016: 3.484,
    2017: 3.192,
    2018: 3.655,
    2019: 3.945,
    2020: 5.396,
    2021: 5.394,
    2022: 5.165,
    2023: 4.994,
    2024: 5.389,
    2025: 5.592,
}
```

---

### 4. Regressão para previsão do preço no Brasil

Foi aplicada regressão para estimativa de tendência do preço da gasolina no Brasil.

Foram testados:

* regressão linear
* regressão polinomial
* tendência baseada nos últimos 24 meses

A abordagem mais coerente foi a regressão linear recente.

---

### 5. Clusterização de países

Foi utilizado **KMeans Clustering** para agrupar países por comportamento do preço da gasolina.

Features utilizadas:

* preço médio
* volatilidade
* preço mínimo
* preço máximo
* amplitude
* variação percentual total

Clusters identificados:

* países subsidiados
* países intermediários
* países voláteis
* outliers

O Brasil foi classificado no cluster **intermediário**.

---

## 📈 Principais insights

### 🇧🇷 Brasil

O Brasil apresentou comportamento semelhante a países como:

* Chile
* África do Sul
* México
* China
* Canadá
* Japão

Com:

* preço médio relativamente elevado
* volatilidade moderada
* crescimento consistente no período analisado

---

### 🌍 Cenário global

Os países foram agrupados em perfis como:

* **subsidiados / baixo custo**
* **intermediários**
* **voláteis**
* **outliers extremos**

---

## 🚀 Próximos passos

Melhorias futuras:

* dashboard interativo com Plotly / Streamlit
* comparação por continentes
* integração com API de câmbio em tempo real

---

## 📷 Exemplos de análises

* ranking de países
* clusterização
* séries temporais
* previsão do Brasil até 2026

---

## 👨‍💻 Autor

Projeto desenvolvido por Anderson Lemos para estudo de **Análise de Dados, Machine Learning e visualização de séries temporais**.
