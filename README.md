# AtividadeRedpill

Atividade em Sala - Livraria Redpill - Matéria:  Inteligência Artificial - Profº Leandro.

# Problema de Negócio

A Empresa Redpill Bookstore está com problemas no seu sistema de
recomendações, o sistema está recomendando apenas os livros que são
recém-lançados sem priorizar os gostos dos usuários, a Redpill é líder de mercado e
referência no ramo de e-books, a empresa não relatou nenhum problema com as
recomendações em seu relatório. Mas, eles desejam reformular o seu sistema para
dar uma comodidade melhor aos seus usuários e recomendar os seus produtos de
forma centralizada com os gostos dos mesmos.
Como não foi relatado nenhum problema com o sistema atual, podemos continuar
recomendando os novos e-books para promover os lançamentos e usar esse
método com os novos usuários.
Não houve relato de problemas por parte da empresa, mas demos uma olhada nos
dados disponibilizados e verificamos que grande parte dos usuários estão
avaliando os e-books com uma nota baixa, esse é um problema que pode atrapalhar
o relacionamento dos usuários com a Redpill.

![Captura de tela 2022-05-23 233223](https://user-images.githubusercontent.com/43474592/169937327-d5857717-8375-45ce-b39d-146a220209ab.png)


# Dados e Premissas

Os Datasets disponibilizados pela empresa contém informações valiosas que podem nos
ajudar na resolução do problema, ao todo são 3 datasets, o primeiro é o (Books.csv) esse
dataset contém todo o acervo da Redpill, o segundo é o (Ratings.csv), esse dataset contém
as avaliações dos usuários, já o terceiro é o (Users.csv) e esse dataset contém algumas
informações sobre os usuários, como a idade e o local onde cliente reside.

# Abordagem utilizada

Para resolvermos o problema da recomendação, a nossa tarefa será difícil, conforme
relatamos no primeiro tópico(Problema de negócio), grande parte dos usuários deram uma
nota baixa nos produtos da Redpill, buscar uma similaridade entre os usuários será uma
tarefa difícil.
Mesmo com o problema das avaliações, continuaremos seguindo com esse método para
coletar as avaliações dos e-books que foram bem avaliados, com isso, podemos criar um
ranking com as melhores avaliações para recomendar aos usuários, conforme a imagem
abaixo.

Neste modelo, utilizaremos a regra de associação para recomendar os e-books mais
populares da plataforma, podemos aplicar esse modelo nos novos usuários e nos usuários
frequentes da Redpill.
Podemos utilizar também uma filtragem colaborativa baseada nos usuários através das
similaridades entre eles, neste caso iremos utilizar o cálculo de distância Euclidiana, este
cálculo vai nos auxiliar na busca de usuários com os perfis similares. Através dessa busca,
quanto mais próximo um usuário estiver do outro, melhor será o grau de recomendação do
e-book.

![Captura de tela 2022-05-23 233737](https://user-images.githubusercontent.com/43474592/169937435-f031ca7e-64c3-42fe-9272-2daaa57119bd.png)


# Técnicas Aplicadas

As técnicas que serão utilizadas nesse projeto são regras de associações, nós iremos
utilizar um sistema de recomendação popular para priorizar os e-books que tiveram as
melhores avaliações, iremos definir um ‘top’ 10 dos itens mais bem classificados para
recomendar aos novos e frequentes usuários da Redpill. Também vamos utilizar o cálculo
de distância euclidiana para recomendar itens com base na similaridade dos usuários.

![Captura de tela 2022-05-23 233755](https://user-images.githubusercontent.com/43474592/169937466-70fe8393-0bf1-4faa-b4fe-2ec4e55818be.png)
