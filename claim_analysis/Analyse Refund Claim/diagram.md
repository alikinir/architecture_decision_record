```mermaid
sequenceDiagram
actor Merchant_System
participant API_Gateway
participant Analysis_Workflow
participant Order_service
participant Enrichment_Orchestrator
participant Segmantation_Engine
participant Merchant_Config_RA
participant Policies_RA
participant Claims_RA
participant Classification_Engine
participant Analysis_Responses_RA
participant Outcome_Workflow


Merchant_System->>API_Gateway: Claim
activate API_Gateway
API_Gateway ->> Analysis_Workflow: Analyze(claim)



API_Gateway ->> Merchant_System: Recommendation

deactivate API_Gateway
```
