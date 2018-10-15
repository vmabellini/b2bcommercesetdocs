Salvar Caracteristicas Impressora TCO
=====================================

Salva as caracteristicas da Impressora TCO para auxiliar o B2B na recomendação de impressoras no projeto TCO.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - PartNumber
     - string
     - Part Number da Impressora TCO
   * - TipoImpressora
     - Enumeração - Mono ou Color
     - Indica se a impressora é Mono ou Color
   * - VelocidadeImpressao
     - Enumeração
     - Indica o intervalo da velocidade de impressão
   * - Categoria
     - Enumeração - Impressora ou Multifuncional
     - Indica se é Impressora ou Multifuncional

.. list-table:: Enumeração VelocidadeImpressao
   :widths: auto
   :header-rows: 1

   * - Valor
   * - Ate29PPM
   * - Ate39PPM
   * - Ate49PPM
   * - Ate59PPM
   * - AcimaDe60PPM

Exemplo de Request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.TCO.DTO">
    <soapenv:Header/>
    <soapenv:Body>
        <tem:SalvarCaracteristicasImpressoraTco>
          <tem:dto>
            <b2b:Categoria>Multifuncional</b2b:Categoria>
            <b2b:PartNumber>ABC-123</b2b:PartNumber>
            <b2b:TipoImpressora>Color</b2b:TipoImpressora>
            <b2b:VelocidadeImpressao>Ate49PPM</b2b:VelocidadeImpressao>
          </tem:dto>
        </tem:SalvarCaracteristicasImpressoraTco>
    </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Body>
        <SalvarCaracteristicasImpressoraTcoResponse xmlns="http://tempuri.org/">
          <SalvarCaracteristicasImpressoraTcoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
          </SalvarCaracteristicasImpressoraTcoResult>
        </SalvarCaracteristicasImpressoraTcoResponse>
    </s:Body>
  </s:Envelope>