Obter arquivos de produto
=======

Para obter os arquivos de um produto inserido no B2B, através do **GetArquivosProduto** preencha a requisição com o **PartNumber** que deseja encontrar.

Exemplo de request

.. code-block:: xml

  <soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:tem="http://tempuri.org/">
   <soapenv:Header/>
   <soapenv:Body>
      <tem:GetArquivosProduto>
         <tem:partNumber>E1670SWU/WM</tem:partNumber>
      </tem:GetArquivosProduto>
   </soapenv:Body>
  </soapenv:Envelope>

  
Exemplo de response

.. code-block:: xml

  <s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <GetArquivosProdutoResponse xmlns="http://tempuri.org/">
         <GetArquivosProdutoResult xmlns:a="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices.Produtos.DTO" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
            <Error xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices">false</Error>
            <ErrorType i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
            <Message i:nil="true" xmlns="http://schemas.datacontract.org/2004/07/B2B.Integration.Webservices"/>
            <a:ArquivosProduto>
               <a:ResponseArquivosProdutoDTO.ArquivoProduto>
                  <a:DownloadGuid>2b5a62d2-3b4d-4d82-9cf9-16d1f1a9448c</a:DownloadGuid>
                  <a:DownloadUrl>http://teste.atma-it.com/orderproductdownloadsfile/2b5a62d2-3b4d-4d82-9cf9-16d1f1a9448c</a:DownloadUrl>
                  <a:Filename>testeArquivo1.pdf</a:Filename>
               </a:ResponseArquivosProdutoDTO.ArquivoProduto>
               <a:ResponseArquivosProdutoDTO.ArquivoProduto>
                  <a:DownloadGuid>2b5a62d2-3b4d-4d82-9cf9-16d1f1a9448c</a:DownloadGuid>
                  <a:DownloadUrl>http://teste.atma-it.com/orderproductdownloadsfile/2b5a62d2-3b4d-4d82-9cf9-16d1f1a9448c</a:DownloadUrl>
                  <a:Filename>testeArquivo2.pdf</a:Filename>
               </a:ResponseArquivosProdutoDTO.ArquivoProduto>
            </a:ArquivosProduto>
         </GetArquivosProdutoResult>
      </GetArquivosProdutoResponse>
   </s:Body>
  </s:Envelope>
