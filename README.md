# 📚 Análise de Banco de Dados de Livros — Proposição de Novo Produto

## 📌 Sobre o Projeto
Este projeto realiza uma análise exploratória e quantitativa no banco de dados de um serviço concorrente no mercado de livros, contendo dados sobre obras, editoras, autores, classificações (ratings) e resenhas (reviews) de usuários.

A análise utiliza consultas SQL para extrair métricas sobre o catálogo e o comportamento dos leitores, gerando insights estratégicos para embasar a proposta de valor e as funcionalidades de um novo produto no segmento de leitura.

## 🎯 Objetivos
- Compreender o volume e a atualidade do catálogo de livros disponível;
- Mapear o nível de interação e a percepção de qualidade dos leitores por meio de notas e resenhas;
- Identificar as editoras de maior destaque em publicações completas (excluindo brochuras e materiais curtos);
- Identificar autores de alta performance com base em um volume mínimo de avaliações representativo;
- Analisar o comportamento de consumo (ratings) versus a produção de conteúdo (reviews) entre os usuários mais engajados.

## 🛠️ Ferramentas e Tecnologias
- Python
- Pandas
- SQLAlchemy (Conexão e consultas ao banco PostgreSQL)
- PostgreSQL
- Jupyter Notebook

## 🔎 Análises e Consultas Realizadas
- Exploração Inicial: Inspeção do modelo relacional (chaves primárias e estrangeiras) e contagem do volume total de dados em cada tabela (books, authors, publishers, ratings e reviews);
- Volume do Catálogo: Filtro temporal para contabilizar livros publicados após 1º de janeiro de 2000;
- Métricas por Livro: Agrupamento e cálculo da quantidade de classificações e nota média por obra;
- Análise de Editoras: Identificação da editora com maior volume de livros com mais de 50 páginas;
- Avaliação e Reputação de Autores: Identificação dos autores com obras que possuem pelo menos 50 avaliações, com análise e ordenação pela média das notas.
- Comportamento dos Usuários Engajados: Subconsultas para medir o número médio de resenhas textuais escritas por usuários com mais de 50 livros classificados.

## 📈 Principais Resultados
- Atualidade do Catálogo: Dos 1.000 livros presentes na base, 819 livros foram publicados após 1º de janeiro de 2000, indicando um catálogo focado em publicações recentes.
- Interpretação de Avaliações: Evidenciou-se que notas médias elevadas devem ser analisadas junto ao volume de avaliações, visto que poucas notas distorcem a percepção de qualidade do produto.
- Liderança Editorial: A Penguin Books destacou-se como a principal editora no segmento de livros completos (> 50 páginas), com 42 obras publicadas.
- Autor em Destaque: Aplicando o filtro rigoroso de no mínimo 50 classificações por livro, o autor/dupla com a maior nota média foi J.K. Rowling/Mary GrandPré, com média de 4,29.

Consumo vs. Produção de Conteúdo:
- Os leitores altamente ativos classificaram, em média, 54,33 livros por pessoa.
- Contudo, esses mesmos usuários produziram uma média de 24,33 resenhas textuais.
- Esse achado comprova que dar uma nota (consumo/classificação) é uma ação mais frequente do que escrever um texto (produção de conteúdo/resenha).

## 💡 Conclusão
Os resultados fornecem direcionamentos claros para o desenvolvimento e curadoria do novo produto:
- Curadoria de Conteúdo e Parcerias: Editoras de grande volume como a Penguin Books e autores com forte apelo do público (como J.K. Rowling) devem ser priorizados em negociações e destaques de catálogo.
- Sistemas de Recomendação: Usuários engajados fornecem um volume massivo de classificações numéricas (mais de 50 por perfil), o que garante uma base rica de dados para alimentar algoritmos de recomendação personalizada.
- Incentivo à Comunidade: Como apenas uma parcela do público ativo escreve resenhas completas (24,33 resenhas vs 54,33 avaliações), o novo produto deve implementar mecânicas de gamificação e incentivos específicos para estimular a escrita de críticas textuais e enriquecer a comunidade.

## 📓 Notebook

A análise completa pode ser consultada no notebook:

[👉 Acessar o notebook do projeto](notebook.ipynb)
