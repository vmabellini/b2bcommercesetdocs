Consultar Status do Site
========================

Através desse método é possível consultar um ID de pedido do site e verificar se o pedido está cancelado, além de poder também visualizar quais são os IDs de pedidos ERP relacionados, e o status de cada um deles no site.

Essa consulta retorna como informação principal a propriedade CanceladoNoSite do tipo Boolean.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
    <soapenv:Header/>
    <soapenv:Body>
        <tem:ConsultarStatusDoSite>
          <!--Optional:-->
          <tem:pedidoId>12345</tem:pedidoId>
        </tem:ConsultarStatusDoSite>
    </soapenv:Body>
  </soapenv:Envelope>
   

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Body>
        <ConsultarStatusDoSiteResponse xmlns="http://tempuri.org/">
          <ConsultarStatusDoSiteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:CanceladoNoSite>false</a:CanceladoNoSite>
              <a:PedidoId>556141</a:PedidoId>
              <a:PedidosErp>
                <a:ConsultaStatusPedidoItemDTO>
                    <a:PedidoErpId>4875f41b-8ad6-482f-956c-bcf7252fe44b</a:PedidoErpId>
                    <a:Status>Nenhum</a:Status>
                </a:ConsultaStatusPedidoItemDTO>
              </a:PedidosErp>
          </ConsultarStatusDoSiteResult>
        </ConsultarStatusDoSiteResponse>
    </s:Body>
  </s:Envelope>
