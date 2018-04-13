Criar fabricante 
=======
Para criar um fabricante, deve ser enviada através do **CreateFabricante** a entidade com seus atributos preenchidos. 

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
        <tem:CreateFabricante>
           <tem:fabricanteDto>
              <b2b:Descricao>Exemplo de descricao</b2b:Descricao>
              <b2b:ErpId>AAA11111</b2b:ErpId>
              <b2b:Nome>Exemplo de nome</b2b:Nome>
              <b2b:OrdemDeExibicao>0</b2b:OrdemDeExibicao>
           </tem:fabricanteDto>
        </tem:CreateFabricante>
     </soapenv:Body>
  </soapenv:Envelope>
   
Exemplo de response

.. code-block:: xml

   <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <CreateFabricanteResponse xmlns="http://tempuri.org/">
           <CreateFabricanteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </CreateFabricanteResult>
        </CreateFabricanteResponse>
     </s:Body>
  </s:Envelope>
   
