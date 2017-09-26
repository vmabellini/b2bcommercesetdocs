Segurança dos Webservices
=========================

Como medida de segurança, é possível habilitar um método de autenticação nos webservices do site para que os endpoints do B2B não fiquem expostos publicamente e vulneráveis a ataques.

Na tela de Administração do B2B, em **Configurações > Configurações > GI API**, é possível habilitar/desabilitar a segurança dos serviços e definir um usuário e senha. Com a segurança configurada, o ERP deverá chamar o método de login no TokenWebService.svc que irá retornar um Token e uma data de validade. Esse Token deve ser armazenado do lado ERP e utilizado em todas as chamadas para os métodos dos Webservices, enviado como parâmetro no header de cada request (tanto no modelo SOAP quanto REST). Mais informações podem ser encontradas na própria tela de administração do B2B, inclusive com um exemplo de request.

É importante ressaltar que **a não ativação do token de segurança pode expor o site a ataques mal-intencionados**, ficando a cargo do cliente ativar e cuidar das credenciais de acesso.
