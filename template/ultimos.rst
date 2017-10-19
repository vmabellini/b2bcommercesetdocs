Últimos releases
================

Versão 0.9.87
-------------
Ajuste no método de Boleto.
Adição dos dados do pedido desmembrados por Centro de Distribuição. Não está implementado no layout de todos os clientes.
Adição de um novo método para geração de respostas de erro via GIAPI: o objeto ErrorResponse. Consulte a documentação para mais detalhes.
Adição do campo DataFaturamento no objeto PedidoSalesSetInformacoesAdicionaisRequest.


Versão 0.9.86
-------------

[OPCIONAL] Extensão de garantia: 
Incluído campo de definição das extensões de garantia no PedidoItemRequest
Novo método: api/v1/serialnumber - Realiza a busca do SerialNumber através do dado de entrada (código do pedido, código do pedido no ERP ou número da nota fiscal)


Versão 0.9.85
-------------

Incluídas interfaces para facilitar as mudanças dos clientes caso os métodos da GIAPI sofram alteração ou sejam adicionados novos métodos
Novo método na GIAPI para receber o status do pagamento de um pedido
Envio de um novo campo ao fechar pedido (StatusPagamentoPedido no objeto PedidoRequest) para indicar se o status do pagamento será confirmado posteriormente (usado em alguns plugins de Cartão de Crédito)
Adição da propriedade NumeroNotaFiscal e LinkNotaFiscal no objeto PedidoRequest
Adição dos campos Simples e Contribuinte no objeto RevendaRequest
Adição dos campos Grupo e OrdemDeExibicao no objeto PrazoDePagamentoItemResponse, o que permite agora retornar as opções de pagamento para outros plugins além do faturado


Versão 0.9.84
-------------

Adição da RevendaId no request de Estoque


Versão 0.9.83
-------------

[OPCIONAL] Adicionado novo método para geração de relatórios de venda



Versão 0.9.82
-------------

Alteração do objeto PrazoDePagamentoRequest incluindo - por CD - PrazoDePagamentoCobrancaDeSTRequest , indicando se ST será cobrada no total do pedido.


Versão 0.9.81
-------------

[SALES SET] Breaking changes em todo o sistema de frete do Sales Set: agora o frete é independente por filial
CarrinhoFreteSalesSetRequest: adição dos campos DistributionCenterId e DistributionCenterPrefix, para identificar de qual filial é o request de frete
CarrinhoFreteSalesSetItemRequest: adição do campo SKU e remoção do campo DistributionCenterId
Criação do objeto CarrinhoSalesSetShippingRequest, para enviar os dados de frete por filial no carrinho de compras
CarrinhoSalesSetRequest: inclusão da propriedade FretesSelecionados do tipo List<CarrinhoSalesSetShippingRequest>, para identificar cada seleção de frete por filial
Criação do objeto PedidoFreteSalesSetRequest para enviar os dados de frete por filial na criação de pedido
PedidoSalesSetRequest: remoção dos campos: TipoFrete, FormaEntregaId, OpcaoEntregaId. Esses dados devem ser lidos agora da lista FretePorCentroDistribuicao


Versão 0.9.80
-------------

[SALES SET] Alteração do objeto InfoMargemSalesSetRequest transformando os campos de porcentagem de int para decimal
[SALES SET] Alteração do objeto PedidoRequest com os campos Encomenda e Necessidade


Versão 0.9.79
-------------

[SALES SET] Alterações nas APIs de preço, frete e pedido contemplando o recurso de contexto de venda


Versão 0.9.78
-------------

Adicionado o campo ValorUnitarioOriginal no objeto InfoMargemSalesSetRequest
Adicionado novo método para obter OpcaoPagamentoSalesSet filtrada de acordo com o carrinho


Versão 0.9.77
-------------

Refatoração dos métodos SalesSet de transportadora, banco e endereço, alterando a estrutura para POST e criando um objeto QueryRequest para passar os parâmetros

Versões mais antigas ainda
==========================

v0.9.76

Release notes

