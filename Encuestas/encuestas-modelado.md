# Encuesta - Modelado 

## Entidades

### Encuestas **(ED)**

- encuesta_id **(PK)**
- name
- descripcion
- img
- fecha
- encuestados

### Preguntas **(ED)**

- preguntas_id **(PK)**
- encuesta_id **(FK)**
- pregunta

### respuestas **(ED)**

- respuesta_id **(PK)**
- pregunta_id **(FK)**
- respuesta
- es_correcta

### encuestados **(ED)**

- encuestados_id **(PK)**
- nombre
- apellido
- edad
- email **(UQ)**

### resultados **(ED | EP)**

- resultado_id **(PK)**
- encuesta_id **(FK)**
- encuestado_id **(FK)**
- preguntas
- correctas

## Relaciones

1. **encuesta** tiene **preguntas** (_1 - M_).
1. **pregunta** tiene **respuestas** (_1 - M_).

1. **encuesta** tiene **resultados** (_1 - M_).
1. **encuestado** tiene **resultados** (_1 - M_).

![Modelo Relacional](Encuentas-db-diagrama.drawio.svg)