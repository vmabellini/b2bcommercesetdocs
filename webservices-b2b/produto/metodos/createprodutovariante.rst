Criar variante de produto 
=======

Para criar um novo variante de produto, através do **CreateProdutoVariante** preencha a entidade abaixo com os dados do variante. Nesse caso, o **PartNumberPai** é o partnumber do produto que o variante será inserido. Ele já deverá estar no B2B.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Nome
     - string
     - Nome do variante de produto
   * - Sku
     - string
     - Sku do variante de produto. **Deve ser único**
   * - PartNumberPai
     - string
     - Partnumber do produto que receberá o variante. **Deve ser único**
   * - NomeSku
     - string
     - Nome completo do Sku do variante de produto.
   * - DistributionCenterPrefix
     - string
     - Prefixo do centro de distribuição que o variante será atrelado (Exemplo: SP)
   * - Altura
     - decimal
     - Altura do variante de produto
   * - Largura
     - decimal
     - Largura do variante de produto
   * - Profundidade
     - decimal
     - Profundidade do variante de produto
   * - Peso
     - decimal
     - Peso do variante de produto
   * - Espencificacoes
     - string
     - Descrição das especificações do variante de produto 

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:CreateProdutoVariante>
           <tem:produtoVarianteDto>
              <b2b:Altura>10</b2b:Altura>
              <b2b:DistributionCenterPrefix>SP</b2b:DistributionCenterPrefix>
              <b2b:Especificacoes>Exemplo de especificações</b2b:Especificacoes>
              <b2b:Largura>100</b2b:Largura>
              <b2b:Nome>Exemplo de Variante</b2b:Nome>
              <b2b:NomeSku>Exemplo de nome de SKU</b2b:NomeSku>
              <b2b:PartNumberPai>AAA-12345</b2b:PartNumberPai>
              <b2b:Peso>100</b2b:Peso>
              <b2b:Profundidade>100</b2b:Profundidade>
              <b2b:Sku>SKU-12345</b2b:Sku>
           </tem:produtoVarianteDto>
        </tem:CreateProdutoVariante>
     </soapenv:Body>
  </soapenv:Envelope>
  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <CreateProdutoVarianteResponse xmlns="http://tempuri.org/">
           <CreateProdutoVarianteResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </CreateProdutoVarianteResult>
        </CreateProdutoVarianteResponse>
     </s:Body>
  </s:Envelope>
