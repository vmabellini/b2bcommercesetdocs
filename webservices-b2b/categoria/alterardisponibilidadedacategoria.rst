Alterar disponibilidade da categoria
=======
A categoria pode ser publicada ou despublicada através do **AlterarDisponibilidadeDaCategoria**, preenchendo o **ErpId** da categoria e o **Publicado** com 0 para indisponível, 1 para disponível.

Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/"
   xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Categorias.DTO">
      <soapenv:Header/>
      <soapenv:Body>
         <tem:AlterarDisponibilidadeDaCategoria>
            <tem:alterarDisponibilidadeDto>
               <b2b:ErpId>111AAA</b2b:ErpId>
               <b2b:Publicado>1</b2b:Publicado>
            </tem:alterarDisponibilidadeDto>
         </tem:AlterarDisponibilidadeDaCategoria>
      </soapenv:Body>
   </soapenv:Envelope>