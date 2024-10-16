sequenceDiagram
  participant cliente
  participant browser as browser
  participant server as server
  
  cliente ->>+ browser: Enter new note
  browser ->>+ server: POST request with new note
  server ->>+ browser: stores new note
  browser ->>+ cliente: update with new note
