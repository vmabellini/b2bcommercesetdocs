Obter bundle 
=======

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:GetBundle>
           <tem:erpId>132465789</tem:erpId>
        </tem:GetBundle>
     </soapenv:Body>
  </soapenv:Envelope>
   
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <GetBundleResponse xmlns="http://tempuri.org/">
           <GetBundleResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Bundles.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:Bundle>
                 <a:DescontoPorVariante>true</a:DescontoPorVariante>
                 <a:ErpId>132465789</a:ErpId>
                 <a:Estoque>10</a:Estoque>
                 <a:GerenciarEstoque>true</a:GerenciarEstoque>
                 <a:Habilitado>true</a:Habilitado>
                 <a:Nome>Bundle Teste Atualizado</a:Nome>
                 <a:PorcentagemDeDesconto>10.0000</a:PorcentagemDeDesconto>
                 <a:ValorDeDesconto i:nil="true"/>
                 <a:Variantes>
                    <a:BundleVariantDTO>
                       <a:MostrarNoDetalheDoProduto>true</a:MostrarNoDetalheDoProduto>
                       <a:PorcentagemDeDesconto>15.00</a:PorcentagemDeDesconto>
                       <a:Quantidade>2</a:Quantidade>
                       <a:Sku>OF01_CT01_DVEN_ZNORM1H_000000000001028164</a:Sku>
                       <a:ValorDeDesconto>0.00</a:ValorDeDesconto>
                    </a:BundleVariantDTO>
                    <a:BundleVariantDTO>
                       <a:MostrarNoDetalheDoProduto>true</a:MostrarNoDetalheDoProduto>
                       <a:PorcentagemDeDesconto>0.00</a:PorcentagemDeDesconto>
                       <a:Quantidade>6</a:Quantidade>
                       <a:Sku>OF01_CJ01_DVEN_ZNORM1H_000000000001026511</a:Sku>
                       <a:ValorDeDesconto>10.00</a:ValorDeDesconto>
                    </a:BundleVariantDTO>
                 </a:Variantes>
              </a:Bundle>
           </GetBundleResult>
        </GetBundleResponse>
     </s:Body>
  </s:Envelope>
   
