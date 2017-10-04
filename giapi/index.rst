APIs de integração (GI API)
===========================

O **Site B2B** realiza chamadas para o ambiente do cliente para obter dados de preços, clientes, estoque, prazos de pagamento e enviar os pedidos feitos pelo site.

Para isso, desenvolvemos uma interface de comunicação baseada em REST onde o Site B2B faz chamadas para os serviços que o cliente irá desenvolver para dar suporte as necessidades da loja. Para facilitar o desenvolvimento e os testes, fornecemos um projeto template desenvolvido em .NET no Visual Studio 2015 com ASP.NET Web Api. Cabe ao cliente decidir se irá utilizar o template como base para criar sua própia Api ou se irá desenvolver utilizando outra linguagem, **contanto que siga estritamente o mesmo formato de entrada/saída e todos os métodos necessários para a integração.**

Existe uma documentação dinâmica no nosso ambiente de homologação gerada automaticamente pela nossa API no endereço: http://apidev.atma-it.com/Help. A mesma documentação também é gerada automaticamente ao executar o projeto template.

Nos subtópicos seguintes detalhamos melhor todo o processo de integração.

.. toctree::

   preparo.rst
   token.rst