Notificar alteração de status
=============================

É possível enviar uma notificação de alteração de status do pedido do ERP através do **NotificarAlteracaoDeSatus** enviando a observação a ser notificada, o id do epdido do erp e o novo status do pedido.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Observacao
     - string
     - Observação a ser notificada
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
   * - -1
     - Cancelado
   * - 0
     - Recebido
   * - 1
     - LiberacaoComercial
   * - 2
     - LiberacaoFinanceira
   * - 3
     - EmSeparacao
   * - 4
     - Despachado
   * - 5
     - Entregue

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:NotificarAlteracaoDeStatus>
           <tem:alteracaoStatusDto>
              <b2b:Observacao>Exemplo de observação</b2b:Observacao>
              <b2b:OrderERPId>AAAA-13245</b2b:OrderERPId>
              <b2b:StatusPedido>LiberacaoFinanceira</b2b:StatusPedido>
           </tem:alteracaoStatusDto>
        </tem:NotificarAlteracaoDeStatus>
     </soapenv:Body>
  </soapenv:Envelope>
   

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <NotificarAlteracaoDeStatusResponse xmlns="http://tempuri.org/">
           <NotificarAlteracaoDeStatusResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:BandeiraDoCartao/>
              <a:ClienteFinalId i:nil="true"/>
              <a:DadosAdicionais/>
              <a:DataCriacao>2017-09-25T19:58:44.87</a:DataCriacao>
              <a:DescontoPedido>0.0000</a:DescontoPedido>
              <a:Descontos/>
              <a:DistributionCentersToChargeSt/>
              <a:FormaDePagamento>Payments.Faturado</a:FormaDePagamento>
              <a:FreteTotal>0.0000</a:FreteTotal>
              <a:Id>556172</a:Id>
              <a:IdNaRevenda i:nil="true"/>
              <a:IdPedidoCliente i:nil="true"/>
              <a:IdPrazoPagamento>2</a:IdPrazoPagamento>
              <a:IdPrazoPagamentoString>2</a:IdPrazoPagamentoString>
              <a:InformacoesDepositoTransferencia/>
              <a:Itens/>
              <a:LicenciadoOpenValueId i:nil="true"/>
              <a:LinkNotaFiscal i:nil="true"/>
              <a:NumeroNotaFiscal i:nil="true"/>
              <a:OrderGuid>5d11ceb0-fa9c-4334-8c33-4db507a41a0b</a:OrderGuid>
              <a:PagamentoBNDES i:nil="true"/>
              <a:RevendaId>1</a:RevendaId>
              <a:StTotal>0.0000</a:StTotal>
              <a:SubTotal>1027.6500</a:SubTotal>
              <a:TipoVenda>1</a:TipoVenda>
              <a:Total>1027.6500</a:Total>
              <a:VendedorErpId i:nil="true"/>
           </NotificarAlteracaoDeStatusResult>
        </NotificarAlteracaoDeStatusResponse>
     </s:Body>
  </s:Envelope>
