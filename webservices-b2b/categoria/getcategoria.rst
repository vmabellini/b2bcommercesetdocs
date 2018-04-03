Obter categoria
=======
Para obter uma categoria em específico, busque através do **GetCategoria** preenchendo com o **ErpId** de uma categoria que já esteja no B2B.

Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
      <soapenv:Header/>
      <soapenv:Body>
         <tem:GetCategoria>
            <tem:erpId>111AAA</tem:erpId>
         </tem:GetCategoria>
      </soapenv:Body>
   </soapenv:Envelope>
