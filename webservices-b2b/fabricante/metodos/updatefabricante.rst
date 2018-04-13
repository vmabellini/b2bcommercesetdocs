Atualizar fabricante
=======
Atualize um fabricante através do **UpdateFabricante**, sendo que a entidade deve ter o mesmo **ErpId** da a ser atualizada.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - ErpId
     - string
     - Código do fabricante no Erp. **Deve ser único**
   * - Descricao
     - string
     - Descrição do fabricante a ser criado
   * - Nome
     - string
     - Nome do fabricante exibido no Site B2B

Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Fabricantes.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:UpdateFabricante>
           <tem:fabricanteDto>
              <b2b:Descricao>Exemplo de descricao</b2b:Descricao>
              <b2b:ErpId>AAA11111</b2b:ErpId>
              <b2b:Nome>Exemplo de nome de fabricante</b2b:Nome>
              <b2b:OrdemDeExibicao>0</b2b:OrdemDeExibicao>
           </tem:fabricanteDto>
        </tem:UpdateFabricante>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <UpdateFabricanteResponse xmlns="http://tempuri.org/">
           <UpdateFabricanteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </UpdateFabricanteResult>
        </UpdateFabricanteResponse>
     </s:Body>
  </s:Envelope>
