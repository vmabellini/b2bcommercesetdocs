Deletar fabricante
=======
Para deletar um fabricante, envie através do **DeleteFabricante** apenas o parâmetro **ErpId**. 

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:DeleteFabricante>
           <tem:erpId>AAA11111</tem:erpId>
        </tem:DeleteFabricante>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <DeleteFabricanteResponse xmlns="http://tempuri.org/">
           <DeleteFabricanteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </DeleteFabricanteResult>
        </DeleteFabricanteResponse>
     </s:Body>
  </s:Envelope>
