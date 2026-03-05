#### Contenido para `ejercicio0.6.md`
```markdown
# Ejercicio 0.6: Nueva nota en SPA

```mermaid
sequenceDiagram
    participant usuario
    participant browser
    participant server

    usuario->>browser: Escribe nota y hace clic en "Save"
    Note right of browser: El JS añade la nota a la lista local y redibuja la UI
    
    browser->>server: POST [https://studies.cs.helsinki.fi/exampleapp/new_note_spa](https://studies.cs.helsinki.fi/exampleapp/new_note_spa)
    activate server
    Note left of server: El servidor recibe el JSON y lo guarda
    server-->>browser: 201 Created
    deactivate server
