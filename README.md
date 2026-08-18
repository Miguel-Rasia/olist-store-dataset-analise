# Analise de Vendas Olist Store

![Dashboard de Vendas](docs\screenshots\dashboard.png)

## Sobre o Projeto
 Esse projeto analisa diversos dados sobre a Olist Store, como a visão geral, os clientes mais valiosos e quais compraram uma única vez, regiões do Brasil mais lucrativas, tempo de entrega, etc.


## Objetivo
O principal objetivo é obter informações valiosas com o projeto para que se tenha uma ideia de quais passos a empresa deveria tomar para um futuro melhor.

## Dados
Os dados utilizados foram o Dataset da empresa brasileira Olist Store, disponível gratuitamente no Kaggle.
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## Ferramentas Utilizadas
Para este projeto foi utilizado o PostgreSQL no processo de ETL para obter novas informações úteis ao projeto e Power BI que utilizou as informações geradas para criar um Dashboard interativo que mostra certas informações em gráficos e que podem ser manipuladas de acordo com o período de tempo desejado.

## Análise com SQL
### 1. Visão Geral
Esta query básica nos mostra somente o faturamento total, o pedido total e o ticket médio que a Olist Store teve no período desse dataset (cerca de 2 anos).

### 2. Categorias e Vendas
O dataset utilizado infelizmente não disponibiliza o nome dos produtos vendidos, então tive que optar pelas categorias desses produtos para continuar. A query agrupa os itens pelas suas categorias e faz um somatório total das vendas e uma contagem dos pedidos, e as lista pelo faturamento de forma decrescente.

### 3. Clientes
De forma similar à query anterior, esta mostra de forma decrescente os clientes mais valiosos e a contagem de seus pedidos.

### 4. Regiões 
Essa query agrupa os estados brasileiros em 5 regiões: Norte, Nordeste, Centro-Oeste, Sudeste e Sul, e mostra qual região os clientes pertencem.

### 5. Datas
Esta query lista todos os dados de datas que o dataset possui e cria uma nova coluna de total_time_order, que se baseia no cálculo do momento em que o produto chegou ao cliente - o momento em que a compra foi efetuada, ou seja, o tempo total para que o cliente recebesse o seu produto.

## Dashboard no Power BI

O dashboard mostra: visões gerais, categorias mais rentáveis, faturamento por cliente por região e quantos clientes compraram 1, 2 ou 3+ vezes.  
Além disso, o dashboard conta com uma opção de selecionar o período de tempo desejado para a análise.

## Principais Insights  

Com as queries no PostgreSQL e o dashboard em Power BI foi possível concluir o seguinte:
- A grande maioria dos clientes compraram uma única vez, mesmos os mais valiosos. Logo, há uma necessidade de manter esses clientes.
- As regiões com a maior média de faturamento são as com menor volume de pedidos. Ou seja, essas regiões podem apresentar um potencial de crescimento e vale uma análise mais aprofundada sobre.
- O faturamento das categorias mais rentáveis não é tão diferente das demais. Então pode ser viável investir nas demais categorias.

## Como Utilizar o Projeto
### PostgreSQL
Baixe o dataset e as views criadas, coloque o dataset em um DB no pgaAdmin 4 e cole o conteúdo das views em queries novas.
### Power BI
Baixe o dashboard e abra-o no Power BI e carregue os dados do dataset + views.

## Autor
**Miguel Rasia**  
Estudante de Ciência da Computação e interessado na área de análise de dados, SQL e Business Intelligence.  
Fiz esse projeto para praticar SQL e Power BI e aprender mais.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Perfil-blue?logo=linkedin)](https://www.linkedin.com/in/miguel-rasia-b4069b318/)
[![GitHub](https://img.shields.io/badge/GitHub-Perfil-black?logo=github)](https://github.com/Miguel-Rasia)