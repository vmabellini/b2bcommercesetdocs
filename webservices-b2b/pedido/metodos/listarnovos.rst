Listar pedidos pendentes (novos)
=============================

Liste todos os pedidos pendentes através do **ListarNovos** passando apenas um parâmetro, o **page**, que deve iniciar por zero e ser incrementado até encerrar os resultados.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:ListarNovos>
           <tem:page>0</tem:page>
        </tem:ListarNovos>
     </soapenv:Body>
  </soapenv:Envelope>


Exemplo de response

.. code-block:: xml

    <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
       <s:Body>
          <ListarNovosResponse xmlns="http://tempuri.org/">
             <ListarNovosResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
                <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
                <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                <a:PageCount>7</a:PageCount>
                <a:PageIndex>0</a:PageIndex>
                <a:PageSize>10</a:PageSize>
                <a:Pedidos>
                   <a:PedidoDTO>
                      <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
                      <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                      <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                      <a:BandeiraDoCartao/>
                      <a:ClienteFinalId i:nil="true"/>
                      <a:DadosAdicionais/>
                      <a:DataCriacao>2017-11-24T18:32:48.193</a:DataCriacao>
                      <a:DescontoPedido>0.0000</a:DescontoPedido>
                      <a:Descontos/>
                      <a:DistributionCentersToChargeSt/>
                      <a:FormaDePagamento>Payments.Faturado</a:FormaDePagamento>
                      <a:FreteTotal>0.0000</a:FreteTotal>
                      <a:Id>556220</a:Id>
                      <a:IdNaRevenda i:nil="true"/>
                      <a:IdPedidoCliente i:nil="true"/>
                      <a:IdPrazoPagamento>5</a:IdPrazoPagamento>
                      <a:IdPrazoPagamentoString>5</a:IdPrazoPagamentoString>
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
                            <a:PartNumber>0010000003135</a:PartNumber>
                            <a:ProdutosExtensoesDeGarantia i:nil="true"/>
                            <a:Quantidade>1</a:Quantidade>
                            <a:Sku>86544</a:Sku>
                            <a:ValorComissao>0</a:ValorComissao>
                            <a:ValorDescontoProduto>0.0000</a:ValorDescontoProduto>
                            <a:ValorTotal>8287.7100</a:ValorTotal>
                            <a:ValorUnitario>8287.7100</a:ValorUnitario>
                         </a:PedidoDTO.PedidoItemDTO>
                      </a:Itens>
                      <a:LicenciadoOpenValueId i:nil="true"/>
                      <a:LinkNotaFiscal i:nil="true"/>
                      <a:NumeroNotaFiscal i:nil="true"/>
                      <a:OrderGuid>b7456cd1-6c6b-49be-a6b1-a679f748658d</a:OrderGuid>
                      <a:PagamentoBNDES i:nil="true"/>
                      <a:RevendaId>72641</a:RevendaId>
                      <a:StTotal>0.0000</a:StTotal>
                      <a:SubTotal>8287.7100</a:SubTotal>
                      <a:TipoVenda>1</a:TipoVenda>
                      <a:Total>8287.7100</a:Total>
                      <a:VendedorErpId i:nil="true"/>
                   </a:PedidoDTO>
                   <a:PedidoDTO>
                      <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
                      <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                      <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                      <a:BandeiraDoCartao/>
                      <a:ClienteFinalId i:nil="true"/>
                      <a:DadosAdicionais/>
                      <a:DataCriacao>2017-11-24T18:36:44.17</a:DataCriacao>
                      <a:DescontoPedido>0.0000</a:DescontoPedido>
                      <a:Descontos/>
                      <a:DistributionCentersToChargeSt/>
                      <a:FormaDePagamento>Payments.Faturado</a:FormaDePagamento>
                      <a:FreteTotal>106.0800</a:FreteTotal>
                      <a:Id>556221</a:Id>
                      <a:IdNaRevenda i:nil="true"/>
                      <a:IdPedidoCliente i:nil="true"/>
                      <a:IdPrazoPagamento>2</a:IdPrazoPagamento>
                      <a:IdPrazoPagamentoString>2</a:IdPrazoPagamentoString>
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
                            <a:PartNumber>0010000000722</a:PartNumber>
                            <a:ProdutosExtensoesDeGarantia i:nil="true"/>
                            <a:Quantidade>1</a:Quantidade>
                            <a:Sku>59569</a:Sku>
                            <a:ValorComissao>0</a:ValorComissao>
                            <a:ValorDescontoProduto>0.0000</a:ValorDescontoProduto>
                            <a:ValorTotal>1052.7000</a:ValorTotal>
                            <a:ValorUnitario>1052.7000</a:ValorUnitario>
                         </a:PedidoDTO.PedidoItemDTO>
                      </a:Itens>
                      <a:LicenciadoOpenValueId i:nil="true"/>
                      <a:LinkNotaFiscal i:nil="true"/>
                      <a:NumeroNotaFiscal i:nil="true"/>
                      <a:OrderGuid>74ab3c6f-53ef-44e3-9b3f-8bf5314db8d3</a:OrderGuid>
                      <a:PagamentoBNDES i:nil="true"/>
                      <a:RevendaId>128372</a:RevendaId>
                      <a:StTotal>0.0000</a:StTotal>
                      <a:SubTotal>1052.7000</a:SubTotal>
                      <a:TipoVenda>1</a:TipoVenda>
                      <a:Total>1158.7800</a:Total>
                      <a:VendedorErpId i:nil="true"/>
                   </a:PedidoDTO>
                   <a:PedidoDTO>
                      <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
                      <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                      <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                      <a:BandeiraDoCartao/>
                      <a:ClienteFinalId i:nil="true"/>
                      <a:DadosAdicionais/>
                      <a:DataCriacao>2018-01-18T15:12:42.247</a:DataCriacao>
                      <a:DescontoPedido>0.0000</a:DescontoPedido>
                      <a:Descontos/>
                      <a:DistributionCentersToChargeSt/>
                      <a:FormaDePagamento>Payments.Faturado</a:FormaDePagamento>
                      <a:FreteTotal>69.1600</a:FreteTotal>
                      <a:Id>556222</a:Id>
                      <a:IdNaRevenda i:nil="true"/>
                      <a:IdPedidoCliente i:nil="true"/>
                      <a:IdPrazoPagamento>8</a:IdPrazoPagamento>
                      <a:IdPrazoPagamentoString>8</a:IdPrazoPagamentoString>
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
                            <a:PartNumber>0100000002876</a:PartNumber>
                            <a:ProdutosExtensoesDeGarantia i:nil="true"/>
                            <a:Quantidade>2</a:Quantidade>
                            <a:Sku>200305</a:Sku>
                            <a:ValorComissao>0</a:ValorComissao>
                            <a:ValorDescontoProduto>0.0000</a:ValorDescontoProduto>
                            <a:ValorTotal>847.0000</a:ValorTotal>
                            <a:ValorUnitario>423.5000</a:ValorUnitario>
                         </a:PedidoDTO.PedidoItemDTO>
                      </a:Itens>
                      <a:LicenciadoOpenValueId i:nil="true"/>
                      <a:LinkNotaFiscal i:nil="true"/>
                      <a:NumeroNotaFiscal i:nil="true"/>
                      <a:OrderGuid>852e98fe-2011-4c08-b1f5-309d2f031fca</a:OrderGuid>
                      <a:PagamentoBNDES i:nil="true"/>
                      <a:RevendaId>120519</a:RevendaId>
                      <a:StTotal>0.0000</a:StTotal>
                      <a:SubTotal>847.0000</a:SubTotal>
                      <a:TipoVenda>1</a:TipoVenda>
                      <a:Total>870.3520</a:Total>
                      <a:VendedorErpId i:nil="true"/>
                   </a:PedidoDTO>
                </a:Pedidos>
             </ListarNovosResult>
          </ListarNovosResponse>
       </s:Body>
    </s:Envelope>
