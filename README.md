# Post-op-process-
```mermaid
graph TD
    A[Surgeon Lists Patient for Dora Call on Cerner] --> B{Patient Listed for Cataract Surgery and Routine Follow-up};
    B --> C[Bookings Team Schedules Dora Appointment on Cerner];
    C -- "Tuesday 11:30 AM Slot (Multiple Patients)" --> D[Patient Receives Pre-Call Information];
    D -- "Discharge Letter, Posters, Leaflets" --> E[Two Days Before Call: Dora Sends Text with Inbound Call Option];
    E --> F[One Week Before Call: BI/IT Sends Patient List to Ufonia];
    F --> G[Dora Conducts Automated Calls (Tuesday 11:30 AM)];
    G -- "If no answer" --> H[Dora Attempts Second Call];
    H -- "Later on Tuesday" --> I[Ufonia Sends Outcome Spreadsheet to Nurses/Admin];
    I --> J{Nurses Review Outcomes};
    J -- "Patient Passed Call" --> K[Nurse Outcomes on Cerner];
    J -- "Failed, Incomplete, or DNA'd Call" --> L[Nurse Calls Patient Back];
    L -- "Patient now passes / No concerns" --> M[Nurse Outcomes on Cerner];
    L -- "Patient still has clinical concerns" --> N[Nurse Emails OPD Ophthalmology Inbox with Patient List];
    N --> O[Admin Team (Michelle, Lisa, Remy, Vicky) Monitors Inbox];
    O --> P[Admin Schedules Consultant-Led Follow-up Appointment];
    P -- "Eventually transition to" --> Q[Nurse-Led Clinic for Follow-up];

    subgraph Pre-Call Communication
        D
        E
    end

    subgraph Dora Call Execution
        F
        G
        H
    end

    subgraph Outcome Management
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
