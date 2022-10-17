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
 <img src='https://s3.us-west-2.amazonaws.com/secure.notion-static.com/71ce4cc2-b26c-4033-a82c-2ba943e35937/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221017%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221017T170250Z&X-Amz-Expires=86400&X-Amz-Signature=60b62d8da5e3ea8e29650b23477073ca461be991ac9f7e09334d26922fb79195&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject' width = 70%\>
</div>

Para avaliar se esses 7% dos pedidos afetados pelo atraso estão diminuindo a satisfação dos clientes de forma considerável, foi feito um cruzamento entre a tabela de pedidos e a tabela de review, o que trouxe o resultado de que existe uma grande disparidade na avaliação feita pelo cliente que recebeu em dia e o cliente que não recebeu em dia, tendo uma grande queda na nota dada por esse segundo grupo.

<div align = 'center'>
 <img src='https://s3.us-west-2.amazonaws.com/secure.notion-static.com/133481c2-c05e-4712-a70d-5c0196517636/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221017%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221017T170331Z&X-Amz-Expires=86400&X-Amz-Signature=3badd5cc113786723169d73e2b1b89f25a3634fefcfa73c4f875d89a44a4d53f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject' width = 70%\>
</div>

Também foi possível constatar o grande número de comentários que reforçam essa indignação das pessoas por parte do tempo de entrega.

<div align = 'center'>
 <img src='https://s3.us-west-2.amazonaws.com/secure.notion-static.com/06a072f9-b093-4f68-bbae-1dadd824911f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221017%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221017T170356Z&X-Amz-Expires=86400&X-Amz-Signature=7dfb8f18976c78f003c806231d75d5bbecf2d72be3b916994d8cbff198c8df68&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject' width = 70%\>
</div>
