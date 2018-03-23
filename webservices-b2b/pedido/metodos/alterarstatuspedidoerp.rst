Alteração de status do pedido
=============================

É possível enviar uma alteração do status do pedido do ERP para o Webservice.
Dentro do modelo de pedidos, um pedido do webservice pode ser quebrado em N pedidos dentro do ERP, cada um com um status próprio.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - ErpId
     - string
     - Código do pedido no Erp. **Deve ser único**
   * - Status
     - OrderSiteStatus
     - Novo status do pedido
