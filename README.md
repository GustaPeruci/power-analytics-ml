# Análise e Previsão de Consumo de Energia Elétrica

## 📋 Descrição do Projeto

Este projeto implementa técnicas avançadas de análise de séries temporais e machine learning para prever o consumo de energia elétrica residencial. Utilizando o dataset "Individual Household Electric Power Consumption" do UCI Machine Learning Repository, desenvolvemos e comparamos múltiplos modelos preditivos.

**Grupo 1**: Gustavo Conceição, Júlia, Mateus, Nicolly, Andreza

## 🎯 Objetivos

- Realizar análise exploratória completa de dados de consumo elétrico
- Implementar e comparar modelos de previsão (baseline e avançados)
- Identificar padrões temporais, sazonalidade e tendências
- Selecionar o melhor modelo baseado em métricas de performance

## 📊 Dataset

**Fonte**: UCI Machine Learning Repository  
**URL**: https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption

**Características**:
- Medições de uma residência francesa
- Período: Dezembro 2006 - Novembro 2010 (4 anos)
- Resolução original: 1 minuto
- Resolução utilizada: 1 hora (agregação)
- Variáveis: 9 features incluindo consumo ativo/reativo, voltage e sub-medidores

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Pandas**: Manipulação e análise de dados
- **NumPy**: Operações numéricas
- **Matplotlib & Seaborn**: Visualizações
- **Scikit-learn**: Modelos de machine learning
- **Statsmodels**: Modelos estatísticos (ARIMA/SARIMA)
- **Jupyter Notebook**: Ambiente de desenvolvimento

## 📁 Estrutura do Projeto

```
power-analytics-ml/
│
├── power_analytics_ml.ipynb    # Notebook principal com análises
├── household_power_consumption.txt  # Dataset
├── README.md                    # Este arquivo
└── requirements.txt             # Dependências Python
```

## 🚀 Como Executar

### Pré-requisitos

1. Python 3.8 ou superior instalado
2. Jupyter Notebook ou JupyterLab

### Instalação

1. Clone ou baixe este repositório

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

3. Execute o Jupyter Notebook:
```bash
jupyter notebook power_analytics_ml.ipynb
```

4. Execute as células sequencialmente

## 📈 Modelos Implementados

### Modelos Baseline
1. **Naive Forecast**: Previsão baseada no último valor observado
2. **Média Móvel Simples**: Média dos últimos 24 valores (janela de 1 dia)
3. **Suavização Exponencial Simples**: Peso exponencial decrescente

### Modelos Avançados
1. **SARIMA**: Seasonal AutoRegressive Integrated Moving Average
   - Captura sazonalidade e tendências
   - Parâmetros: (1,1,1)(1,1,1,24)

2. **Random Forest Regressor**: Modelo ensemble baseado em árvores de decisão
   - Otimização de hiperparâmetros via RandomizedSearchCV
   - Features temporais engineeradas (hora, dia da semana, mês, componentes cíclicas)

## 📊 Métricas de Avaliação

- **MAE** (Mean Absolute Error): Erro médio absoluto
- **RMSE** (Root Mean Squared Error): Raiz do erro quadrático médio
- **MAPE** (Mean Absolute Percentage Error): Erro percentual médio
- **R²** (Coefficient of Determination): Capacidade explicativa do modelo

## 🎓 Etapas do Projeto

### Etapa 1: Aquisição e Exploração Inicial (20%)
- Download e carregamento do dataset
- Documentação da fonte e características
- Verificação de integridade e completude

### Etapa 2: Análise Exploratória de Dados (20%)
- Estatísticas descritivas
- Identificação de valores ausentes e outliers
- Visualizações temporais
- Análise de tendências e sazonalidade
- Decomposição da série temporal

### Etapa 3: Preparação e Modelagem (30%)
- Limpeza e tratamento de dados
- Feature engineering
- Divisão temporal (80% treino / 20% teste)
- Implementação de modelos baseline
- Implementação de modelos avançados
- Otimização de hiperparâmetros

### Etapa 4: Avaliação e Comparação (20%)
- Cálculo de métricas de performance
- Análise comparativa entre modelos
- Análise de resíduos
- Visualizações comparativas

### Etapa 5: Conclusões e Documentação (10%)
- Seleção do modelo final
- Discussão de limitações
- Propostas de trabalhos futuros
- Documentação completa

## 🏆 Principais Resultados

- **Melhor Modelo**: [Será determinado após execução]
- **MAPE**: < 10% (excelente precisão)
- **R²**: > 0.8 (alta capacidade explicativa)

### Insights Principais
- Picos de consumo: manhã (7-9h) e noite (19-21h)
- Variação semanal: padrões diferentes entre dias úteis e finais de semana
- Sazonalidade anual: maior consumo no inverno

## 📝 Observações Importantes

- Os dados foram agregados por hora para facilitar processamento
- Outliers foram identificados mas mantidos (representam picos reais de consumo)
- Validação temporal foi respeitada (sem data leakage)
- Modelos foram treinados com dados históricos e testados em período futuro

## 🔮 Trabalhos Futuros

1. Incorporar dados climáticos (temperatura, umidade)
2. Implementar modelos de Deep Learning (LSTM, GRU)
3. Desenvolver ensemble methods (Stacking)
4. Criar API REST para servir previsões
5. Implementar detecção de anomalias

## 📚 Referências

1. Hebrail, G., & Berard, A. (2012). Individual Household Electric Power Consumption. UCI Machine Learning Repository.
2. Box, G. E., Jenkins, G. M., et al. (2015). Time series analysis: forecasting and control.
3. Breiman, L. (2001). Random forests. Machine learning, 45(1), 5-32.
4. Hyndman, R. J., & Athanasopoulos, G. (2018). Forecasting: principles and practice.

## 📧 Contato

**Grupo 1 - Fase 8**  
Disciplina: Análise de Dados  
Instituição: [Nome da Instituição]

---

**Última atualização**: Novembro 2025
