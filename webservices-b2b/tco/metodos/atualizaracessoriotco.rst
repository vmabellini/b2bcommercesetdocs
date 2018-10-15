Atualizar Acessorio TCO
=======================

Atualiza a relação de um acessório com a impressora TCO

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
   * - Rendimento
     - int
     - Indica o rendimento do Acessorio
   * - ContabilizarPreco
     - bool
     - se enviado 1, indica que o preço do acessorio deve ser levado em consideração no calculo TCO
   * - TipoEquipamento
     - Enumeração
     - Indica o Tipo do acessorio

.. list-table:: Enumeração TipoEquipamento
   :widths: auto
   :header-rows: 1

   * - Valor
   * - TonerPreto
   * - TonerCiano
   * - TonerAmarelo
   * - TonerMagenta
   * - CilindroPreto
   * - CilindroCiano
   * - CilindroAmarelo
   * - CilindroMagenta
   * - ReveladorPreto
   * - ReveladorCiano
   * - ReveladorAmarelo
   * - ReveladorMagenta
   * - Fusor

Exemplo de Request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.TCO.DTO">
    <soapenv:Header/>
    <soapenv:Body>
      <tem:AtualizarAcessorioTco>
        <tem:dto>
          <b2b:AcessorioPartNumber>DFG-321</b2b:AcessorioPartNumber>
          <b2b:ContabilizarPreco>true</b2b:ContabilizarPreco>
          <b2b:ProdutoTcoPartNumber>ABC-123</b2b:ProdutoTcoPartNumber>
          <b2b:Rendimento>3500</b2b:Rendimento>
          <b2b:TipoEquipamento>TonerPreto</b2b:TipoEquipamento>
        </tem:dto>
      </tem:AtualizarAcessorioTco>
    </soapenv:Body>
  </soapenv:Envelope>

Exemplo de Response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Body>
      <AtualizarAcessorioTcoResponse xmlns="http://tempuri.org/">
        <AtualizarAcessorioTcoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
          <a:Error>false</a:Error>
          <a:ErrorType i:nil="true"/>
          <a:Message i:nil="true"/>
        </AtualizarAcessorioTcoResult>
      </AtualizarAcessorioTcoResponse>
    </s:Body>
  </s:Envelope>