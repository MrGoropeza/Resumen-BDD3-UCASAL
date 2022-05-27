# Link a algo
Sintaxis: `[[<nombresito de la nota>#<header>|<texto que se ve>]]`

# Enlace a archivo audio, video, o pdf
`![[path al archivo]]`

# Headers
Sintaxis: `# titulo`. Entre mas `#` uno ponga, menor el nivel del titulo.
va un # detras.
Ejemplos:
# head1
## Head2

# Cursiva
Sintaxis: `*texto*` o `_texto_`
Ejemplos
*cursiva con asterisco* | _cursiva con barra baja_

# Negrita
Sintaxis: `**texto**`
Ejemplos:
**texto entre doble asterisco**

# Listas
Sintaxis: `- elemento` o `1. elemento`
Ejemplos:
- item1
- item2
- item3
1. item1
2. item2
3. item3
	1. item3a
	2. item3b

# Cajas con texto
Sintaxis:  `> contenido de la caja xd`
Ejemplo:
>soy el texto de la caja owo.

\-la fuente de los deseos

# Texto como si fuera codigo
Sintaxis: es un texto que va entre \`.
`print("hola");`

Se pude especificar el codigo que va a usar:

```dart
	String variable = "esto es codigo dart OwO";
```

# Lista de tareas
Sintaxis: `- [] tarea sin marcar` o `- [x] tarea marcada`
Ejemplos:
- [x] tarea1 marcada
- [ ] tarea 2 sin marcar
- [?] marque la tarea con un signo de pregunta, se puede marcar con cualquier caracter

# Tablas
Sintaxis:
`columna1 | columna2`
`------- | --------` En esta parte se puede poner `:` a los lados de los signos menos para justificar el texto
`contenido1 | contenido 2`

Ejemplos:
Columna 1 | Columna 2
-----------| ---------
Contenido celda 1 | Contenido Celda 2
Se puede justificar el contenido con `:` en la parte separadora de titulos y contenidos.

Columna 1 con un titulo muy largo xd | Columna 2 con un titulo re largo tambien
:-----------| ---------:
Contenido celda 1 | Contenido Celda 2

# Tachar texto
Sintaxis: `~~texto~~`
Ejemplo:
~~texto tachado xd~~

# Resaltar texto
Sintaxis: `==texto==`
Ejemplo: ==hola soy texto resaltado==

# Barra horizontal
Sintaxis: `***` o `---` o `___`
Ejemplo:
***
---
___
# Notas al pie
## Simples
Sintaxis:
- `[^1]` para colocarla.
- Para darle el texto a la nota: `[^1]: texto de la nota`

Ejemplo:
Hola tengo nota al pie [^1]

[^1]: contenido de la nota xd

## Con muchos parrafos y/o codigo
Sintaxis:
- `[^nombresito]` para colocarla.
- Para darle el texto a la nota: `[^nombresito]: texto de la nota`

Ejemplo:
Hola, tengo una nota grande al pie[^notaGrande]
	[^notaGrande]: este es el primer parrafo. 
	segundo parrafo.

# Fórmulas
Sintaxis: texto escrito en TeX o LaTeX

Ejemplo:
$$\begin{vmatrix}a & b\\ c & d \end{vmatrix}=ad-bc$$
# Comentarios
Sintaxis:
- En la mismas línea: `%%comentario%%`
- Bloque de comentario:
`%%inicio comentario`
`hola sigo comentado`
`fin comentario%%`

Ejemplo:
- En la línea: %%comentario xd%%
- En bloque:
%% inicio comentario
sigo comentado
fin comentario %%

# Tremendas cajas de advertencia
Sintaxis: 
- Titulo: `> [!tipo] titulo`
	- Para usar tipos de cajas, en `tipo` se puede reemplazar por:
		- note
		- abstract, summary, tldr 
		- info, todo
		- tip, hint, important
		- success, check, done
		- question, help, faq
		- warning, caution, attention
		- failure, fail, missing
		- danger, error
		- bug
		- example
		- quote, cite
- Para hacer la caja comprimible: `> [!tipo]- titulo` Se puede colocar un `+` o un `-`
Ejemplos:
> [!INFO]
> holis linea 1
> holis linea 2

> [!bug]- holis
> contenido xd

# Diagramas
Se pueden realizar diagramas a través de Mermald:
https://mermaid-js.github.io/mermaid/#/
Por ahora no pienso resumir esto xd, pero se ve muy interesante.

