Alterar endereço da revenda
=======

Para alterar um endereço de uma revenda, ou adicionar um que não tenha sido inserido antes, através do **SetRevendaEndereco** preencha a entidade com os seguintes atributos:

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - RevendaId
     - int
     - Código da revenda no Erp. **Deve ser único**
   * - Cobranca
     - bool
     - Representa de o endereço é ou não de cobrança
   * - Entrega
     - bool
     - Representa de o endereço é ou não de entrega
   * - Faturamento
     - bool
     - Representa de o endereço é ou não de faturamento
   * - Endereco
     - EnderecoDTO
     - Novo endereco
     
.. list-table:: Propriedades do EnderecoDTO
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Estado
     - string
     - Prefixo do Estado (ex: SP)
   * - Cidade
     - string
     - Nome da cidade
   * - Bairro
     - string
     - Nome do bairro
   * - Rua
     - string
     - Nome da rua
   * - Numero
     - string
     - Número do endereço, podendo ter letras (ex: 125 A)
   * - Complemento
     - string
     - Complemento do endereço
   * - Cep
     - string
     - Cep (apenas números)
     
     
Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Revendas.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:SetRevendaEndereco>
           <tem:revendaEnderecoDto>
              <b2b:Cobranca>0</b2b:Cobranca>
              <b2b:Endereco>
                 <b2b:Bairro>Bairro</b2b:Bairro>
                 <b2b:Cep>12345678</b2b:Cep>
                 <b2b:Cidade>Cidade</b2b:Cidade>
                 <b2b:Complemento>Complemento</b2b:Complemento>
                 <b2b:Estado>SP</b2b:Estado>
                 <b2b:Numero>123 A</b2b:Numero>
                 <b2b:Rua>Rua</b2b:Rua>
              </b2b:Endereco>
              <b2b:Entrega>1</b2b:Entrega>
              <b2b:Faturamento>0</b2b:Faturamento>
              <b2b:RevendaId>123</b2b:RevendaId>
           </tem:revendaEnderecoDto>
        </tem:SetRevendaEndereco>
     </soapenv:Body>
  </soapenv:Envelope>
  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <SetRevendaEnderecoResponse xmlns="http://tempuri.org/">
           <SetRevendaEnderecoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </SetRevendaEnderecoResult>
        </SetRevendaEnderecoResponse>
     </s:Body>
  </s:Envelope>
