# Specifiche Software - Modulo 01

## NF

### Logging

#### SSS_NF_SW_LOG_001

- Al superamento della soglia di 10MB, il file di log deve essere troncato preservando l'ultimo 33% del contenuto attuale. L'operazione deve essere atomica e configurabile tramite parametro di avvio o file di configurazione.

- Traccibilità
    - [REQ_NF_SW_LOG_001](REQ_M01.md#REQ_NF_SW_LOG_001)
    - [CON_NF_SW_LOG_001](CON_M01.md#CON_NF_SW_LOG_001)

