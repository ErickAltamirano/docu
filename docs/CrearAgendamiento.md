## Metodos
--------------------------------

| Metodo      | URL |Descripcion                          |
| ----------- | --------------------------------- |------------------------------------ |
| `POST`      | http://localhost:8080/api/agendamiento|:material-check:     Crear agendamiento   |

Para crear un agendamiento se debe enviar en el BODY de la petición, la siguiente estructura en formato JSON.


| Parámetro | Tipo | Longitud | Descripción | Obligatorio|
| ------ | ------ | --------- | --------- | ------ |
|descripcion|varchar|1000|Descripción del procedimiento a realizar en el estudio.|Si|
|fecha|varchar|50|Fecha a realizar el estudio|Si|
|hora|varchar|50|Hora a realizar el estudio|Si|
|medicoReferencista|object||Objeto médico referencista correspondiente al agendamiento.|Si|
|personalEquipo|object||Objeto personal-equipo correspondiente al agendamiento.|Si|
|pacientePersonal|object||Objeto paciente-personal correspondiente al agendamiento.|Si|
|usarConvenio|boolean||Variable utilizada para pacientes de tipo Empresarial|No|


### Nota:
* En caso de no utilizar médicos referencistas, seleccionar la opcion OTROS para todos los agendamientos.
* Para seleccionar el equipo al cual va dirigido el agendamiento se debe consultar en el servicio personal-equipo.
* El identificador del personal debe ser solicitado al soporte técnico de DIMPACS.

## AUTHORIZATION Bearer Token

----------------------------------
| Parametro | Valor |
| ------ | ---- |
| Token | < token > |



## BODY raw
----------------------------------

    {
    "descripcion":"RX PRUEBA",
    "fecha":"2021-01-01",
    "hora": "16:00",
    "medicoReferencista":{
        "id":1
    },
    "personalEquipo":{
        "id":2
    },
    "pacientePersonal":{
        "paciente":{
            "id":1
        },
        "personal":{
            "id":2
        }
    }
    }