Listar pedidos 
=============================

Liste todos os pedidos pendentes através do **Listar** passando a entidade abaixo:

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Ate
     - DateTime
     - Data limite do pedido
   * - De
     - DateTime
     - Data limite do pedido
   * - Novos
     - bool
     - 0 para pedidos não pendentes, 1 para pedidos pendentes

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:Listar>
           <tem:filtro>
              <b2b:Ate>2018-12-04</b2b:Ate>
              <b2b:De>2010-12-04</b2b:De>
              <b2b:Novos>0</b2b:Novos>
           </tem:filtro>
        </tem:Listar>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <ListarResponse xmlns="http://tempuri.org/">
           <ListarResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:PageCount>1</a:PageCount>
              <a:PageIndex>0</a:PageIndex>
              <a:PageSize>2147483647</a:PageSize>
              <a:Pedidos>
                 <a:PedidoDTO>
                    <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
                    <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                    <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                    <a:BandeiraDoCartao/>
                    <a:ClienteFinalId i:nil="true"/>
                    <a:DadosAdicionais/>
                    <a:DataCriacao>2018-02-09T12:24:10.86</a:DataCriacao>
                    <a:DescontoPedido>0.0000</a:DescontoPedido>
                    <a:Descontos>
                       <a:PedidoDTO.DescontoDTO>
                          <a:BandeiraDoCartao i:nil="true"/>
                          <a:DataFim i:nil="true"/>
                          <a:DataInicio i:nil="true"/>
                          <a:DescontoPercentual>10.0000</a:DescontoPercentual>
                          <a:DescontoValor>0.0000</a:DescontoValor>
                          <a:Id>8</a:Id>
                          <a:Nome>Teste Qa - Bundle Discount</a:Nome>
                          <a:Promocode i:nil="true"/>
                          <a:TipoDeDesconto>AssignedToBundle</a:TipoDeDesconto>
                       </a:PedidoDTO.DescontoDTO>
                    </a:Descontos>
                    <a:DistributionCentersToChargeSt/>
                    <a:FormaDePagamento>Payments.Faturado</a:FormaDePagamento>
                    <a:FreteTotal>84.3000</a:FreteTotal>
                    <a:Id>556227</a:Id>
                    <a:IdNaRevenda i:nil="true"/>
                    <a:IdPedidoCliente i:nil="true"/>
                    <a:IdPrazoPagamento>7</a:IdPrazoPagamento>
                    <a:IdPrazoPagamentoString>7</a:IdPrazoPagamentoString>
                    <a:InformacoesDepositoTransferencia/>
                    <a:Itens>
                       <a:PedidoDTO.PedidoItemDTO>
                          <a:BundleId i:nil="true"/>
                          <a:CentroDistribuicaoId>1</a:CentroDistribuicaoId>
                          <a:CentroDistribuicaoPrefix>DG</a:CentroDistribuicaoPrefix>
                          <a:ESD>true</a:ESD>
                          <a:Encomenda>false</a:Encomenda>
                          <a:ExtensoesDeGarantia i:nil="true"/>
                          <a:MpDoBem>false</a:MpDoBem>
                          <a:Necessidade>false</a:Necessidade>
                          <a:Open>false</a:Open>
                          <a:PartNumber>0010000003369</a:PartNumber>
                          <a:ProdutosExtensoesDeGarantia i:nil="true"/>
                          <a:Quantidade>1</a:Quantidade>
                          <a:Sku>54151</a:Sku>
                          <a:ValorComissao>0</a:ValorComissao>
                          <a:ValorDescontoProduto>321.8200</a:ValorDescontoProduto>
                          <a:ValorTotal>2896.3400</a:ValorTotal>
                          <a:ValorUnitario>2896.3400</a:ValorUnitario>
                       </a:PedidoDTO.PedidoItemDTO>
                       <a:PedidoDTO.PedidoItemDTO>
                          <a:BundleId i:nil="true"/>
                          <a:CentroDistribuicaoId>1</a:CentroDistribuicaoId>
                          <a:CentroDistribuicaoPrefix>DG</a:CentroDistribuicaoPrefix>
                          <a:ESD>true</a:ESD>
                          <a:Encomenda>false</a:Encomenda>
                          <a:ExtensoesDeGarantia i:nil="true"/>
                          <a:MpDoBem>false</a:MpDoBem>
                          <a:Necessidade>false</a:Necessidade>
                          <a:Open>false</a:Open>
                          <a:PartNumber>0010000003574</a:PartNumber>
                          <a:ProdutosExtensoesDeGarantia i:nil="true"/>
                          <a:Quantidade>1</a:Quantidade>
                          <a:Sku>200199</a:Sku>
                          <a:ValorComissao>0</a:ValorComissao>
                          <a:ValorDescontoProduto>72.0000</a:ValorDescontoProduto>
                          <a:ValorTotal>648.0000</a:ValorTotal>
                          <a:ValorUnitario>648.0000</a:ValorUnitario>
                       </a:PedidoDTO.PedidoItemDTO>
                       <a:PedidoDTO.PedidoItemDTO>
                          <a:BundleId i:nil="true"/>
                          <a:CentroDistribuicaoId>1</a:CentroDistribuicaoId>
                          <a:CentroDistribuicaoPrefix>DG</a:CentroDistribuicaoPrefix>
                          <a:ESD>true</a:ESD>
                          <a:Encomenda>false</a:Encomenda>
                          <a:ExtensoesDeGarantia i:nil="true"/>
                          <a:MpDoBem>false</a:MpDoBem>
                          <a:Necessidade>false</a:Necessidade>
                          <a:Open>false</a:Open>
                          <a:PartNumber>0110000003009</a:PartNumber>
                          <a:ProdutosExtensoesDeGarantia i:nil="true"/>
                          <a:Quantidade>2</a:Quantidade>
                          <a:Sku>61155</a:Sku>
                          <a:ValorComissao>0</a:ValorComissao>
                          <a:ValorDescontoProduto>66.0200</a:ValorDescontoProduto>
                          <a:ValorTotal>594.2000</a:ValorTotal>
                          <a:ValorUnitario>297.1000</a:ValorUnitario>
                       </a:PedidoDTO.PedidoItemDTO>
                    </a:Itens>
                    <a:LicenciadoOpenValueId i:nil="true"/>
                    <a:LinkNotaFiscal i:nil="true"/>
                    <a:NumeroNotaFiscal i:nil="true"/>
                    <a:OrderGuid>38a6a2fa-1699-4534-a928-58b288c005ce</a:OrderGuid>
                    <a:PagamentoBNDES i:nil="true"/>
                    <a:RevendaId>1</a:RevendaId>
                    <a:StTotal>0.0000</a:StTotal>
                    <a:SubTotal>4138.5400</a:SubTotal>
                    <a:TipoVenda>1</a:TipoVenda>
                    <a:Total>4015.9130</a:Total>
                    <a:VendedorErpId i:nil="true"/>
                 </a:PedidoDTO>
                 <a:PedidoDTO>
                    <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
                    <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                    <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                    <a:BandeiraDoCartao/>
                    <a:ClienteFinalId i:nil="true"/>
                    <a:DadosAdicionais/>
                    <a:DataCriacao>2018-02-14T18:38:34.51</a:DataCriacao>
                    <a:DescontoPedido>0.0000</a:DescontoPedido>
                    <a:Descontos/>
                    <a:DistributionCentersToChargeSt/>
                    <a:FormaDePagamento>Payments.Faturado</a:FormaDePagamento>
                    <a:FreteTotal>0.0000</a:FreteTotal>
                    <a:Id>556228</a:Id>
                    <a:IdNaRevenda i:nil="true"/>
                    <a:IdPedidoCliente i:nil="true"/>
                    <a:IdPrazoPagamento>1</a:IdPrazoPagamento>
                    <a:IdPrazoPagamentoString>1</a:IdPrazoPagamentoString>
                    <a:InformacoesDepositoTransferencia/>
                    <a:Itens>
                       <a:PedidoDTO.PedidoItemDTO>
                          <a:BundleId i:nil="true"/>
                          <a:CentroDistribuicaoId>1</a:CentroDistribuicaoId>
                          <a:CentroDistribuicaoPrefix>DG</a:CentroDistribuicaoPrefix>
                          <a:ESD>true</a:ESD>
                          <a:Encomenda>false</a:Encomenda>
                          <a:ExtensoesDeGarantia i:nil="true"/>
                          <a:MpDoBem>false</a:MpDoBem>
                          <a:Necessidade>false</a:Necessidade>
                          <a:Open>false</a:Open>
                          <a:PartNumber>0010000003574</a:PartNumber>
                          <a:ProdutosExtensoesDeGarantia i:nil="true"/>
                          <a:Quantidade>1</a:Quantidade>
                          <a:Sku>200199</a:Sku>
                          <a:ValorComissao>0</a:ValorComissao>
                          <a:ValorDescontoProduto>0.0000</a:ValorDescontoProduto>
                          <a:ValorTotal>720.0000</a:ValorTotal>
                          <a:ValorUnitario>720.0000</a:ValorUnitario>
                       </a:PedidoDTO.PedidoItemDTO>
                    </a:Itens>
                    <a:LicenciadoOpenValueId i:nil="true"/>
                    <a:LinkNotaFiscal i:nil="true"/>
                    <a:NumeroNotaFiscal i:nil="true"/>
                    <a:OrderGuid>b95a69ce-f0cb-4067-9567-c6726a7e8bd5</a:OrderGuid>
                    <a:PagamentoBNDES i:nil="true"/>
                    <a:RevendaId>1</a:RevendaId>
                    <a:StTotal>0.0000</a:StTotal>
                    <a:SubTotal>720.0000</a:SubTotal>
                    <a:TipoVenda>1</a:TipoVenda>
                    <a:Total>720.0000</a:Total>
                    <a:VendedorErpId i:nil="true"/>
                 </a:PedidoDTO>
              </a:Pedidos>
           </ListarResult>
        </ListarResponse>
     </s:Body>
  </s:Envelope>
