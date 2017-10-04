Produto
=======

Todos os produtos do site devem ser enviados através do webservice de produto.

O webservice permite cadastrar todas as características do produto. Também é possível editar as informações posteriormente via admin do Site B2B, mas o indicado é que todo produto venha pelo webservice primeiro.

Essas são as características principais de um produto:

.. list-table:: Propriedades da entidade
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - PartNumber
     - string
     - Código do produto no ERP. **Deve ser único.** 

       Além de servirem como chave primária, os Part Numbers são propriedades importantes para a busca de produtos pois muitos vendedores utilizam esse código para localizar os produtos.
   * - Nome
     - string(400)
     - Nome do produto. É o principal campo de busca além do Part Number, portanto deve ser bastante claro e amigável ao usuário.
   * - Ativo
     - bool
     - Indica se o produto está ativo no site. Produtos inativos não ficam visíveis na busca, nas vitrines e nem permitem a compra.
   * - DescricaoCurta
     - string
     - Descrição curta do produto. Apenas texto sem formatação.
   * - DescricaoCompleta
     - string
     - Descrição completa do produto. Conteúdo pode ser enviado com formatação HTML, permitindo a inclusão de imagens, vídeos e links para deixar a página bastante completa.
   * - FabricanteErpId
     - string
     - ErpId do fabricante do produto. Todo produto precisa ter um fabricante vinculado.
   * - CategoriaErpIds
     - string
     - ErpId das categorias do produto. Um produto pode estar vinculado a mais de uma categoria ao mesmo tempo.

Existem muitas outras propriedades nas entidades de produto. Os detalhes específicos estão na documentação de cada método.

Todo produto possui N variantes. Quando o cliente faz a compra no site, ele na verdade compra um dos variantes do produto.

**ATENÇÃO: Existem dois modos possíveis de lidar com produtos no Site B2B e esse modo deve ser escolhido antes da integração ser iniciada, devendo contatar a Atma para que nós possamos configurar corretamente seu ambiente da forma correta.**

Modo automático
--------------- 

O modo automático (padrão) parte do conceito de que os variantes são determinados pelo Centro de Distribuição (CD). Ou seja, o produto ABC-12345 terá um variante para cada CD cadastrado no Site B2B. 

O variante não possui um identificador exclusivo no ERP do cliente, sendo identificado pela combinação do Part Number do produto + Id do CD.

Nesse cenário a integração é um pouco mais simples pois são necessários menos métodos a serem integrados, visto que **a criação de variantes será automática no Site B2B no momento em que uma informação de estoque for enviada para o PartNumber + CD desejado.**

Modo manual
-----------

Parte do conceito de que os variantes possuem uma identificação única do lado do ERP. Ou seja, produto ABC-12345 pode ter inúmeros variantes por CD, todos eles com um Id exclusivo que é enviado para o ERP.

Nesse cenário a integração é mais complexa pois é necessária a integração com os métodos que manipulam os variantes.

**OBS: como padrão, o Site B2B vem no modo automático. Caso sua plataforma necessite controlar os variantes, entrar em contato com a Atma para que a configuração seja realizada.**


Métodos gerais
--------------

.. toctree::
   
   metodos/aguardodedisponibilidadedeprodutos.rst
   metodos/alterardisponibilidadedoproduto.rst
   metodos/createproduto.rst
   metodos/deleteproduto.rst
   metodos/desvinculardacategoria.rst
   metodos/desvinculartodosdacategoria.rst
   metodos/getproduto.rst
   metodos/updateproduto.rst
   metodos/vincularacategoria.rst

Métodos adicionais do modo manual
---------------------------------

.. toctree::

   metodos/alterardisponibilidadedovariante.rst
   metodos/alterarvisibilidadedevariantedoproduto.rst
   metodos/createprodutovariante.rst
   metodos/deleteprodutovariante.rst
   metodos/getvariante.rst
   metodos/updateprodutovariante.rst
