# psql
```bash
	psql [opciones]

	[opciones] pueden ser:
		-U <user> 
		-d <database>
		-c <consulta SQL entre "">
		-h <ip del servidor>
```
ejecutar psql sin opciones nos manda a la consola para hacer consultas SQL de postgres.

## Comandos útiles
### Ver bases de datos tengo
```bash
	psql -c "\l"
```

### Ver tablas de una BDD
```bash
	psql -d [nombre BDD] -c "\dt"
```

### Ver columnas de una tabla
```bash
	psql -d [nombre BDD] -c "\d+ [nombre tabla]"
```


```bash
\du detalle usuarios
```

# pg_dump
```bash
	pg_dump [opciones]... [base de datos]

	opciones de conexión:
		-d [base de datos]
		-h [ip del servidor]
		-p [puerto]
		-U [usuario]

	opciones generales:
		-f [nombre del archivo generado]
		-F [formato]  (puede ser c, d, t o p: Custom, Directory, Tar, Plain text)
		-v (para que muestre que va haciendo el comando mientras se ejecuta, bastante util para saber si esta haciendo algo)

	opciones de salida:
		son una banda de opciones, pg_dump --help para ver todas las opciones xd
```
# pg_basebackup
```bash
	pg_basebackup
```

