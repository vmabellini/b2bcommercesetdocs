Atualizar estoque
=======
A atualização de estoque de variantes de produtos pode ser feita através do **AlterarDisponibilidadeDaCategoria** de dois modos:
Variante manual ou automático (Saiba mais em :doc:`Produtos <../../../webservices-b2b/produto/index.html>`.

Em qualquer um dos modos, deve ser preenchido o **PartNumber** do produto e a **Quantidade** com o novo estoque.

Caso o B2B esteja utilizando variantes manuais, deve ser preenchida o **Sku** do variante do produto. Já se estiver utilizando os automáticos, preencha o **CentroDeDistribuicaoPrefix** e/ou o **CentroDeDistribuicaoId**.

Exemplo de request utilizando Variantes Manuais

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Estoque.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:AtualizarEstoque>
           <tem:listaEstoqueDto>
              <b2b:ProdutoEstoques>
                 <b2b:ProdutoEstoqueDTO>
                    <b2b:PartNumber>AAA1111</b2b:PartNumber>
                    <b2b:VarianteProdutoEstoques>
                       <b2b:VarianteProdutoEstoqueDTO>
                          <b2b:CentroDeDistribuicao>0</b2b:CentroDeDistribuicao>
                          <b2b:CentroDeDistribuicaoPrefix></b2b:CentroDeDistribuicaoPrefix>
                          <b2b:Quantidade>10</b2b:Quantidade>
                          <b2b:Sku>AAA11111S</b2b:Sku>
                       </b2b:VarianteProdutoEstoqueDTO>
                    </b2b:VarianteProdutoEstoques>
                 </b2b:ProdutoEstoqueDTO>
              </b2b:ProdutoEstoques>
           </tem:listaEstoqueDto>
        </tem:AtualizarEstoque>
     </soapenv:Body>
  </soapenv:Envelope>
  
Exemplo de request utilizando Variantes Automáticos 

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/" xmlns:b2b="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Estoque.DTO">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:AtualizarEstoque>
           <tem:listaEstoqueDto>
              <b2b:ProdutoEstoques>
                 <b2b:ProdutoEstoqueDTO>
                    <b2b:PartNumber>AAA1111</b2b:PartNumber>
                    <b2b:VarianteProdutoEstoques>
                       <b2b:VarianteProdutoEstoqueDTO>
                          <b2b:CentroDeDistribuicao>5</b2b:CentroDeDistribuicao>
                          <b2b:CentroDeDistribuicaoPrefix>SP</b2b:CentroDeDistribuicaoPrefix>
                          <b2b:Quantidade>10</b2b:Quantidade>
                          <b2b:Sku></b2b:Sku>
                       </b2b:VarianteProdutoEstoqueDTO>
                    </b2b:VarianteProdutoEstoques>
                 </b2b:ProdutoEstoqueDTO>
              </b2b:ProdutoEstoques>
           </tem:listaEstoqueDto>
        </tem:AtualizarEstoque>
     </soapenv:Body>
  </soapenv:Envelope>

Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <AtualizarEstoqueResponse xmlns="http://tempuri.org/">
           <AtualizarEstoqueResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <a:Error>false</a:Error>
              <a:ErrorType i:nil="true"/>
              <a:Message i:nil="true"/>
           </AtualizarEstoqueResult>
        </AtualizarEstoqueResponse>
     </s:Body>
  </s:Envelope>
