![agenciaimagen](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/e28e1bcc-9a59-4068-a63e-7fc5618a5949)


# Agencia de Viajes Mayorista ✈
 <br> 
 
## Temática del proyecto

Nuestro equipo de desarrollo esta trabajando en un sistema de gestión de reservas para una agencia de viajes mayorista. Nuestro objetivo es diseñar una base de datos eficiente que pueda manejar todas las operaciones relacionadas con las reservas, de una manera óptima y eficiente.

## Modelo de negocio:

**Gestión de Clientes y Empleados:** Necesitamos una base de datos que nos permita registrar la información de los clientes que realizan reservas en nuestra agencias, ya sea individuos o agencias de viaje. Ademas es esencial poder gestionar la información de los empleados involucrados en el proceso de reserva.

**Gestión de Reservas:** Necesitamos un sistema que pueda registrar cada reserva realizada, incluyendo la fecha y la hora de la reserva, el cliente que la realizó, el empleado encargado de dicha reserva y que viaje reservó.

**Gestión de Viajes y Paquetes Turísticos:** Es importante poder clasificar y organizar los diferentes viajes y paquetes turísticos que ofrecemos, incluyendo detalles sobre, nombre, descripción, fechas y precio.
**Gestión de Proveedores y Servicios:** La base de datos debe permitirnos registrar y gestionar la información de los proveedores de servicios turísticos, como aerolíneas y hoteles.

**Registro de inscripciones a Paquetes:** Registra la inscripción de los clientes a los diferentes paquetes turísticos ofrecidos.

## Objetivo:
Diseñar e implementar una base de datos relacional que satisfaga todas las necesidades de gestión de reservas para nuestra agencia de viajes. Esta base de datos deberá ser eficiente, escalable y fácil de mantener, permitiendo una gestión ágil y precisa de todas las operaciones relacionadas con las reservas y la oferta de paquetes turísticos.

## Diagrama entidad relación (DER)

![DERAgenciaViajes](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/08069573-26b5-4146-8ddd-8e1fc4580116)

## Listado de Tablas

1.1 Tabla Cliente

1.2 Tabla Empleado

1.3 Tabla Reserva

1.4 Tabla Viaje

1.5 Tabla Reserva_Hotel

1.6 Tabla Hotel

1.7 Tabla Reserva_Vuelo

1.8 Tabla Vuelo

1.9 Tabla Cliente_Tour_Paquete

1.10 Tabla Tour_Paquete

1.11 Tabla Tour_Paquete_Viaje


## 1.1 Tabla Cliente

La tabla Cliente muestra información de todos los clientes.

La primary key de la tabla Cliente aparece como foreign key en las tablas, Reserva y Cliente_Tour_Paquete.

La tabla Cliente se une a la tabla Tour_Paquete mediante la tabla Cliente_Tour_Paquete.

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 26 52](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/3533b159-6569-43ec-8b1a-5ffb7f587027)


## 1.2 Tabla Empleado

La tabla Empleado muestra información de todos los empleados de la agencia que trabajan en atención al cliente, en reservas de viajes.

La primary key de la tabla Empleado aparece como foreign key en la tabla Reserva.

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 27 35](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/1fa8930d-bb12-4eeb-9931-cbba888d719b)


## 1.3 Tabla Reserva

La tabla Reserva contiene información de las reservas de viajes hechas por un cliente.

La primary key de la tabla Reserva aparece como foreign key en las tablas Reserva_Vuelo y Reserva_Hotel.

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 28 19](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/43c31042-e2e7-4e69-a2ae-fdb620b080be)


## 1.4 Tabla Viaje

La tabla Viaje representa un conjunto específico de servicios turísticos que la agencia de viajes organiza y ofrece.

La primary key de la tabla Viaje aparece como foreign key en las tablas Reserva y Tour_Paquete_Viaje.

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 28 49](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/a57d12de-9305-4ce3-8186-97f16d5703cc)


