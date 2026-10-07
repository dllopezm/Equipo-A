# inventarioreto0 documentation
## Summary

- [Introduction](#introduction)
- [Database Type](#database-type)
- [Table Structure](#table-structure)
	- [ RAM](# ram)
	- [Placa base](#placa base)
	- [CPU](#cpu)
	- [GPU](#gpu)
	- [FUENTE ALIMENTACION](#fuente alimentacion)
	- [REFRIGERACIÓN](#refrigeración)
	- [ALMACENAMIENTO](#almacenamiento)
	- [PLACA DE EXPANSIÓN](#placa de expansión)
- [Relationships](#relationships)
- [Database Diagram](#database-diagram)

## Introduction

## Database type

- **Database system:** SQLite
## Table structure

###  RAM

| Name                  | Type         | Settings                       | References | Note |
| --------------------- | ------------ | ------------------------------ | ---------- | ---- |
| **id**                | INTEGER      | 🔑 PK, not null, autoincrement |            |      |
| **MARCA**             | VARCHAR(255) | null                           |            |      |
| **MODELO ESPECIFICO** | VARCHAR(255) | null                           |            |      |
| **NUMERO SERIE**      | VARCHAR(255) | null                           |            |      |
| **CAPACIDAD MB**      | INTEGER      | null                           |            |      |
| **VELOCIDAD MHz**     | INTEGER      | null                           |            |      |
| **VOLTAJE V**         | INTEGER      | null                           |            |      |
| **ESTADO**            | VARCHAR(255) | null                           |            |      |
| **CANTIDAD**          | NUMERIC      | null                           |            |      |
| **UBICACIÓN**         | VARCHAR(255) | null                           |            |      | 


### Placa base

| Name                       | Type         | Settings                   | References | Note |
| -------------------------- | ------------ | -------------------------- | ---------- | ---- |
| **id**                     | INTEGER      | 🔑 PK, null, autoincrement |            |      |
| **MARCA**                  | VARCHAR(255) | null                       |            |      |
| **MODELO**                 | VARCHAR(255) | null                       |            |      |
| **NUMERO SERIE**           | VARCHAR(255) | null                       |            |      |
| **Nº DE MODULOS RAM**      | INTEGER      | null                       |            |      |
| **Nº RAM COMPATIBLES**     | INTEGER      | null                       |            |      |
| **VELOCIDAD MAX  RAM MHz** | INTEGER      | null                       |            |      |
| **Nº DISCOS DUROS **       | INTEGER      | null                       |            |      |
| **TIPO PCI EXPRESS**       | INTEGER      | null                       |            |      |
| **SOCKET**                 | TEXT(65535)  | null                       |            |      |
| **COMPATIBILIDAD M.2**     | INTEGER      | null                       |            |      |
| **CANTIDAD**               | NUMERIC      | null                       |            |      |
| **UBICACIÓN**              | VARCHAR(255) | null                       |            |      | 


### CPU

| Name                         | Type         | Settings                       | References | Note |
| ---------------------------- | ------------ | ------------------------------ | ---------- | ---- |
| **id**                       | INTEGER      | 🔑 PK, not null, autoincrement |            |      |
| **MARCA**                    | VARCHAR(255) | null                           |            |      |
| **MODELO**                   | VARCHAR(255) | null                           |            |      |
| **SOCKET**                   | VARCHAR(255) | null                           |            |      |
| **NÚMERO DE IDENTIFICACIÓN** | VARCHAR(255) | null                           |            |      |
| **VELOCIDAD GHz**            | VARCHAR(255) | null                           |            |      |
| **VOLTAJE V**                | VARCHAR(255) | null                           |            |      |
| **NÚMERO DE NÚCLEOS**        | NUMERIC      | null                           |            |      |
| **NÚMERO DE HILOS**          | NUMERIC      | null                           |            |      |
| **NÚCLEOS EFICIENTES**       | NUMERIC      | null                           |            |      |
| **ESTADO**                   | VARCHAR(255) | null                           |            |      |
| **CANTIDAD**                 | NUMERIC      | null                           |            |      |
| **UBICACIÓN**                | VARCHAR(255) | null                           |            |      | 


### GPU

| Name             | Type         | Settings                       | References | Note |
| ---------------- | ------------ | ------------------------------ | ---------- | ---- |
| **id**           | INTEGER      | 🔑 PK, not null, autoincrement |            |      |
| **MARCA**        | VARCHAR(255) | null                           |            |      |
| **MODELO**       | VARCHAR(255) | null                           |            |      |
| **VRAM (Mb)**    | NUMERIC      | null                           |            |      |
| **TIPO MEMORIA** | VARCHAR(255) | null                           |            |      |
| **VERSIÓN PCI**  | VARCHAR(255) | null                           |            |      |
| **CANTIDAD**     | NUMERIC      | null                           |            |      |
| **UBICACIÓN**    | VARCHAR(255) | null                           |            |      | 


### FUENTE ALIMENTACION

| Name                     | Type         | Settings                       | References | Note |
| ------------------------ | ------------ | ------------------------------ | ---------- | ---- |
| **id**                   | INTEGER      | 🔑 PK, not null, autoincrement |            |      |
| **TAMAÑO**               | TEXT(65535)  | null                           |            |      |
| **POTENCIA CONSUMO W**   | NUMERIC      | null                           |            |      |
| **CERTIFICACIÓN 80PLUS** | TEXT(65535)  | not null                       |            |      |
| **CANTIDAD**             | NUMERIC      | null                           |            |      |
| **UBICACIÓN**            | VARCHAR(255) | null                           |            |      | 


### REFRIGERACIÓN

| Name                       | Type         | Settings                       | References | Note |
| -------------------------- | ------------ | ------------------------------ | ---------- | ---- |
| **id**                     | INTEGER      | 🔑 PK, not null, autoincrement |            |      |
| **TIPO**                   | VARCHAR(255) | null                           |            |      |
| **Nº VENTILADORES**        | NUMERIC      | null                           |            |      |
| **TAMAÑO  (mm)RADIADOR**   | VARCHAR(255) | null                           |            |      |
| **TAMAÑO VENTILADOR (mm)** | VARCHAR(255) | null                           |            |      |
| **CANTIDAD**               | NUMERIC      | null                           |            |      |
| **UBICACIÓN**              | VARCHAR(255) | null                           |            |      |
| ****                       |              | null                           |            |      | 


### ALMACENAMIENTO

| Name                                        | Type         | Settings                       | References | Note |
| ------------------------------------------- | ------------ | ------------------------------ | ---------- | ---- |
| **id**                                      | INTEGER      | 🔑 PK, not null, autoincrement |            |      |
| **MODELO**                                  | VARCHAR(255) | null                           |            |      |
| **TIPO**                                    | VARCHAR(255) | null                           |            |      |
| **VELOCIDAD TRANFERENCIA (Mb/seg)b**        | NUMERIC      | null                           |            |      |
| **VELOCIDAD TRVELOCIDAD LECTURA (Mb/seg)b** | NUMERIC      | null                           |            |      |
| **VELOCIDAD ESCRITURA(Mb/seg)b**            | NUMERIC      | null                           |            |      |
| **CAPACIDAD (Gb)**                          | VARCHAR(255) | null                           |            |      |
| **PUERTO **                                 | VARCHAR(255) | null                           |            |      |
| **CANTIDAD**                                | NUMERIC      | null                           |            |      |
| **UBICACIÓN**                               | VARCHAR(255) | null                           |            |      | 


### PLACA DE EXPANSIÓN

| Name               | Type         | Settings                       | References | Note |
| ------------------ | ------------ | ------------------------------ | ---------- | ---- |
| **id**             | INTEGER      | 🔑 PK, not null, autoincrement |            |      |
| **TIPO**           | VARCHAR(255) | null                           |            |      |
| **PUERTO**         | VARCHAR(255) | null                           |            |      |
| **NÚMERO PUERTOS** | NUMERIC      | null                           |            |      |
| **CANTIDAD**       | NUMERIC      | null                           |            |      |
| **UBICACIÓN**      | VARCHAR(255) | null                           |            |      | 


## Relationships


## Database Diagram

```mermaid
erDiagram
	 RAM {
		INTEGER id
		VARCHAR(255) MARCA
		VARCHAR(255) MODELO ESPECIFICO
		VARCHAR(255) NUMERO SERIE
		INTEGER CAPACIDAD MB
		INTEGER VELOCIDAD MHz
		INTEGER VOLTAJE V
		VARCHAR(255) ESTADO
		NUMERIC CANTIDAD
		VARCHAR(255) UBICACIÓN
	}

	Placa base {
		INTEGER id
		VARCHAR(255) MARCA
		VARCHAR(255) MODELO
		VARCHAR(255) NUMERO SERIE
		INTEGER Nº DE MODULOS RAM
		INTEGER Nº RAM COMPATIBLES
		INTEGER VELOCIDAD MAX  RAM MHz
		INTEGER Nº DISCOS DUROS 
		INTEGER TIPO PCI EXPRESS
		TEXT(65535) SOCKET
		INTEGER COMPATIBILIDAD M.2
		NUMERIC CANTIDAD
		VARCHAR(255) UBICACIÓN
	}

	CPU {
		INTEGER id
		VARCHAR(255) MARCA
		VARCHAR(255) MODELO
		VARCHAR(255) SOCKET
		VARCHAR(255) NÚMERO DE IDENTIFICACIÓN
		VARCHAR(255) VELOCIDAD GHz
		VARCHAR(255) VOLTAJE V
		NUMERIC NÚMERO DE NÚCLEOS
		NUMERIC NÚMERO DE HILOS
		NUMERIC NÚCLEOS EFICIENTES
		VARCHAR(255) ESTADO
		NUMERIC CANTIDAD
		VARCHAR(255) UBICACIÓN
	}

	GPU {
		INTEGER id
		VARCHAR(255) MARCA
		VARCHAR(255) MODELO
		NUMERIC VRAM (Mb)
		VARCHAR(255) TIPO MEMORIA
		VARCHAR(255) VERSIÓN PCI
		NUMERIC CANTIDAD
		VARCHAR(255) UBICACIÓN
	}

	FUENTE ALIMENTACION {
		INTEGER id
		TEXT(65535) TAMAÑO
		NUMERIC POTENCIA CONSUMO W
		TEXT(65535) CERTIFICACIÓN 80PLUS
		NUMERIC CANTIDAD
		VARCHAR(255) UBICACIÓN
	}

	REFRIGERACIÓN {
		INTEGER id
		VARCHAR(255) TIPO
		NUMERIC Nº VENTILADORES
		VARCHAR(255) TAMAÑO  (mm)RADIADOR
		VARCHAR(255) TAMAÑO VENTILADOR (mm)
		NUMERIC CANTIDAD
		VARCHAR(255) UBICACIÓN
		 
	}

	ALMACENAMIENTO {
		INTEGER id
		VARCHAR(255) MODELO
		VARCHAR(255) TIPO
		NUMERIC VELOCIDAD TRANFERENCIA (Mb/seg)b
		NUMERIC VELOCIDAD TRVELOCIDAD LECTURA (Mb/seg)b
		NUMERIC VELOCIDAD ESCRITURA(Mb/seg)b
		VARCHAR(255) CAPACIDAD (Gb)
		VARCHAR(255) PUERTO 
		NUMERIC CANTIDAD
		VARCHAR(255) UBICACIÓN
	}

	PLACA DE EXPANSIÓN {
		INTEGER id
		VARCHAR(255) TIPO
		VARCHAR(255) PUERTO
		NUMERIC NÚMERO PUERTOS
		NUMERIC CANTIDAD
		VARCHAR(255) UBICACIÓN
	}
```
