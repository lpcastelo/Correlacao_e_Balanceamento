# Correlacao_e_Balanceamento
Aqui você irá encontrar a atividade do módulo 17 do curso de Cientista de Dados da Ebac.

A atividade consiste em aplicar técnicas de pré-processamento de dados, preparando a base para etapas mais avançadas de análise e modelagem preditiva.

Durante a atividade serão abordados temas como:

* Análise de correlação entre variáveis
* Balanceamento de classes
* Tratamento de variáveis categóricas
* Transformação e codificação de dados
* Preparação da base para modelos de Machine Learning

O objetivo é melhorar a qualidade e a representatividade dos dados, reduzindo possíveis vieses e garantindo que as variáveis estejam adequadamente preparadas para o treinamento de modelos analíticos e preditivos.

## Contexto

Esta é a **primeira etapa** de um projeto de Credit Score (previsão da pontuação de crédito de clientes), continuado em módulos posteriores do curso — incluindo a aplicação de Árvore de Decisão sobre esta mesma base tratada (ver repositório `Arvore_de_decisao`).

## Dados

Base `CREDIT_SCORE_PROJETO_PARTE1.csv` (164 clientes), com variáveis como idade, renda, escolaridade, estado civil, número de filhos e tipo de moradia. Variável alvo: `Credit Score` (Low/Average/High).

## Etapas realizadas

1. Correção de tipos (conversão de `Income` de texto para numérico) e imputação de `Age` faltante pela mediana.
2. Análise univariada e bivariada (relação entre escolaridade, renda, moradia própria e score de crédito).
3. Codificação de variáveis categóricas: One-Hot Encoding (`Gender`, `Marital Status`, `Home Ownership`) e Label Encoding (`Education`, `Credit Score`).
4. Separação em treino (75%) e teste (25%).
5. Balanceamento das classes de treino com SMOTE, já que `Credit Score` estava fortemente desbalanceada (69% "High", 22% "Average", 9% "Low").

## Resultados

Após o SMOTE, o conjunto de treino passou de 123 registros desbalanceados para 243 registros com exatamente 81 amostras por classe. As bases resultantes (`X_train_balanced.csv`, `y_train_balanced.csv`, `X_test.csv`, `y_test.csv`) foram exportadas para uso na modelagem dos módulos seguintes.

## Tecnologias

- Python, pandas
- scikit-learn (get_dummies, LabelEncoder, train_test_split)
- imbalanced-learn (SMOTE)
- matplotlib, seaborn

## Como executar

1. Instale as dependências: `pip install pandas scikit-learn imbalanced-learn matplotlib seaborn plotly`.
2. Coloque `CREDIT_SCORE_PROJETO_PARTE1.csv` no mesmo diretório do notebook.
3. Execute `Profissao Cientista de Dados M17 Projeto.ipynb` em ordem.
