# 📍 Pontos Turísticos da Baixada Santista: Análise de Similaridade

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![NLTK](https://img.shields.io/badge/NLTK-3.8-yellow.svg)](https://www.nltk.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-orange.svg)](https://scikit-learn.org/stable/)
[![Numpy](https://img.shields.io/badge/Numpy-1.2x-brightgreen.svg)](https://numpy.org/)
[![Google Colab](https://img.shields.io/badge/Google_Colab-Pronto_para_uso-blueviolet.svg)](https://colab.research.google.com/)

---

## 📖 Descrição

Este projeto é um sistema de recomendação de conteúdo que utiliza **Processamento de Linguagem Natural (NLP)** para sugerir pontos turísticos na Baixada Santista com base nas preferências textuais do usuário.

### Observação Importante sobre os Dados:

Atualmente, a base de dados do projeto contém apenas **8 arquivos** de pontos turísticos na pasta ZIP. Devido a este conjunto de dados limitado, o resultado da similaridade pode não ser um "match" exato para buscas muito específicas. O objetivo primário do projeto é demonstrar a metodologia de Similaridade do Cosseno.


### O que o projeto faz?

O script solicita que o usuário descreva o tipo de local que deseja visitar (ex: "uma praia popular e movimentada, com boa infraestrutura"). Em seguida, ele compara essa descrição com uma base de dados de pontos turísticos (armazenados em arquivos `.txt`) e recomenda aquele que tiver a maior **Similaridade do Cosseno**.

No exemplo do estudo, a busca por uma "praia bem popular e movimentada" recomendou com sucesso a **Praia da Enseada**.

### Com o que foi feito?

Este projeto foi desenvolvido inteiramente em **Python**, utilizando as seguintes bibliotecas principais:

* **Google Colab:** Para o ambiente de desenvolvimento e upload de arquivos.
* **NLTK (Natural Language Toolkit):** Para a etapa de NLP, especificamente para carregar e customizar a lista de *stopwords* (palavras de parada, como 'o', 'de', 'para') do português.
* **Scikit-learn (Sklearn):** Para a vetorização dos textos usando `TfidfVectorizer` e para o cálculo da `cosine_similarity` (Similaridade do Cosseno).
* **Numpy:** Para manipulações matemáticas e cálculos dos ângulos de similaridade.
* **Zipfile e OS:** Para a manipulação dos arquivos `.zip` e leitura dos dados do sistema de arquivos.

### Por que? (A Metodologia)

O objetivo central foi aplicar conceitos de **Ciência de Dados** e **Recuperação de Informação (RI)** em um cenário prático. A **Similaridade do Cosseno** é uma métrica poderosa para determinar o quão "próximos" dois documentos estão em um espaço vetorial.

O processo funciona assim:
1.  Textos (a busca do usuário e as descrições dos locais) são "limpos" (removendo *stopwords*).
2.  Eles são transformados em vetores numéricos pela técnica **TF-IDF** (Term Frequency-Inverse Document Frequency), que dá peso à relevância das palavras.
3.  A Similaridade do Cosseno calcula o ângulo entre o vetor da busca e os vetores de cada ponto turístico. Um ângulo menor (mais próximo de 0°) significa uma similaridade maior.

---

## 🚀 Instruções de Instalação e Uso

Este projeto foi desenvolvido para rodar no ambiente do Google Colab, o que facilita a configuração.

### Pré-requisitos

Para executar o projeto, você precisará das seguintes bibliotecas:

* `nltk`
* `scikit-learn`
* `numpy`

### Etapas de Instalação

No seu ambiente Python, você pode instalar as dependências com:


pip install nltk scikit-learn numpy


Em seguida, dentro do próprio script, é necessário baixar os pacotes de stopwords do NLTK:

Python

import nltk
nltk.download('stopwords')
No arquivo .ipynb do projeto, esta etapa já está incluída.

▶️ Instruções de Uso
Para testar o sistema de recomendação, siga estes passos no notebook (.ipynb):

Execute a Célula 1 (Importação das Bibliotecas): Isso irá carregar todas as ferramentas necessárias e baixar as stopwords.

Execute a Célula 2 (files.upload()): Uma janela de upload aparecerá. Envie o arquivo pontos_turisticos.zip que contém a base de dados.

Execute a Célula 3 (Extrair o conteúdo do zip): Esta célula irá descompactar os arquivos .txt para que o código possa lê-los.

Modifique a Célula 4 (Variável descricao):

Este é o passo mais importante! Altere o texto da variável descricao para o que você deseja buscar.

Exemplo: descricao = '''Estou procurando um lugar histórico, bom para fotos.'''

Execute o restante das células: Siga executando as células de "Stopwords", "Vetorização" e "Impressão das similaridades".

Confira o Resultado: A última célula, "Ponto Turístico Recomendado", irá imprimir o nome e a descrição do local mais similar à sua busca, junto com o ângulo de similaridade. 


## 🤝 Contribuição e Contato

Este projeto foi desenvolvido como um estudo de caso em Ciência de Dados e tem um código aberto. Se você tiver sugestões, encontrar bugs ou quiser discutir melhorias, sinta-se à vontade para abrir uma *Issue* neste repositório.

### Liberdade de Uso e Expansão:

O código aqui presente é de livre uso para estudos e projetos. **Você tem total liberdade para expandir o projeto e adicionar mais pontos turísticos à base de dados** (seguindo o formato de arquivos `.txt` dentro do ZIP) ou adaptar o código conforme sua vontade.

Para ver outros projetos, visite meu perfil no GitHub:

* **GitHub:** [github.com/Marques07](https://github.com/Marques07)

Se utilizar este código como base para seus estudos, por favor, cite este repositório.
