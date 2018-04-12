Integrar pedido
=============================

É possível realizar uma integração de pedido através do **IntegrarPedido**, informando se ele está cancelado ou não, e seu respectivo id no Erp e no B2B.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Cancelado
     - bool
     - 0 para não cancelado, 1 para cancelado
   * - PedidoErpId
     - string
     - Id do Pedido no Erp
   * - PedidoId
     - int
     - Id do Pedido no B2B

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO" xmlns:arr="http://schemas.microsoft.com/2003/10/Serialization/Arrays">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:IntegrarPedido>
           <tem:pedidoIntegracao>
              <b2b:Cancelado>0</b2b:Cancelado>
              <b2b:PedidoErpId>
                 <arr:string>AAAA-13245</arr:string>
              </b2b:PedidoErpId>
              <b2b:PedidoId>556172</b2b:PedidoId>
           </tem:pedidoIntegracao>
        </tem:IntegrarPedido>
     </soapenv:Body>
  </soapenv:Envelope>


Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <IntegrarPedidoResponse xmlns="http://tempuri.org/">
           <IntegrarPedidoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </IntegrarPedidoResult>
        </IntegrarPedidoResponse>
     </s:Body>
  </s:Envelope>
