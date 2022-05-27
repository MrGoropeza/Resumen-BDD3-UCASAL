# Métricas DR 
**DR**: Disaster Recovery

## Recovery Time Objective (RTO)
Se mide en horas usualmente. Se refiere a la cantidad máxima de tiempo que un sistema puede estar caido.
Dado un RTO de 24hrs, si un sistema se cae un miercoles por la tarde, debería estar nuevamente operativo el jueves por la tarde.

## Recovery Point Objective (RPO)
Se mide en horas usualmente. Se refiere a la cantidad máxima de datos que un sistema puede perder. 
Dado un RPO de 1 hora, se deben tomar backups por lo menos cada hora ya que uno esta dispuesto a perder solamente los datos entre el último backup y el momento de fallo en sistema. De esta forma, en el peor de los casos, se puede llegar a perder 1 hora de datos.

# Causas más comunes de Desastres Tecnológicos
## Desastres menores
- Un simple error humano
- Error de software
- Pérdida de un dispositivo

## Desastres operacionales
- Error de un Admin de IT
- Viruses
- Fallo de migración de tecnología
- Fallo de hardware

## Desastres mayores
- Hackeos
- Desastres naturales
- Robo de información de la organización
- Empleado malintenciado

# 7 Reglas para un DR en IT
1. Planificar con antelación y documentar
2. Replicar aplicaciones
3. Planes de backups: on-site y off-site
	- On-site: Backups en el mismo lugar físico de las organización
	- Off-site: Backups en un lugar físico distinto al de la organización
4. Automatizar
5. Probar los planes
6. Proteger el entorno
7. Elegir sabiamente al socio de DR