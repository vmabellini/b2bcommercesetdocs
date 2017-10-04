Revenda
=======

A integração de revendas envolve um número elevado de fluxos possíveis de integrações e por isso é necessária uma atenção especial ao desenvolver essa parte.

Criação de revenda
------------------

A partir da versão 17.5.0 do Site B2B nós criamos um novo método de criação de revenda chamado **CreateRevendaCompleta**.

O **CreateRevendaCompleta** é semelhante ao antigo **CreateRevenda**, com a diferença que ele recebe também durante a criação os endereços de Cobrança e Entrega. Dessa maneira nós evitamos uma série de problemas com revendas sem endereço, pois através desse método garantimos a atomicidade da operação validando os endereços essenciais. Na versão anterior, era necessário utilizar o método **SetRevendaEndereco** separadamente.