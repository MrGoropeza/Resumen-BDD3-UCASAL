Hay que saber en donde esta el archivo .dmp, a esa dirección la voy a llamar: **pathToFile**

Pasos:
1. Si es que no hay una base de datos donde poner todo lo del backup, crear una:
```bash
	psql -c "create database [nombre];"
```
2. Realizar la recuperación del backup en la base de datos creada o ya existente:
```bash
	pg_restore -d [nombre BDD] pathToFile/archivo.dmp
```

