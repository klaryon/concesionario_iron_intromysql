# Laboratorio Introducción MySql 

## Codigo base de datos Consesionario de coches - Ironhack Data Analysis
### Equipo 7: Paula, Esteban, Adrián, Clarissa

Como experto en datos, trabajas en una empresa de concesionarios de automóviles que vende coches nuevos de diversas marcas y modelos. Tu empresa es pequeña y nueva, pero tiene sucursales en varios países. Desde la fundación de la empresa, tus colegas han vendido varios coches a los clientes. Ahora tu jefe se ha dado cuenta de que tu empresa necesita imperativamente una base de datos para mantener registros sobre los coches, vendedores, clientes y facturas. Tu jefe confía mucho en ti, por lo que te ha asignado el desafío de diseñar, crear y gestionar la base de datos.

![Diagram](https://github.com/klaryon/concesionario_iron_intromysql/blob/main/Consesionario_database_image.png)

```sql
CREATE DATABASE Concesionario;

USE DATABASE Concesionario;
CREATE SCHEMA Concesionario_class;

CREATE TABLE Coches (
    ID INT,
    VIN VARCHAR(50),
    Fabricante VARCHAR(100),
    Modelo VARCHAR(50),
    Year INT,
    Color VARCHAR(50)
);

CREATE TABLE Clientes (
    ID INT,
    ClienteID VARCHAR(50),
    Nombre VARCHAR(100),
    Telefono VARCHAR(50),
    Mail VARCHAR(50),
    Direccion VARCHAR(50),
    Ciudad VARCHAR(50),
    Estado VARCHAR(50),
    Pais VARCHAR(50),
    CodigoPostal VARCHAR(50)
);

CREATE TABLE Vendedores (
    ID INT,
    Vendedor_ID VARCHAR(50),
    Vendedor_nombre VARCHAR(25),
    Vendedor_tienda VARCHAR(25)
);

CREATE TABLE Facturas (
    ID INT,
    Numero_fact INT,
    Fecha_fact VARCHAR(10),
    Coche VARCHAR(50),
    Cliente VARCHAR(50),
    Vendedor VARCHAR(50)
);

INSERT INTO Coches (ID, VIN, Fabricante, Modelo, Year, Color)
VALUES 
(0,'3K096I98581DHSNUP', 'Volkswagen', 'Tiguan', 2019, 'Azul'),
(1,'ZM8G7BEUQZ97IH46V', 'Peugeot', 'Rifter', 2019, 'Rojo'), 
(2,'RKXVNNIHLVVZOUB4M', 'Ford', 'Fusion', 2018, 'Blanco'), 
(3,'HKNDGS7CU31E9Z7JW', 'Toyota', 'RAV4', 2018, 'Plata'), 
(4,'DAM41UDN3CHU2WVF6', 'Volvo', 'V60', 2019, 'Gris'), 
(5,'DAM41UDN3CHU2WVF6', 'Volvo', 'V60 Cross Country', 2019, 'Gris');

INSERT INTO Clientes (ID, ClienteID, Nombre, Telefono, Mail, Direccion, Ciudad, Estado, Pais, CodigoPostal)
VALUES
(0, 10001, 'Pablo Picasso', '+34 636 17 63 82', '-', 'Paseo de la Chopera, 14', 'Madrid', 'Madrid', 'España', '28045'), 
(1, 20001, 'Abraham Lincoln', '+1 305 907 7086', 'ana.leon@gmail.com', '120 SW 8th St', 'Miami', 'Florida', 'Estados Unidos', '33130'), 
(2, 30001, 'Napoléon Bonaparte', '+33 1 79 75 40 00', '-', '40 Rue du Colisée', 'París', 'Île-de-France', 'Francia', '75008');


INSERT INTO Vendedores (ID, vendedor_id, vendedor_nombre,vendedor_tienda)
VALUES
(0, 00001,'Petey,Cruiser','Madrid'),
(1, 00002,'Anna Sthesia','Barcelona'),
(2, 00003,'Paul Molive','Berlín'),
(3, 00004,'Gail Forcewind','París'),
(4, 00005,'Paige,Turner','Mimia'),
(5, 00006,'Bob Frapples','Ciudad de México'),
(6, 00007,'Walter,Melon','Ámsterdam'),
(7, 00008,'ShondaLeer','São Paulo');

INSERT INTO Facturas (ID, Numero_fact, Fecha_fact, Coche, Cliente, Vendedor)
VALUES 
(0, 852399038,	'22-08-2018','0','1','3'),
(1, 731166526,	'31-12-2018','3','0','5'),
(2, 271135104,	'22-01-2019','2','2','7');
```
