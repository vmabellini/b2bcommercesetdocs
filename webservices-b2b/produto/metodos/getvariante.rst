Obter variante de produto
=======

Para obter detalhes de um varitante de produto inserido no B2B, através do **GetVariante** preencha a requisição com o **Sku** que deseja encontrar.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:GetVariante>
           <tem:sku>SKU-12345</tem:sku>
        </tem:GetVariante>
     </soapenv:Body>
  </soapenv:Envelope>

  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <GetVarianteResponse xmlns="http://tempuri.org/">
           <GetVarianteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:Variante>
                 <a:Altura>0</a:Altura>
                 <a:DistributionCenterPrefix>SP</a:DistributionCenterPrefix>
                 <a:Especificacoes i:nil="true"/>
                 <a:Largura>0</a:Largura>
                 <a:Nome>Exemplo de Variante</a:Nome>
                 <a:NomeSku>Exemplo de nome de SKU</a:NomeSku>
                 <a:PartNumberPai>AAA-12345</a:PartNumberPai>
                 <a:PermiteEncomenda>false</a:PermiteEncomenda>
                 <a:PermiteNecessidade>false</a:PermiteNecessidade>
                 <a:Peso>0</a:Peso>
                 <a:Profundidade>0</a:Profundidade>
                 <a:Sku>SKU-12345</a:Sku>
              </a:Variante>
           </GetVarianteResult>
        </GetVarianteResponse>
     </s:Body>
  </s:Envelope>
