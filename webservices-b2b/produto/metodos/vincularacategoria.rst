Vincular categoria ao produto
=======

Para adicionar uma categoria a um produto, ela deve ser vinculada a ele através do **VincularACategoria**. Envie a requisição com o **PartNumber** do produto e o **CódigoErpId** da categoria.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:VincularACategoria>
           <tem:partNumber>AAA-12345</tem:partNumber>
           <tem:categoriaErpId>000018</tem:categoriaErpId>
        </tem:VincularACategoria>
     </soapenv:Body>
  </soapenv:Envelope>
  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <VincularACategoriaResponse xmlns="http://tempuri.org/">
           <VincularACategoriaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </VincularACategoriaResult>
        </VincularACategoriaResponse>
     </s:Body>
  </s:Envelope>
