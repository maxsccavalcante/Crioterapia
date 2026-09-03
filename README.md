INSIGHT DO PROJETO - Previsão de Resultado de Tratamento de Crioterapia

Objetivo: usar Naive Bayes (GaussianNB) para prever, a partir de características do paciente (sexo, idade, número de verrugas, tipo e área afetada), se o tratamento de crioterapia teve sucesso ou não.

Resultado obtido:
- Acurácia no treino: ~0.81 (81%)
- Acurácia na validaçãoo (dados nunca vistos): ~0.67-0.74
- O modelo generaliza razoavelmente bem, mas o gap entre treino e validação sugere que há espaço para melhorar (mais dados ajudariam, já que a base tem só 90 pacientes).

Alterações feitas no notebook original:
1. Corrigido bug na função plot_corr(): referenciava uma variável inexistente (dados_mamiferos_treino) em vez do parâmetro correto (df_crioterapia_treino), o que causava NameError.
2. Adicionada verificação com os.path.exists() antes de cada Image(), para as imagens ilustrativas (Workflow.png, Treinamento.png, ConfusionMatrix.jpg) não travarem a execução do notebook quando ausentes da pasta.
3. Adicionado random_state fixo no train_test_split (execuções anteriores), garantindo resultados reproduzíveis entre diferentes execuções.
