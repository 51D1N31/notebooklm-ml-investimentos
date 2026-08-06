# notebooklm-ml-investimentos

## 🛠️ Engenharia de Prompts e "Cicatrizes"

Durante a exploração das fontes no NotebookLM, o foco foi evitar respostas superficiais e forçar a IA a adotar um perfil analítico e crítico, voltado para as nuances reais do mercado financeiro.

### Teste 1: O desafio da Predição (Modelos Supervisionados)
* **O Prompt Inicial:** *"Me explique como usar modelos supervisionados no mercado de ações de acordo com as fontes."*
* **Troubleshooting (A Cicatriz):** A resposta veio extremamente genérica. A IA explicou o que é um modelo supervisionado, mas não abordou o maior desafio de dados financeiros: a não-estacionariedade e o risco de overfitting ao tentar prever séries temporais com alto ruído.
* **O Prompt Refinado:** *"Atue como um Cientista de Dados Sênior especialista em Finanças Quantitativas. Com base EXCLUSIVAMENTE nos documentos fornecidos, crie um resumo técnico sobre a aplicação de Modelos Supervisionados para previsão de retornos... [inserir prompt completo]"*
* **Resultado:** A IA produziu uma resposta madura, destacando que modelos supervisionados em finanças não devem buscar prever o preço exato, mas sim tendências probabilísticas, com forte foco em backtesting robusto.

### Teste 2: Diversificação de Portfólio (Modelos Não Supervisionados)
* **O Prompt Inicial:** *"O que as fontes dizem sobre modelos não supervisionados?"*
* **Troubleshooting:** Faltou aplicabilidade. A IA definiu o conceito estatístico, mas não como isso resolve o problema de um analista de dados no mercado.
* **O Prompt Refinado:** *"Aja como um Gestor de Portfólio Quantitativo. Extraia das fontes as aplicações práticas de Modelos Não Supervisionados... [inserir prompt completo]"*
* **Resultado:** O NotebookLM gerou insights práticos fantásticos, detalhando como algoritmos de clusterização identificam ações que se movem juntas, auxiliando na redução de redundância de risco dentro de uma carteira de investimentos.
