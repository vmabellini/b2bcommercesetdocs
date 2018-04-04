Deletar produto
=======
Para deletar um produto, envie através do **DeleteProduto** apenas o parâmetro **PartNumber**. 

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:DeleteProduto>
           <tem:partNumber>AAA-12345</tem:partNumber>
        </tem:DeleteProduto>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <DeleteProdutoResponse xmlns="http://tempuri.org/">
           <DeleteProdutoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </DeleteProdutoResult>
        </DeleteProdutoResponse>
     </s:Body>
  </s:Envelope>
