Retornar opções de pagamento para outros plugins
================================================

A partir da versão 17.2.0 do Site B2B (versão 0.9.85 da GIAPI), implementamos mudanças na API de retorno de prazos de pagamento para que seja possível retornar opções para outros plugins de pagamento, além do tradicional Pagamento Faturado. Com isso, alguns plugins como Braspag e Moip podem ter seus totais calculados do lado do ERP e retornados via API de acordo com as regras de negócio específicas de cada cliente.

Eis abaixo a lista de mudanças:

- Instalar os plugins específicos que retornam os dados da API de prazoDePagamento. Eles são identificados pelo sufixo Faturado no nome de sistema. Por exemplo, temos um plugin chamado Payments.Braspag e outro chamado Payments.BraspagFaturado.
- É possível agora enviar um parâmetro "grupo" que identifica de qual plugin se refere aquele valor e opção de pagamento, assim como um outro parâmetro "ordemDeExibicao" que ordena de forma númerica as opções a serem listadas.
- O parâmetro "grupo" deve ser preenchido com o nome de sistema do plugin de pagamento. No caso, "Payments.BraspagFaturado" é o valor correto.
- Para os itens do plugin do pagamento Faturado tradicional, basta deixar o "grupo" vazio ou colocar como "Payments.Faturado".
- O campo "ordemDeExibicao" não é obrigatório mas é importante utilizá-lo para ordenar cada grupo e exibir os itens de forma organizada.