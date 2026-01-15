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

1️⃣ Importação da base de dados

Nesta etapa, a base de dados é carregada utilizando Pandas.

import pandas as pd
import plotly.express as px

tabela = pd.read_csv("cancelamentos.csv")
display(tabela)


pd.read_csv() importa a base de dados

display() permite uma visualização inicial do dataset

2️⃣ Visualização inicial e remoção de colunas irrelevantes

Após a importação, é realizada uma avaliação das colunas disponíveis, removendo informações que não agregam valor à análise.

tabela = tabela.drop(columns="CustomerID")
display(tabela)


A coluna CustomerID é removida por não contribuir para a análise de churn

Reduz ruído e melhora a clareza do dataset

3️⃣ Identificação e correção de problemas na base de dados

Nesta fase, são analisados possíveis problemas como:

Valores inconsistentes

Dados nulos

Tipos de dados incorretos

# Identificar possíveis erros da base de dados


Essa etapa é fundamental para garantir a qualidade da análise.

4️⃣ Aplicação de filtros na base de dados

A análise foca em perfis específicos de clientes, aplicando filtros relevantes.

🔹 Filtro 1: Tipo de contrato
condicao = tabela["duracao_contrato"] != "Monthly"
tabela = tabela[condicao]


Remove contratos mensais

Mantém apenas contratos com maior prazo

🔹 Filtro 2: Número de ligações para o call center
condicao = tabela["ligacoes_callcenter"] <= 4
tabela = tabela[condicao]


Mantém clientes com até 4 ligações

Ajuda a identificar padrões de comportamento menos críticos

🔹 Filtro 3: Dias de atraso
# Dias de atraso menor ou igual


Reduz distorções causadas por clientes com alto índice de inadimplência

Permite análises mais equilibradas

5️⃣ Análise exploratória e visualização dos dados

Após o tratamento e filtragem, são criadas visualizações para identificar padrões e tendências.

px.histogram(tabela, x="cancelou", color="duracao_contrato")


Uso de gráficos interativos

Comparação entre clientes cancelados e ativos

Identificação de variáveis com maior impacto no churn

📊 Principais Insights (Exemplo)

Clientes com maior número de ligações ao call center tendem a cancelar mais

Contratos mensais apresentam maior taxa de churn

Atrasos recorrentes estão associados ao cancelamento

(Os insights podem variar conforme a análise final)

⚠️ Observações Importantes

Projeto desenvolvido para fins educacionais e demonstrativos

A análise pode ser expandida com modelos preditivos

A qualidade dos dados impacta diretamente os resultados

📈 Possíveis Evoluções do Projeto

Criação de modelo preditivo de churn

Aplicação de Machine Learning

Feature engineering

Análise de correlação

Dashboard interativo

Deploy do projeto

👨‍💻 Autor

Jorge Ferreira
Analista de Dados | Python | Análise de Dados | BI

Projeto desenvolvido para estudo, prática e composição de portfólio profissional.





