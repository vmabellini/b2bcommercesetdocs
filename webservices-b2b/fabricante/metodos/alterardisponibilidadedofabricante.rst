Alterar disponibilidade do fabricante
=======
O fabricante pode ser publicado ou despublicado através do **AlterarDisponibilidadeDoFabricante**, preenchendo o **ErpId** do fabricante e o **Publicado** com 0 para indisponível, 1 para disponível.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Fabricantes.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:AlterarDisponibilidadeDoFabricante>
           <tem:alterarDisponibilidadeDto>
              <b2b:ErpId>AAA11111</b2b:ErpId>
              <b2b:Publicado>0</b2b:Publicado>
           </tem:alterarDisponibilidadeDto>
        </tem:AlterarDisponibilidadeDoFabricante>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <AlterarDisponibilidadeDoFabricanteResponse xmlns="http://tempuri.org/">
           <AlterarDisponibilidadeDoFabricanteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </AlterarDisponibilidadeDoFabricanteResult>
        </AlterarDisponibilidadeDoFabricanteResponse>
     </s:Body>
  </s:Envelope>
