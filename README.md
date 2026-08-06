# Machine Learning Aplicado a Investimentos

## 🎯 Contexto e Objetivos
Este repositório contém um Caderno Temático desenvolvido como parte do bootcamp promovido pelo Santander Brasil em parceria com a DIO. O objetivo central deste projeto é utilizar o **NotebookLM** da Google como uma ferramenta de aprendizagem ativa para explorar as aplicações de Inteligência Artificial no mercado financeiro.

O foco escolhido foi a distinção e aplicabilidade de **Modelos Supervisionados (predição de ativos)** e **Modelos Não Supervisionados (clusterização e gestão de risco)**. A proposta é consolidar o aprendizado em IA Generativa aliado à análise quantitativa de dados, unindo o rigor estatístico acadêmico com demandas reais do mercado corporativo — como a necessidade de lidar com dados não-estacionários e alta volatilidade —, inspirando-se em desafios práticos de finanças quantitativas.

---

## 📚 Curadoria de Fontes
Para garantir que a IA gerasse respostas com alto rigor técnico e sem alucinações, foram selecionados materiais especializados (papers e relatórios da indústria) focados em Finanças Quantitativas. Os seguintes documentos foram carregados no NotebookLM:

1. **[CFA Institute Equips the Investment Sector to Navigate AI Developments](https://www.cfainstitute.org/about/press-room/2025/ai-in-asset-management-report-2025)**
2. **[Artificial Intelligence and the Future of Finance](https://rpc.cfainstitute.org/research/reports/2026/artificial-intelligence-future-of-finance)**
3. **[New CFA Institute Report Urges Financial Sector to Prioritize Explainability in AI Adoption](https://www.cfainstitute.org/about/press-room/2025/explainable-ai-in-finance-2025)**
4. **[Random Forest vs XGBoost: Qual Algoritmo Escolher para Seus Dados Tabulares?](https://turing.education/blog/random-forest-vs-xgboost-qual-algoritmo-escolher-para-seus-dados-tabulares)**
5. **[XGBoost vs Random Forest for Stock Prediction](https://slmaj.com/blog/xgboost-vs-random-forest)**

*(Nota: Todos os arquivos originais em formato PDF/TXT alimentaram a base de conhecimento exclusiva deste caderno).*

---

## 🛠️ Engenharia de Prompts e "Cicatrizes"
Durante o processo de construção deste guia, o desafio foi extrair da IA respostas que fugissem de definições rasas da Wikipedia e adotassem a postura crítica de um analista quantitativo. Abaixo, documento o processo de *troubleshooting* (tentativa e erro):

### Ciclo 1: Explorando Modelos Supervisionados
* **Prompt Inicial (A Cicatriz):** *"Me explique como usar modelos supervisionados no mercado de ações de acordo com as fontes."*
* **Troubleshooting:** A resposta gerada foi demasiadamente genérica, ignorando problemas cruciais das séries temporais financeiras, como o ruído dos dados históricos e o vazamento de informações (look-ahead bias).
* **Prompt Refinado (Ouro):** *"Atue como um Cientista de Dados Sênior especialista em Finanças Quantitativas. Com base EXCLUSIVAMENTE nos documentos fornecidos, crie um resumo técnico sobre a aplicação de Modelos Supervisionados (como Random Forest ou XGBoost) para previsão de retornos de ativos. Foque nos riscos de usar dados históricos financeiros e explique como evitar o overfitting no mercado."*
* **Resultado Obtido:** A IA mudou a abordagem e passou a destacar que modelos em finanças não buscam acertar o preço exato, mas encontrar alfas probabilísticos, apontando a necessidade de métodos de validação robustos (Walk-Forward).

### Ciclo 2: Gestão de Risco e Modelos Não Supervisionados
* **Prompt Inicial (A Cicatriz):** *"O que as fontes dizem sobre modelos não supervisionados e investimentos?"*
* **Troubleshooting:** A resposta definiu algoritmos (como PCA e K-Means) apenas do ponto de vista estatístico, sem conectá-los à dor real de um gestor: a diversificação de carteiras.
* **Prompt Refinado (Ouro):** *"Aja como um Gestor de Portfólio Quantitativo. Extraia das fontes fornecidas as aplicações práticas de Modelos Não Supervisionados. Estruture a resposta explicando como essas técnicas ajudam a identificar correlações ocultas entre ações para melhorar a diversificação da carteira e reduzir o risco sistêmico."*
* **Resultado Obtido:** O NotebookLM conectou com precisão a redução de dimensionalidade à descoberta de estruturas latentes de risco, permitindo alocações de capital muito mais seguras.

---

## 📓 Miniguia de Estudo (Entrega Final)

### 1. Resumo Estruturado do Assunto
No mercado financeiro, os modelos supervisionados baseados em árvores, como Random Forest e XGBoost, dominam a previsão de retornos e a geração de sinais de trading a partir de dados estruturados e tabulares. Enquanto o Random Forest utiliza o método de bagging para treinar múltiplas árvores de decisão independentes a partir de subamostras aleatórias de dados, diluindo a variância e mitigando o risco de overfitting, o XGBoost emprega o gradient boosting sequencial para focar nos erros residuais e extrair sinais preditivos sutis de bases de dados imensas. Para evitar distorções e look-ahead bias decorrentes do fluxo temporal dos dados, esses algoritmos dependem de uma rigorosa Walk-Forward Validation.

Por outro lado, a gestão de risco e a diversificação de carteiras são aprimoradas por modelos não supervisionados, que buscam descobrir estruturas ocultas e relações de dependência intrínsecas nos dados. A Análise de Componentes Principais (PCA) destaca-se ao reduzir a dimensionalidade de grandes conjuntos de dados financeiros. O PCA quantifica matematicamente o teor de informação contido nos dados por meio da variância, projetando os retornos dos ativos sob um novo sistema de coordenadas lineares ortogonais.

Para contornar as limitações de interações estritamente lineares, o mercado utiliza autoencoders para a estruturação de deep portfolios. Sendo formalmente compreendidos como a contraparte não linear do PCA, os autoencoders são redes neurais não supervisionadas projetadas para reconstituir os seus próprios dados de entrada e aprender representações latentes sem a necessidade de estimar explicitamente a matriz de variância-covariância clássica. 

Adicionalmente, técnicas de agrupamento (clustering) baseadas na teoria dos grafos oferecem uma via robusta de diversificação de risco. A estratégia de Hierarchical Risk Parity (HRP) sintetiza as dependências mútuas entre as ações organizando o mercado sob uma árvore geradora mínima. O método distribui o capital de forma ponderada pelo risco ao longo desses clusters naturais de ativos, fornecendo proteção superior fora da amostra e reduzindo a concentração excessiva.

### 2. Glossário Quant/ML
* **Walk-Forward Validation:** Técnica obrigatória para séries temporais financeiras que avança a janela de teste cronologicamente, impedindo o vazamento de dados do futuro durante o treinamento. 
* **Overfitting (Sobreajuste):** Risco crítico em mercados devido à baixíssima relação sinal-ruído; ocorre quando o modelo memoriza os ruídos históricos falhando ao operar com dados inéditos. 
* **Análise de Componentes Principais (PCA):** Transformação matemática linear que reduz a dimensionalidade de grandes matrizes projetando-os em eixos baseados na direção de maior variância. 
* **Valores de Shapley (SHAP):** Método de Inteligência Artificial Explicável (XAI) que decompõe uma previsão, quantificando o peso exato de cada variável no resultado final. 
* **Autoencoders:** Redes neurais não supervisionadas (contraparte não-linear do PCA) usadas para aprender representações latentes de risco e construir carteiras complexas. 
* **Métodos de Ensemble:** Arquitetura que combina múltiplos algoritmos preditivos através de um sistema de consenso para cancelar erros não correlacionados.

### 3. Prompts de Revisão (Para uso futuro)
Para manter o conhecimento fresco ou simular entrevistas técnicas, utilize os seguintes prompts neste caderno do NotebookLM:

> **Prompt 1: Validação de Modelos e Resistência a Ruídos**
> *"Atue como um Gerente de Pesquisa Quantitativa me entrevistando para uma vaga. Faça-me perguntas sequenciais sobre os riscos de 'overfitting' no mercado de ações. Exija que eu explique por que divisões aleatórias padrão (train/test split) falham e como implementar a técnica de 'Walk-Forward Validation'. Compare o tratamento de ruído entre Random Forest e XGBoost."*

> **Prompt 2: Redução de Dimensionalidade**
> *"Inicie uma simulação de entrevista técnica (Diretor de Alocação de Ativos). Peça-me para explicar o PCA, focando na intuição estatística de que 'variância é informação'. Como eu usaria um 'Scree Plot' para reter fatores sistemáticos? Em quais cenários eu utilizaria 'Autoencoders' para superar o PCA na construção de 'Deep Portfolios'?"*

> **Prompt 3: Explicabilidade e Governança**
> *"Assuma o papel de um Oficial de Conformidade (Compliance). Peça-me para explicar o que são os Valores de Shapley (SHAP) e como eles decompõem a previsão de um modelo. Questione por que a literatura sugere inserir uma 'estrutura econômica' em vez de deixar o algoritmo otimizar apenas a acurácia estatística bruta."*
