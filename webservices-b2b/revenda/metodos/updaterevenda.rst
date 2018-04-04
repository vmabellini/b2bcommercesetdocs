Atualizar revenda
=======

Atualize uma revenda através do **UpdateRevenda** enviando a entidade da revenda (sem os endereços) e tendo o mesmo Id da a ser atualizada.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Id
     - int
     - Código da revenda no Erp. **Deve ser único**
   * - Fantasia
     - string
     - Nome fantasia da revenda
   * - RazaoSocial
     - string
     - Razão social da revenda
   * - Tipo
     - string
     - Campo aberto para preencher de acordo com um possível tipo da revenda
   * - Cnpj
     - string
     - Cnpj da revenda. **Deve ser único**
   * - SetorId
     - int?
     - Campo aberto para preencher de acordo com um possível setor da revenda
   * - RamoAtividadeId
     - int?
     - Campo aberto para preencher de acordo com um possível ramo atividade da revenda
   * - OrigemId
     - int?
     - Campo aberto para preencher de acordo com um possível origem da revenda 
   * - InscricaoEstadual
     - string
     - Inscrição estadual da revenda
   * - InscricaoMunicipal
     - string
     - Inscrição Municipal da revenda (caso houver)
   * - InscricaoSuframa
     - string
     - Inscrição Superintendência da Zona Franca de Manaus da revenda (caso houver)
   * - InscricaoRural
     - string
     - Incrição Rural da revenda (caso houver)
   * - SituacaoId
     - int?
     - Campo aberto para preencher de acordo com um possível situação id da revenda
   * - Email
     - string
     - Email da revenda
   * - EmailFinanceiro
     - string
     - Possível email dedicado ao financeiro da revenda
   * - Observacao
     - string
     - Campo livre para preencher de acordo com possíveis observações da revenda
   * - Suframa
     - string
     - Campo dedicado a revendas atreladas a Superintendência da Zona Franca de Manaus
   * - Grupo
     - string
     - Campo aberto para preencher de acordo com um possível grupo da revenda
   * - Website
     - string
     - Website da revenda
   * - Ativo
     - bool
     - Controla se a revenda será ativa ou desativada no B2B
   * - ClienteCorporativo
     - bool?
     - Controla se a revenda é um cliente corporativo ou não
   * - VendedorErpId
     - string
     - Id de um possível Usuário do B2B que seja um vendedor da revenda
   * - VendedorResponsavelEmail
     - string
     - Caso o VendedorErpId não represente nenhum Usuário, será utilizado esse campo para preencher o email de um possível vendedor responsável pela revenda
   * - VendedorErpId
     - string
     - Id de um possível Usuário do B2B que seja um vendedor da revenda
   * - Pendencia
     - bool
     - Ignorar caso SaleSet não tiver sendo utilizado
   * - Segmento
     - string
     - Segmento Id da revenda
   * - Contribuinte
     - bool
     - Controla se a revenda é contribuinte ou não
   * - Perfil
     - string
     - Campo não utilizado, manter em branco.
   * - DataFundacao
     - DateTime?
     - Data de fundação da revenda
   * - Atributos
     - List<RevendaAtributoDTO>
     - Lista com os atributos da revenda
   
   
.. list-table:: Propriedades do RevendaAtributoDTO
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

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Revendas.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:UpdateRevenda>
           <tem:revenda>
              <b2b:Ativo>1</b2b:Ativo>
              <b2b:Atributos>
                 <b2b:RevendaAtributoDTO>
                    <b2b:NomeDoAtributo>Exemplo de atributo</b2b:NomeDoAtributo>
                    <b2b:Valor>Valor de atributo</b2b:Valor>
                 </b2b:RevendaAtributoDTO>
              </b2b:Atributos>
              <b2b:ClienteCorporativo>0</b2b:ClienteCorporativo>
              <b2b:Cnpj>61.353.741/0001-40</b2b:Cnpj>
              <b2b:Contribuinte>0</b2b:Contribuinte>
              <b2b:DataFundacao>2002-09-24</b2b:DataFundacao>
              <b2b:Email>teste@teste.com</b2b:Email>
              <b2b:EmailFinanceiro>teste@financeiro.com</b2b:EmailFinanceiro>
              <b2b:Fantasia>Exemplo de nome fantasia</b2b:Fantasia>
              <b2b:Grupo>Exemplo de grupo</b2b:Grupo>
              <b2b:Id>132456</b2b:Id>
              <b2b:InscricaoEstadual>123456789</b2b:InscricaoEstadual>
              <b2b:InscricaoMunicipal>1234</b2b:InscricaoMunicipal>
              <b2b:InscricaoRural>1234</b2b:InscricaoRural>
              <b2b:InscricaoSuframa>1324</b2b:InscricaoSuframa>
              <b2b:Observacao>Exemplo de observacao</b2b:Observacao>
              <b2b:OrigemId>123</b2b:OrigemId>
              <b2b:RamoAtividadeId>1</b2b:RamoAtividadeId>
              <b2b:RazaoSocial>Exemplo de razão social</b2b:RazaoSocial>
              <b2b:Segmento>1</b2b:Segmento>
              <b2b:SetorId>1</b2b:SetorId>
              <b2b:SituacaoId>1</b2b:SituacaoId>
              <b2b:Suframa>Exemplo de conteúdo de suframa</b2b:Suframa>
              <b2b:Tipo>1</b2b:Tipo>
              <b2b:VendedorResponsavelEmail>teste@vendedor.com</b2b:VendedorResponsavelEmail>
              <b2b:Website>teste.com.br</b2b:Website>
           </tem:revenda>
        </tem:UpdateRevenda>
     </soapenv:Body>
  </soapenv:Envelope>
  
  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <UpdateRevendaResponse xmlns="http://tempuri.org/">
           <UpdateRevendaResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </UpdateRevendaResult>
        </UpdateRevendaResponse>
     </s:Body>
  </s:Envelope>
