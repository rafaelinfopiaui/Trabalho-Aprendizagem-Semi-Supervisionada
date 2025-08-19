# Aprendizagem Semi-Supervisionada: Classificador de Imagens CIFAR-10

### Introdução e Objetivo

Este projeto visa desenvolver um classificador de imagens que aproveita tanto os dados rotulados quanto os não rotulados para maximizar a acurácia, simulando cenários reais onde a rotulação é limitada por restrições de recursos

### Conjunto de Dados

O projeto utiliza o conjunto de dados CIFAR-10, que contém 60.000 imagens coloridas de 32x32 pixels, divididas em 10 classes
Para simular o aprendizado semi-supervisionado, a divisão dos dados foi a seguinte:
* **Imagens Rotuladas**: 5.000 imagens (500 por classe).
* **Imagens Não Rotuladas**: 45.000 imagens.
* **Imagens para Teste**: 10.000 imagens, usadas para a avaliação final.

### Metodologia

A metodologia do projeto seguiu as seguintes etapas:
1.  **Pré-processamento:** Normalização dos valores dos pixels para o intervalo `[0,1]` e tratamento de valores ausentes.
2.  **Aumento de Dados:** Aplicação de transformações como rotações e espelhamentos apenas no conjunto rotulado para aumentar a variedade.
3.  **Algoritmo e Arquitetura:**
    * **Algoritmo Principal:** MixMatch, uma técnica que combina consistência e *mixup*.
    * **Arquitetura:** Uma CNN com 13 camadas convolucionais, inspirada na WideResNet.
    * **Função de Perda:** Uma combinação de entropia cruzada para dados rotulados e erro quadrático médio para a consistência em dados não rotulados.

### Resultados

O modelo foi avaliado com as seguintes métricas : Acurácia, F1-Score, Precisão e Recall. Os resultados demonstraram que o modelo semi-supervisionado superou o modelo puramente supervisionado, atingindo um ganho de 16,3 pontos percentuais em acurácia.

### Como Executar o Projeto

1.  Clone este repositório.
2.  Instale as dependências usando `pip install -r requirements.txt`.
3.  Abra o arquivo `.ipynb` no Google Colab ou em um ambiente Jupyter.
4.  Execute as células na ordem para reproduzir os resultados.

### Grupo e Informações do Projeto

* **Integrantes:** Ailton Medeiros, Francisco Júnior, Gabriell Ibiapina, João Pedro Leocácio, João Vitor Rosado, Lais Eulálio, Mauricio Lima, Pablo Batista, Pedro Paulo Lucena, Rafael Oliveira, Wálisson Aguiar, Weyk Lopes.
* **Disciplina:** Deep Learning e Machine Learning.
* **Professor:** Arthur Felipe da Silva Veloso.
