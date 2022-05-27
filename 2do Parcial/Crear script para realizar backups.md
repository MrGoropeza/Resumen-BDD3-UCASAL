1. Crear un archivo .sql con la lógica requerida:
Código del copiar_sueldos.sql:
```text
	copy empleados ("EMPLEADO_APELLIDO","EMPLEADO_SALARIO") to '/home/postgres/sueldos.txt' with delimiter ',';
```

2. Crear script (archivo con terminación .sh) que haga uso del archivo .sql del paso anterior:
Código del sueldos.sh:
```sh
	psql -d rrhh -f '/home/postgres/copiar_sueldos.sql'
```

3. Dar permisos de ejecución al nuevo script:
```bash
	sudo chmod +x /path/to/script/sueldos.sh
```

4. Ejecutar el nuevo script:
```bash
	/path/to/script/./sueldos.sh
```