Alterações estruturais na API de opções de pagamento do Sales Set
Alterações estruturais na API de margem Sales Set

v0.9.75.1

Release notes

Adicionado funcionalidade de lista de preços para alguns clientes

v0.9.74

Release notes

Adicionado o campo revendaId na API de /arquivospedido

v0.9.73

Release notes

Adicionado o campo RevendaId no objeto ComissaoPesquisaRequest
Adicionado o campo RevendaId no objeto ComissaoDetalheResponse

v0.9.72

Release notes

Adicionada a propriedade CentroDistribuicaoPrefix no PedidoItemRequest e FretePorCentroDistribuicaoRequest

v0.9.71

Release notes

Adicionada a propriedade VendedorRevendaId no FreteRequest e CentroDistribuicaoPrefix no FreteItemRequest para os casos onde é necessário saber qual a revenda do vendedor que está logado no site buscando o preço

v0.9.7

Release notes

Adicionada a propriedade VendedorRevendaId no PrecoRequest para os casos onde é necessário saber qual a revenda do vendedor que está logado no site buscando o preço
Adicionado parâmetro revendaId no GET de Pedido (opcional) para auxiliar a busca pelo pedido em alguns casos

v0.9.6

Release notes

Atualizado o formato das condições de pagamento para permitir que o ID da condição seja string. A propriedade CondicaoId (int) será descontinuada e deverá ser substituída pelo CondicaoStringId
Adicionada estrutura de DimensoesUnitarias nos itens da api de frete para auxiliar com o cálculo de frete em alguns casos

v0.9.5

Release notes

O método de cálculo de frete agora envia também uma informação do contexto de venda atual, permitindo devolver um valor diferenciado para cada caso

v0.9.4

Release notes

Envio de Skus nos métodos de preço para alguns casos opcionais
Novos métodos para o Sales Set
Alteração opcional no funcionamento da GIAPI para que seja possível cadastrar os Variantes do produto manualmente

v0.9.3

Release notes

Foi adicionado um novo conjunto de APIs para serem utilizados pelos clientes que irão implementar o recurso de Sales Set no site do B2B. Todas essas APIs novas estão devidamente marcadas como [SALES SET] e não são necessárias para quem utiliza o B2B padrão

v0.9.2

Release notes

Foi adicionada uma nova API para obter preços múltiplos. Para os clientes com limitação de requests nos servidores essa opção pode ser mais vantajosa. Basta implementar os métodos da nova API de /precos e habilitar a opção no Admin do site (/Admin/Setting/GIAPI > Ativar request único para preço múltiplo na API (/precos)). Por padrão essa opção virá desabilitada para não impactar o sistema atual.

v0.9.1

Release notes

Adicionamos um novo campo de sócios para revendas, conforme solicitado por alguns clientes.

v0.9

Release notes

O método de integração de pedidos agora tem campos de bandeira do cartão e id do pagamento da integração de compras com cartão.

v0.8

Release notes

[BUGFIX] O retorno do método pedido/pesquisa estava com a documentação incorreta na API.

v0.7

Release notes

A loja B2B agora também envia os dados de frete separados por Centro de Distribuição através de um novo objeto "FretePorCentroDistribuicao".

v0.6

Release notes

[BUGFIX] Adicionado o parâmetro EncargoFinanceiro no retorno de item de prazo de pagamento. O campo é informativo e renderizado na tela de checkout para as opções de pagamento faturado.

v0.5

Release notes

Adicionado o parâmetro RevendaId na chamada do simulador de preço (api/v1/preco/simulador). O site agora envia qual é a revenda do usuário logado, permitindo que a API retorne preços diferentes para revendas diferentes.

v0.4

Release notes

[OBRIGATÓRIO] Adicionado tipo de preço na chamada de Preço, para que seja possível retornar um preço diferenciado dependendo do contexto de navegação (catálogo, venda consumo, venda revenda, venda comissionada)
[OBRIGATÓRIO] A pesquisa de pedido foi remodelada para deixar mais claro e evitar erros sobre as formas de filtro de pedido que o site executa