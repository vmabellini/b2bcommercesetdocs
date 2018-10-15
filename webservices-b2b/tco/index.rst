Calculadora TCO
===============

A calculadora TCO é uma funcionalidade que permite o usuário calcular seus gastos com impressora e receber recomendações de outras impressoras com todos os calculos de custos realizados.

Para que seja possível utilizar a calculadora TCO é necessário que os produtos sejam cadastrados com a flag IsTCO ligada (consulte :doc:`criar produto <../produto/metodos/createproduto>` ou :doc:`atualizar produto <../produto/metodos/updateproduto>`).

Após marcar as flags nos produtos principais é necessário cadastrar os acessórios que entraram no calculo do TCO.

Também é necessário cadastrar algumas caracteristicas ao produto, para que as recomendações possam ser feitas de acordo com a necessidade do cliente.

Os métodos do webservice que permitem realizar essas associações estão listados abaixo.

Métodos
-------

.. toctree::

   metodos/relacionaracessoriotco.rst
   metodos/atualizaracessoriotco.rst
   metodos/obteracessoriotco.rst
   metodos/removeracessoriotco.rst
   metodos/salvarcaracteristicasimpressoratco.rst
   metodos/obtercaracteristicasimpressoratco.rst
