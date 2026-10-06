# FitZone API Testing

## Descripción

Proyecto de pruebas de API REST realizado como ejercicio práctico de QA
Functional / API Testing sobre una aplicación ficticia de gestión de socios,
clases y reservas de un gimnasio.

El proyecto utiliza Postman para el diseño y ejecución de pruebas,
Newman para la ejecución Data Driven y Mock Server para simular respuestas
del backend.

## Objetivo

Validar el comportamiento de diferentes recursos de la API mediante pruebas
funcionales, pruebas CRUD, encadenamiento de solicitudes, validación de datos
y consumo de un Mock Server.

## Herramientas utilizadas

- Postman
- Newman
- REST API
- JSON Server
- Visual Studio Code
- Git
- GitHub
- HTTP / JSON
- CSV para pruebas Data Driven

## Pruebas realizadas

### CRUD y pruebas encadenadas

Se realizaron operaciones sobre los recursos de la API:

- GET
- POST
- PUT
- PATCH
- DELETE

También se implementó encadenamiento de solicitudes mediante variables de
colección, por ejemplo utilizando el ID generado al crear un recurso.

### Consultas

Se realizaron consultas para:

- Listar socios.
- Buscar un socio por ID.
- Filtrar socios por plan PLUS.

### Data Driven Testing

Se utilizaron datos externos mediante un archivo CSV con diferentes
combinaciones de datos válidos e inválidos.

Se validaron:

- Plan permitido.
- Rango de edad.
- Formato del correo electrónico.
- Correspondencia entre la validez esperada del CSV y la respuesta obtenida.

La ejecución con Newman realizó:

- 12 iteraciones.
- 12 solicitudes.
- 24 assertions.
- 0 fallos.

## Mock Server

Se creó un Mock Server de FitZone utilizando Examples de Postman para el
recurso `clases`.

Se implementaron ejemplos para:

- GET - Listar clases.
- GET - Obtener clase por ID.
- POST - Crear clase.
- PUT - Reemplazar clase.
- PATCH - Modificar clase.
- DELETE - Eliminar clase.

También se realizó el consumo del Mock Server mediante un archivo
`consumo-mock.http`.

## Estructura del proyecto

```text
Reto-Modulo2/
│
├── ejercicio1/
│   └── servicio-fitzone/
│       ├── db.json
│       ├── db.seed.json
│       ├── Reto-FitZone.json
│       ├── Reto-FitZone-Mock.JSON
│       ├── socios-data.csv
│       ├── mock-url.txt
│       └── consumo-mock.http
│
└── ejercicio2/
    ├── Capturas/
    ├── consumo-mock.http
    ├── Mock-FitZone.postman_collection.json
    └── mock-url.txt