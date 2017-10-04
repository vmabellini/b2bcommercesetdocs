Categoria
=========

Os webservices de categoria envolvem a criação, alteração, exclusão e listagem das categorias no Site B2B.

A entidade Categoria é bastante simples.

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - ErpId
     - string
     - Código da categoria no Erp. **Deve ser único**
   * - Descricao
     - string
     - Descrição da categoria a ser criada
   * - Nome
     - string
     - Nome da categoria exibido no Site B2B
   * - ErpIdPai
     - string
     - ErpId da categoria pai. Caso essa categoria seja uma categoria raiz, deve-se enviar como null.

Métodos:

.. toctree::
   
   metodos/createcategoria.rst
   metodos/updatecategoria.rst
   metodos/deletecategoria.rst
   metodos/getcategoria.rst
   metodos/listcategorias.rst
   metodos/alterardisponibilidadedacategoria.rst
