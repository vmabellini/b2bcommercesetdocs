Criar produto
=======

Crie um produto através do **CreateProduto** enviando a entidade que tenha um **PartNumber** único. 

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:CreateProduto>
           <!--Optional:-->
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
              <b2b:ShowOnHomePage>1</b2b:ShowOnHomePage>
           </tem:produtoDto>
        </tem:CreateProduto>
     </soapenv:Body>
  </soapenv:Envelope>

  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <CreateProdutoResponse xmlns="http://tempuri.org/">
           <CreateProdutoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </CreateProdutoResult>
        </CreateProdutoResponse>
     </s:Body>
  </s:Envelope>
