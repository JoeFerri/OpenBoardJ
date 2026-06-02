# Software System Specifications - Module 01

## NF

### Logging

#### SSS_NF_SW_LOG_001

* When the 10MB threshold is exceeded, the log file must be truncated while preserving the last 33% of the current content. The operation must be atomic and configurable via startup parameter or configuration file.
* Traceability
    * [REQ_NF_SW_LOG_001](REQ_M01.md#REQ_NF_SW_LOG_001)
    * [CON_NF_SW_LOG_001](CON_M01.md#CON_NF_SW_LOG_001)