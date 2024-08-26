sequenceDiagram
    participant browser
    participant server
    participant user

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: HTML document
    deactivate server

    user->>browser: Writes note and clicks Save
    browser->>server: POST note
    activate server
    server-->>browser: Saving new note
    deactivate server

    browser->>user: Shows new note