Obter produto
=======

Para obter detalhes de um produto inserido no B2B, através do **GetProduto** preencha a requisição com o **PartNumber** que deseja encontrar.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:GetProduto>
           <tem:partNumber>AAA-12345</tem:partNumber>
        </tem:GetProduto>
     </soapenv:Body>
  </soapenv:Envelope>

  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <GetProdutoResponse xmlns="http://tempuri.org/">
           <GetProdutoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:Produto>
                 <a:Altura>10</a:Altura>
                 <a:Ativo>true</a:Ativo>
                 <a:Atributos>
                    <a:ProdutoAtributoDTO>
                       <a:NomeDoAtributo>Exemplo de atributo</a:NomeDoAtributo>
                       <a:Valor>Exemplo de valor de atributo</a:Valor>
                    </a:ProdutoAtributoDTO>
                 </a:Atributos>
                 <a:AtributosDoSistema>
                    <a:ProdutoAtributoDTO>
                       <a:NomeDoAtributo>system_Exemplo de atributo do sistema</a:NomeDoAtributo>
                       <a:Valor>Exemplo de valor de atributo do sistema</a:Valor>
                    </a:ProdutoAtributoDTO>
                 </a:AtributosDoSistema>
                 <a:CodigoERP>1324</a:CodigoERP>
                 <a:CodigoFiscal>1324</a:CodigoFiscal>
                 <a:DescricaoCompleta>Exemplo de descrição completa</a:DescricaoCompleta>
                 <a:DescricaoCurta>Exemplo de descrição curta</a:DescricaoCurta>
                 <a:EAN>AAABBBB</a:EAN>
                 <a:ESD>false</a:ESD>
                 <a:ExtensaoDeGarantia>false</a:ExtensaoDeGarantia>
                 <a:FabricanteErpId>014</a:FabricanteErpId>
                 <a:Largura>0</a:Largura>
                 <a:Nome>Exemplo de produto</a:Nome>
                 <a:OpenValue>false</a:OpenValue>
                 <a:PartNumber>AAA-12345</a:PartNumber>
                 <a:Peso>10</a:Peso>
                 <a:PossuiMP>false</a:PossuiMP>
                 <a:Profundidade>2</a:Profundidade>
                 <a:Promocao i:nil="true"/>
                 <a:ShowOnHomePage i:nil="true"/>
                 <a:SoftwareLicenca i:nil="true"/>
                 <a:StockReserveHours i:nil="true"/>
              </a:Produto>
           </GetProdutoResult>
        </GetProdutoResponse>
     </s:Body>
  </s:Envelope>
