Deletar bundle 
=======

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:DeleteBundle>
           <tem:erpId>132465789</tem:erpId>
        </tem:DeleteBundle>
     </soapenv:Body>
  </soapenv:Envelope>
   
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <DeleteBundleResponse xmlns="http://tempuri.org/">
           <DeleteBundleResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </DeleteBundleResult>
        </DeleteBundleResponse>
     </s:Body>
  </s:Envelope>
   
