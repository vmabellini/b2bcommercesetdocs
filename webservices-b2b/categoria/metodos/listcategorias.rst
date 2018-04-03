Listar categorias
=======
Através do **ListCategorias**, faça uma busca o preenchendo o **Nome** com uma parte ou o nome inteiro da categoria. Caso não preenchido, serão retornadas todas as categorias.

O resultado da listagem é dividido por páginas, assim, a **Pagina** deve ser preenchida a princípio com o número 0 (zero) e deve ser incrementada até ter um retorno vazio, indicando que não foram encontrados mais resultados.

Exemplo de request

.. code-block:: xml

   <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
      <soapenv:Header/>
      <soapenv:Body>
         <tem:ListCategorias>
            <tem:nome>Teste</tem:nome>
            <tem:pagina>0</tem:pagina>
         </tem:ListCategorias>
      </soapenv:Body>
   </soapenv:Envelope>
   
Exemplo de response

.. code-block:: xml
   
   <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
      <s:Body>
         <ListCategoriasResponse xmlns="http://tempuri.org/">
            <ListCategoriasResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Categorias.DTO" 
            xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
               <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
               <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
               <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
               <a:Categorias>
                  <a:CategoriaDTO>
                     <a:Descricao i:nil="true"/>
                     <a:ErpId i:nil="true"/>
                     <a:ErpIdPai i:nil="true"/>
                     <a:Nome>Teste 5</a:Nome>
                     <a:OrdemDeExibicao>0</a:OrdemDeExibicao>
                  </a:CategoriaDTO>
                  <a:CategoriaDTO>
                     <a:Descricao i:nil="true"/>
                     <a:ErpId i:nil="true"/>
                     <a:ErpIdPai i:nil="true"/>
                     <a:Nome>Teste 6</a:Nome>
                     <a:OrdemDeExibicao>0</a:OrdemDeExibicao>
                  </a:CategoriaDTO>
                  <a:CategoriaDTO>
                     <a:Descricao i:nil="true"/>
                     <a:ErpId i:nil="true"/>
                     <a:ErpIdPai i:nil="true"/>
                     <a:Nome>Teste 9</a:Nome>
                     <a:OrdemDeExibicao>0</a:OrdemDeExibicao>
                  </a:CategoriaDTO>
                  <a:CategoriaDTO>
                     <a:Descricao i:nil="true"/>
                     <a:ErpId i:nil="true"/>
                     <a:ErpIdPai i:nil="true"/>
                     <a:Nome>Teste 8</a:Nome>
                     <a:OrdemDeExibicao>0</a:OrdemDeExibicao>
                  </a:CategoriaDTO>
               </a:Categorias>
            </ListCategoriasResult>
         </ListCategoriasResponse>
      </s:Body>
   </s:Envelope>
