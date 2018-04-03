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

Exemplo de response

.. code-block:: xml

   <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
      <s:Body>
         <GetCategoriaResponse xmlns="http://tempuri.org/">
            <GetCategoriaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Categorias.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
               <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
               <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
               <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
               <a:Categoria>
                  <a:Descricao>Exemplo de descricao</a:Descricao>
                  <a:ErpId>111AAA</a:ErpId>
                  <a:ErpIdPai i:nil="true"/>
                  <a:Nome>Nome da categoria</a:Nome>
                  <a:OrdemDeExibicao>0</a:OrdemDeExibicao>
               </a:Categoria>
            </GetCategoriaResult>
         </GetCategoriaResponse>
      </s:Body>
   </s:Envelope>
