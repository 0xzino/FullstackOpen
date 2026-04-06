```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User inputs into the text field and clicks on the save button
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa {"content":"Mangos are cool!","date":"2026-04-06T20:45:23.089Z"}

    activate server
    server-->>browser: {"message":"note created"}
    deactivate server

    Note right of browser: The browser redraws notes after pushing the submitted note from the form