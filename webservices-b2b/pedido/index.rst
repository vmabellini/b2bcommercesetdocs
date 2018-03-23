Pedido
======

Os webservices de pedido envolvem a alteração de status dos pedidos efetuados. Além disso, em alguns modelos, é possível que a integração de pedido seja feita de forma passiva (o Erp vem buscar no webservice os pedidos efetuados em uma fila) ao invés de ativa (o site envia os pedidos para o Erp ao concluir o checkout).

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - ErpId
     - string
     - Código do fabricante no Erp. **Deve ser único**
   * - Descricao
     - string
     - Descrição do fabricante a ser criado
   * - Nome
     - string
     - Nome do fabricante exibido no Site B2B

Métodos
-------

.. toctree::
   
   metodos/alterarstatuspedidoerp.rst
