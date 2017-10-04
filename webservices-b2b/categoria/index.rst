Categoria
=========

Os webservices de categoria envolvem a criação, alteração, exclusão e listagem das categorias no Site B2B.

A entidade Categoria é bastante simples. É exigido que do lado do Erp cada categoria tenha seu próprio ID único (**ErpId**). Dessa forma podemos mapear as entidades entre os sistemas de forma simplificada.
Além disso, as categorias são organizadas em forma de árvore, geralmente com dois ou mais níveis (**ex: Informática > Impressoras**). Para tal, basta enviar em cada chamada ao **CreateCategoria** o **ErpId** da categoria pai no campo **ErpIdPai**.

**OBS: para que as categorias sejam criadas corretamente, é necessário criá-las na ordem correta dos níveis (ex: criar primeiro a categoria Informática antes de criar a sub-categoria Impressoras).**

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
