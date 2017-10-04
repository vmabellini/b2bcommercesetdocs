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

Preparando o Site B2B
---------------------

Depois de seguir as instruções e configurar as integrações com os webservices do Site B2B e também criar a GIAPI