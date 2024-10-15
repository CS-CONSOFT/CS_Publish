Author: Agnaldo Barros e Valter Gabriel
Data:   15.10.2024
Ojetivo: 
Efetuar as publicações nos diversos containers de homologação e produção.

Objetivo: efetuar deploy do produto CS-Icorp Tabelas nos ambientes de homologação e produção
Os ambientes de produção são diversos, ex. app1, app3, app4, etc...
A URL Base que será consumida é diferente para cada ambiente. Ex. https://app1.csicorpnet.com.br; https://app3.csicorpnet.com.br, etc...
Para atender esse requisito, definimos o ambiente que será passado. Ex. dev, prod, etc...
Esses identificadores serão responsáveis por rotear a URL base de acordo com o ambiente desejado
O mapeamento da URL se dá da seguinte maneira atualmente:

dev aponta para       -> https://dsv17.csicorpnet.com.br -> executando no container teste1.csicorpnet.com.br
prod_app1 aponta para -> https://app1.csicorpnet.com.br  -> executando no container teste2.csicorpnet.com.br
prod_app3 aponta para -> https://app3.csicorpnet.com.br  -> executando no container teste3.csicorpnet.com.br
prod_app4 aponta para -> https://app4.csicorpnet.com.br

Por fim, a versão deve ser fornecida, sendo ela o valor de versão do projeto. 

Containers:

