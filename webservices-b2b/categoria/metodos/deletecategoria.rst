Deletar categoria
=======
Para deletar uma categoria, envie através do **DeleteCategoria** apenas o parâmetro **ErpId**. 

Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
      <soapenv:Header/>
      <soapenv:Body>
         <tem:DeleteCategoria>
            <tem:erpId>111AAA</tem:erpId>
         </tem:DeleteCategoria>
      </soapenv:Body>
   </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

   <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
      <s:Body>
         <DeleteCategoriaResponse xmlns="http://tempuri.org/">
            <DeleteCategoriaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
               <a:Error>false</a:Error>
               <a:ErrorType i:nil="true"/>
               <a:Message i:nil="true"/>
            </DeleteCategoriaResult>
         </DeleteCategoriaResponse>
      </s:Body>
   </s:Envelope>
