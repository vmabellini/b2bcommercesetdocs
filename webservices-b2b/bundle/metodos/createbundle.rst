
Criar bundle 
=======

Exemplo de request

.. code-block:: xml

     <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Bundles.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:CreateBundle>
           <tem:bundle>
              <b2b:DescontoPorVariante>1</b2b:DescontoPorVariante>
              <b2b:ErpId>132465789</b2b:ErpId>
              <b2b:Estoque>10</b2b:Estoque>
              <b2b:GerenciarEstoque>1</b2b:GerenciarEstoque>
              <b2b:Habilitado>1</b2b:Habilitado>
              <b2b:Nome>Bundle Teste</b2b:Nome>
              <b2b:PorcentagemDeDesconto>10</b2b:PorcentagemDeDesconto>
              <b2b:ValorDeDesconto>0</b2b:ValorDeDesconto>
              <b2b:Variantes>
                 <b2b:BundleVariantDTO>
                    <b2b:MostrarNoDetalheDoProduto>1</b2b:MostrarNoDetalheDoProduto>
                    <b2b:PorcentagemDeDesconto>15</b2b:PorcentagemDeDesconto>
                    <b2b:Quantidade>2</b2b:Quantidade>
                    <b2b:Sku>123546</b2b:Sku>
                    <b2b:ValorDeDesconto>0</b2b:ValorDeDesconto>
                 </b2b:BundleVariantDTO>
                 <b2b:BundleVariantDTO>
                    <b2b:MostrarNoDetalheDoProduto>1</b2b:MostrarNoDetalheDoProduto>
                    <b2b:PorcentagemDeDesconto>0</b2b:PorcentagemDeDesconto>
                    <b2b:Quantidade>6</b2b:Quantidade>
                    <b2b:Sku>123465</b2b:Sku>
                    <b2b:ValorDeDesconto>10</b2b:ValorDeDesconto>
                 </b2b:BundleVariantDTO>
              </b2b:Variantes>
           </tem:bundle>
        </tem:CreateBundle>
     </soapenv:Body>
  </soapenv:Envelope>
   
Exemplo de response

.. code-block:: xml

    <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <CreateBundleResponse xmlns="http://tempuri.org/">
           <CreateBundleResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </CreateBundleResult>
        </CreateBundleResponse>
     </s:Body>
  </s:Envelope>
   
