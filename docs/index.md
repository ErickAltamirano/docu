

DIMPACS utiliza autenticación OAuth2, para obtener el token de acceso debe solicitar las credenciales de acceso al servidor, las cuales serán enviadas como parámetro en el header AUTHORIZATION de tipo BASIC AUTH, además deberá solicitar una cuenta de usuario, la cual será enviada en el BODY de la petición.

Si la solicitud es correcta retornara una estructura en formato JSON, en la cual encontrara el access_token, esta clave de acceso debe ser enviada como parámetro en el header AUTHORIZATION de tipo BEARER TOKEN en cada servicio que se consuma.

Nota: La clave de acceso (access_token) caduca cada 12 horas.



## Metodos
--------------------------------

| Metodo      | URL |Descripcion                          |
| ----------- | --------------------------------- |------------------------------------ |
| `POST`      | http://localhost:8080/oauth/token|:material-check:     Obtener token   |

## AUTHORIZATION Basic Auth

-------------------------------
| Parametro      | Valor                          |
| ----------- | ------------------------------------ |
| `Username`  |username  |
| `Password`  |password  |

## BODY urlencoded

-------------------------------------------------
| Parametro      | Valor                          |
| ----------- | ------------------------------------ |
| `username`  | recepcion|
| `password`  | 12345  |
| `grant_type` | password |






## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

