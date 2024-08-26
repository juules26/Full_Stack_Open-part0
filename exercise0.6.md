sequenceDiagram
    participant user
    participant browser

    user->>browser: Writes new note and clicks Save
    activate browser
    browser->>browser: Updates HTML with new note
    deactivate browser
    browser-->>user: Displays new note

    1.write new note
    2.request sent to browser: url
        post method
        status: code created (message created)
        response: content added + date

headers: request url method POST
payload: data sent to server
response: data received from server