# Combinação de modelos - Bagging

No decorrer desta atividade busquei criar um modelo simplificado da técnica `Bagging` usando árvores de decisão. Para tal, defini uma função com as características:
- Seleção do modelo de decisão: Regressão (regressor) ou classificação (classifier)
- Separação dos dados a serem preenchidos/sugeridos pelo modelo
- Criação de amostras (amostragem com repetição)
- Avaliação da quantidade de dados repetidos
- Geração de modelos para cada amostra criada:
  - Separação em dados de treino e teste
  - Criação e treino da árvore de decisão
  - Pós-poda utilizando ccp_alphas para selecionar a *melhor árvore* com o melhor "score"
 - Seguido pela obtenção dos dados antes faltantes (separados no segundo item)  agora sugeridos pela *melhor árvore* 
- Agregação de acordo com o modelo de decisão (classificação ou regressão)
A função retorna as melhores previsões geradas por cada modelo gerado para cada amostragem e também, por meio da agregação, os valores mais adequados filtrados a partir da saída dos modelos de aprendizado (de acordo com a técnica) para substituir os dados faltantes.

Uma segunda função para anexar os dados obtidos pelo **Bagging** (agregação) ao dataframe também está presente.


## Bibliotecas
- [Pandas](https://pandas.pydata.org/)
- [Numpy](https://numpy.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Scikit-learn](https://scikit-learn.org/stable/)
- [Random](https://docs.python.org/pt-br/3.13/library/random.html)
- [Collections](https://docs.python.org/3/library/collections.html)
