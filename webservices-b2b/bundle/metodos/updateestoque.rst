
Atualizar estoque 
=======

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Bundles.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:UpdateEstoque>
           <tem:estoqueDTO>
              <b2b:ErpId>132465789</b2b:ErpId>
              <b2b:NovoEstoque>18</b2b:NovoEstoque>
           </tem:estoqueDTO>
        </tem:UpdateEstoque>
     </soapenv:Body>
  </soapenv:Envelope>
   
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <UpdateEstoqueResponse xmlns="http://tempuri.org/">
           <UpdateEstoqueResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </UpdateEstoqueResult>
        </UpdateEstoqueResponse>
     </s:Body>
  </s:Envelope>
