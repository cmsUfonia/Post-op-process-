# Post-op-process-
```mermaid
graph TD
    A[Surgeon Lists Patient for Dora Call on Cerner] --> B{Patient Listed for Cataract Surgery and Routine Follow-up};
    B --> C[Bookings Team Schedules Dora Appointment on Cerner];
    C -- "Tuesday 11:30 AM Slot (Multiple Patients)" --> D[Patient Receives Pre-Call Information];
    D -- "Discharge Letter, Posters, Leaflets" --> E[Two Days Before Call: Dora Sends Text with Inbound Call Option];
    E --> F[One Week Before Call: BI/IT Sends Patient List to Ufonia];
    F --> G["Dora Conducts Automated Calls (Tuesday 11:30 AM)"];
    G -- "If no answer" --> H[Dora Attempts Second Call];
    H -- "Later on Tuesday" --> I[Ufonia Sends Outcome Spreadsheet to Nurses/Admin];
    I --> J{Nurses Review Outcomes};
    J -- "Patient Passed Call" --> K[Nurse Outcomes on Cerner];
    J -- "Failed, Incomplete, or DNA'd Call" --> L[Nurse Calls Patient Back];
    L -- "Patient now passes / No concerns" --> M[Nurse Outcomes on Cerner];
    L -- "Patient still has clinical concerns" --> N[Nurse Emails OPD Ophthalmology Inbox with Patient List];
    N --> O["Admin Team (Michelle, Lisa, Remy, Vicky) Monitors Inbox"];
    O --> P[Admin Schedules Consultant-Led Follow-up Appointment];
    P -- "Eventually transition to" --> Q[Nurse-Led Clinic for Follow-up];

    subgraph " "
        D
        E
    end
    linkStyle 0 stroke-width:0; style D stroke-width:0px; style E stroke-width:0px;

    subgraph " "
        F
        G
        H
    end
    linkStyle 0 stroke-width:0; style F stroke-width:0px; style G stroke-width:0px; style H stroke-width:0px;

    subgraph " "
        I
        J
        K
        L
        M
        N
        O
        P
        Q
    end
    linkStyle 0 stroke-width:0; style I stroke-width:0px; style J stroke-width:0px; style K stroke-width:0px; style L stroke-width:0px; style M stroke-width:0px; style N stroke-width:0px; style O stroke-width:0px; style P stroke-width:0px; style Q stroke-width:0px;


    %% External labels (adjust positioning as needed in the editor)
    style D fill:#fff,stroke:#fff,stroke-width:0px
    style E fill:#fff,stroke:#fff,stroke-width:0px
    style F fill:#fff,stroke:#fff,stroke-width:0px
    style G fill:#fff,stroke:#fff,stroke-width:0px
    style H fill:#fff,stroke:#fff,stroke-width:0px
    style I fill:#fff,stroke:#fff,stroke-width:0px
    style J fill:#fff,stroke:#fff,stroke-width:0px
    style K fill:#fff,stroke:#fff,stroke-width:0px
    style L fill:#fff,stroke:#fff,stroke-width:0px
    style M fill:#fff,stroke:#fff,stroke-width:0px
    style N fill:#fff,stroke:#fff,stroke-width:0px
    style O fill:#fff,stroke:#fff,stroke-width:0px
    style P fill:#fff,stroke:#fff,stroke-width:0px
    style Q fill:#fff,stroke:#fff,stroke-width:0px


    classDef externalLabel fill:#fff,stroke:#fff,font-weight:bold,text-align:right
    class R,S,T externalLabel

    R("   **Pre-Call Communication**"):::externalLabel
    S("   **Dora Call Execution**"):::externalLabel
    T("   **Outcome Management**"):::externalLabel

    D --> R
    E --> R
    F --> S
    G --> S
    H --> S
    I --> T
    J --> T
    K --> T
    L --> T
    M --> T
    N --> T
    O --> T
    P --> T
    Q --> T

    linkStyle 25,26,27,28,29,30,31,32,33,34,35,36,37 stroke-width:0px,fill:none,stroke:none;
