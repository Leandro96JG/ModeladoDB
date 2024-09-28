# EntrenaGlamurDB

## Lista De Necesidades Para El Sistema

- Registrar participantes para el evento "Entrena Tu Glamur".
- El evento tendrá 4 desciplinas: _KickBoxing_, _Pilates_ , _Yoga_ y _Zumba_.
- Cada disciplina tendrá 3 bloques de horarios:
 - Bloque 1 de 9:00 a 12:00
 - Bloque 2 de 14:00 a 17:00
 - Bloque 3 de 18:00 a 21:00
- Cada actividad tendrá un máximo de 10 participantes, excepto _Yoga_ que tendrá 20.
- Cada participante sólo se podrá registrara una sóla actividad.

## Entidades

### Actividades
    
- actividad_id
- actividad
- capacidad_maxima

### Participantes
- participante_id
- nombre
- apellido
- celular
- actividad_id
- bloque_id

### bloques

- bloque_id
- actividad_id **(FK)**
- bloque
- inicio
- final

## Relaciones entre entidades

1. **participante** tienen **actividad** (_1 - M_).  
1. **participante** tiene **bloque** (_1 - 1_).  
1. **actividad** tiene **bloques** (_1 - M_).  
