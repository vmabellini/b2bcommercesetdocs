Atualizar produto
=======

Atualize um produto através do **UpdateProduto** enviando a entidade que tenha um **PartNumber** já inserido no B2B. 

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - PartNumber
     - string
     - Código do produto no ERP. **Deve ser único.** 

       Além de servirem como chave primária, os Part Numbers são propriedades importantes para a busca de produtos pois muitos vendedores utilizam esse código para localizar os produtos.
   * - Nome
     - string(400)
     - Nome do produto. É o principal campo de busca além do Part Number, portanto deve ser bastante claro e amigável ao usuário.
   * - Ativo
     - bool
     - Indica se o produto está ativo no site. Produtos inativos não ficam visíveis na busca, nas vitrines e nem permitem a compra.
   * - DescricaoCurta
     - string
     - Descrição curta do produto. Apenas texto sem formatação.
   * - DescricaoCompleta
     - string
     - Descrição completa do produto. Conteúdo pode ser enviado com formatação HTML, permitindo a inclusão de imagens, vídeos e links para deixar a página bastante completa.
   * - FabricanteErpId
     - string
     - ErpId do fabricante do produto. Todo produto precisa ter um fabricante vinculado.
   * - CategoriaErpIds
     - string
     - ErpId das categorias do produto. Um produto pode estar vinculado a mais de uma categoria ao mesmo tempo.
   * - Altura
     - decimal
     - Altura do produto.
   * - Peso
     - decimal
     - Peso do produto.
   * - Profundidade
     - decimal
     - Profundidade do produto.
   * - Largura
     - decimal
     - Largura do produto.
   * - EAN
     - string
     - Campo aberto para poissível EAN.
   * - CodigoErp
     - int
     - Campo aberto para poissível código do Erp.
   * - CodigoFiscal
     - int
     - Campo aberto para poissível código fiscal do Erp.
   * - ExtensaoDeGarantia
     - bool
     - 0 para não ser extensao de garantia, 1 para ser.
   * - Atributos
     - Lista de ProdutoAtributoDTO
     - Lista com os atributos do produto
   * - AtributosDoSistema
     - Lista de ProdutoAtributoDTO
     - Lista com os atributos do sistema do produto
   * - IsTCO
     - bool
     - 0 para não ser um produto TCO, 1 para ser.
   * - RelatedPartnumbers
     - List<RelatedPartNumber>
     - Partnumbers relacionados a esse produto. Pode ser usado em algumas configurações do site.
   * - ContextoBundle
     - Opções: Normal, SomenteBundleEVisivelNoSite, SomenteBundleEOcultoNoSite
     - Permite que um produto seja vendido somente como bundle

       Produtos somente bundle não podem ser vendidos a não ser que estejam dentro de um bundle
       Duas opções distintas: o produto pode aparecer na busca e vitrine no site, ou completamente oculto

.. list-table:: Propriedades do ProdutoAtributoDTO
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - NomeDoAtributo
     - string
     - Nome do atributo 
   * - Valor
     - string
     - Valor do atributo 

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:UpdateProduto>
           <tem:produtoDto>
              <b2b:Altura>10</b2b:Altura>
              <b2b:Ativo>1</b2b:Ativo>
              <b2b:Atributos>
                 <b2b:ProdutoAtributoDTO>
                    <b2b:NomeDoAtributo>Exemplo de atributo</b2b:NomeDoAtributo>
                    <b2b:Valor>Exemplo de valor de atributo</b2b:Valor>
                 </b2b:ProdutoAtributoDTO>
              </b2b:Atributos>
              <b2b:AtributosDoSistema>
                 <b2b:ProdutoAtributoDTO>
                    <b2b:NomeDoAtributo>Exemplo de atributo do sistema</b2b:NomeDoAtributo>
                    <b2b:Valor>Exemplo de valor de atributo do sistema</b2b:Valor>
                 </b2b:ProdutoAtributoDTO>
              </b2b:AtributosDoSistema>
              <b2b:CodigoERP>1324</b2b:CodigoERP>
              <b2b:CodigoFiscal>1324</b2b:CodigoFiscal>
              <b2b:DescricaoCompleta>Exemplo de descrição completa</b2b:DescricaoCompleta>
              <b2b:DescricaoCurta>Exemplo de descrição curta</b2b:DescricaoCurta>
              <b2b:EAN>AAABBBB</b2b:EAN>
              <b2b:ExtensaoDeGarantia>0</b2b:ExtensaoDeGarantia>
              <b2b:FabricanteErpId>014</b2b:FabricanteErpId>
              <b2b:Largura>0</b2b:Largura>
              <b2b:Nome>Exemplo de produto</b2b:Nome>
              <b2b:PartNumber>AAA-12345</b2b:PartNumber>
              <b2b:Peso>10</b2b:Peso>
              <b2b:Profundidade>2</b2b:Profundidade>
              <b2b:RelatedPartnumbers>
                <b2b:RelatedPartnumber>
                  <b2b:Partnumber>123456</b2b:Partnumber>
                  </b2b:RelatedPartnumber>
                  <b2b:RelatedPartnumber>
                     <b2b:Partnumber>654321</b2b:Partnumber>
                  </b2b:RelatedPartnumber>
               </b2b:RelatedPartnumbers>
                 <b2b:ShowOnHomePage>1</b2b:ShowOnHomePage>
              </tem:produtoDto>
           </tem:UpdateProduto>
        </soapenv:Body>
     </soapenv:Envelope>

  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <UpdateProdutoResponse xmlns="http://tempuri.org/">
           <UpdateProdutoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </UpdateProdutoResult>
        </UpdateProdutoResponse>
     </s:Body>
  </s:Envelope>
