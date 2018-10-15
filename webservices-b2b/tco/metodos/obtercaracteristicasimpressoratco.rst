Obter Caracteristicas Impressora TCO
====================================

Para obter as caracteristicas da Impressora TCO através do **ObterCaracteristicasImpressoraTco** preencha a requisição com o **PartNumber** que deseja encontrar.

Exemplo de Request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
    <soapenv:Header/>
    <soapenv:Body>
      <tem:ObterCaracteristicasImpressoraTco>
        <tem:partNumber>ABC-123</tem:partNumber>
      </tem:ObterCaracteristicasImpressoraTco>
    </soapenv:Body>
  </soapenv:Envelope>

Exemplo de Response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Body>
      <ObterCaracteristicasImpressoraTcoResponse xmlns="http://tempuri.org/">
        <ObterCaracteristicasImpressoraTcoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.TCO.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
          <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
          <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
          <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
          <a:Categoria>Multifuncional</a:Categoria>
          <a:PartNumber>Z8Z17A-I</a:PartNumber>
          <a:TipoImpressora>Color</a:TipoImpressora>
          <a:VelocidadeImpressao>Ate49PPM</a:VelocidadeImpressao>
        </ObterCaracteristicasImpressoraTcoResult>
      </ObterCaracteristicasImpressoraTcoResponse>
    </s:Body>
  </s:Envelope>