# Finite_State_Machines
FSM concepts for embedded systems. (Spanish)

1. Sistemas Embebidos

def: "Un sistema embebido es un sistema de computación deiseñado para realizar una o algunas funciones dedicadas. Frecuentemente es un sistema de computación en tiempo real."

- Componentes:
  - CPU
  - Módulos de comunicación
  - Módulos de presentación
  - Actuadores
  - Entradas/Salidas
  - Reloj
  - Módulo de Energía

- Arquitecturas de computadores más empleadas
  - Microprocesador
  - Memoria
  - Caché
  - Disco Duro
  - BIOS-ROM
  - CMOS-RAM
  - Chipset
  - Entradas
  - Salidas
  - Ranuras de expansión

- Consideraciones:
  - Analizar diferentes opciones y hacer un buen balance entre precio, prestaciones, disponibilidad, soporte, etc. 
  - Contar con capacidad de procesamiento suficiente para usar lenguajes de programación de alto nivel y usar sistemas operativos. 
  - Usar herramientas para
    [ ] definir funcionalidad mediante diagramas
    [ ] generar documentación automáticamente
    [ ] simular el funcionamiento del sistema
 
- Restricciones temporales:
  - En algunos casos el tiempo es crítico. p/e: monitoreo de vibraciones
  - En otros casos, se puede esperar. p/e: temperatura de un lago
 
- El diseño de sistemas embebidos implica trabajar simultáneamente entre HW y SW

-  Habilidades y herramientas útiles:
  - Programación de microcontroladores. (8, 16 y 32 bits)
  - Programación de alto nivel (C, C++, C#, java)
  - Modelado de software (diagramas de estado, statecharts)
  - Metodologías de administración de proyectos (Scrum, XP, etc)
  - Manejo de módulos de comunicación. WiFi, ZigBee, USB, RS-232, etc.
  - Conceptos de bajo consumo, baterías y autonomía.
  - FPGAs y DSPs
  - EMI y PCBs
  
### DIAGRAMAS DE ESTADO (STATECHARTS, STATE FLOWS)
  
  1. Sistemas Reactivos
  
  - Reaccionan a estímulos externos e internos (eventos), efectuando la acción apropiada en un contexto particular. Estas reacciones dependen tanto de la naturaleza del evento, como del contexto (estado) del sistema. Provocan que el sistema cambie de un estado a otro. el conjunto de reacciones define su comportamiento dinámico. Los eventos y los estados son un medio natural para describir su comportamiento dinámico. Un fragmento básico de tal descripción, contituye una reacción (transisción de estados). 
  
  El comportamiento suele describirse por medio de fragmentos como:
  "Cuando se recibe una falla de energía en operación normal, el sistema de comunicación está activo, se cambia a modo falla activando los mecanismos de protección, enciando dicha falla al sistema de control".
  
  2. Software embebido reacivo
  
  - Ejecuta una porción de código en respuesta a un evento. Permanece en reposo durante la ausencia de eventos. En ciertos casos, se les requiere respuesta "inmediata". Manejan diversas actividades al mismo tiempo. Se ejecutan en ambientes con recursos limitados. Requieren lidiar con el aoplamiento y relación entre actividades del sistema. Generalmente, el acceso a dispositivos y recursos se comparte entre actividades concurrentes. 
  
  El desafío es lograr en el SW embebido:
  * FLEXIBILIDAD
  * ESCALABILIDAD
  * ROBUSTEZ
  * SEGURIDAD
  * EFICIENCIA
  * ENCAPSULAMIENTO
  * REUTILIZACIÓN
  * SIMPLEZA
  
  3. Máquinas de Estado
  
  - Las máquinas de estados y sus correspondientes diagramas son el mecanismo formal y natural para representar el comoportamiento dinámico de un sistema reactivo de manera visual, clara e intutiva. Se definen por un conjunto finito de estados y transiciones (FSM). Su uso como estructura de programa reduce el "spaghetthi code", genera documentación y un lenguaje común para comprender la funcionalidad del sistema. 
