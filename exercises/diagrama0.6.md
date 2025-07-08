sequenceDiagram
    participant Navegador
    participant Servidor

    Note right of Navegador: El usuario escribe una nota y hace clic en Save

    Navegador->>Servidor: POST /exampleapp/new_note_spa (con JSON)
    Servidor-->>Navegador: 201 Created

    Note right of Navegador: La nota se agrega a la lista localmente (sin recargar)