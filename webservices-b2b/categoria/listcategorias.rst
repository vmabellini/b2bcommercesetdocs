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
            <tem:nome></tem:nome>
            <tem:pagina>0</tem:pagina>
         </tem:ListCategorias>
      </soapenv:Body>
   </soapenv:Envelope>
