Retornar opções de pagamento para outros plugins
================================================

** ATENÇÃO: a partir da versão 0.10.0 da GIAPI o método /prazoDePagamento foi descontinuado **
** Verificar a documentação do NOVO CHECKOUT **

A partir da versão 17.2.0 do Site B2B (versão 0.9.85 da GIAPI), implementamos mudanças na API de retorno de prazos de pagamento para que seja possível retornar opções para outros plugins de pagamento, além do tradicional Pagamento Faturado. Com isso, alguns plugins como Braspag e Moip podem ter seus totais calculados do lado do ERP e retornados via API de acordo com as regras de negócio específicas de cada cliente.

Eis abaixo a lista de mudanças:

- Instalar os plugins específicos que retornam os dados da API de prazoDePagamento. Eles são identificados pelo sufixo Faturado no nome de sistema. Por exemplo, temos um plugin chamado Payments.Braspag e outro chamado Payments.BraspagFaturado.
- É possível agora enviar um parâmetro "grupo" que identifica de qual plugin se refere aquele valor e opção de pagamento, assim como um outro parâmetro "ordemDeExibicao" que ordena de forma númerica as opções a serem listadas.
- O parâmetro "grupo" deve ser preenchido com o nome de sistema do plugin de pagamento. No caso, "Payments.BraspagFaturado" é o valor correto.
- Para os itens do plugin do pagamento Faturado tradicional, basta deixar o "grupo" vazio ou colocar como "Payments.Faturado".
- O campo "ordemDeExibicao" não é obrigatório mas é importante utilizá-lo para ordenar cada grupo e exibir os itens de forma organizada.

Retornar mensagens customizadas nas opções de pagamentos
========================================================

** ATENÇÃO: a partir da versão 0.10.0 da GIAPI o método /prazoDePagamento foi descontinuado **
** Verificar a documentação do NOVO CHECKOUT **

A partir da versão 18.15 do Site B2B, implementamos a opção de retornar mensagens customizadas a serem exibidas para o cliente nos métodos de pagamento na tela de finalizar pedido.

- Ao solicitarmos os prazos de pagamentos, se o retorno tiver uma lista de mensagens preenchidas com o Grupo contendo o nome do sistema do plugin, seu Tipo (Erro, Alerta, Info) e sua mensagem, será exibida uma mensagem de alerta ou erro para ele. Por exemplo, enviar uma resposta com o Grupo "Payments.BraspagFaturado", do Tipo "Erro", e a mensagem, será exibida essa mensagem apenas nesse método de plugin.
- Caso a mensagem tiver como Grupo "Global", a mensagem será exibida em todos os métodos de pagamento.
- Se o Grupo não for preenchido, a mensagem é atrelada a opção de pagamento faturado, mantendo a funcionalidade original antes da versão 18.15 do Site B2B.

Obs: O nome do plugin pode ser encontrado indo até a lista de plugins instalados no seu Site B2B: Painel de administração, Configurações, Formas De Pagamento. O nome a ser usado no grupo está na coluna "Nome do sistema".
