sequenceDiagram
  participant cliente
  participant browser as browser
  participant server as server
  
  cliente ->>+ browser: righting new note
  cliente ->>+ browser: click button submit
  Note right of browser: The SPA application's JavaScript handles the action and generates a new note locally
  browser ->>+ browser: Generate new note
  browser ->>+ server: Send new note
