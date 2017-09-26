Estrutura básica das chamadas dos Webservices
=============================================

Todas as chamadas aos nossos webservices possuem objetos distintos de Request e Response. 

Enquanto todos os objetos de Request variam entre si, todos os objetos de Response possuem as seguintes propriedades em comum:

.. list-table:: Estrutura básica
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - Error
     - bool
     - **true** ou **false** indicando se ocorreu algum erro na chamada
   * - ErrorType
     - string
     - Tipo do Erro. Os valores podem ser:
       **InvalidParameterException**: Erro ocorrido quando algum campo do 
       request do webservice possui algum valor inválido. 
       Ex: Id não encontrado, CNPJ inválido.

       **SystemException**: Qualquer outro erro não previsto pelo sistema.
   * - Message
     - string
     - Mensagem do erro.
   * - [Dados do objeto]
     - [object]
     - Dados requisitados. A existência dos campos de dados depende da 
       natureza do Webservice. Caso a função do webservice chamado seja 
       de cadastro, (geralmente) a resposta não receberá esses campos, 
       deixando esses dados para webservices de busca e listagem.

Dessa forma, ao realizar qualquer chamada para os Webservices do Site B2B, a primeira coisa a fazer é verificar se a propriedade **Error** é false. Caso contrário, deve-se ler o tipo de erro e a mensagem para realizar o tratamento adequado.