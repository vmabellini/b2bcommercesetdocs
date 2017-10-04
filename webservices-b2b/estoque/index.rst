Estoque
=======

O webservice de estoque possui apenas um método que serve para alterar a quantidade em estoque de um ou mais produtos.

Cabe a integração chamar periodicamente esse método para atualizar os estoques do **Site B2B**. A frequência de chamadas a esse método depende da estratégia a ser adotada de acordo com a quantidade de pedidos que o **Site B2B** recebe diariamente. É recomendado que o estoque seja completamente atualizado pelo menos uma vez por dia, durante um horário de baixo acesso (madrugada).

O sistema de atualização de estoque é o único que além de poder ser ativado via webservice (ERP envia pro Site B2B), **também pode ser demandado (Site B2B pede pro ERP via GIAPI)**.

Toda vez que um pedido estiver prestes a ser efetuado, o **Site B2B** realiza uma verificação no ERP para atualizar o estoque e obter o dado mais recente, evitando que um pedido seja fechado sem estoque ativo no ERP.

Métodos:

.. toctree::
   
   metodos/atualizarestoque.rst
