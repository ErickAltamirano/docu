
## Metodos
---------------------------------------
| Metodo      | URL |Descripcion                          |
| ----------- | --------------------------------- |------------------------------------ |
| `GET`      | http://localhost:8080/api/estadoCivil |   Obtener listado de estados civiles   |

Devuelve un listado de estados civiles registrados en el sistema.

## AUTHORIZATION Bearer Token

----------------------------------
| Parametro | Valor |
| ------ | ---- |
| Token | < token > |

## Obtener listado de estados civiles
----------------------------------

    curl --location --request GET 'http://localhost:8080/api/estadoCivil'