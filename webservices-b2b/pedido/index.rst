Pedido
======

Os webservices de pedido envolvem a alteração de status dos pedidos efetuados. Além disso, em alguns modelos, é possível que a integração de pedido seja feita de forma passiva (o Erp vem buscar no webservice os pedidos efetuados em uma fila) ao invés de ativa (o site envia os pedidos para o Erp ao concluir o checkout).

Na maioria dos casos não se usa o webservice de pedido, exceto para atualização de status de pedidos.


Métodos
-------

.. toctree::
   
   metodos/alterarstatuspedidoerp.rst
   metodos/integrarpedido.rst
   metodos/listar.rst
   metodos/listarnovos.rst
   metodos/notificaralteracaodestatus.rst
