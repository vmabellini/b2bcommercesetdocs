Obter id de revendas pelo email de usuário
=======
Obtenha o id das revendas atreladas a um usuário **GetRevendaIdsByEmailUsuario** enviando o seu email.
     
Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
   <soapenv:Header/>
   <soapenv:Body>
      <tem:GetRevendaIdsByEmailUsuario>
         <!--Optional:-->
         <tem:emailUsuario>teste@atma-it.com</tem:emailUsuario>
      </tem:GetRevendaIdsByEmailUsuario>
   </soapenv:Body>
  </soapenv:Envelope>
  
  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <GetRevendaIdsByEmailUsuarioResponse xmlns="http://tempuri.org/">
         <GetRevendaIdsByEmailUsuarioResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Revendas.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
            <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
            <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
            <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
            <a:RevendaIds xmlns:b="http://schemas.datacontract.org/2004/07/System">
               <b:int>4</b:int>
               <b:int>1</b:int>
            </a:RevendaIds>
         </GetRevendaIdsByEmailUsuarioResult>
      </GetRevendaIdsByEmailUsuarioResponse>
   </s:Body>
  </s:Envelope>
