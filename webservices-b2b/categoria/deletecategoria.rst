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