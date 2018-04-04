Alterar disponibilidade do  produto
=======

O produto pode ser publicada ou despublicada através do **AlterarDisponibilidadeDoProduto**, preenchendo o **PartNumber** do produto e o **Publicado** com 0 para indisponível, 1 para disponível.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - PartNumber
     - string
     - Partnumber do produto. **Deve ser único**
   * - Publicado
     - bool
     - Novo status do produto

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:AlterarDisponibilidadeDoProduto>
           <tem:alterarDisponibilidadeDto>
              <b2b:PartNumber>AAA-12345</b2b:PartNumber>
              <b2b:Publicado>1</b2b:Publicado>
           </tem:alterarDisponibilidadeDto>
        </tem:AlterarDisponibilidadeDoProduto>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <AlterarDisponibilidadeDoProdutoResponse xmlns="http://tempuri.org/">
           <AlterarDisponibilidadeDoProdutoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </AlterarDisponibilidadeDoProdutoResult>
        </AlterarDisponibilidadeDoProdutoResponse>
     </s:Body>
  </s:Envelope>
