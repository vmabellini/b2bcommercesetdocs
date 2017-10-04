Fabricante
==========

Os webservices de fabricante envolvem a criação, alteração, exclusão e listagem dos fabricantes no Site B2B.

A entidade Fabricante é a mais simples de todas. É exigido que do lado do Erp cada fabricante tenha seu próprio ID único (**ErpId**). Dessa forma podemos mapear as entidades entre os sistemas de forma simplificada.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - ErpId
     - string
     - Código do fabricante no Erp. **Deve ser único**
   * - Descricao
     - string
     - Descrição do fabricante a ser criado
   * - Nome
     - string
     - Nome do fabricante exibido no Site B2B

Métodos
-------

.. toctree::
   
   metodos/createfabricante.rst
   metodos/updatefabricante.rst
   metodos/deletefabricante.rst
   metodos/getfabricante.rst
   metodos/listfabricante.rst
   metodos/alterardisponibilidadedofabricante.rst
