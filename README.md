# challenge3
Challenge 3 - Alura Oracle One


O propósito da análise realizada, destacando o objetivo principal: prever o churn de clientes com base em variáveis relevantes.

Estrutura do projeto e organização dos arquivos, como o notebook principal, os dados tratados em CSV e qualquer pasta de visualizações.

Descrição do processo de preparação dos dados, incluindo:

Classificação das variáveis em categóricas e numéricas.

Etapas de normalização ou codificação.

Separação dos dados em conjuntos de treino e teste.

Justificativas para as escolhas feitas durante a modelagem.

Exemplos de gráficos e insights obtidos durante a análise exploratória de dados (EDA).

Instruções para executar o notebook, incluindo quais bibliotecas precisam ser instaladas e como carregar os dados tratados.

Perfeito, Wally 👌
Aqui está a separação dos **passos em blocos**, já estruturada para você visualizar o fluxo completo:

---

## **📊 PREPARAÇÃO DOS DADOS**

**1 - Extração do Arquivo Tratado**

* Carregar o dataset já limpo (ex.: `dados_tratados.csv`).

**2 - Remoção de Colunas Irrelevantes**

* Ex.: IDs que não têm impacto na previsão.

**3 - Encoding**

* Transformar variáveis categóricas em numéricas (`OneHotEncoder` ou `get_dummies`).

**4 - Verificação da Proporção de Evasão**

* Analisar a distribuição da variável alvo (`Cancelou`).

**5 - Balanceamento de Classes (opcional)**

* Usar técnicas como **SMOTE** ou **undersampling** se a classe estiver desbalanceada.

**6 - Normalização ou Padronização (se necessário)**

* Ex.: `StandardScaler` para padronizar variáveis numéricas.

---

## **🔎 CORRELAÇÃO E SELEÇÃO DE VARIÁVEIS**

**7 - Análise de Correlação**

* Calcular correlação das features com o target.
* Definir limiar de seleção (ex.: `|r| > 0.1`).

**8 - Análises Direcionadas**

* Selecionar variáveis relevantes com base na análise estatística e no conhecimento de negócio.

---

## **🤖 MODELAGEM PREDITIVA**

**9 - Separação de Dados**

* Dividir em treino e teste (`train_test_split`).

**10 - Criação de Modelos**

* Treinar diferentes algoritmos:

  * Regressão Logística
  * KNN
  * Árvore de Decisão
  * Random Forest

**11 - Avaliação dos Modelos**

* Métricas: **Acurácia, Precisão, Recall, F1-score, Matriz de Confusão**.

---

## **📌 INTERPRETAÇÃO E CONCLUSÕES**

**12 - Análise de Importância das Variáveis**

* Identificar quais features têm maior peso nos modelos (ex.: `feature_importances_` da Random Forest).

**13 - Conclusão Estratégica**

* Relatório final:

  * Destacar **principais fatores que influenciam a evasão**.
  * Comparar desempenho dos modelos.
  * Definir **estratégias de retenção** (ex.: clientes de alto risco recebem ofertas personalizadas, revisão de preços, programas de fidelidade).

---

👉 Quer que eu **compare seu código** com esses 13 passos e marque onde já está coberto e onde faltaria complementar?

