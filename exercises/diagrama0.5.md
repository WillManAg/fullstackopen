sequenceDiagram
    participant Navegador
    participant Servidor

    Navegador->>Servidor: GET /exampleapp/spa
    Servidor-->>Navegador: HTML

    Navegador->>Servidor: GET /exampleapp/main.css
    Servidor-->>Navegador: CSS

    Navegador->>Servidor: GET /exampleapp/spa.js
    Servidor-->>Navegador: JavaScript

    Note right of Navegador: El navegador ejecuta spa.js

    Navegador->>Servidor: GET /exampleapp/data.json
    Servidor-->>Navegador: JSON con las notas

    Note right of Navegador: El navegador renderiza las notas sin recargar la página