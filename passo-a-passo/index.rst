Passo-a-passo recomendado
=========================

Para facilitar o processo de desenvolvimento de toda a integração, **nós recomendamos seguir os passos abaixo**:

#. **Integrar inicialmente com os webservices do site B2B;** desenhar o fluxo da informação e identificar a melhor abordagem para realizar a carga inicial de Categorias, Fabricantes, Produtos e Revendas.
#. Determinar qual será a frequência necessária para que novos produtos sejam integrados no site B2B e criar rotinas de atualização de acordo com essas regras.
#. Testar se a carga de dados está funcionando corretamente em um ambiente de homologação; nesse período o site B2B estará conectado com a GIAPI de demonstração, o que permite testar todo o fluxo de dados da navegação com dados fictícios.
#. Iniciar o desenvolvimento da GIAPI, **levando em consideração os seguintes aspectos**:

   * Seu ERP atual possui ferramentas que facilitam o desenvolvimento de uma API REST para integrar-se ao site B2B?
   * Seu ERP atual possui limitações técnicas que podem comprometer o desempenho do site com muitos usuários simultâneos?
   * Será necessária uma camada intermediária entre o ERP e o site B2B desenvolvida em uma linguagem mais moderna que possua mais recursos para fornecer os métodos da GIAPI?

É importante ressaltar que **antes do desenvolvimento das integrações é necessário toda uma análise do ambiente atual** para evitar problemas futuros, como lentidão do site, conexão ruim entre o site B2B e a GIAPI, dificuldades técnicas de fornecer a estrutura necessária para a API e etc.

Recomendamos que o desenvolvimento da GIAPI se inicie através dos métodos de obtenção de preço de produtos, pois eles costumam ser muito requisitados e podem servir como um bom parâmetro para medir o desempenho da comunicação entre as plataformas.


Divisão do projeto
==================

Recomendamos seguir a tabela abaixo para delimitar cada versão da integração.
Essa tabela serve como guideline para que seja possível subir o site com o mínimo de funcionalidades básicas necessárias para o início da operação.

Fase 1
------

.. list-table:: Fase 1
   :widths: auto
   :header-rows: 1

   * - Módulo
     - Tipo de integração
     - Método
     - Descrição
   * - Categorias
     - WebService
     - CreateCategoria
     - Integração básica de catálogo
   * - Fabricantes
     - WebService
     - CreateFabricante
     - Integração básica de catálogo
   * - Produtos
     - WebService
     - CreateProduto
     - Integração básica de catálogo
   * - Produtos
     - WebService
     - VincularACategoria
     - Integração básica de catálogo
   * - Estoque
     - WebService
     - AtualizarEstoque
     - Integração básica de catálogo
   * - Token
     - API
     - /token
     - Autenticação com a GIAPI
   * - Pedido
     - API
     - /checkout
     - Cálculo e exibição de frete e formas de pagamento
   * - Preço
     - API
     - /preco e /precos
     - Fornecimento de preços de acordo com o usuário logado

Fase 2
------

.. list-table:: Fase 2
   :widths: auto
   :header-rows: 1

   * - Módulo
     - Tipo de integração
     - Método
     - Descrição
   * - Revendas
     - Webservice
     - CreateRevendaCompleta
     - Carrega os dados da revenda no site B2B
   * - Revendas
     - Webservice
     - CreateUsuario
     - Carrega os dados do usuário vinculado à revenda no site B2B
   * - Pedidos
     - WebService
     - ListarNovos
     - Obtenção dos pedidos pendentes de integração (caso utilize a integração PASSIVA de pedidos)
   * - Pedidos
     - WebService
     - IntegrarPedido
     - Notificação de pedido integrado (caso utilize a integração PASSIVA de pedidos)
   * - Preço
     - API
     - /preco/simulador e /precos/simulador
     - Simulador de preço
   * - Pedidos
     - API
     - /pedido
     - Envio de pedido para o ERP (caso utilize a integração ATIVA de pedidos)
   * - Pedidos
     - API
     - /pedido/pesquisa
     - Listagem de pedidos registrados no ERP
   * - Pedidos
     - API
     - /pedido/notafiscal
     - Consulta de notas fiscais dos pedidos

Fase 3
------

.. list-table:: Fase 3
   :widths: auto
   :header-rows: 1

   * - Módulo
     - Tipo de integração
     - Método
     - Descrição
   * - Estoque
     - API
     - /estoque
     - Verificação de estoque em tempo real antes de fechar um pedido
   * - Cliente Final
     - API
     - /clientefinal/*
     - Busca e envio de dados de cliente final para o módulo de faturamento direto
   * - Revendas
     - API
     - /revenda/*
     - Busca e envio de dados de revendas e usuários do site
   * - Comissões
     - API
     - /comissao/*
     - Consulta e solicitação de comissões (quando ativado o módulo de faturamento direto)
   * - CEP
     - API
     - /cep
     - Consulta de endereços por CEP
   * - Pedidos
     - API
     - /pedido/arquivo e /arquivospedido
     - Consulta de arquivos relacionados aos pedidos


OBS: alguns módulos opcionais não estão visíveis nessa lista.