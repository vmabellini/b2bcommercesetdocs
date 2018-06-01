Alteração de status do pedido
=============================

É possível enviar uma alteração do status do pedido do ERP para o Webservice através do **AtualizarStatusPedidoErp**.
Dentro do modelo de pedidos, um pedido do webservice pode ser quebrado em N pedidos dentro do ERP, cada um com um status próprio.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - ErpId
     - string
     - Código do pedido no Erp. **Deve ser único**
   * - Status
     - OrderSiteStatus
     - Novo status do pedido (Descricao)
   * - Arquivos
     - ArquivosPedidoDTO
     - Contem uma lista de Arquivos do pedido.
     
.. list-table:: Propriedades do ArquivosPedidoDTO
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Arquivos
     - Lista de ArquivosPedidoItemResponse
     - Lista com arquivos do pedido

.. list-table:: Propriedades do ArquivosPedidoItemResponse
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - TipoArquivo
     - TipoDeArquivoDTO
     - Indica qual arquivo está sendo enviado
   * - Url
     - string
     - Contém a url onde o arquivo está hospedado.

.. list-table:: OrderSiteStatus
   :widths: auto
   :header-rows: 1

   * - Id
     - Descricao
   * - 0
     - Nenhum
   * - 1
     - LibComercial
   * - 2
     - LibFinanceira
   * - 3
     - Separacao
   * - 4
     - Despacho
   * - 5
     - Entrega

.. list-table:: TipoDeArquivoDTO
   :widths: auto
   :header-rows: 1

   * - Id
     - Descricao
   * - 0
     - SegundaViaBoleto
   * - 1
     - SegundaViaTransferencia
   * - 2
     - Xml
   * - 3
     - Danfe
   * - 4
     - NumeroDeSerie
   * - 5
     - GARE
   * - 6
     - GNRE
   * - 7
     - Outros

Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Pedidos.DTO">
      <soapenv:Header/>
      <soapenv:Body>
         <tem:AtualizarStatusPedidoErp>
          <b2b:Arquivos>
               <!--Optional:-->
               <b2b:Arquivos>
                  <!--Zero or more repetitions:-->
                  <b2b:ArquivosPedidoItemResponse>
                     <b2b:TipoArquivo>Danfe</b2b:TipoArquivo>
                     <b2b:Url>http://www.meuservidor.com/danfe.pdf</b2b:Url>
                  </b2b:ArquivosPedidoItemResponse>
                  <b2b:ArquivosPedidoItemResponse>
                     <b2b:TipoArquivo>SegundaViaBoleto</b2b:TipoArquivo>
                     <b2b:Url>http://www.meuservidor.com/boleto.pdf</b2b:Url>
                  </b2b:ArquivosPedidoItemResponse>
               </b2b:Arquivos>
            </b2b:Arquivos>
            <!--Optional:-->
            <tem:statusPedidoErpDto>
               <b2b:ErpId>123456</b2b:ErpId>
               <b2b:Status>LibComercial</b2b:Status>
            </tem:statusPedidoErpDto>
         </tem:AtualizarStatusPedidoErp>
      </soapenv:Body>
   </soapenv:Envelope>
   

Exemplo de response

.. code-block:: xml

   <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
      <s:Body>
         <AtualizarStatusPedidoErpResponse xmlns="http://tempuri.org/">
            <AtualizarStatusPedidoErpResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
               <a:Error>false</a:Error>
               <a:ErrorType i:nil="true"/>
               <a:Message i:nil="true"/>
            </AtualizarStatusPedidoErpResult>
         </AtualizarStatusPedidoErpResponse>
      </s:Body>
   </s:Envelope>
