sequenceDiagram
    participant browser
    participant server


    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Response HTTP 201 Created
    deactivate server

    Note right of browser: The browser doesn't refresh for adding new note on the DOM.
    Note right of browser: The Javascript code adds a new note using the browser's API.
