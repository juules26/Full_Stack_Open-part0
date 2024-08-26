sequenceDiagram
    participant user
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server-->>browser: HTML document
    deactivate server

    user->>browser: Writes new note and clicks Save
    activate browser
    browser->>browser: Updates HTML with new note
    deactivate browser
    browser-->>user: Displays new note