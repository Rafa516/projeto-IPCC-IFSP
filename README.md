<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/8a/Instituto_Federal_de_S%C3%A3o_Paulo_-_Marca_Horizontal_2015.svg" alt="Logo do IFSP - Instituto Federal de São Paulo" width="400">
</p>

# Trabalho Prático – Obtenção e Visualização de Dados com Python

## Integrantes

- Luan Nascimento Caetano
- Rafael da Silva Oliveira

## Objetivo

Este trabalho tem como objetivo integrar os conceitos iniciais de programação e análise de dados estudados na disciplina, utilizando **Python** e, obrigatoriamente, as bibliotecas **NumPy, Pandas e Matplotlib**.

A atividade deverá ser desenvolvida **em duplas** e consistirá na obtenção, organização, tratamento e visualização de um conjunto de dados. Cada trabalho deverá demonstrar não apenas o funcionamento do programa, mas também a utilização adequada das estruturas e técnicas estudadas durante as aulas. Não se espera, ainda, uma análise dos dados. O foco nesta disciplina é a familiarização com as técnicas de programação necessárias.

**Prazo para entrega: 15 dias a partir da data de disponibilização da atividade.**

## Descrição da tarefa

Cada dupla deverá escolher ou criar um conjunto de dados relacionado a um tema de seu interesse. Alguns exemplos são: desempenho de alunos, vendas de uma empresa, temperaturas de diferentes cidades, resultados esportivos, consumo de energia, dados populacionais, preços de produtos ou informações sobre filmes e séries. Existem diversos repositórios de conjuntos de dados adequados:

- <https://www.kaggle.com/datasets>
- <https://archive.ics.uci.edu/datasets>
- <https://www.kaggle.com/datasets/abdoomoh/all-seaborn-built-in-datasets>
- <https://basedosdados.org/search>

O conjunto utilizado deverá possuir uma quantidade suficiente de registros e atributos para permitir operações de seleção, filtragem, limpeza, cálculo de estatísticas e geração de gráficos.

O programa deverá realizar as seguintes etapas:

### 1. Organização inicial dos dados

Os dados deverão ser inicialmente representados ou manipulados por meio de pelo menos uma **estrutura de dados nativa do Python**, como:

- lista;
- lista de listas;
- tupla;
- dicionário;
- lista de dicionários.

Parte desses dados deverá posteriormente ser convertida ou utilizada na construção de estruturas do NumPy ou do Pandas.

### 2. Utilização do NumPy

A solução deverá empregar o **NumPy** para realizar operações numéricas sobre os dados.

Devem ser demonstradas, no mínimo:

- criação ou conversão de dados para arrays NumPy;
- acesso a elementos ou subconjuntos dos dados utilizando **indexação e slicing**;
- realização de pelo menos duas operações ou cálculos utilizando recursos do NumPy, tais como média, soma, mínimo, máximo, desvio-padrão ou outras operações apropriadas ao problema.

### 3. Utilização do Pandas

Os dados deverão ser organizados em pelo menos um **DataFrame do Pandas**.

A dupla deverá realizar operações que demonstrem:

- criação ou importação de um DataFrame;
- seleção de linhas e/ou colunas;
- **filtragem de registros de acordo com alguma condição**;
- identificação de dados ausentes, incorretos ou inválidos;
- **remoção ou tratamento desses dados inválidos**;
- ordenação dos dados segundo algum critério;
- cálculo de pelo menos duas informações estatísticas ou agregadas relevantes.

O conjunto de dados deverá possuir alguns registros ausentes ou inválidos. Caso os dados originais não apresentem esses problemas, a dupla poderá introduzir propositalmente alguns valores inválidos para demonstrar as técnicas de identificação, filtragem e limpeza.

### 4. Visualização com Matplotlib

Utilizando o **Matplotlib**, deverão ser produzidos **pelo menos três gráficos**, sendo obrigatoriamente utilizados pelo menos dois tipos diferentes de representação.

Podem ser utilizados, por exemplo, gráficos de:

- barras;
- linhas;
- dispersão;
- histogramas;
- setores (pizza).

Os gráficos deverão possuir títulos e identificação adequada dos eixos e, quando necessário, legendas.

Os gráficos escolhidos deverão ser coerentes com os dados analisados e contribuir para a interpretação dos resultados.

## Requisitos obrigatórios

O trabalho deverá demonstrar claramente o uso de:

**Python:** estruturas de dados nativas, condicionais e/ou repetições quando apropriadas.

**NumPy:** arrays, indexação/slicing e operações numéricas.

**Pandas:** DataFrames, seleção, filtragem, ordenação, identificação e tratamento ou remoção de dados inválidos.

**Matplotlib:** construção e personalização básica de gráficos.

Não será considerado suficiente utilizar as bibliotecas apenas para importar os dados. O código deverá demonstrar efetivamente a aplicação dos recursos estudados.

## Entrega

Cada dupla deverá entregar um **Jupyter Notebook (`.ipynb`)**, que poderá ser desenvolvido no JupyterLab ou no Google Colab.

O notebook deverá conter células de texto explicando:

1. o tema escolhido;
2. a origem e o significado dos dados;
3. as etapas de tratamento realizadas;
4. os gráficos gerados.

O código deverá estar organizado em células e acompanhado de comentários sempre que forem necessários para facilitar sua compreensão.

Caso seja utilizado um arquivo externo, como um arquivo CSV, esse arquivo também deverá ser entregue juntamente com o notebook.

## Desenvolvimento em dupla

A atividade deverá ser realizada **exclusivamente em pares**. Os nomes dos dois integrantes deverão aparecer claramente no início do notebook.

Espera-se que ambos os integrantes participem do desenvolvimento e sejam capazes de explicar as decisões tomadas, as operações realizadas e o funcionamento do código apresentado.

## Prazo

A entrega deverá ser realizada **em até 15 dias**, contados a partir da disponibilização desta atividade.

O trabalho deverá representar uma pequena análise completa de dados: **organizar → selecionar → limpar → visualizar**.
