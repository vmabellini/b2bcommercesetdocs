Obter fabricante
=======
Para obter um fabricante em específico, busque através do **GetFabricante** preenchendo com o **ErpId** de um fabricante que já esteja no B2B.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:GetFabricante>
           <tem:erpId>AAA11111</tem:erpId>
        </tem:GetFabricante>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <GetFabricanteResponse xmlns="http://tempuri.org/">
           <GetFabricanteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Fabricantes.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:Fabricante>
                 <a:Descricao>Exemplo de descricao</a:Descricao>
                 <a:ErpId>AAA11111</a:ErpId>
                 <a:Nome>Exemplo de nome de fabricante</a:Nome>
                 <a:OrdemDeExibicao>0</a:OrdemDeExibicao>
              </a:Fabricante>
           </GetFabricanteResult>
        </GetFabricanteResponse>
     </s:Body>
  </s:Envelope>