## 1.5 Tabla Reserva_Hotel

La tabla Reserva_Hotel es una tabla intermedia entre Reserva y Hotel.

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 29 29](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/f3750ad8-95dd-42a5-b784-d870095786ec)

## 1.6 Tabla Hotel

La tabla Hotel contiene la información relevante de los Hoteles.

La primary key de la tabla Hotel aparece como foreign key en la tabla intermedia Reserva_Hotel.

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 29 56](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/c0b76852-20d4-453d-91a9-0aa79fc69699)

## 1.7 Tabla Reserva_Vuelo

La tabla Reserva_Vuelo es una tabla intermedia entre Reserva y Vuelo.


### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 30 42](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/f54a0a63-5c46-484d-8850-f52a22743d34)

## 1.8 Tabla Vuelo

La tabla contiene información relevante de los vuelos.

La primary key de la tabla Vuelo aparece como foreign key en la tabla intermedia Reserva_Vuelo.

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 31 24](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/48afb241-8970-47eb-a29b-7291698efa6a)


## 1.9 Tabla Tour_Paquete

La tabla contiene información sobre los distintos paquetes de tour que se pueden hacer en determinado destino.

La primary key de la tabla Tour_Paquete aparece como foreign key en las tablas intermedias Cliente_Tour_Paquete y Tour_Paquete_Viaje.

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 32 13](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/c8d635ce-3b85-4c5b-b14c-6c6cbe707622)

## 1.10 Tabla Cliente_Tour_Paquete

La tabla Cliente_Tour_Paquete es una tabla intermedia entre Cliente y Tour_Paquete

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 19 59 50](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/ab236ce9-65e0-45d3-998a-aabd0bf5f140)

## 1.11 Tabla Tour_Paquete_Viaje

La tabla Tour_Paquete_Viaje es una tabla intermedia entre Viaje y Tour_Paquete

### Columnas

