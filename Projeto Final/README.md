
# 🧠 Classificação de Tumores Cerebrais com Rede Neural em PyTorch

Este projeto utiliza uma rede neural artificial (RNA) totalmente conectada (fully connected) implementada com PyTorch para classificar dados relacionados a tumores cerebrais. O projeto trabalha com um dataset contendo imagens de ressonâncias magnéticas do cérebro onde não há tumores e onde existem diferentes tipos de tumores. O foco é desenvolver criar e treinar uma rede neural capaz de prever a classe do tumor com base em características extraídas dos dados.


## 📁 Sobre o Projeto

O projeto realiza todas as etapas de um fluxo típico de machine learning:

- Leitura e tratamento dos dados
- Normalização e codificação de variáveis
- Divisão dos dados em conjuntos de treino e teste
- Definição e treinamento da rede neural densa
- Avaliação com métricas de desempenho
- Visualizações dos resultados

## 🧠 Arquitetura da Rede Neural

A arquitetura do modelo é composta por camadas densas (fully connected), ativação `ReLU`, e uma camada final com ativação adequada à tarefa de classificação.
Minibatches foram criados utilizando Dataloaders com o intuito de acelerar e melhorar a estabilidade do treinamento. 
O treinamento é feito utilizando backpropagation com a função de perda `CrossEntropyLoss` e o otimizador `Adam`.

## 🔍 Tecnologias e Bibliotecas


- [PyTorch](https://pytorch.org/)
- [Pandas](https://pandas.pydata.org/)
- [Scikit-learn](https://scikit-learn.org/)
- [Matplotlib](https://matplotlib.org/)


## 📦 Seções do Código

- `Importação das bibliotecas`: 
- `Importação dos dados`
- `Metodologia do Projeto`
- `Criação de Datasets de Treino e Teste`
- `Criação e Avaliação do Modelo`
- `Conclusão`

## 📊 Resultados Obtidos


Relatório de Classificação no conjunto de teste completo:
                   precision    recall  f1-score   support

    glioma_tumor           0.59      0.78      0.67       246
    meningioma_tumor       0.56      0.37      0.45       233
    no_tumor               0.57      0.42      0.48       119
    pituitary_tumor        0.82      0.90      0.86       263

    accuracy                                   0.66       861
    macro avg              0.63      0.62      0.62       861
    weighted avg           0.65      0.66      0.64       861


66% de acurácia com os dados de teste

Melhor f1-score para a classificação de pituitary tumor

Pior f1-score para a classificação de meningioma_tumor 


## Conclusão

Com base nas Métricas de classificação (acurácia, precisão, recall e F1-score) o modelo possui bom desempenho na classificação das imagens. 

Os valores próximos de acurácia para os dados de treino e teste não indicam overfitting ou underfitting.


Com base nos valores de f1-score (média harmônica da precisão e recall) o modelo obteve melhores resultados para a identificação de pituitary_tumor e piores resultados para meningioma_tumor.




## 🎯  Próximos passos
- Explorar arquiteturas mais complexas e adequadas para imagens, como redes convolucionais (CNNs);

- Utilizar Transfer Learning para reutilizar modelos já treinados em grandes bancos de dados em conjunto com o modelo original;

- Realizar validação cruzada para obter uma avaliação mais confiável;

- Considerando que a quantidade de imagens que não possuem tumor é menos da metade das existentes para cada uma das outras classes, seria interessante obter mais imagens desse tipo, ou gerar novas imagens a partir de transformações.
