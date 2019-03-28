Trocas e devolução de mercadorias
=================================

Temos um módulo de trocas e devoluções que permite o usuário preencher uma lista de itens que ele deseja retornar, bem como os motivos.

A implementação desse módulo é bastante simples:

# Configurar os motivos possíveis de devolução através do Admin > Configuração > SRM > Motivos. Alguns motivos podem ou não solicitar os produtos, como em caso de troca por exemplo. O ID no ERP é um campo aberto que será enviado via GIAPI para facilitar a identificação do motivo cadastrado pelo site.

  .. image:: rma.png

# Ao acessar a tela do RMA, o usuário irá criar uma solicitação e irá selecionar o motivo. Após a criação da solicitação, a GIAPI irá receber todos os dados através da API de pedido RMA (http://apidev.atma-it.com/Help/Api/GET-api-v1-pedido_pedidoErpId_revendaId). O que nós esperamos em retorno é um ID que identifica essa solicitação no ERP, para que posteriormente possamos consultar o andamento desse RMA.
# Ao consultar o status de um RMA, o sistema chama a API http://apidev.atma-it.com/Help/Api/GET-api-v1-rma-detalhes-srmId, retornando qual a etapa atual dessa solicitação, os logs de ações efetuadas ao longo do tempo e também uma flag que indica se a solicitação foi rejeitada.

Integração de novo RMA
======================
# Quando o usuário finalizar a criação de RMA pelo site, ele será integrado via GIAPI através do método IntegrarPedido, onde será enviado o request de RmaPedidoRequest:

.. list-table:: RmaPedidoRequest
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
   * - Id
     - int
   * - NotaFiscal
     - string
   * - Data
     - DateTime
   * - ContatoNome
     - string
   * - ContatoDDD
     - string
   * - ContatoTelefone
     - string
   * - ContatoEmail
     - string
   * - RevendaId
     - int
   * - MotivoErpId
     - string
   * - MotivoDetalhes
     - string
   * - Itens
     - RmaPedidoItemRequest
     
.. list-table:: RmaPedidoItemRequest
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
   * - PartNumber
     - string
   * - SerialNumber
     - string
   * - Lacrado
     - bool
     
Consulta de detalhes de solicitação
===================================
# Quando o usuário consultar as solicitações, e selecionar alguma para ver os detalhes, será solicitado via GIAPI os seus detalhes (http://apidev.atma-it.com/Help/Api/GET-api-v1-rma-detalhes-srmId)

Atualização de status de RMA
============================
# O status de RMA pode ser atualizado via WebService através do método AtualizarStatus (https://atmab2b.readthedocs.io/pt_BR/latest/webservices-b2b/rma/AtualizacaoStatus.html)

  
