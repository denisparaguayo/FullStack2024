Part 0: Fundamentos de las aplicaciones web
0.4: Nueva nota

```
title 0.4: Nueva nota


    participant browser
    participant server

    note over browser
        El cliente agrega una nueva nota: "Hola desde Paraguay"
    end note

    browser->server: POST https://studies.cs.helsinki.fi/exampleapp/new_note

    note over server
        El servidor guarda una nueva nota
    end note

    note over browser
        El método POST recarga el navegador, generando una nueva llamada al servidor
    end note

    browser->server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    server-->browser: Código HTML
    browser->server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server-->browser: main.css
    browser->server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server-->browser: main.js

    note over browser
        El navegador comienza a ejecutar el código JavaScript
        que solicita datos JSON al servidor
    end note

    browser->server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->browser: [{ contenido: "HTML es fácil", fecha: "2019-05-23" }, ...]

    note over browser
        El navegador ejecuta el controlador de eventos
        que renderiza las notas para mostrarlas
    end note

```

![Imagen del Esquema](part0/nuevaNota.png)
