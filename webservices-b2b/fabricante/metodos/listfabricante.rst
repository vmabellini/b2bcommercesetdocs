Listar fabricantes
=======
Através do **ListCategorias**, é possível listar todos os fabricantes. O resultado da listagem é dividido por páginas, assim, a **Pagina** deve ser preenchida a princípio com o número 0 (zero) e deve ser incrementada até ter um retorno vazio, indicando que não foram encontrados mais resultados.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
     <soapenv:Header/>
     <soapenv:Body>
        <tem:ListFabricantes/>
     </soapenv:Body>
  </soapenv:Envelope>
   
Exemplo de response

.. code-block:: xml
   
   <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
     <s:Body>
        <ListFabricantesResponse xmlns="http://tempuri.org/">
           <ListFabricantesResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Fabricantes.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
              <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
              <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
              <a:Fabricantes>
                 <a:FabricanteDTO>
                    <a:Descricao>Exemplo de descricao</a:Descricao>
                    <a:ErpId>AAA11111</a:ErpId>
                    <a:Nome>Exemplo de nome de fabricante</a:Nome>
                    <a:OrdemDeExibicao>0</a:OrdemDeExibicao>
                 </a:FabricanteDTO>
                 <a:FabricanteDTO>
                    <a:Descricao>Exemplo de descricao 02</a:Descricao>
                    <a:ErpId>AAA11112</a:ErpId>
                    <a:Nome>Exemplo de nome de fabricante 02</a:Nome>
                    <a:OrdemDeExibicao>0</a:OrdemDeExibicao>
                 </a:FabricanteDTO>
              </a:Fabricantes>
           </ListFabricantesResult>
        </ListFabricantesResponse>
     </s:Body>
  </s:Envelope>
