> [!tip] Aclaraciones
>  `<outpath>`: lugar donde guardar el archivo
>  `-f` es lo mismo que `>`
>  `-Fc` significa format custom
  
# En un archivo plano
```bash 
	pg_dump -v -d [nombre BDD] -f <outpath>/nombreArchivo.sql
```

# En un archivo .dmp
```bash
	pg_dump -v -Fc -d [nombre BDD] -f <outpath>/nombreArchivo.dmp
```

# De una sola tabla
```bash
	pg_dump -v -t [nombre tabla] -d [nombre BDD] -f <outpath>/nombreArchivo.sql
```

# Con copy 
```bash
	psql -d [nombre BDD] -c "copy [tabla] to '<outpath>/nombreArchivo.txt' with delimiter ',';"
```

