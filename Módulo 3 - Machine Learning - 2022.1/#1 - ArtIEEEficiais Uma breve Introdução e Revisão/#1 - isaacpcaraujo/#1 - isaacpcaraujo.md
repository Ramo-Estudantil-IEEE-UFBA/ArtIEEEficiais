# Introdução aos conceitos de Aprendizado de Maquina


## O que é Aprendizado de Maquina

<br>

> Aprendizado de Máquina é o campo de estudo que dá aos computadores a habilidade de aprender sem ser explicitamente programado. - Arthur Samuel, 1959

<br>

o **Aprendizado de Máquina** é ótimo para:

* Problemas para os quais as soluções existentes exigem muita configuração 
manual ou longas listas de regras: um algoritmo de Aprendizado de Máquina 
geralmente simplifica e melhora o código;
* Problemas complexos para os quais não existe uma boa solução quando 
utilizamos uma abordagem tradicional: as melhores técnicas de Aprendizado de 
Máquina podem encontrar uma solução;
* Ambientes flutuantes: um sistema de Aprendizado de Máquina pode se adaptar 
a novos dados;
* Compreensão de problemas complexos e grandes quantidades de dados

<br>

## Tipos de Sistemas do Aprendizado de Máquina

<br>

### Aprendizado Supervisionado/Não Supervisionado: 

<br>

**Supervisionado**: No aprendizado supervisionado, os dados de treinamento que você fornece ao algoritmo incluem as soluções desejadas.

* k-Nearest Neighbours
* Regressão Linear
* Regressão Logística
* Máquinas de Vetores de Suporte (SVM)
* Árvores de Decisão e Florestas Aleatórias
* Redes Neurais

**Não Supervisionado**: No aprendizado não supervisionado, como você pode imaginar, os dados de treinamento não são rotulados. O sistema tenta aprender sem um professor.

Clustering:
* k-Means
* Clustering Hierárquico [HCA, do inglês]
* Maximização da Expectativa
* Visualização e redução da dimensionalidade

Análise de Componentes Principais [PCA, do inglês]:
* Kernel PCA
* Locally-Linear Embedding (LLE)
* t-distributed Stochastic Neighbor Embedding (t-SNE)

Aprendizado da regra da associação:
* Apriori
* Eclat

**Aprendizado Semi-supervisionado**: Alguns algoritmos podem lidar com dados de treinamento parcialmente rotulados, uma grande quantidade de dados não rotulados e um pouco de dados rotulados. 

**Aprendizado por reforço**: O aprendizado por eforço é um bicho muito diferente. O sistema de aprendizado, chamado de agente nesse contexto, pode observar o ambiente, selecionar e executar ações e obter 
recompensas em troca — ou penalidades na forma de recompensas negativas. Ele deve aprender por si só qual é a melhor estratégia, chamada de política, para 
obter o maior número de recompensas ao longo do tempo.

**Aprendizado Online e em Lote**: **No aprendizado em lote**, o sistema é incapaz de aprender de forma incremental: ele deve 
ser treinado com a utilização de todos os dados disponíveis. Isso geralmente demandará muito tempo e recursos de computação, portanto, normalmente é feito offline. Primeiro, o sistema é treinado, em seguida, é lançado em produção, e roda sem aprender mais nada; apenas aplicando o que aprendeu. Isso é chamado de aprendizado offline. Já no **No aprendizado online**, você treina o sistema de forma incremental, alimentando sequencialmente as instâncias de dados individualmente ou em pequenos grupos, chamados de minilotes. Cada etapa do aprendizado é rápida e barata, então o sistema pode aprender rapidamente sobre os novos dados assim que eles chegam.

<br>

### Aprendizado Baseado em Instância Versus Aprendizado Baseado em Modelo

<br>

**Aprendizado baseado em instância**: o sistema aprende os exemplos por meio da memorização e, em seguida, generaliza para novos casos utilizando uma medida de similaridade

**Aprendizado baseado em modelos**: Outra maneira de generalizar a partir de um conjunto de exemplos seria construir um 
modelo desses exemplos e utilizar esse modelo para fazer previsões. 

<br>

## Principais Desafios do Aprendizado de Máquina ##

<br>

