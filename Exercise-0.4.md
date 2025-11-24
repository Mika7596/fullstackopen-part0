# New note diagram

```mermaid
sequenceDiagram
    autonumber
    participant  Browser
    participant  Server

    Note over Browser: The user writes a new note and clicks on "Save" button

    Browser->>Server: POST /exampleapp/new_note (body: data on the form)
    Note over Server: The server adds the current date to new note's body and saves the whole object
    Server-->>Browser: 302 Redirect a /exampleapp/notes

    Browser->>Server: GET /exampleapp/notes
    Server-->>Browser: HTML (notes)

    Browser->>Server: GET /exampleapp/main.css
    Server-->>Browser: main.css

    Browser->>Server: GET /exampleapp/main.js
    Server-->>Browser: main.js


    Browser->>Server: GET /exampleapp/data.json
    Server-->>Browser: data.json

    Note over Browser: Now all notes, including the new one, are being rendered
