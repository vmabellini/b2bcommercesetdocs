Obter revenda
=======
Obtenha todas as informações de uma Revenda através do **ObterRevenda** enviando o seu Id.
     
Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:GetRevenda>
           <tem:revendaId>123</tem:revendaId>
        </tem:GetRevenda>
     </soapenv:Body>
  </soapenv:Envelope>
  
  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <GetRevendaResponse xmlns="http://tempuri.org/">
           <GetRevendaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Revendas.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:Revenda>
                 <a:Ativo>false</a:Ativo>
                 <a:Atributos/>
                 <a:ClienteCorporativo>false</a:ClienteCorporativo>
                 <a:Cnpj>02353900000148</a:Cnpj>
                 <a:Contribuinte>false</a:Contribuinte>
                 <a:DataFundacao>2017-12-08T13:55:00</a:DataFundacao>
                 <a:Email>re@fs.com</a:Email>
                 <a:EmailFinanceiro i:nil="true"/>
                 <a:Fantasia>ytr</a:Fantasia>
                 <a:Grupo>ytr</a:Grupo>
                 <a:Id>123</a:Id>
                 <a:InscricaoEstadual>65</a:InscricaoEstadual>
                 <a:InscricaoMunicipal>6</a:InscricaoMunicipal>
                 <a:InscricaoRural i:nil="true"/>
                 <a:InscricaoSuframa i:nil="true"/>
                 <a:Observacao>654</a:Observacao>
                 <a:OrigemId>4</a:OrigemId>
                 <a:Pendencia>false</a:Pendencia>
                 <a:Perfil>Nenhum</a:Perfil>
                 <a:RamoAtividadeId>8</a:RamoAtividadeId>
                 <a:RazaoSocial>tre</a:RazaoSocial>
                 <a:Segmento i:nil="true"/>
                 <a:SetorId i:nil="true"/>
                 <a:SituacaoId i:nil="true"/>
                 <a:Suframa i:nil="true"/>
                 <a:Tipo i:nil="true"/>
                 <a:VendedorErpId i:nil="true"/>
                 <a:VendedorResponsavelEmail i:nil="true"/>
                 <a:Website i:nil="true"/>
              </a:Revenda>
           </GetRevendaResult>
        </GetRevendaResponse>
     </s:Body>
  </s:Envelope>
