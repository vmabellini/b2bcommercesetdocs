Desbloquear revenda
=======
Para reativar/desbloquear uma revenda do B2B, através do **DesbloquearRevenda** envie o Id da revenda.
     
Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:DesbloquearRevenda>
           <tem:revendaId>123</tem:revendaId>
        </tem:DesbloquearRevenda>
     </soapenv:Body>
  </soapenv:Envelope>
  
  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <DesbloquearRevendaResponse xmlns="http://tempuri.org/">
           <DesbloquearRevendaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </DesbloquearRevendaResult>
        </DesbloquearRevendaResponse>
     </s:Body>
  </s:Envelope>
