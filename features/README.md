# Documentazione Requisiti e Specifiche - OpenBoardJ

Sezione di tracciabilità di OpenBoardJ. Questa cartella è stata introdotta per gestire in modo strutturato l'evoluzione delle funzionalità, facilitando la manutenzione del codice e la comunicazione tra sviluppatori.

## Scopo
L'obiettivo di questa cartella è documentare i requisiti, i vincoli e le specifiche tecniche prima della loro implementazione nel core del progetto. Questo garantisce che ogni modifica sia pianificata, tracciabile e coerente con la filosofia del software originale.

## Codifica dei File
I file sono suddivisi per modulo (es. `M01` per il primo modulo analizzato) e categoria:
- `REQ_Mnn.md`: **Requisiti (Requirements)**. Definiscono *cosa* il sistema deve fare dal punto di vista funzionale o non funzionale.
- `SSS_Mnn.md`: **Specifiche Software (Software System Specifications)**. Definiscono *come* il requisito viene implementato tecnicamente.
- `CON_Mnn.md`: **Vincoli (Constraints)**. Definiscono i limiti ambientali o tecnologici che influenzano lo sviluppo (es. performance, I/O, compatibilità).

## Convenzione Naming
Ogni entità è identificata da un codice univoco nel formato:
`{TYPE}_{CAT}_{AREA}_{SUB}_{NNN}`

- **TYPE**: `REQ` (Requisito), `SSS` (Specifica), `CON` (Vincolo).
- **CAT**: `F` (Funzionale), `NF` (Non Funzionale).
- **AREA**: Categoria di sistema (es. `SW` per software, `DB` per database, `GUI` per interfaccia).
- **SUB**: Sottocategoria opzionale (es. `LOG` per logging, `UX` per esperienza utente).
- **NNN**: Contatore numerico a tre cifre.

## Protocollo di Analisi e Tracciabilità
Per garantire l'integrità del progetto, seguiamo un protocollo di tracciabilità bidirezionale:

1. **Definizione**: Ogni nuovo requisito (`REQ`) deve essere associato a una specifica (`SSS`) che ne descrive l'implementazione.
2. **Vincoli**: I vincoli (`CON`) fungono da base per la validazione delle specifiche.
3. **Hypertext Tracing**: Ogni file contiene link diretti agli elementi correlati.
   - I `REQ` linkano alle rispettive `SSS`.
   - Le `SSS` linkano ai `REQ` e ai `CON` di riferimento.
   - I `CON` restano indipendenti (definiscono il perimetro).

## Contributi e Workflow (Issue-based)

Per mantenere il progetto ordinato, non accettiamo modifiche dirette ai file di documentazione se non tramite il processo di revisione via **Issue**:

1. **Apertura Issue**: Se vuoi proporre un nuovo requisito o modificare uno esistente, apri una nuova *Issue* nel repository.
2. **Template Proposta**: Nell'issue, includi:
   - **Codifica**: Il codice del requisito (es. `REQ_NF_SW_LOG_001`).
   - **Descrizione**: Una breve spiegazione della necessità.
   - **Documentazione**: Il testo in formato Markdown che vorresti vedere nei file `REQ_Mnn.md`, `SSS_Mnn.md` o `CON_Mnn.md`.
   - **Impatto**: Indica quali file/specifiche verrebbero influenzati.
3. **Validazione**: la proposta deve essere validata, eventuali modifiche o chiarimenti verranno discussi direttamente nei commenti dell'issue.
4. **Accettazione/Chiusura**:
   - **Accettata**: La proposta viene integrata nei file ufficiali e l'Issue viene chiusa con un link al commit di aggiornamento.
   - **Rifiutata**: L'Issue viene chiusa motivando la decisione, mantenendo lo storico per future consultazioni.

