# New note on SPA diagram

```mermaid
sequenceDiagram
    autonumber
    participant Browser
    participant Server

    Note over Browser: The user writes a new note and clicks on "saves" button



    Browser->>Server: POST /exampleapp/new_note_spa (JSON with the new note)
    Server-->>Browser: 201 Created (updated JSON)

    Note over Browser: spa.js adds the new note to the notes array
    Note over Browser: DOM is actualized without refreshing the web page
