# challenge3
Challenge 3 - Alura Oracle One

# **📌 Desafio — Previsão de Churn**

## **🎯 Propósito da Análise**

O objetivo principal deste projeto é **prever a evasão de clientes (churn)** em uma empresa de serviços, utilizando dados históricos de clientes.
A análise buscou:

* Identificar variáveis mais relevantes que influenciam o cancelamento.
* Treinar e avaliar modelos preditivos para classificar clientes em risco.
* Propor **estratégias de retenção** baseadas nos insights obtidos.

---

# **📊 PREPARAÇÃO DOS DADOS**

**1 - Extração do Arquivo Tratado**

* Leitura do dataset tratado (`dados_tratados.csv`).
* Remoção de linhas nulas em `Cancelou`.

**2 - Remoção de Colunas Irrelevantes**

* Exclusão de colunas como `ID_Cliente` (não influenciam na previsão).

**3 - Encoding (Transformação de variáveis categóricas)**

* Variável alvo (`Cancelou`) transformada em binária (Sim/Não → 1/0).
* Variáveis categóricas transformadas com `get_dummies`.

**4 - Verificação da Proporção de Evasão**

* Visualização da distribuição de clientes que cancelaram x não cancelaram.

**5 - Balanceamento de Classes**

* Aplicação do **SMOTE** para equilibrar as classes.

**6 - Normalização / Padronização**

* Uso de `StandardScaler` para padronizar variáveis numéricas.

---

# **🔎 CORRELAÇÃO E SELEÇÃO DE VARIÁVEIS**

**7 - Análise de Correlação**

* Cálculo da matriz de correlação.
* Identificação de variáveis mais relacionadas ao `Cancelou`.

**8 - Análises Direcionadas**

* Cancelamento por:

  * Tipo de contrato
  * Método de pagamento
  * Tempo de permanência
  * Idosos

---

# **🤖 MODELAGEM PREDITIVA**

**9 - Separação de Dados**

* Divisão em treino (70%) e teste (30%), mantendo balanceamento.

**10 - Criação de Modelos**

* Treinados:

  * **Regressão Logística**
  * **Random Forest**
  * **Gradient Boosting**

**11 - Avaliação dos Modelos**

* Métricas:

  * **Precisão, Recall, F1-score**
  * **AUC (ROC)**
  * **Matriz de confusão e Curva ROC**

---

# **📌 INTERPRETAÇÃO E CONCLUSÕES**

**12 - Análise de Importância das Variáveis**

* Avaliação com `feature_importances_` (RF, GB), coeficientes (LR) e **Permutation Importance**.
* Variáveis mais relevantes:

  * **Tipo\_Contrato** (month-to-month → risco muito maior)
  * **Meses\_Permanencia** (clientes novos cancelam mais)
  * **Cobranca\_Mensal** (valores altos aumentam evasão)
  * **Metodo\_Pagamento** (pagamentos manuais = maior churn)
  * **Serviços adicionais** (Suporte Técnico, Segurança Online, Streaming).

**13 - Conclusão Estratégica**

📌 **Principais insights:**

1. Contrato mensal aumenta risco de churn.
2. Clientes recentes (baixo tempo de permanência) são mais vulneráveis.
3. Cobranças altas sem valor agregado elevam evasão.
4. Métodos de pagamento manuais têm maior risco.
5. Experiência em suporte técnico e serviços extras influenciam retenção.

🎯 **Estratégias de retenção sugeridas:**

* Incentivar contratos anuais/semestrais.
* Onboarding ativo nos primeiros meses.
* Ofertas mais acessíveis ou pacotes flexíveis.
* Incentivo ao débito automático.
* Melhorar suporte e oferecer benefícios digitais temporários.

📈 **Ações práticas:**

* Criar segmentação de risco (alto/médio/baixo).
* Testar campanhas A/B para ofertas.
* Monitoramento proativo de clientes em risco.
* Acompanhar KPIs: churn, adesão às ofertas, LTV e custo de retenção.

✅ **Resumo final:**
A evasão é mais influenciada por **contrato, permanência, valor da cobrança, forma de pagamento e serviços adicionais**.
Aplicar estratégias direcionadas nesses pontos pode reduzir churn e aumentar o faturamento recorrente.
