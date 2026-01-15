# 📊 Análise de Dados – Cancelamento de Clientes (Churn)

Este projeto tem como objetivo realizar uma **análise exploratória de dados (EDA)** para entender os principais fatores relacionados ao **cancelamento de clientes**, utilizando Python e bibliotecas voltadas para análise e visualização de dados.

O estudo percorre desde a importação e limpeza da base até a aplicação de filtros e análise de padrões relevantes.

---

## 🎯 Objetivo do Projeto

- Analisar o comportamento de clientes cancelados
- Identificar padrões e variáveis relevantes para o churn
- Realizar tratamento e limpeza da base de dados
- Gerar insights por meio de visualizações
- Demonstrar habilidades em **Análise de Dados e EDA**

---

## 🧰 Tecnologias Utilizadas

- **Python**
- **Pandas** – Manipulação e tratamento de dados
- **Plotly Express** – Visualização de dados interativa
- **Jupyter Notebook** – Ambiente de análise

---

Isso garante:
- Syntax highlight correto
- Leitura profissional
- Boa visualização para recrutadores

---

## 📄 README.md (com código Python corretamente formatado)

```markdown
# 📊 Análise de Dados – Cancelamento de Clientes (Churn)

Este projeto realiza uma **Análise Exploratória de Dados (EDA)** com foco em **cancelamento de clientes (churn)**, utilizando Python e bibliotecas de análise e visualização de dados.

---

## 🧰 Tecnologias Utilizadas

- Python
- Pandas
- Plotly Express
- Jupyter Notebook

---

## 🧠 Etapas da Análise e Código

### 1️⃣ Importação das bibliotecas e base de dados

```python
import pandas as pd
import plotly.express as px

tabela = pd.read_csv("cancelamentos.csv")
display(tabela)

tabela = tabela.drop(columns="CustomerID")
display(tabela)

condicao = tabela["duracao_contrato"] != "Monthly"
tabela = tabela[condicao]
condicao = tabela["ligacoes_callcenter"] <= 4
tabela = tabela[condicao]
px.histogram(
    tabela,
    x="cancelou",
    color="duracao_contrato",
    title="Cancelamento de clientes por tipo de contrato"
)
```

📊 Estrutura da Base de Dados
Coluna	Descrição
cancelou	Indica se o cliente cancelou
duracao_contrato	Tipo de contrato
ligacoes_callcenter	Quantidade de ligações
dias_atraso	Dias de atraso
⚠️ Observações

Projeto com foco educacional e de portfólio

A análise pode ser expandida para modelos preditivos

A qualidade dos dados impacta diretamente os resultados

👨‍💻 Autor

Jorge Ferreira
Analista de Dados | Python | Análise de Dados



