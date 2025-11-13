📊 Análise de Vendas — Projeto Completo de Limpeza, Exploração e Relatórios

Este projeto realiza uma análise completa de vendas utilizando Python, incluindo pré-processamento dos dados, criação de colunas derivadas, identificação automática da coluna de data, geração de séries temporais, gráficos exploratórios e tabelas de agregação.
O objetivo é fornecer uma base organizada e replicável para análises futuras e dashboards em Power BI.

🚀 Objetivos do Projeto

Limpar e padronizar o dataset de vendas.

Detectar automaticamente a coluna de data, mesmo quando ela vem em formato inconsistente.

Criar colunas derivadas:

Data (apenas data)

Mes_Ano (YYYY-MM)

Total da Venda

Gerar análises essenciais para negócios:

Vendas por produto

Vendas diárias

Vendas mensais

Exportar arquivos organizados em CSV/Excel para uso posterior.

Criar gráficos em Python para exploração inicial.

📁 Estrutura do Projeto
📂 data/
 ├── vendas_original.xlsx
 ├── vendas_limpo.xlsx
 ├── vendas_por_produto.csv
 └── vendas_mensais.csv

📂 src/
 ├── limpeza_e_preprocessamento.ipynb
 └── analises.ipynb

📄 README.md

🔧 Tecnologias Utilizadas

Python 3.10+

Pandas — limpeza e manipulação de dados

Matplotlib / Seaborn — visualização

NumPy — operações auxiliares

OpenPyXL — leitura/escrita de Excel

🧼 Etapas da Limpeza e Preparação
✔️ 1. Carregamento do dataset

Dataset importado diretamente de .xlsx.

✔️ 2. Identificação automática da coluna de data

Um algoritmo tenta múltiplas estratégias:

infer_datetime_format

formatos comuns (%d/%m/%Y, %Y-%m-%d, etc.)

timestamps em segundos e milissegundos

E escolhe automaticamente a coluna mais adequada.

✔️ 3. Criação das colunas derivadas

Data → apenas a data

Mes_Ano → período YYYY-MM

Total → multiplicação de preço × quantidade (se aplicável)

✔️ 4. Tratamento de valores ausentes

Remoção ou preenchimento conforme a necessidade.

📈 Análises Realizadas
1. Vendas por Produto

Agrupamento da soma de vendas por item, ordenando do mais vendido para o menos vendido.

2. Séries Temporais

Vendas por dia

Vendas por mês

Tendência mensal

3. Gráficos Explorativos

Inclui:

Vendas por produto

Vendas diárias

📝 Conclusões do Projeto

A automatização da detecção da coluna de data resolveu inconsistências de formatação comuns em bases reais.

A análise mostrou comportamento claro de tendência temporal (picos e sazonalidade).

A criação de colunas derivadas (como Mes_Ano e Total) facilita construções de dashboards no Power BI e modelos de previsão.

A organização em arquivos limpos padroniza o fluxo de dados e permite reutilização em outros relatórios.