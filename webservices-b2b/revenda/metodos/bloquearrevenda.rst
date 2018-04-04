Bloquear revenda
=======
Para desativar/bloquear uma revenda do B2B, através do **BloquearRevenda** envie o Id da revenda.
     
Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:BloquearRevenda>
           <tem:revendaId>123</tem:revendaId>
        </tem:BloquearRevenda>
     </soapenv:Body>
  </soapenv:Envelope>
  
  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <BloquearRevendaResponse xmlns="http://tempuri.org/">
           <BloquearRevendaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </BloquearRevendaResult>
        </BloquearRevendaResponse>
     </s:Body>
  </s:Envelope>