* **Quantidade Insuficiente de Dados de Treinamento**;
* **Dados de Treinamento Não Representativos**: A fim de generalizar bem, é crucial que seus dados de treinamento sejam representativos dos novos casos para os quais você deseja generalizar;
* **Dados de Baixa Qualidade**: Se os dados de treinamento estiverem cheios de erros, outliers e ruídos, o sistema terá mais dificuldade para detectar os padrões subjacentes, portanto, menos propício a um bom funcionamento.
* **Características Irrelevantes**: Seleção das características: selecionar as mais úteis para treinar entre as existentes, Extração das características: combinar características existentes para produzir 
uma mais útil (como vimos anteriormente, os algoritmos de redução de dimensionalidade podem ajudar), Criação de novas características ao coletar novos dados.
* **Sobreajustando os dados de treinamento**: significa que o modelo funciona bem nos dados de treinamento, mas não generaliza tão bem. O sobreajuste acontece quando o modelo é muito complexo em relação à quantidade e ao ruído dos dados de treinamento. As possíveis 
soluções são: Simplificar o modelo ao selecionar um com menos parâmetros, Coletar mais dados de treinamento e Reduzir o ruído nos dados de treinamento (por exemplo,corrigir erros de dados e remover outliers).
* **Subajustando os dados de Treinamento**: é o oposto de sobreajuste: ocorre quando seu modelo é muito simples para o aprendizado da estrutura subjacente dos dados. As principais opções para resolver esses problemas são: Selecionar um modelo mais poderoso, com mais parâmetros; Alimentar o algoritmo de aprendizado com melhores características (feature 
engineering); Reduzir as restrições no modelo (por exemplo, reduzindo o hiperparâmetro de regularização).

## Exercícios

1. Como você definiria o Aprendizado de Máquina?
2. Você saberia nomear quatro tipos de problemas nos quais o AM se destaca?
3. O que é um conjunto de treinamento rotulado?
4. Quais são as duas tarefas supervisionadas mais comuns?
5. Você consegue nomear quatro tarefas comuns sem supervisão?
6. Que tipo de algoritmo de Aprendizado de Máquina você utilizaria para permitir 
que um robô ande em vários terrenos desconhecidos?
7. Que tipo de algoritmo você utilizaria para segmentar seus clientes em vários grupos?
8. Você enquadraria o problema da detecção de spam como um problema de aprendizado 
supervisionado ou sem supervisão?
9. O que é um sistema de aprendizado online?
10. O que é o out-of-core learning?
11. Que tipo de algoritmo de aprendizado depende de uma medida de similaridade 
para fazer previsões?
12.Qual a diferença entre um parâmetro de modelo e o hiperparâmetro do algoritmo 
de aprendizado?
13. O que os algoritmos de aprendizado baseados em modelos procuram? Qual é a estratégia mais comum que eles utilizam para ter sucesso? Como fazem 
previsões?
14. Você pode citar quatro dos principais desafios no Aprendizado de Máquina?
15. Se o seu modelo é ótimo nos dados de treinamento, mas generaliza mal para novas instâncias, o que está acontecendo? Você pode nomear três soluções possíveis?
16. O que é um conjunto de testes e por que você o utilizaria?
17. Qual é o propósito de um conjunto de validação?
18. O que pode dar errado se você ajustar os hiperparâmetros utilizando o conjunto 
de teste?
19. O que é validação cruzada e por que você preferiria usá-la ao invés de um 
conjunto de validação?

# Projeto de Aprendizado de Maquina ##

## Enquadre o Problema ##

Como um cientista de dados bem organizado, a primeira coisa a fazer é obter sua lista de verifcação do projeto. Primeiro, você precisa enquadrar o problema: será supervisionado, sem supervisão ou um Aprendizado por Reforço? Será uma tarefa de classificação, de regressão ou outra coisa? Você deve utilizar técnicas de aprendizado em lote ou online? 

## Selecione uma Medida de Desempenho ##

Seu próximo passo é selecionar uma medida de desempenho. Uma medida típica de desempenho para problemas de regressão é a Raiz do Erro Quadrático Médio (sigla 
RMSE, em inglês)

## Verifique as Hipóteses ##

uma boa prática é listar e verificar as hipóteses que foram feitas até agora (por 
você ou outros); fica mais fácil pegar problemas sérios logo no início.

<br>

Colocando a mão na massa:

<br>

## Obtenha os Dados e Crie o Espaço de Trabalho ##

Utilize o arquivo ***housing.csv*** para a realização deste projeto de AM.



