Obter Acessorio TCO
===================

Retorna o acessorio relacionado com a impressora informada

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - ProdutoTcoPartNumber
     - string
     - Part Number da Impressora TCO
   * - AcessorioPartNumber
     - string
     - Part Number do Acessorio

Exemplo de Request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.TCO.DTO">
    <soapenv:Header/>
    <soapenv:Body>
      <tem:ObterAcessorioTco>
        <tem:dto>
          <b2b:AcessorioPartNumber>DFG-321</b2b:AcessorioPartNumber>
          <b2b:ProdutoTcoPartNumber>ABC-123</b2b:ProdutoTcoPartNumber>
        </tem:dto>
      </tem:ObterAcessorioTco>
    </soapenv:Body>
  </soapenv:Envelope>

Exemplo de Response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Body>
      <ObterAcessorioTcoResponse xmlns="http://tempuri.org/">
        <ObterAcessorioTcoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.TCO.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
          <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
          <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
          <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
          <a:AcessorioPartNumber>Z8Z17A-I</a:AcessorioPartNumber>
          <a:ContabilizarPreco>true</a:ContabilizarPreco>
          <a:ProdutoTcoPartNumber>W9050MC-I</a:ProdutoTcoPartNumber>
          <a:Rendimento>3500</a:Rendimento>
          <a:TipoEquipamento>TonerPreto</a:TipoEquipamento>
        </ObterAcessorioTcoResult>
      </ObterAcessorioTcoResponse>
    </s:Body>
  </s:Envelope>