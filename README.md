# **Reconhecimento de Tweets contendo Discurso de Ódio**

<p align="justify">
  <img src="https://user-images.githubusercontent.com/92948655/164021523-811ff5c8-bd41-45f7-8237-e8e21a5ac62a.png" width="600px"/>
</p>

*Fonte da imagem [aqui](https://ck37.com/project/hatespeech/).*

## **Definições**

Segundo o [SaferLab](https://saferlab.org.br/o-que-e-discurso-de-odio/) - projeto da SaferNet Brasil voltado para o apoio ao protagonismo jovem na criação de conteúdos sobre direitos humanos na internet - discurso de ódio pode ser definido como sendo qualquer tipo de manifestação que ataque ou incite o ódio contra determinados grupos sociais tendo como base raça, etnia, gênero, orientação sexual, religiosa ou origem nacional.

A análise de uma manisfestação como sendo ou não um discurso de ódio envolve um equilíbrio cuidadoso entre a liberdade de expressão e a defesa da dignidade humana.

A definição de falas e textos como conteúdo de ódio levam em consideração diversas camadas de regras como tratados internacionais, a Constituição brasileira, leis e os termos de uso de diferentes plataformas.

## **Números Atuais**

Segundo a SaferNet Brasil, desde a sua fundação em 2006 até 2021, já foram recebidas mais de 2 milhões e meio de denúncias envolvendo discurso de ódio em redes sociais. Destas denúncias, cerca de 23% envolvem racismo. Dentre as vítimas que procuram ajuda, 68% se auto declararam mulheres.

Por meio de visualizações disponibilizadas pelo projeto SaferLab, é possível notar que o número de publicações removidas de redes sociais por serem classificadas como discurso de ódio vinha em ritmo de diminuição até meados de 2017-2018. Muito provavelmente em virtude da popularização de iniciativas que visem coibir este tipo de discurso e também à pressão exercida para que as plataformas criem recursos que visem a remoção destes tipos de publicações.

Porém, de 2020 em diante é possível observar um leve aumento no número de remoções, o que demanda maior atenção ao assunto e a proposição de ferramentas cada vez mais bem treinadas para a detecção de publicações que são discurso de ódio.

</br>
<p align="justify">
  <img src="https://user-images.githubusercontent.com/92948655/164914146-d6bf4c69-ecb3-4cdc-9669-5ad2803e2d9a.png" width="700px"/>
</p>


## **Objetivo do Projeto**

Tendo em vista o cenário apresentado, tal projeto tem como objetivo o **desenvolvimento de um modelo de Rede Neural Recorrente (RNN) do tipo *many to one* que seja capaz de classificar tweets escritos em pt-BR como sendo ou não discursos de ódio.**


## **Sobre a Base de Dados**

O conjunto de dados utilizado para o desenvolvimento do presente projeto foi retirado da plataforma Kaggle em 19 de abril de 2022 e pode ser consultado [aqui](https://www.kaggle.com/datasets/hrmello/brazilian-portuguese-hatespeech-dataset).

Dentre os arquivos disponíveis, optou-se por aquele que contém a classificação binária dos tweets como sendo (1) ou não (0) um discurso de ódio. 

Cada tweet foi classificado por diferentes usuários, porém uma coluna de combinação foi disponibilizada no arquivo. Para que um tweet fosse classificado na coluna de combinação como sendo um discurso de ódio, era necessário que a maioria dos usuários o classificassem desta forma.

Segundo a plataforma, o arquivo possui 5666 valores únicos, ou seja, mais de cinco mil tweets únicos.


## **Principais Conclusões**

- A acurácia máxima de 0.71 foi alcançada para dados de teste utilizando-se um modelo de rede neural recorrente com algoritmo LSTM bidirecional; 

- Tendo em vista a complexidade dos dados e sua análise quanto a serem ou não discursos de ódio, o resultado alcançado mostrou-se bastante proveitoso.

- Todas as configurações de modelos implementadas ao longo do projeto e com conjuntos de dados que foram submetidos a diferentes transformações, apresentaram métricas similares, acima de 0.67.

- A transformação dos dados em termos de lematização e stemização não promoveu o aumento de desempenho do modelo tradicional de RNN com LSTM quando do treinamento. Uma provável justificativa é que os dados sem transformação auxiliaram no entendimento do contexto pelo modelo e na geração de previsões mais assertivas. 


## **Links que auxiliaram no desenvolvimento deste Projeto** ❤

- [Getting Started with Recurrent Neural Network (RNNs)](https://towardsdatascience.com/getting-started-with-recurrent-neural-network-rnns-ad1791206412)
- [Deep Convolutional Neural Network for Sentiment Analysis (Text Classification)](https://machinelearningmastery.com/develop-word-embedding-model-predicting-movie-review-sentiment/)
- [How to Use the Keras Functional API for Deep Learning](https://machinelearningmastery.com/keras-functional-api-deep-learning/)
- [How to Develop a Bidirectional LSTM For Sequence Classification in Python with Keras](https://machinelearningmastery.com/develop-bidirectional-lstm-sequence-classification-python-keras/)
- [Building a convolutional neural network for natural language processing](https://towardsdatascience.com/how-to-build-a-gated-convolutional-neural-network-gcnn-for-natural-language-processing-nlp-5ba3ee730bfb)
