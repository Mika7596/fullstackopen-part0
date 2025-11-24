# SPA diagram

```mermaid
sequenceDiagram
    autonumber
    participant Browser 
    participant Server 

    Browser->>Server: GET /exampleapp/spa
    Server-->>Browser: HTML (spa)

    Browser->>Server: GET /exampleapp/main.css
    Server-->>Browser: main.css

    Browser->>Server: GET /exampleapp/spa.js
    Server-->>Browser: spa.js
    Note over Browser: The browser executes spa.js
    Browser->>Server: GET /exampleapp/data.json
    Server-->>Browser: data.json (notas)

    Note over Browser: The notes are being shown without refreshing or rerendering the web page (by the server).
