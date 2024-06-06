
# Exámen FBBDD-1

Surge la problemática de optimizar el uso de espacios en los complejos polideportivos. Dada la subdivisión de complejos deportivos en aquellos destinados a un único deporte y los polideportivos, es esencial garantizar una distribución eficiente de las áreas designadas para cada deporte en los complejos polideportivos.

La pregunta clave es, cómo maximizar la utilización de los espacios disponibles en los complejos polideportivos, considerando las diferentes áreas destinadas a distintos deportes con indicadores de localización específicos. La optimización deberá tener en cuenta la variedad de deportes que se celebran en un mismo complejo polideportivo, garantizando la eficacia en la organización de eventos y minimizando posibles conflictos de programación.

Además, la gestión de eventos en cada complejo añade complejidad al escenario. ¿Cómo asegurar que los eventos programados en una sede no entren en conflicto con la disponibilidad de áreas específicas en los complejos polideportivos? Esto implica coordinar fechas, duraciones, participantes y comisarios de manera eficiente, evitando superposiciones y garantizando un flujo adecuado de las actividades deportivas.

La necesidad de mantener una lista actualizada de comisarios y su participación en eventos plantea otra dimensión de la problemática. ¿Cómo gestionar eficazmente la asignación de comisarios a eventos específicos, considerando sus roles como jueces u observadores, para asegurar una cobertura adecuada en cada competición?

Finalmente, la gestión del equipamiento necesario para eventos y mantenimiento también representa un desafío. ¿Cómo garantizar que cada evento cuente con el equipamiento requerido y que se realice un mantenimiento efectivo de las instalaciones sin afectar la realización de competiciones?

La problemática central radica en la optimización integral de los recursos y espacios en las sedes olímpicas, particularmente en los complejos polideportivos, para lograr una gestión eficiente y exitosa de los eventos deportivos.


## Autor

- [@Oliver López](https://github.com/Oliwashere)

## Caracteristicas

1. **Complejos Deportivos:**
    - Los complejos deportivos están especializados en un único deporte.
    - Cada complejo deportivo tiene una localización específica, un jefe de organización individual y un área total ocupada.
2. **Complejos Polideportivos:**
    - Los complejos polideportivos albergan múltiples deportes, con áreas designadas para cada uno y un indicador de localización.
    - Al igual que los complejos deportivos, los polideportivos tienen una localización, un jefe de organización individual y un área total ocupada.
3. **Información Específica para Cada Tipo de Sede:**
    - Se mantiene información específica para cada tipo de sede, como el número de complejos y su presupuesto aproximado.
4. **Eventos en los Complejos:**
    - Cada complejo, ya sea deportivo o polideportivo, celebra eventos.
    - Para cada evento se registra información detallada, incluyendo fecha, duración, número de participantes y número de comisarios.
5. **Comisarios y su Involucramiento en Eventos:**
    - Se mantiene una lista de todos los comisarios, identificando si desempeñan el papel de juez u observador en cada evento.
    - La relación entre comisarios y eventos se registra para rastrear su participación específica.
6. **Equipamiento Necesario:**
    - Tanto para eventos como para el mantenimiento de los complejos, se requiere cierto equipamiento específico, como arcos, pértigas, barras paralelas, etc.

## Fases

1. **Extrapolación del caso de estudio hacia un modelo conceptual:**

Se extrae información clave de la descripción dada por el cliente.

En este caso:

**Polideportivos**:
Área - ID_Polideportivo

**Deportivos**:
Deporte 

**Evento**:
Fecha - Duración - Participantes - Comisario -  Equipamiento - ID_Evento - Lugar - Jefe


2. **Conversión formal del modelo conceptual al modelo lógico**:

Finalizado el mapa conceptual, se organiza la información por tablas especificando us identificadores y relaciones con las otras tablas.

En este caso:

**Polideportivos**:

Área: El área total ocupada

ID_Polideportivo: ID representativo del complejo



**Deportivos**:

Deporte: Deporte practicado en tal complejo



**Eventos**:

Fecha: Fecha de celebración del evento

Duración: Duración del evento en el complejo

Participantes: Cantidad de participantes que asistieron al complejo

Comisarios: Cantidad de comisarios designados al evento 

Equipamiento: Tipo de equipamiento necesario para la celebración del evento

ID_Evento: ID representativo del evento

Lugar: Complejo en el cual se celebra el evento

Jefe: El jefe de organización asignado al evento



3. **Normalización del modelo lógico**:
Se eliminar redundancias y se optimiza el orden de la información.

En este caso:

Se cambió el nombre de “Lugar” a “Complejo” teniendo en cuenta los datos extrapolados.

Se cambió el nombre de “Jefe” a “Organizador” teniendo en cuenta los datos extrapolados.

Se mantuvieron las 3 tablas base


4. **Implementación mySQL**:
Se importan los datos a mySQL para realizar el modelo físico.

## Resultados

Se cumplieron los siguientes requerimientos:
1. Extrapolación del caso de estudio hacia un modelo conceptual.
2. Conversión formal del modelo conceptual al modelo lógico.
3. Normalización hasta la 3FN de dicho modelo lógico.
4. Conversión del modelo lógico a modelo físico.
5. Construcción formal del modelo físico con 3 consultas de las anteriormente listadas.
6. Creación del modelo UML tipo E-R basado en el estándar de MySQL Workbench.
