Deletar variante de produto
=======
Para deletar um variante de produto, envie através do **DeleteProdutoVariante** apenas o parâmetro **Sku**. 

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:DeleteProdutoVariante>
           <tem:sku>SKU-12345</tem:sku>
        </tem:DeleteProdutoVariante>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <DeleteProdutoVarianteResponse xmlns="http://tempuri.org/">
           <DeleteProdutoVarianteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </DeleteProdutoVarianteResult>
        </DeleteProdutoVarianteResponse>
     </s:Body>
  </s:Envelope>
