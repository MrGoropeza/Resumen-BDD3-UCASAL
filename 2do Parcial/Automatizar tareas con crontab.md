# Comandos de crontab
```bash
	crontab -e (editar el crontab)
	crontab -l (listar las tareas en crontab)
	crontab -r (borrar el archivo de crontab)
```

# Sintaxis en crontab
```bash
	* * * * * [comando a ejecutar]
```
Donde los asteriscos significan lo siguiente:
Posición | Significado | Intervalo Válido
	- | - | -
1 | minutos | 0 a 59
2 | horas | 0 a 23
3 | dia del mes | 1 a 31
4 | mes | 1 a 12
5 | dia de la semana | 0 a 6 (domingo=0)

En la posicion de cada asterisco puede haber un solo elemento o varios separados por `,`

## Para poner patrones repetitivos
hay que colocar un `/numero` luego del asterico o los elementos
```bash
	*/2 en la parte de minutos significa que la tarea se hará cada dos minutos
```

## Comando a ejecutar
En esta parte ponemos la dirección del script .sh