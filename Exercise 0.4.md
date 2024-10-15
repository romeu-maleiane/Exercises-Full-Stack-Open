sequenceDiagram
  participant cliente
  participant browser as browser
  participant server as server
  
  cliente ->>+ browser: righting new note
  cliente ->>+ browser: click button submit
  browser ->>+ server: new note
  browser ->>+ server: GET https: //studies.cs.helsinki.fi/exampleapp/notes
  server -->>- browser: HTML docoment
  browser ->>+ server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  server -->>- browser: css file
  browser ->>+ server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
  server -->>- browser: javascript file
  browser->>+ server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
  server-->>- browser: {content: "7", date: "2024-10-15T21:33:07.672Z"}
