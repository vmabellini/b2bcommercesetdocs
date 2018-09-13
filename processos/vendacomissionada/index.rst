Venda Comissionada
==================

A plataforma B2B permite que um representante faça um pedido em nome de um terceiro e consiga colocar um preço personalizado afim de receber uma comissão.

Eis alguns detalhes de como funciona o processo:

    ** O ERP deve possuir e fornecer uma lista de clientes finais **

    O cliente final é buscado por ID, CNPJ e CPF.

    O Site B2B NÃO armazena os clientes finais em uma tabela própria. O cliente final SEMPRE é consultado via ERP.

    Para isso, deve-se implementar todos os métodos da GIAPI relacionados ao cliente final (/api/v1/clienteFinal).

    ** O ERP deve estar preparado para realizar os cálculos de frete, prazo de pagamento, preço e pedido para o cliente final **

    Para as APIs de frete, prazo de pagamento, preço e pedido, o B2B irá enviar os dados do cliente final em cada chamada.

    A integração deve estar preparada para receber essas informações e retornar os preços e totais ajustados de acordo com o cliente final.

    ** O módulo de comissões deve estar implementado **

    No http://apidev.atma-it.com/Help, existe a documentação do módulo de Comissões.

    Esses métodos devem ser implementados afim de que o representante possa alterar o preço de um produto no carrinho e a comissão a ser recebida seja apresentada corretamente.

    ** O cliente final pode ser cadastrado no momento da venda **

    O primeiro passo para realizar uma venda comissionada é informar o CNPJ ou CPF do cliente final.

    Esse CNPJ/CPF será consultado no ERP. Caso ele não exista, o Site B2B irá abrir um formulário de cadastro.

    Ao final do cadastro os dados do cliente final serão enviados para o ERP para serem armazenados.

    OBS: todos os métodos para esse fluxo também estão na api de cliente final (/api/v1/clienteFinal).