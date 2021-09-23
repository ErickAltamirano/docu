## Metodos
--------------------------------

| Metodo      | URL |Descripcion                          |
| ----------- | --------------------------------- |------------------------------------ |
| `POST`      | http://localhost:8080/api/paciente|:material-check:     Crear paciente   |


Para crear un paciente se debe enviar en el BODY de la petición, la siguiente estructura en formato JSON.


| Parámetro | Tipo | Longitud | Descripción | Obligatorio|
| ------ | ------ | --------- | --------- | ------ |
| nombre| varchar|50 |Nombre del paciente |	Si |
| apellido|varchar |50 |Apellido del paciente |	Si |
|email | varchar| 50| 	Email del paciente| 	Si|
|fechaNacimiento |date | |Fecha de nacimiento del paciente en formato yyyy-MM-dd |	Si |
| celular| varchar|50 |Celular del paciente | Si|
| direccion| varchar|250 |Dirección del domicilio del paciente |Si |
| tipoIdentificacion|varchar |50 | Tipo de identificación (Cedula, Ruc).|Si |
| numeroIdentificacion|varchar |50 |Número de identificación del paciente |Si |
| genero|varchar |50 |Genero del paciente (F: Femenino, M: Masculino, O:Otros). |Si |
|telefono |varchar |50 |Número de teléfono del paciente |No |
|estadoCivil |object | |Objeto estado civil correspondiente al paciente. |Si |
| pacienteTipo|object | |Objeto del tipo de paciente que corresponde al paciente. |Si |
|responsable |object | |	Objeto responsable correspondiente al paciente. | Si|
|empresaId | number| |	Identificador interno de la empresa. |Si |
|convenio |object | |Objeto convenio correspondiente al paciente. |No |




### Nota:
* El responsable se puede crear con los datos del paciente, o en su defecto crear un responsable genérico para todos los pacientes.
* El identificador de la empresa debe ser solicitado al soporte técnico de DIMPACS.
* El convenio es obligatorio cuando se selecciona el tipo de paciente EMPRESARIAL.


## AUTHORIZATION Bearer Token

----------------------------------
| Parametro | Valor |
| ------ | ---- |
| Token | < token > |



## BODY raw
----------------------------------

    {
    "nombre": "Andrea",
    "apellido": "López",
    "email": "alopez@hotmail.com",
    "fechaNacimiento": "1962-01-02",
    "celular": "09999999",
    "direccion": "Quito",
    "tipoIdentificacion": "cedula",
    "numeroIdentificacion": "1700000000",
    "genero": "F",
    "telefono": "020000000",
    "estadoCivil": {
        "id": 1
    },
    "pacienteTipo": {
        "id": 2
    },
    "responsable": {
        "id": 1
    },
    "empresaId":1
    }






