Revenda
=======

A integração de revendas envolve um número elevado de fluxos possíveis de integrações e por isso é necessária uma atenção especial ao desenvolver essa parte.

O diagrama abaixo ilustra o fluxo de cadastro de revenda:

.. image:: fluxo.png

Conceitos principais
--------------------

- **Toda revenda é criada via webservice apenas (exceto FastTrack)**
     Quando um cliente realiza o cadastro de sua revenda pelo Site B2B, a revenda não é criada automaticamente. Ao invés disso, ela é armazenada em uma tabela de pré-cadastro e seus dados são enviados via GIAPI para o ERP, para que ocorra o processo de análise e aprovação/rejeição seguindo o fluxo de cada cliente.
- **Toda revenda deve ter um usuário MASTER**
     A revenda em si é apenas uma entidade que representa uma empresa no sistema, mas quem efetua login e faz os pedidos são os **vendedores** da revenda. Por isso, toda revenda deve possuir um usuário MASTER.
     O usuário MASTER é o administrador daquela revenda e possui total acesso a todos as informações da revenda no Site B2B, bem como visualizar pedidos, comissões e também ter o poder de criar usuários CONVIDADOS.
- **Toda revenda pode possuir N usuários CONVIDADOS**
     Além do usuário MASTER que possui permissão total dentro da revenda, é possível que a revenda crie N usuários CONVIDADOS.
     Cada usuário CONVIDADO pode ter restrições específicas de acesso ao site, sendo que essas restrições são configuráveis via Admin do Site B2B.

FastTrack
---------

TODO: bazan

Criação de revenda
------------------

A partir da versão 17.5.0 do Site B2B nós criamos um novo método de criação de revenda chamado **CreateRevendaCompleta**.

O **CreateRevendaCompleta** é semelhante ao antigo **CreateRevenda**, com a diferença que ele recebe também durante a criação os endereços de Cobrança e Entrega. Dessa maneira nós evitamos uma série de problemas com revendas sem endereço, pois através desse método garantimos a atomicidade da operação validando os endereços essenciais. Na versão anterior, era necessário utilizar o método **SetRevendaEndereco** separadamente.