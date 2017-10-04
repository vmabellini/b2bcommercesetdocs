FAQ
===

- **Como testar se a minha API está enviando a resposta no formato certo?**

  Nossa plataforma fornece uma área de log onde é possível visualizar toda a troca de mensagens entre a loja B2B e a sua API. Você pode ligar e desligar o log no caminho Admin > Configuração > Configurações > GI Api, através da opção DebugMode. Com o DebugMode ligado, é possível visualizar os logs através do link "ver logs de chamadas da API".

  O log irá mostrar detalhadamente quais são os dados que enviamos no request e quais os dados que retornaram a resposta da sua API. Em caso de erro de formatação ou resposta, a coluna Exception irá indicar o erro recebido.


- **Consegui pegar o erro no log, mas ainda assim não entendi qual o problema. Existe alguma ferramenta para me ajudar?**

  - Google Postman

  Através do Postman é possível simular todos os requests para a sua API.
  Muito útil também para realizar comparações dos retornos da sua API com a API demo da GI API para ver as diferenças e diagnosticar eventuais erros nos formatos de dados e Headers HTTP.

  - Fiddler

  Ferramenta mais avançada, permite diagnosticar com mais detalhes os requests e responses para a API, além de capturar todas as chamadas que o seu PC dispara para a rede/internet.


- **Estou recebendo o erro "Data at the root level is invalid. Line 1, position 1." ao ativar minha API e o site não conecta ao ERP para realizar autenticação no Token**

  Faça uma requisição via Postman no endereço onde está publicado sua API. Verifique se o Json está corretamente formato e também
  - O Status HTTP deve retornar código 200
  - Verifique se o campo Content-Type contém application/json;charset=UTF-8
