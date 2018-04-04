Desvincular todos os produtos da categoria
=======

Desvincule todos os produtos de uma categoria enviando o **CodigoErpId** da categoria através do **DesvincularTodosDaCategoria**.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:DesvincularTodosDaCategoria>
           <tem:categoriaErpId>000018</tem:categoriaErpId>
        </tem:DesvincularTodosDaCategoria>
     </soapenv:Body>
  </soapenv:Envelope>

  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <DesvincularTodosDaCategoriaResponse xmlns="http://tempuri.org/">
           <DesvincularTodosDaCategoriaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </DesvincularTodosDaCategoriaResult>
        </DesvincularTodosDaCategoriaResponse>
     </s:Body>
  </s:Envelope>
