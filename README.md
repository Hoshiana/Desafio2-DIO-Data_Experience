# Desafio2-DIO-Data_Experience
Desafio 2 - DIO Bootcamp Data Experience
 #  Documento de Requisitos de Projeto  

Responsável Técnico: Antonio Augusto Borges


#  Análise Geral

*O cliente Mecânicos Independentes Ltda (empresa fictícia) do ramo serviços e comércio, necessita armazenar seus dados através de um Sistema de Controle e Gerenciamento de Ordens de Serviços. Foi iniciado o levantamento de requisitos conforme descrito nesse documento.*


##  Modelagem Relacional

*Neste projeto será elaborado a modelagem lógica do negócio. O SGBD utilizado será o MySQL Server. Ao desenvolvedor cabe somente a modelagem para posteriormente a construção do banco de dados em sua forma otimizada, ficando à cargo da Mecânicos Independentes Ltda a sua manutenção como Backups e segurança.*


##  Artefatos – Entrega

###  Modelagem Lógica

###  Requisitos

*A Mecânicos Independentes Ltda necessita armazenar os seus dados de vendas e serviços. O estoque não faz parte do escopo desse projeto, porém, utilizará dos produtos cadastrados nessa modelagem.*

###  Dos cadastros Gerais

De forma geral, seguem os requisitos de cadastro abaixo.
1.  Cadastro de Produtos
2.  Cadastro de fornecedores de Produtos
3.  Cadastro de Categorias
4.  Cadastro de Ordens de Serviços
5.  Cadastro de Clientes
6.  Cadastro de Endereço de Clientes
7.  Cadastro de Formas de Pagamentos
8.  Cadastro de mecânicos *(Os mecânicos cuidam das Ordens de Serviços, acompanhando as mesmas desde a recepção do veículo até a entrega ao cliente, levantando necessidades de reparos e substituição de peças.).*

##  Dos Campos

Todos os cadastros deverão ter números de identificação automáticos e aleatórios, de forma a deixar a cargo do sistema o controle de identificação de transações.

| Cadastro: |	Produto |
|---|---|
| Produto |	Nome do Produto |
| Código | Código do Produto |
| Valor | Valor de Venda do Produto |
| Custo Médio |	Custo de Compra do Produto |

| Cadastro: |	Fornecedor |
|---|---|
| Nome |	Nome ou Razão Social do Vendedor |

| Cadastro: |	Ordem de Serviço |
|---|---|
| Ordem de Serviço | 	Número da OS |
| Entrada |	Data da Emissão da Ordem de Serviço |
| Saida |	Data da Entrega da Ordem de Serviço |
| Veículo |	Nome do Veículo |
| Placa |	Número da Placa |
| Quantidade |	Quantidade de Produtos substituídos |
| Valor Produto |	Valor unitário Produto |
| Total Produto |	Valor Total dos produtos substituídos |
| Descrição dos Serviços |	Valor dos Serviços Executados |
| Total Serviços |	Total dos Serviços |
| Total |	Valor Total da Ordem de Serviço

| Cadastro: |	Cliente |
|---|---|
| Nome | Nome do Cliente |
| Telefone | Número de contato |
| Sexo | Sexo do Cliente |
| Nascimento | Data de Nascimento do Cliente |


| Cadastro: |	Endereço |
|---|---|
| Rua |	Nome da Rua |
| Cidade | Nome da Cidade |
| Estado | Nome do Estado |

| Cadastro: | Forma de Pagamento |
|---|---|
| Forma |	Nome da Forma de Pagamento |

| Cadastro: |	Mecânico |
|---|---|
| Nome | Nome do Mecânico |
| Sexo | Sexo do Mecânico |
| Código de registro | Código do mecânico |

##  Particularidades

*Requisitos levantados pelo desenvolvedor quanto a detalhes do modelo de negócio da Mecânicos Independentes Ltda. As particularidades são requisitos e são obrigatórios.*

1.  Clientes levam seus veículos à oficina mecânica para serem consertados ou para passarem por revisões periódicas;
2.  Cada veículo é designado a um mecânico responsável que identifica os serviços a serem executados e preenche uma Ordem de Serviço com data estimada de entrega;
3.  A partir da Ordem de Serviço, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra;
4.  Na Ordem de Serviços pode conter um ou mais produtos, diferentes ou do mesmo tipo, contendo um subtotal de produtos do mesmo tipo e um total, com a soma de todos os produtos.






 
