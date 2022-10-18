# Análise Brazilian Ecommerce Dataset

### Desafio proposto

Analisar a base de dados disponível para ajudar a área de negócios da empresa a entender **se entregas atrasadas estão sendo um problema**  com a finalidade da **aprovação de um investimento em uma área de melhoria da experiência do cliente ao ter um atraso na entrega.**

Link para acesso ao dataset: [https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce?select=olist_customers_dataset.csv](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce?select=olist_customers_dataset.csv)

- Algumas considerações são importantes
    - O **time de logística não considera que o atraso na entrega é um problema relevante** e falou que, em média, as entregas estão sendo feitas 10 dias antes do prazo combinado
    - Não é desejado a previsão de uma entrega atrasada, apenas a **exposição que esse é um problema que pode impactar os clientes**

<div align = 'center'>
 <img src='https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb' width = 50%\>
</div>

### O Projeto

Inicialmente, foi criado um banco de dados a partir das bases em csv para facilitar tratamentos futuros através do uso de SQL.

Com o banco de dados criado, foi realizada a conexão utilizando o sqlite3 e a base  de ‘orders’ foi visualizada para um entendimento geral. 

Adiante, foi constatado que na média, a empresa está entregando com 12 dias de antecedência (indo de acordo com o que o time da logística levantou), porém, mesmo assim está ocorrendo atraso na entrega de cerca de 7% dos pedidos, chegando a 19% de atrasos no mês que apresentou um maior percentual.

<div align = 'center'>
 <img src='https://user-images.githubusercontent.com/114163919/196523223-20a69947-a3b1-4496-8b85-7bc3b45790de.png' width = 70%\>
</div>


Para avaliar se esses 7% dos pedidos afetados pelo atraso estão diminuindo a satisfação dos clientes de forma considerável, foi feito um cruzamento entre a tabela de pedidos e a tabela de review, o que trouxe o resultado de que existe uma grande disparidade na avaliação feita pelo cliente que recebeu em dia e o cliente que não recebeu em dia, tendo uma grande queda na nota dada por esse segundo grupo.

<div align = 'center'>
 <img src='https://user-images.githubusercontent.com/114163919/196523416-bd1f0a9e-662c-4e96-8832-4c7598eece9f.png' width = 70%\>
</div>

Também foi possível constatar o grande número de comentários que reforçam essa indignação das pessoas por parte do tempo de entrega.

<div align = 'center'>
 <img src='https://user-images.githubusercontent.com/114163919/196523509-d9464598-ce8b-4df8-84c1-92d5eb16ec63.png' width = 70%\>
</div>
