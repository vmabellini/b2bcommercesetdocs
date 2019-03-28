Processo de confirmação de pagamento
====================================

A partir da versão 17.2.0 do B2B (versão 0.9.85 da GIAPI) nós implementamos uma forma de poder cancelar os pedidos realizados no sistema em caso de erro ao efetuar o pagamento (plugins de cartão de crédito).
Essa mudança foi realizada para evitar o cenário de: usuário fecha o pedido com cartão - o cartão é cobrado - ocorre um erro na integração de pedido, fazendo com que seja necessário realizar um estorno do pagamento.
Para isso, primeiro realizamos a integração no ERP, depois o pagamento, e existe um método para notificarmos o ERP se o pagamento deu certo ou não.

Por isso realizamos as seguintes mudanças:

Ao fechar o pedido nós enviamos no objeto **PedidoRequest** uma propriedade chamada **StatusPagamentoPedido**. Essa propriedade pode ser enviada com dois valores:

- **NaoExigeConfirmacao** - significa que o pedido foi realizado com um plugin que não confirma o pagamento. É o valor padrão enviado hoje.
- **Pendente** - significa que o ERP deve integrar o pedido, porém deve aguardar a confirmação para que ele continue seu fluxo.

Quando o pedido é enviado como Pendente, o site irá enviar os dados de cartão de crédito para o respectivo gateway de pagamento, obter a resposta e então chamar um outro método da GI API: pedido/pagamento/status.
Esse método recebe o ID do pedido do site e o novo status, que pode ser:

- Confirmado - significa que o pagamento foi aprovado pelo Gateway e o pedido pode prosseguir no ERP
- Erro - significa que o pagamento não foi aprovado por algum motivo e por isso o pedido deve ser cancelado no ERP. O pedido também é cancelado automaticamente no site.

Para que esse novo fluxo funcione, é necessário entrar em contato com o suporte e pedir para que essa alteração seja ativada no site B2B após a GI API ter sido atualizada com o novo método.