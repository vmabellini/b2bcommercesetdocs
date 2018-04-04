Alterar disponibilidade do variante de produto
=======

O variante de produto pode ser publicada ou despublicada através do **AlterarDisponibilidadeDoVariante**, preenchendo o **Sku** do produto e o **Publicado** com 0 para indisponível, 1 para disponível.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Sku
     - string
     - Sku do variante de produto. **Deve ser único**
   * - Publicado
     - bool
     - Novo status do variante de produto

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:AlterarDisponibilidadeDoVariante>
           <tem:alterarDisponibilidadeDto>
              <b2b:Publicado>1</b2b:Publicado>
              <b2b:Sku>SKU-12345</b2b:Sku>
           </tem:alterarDisponibilidadeDto>
        </tem:AlterarDisponibilidadeDoVariante>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <AlterarDisponibilidadeDoVarianteResponse xmlns="http://tempuri.org/">
           <AlterarDisponibilidadeDoVarianteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </AlterarDisponibilidadeDoVarianteResult>
        </AlterarDisponibilidadeDoVarianteResponse>
     </s:Body>
  </s:Envelope>