![Captura de pantalla 2024-07-01 a la(s) 20 01 16](https://github.com/MartinMasde/proyecto-agencia-viajes-masdeayala/assets/132627081/fa641c38-fa01-40fc-bcd5-15386271c4f7)


## Estructura e ingesta de datos
* Se realiza principalmente por medio del archivo data_ingestion.sql
* Las carga de las tablas: Cliente, Cliente_Tour_Paquete, Empleado, Hotel, Reserva, Reserva_Hotel, Reserva_Vuelo, Tour_Paquete, Tour_Paquete_Viaje, Viaje y Vuelo se realizan por medio de sus archivos .csv respectivos, dichos archivos se encuentran en el directorio ./structure/data-csv

## Objetos de la base de datos


### Documentación de Vistas

### Vista: ReservasCliente

**Descripción:** Esta vista muestra las reservas de viajes realizadas por un cliente en especifico, se muestran en orden ascendente por fecha de reserva.

**Columnas:**

* **NombreCompleto:** El nombre y el apellido del cliente
* **Dirección:** La dirección del cliente
* **Teléfono:** El número de teléfono del cliente
* **Email:** La dirección de correo electrónico del cliente
* **TipoCliente:** Si el cliente es una persona física o una agencia de viajes
* **FechaReserva:** La fecha en que fue realizada la reserva
* **Destino:** El destino de viaje elegido por el cliente
* **FechaSalida:** La fecha en la que iniciará el viaje
* **FechaRegreso:** La fecha en la que finalizará el viaje
* **DescripcionViaje:** Una pequeña descripción del viaje elegido por el cliente
* **Precio:** El importe en dolares del viaje

**Ejemplo de consulta:**

```sql
SELECT * FROM ReservasCliente
WHERE NombreCompleto = 'Xerxes Dukes';
```

### Vista: DestinoConMasReservas

**Descripción:** Esta vista mostrara los destinos de viaje con mas reservas realizadas.

**Columnas:**

* **Destino:** El destino del viaje
* **TotalReservas:** La cantidad de reservas hechas

**Ejemplo de consulta:**

```sql
SELECT * FROM DestinoConMasReservas
ORDER BY TotalReservas ASC;
```

### Vista: CantidadReservasPorEmpleado

**Descripción:** Esta vista mostrara la cantidad de reservas de viajes hechas por cada empleado.

**Columnas:**

* **Nombre:** El nombre del empleado que hizo la reserva 
* **Email:** La dirección de correo electrónico del empleado
* **TotalReservas:** La cantidad de reservas realizadas

**Ejemplo de consulta:**

```sql
SELECT * FROM CantidadReservasPorEmpleado 
ORDER BY TotalReservas DESC;
```

### Vista: ClientesConMenosReservas

**Descripción:** Esta vista muestra los 10 clientes con menos reservas realizadas.

**Columnas:**

* **idCliente:** El id del cliente
* **Nombre:** El nombre del cliente
* **Apellido:** El apellido del cliente
* **TotalReservas:** El total de las reservas realizadas

**Ejemplo de consulta:**

```sql
SELECT * FROM ClientesConMenosReservas;
```
### Vista: ClientesConMasReservas

**Descripción:** Esta vista muestra los 10 clientes con mas reservas realizadas.

**Columnas:**

* **idCliente:** El id del cliente
* **Nombre:** El nombre del cliente
* **Apellido:** El apellido del cliente
* **TotalReservas:** El total de las reservas realizadas

**Ejemplo de consulta:**

```sql
SELECT * FROM ClientesConMasReservas;
```

## Documentación de Funciones

### Función: reservas_empleado_periodo

**Descripción:** Esta función cuenta la cantidad de reservas de viajes realizada por un empleado en un intervalo de tiempo determinado.

**Parámetros:**

* **empleado_id:** Identificador único del empleado
* **fecha_inicio:** Fecha de inicio del intervalo (formato YYYY-MM-DD)
* **fecha_fin:** Fecha de fin del intervalo (formato YYYY-MM-DD)

**Retorno:**

* Número total de reservas realizadas por el empleado en el intervalo de tiempo especificado.

**Ejemplo de uso:**

```sql
SELECT reservas_empleado_periodo(1, '2024-01-01', '2024-03-31');
```

### Función: CalcularPrecioConDescuento

**Descripción:** Esta función dado un id de un Hotel y un intervalo de fechas en las que el huesped desea alojarse, calcula si son mas de 5 noches y aplica un descuento de 10% al precio por noche, en caso de ser menos de 5 noches se mantiene el precio original.

**Parámetros:**

* **Hotel_id:** Identificador único del Hotel
* **FechaCheckIn:** Fecha de inicio de la estadia en el Hotel (formato YYYY-MM-DD)
* **FechaCheckOut:** Fecha de fin de la estadia en el Hotel (formato YYYY-MM-DD)

**Retorno:**

* Nombre del Hotel, el precio original y el precio por noche con descuento si este correspondiera, de acuerdo a la cantidad de noches de hospedaje.

**Ejemplo de uso:**

```sql
SELECT 
    H.Nombre,
    H.PrecioPorNoche,
    CalcularPrecioConDescuento(H.idHotel, '2023-12-01', '2023-12-10') AS PrecioPorNocheConDescuento
FROM 
    Hotel H
WHERE 
    H.idHotel = 5;
```

## Documentación de Procedimientos Almacenados

### Procedimiento: sp_nueva_reserva

**Descripción:** Este procedimiento crea una nueva reserva en la base de datos.

**Parámetros:**

* **p_fechaViaje:** La fecha del viaje a realizar
* **p_idCliente:** Identificador del cliente que hace la reserva
* **p_idViaje:** Identificador del viaje que va a reservar
* **p_idEmpleado:** Identificador del empleado encargado de hacer la reserva

**Retorno:**

* El ID de la reserva realizada con éxito o un mensaje de error.

**Ejemplo de uso:**

```sql
CALL sp_nueva_reserva('2024-08-01', 30, 2, 4);
```

### Procedimiento: sp_agregar_cliente

**Descripción:** Este procedimiento agrega un nuevo cliente a la base de datos.

**Parámetros:**

* **p_Nombre:** El nombre del cliente
* **p_Apellido:** El apellido del cliente
* **p_Direccion:** La dirección del cliente
* **p_Telefono:** El teléfono del cliente
* **p_Email:** La dirección de correo electrónico del cliente
* **p_TipoCliente:** Que tipo de cliente es, agencia o persona

**Retorno:**

* El ID del cliente agregado con éxito o un mensaje de error.

**Ejemplo de uso:**

```sql
CALL sp_agregar_cliente ('Martin', 'Mas', 'Chucarro 1168', '777-777-7777', 'martin@email.com', 'Persona');
```

### Procedimiento: sp_eliminar_cliente

**Descripción:** Procedimiento utilizando TCL (Transactional Control Language), este procedimiento elimina un cliente de la base de datos mientras dicho cliente no tenga reservas asociadas.

**Parámetros:**

* **p_idCliente:** El identificador del cliente a eliminar

**Retorno:**

* Un mensaje de exito al eliminarlo, un mensaje indicando que el cliente tiene reservas asociadas y no se puede eliminar o un mensaje de error.

**Ejemplo de uso:**

```sql
CALL sp_eliminar_cliente (19);
```

## Documentación de Triggers

### Trigger: trg_after_update_reserva

**Descripción:** Este trigger registra las modificaciones (UPDATE) en las Reservas en la tabla Log_Auditoria.

**Detalles:**

* **Tabla afectada:** Reserva
* **Acción:** UPDATE
* **Información registrada:** NombreTabla, NombreColumna, ValorAnterior, ValorNuevo, Usuario, FechaActualizacion

**Ejemplo:**

* Se actualiza una reserva.
* El trigger registra la acción en la tabla Log_Auditoria con los detalles correspondientes.

### Trigger: trg_before_insert_empleado

**Descripción:** Este trigger al registrar un nuevo empleado verifica que su email no este repetido.

**Detalles:**

* **Tabla afectada:** Empleado
* **Acción:** INSERT
* **Validación:** Correo electrónico único

**Ejemplo:**

* Se intenta insertar un nuevo empleado con un email ya registrado.
* El trigger genera un error y la inserción no se realiza.

## Roles y Permisos
`./objects/roles_users.sql`

Se general tres roles:

1. `administrador`: Este rol tiene todos los permisos en la base de datos.
2. `encargado`: Este rol tiene permisos para generar CRUD en todas las tablas.
2. `empleado`: Este rol tiene permisos para SELECT, INSERT y UPDATE en las tablas.

Se crea un usuario con el rol administrador.

Se crea un usuario con el rol encargado.

Se crean dos usuarios con el rol empleado.

## Back up de la base de datos

Se puede ejecutar un backup de manera manual con el comando `make backup-db`, y se almacenara en la carpeta back-up. 

## Herramientas y tecnologias usadas
* Makefile (para generar una interfaz sencilla de procesos)
* Docker (para generar un container)
* MySQL (Motor de bases de datos `version: latest`)
* MySQL Workbench (Interfaz grafica)
* Mockaroo (para otorgar datos ficticios)
* Visual Studio Code (para editar el código)

## Como levantar el proyecto en CodeSpaces GitHub
* env: Archivo con contraseñas y data secretas
* Makefile: Abstracción de creación del proyecto
* docker-compose.yml: Permite generar las bases de datos en forma de contenedores

#### Pasos para arrancar el proyecto

* En la terminal de linux escribir :
    - `make` _si te da un error de que no conexion al socket, volver al correr el comando `make`_
    - `make clean-db` limpiar la base de datos
    - `make test-db` para mirar los datos de cada tabla
    - `make backup-db` para realizar un backup de mi base de datos
    - `make access-db` para acceder a la base de datos

