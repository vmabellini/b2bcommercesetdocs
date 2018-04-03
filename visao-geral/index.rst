Visão Geral
===========

A plataforma de B2B foi criada com o intuito de ser integrada de forma simples com qualquer sistema externo.
Para isso é importante entender todas as entidades que irão compor a solução final:

Site B2B
--------

O site B2B abrange toda a plataforma de vendas acessível as revendas, com sua estrutura de busca, vitrines, banners, fluxo completo de pagamento, disparo de e-mails, cadastro de revendedores e vendedores, regras de precificação e integrações com gateways de pagamento. **Todos os dados necessários para compor o catálogo de produtos, informações de estoque, categorias, fabricantes e usuários deverão ser cadastrados através de webservices fornecidos pelo site.**

API de integração genérica (GIAPI)
----------------------------------

As demais informações que o site b2b precisa obter para seu funcionamento correto (preços de produtos, prazos de pagamento, envio de pedidos, tracking de pedidos e etc.) são obtidas através de um canal de comunicação genérico que pode ser implementado em diversas plataformas e linguagens de programação, **contanto que siga estritamente todas as especificações técnicas descritas nesse manual**.

Essa integração irá ocorrer através de uma API REST que deverá ser desenvolvida pelo cliente. Dessa forma, o site B2B precisa apenas saber qual é a URL base do endereço dessa API genérica, e toda a comunicação entre as plataformas será efetuada.

O site B2B provê ferramentas de log para que seja possível identificar quais são os requests sendo disparados para a GIAPI e quais são as respostas enviadas na integração.

Modularização
-------------

A partir da versão 18.5, é possível modularizar quais recursos estarão disponíveis em seu Site B2B.

A idéia é reduzir o tempo gasto para realizar as integrações, disponibilizando o novo Site B2B o mais rápido possível para seu cliente.

Segue uma lista de módulos que podem ser ativados/desativados no sistema. Para alterar a disponibilidade desses módulos é necessário entrar em contato com o suporte técnico para que possamos realizar a configuração correta da sua loja. Para mais informações, consulte o nosso suporte técnico:

**Módulos ativados por padrão**

    * (Estoque) Verificação de estoque online

    O Site B2B deixa de consultar o estoque em tempo real do ERP durante o fechamento do pedido.

    Desativando esse módulo, elimina-se a necessidade de implementar a api /estoque.

    * (Faturamento direto) Venda comissionada

    Com isso o Site B2B não faz mais faturamento direto para um CPF ou CNPJ.

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /clientefinal.

    * (Comissões) Módulo de comissões do site

    O Site B2B deixa de ter a funcionalidade de consulta e solicitação de comissões.

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /comissao.

    * (CEP) Módulo de consultar endereços via CEP no ERP

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /cep.

    * (Simulador de preços) Módulo de simulador de preço

    O Site B2B possui um módulo que permite ao revendedor selecionar um Estado diferente e um tipo fiscal de cliente para simular os preços da loja em seu contexto. Geralmente utilizado em conjunto com a venda comissionada.

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /preco/simulador e /precos/simulador (caso a API de /precos esteja ativada).

**Módulos desativados por padrão**

    * (Relatórios) Módulo que obtém relatórios personalizados através do ERP

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /relatorios.

    * (RMA) Módulo de Retorno de Mercadoria Avariada

    O Site B2B possui um módulo com um passo-a-passo para o revendedor solicitar o retorno de uma mercadoria com problemas.

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /rma.

    * (Arquivos de pedido) Módulo que permite ao usuário subir arquivos relacionados a um pedido efetuado no Site B2B

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /pedido/arquivo e /arquivospedido.

    * (Lista de preços) Módulo de obter Lista de Preços da revendas

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /preco/pricelist.

    * (Preços múltiplos) Módulo para obter múltiplos preços simultaneamente pela GIAPI

    Esse módulo serve como otimização, para evitar múltiplos requests simultâneos para a API de /preco durante a navegação do site.

    Desativando esse módulo, elimina-se a necessidade de implementar as apis de /precos.


