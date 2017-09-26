Webservices do Site B2B
=======================

O **Site B2B** oferece uma camada de serviços que o cliente deverá chamar para realizar as seguintes tarefas:

* Carregar a lista de produtos para o site
* Gerenciar categorias e fabricantes
* Enviar atualização da lista de estoque
* Enviar a lista de revendas e usuários da revenda para acesso ao site

A integração com os webservices do site é bastante simples e baseada em uma camada desenvolvida em WCF, fornecendo os métodos SOAP/REST para fácil integração com outras linguagens e sistemas. 

OBS: **nós recomendamos o uso da interface WSDL/SOAP padrão**, principalmente se for integrado com uma plataforma .NET, para facilitar os testes e agilizar o processo de desenvolvimento.

Nos subtópicos seguintes abordaremos cada método de forma detalhada.

.. toctree::
   
   estrutura.rst
   seguranca.rst
   enderecos.rst