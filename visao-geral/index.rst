Visão Geral
===========

A plataforma de B2B foi criada com o intuito de ser integrada de forma simples com qualquer sistema externo.
Para isso é importante entender todas as entidades que irão compor a solução final:

Site B2B
--------

O site B2B abrange toda a plataforma de vendas acessível as revendas, com sua estrutura de busca, vitrines, banners, fluxo completo de pagamento, disparo de e-mails, cadastro de revendedores e vendedores, regras de precificação e integrações com gateways de pagamento. Todos os dados necessários para compor o catálogo de produtos, informações de estoque, categorias, fabricantes e usuários deverão ser cadastrados através de webservices fornecidos pelo site.

API de integração genérica (GIAPI)
----------------------------------

As demais informações que o site b2b precisa obter para seu funcionamento correto (preços de produtos, prazos de pagamento, envio de pedidos, tracking de pedidos e etc.) são obtidas através de um canal de comunicação genérico que pode ser implementado em diversas plataformas e linguagens de programação, contanto que siga estritamente todas as especificações técnicas descritas nesse manual.
Essa integração irá ocorrer através de uma API REST que deverá ser desenvolvida pelo cliente. Dessa forma, o site B2B precisa apenas saber qual é a URL base do endereço dessa API genérica, e toda a comunicação entre as plataformas será efetuada.
O site B2B provê ferramentas de log para que seja possível identificar quais são os requests sendo disparados para a GIAPI e quais são as respostas enviadas na integração.