# Manualmente
1. Marcar checkpoint en la base de datos:
```bash
	psql -c "checkpoint;"
```

2. Marcar en Postgres que se va a realizar un backup:
```bash
	psql -c "select pg_start_backup('string');"
```
En **'string'** poner un nombre piola xd. Se suele poner la fecha.

3. Realizar el backup físico:
```bash
	tar czvf <outpath>/nombreArchivo.tar.gz $PGDATA* --exclude 'pg_wal/*'
```

4. Marcar en Postgres que se terminó el backup:
```bash
	psql -c "select pg_stop_backup();"
```

# Con pg_basebackup
```bash
	pg_basebackup -D <outpath> -Ft -X none -z
```

>[!tip] Aclaraciones
>`-d <outpath>` es para decir donde se va a realizar el backup. **El directorio debe estar vacío.**
>`-Ft` es para decir que el archivo de salida será .tar
>`-X` es para decir si se va a incluir o no la carpeta wal.
>Puede ser:
>- **none** (osea que no se va a copiar, esta es la opcion default)
>- **fetch** (que se copien los ultimos wals hasta donde empezamos el backup)
>- **stream** (que se copien todos los wals anteriores al backup y tambien los que se vayan generando mientras se realiza el backup)
>
>`-z` es para decir que el archivo de salida salga comprimido


