sequenceDiagram
    participant Navegador
    participant Servidor

    Navegador->>Servidor: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    Servidor-->>Navegador: Redirecciona a /notes

    Navegador->>Servidor: GET https://studies.cs.helsinki.fi/exampleapp/notes
    Servidor-->>Navegador: HTML de la página

    Navegador->>Servidor: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Servidor-->>Navegador: Archivo CSS

    Navegador->>Servidor: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Servidor-->>Navegador: Archivo JavaScript

    Note right of Navegador: El navegador ejecuta el JavaScript y pide las notas en JSON

    Navegador->>Servidor: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Servidor-->>Navegador: JSON con las notas

    Note right of Navegador: El navegador procesa los datos y muestra las notas en la página
