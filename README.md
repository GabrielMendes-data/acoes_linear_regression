# 📈 Previsão de Preços de Ações

Projeto de Machine Learning e análise exploratória usando dados públicos de mercado financeiro e indicadores econômicos.  
O objetivo é prever o preço das ações da **JBS**, **Marfrig** e **BRF** (primeiro dia útil do mês) e analisar a relação com o dólar, IBOV, IPCA, exportação de carnes e saldo da balança comercial.

---

## 🎯 Objetivo

- Aplicar **modelos de regressão linear** para prever o preço de fechamento das ações (JBS, Marfrig, BRF) com base em indicadores econômicos brasileiros.
- Analisar a influência de cada variável preditora nos preços das empresas do setor.

---

## 📁 Dados utilizados

- **Yahoo Finance:** Preço de fechamento mensal das ações (JBS, Marfrig, BRF), dólar (USDBRL), IBOVESPA.
- **Banco Central do Brasil:** IPCA mensal.
- **Balança Comercial:** Exportação total e de carnes (planilhas Excel).
- **Período:** jan/2010 a dez/2024, dados mensais.

Principais variáveis:
- `close_jbs`, `close_marfrig`, `close_brf`: Preços das ações.
- `close_dolar`, `close_ibov`: Dólar e Ibovespa.
- `value_ipca`: IPCA mensal.
- `saldo_balanca_com`: Saldo da balança comercial.
- `value_exp_carnes`: Valor exportado em carnes.

---

## 📊 Modelos utilizados

- **Regressão Linear Simples:** Uma variável por vez.
- **Regressão Linear Múltipla:** Combinação de 2 a 4 variáveis explicativas para cada empresa.
- **Avaliação com split único** (25% para teste, mesmo índice para todos os alvos).

---

## 🏆 Resultados (exemplo)

| Empresa   | Variáveis                        | R² treino | R² teste | EMA  | EQM   |
|-----------|----------------------------------|-----------|----------|------|-------|
| JBS       | Dólar, IBOV, IPCA                | 81.0%     | 72.5%    | 2.10 | 6.30  |
| Marfrig   | Dólar, IBOV, Balança Comercial   | 80.5%     | 70.3%    | 1.92 | 5.85  |
| BRF       | Dólar, Exportação Carnes         | 76.2%     | 65.1%    | 2.25 | 7.10  |

> 🔍 **Insight:** O preço do dólar e do Ibovespa estão entre as variáveis mais influentes nos preços das empresas de proteína animal. Exportação de carnes impacta fortemente a BRF.

---

## 📌 Etapas do projeto

1. **Importação e limpeza** dos dados
2. **Análise exploratória:** gráficos de séries temporais, correlação e dispersão
3. **Modelagem preditiva:** regressão linear simples e múltipla
4. **Avaliação e comparação** dos modelos para cada empresa

---

## 💻 Tecnologias utilizadas

- Python
- Pandas, Numpy
- Matplotlib, Seaborn
- Scikit-learn
- yfinance, requests

---

## 🚀 Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/GabrielMendes-data/acoes_linear_regression.git
   cd acoes_linear_regression
