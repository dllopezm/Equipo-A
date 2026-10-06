# Ficha del gestor: SQLite

Equipo A · Integrantes: Angel, Lorenzo, Lanzarote, Alex

## 1\. Qué es 

| \# | Campo | Respuesta | Fuente (URL) |
| :---- | :---- | :---- | :---- |
| 1 | Quién lo desarrolla y desde cuándo. ¿Nació de otro producto? | SQLite fue creado por D. Richard Hipp en el año 2000\. Nació por la necesidad de tener una base de datos embebida y sin servidor, para sustituir problemas que tenían con Informix. Su primera versión (SQLite 1.0) salió el 17 de agosto del 2000\. | [SQLite Developers](https://www3.sqlite.org/matrix/crew.html) |
| **2** | Licencia: libre o de pago. Cuál exactamente. ¿Hay versión gratuita? ¿Ha cambiado de licencia? (apartado 6\) | Licencia: SQLite es gratuito y de dominio público (Public Domain). No necesita una licencia para utilizarlo, modificarlo o distribuirlo. No tuvo cambios de licencia. | [SQLite Copyright](https://www.sqlite.org/copyright.html)  |
| 3 | Dos empresas u organizaciones conocidas que lo usan | Apple y Microsoft son dos empresas conocidas que usan SQLite. | w[Well-Known Users Of SQLite](https://www.sqlite.org/famous.html)  |

## 2\. Cómo guarda los datos

| \# | Campo | Respuesta | Fuente (URL) |
| :---- | :---- | :---- | :---- |
| **4** | Modelo de datos: relacional (tablas), documental, clave-valor, columnar, de grafos… (apartado 4\) | Es un modelo relacional. La información se organiza en diversas tablas interrelacionadas. | [https\://www\.ibm.com/think/topics/relational-databases](https://www.ibm.com/think/topics/relational-databases) |
| 5 | Cómo quedaría el equipo EQ-04, con sus dos módulos de RAM, guardado en este gestor. Un dibujo o un ejemplo | ![image1](https://github.com/dllopezm/Equipo-A/blob/Proyecto-0/GBD/bd/Captura%20de%20pantalla%202026-10-06%20130644.png)| El ejemplo está hecho por mí ©Lorenzo |
| 6 | ¿Hay que definir la estructura antes de guardar datos (esquema fijo) o no? | Hay que hacerlo con un esquema fijo/definido | [https\://sqlite.org/lang\_createtable.html](https://sqlite.org/lang_createtable.html) |

## 3\. Dónde vive

| \# | Campo | Respuesta | Fuente (URL) |
| :---- | :---- | :---- | :---- |
| **7** | Dentro de la aplicación (embebido), en un servidor al que se conectan los clientes, o como servicio en la nube (apartado 5.1) | SQLite fue diseñado exclusivamente para esto. "Embebido" significa que la base de datos forma parte de tu propio programa. No utiliza la arquitectura cliente-servidor ni funciona como un servicio independiente. En su lugar, el motor de la base de datos se integra directamente en el código de la aplicación y gestiona los datos guardándolos en un único archivo ordinario en el disco local.  | [https\://sqlite.org/about.html](https://sqlite.org/about.html) |
| 8 | ¿Puede repartir o copiar los datos entre varias máquinas? ¿Cómo se llama eso en este gestor? (apartado 5.2) | **No de forma nativa.** Al ser un archivo local, no incluye replicación distribuida de fábrica. Sin embargo, se puede lograr mediante herramientas externas de terceros como **LiteFS**, **rqlite** o **dqlite** (sistemas de bases de datos distribuidas basadas en SQLite).  | [https\://sqlite.org/about.html](https://sqlite.org/about.html)  |
| 9 | Sistemas operativos en los que funciona | **Multiplataforma.** Funciona en prácticamente cualquier sistema operativo, incluyendo **Windows, macOS, Linux, Android, iOS** | [https\://sqlite.org/about.html](https://sqlite.org/about.html)    |

## 

## 4\. Qué ofrece como gestor

| \# | Campo | Respuesta | Fuente (URL) |
| :---- | :---- | :---- | :---- |
| **10** | Lenguaje: ¿SQL u otro? Un ejemplo de cómo se pide «el equipo EQ-04» (apartado 3.3) | Utiliza SQL estándar. Un ejemplo de consulta sería: SELECT \* FROM equipos WHERE id \= 'EQ-04';   | [https\://www\.sqlite.org/](https://www.sqlite.org/)  |
| 11 | ¿Tiene transacciones? ¿Cumple ACID del todo, en parte o no? (apartado 3.2) | Sí, tiene transacciones y cumple ACID del todo. Es un motor transaccional completamente conforme con ACID (Atomicidad, Consistencia, Aislamiento y Durabilidad) de forma nativa.  | [https\://www\.sqlite.org/transactional.html](https://www.sqlite.org/transactional.html)  |
| 12 | ¿Tiene usuarios y permisos propios? (apartado 3.4) | No. Como es una base de datos simple que se guarda en un solo archivo, no tiene una pantalla para crear usuarios ni contraseñas dentro de ella. Quien controle el archivo desde el ordenador, controla los datos.  | [https\://www\.sqlite.org/different.html](https://www.sqlite.org/different.htmlç)  |
| 13 | Una herramienta gráfica para administrarlo o consultarlo | Un ejemplo de herramienta gráfica de código abierto es DB Browser for SQLite  | [https\://sqlitebrowser.org/](https://sqlitebrowser.org/)  |

## 5\. Valoración

| \# | Campo | Respuesta |
| :---- | :---- | :---- |
| 14 | Para qué destaca | SQLite destaca en su facilidad de uso sin configuración previa, ligereza y compatibilidad amplia con muchos dispositivos y sistemas operativos. |
| 15 | Una limitación importante | Una limitación importante es la gestión de la escritura cuando lo hacen varias personas a la vez. |
| 16 | Clasificación: por modelo, por ubicación y por licencia (apartado 6\) | **Por modelo:** Es un sistema Relacional que organiza los datos en tablas de filas y columnas usando el idioma SQL que conecta las tablas de forma lógica. **Por ubicación:** Es una base de datos **Local / Embebida**. La base de datos corre dentro del mismo proceso de la aplicación y accede directamente al sistema de archivos local sin usar estructura cliente-servidor a través de una red **Por licencia:** Es de **Dominio Público** No tiene una licencia de código abierto restrictiva tradicional; cualquiera puede copiar, modificar, publicar, compilar, vender o distribuir el código fuente de SQLite. |
| 17 | ¿Serviría para el inventario del aula? ¿Por qué sí o por qué no? | SQLites serviría a no ser que se quisiera que muchas personas a la vez modifiquen la tabla o si no se quiere que alguna persona no toque algo de la tabla. |
  

## 6\. La prueba

Qué hicimos, qué salió y qué nos llamó la atención (tres o cuatro líneas). Captura en `E2-prueba.png`.  
![Prueba](https://github.com/dllopezm/Equipo-A/blob/Proyecto-0/GBD/bd/Captura%20de%20pantalla%202026-10-06%20130710.png)
Preguntas: 

- ¿qué devuelve el SELECT? 

El SELECT devuelve toda la información de la base de datos 

- ¿Qué pasa con el último INSERT, y por qué? ¿Qué regla de la teoría es esa?

En el último INSERT da error debido a que al estar definida al etiqueta como PRIMARY KEY solo deja un nombre (“etiqueta”) la solución  es poner otro distinto (como en la segunda captura).

La regla es “La Regla de Unicidad”
