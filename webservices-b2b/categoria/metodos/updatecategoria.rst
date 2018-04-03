Atualizar categoria
=======
Atualize uma categoria através do **UpdateCategoria**, sendo que a entidade deve ter o mesmo **ErpId** da a ser atualizada.

Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" 
   xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Categorias.DTO">
      <soapenv:Header/>
      <soapenv:Body>
         <tem:UpdateCategoria>
            <tem:categoriaDto>
               <b2b:Descricao>Exemplo de descrição</b2b:Descricao>
               <b2b:ErpId>111AAA</b2b:ErpId>
               <b2b:ErpIdPai>123ABC</b2b:ErpIdPai>
               <b2b:Nome>Exemplo de nome</b2b:Nome>
               <b2b:OrdemDeExibicao>0</b2b:OrdemDeExibicao>
            </tem:categoriaDto>
         </tem:UpdateCategoria>
      </soapenv:Body>
   </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

   <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
      <s:Body>
         <UpdateCategoriaResponse xmlns="http://tempuri.org/">
            <UpdateCategoriaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
               <a:Error>false</a:Error>
               <a:ErrorType i:nil="true"/>
               <a:Message i:nil="true"/>
            </UpdateCategoriaResult>
         </UpdateCategoriaResponse>
      </s:Body>
   </s:Envelope>
