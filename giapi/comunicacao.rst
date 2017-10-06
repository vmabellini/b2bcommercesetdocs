Comunicação entre as plataformas
================================

Como toda API REST, a GIAPI é baseada em comunicação HTTP simples entre os dois sistemas (Site B2B e GIAPI implementada pelo cliente).

Para tal seguem alguns conceitos básicos que devem ser seguidos durante o desenvolvimento:

- **Toda a comunicação é baseada nos verbos GET e POST**

  Para facilitar o proceso de integração, utilizamos somente GET e POST para comunicação. Isso facilita a implementação na maioria das linguagens.

- **Toda a comunicação é baseada em dados JSON**

  O formato JSON é muito leve e amplamente utilizado hoje não apenas para websites como para comunicação entre sistemas visando a facilidade de adoção, uso de banda reduzido e simplicidade para a leitura.
  Para que esse padrão seja entendido corretamente do lado do Site B2B lembre-se sempre de definir o "Content-type: application/json" na resposta.

- **Todas as chamadas para a GIAPI enviam o token de autenticação**

  O token é enviado no header e a responsabilidade de validação é do cliente. Cabe a GIAPI gerar, armazenar e validar os tokens de acordo com o tempo de vida de cada um.
  Lembre-se: a segurança da comunicação é fundamental e de responsabilidade do desenvolvedor da API.

- **O Site B2B entende os códigos HTTP de resposta**

  Do nosso lado nós interpretamos os códigos HTTP informados seguindo o padrão:

  - 404 (Not Found): deve ser utilizado quando o Site B2B solicita uma entidade da GIAPI e ela não é encontrada.
    Ex: consulta de revenda por CNPJ

  - 500 (Internal Server Error): deve ser a resposta padrão para quando ocorre um erro na GIAPI.
    Quanto mais detalhes forem informados na resposta HTTP, melhor.
    O padrão para envio de mensagens com o conteúdo do erro é um JSON no seguinte formato **(não é necessário preencher todos os campos)**:


    .. code-block:: json

       {
         "message": "Mensagem de erro personalizada",
         "exceptionMessage": "Dados da exceçao retornada",
         "exceptionType": "Tipo da exceção",
         "stackTrace": "Dados técnicos de erro para debug"
       }

- **Retorno de erro personalizado**

  A partir da versão 17.6.x teremos também a opção de retornar um objeto específico de erro.
  Basta retornar o objeto ErrorResponse preenchido em qualquer uma das chamadas da GIAPI informando a mensagem de erro e o tipo do erro. Dessa maneira não é obrigatório retornar o código 500 do Http para informar algum problema.