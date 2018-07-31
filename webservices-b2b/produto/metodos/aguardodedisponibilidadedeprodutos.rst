Aguardo de Disponibilidade de Produto
=====================================

Busca os usuários que se inscreveram para receber o e-mail de retorno de estoque.

.. list-table:: Propriedades do request
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - PartNumber
     - string
     - Código do produto no ERP.
   * - IdRevenda
     - int
     - Código da revenda. **Não obrigatório**
   * - DistributionCenterId
     - int
     - Código do centro de distribuição **Não obrigatório**

Exemplo de request

.. code-block:: xml

    <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO">
    <soapenv:Header/>
    <soapenv:Body>
        <tem:AguardoDeDisponibilidadeDeProdutos>
            <tem:request>
                <b2b:DistributionCenterId>2</b2b:DistributionCenterId>
                <b2b:IdRevenda>?</b2b:IdRevenda>
                <b2b:PartNumber>?</b2b:PartNumber>
            </tem:request>
        </tem:AguardoDeDisponibilidadeDeProdutos>
    </soapenv:Body>
    </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

    <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Body>
        <AguardoDeDisponibilidadeDeProdutosResponse xmlns="http://tempuri.org/">
            <AguardoDeDisponibilidadeDeProdutosResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
                <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
                <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
                <a:ListaDeAguardoDeDisponibilidade>
                <a:AguardoDeDisponibilidadeDTO>
                    <a:CentroDeDistribuicao>1</a:CentroDeDistribuicao>
                    <a:Data>2018-02-20T17:28:05.053</a:Data>
                    <a:EmailDoUsuario>usuario@provedor.com</a:EmailDoUsuario>
                    <a:IdRevenda>1</a:IdRevenda>
                    <a:IdVariante>19404</a:IdVariante>
                    <a:NomeDoProduto>Produto de Teste</a:NomeDoProduto>
                    <a:PartNumber>ABC-123</a:PartNumber>
                    <a:Revenda>Atma Serviços LTDA - ME</a:Revenda>
                </a:AguardoDeDisponibilidadeDTO>
                <a:AguardoDeDisponibilidadeDTO>
                    <a:CentroDeDistribuicao>1</a:CentroDeDistribuicao>
                    <a:Data>2018-02-16T12:04:28.697</a:Data>
                    <a:EmailDoUsuario>usuario2@provedor.com</a:EmailDoUsuario>
                    <a:IdRevenda>1</a:IdRevenda>
                    <a:IdVariante>20078</a:IdVariante>
                    <a:NomeDoProduto>Produto de Teste 2</a:NomeDoProduto>
                    <a:PartNumber>86043</a:PartNumber>
                    <a:Revenda>Atma Serviços LTDA - ME</a:Revenda>
                </a:AguardoDeDisponibilidadeDTO>
                </a:ListaDeAguardoDeDisponibilidade>
            </AguardoDeDisponibilidadeDeProdutosResult>
        </AguardoDeDisponibilidadeDeProdutosResponse>
    </s:Body>
    </s:Envelope>