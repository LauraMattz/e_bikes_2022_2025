# 🚲⚡ Boom de Bikes e Patinetes Elétricos no Brasil (2022–2025)

Este repositório apresenta uma análise exploratória e visual das **importações de bicicletas, patinetes e scooters elétricos no Brasil**, com foco no período recente de forte crescimento do mercado.

A análise parte de uma pergunta simples:

> O aumento visível desses veículos nas ruas é apenas percepção ou os dados confirmam um boom?

Os dados mostram que **sim, o boom é real**, especialmente a partir de 2024.

![Mapa das importações de bikes e patinetes elétricos por estado](images/mapa_importacoes_ebikes.png)

---

## 📌 Conteúdo do projeto

* 📊 Análise temporal das importações (2022–2025*)
* 🗺️ Mapas por estado (UF) com:

  * quantidade importada
  * proxy de preço (valor médio por unidade)
* 📈 Comparação entre **São Paulo**, **Rio de Janeiro** e **Brasil**
* 🧠 Interpretação econômica do crescimento, escala e segmentação regional

⚠️ *Os dados de 2025 são parciais.*

---

## 🔎 Fonte dos dados

Os dados utilizados são **públicos e gratuitos**, provenientes de:

* **Comex Stat / MDIC** (Ministério do Desenvolvimento, Indústria, Comércio e Serviços)
* Acesso via API
* Microdados de importação

### NCM analisado

**8711.60.00**

Inclui:

* bicicletas elétricas
* patinetes elétricos
* scooters elétricas
* outros ciclos com motor elétrico

Esse NCM funciona como uma **proxy direta da entrada desses veículos no Brasil**.

---

## 🧪 Metodologia

Toda a análise foi desenvolvida em **Google Colab**, utilizando **Python**, com um pipeline simples e reproduzível:

1. 📥 Download automatizado dos microdados via API
2. 🧹 Limpeza e tratamento dos dados com `pandas`
3. 📊 Agregação por ano e estado (UF)
4. 📐 Cálculo dos principais indicadores:

   * quantidade importada
   * valor total importado (US$ FOB)
   * valor médio por unidade (proxy de preço)
5. 🗺️ Visualizações com `matplotlib` e `geopandas`

---

## 📊 Indicadores analisados

* **Quantidade importada**
* **Valor total importado (US$ FOB)**
* **Proxy de preço** = valor total / quantidade

⚠️ O proxy de preço representa o **valor médio de importação na entrada do país**
(não inclui impostos, frete interno ou margens do varejo).

---

## 🗺️ Interpretação geral dos resultados

* O mercado de mobilidade elétrica leve cresce fortemente a partir de 2024
* O preço médio de importação cai, indicando **entrada em escala**
* Estados líderes em volume não são os mesmos líderes em preço
* Estratégias regionais distintas emergem:

  * alguns estados atuam como hubs logísticos
  * outros concentram produtos mais caros / premium

Esses padrões ajudam a explicar por que bikes e patinetes elétricos se tornaram rapidamente parte do cotidiano urbano.

---

## ⚠️ Limitações

* Dados de 2025 são parciais
* UF de importação ≠ local de uso final
* Proxy de preço não representa preço ao consumidor

Apesar disso, os dados são consistentes para análise de **tendências e padrões estruturais**.

---

## 📁 Estrutura do repositório

```text
├── e_bikes_documentado.ipynb   # Notebook principal (análise completa)
├── data/                       # (opcional) dados brutos ou processados
├── out_frames/                 # (opcional) imagens e mapas gerados
└── README.md                   # Este arquivo
```

---

## ▶️ Como usar

1. Abra o notebook `e_bikes_documentado.ipynb` no **Google Colab** ou localmente
2. Execute as células em ordem
3. Explore os gráficos, mapas e tabelas
4. Ajuste parâmetros (anos, estados, métricas) conforme necessário

---

## 📣 Observação final

Este projeto tem caráter **exploratório e analítico**, usando exclusivamente dados públicos.

Ele pode ser reutilizado ou adaptado para estudos sobre:

* mobilidade urbana
* economia verde
* comércio exterior
* políticas públicas
