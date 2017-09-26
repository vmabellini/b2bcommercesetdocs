Fluxo de cadastro de revendas
=============================

O fluxo de cadastro de revendas é um dos principais e também um dos mais complexos visto que existem muitos cenários possíveis.

Conceitos essenciais
--------------------

Todo usuário do site (qualquer um que possa realizar login) deve estar vinculado a uma revenda específica.
Toda revenda possui um usuário MASTER que tem acesso completo e irrestrito a todas as ações possíveis na plataforma B2B. A revenda também pode ter inúmeros outros usuários CONVIDADOS, que representam os vendedores e podem ter restrições de acesso, configuráveis pelo usuário MASTER através do Site B2B.

Quando a revenda já existe no ERP
---------------------------------

O site B2B espera uma carga inicial de revendas e usuários das revendas, para que a plataforma já inicie com uma base de clientes prontos para efetuarem login e registrarem pedidos.
Para que isso aconteça, a integração com os webservices deve chamar o método de CreateRevenda e em caso de sucesso, cadastrar também pelo menos um usuário MASTER para essa revenda. 
