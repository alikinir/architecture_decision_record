```mermaid
graph TD
    A[Start] --> B[Submit Refund/Return Claim]
    B --> C{Should Filter?}
    C -->|Yes| D[Filtered]
    C -->|No| E{First Time Seen?}
    E -->|No| F{Should Return Last Response?}
    F -->|Yes| G[Get Last Response]
    G --> H[Last Response]
    F -->|No| I[Duplicate]
    E -->|Yes| J[Get Related Order]
    J --> |Not Found| K[Error]
    J --> L[Analyze Claim]
    L --> M[Response]

```
