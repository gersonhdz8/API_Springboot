
# Proyecto API de Médicos
Descripción
Este proyecto es una API REST para la gestión de médicos, pacientes y consultas. Permite registrar, actualizar, eliminar y consultar la información de médicos y pacientes, así como agendar consultas médicas. La API está protegida con JWT (JSON Web Tokens) y utiliza Spring Security para la autenticación y autorización.


## Endpoints
#### Médicos

**POST** /medicos
Registra un nuevo médico en la base de datos.
Requiere autenticación.

**GET** /medicos
Obtiene el listado de médicos activos.
Requiere autenticación.

**PUT** /medicos
Actualiza los datos de un médico existente.
Requiere autenticación.

**DELETE** /medicos/{id}
Elimina (desactiva) un médico registrado.
Requiere autenticación.

**GET** /medicos/{id}
Obtiene los detalles de un médico por su ID.
Requiere autenticación.

#### Pacientes
**POST** /pacientes
Registra un nuevo paciente en la base de datos.
Requiere autenticación.

**GET** /pacientes
Obtiene el listado de pacientes activos.
Requiere autenticación.

**PUT** /pacientes
Actualiza los datos de un paciente existente.
Requiere autenticación.

**DELETE** /pacientes/{id}
Elimina (desactiva) un paciente registrado.
Requiere autenticación.

**GET** /pacientes/{id}
Obtiene los detalles de un paciente por su ID.
Requiere autenticación.

#### Consultas

**POST** /consultas
Registra una nueva consulta médica.
Requiere autenticación.

## Tecnologías Utilizadas

- Spring Boot
- Spring Security
- JWT (JSON Web Tokens)
- Spring Data JPA
- Flyway
- MySQL
- Maven


## Seguridad

La API utiliza JWT para la autenticación y autorización. Los usuarios deben autenticarse y recibir un token JWT, que debe ser incluido en el encabezado de las solicitudes a los endpoints protegidos.
Este proyecto utiliza Spring Security para gestionar la seguridad de los endpoints. A continuación, se describen los principales componentes de seguridad:

### Filtros de Seguridad
Filtro de Autenticación JWT: Se encarga de interceptar las solicitudes HTTP para verificar la presencia y validez del token JWT.

### Migraciones de Base de Datos
Flyway se utiliza para gestionar las migraciones de la base de datos. Las migraciones se encuentran en la carpeta src/main/resources/db/migration.

Cada archivo de migración debe seguir la convención de nomenclatura de Flyway, por ejemplo: V1__crear_tabla_medicos.sql.






