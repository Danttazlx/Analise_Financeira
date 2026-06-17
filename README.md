# 💳 Crédito em Risco: ETL e Análise de Inadimplência

Análise de dados financeiros de clientes com foco em identificar risco de inadimplência através da taxa de utilização do crédito, usando Python e Pandas.

## 🎯 Sobre o projeto

Este projeto simula uma rotina real de análise de dados financeiros: carregar uma base de clientes, tratar e limpar os dados, criar métricas relevantes para o negócio e responder perguntas estratégicas usando apenas Python.

## ❓ Perguntas respondidas

1. **Qual a taxa de utilização do crédito de cada cliente?**
   Calculada como `gasto_mensal / limite_credito`, permitindo identificar quem está próximo de esgotar o limite disponível.

2. **Quais clientes estão em maior risco?**
   Identificados todos os clientes com taxa de utilização acima de 80%, ordenados do maior risco para o menor.

3. **Qual o perfil dos clientes inadimplentes?**
   Análise de idade média, renda média e concentração geográfica dos clientes com status "Inadimplente".

## 🔍 Principais insights

- **100% dos clientes com taxa de utilização acima de 80%** estavam classificados como "Atrasado" ou "Inadimplente" — nenhum estava "Em dia". Isso sugere que a taxa de utilização pode funcionar como um indicador antecipado de risco.
- Os clientes inadimplentes têm **idade média de 30 anos** e **renda média de R$ 3.150,00**, abaixo da média geral da base.
- A inadimplência está concentrada principalmente em São Paulo.

## 🛠️ Tecnologias utilizadas

- **Python**
- **Pandas** — ETL, tratamento e análise de dados
- **Jupyter Notebook**

## 📂 Estrutura do projeto

```
├── analise_financeira.ipynb              # Notebook com todo o processo de ETL e análise
├── clientes_financeiro.csv               # Dados originais (fictícios)
├── clientes_financeiro_analisado.csv     # Base tratada com taxa de utilização calculada
├── clientes_risco_e_inadimplencia.csv    # Recorte de clientes em risco e/ou inadimplentes
└── README.md
```

## 🔄 Processo (ETL)

**Extract** — Carregamento do CSV com dados de clientes (renda, limite de crédito, gasto mensal, status de pagamento).

**Transform** — Limpeza de dados (verificação de nulos e duplicatas, padronização de texto), criação da coluna de taxa de utilização do crédito, filtragem de clientes em risco e segmentação de inadimplentes.

**Load** — Exportação dos resultados tratados em arquivos CSV prontos para consumo em ferramentas de BI.

## 📊 Próximos passos

- Construção de dashboard interativo no Power BI a partir da base tratada
- Expansão da análise com visualizações em Python (Matplotlib/Seaborn)

---

Projeto desenvolvido como parte da minha transição de carreira para análise de dados, aplicando conhecimentos de Python, Pandas e lógica de programação.
