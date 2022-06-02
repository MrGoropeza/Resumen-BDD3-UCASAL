# Pasos en Master
Guía que yo segui: https://girders.org/postgresql/2021/11/05/setup-postgresql14-replication/
## Preparación
Postgres iniciado en Master y parado en Slave.
IP del master: 172.16.194.128
IP del slave: 172.16.194.129
## 1. Crear usuario para la replicacion
> [!tip] Comandos
> psql -c "CREATE USER repuser
> SUPERUSER LOGIN REPLICATION CONNECTION LIMIT 1 ENCRYPTED PASSWORD '123';"

> [!warning] Cuidado con la config
> **postgresql.conf**:
> 	listen_adresses='*'
> **pg_hba.conf**:
> 	host replication repuser <ip_del_esclavo>/24 trust

## 2. Editar los archivos de configuración
1. Crear la carpeta de archivado: ```
```shell
	mkdir /home/postgres/archivado
	#aca se van a crear los backups de los wals
```

2. Cambiar en postgresql.conf:
```conf
	wal_level = replica
	max_wal_senders = 2
	wal_keep_size = '1GB'
	wal_compression = on
	archive_mode = on
	archive_command = 'cp -i %p /home/postgres/archivado/%f </dev/null'
```

3. Reiniciar el postgres.


# Clonar la maquina virtual con VMWare

# Pasos en el esclavo
## 1. Borrar la carpeta data
Hay que darle permisos al usuario **postgres** para que pueda borrar la carpeta data:
### 1. Entramos al esclavo con el usuario **osboxes**
```bash
	sudo chmod 777 /usr/local/pgsql/
```
Osea le damos permisos a todos los usuario para que puedan modificar la carpeta pgsql.

### 2. Eliminamos la carpeta data (con el usuario **postgres**)
```bash
	rm -r /usr/local/pgsql/data
```

## 2. Iniciar el postgres
```bash
	pg_ctl start
```
## 3. Realizar el backup físico completo del host
```
	pg_basebackup --pgdata [direccion de la carpeta data] --format=p --write-recovery-conf --checkpoint=fast --label=mffb --progress --host=[ip del master] --port=5432 --username=[usuario de replicacion creado al principio]
```
