Alteração de status do pedido
=============================

É possível enviar uma alteração do status do pedido do ERP para o Webservice através do **AtualizarStatusPedidoErp**.
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
     - Novo status do pedido (Descricao)
     
.. list-table:: OrderSiteStatus
   :widths: auto
   :header-rows: 1

   * - Id
     - Descricao
   * - 0
     - Nenhum
   * - 1
     - LibComercial
   * - 2
     - LibFinanceira
   * - 3
     - Separacao
   * - 4
     - Despacho
   * - 5
     - Entrega

Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO">
      <soapenv:Header/>
      <soapenv:Body>
         <tem:AtualizarStatusPedidoErp>
            <!--Optional:-->
            <tem:statusPedidoErpDto>
               <b2b:ErpId>123456</b2b:ErpId>
               <b2b:Status>LibComercial</b2b:Status>
            </tem:statusPedidoErpDto>
         </tem:AtualizarStatusPedidoErp>
      </soapenv:Body>
   </soapenv:Envelope>
   

Exemplo de response

.. code-block:: xml

   <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
      <s:Body>
         <AtualizarStatusPedidoErpResponse xmlns="http://tempuri.org/">
            <AtualizarStatusPedidoErpResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
               <a:Error>false</a:Error>
               <a:ErrorType i:nil="true"/>
               <a:Message i:nil="true"/>
            </AtualizarStatusPedidoErpResult>
         </AtualizarStatusPedidoErpResponse>
      </s:Body>
   </s:Envelope>
