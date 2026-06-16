# 2BI_InteligenciaArtificial
Disciplina de Inteligência Artificial, Professor Munif, Unicesumar 2026.

Lauren Kunz e Silva. RA: 23118770-2. 
Vinicius Seifert Fonceca. RA: 21044082-2. 

   Predição de Depressão em Adolescentes Utilizando Técnicas de Inteligência Artificial. 

 1. Resumo do Projeto

  O uso excessivo de redes sociais e dispositivos eletrônicos tem sido associado ao aumento de problemas relacionados à saúde mental, especialmente entre adolescentes. Com o crescimento das plataformas digitais, torna-se importante compreender como hábitos tecnológicos e fatores comportamentais podem influenciar o desenvolvimento de transtornos psicológicos, como a depressão.

  Problema: É possível prever a ocorrência de depressão em adolescentes utilizando informações relacionadas ao uso de redes sociais, hábitos de sono, desempenho acadêmico, atividade física e indicadores emocionais?

 Hipótese da Equipe: Acredita-se que algoritmos de Inteligência Artificial sejam capazes de identificar padrões comportamentais associados à depressão, permitindo prever sua ocorrência com níveis satisfatórios de precisão.

2. Dataset Utilizado

  Foi utilizado o Teen Mental Health Dataset, contendo 1.200 registros de adolescentes e informações relacionadas ao uso de redes sociais, hábitos de vida e indicadores emocionais.

 Origem:  https://www.kaggle.com/datasets/algozee/teenager-menthal-healy
Quantidade de Registros: 1.200 registros
Variável Alvo: depression_label


3. Métodos de IA Utilizados

Foram utilizados dois algoritmos de classificação:

Árvore de Decisão (Decision Tree)
Rede Neural Artificial Multicamadas (MLP)

4. Avaliação dos Modelos

  Os modelos foram avaliados utilizando: Acurácia, Precisão, Recall, F1-Score e Matriz de Confusão. Além disso, foram gerados gráficos comparativos para análise do desempenho.

 5. Apresentação dos Resultados e Comparação dos Modelos

5.1. Resultados da Árvore de Decisão: 

   Após o treinamento da Árvore de Decisão, o modelo foi avaliado utilizando 240 registros do conjunto de testes. 

Métrica Resultado
Acurácia 99,17%
Precisão 83,33%
Recall 83,33%
F1-Score 83,33%


Análise da Matriz de Confusão da Árvore de Decisão. 

A matriz de confusão apresentou os seguintes resultados:

Classe Real            Classe Prevista                  Quantidade
Verdadeiros Negativos | Não depressão → Não depressão | 233
Falsos Positivos      | Não depressão → Depressão     | 1
Falsos Negativos      | Depressão → Não depressão.    | 1
Verdadeiros Positivos | Depressão → Depressão         | 5


  O modelo classificou corretamente 238 dos 240 registros avaliados, cometendo apenas dois erros. Os resultados demonstram elevada capacidade de identificação dos casos de depressão e não depressão.

5.2. Resultados da Rede Neural (MLP)

   A Rede Neural Multicamadas foi implementada manualmente utilizando NumPy, contendo uma camada oculta com 8 neurônios e função de ativação sigmóide.

Métrica    Resultado
Acurácia   97,50%
Precisão  50,00%
Recall    33,33%
F1-Score  40,00%


Análise da Curva de Perda da Rede Neural.  

A Figura apresenta a curva de perda da Rede Neural durante o treinamento.

  Observa-se uma redução contínua do erro ao longo das épocas, passando de aproximadamente 0,22 para valores próximos de 0,01. Esse comportamento indica que a rede conseguiu aprender os padrões presentes nos dados e ajustar seus pesos adequadamente.

 A estabilização da curva nas últimas épocas demonstra que o modelo atingiu convergência, apresentando um processo de treinamento estável e eficiente.

Análise da Matriz de Confusão

  A matriz de confusão apresentou os seguintes resultados:


Classe Real               Classe Prevista                 Quantidade
Verdadeiros Negativos  | Não depressão → Não depressão   | 232
Falsos Positivos       | Não depressão → Depressão       | 2
Falsos Negativos       | Depressão → Não depressão       | 4
Verdadeiros Positivos  | Depressão → Depressão           | 2


   Embora a rede neural tenha apresentado boa acurácia geral, observou-se uma menor capacidade de identificar corretamente os casos positivos de depressão, resultando em valores reduzidos de recall e F1-score.

5.3 Comparação Entre os Modelos


A Tabela a seguir apresenta a comparação direta entre os modelos desenvolvidos.

Métrica
          Árvores de Decisão | Rede Neural
Acurácia     99,17%              97,50%
Precisão     83,33%              50,00%
Recall       83,33%              33,33%
F1-Score     83,33%              40,00%


6. Conclusão.  

   Observa-se que a Árvore de Decisão apresentou melhor desempenho em todas as métricas analisadas.

   A diferença mais significativa ocorreu no Recall, métrica responsável por indicar a capacidade do modelo em identificar corretamente os adolescentes que apresentam depressão. Enquanto a Árvore de Decisão conseguiu identificar aproximadamente 83% dos casos positivos, a Rede Neural identificou apenas cerca de 33%.

  O F1-Score também evidenciou a superioridade da Árvore de Decisão, demonstrando melhor equilíbrio entre Precisão e Recall.

  Uma possível justificativa para esse resultado é o tamanho relativamente reduzido do conjunto de dados e o desbalanceamento entre as classes. Em cenários com menor quantidade de dados, modelos baseados em árvores frequentemente apresentam desempenho superior ao de Redes Neurais, que normalmente necessitam de maiores volumes de exemplos para atingir seu potencial máximo.

   Dessa forma, conclui-se que a hipótese inicial foi confirmada, evidenciando que técnicas de Inteligência Artificial podem ser utilizadas para auxiliar na identificação de fatores relacionados à depressão em adolescentes. Para o conjunto de dados analisado, a Árvore de Decisão mostrou-se a solução mais eficiente entre os métodos avaliados.

