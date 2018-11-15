Criar usuário
=======
Para ter acesso ao B2B, é necessário criar um usuário com login e senha que é atrelado a uma revenda. A sua criação é feita através do **CreateUsuario** enviando a entidade abaixo devidamente preenchida:

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - AtivarPorEmail
     - bool
     - Representa se usuário precisará receber um email para ser ativado ou se já entrará como ativo
   * - EmailDeAcesso
     - string
     - Email de acesso do usuário
   * - LimiteDeCompra
     - decimal?
     - Caso o usuário tenha, represena o seu limite de compra total
   * - Master
     - bool
     - Representa se o usuário é o master de sua revenda, se sim, as quatro opções abaixo serão verdadeiras
   * - PodeAcessarComissoes
     - bool
     - Representa se o usuário pode acessar comissões
   * - PodeAcessarSomentePropriasComissoes
     - bool
     - Representa se o usuário pode acessar somente as próprias comissões
   * - PodeCriarConvidado
     - bool
     - Representa se o usuário pode criar convidado
   * - PodeEfetuarCompra
     - bool
     - Representa se o usuário pode efetuar compra
   * - Nome
     - string
     - Nome do usuário
   * - RevendaId
     - string
     - Id da Revenda que o usuário será atrelado
   * - Segmento
     - string
     - Campo aberto para possível preencher como o segmento do usuário
   * - Senha
     - string
     - Senha que o usuário usará para acessar o site
   * - ErpId
     - string
     - Id do usuário no Erp
    
     
Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Revendas.DTO">
      <soapenv:Header/>
      <soapenv:Body>
         <tem:CreateUsuario>
            <tem:usuario>
               <b2b:AtivarPorEmail>0</b2b:AtivarPorEmail>
               <b2b:EmailDeAcesso>teste21345@atma-it.com</b2b:EmailDeAcesso>
               <b2b:ErpId>78945</b2b:ErpId>
               <b2b:LimiteDeCompra>0</b2b:LimiteDeCompra>
               <b2b:Master>0</b2b:Master>
               <b2b:Nome>Teste Atma</b2b:Nome>
               <b2b:PodeAcessarComissoes>1</b2b:PodeAcessarComissoes>
               <b2b:PodeAcessarSomentePropriasComissoes>0</b2b:PodeAcessarSomentePropriasComissoes>
               <b2b:PodeCriarConvidado>1</b2b:PodeCriarConvidado>
               <b2b:PodeEfetuarCompra>1</b2b:PodeEfetuarCompra>
               <b2b:RevendaId>1</b2b:RevendaId>
               <b2b:Segmento>Teste</b2b:Segmento>
               <b2b:Senha>123456</b2b:Senha>
               <b2b:ErpId>COD001</b2b:ErpId>
            </tem:usuario>
         </tem:CreateUsuario>
      </soapenv:Body>
   </soapenv:Envelope>

  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <CreateUsuarioResponse xmlns="http://tempuri.org/">
           <CreateUsuarioResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </CreateUsuarioResult>
        </CreateUsuarioResponse>
     </s:Body>
  </s:Envelope>
