Trocas e devolução de mercadorias (SRM/RMA)
===========================================

Temos um módulo de trocas e devoluções que permite o usuário preencher uma lista de itens que ele deseja retornar, bem como os motivos.

A implementação desse módulo é bastante simples:

# Configurar os motivos possíveis de devolução através do Admin > Configuração > SRM > Motivos. Alguns motivos podem ou não solicitar os produtos, como em caso de troca por exemplo. O ID no ERP é um campo aberto que será enviado via GIAPI para facilitar a identificação do motivo cadastrado pelo site.

  .. image:: rma.png

# Ao acessar a tela do RMA, o usuário irá criar uma solicitação e irá selecionar o motivo. Após a criação da solicitação, a GIAPI irá receber todos os dados através da API de pedido RMA (http://apidev.atma-it.com/Help/Api/POST-api-v1-rma-pedido). O que nós esperamos em retorno é um ID que identifica essa solicitação no ERP, para que posteriormente possamos consultar o andamento desse RMA.
# Ao consultar o status de um RMA, o sistema chama a API http://apidev.atma-it.com/Help/Api/GET-api-v1-rma-detalhes-srmId, retornando qual a etapa atual dessa solicitação, os logs de ações efetuadas ao longo do tempo e também uma flag que indica se a solicitação foi rejeitada.
