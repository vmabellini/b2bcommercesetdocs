Alterar status de RMA
=====================
O RMA pode ter seu status atualizado através do **Atualizar status**.

.. list-table:: Propriedades da entidade RmaStatusDTO
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Tipo
     - Descrição
   * - SrmId
     - string
     - Código do RMA no Erp. **Deve ser único**
   * - Rejeitado
     - bool
     - Sinaliza se está rejeitado ou não
   * - EtapaAtual
     - RmaEtapaDTO
     - Etapa atual do RMA
     
.. list-table:: Propriedades do enum RmaEtapaDTO
   :widths: auto
   :header-rows: 1

   * - Propriedade
     - Int
   * - Solicitacao
     - 10
   * - Analise
     - 20
   * - Conferencia
     - 30
   * - Encerrado
     - 40
