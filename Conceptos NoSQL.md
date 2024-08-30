CONCEPTOS RELEVANTES
1. Base de Datos NoSQL: Definición y Tipos


Las bases de datos NoSQL (Not Only SQL) son un tipo de sistema de gestión de bases de datos que no se basan en el modelo relacional tradicional de tablas y filas. Son diseñadas para manejar grandes volúmenes de datos no estructurados y para ser escalables horizontalmente.

![NoSQL](https://th.bing.com/th/id/OIG3.bGB3Bd_L05i3IFD2YiRC?pid=ImgGn)


Tipos de Bases de Datos NoSQL:

*  Bases de Datos de Documentos: Almacenan datos en documentos similares a JSON. Ejemplos: MongoDB, CouchDB.

* Bases de Datos Clave-Valor: Utilizan un par clave-valor para almacenar datos. Ejemplos: Redis, DynamoDB.

* Bases de Datos de Columnas Anchas: Optimizadas para consultas en grandes volúmenes de datos organizados en columnas. Ejemplos: Apache Cassandra, HBase.

* Bases de Datos de Grafos: Especializadas en modelar relaciones complejas entre datos. Ejemplos: Neo4j, Amazon Neptune.

2. Comparación entre Bases de Datos Relacionales y No Relacionales:
   
|Característica |Relacionales (SQL)|No Relacionales (NoSQL)|
|---------------|------------------|-----------------------|       
|Modelo de Datos|Tablas y filas    |Documentos, clave-valor, grafos, 
columnas anchas|	Vertical (más potencia)|Horizontal (más nodos)
Consistencia|	Consistencia fuerte|	Consistencia eventual
Flexibilidad de Esquema|	Esquema rígido|	Esquema flexible
Consultas|	SQL	Propietarias| específicas por tipo de NoSQL
Transacciones|	ACID|	BASE (Basically Available, Soft state, Eventual consistency)

1. Modelado de Datos en Bases de Datos No Relacionales
* Documentos: Se modelan como colecciones de documentos (similar a objetos JSON) donde cada documento puede tener un esquema diferente.
* Clave-Valor: Los datos se modelan en pares simples de clave y valor, ideales para búsquedas rápidas de datos específicos.
* Columnas Anchas: Datos organizados en filas, pero cada fila puede tener un conjunto variable de columnas.
* Grafos: Modelan entidades y relaciones como nodos y aristas, optimizando las consultas de relaciones complejas.
Comparado con las bases de datos relacionales, donde los esquemas son predefinidos y más rígidos, las bases de datos NoSQL ofrecen flexibilidad para manejar datos no estructurados.
![](https://th.bing.com/th/id/OIG1.4yZnnV14jXGuP6WNkm.y?w=1024&h=1024&rs=1&pid=ImgDetMain)


4. Sharding y Particionamiento Horizontal en NoSQL
Sharding es el proceso de dividir una base de datos en múltiples partes llamadas shards para distribuir la carga de trabajo.
Particionamiento Horizontal implica dividir las filas de una tabla en diferentes nodos para mejorar la escalabilidad.
Implementación: En MongoDB, por ejemplo, los datos se dividen en shards basados en una clave de shard. Cada shard se aloja en un servidor diferente, permitiendo escalabilidad horizontal.
![](https://th.bing.com/th/id/OIG3.pvFYOosLGw8rOAOB_ErM?w=1024&h=1024&rs=1&pid=ImgDetMain)


5. Consistencia Eventual vs. Consistencia Fuerte
Consistencia Eventual: Asegura que, con el tiempo, todos los nodos alcanzarán la consistencia, pero no garantiza que las lecturas sean consistentes en todo momento. Ejemplos de uso: redes sociales, donde la consistencia inmediata no es crítica.
Consistencia Fuerte: Asegura que todas las lecturas devuelven los datos más recientes. Se utiliza en aplicaciones donde la exactitud es crítica, como en sistemas bancarios.
![Texto alternativo](https://th.bing.com/th/id/OIG3.YEmg.j2_i1q9lIIfQ8Qc?pid=ImgGn)

6. Replicación de Datos en Bases de Datos No Relacionales
Replicación Maestra-Esclava: Un nodo maestro acepta todas las escrituras y las replica a uno o más nodos esclavos.
Replicación Maestra-Maestra: Varios nodos maestros permiten lecturas y escrituras, y sincronizan los datos entre sí.
Ventajas: Mejora la disponibilidad, tolerancia a fallos y escalabilidad.
![Texto alternativo](https://th.bing.com/th/id/OIG4.rIgJXT_.knAyREZWX1Ma?pid=ImgGn)

7. CAP Theorem (Teorema CAP) y su Relevancia en NoSQL
El teorema CAP establece que una base de datos distribuida no puede garantizar simultáneamente:

* Consistencia: Todos los nodos ven los mismos datos en el mismo momento.
* Disponibilidad: Garantía de que cada solicitud recibe una respuesta.
* Tolerancia a Particiones: El sistema sigue funcionando a pesar de la caída de una parte de la red.

NoSQL prioriza generalmente disponibilidad y tolerancia a particiones, aceptando consistencia eventual.
![Texto alternativo](https://th.bing.com/th/id/OIG4.S5waoiFR7E.NpI7KtQwk?w=1024&h=1024&rs=1&pid=ImgDetMain)

8. MongoDB: Características y Casos de Uso
Características: Base de datos orientada a documentos, esquema flexible, soporte para consultas ad-hoc, índice secundario.
Casos de Uso: Aplicaciones web, sistemas de gestión de contenido, big data, almacenamiento de catálogos de productos.
![Texto alternativo](https://th.bing.com/th/id/OIG2.GgTrs29lYOO2FnD3BpGB?pid=ImgGn)

9. Cassandra: Arquitectura y Escalabilidad
Arquitectura: Basada en un modelo peer-to-peer, cada nodo es igual y pueden agregarse o quitarse fácilmente.
Escalabilidad: Escalabilidad horizontal, lo que permite manejar grandes volúmenes de datos distribuidos en múltiples nodos.
![Texto alternativo](https://th.bing.com/th/id/OIG3.Yv__m0LcHsE7GB_SBdhD?w=1024&h=1024&rs=1&pid=ImgDetMain)

10.  Bases de Datos de Grafos: Neo4j y Casos de Uso
Características: Modelo de nodos y aristas, ideal para datos altamente conectados.
Neo4j: Una de las bases de datos de grafos más populares.
Casos de Uso: Redes sociales, gestión de fraudes, motores de recomendación.
![Texto alternativo](https://th.bing.com/th/id/OIG1.kRXYvw.PqdFpok2ZZA0b?w=1024&h=1024&rs=1&pid=ImgDetMain)

11.  Bases de Datos Clave-Valor: Redis y Casos de Uso
Características: Almacenamiento simple de pares clave-valor, muy rápido, soporta estructuras de datos avanzadas (listas, conjuntos).
Redis: Es una base de datos en memoria popular que soporta persistencia en disco.
Casos de Uso: Caché, colas de mensajes, almacenamiento de sesiones.
![Texto alternativo](https://th.bing.com/th/id/OIG3.3TFH1fOL7f_l0QfkH9dx?pid=ImgGn)

12.  Almacenamiento Orientado a Columnas: Apache HBase y Casos de Uso
Características: Basada en Google Bigtable, diseñada para manejar tablas muy grandes con miles de millones de filas y millones de columnas.
HBase: Base de datos distribuida, escalable y no relacional.
Casos de Uso: Almacenamiento de grandes volúmenes de datos, aplicaciones de análisis en tiempo real.
![Texto alternativo](https://th.bing.com/th/id/OIG2.3FSlLhF7osKx4Py5VSqT?pid=ImgGn)

13.  Indexación en Bases de Datos No Relacionales
Métodos de Indexación: Índices secundarios, índices compuestos, índices de texto completo.
Rendimiento: La indexación mejora significativamente la velocidad de las consultas, aunque puede incrementar el tiempo de escritura y el uso de almacenamiento.
![Texto alternativo](https://th.bing.com/th/id/OIG2.Sk8zfSZPiseQax5XE5S3?pid=ImgGn)

14.  Control de Concurrencia en NoSQL
Bloqueo Optimista: Se asume que no habrá conflictos y se verifican conflictos solo al final.
Bloqueo Pessimista: Se asumen conflictos y se bloquean los recursos.
Diferencias con Relacionales: NoSQL tiende a evitar bloqueo de registros a favor de modelos de consistencia eventual.
![Texto alternativo](https://th.bing.com/th/id/OIG1.5nH.hrSuP11G2R3bZ0ez?pid=ImgGn)

15.  Estrategias de Backup y Recuperación de Datos en NoSQL
Backup Completo: Copia todos los datos, pero puede ser lento y costoso.
Backup Incremental: Solo copia los cambios desde el último backup, más eficiente.
![Texto alternativo](https://th.bing.com/th/id/OIG4.AD5PIWGvBOCQqfNE4xvo?w=1024&h=1024&rs=1&pid=ImgDetMain)
