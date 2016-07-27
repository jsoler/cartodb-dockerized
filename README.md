Carto DB

Componentes

PostgreSQL
PostGIS
Redis
CartoDB PostgreSQL extension
CartoDB Editor
Maps API
SQL API


Asociacion Componentes - Servicios dockerizados

Base de datos -> PostgreSQL, PostGIS, CartoDB PostgreSQL extension
Redis -> Redis -> dependen Base de datos
Maps API -> Maps API -> dependen de Redis
SQL API -> SQL API -> dependen de Redis
CartoDB Editor -> depende de Base de datos 


