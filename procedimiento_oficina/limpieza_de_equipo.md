# Limpieza de equipos

Autor: Vladimir Támara

Contribuciones: David Castillo, Daniel Cardona

Dirigido a: Gestor de soporte, Adminsitrador de red y webmaster, Asesor en TI 

----

En GLPI se han programado con solicitudes recurrentes las limpiezas de todos los equipos del CINEP una vez al año. Por esto mismo cuando ingresen o salgan equipos es importante poner solicitud para que el asesor en TI cree, elimine o actualice las solicitudes recurrentes.

El asesor en TI envía al comienzo del año el calendario de limpiezas y solicita ajustes iniciales.

En GLPI se ha programado que la solicitud se cree una semana antes de la semana de la limpieza.

El procedimiento a seguir es:

1. Cuando se vea el tiquete en GLPI asegurar: (a) que la solicitud tiene como equipo asociado el correcto (b) que en el inventario de ese equipo está bien el nombre, oficina y usuario en equipo y en  GLPI (si la solicitud recurrente tiene errores poner solicitud de corrección al asesor en TI). (c) de requerirse correrle el fusion manual para asegurar actualización. 
2. Cuadrar con el usuario.
3. En el momento de la limpieza:
 * Si la placa de equipo no es legible imprimir el número de inventario y pegarlo con cinta transparente.
 * Usar manilla anti-estática.  
 * Emplear trapo limpio.
 * Procedimiento para limpiar teclado
   * Soplar para quitar partículas
   * Limpiar con espuma y trapo para remover grasa
   * Soplar nuevamente para remover exceso de espumoso
   * Aplicar Silicona
 * Procedimiento para limpiar monitor
   * Aplicar espuma limpiadora en el exterior pero no sobre la pantalla
   * Aplicar solución con base en alcohol sobre la pantalla
 * Procedimiento para limpiar CPUs
   * Destapar, soplar el interior manteniendo quietos los ventiladores (por ejemplo con lapices).
   * Desmontar el ventilador que está sobre el procesador pero no quitar el procesador
   * Aplicar pasta térmica sobre el procesador hacía la mitad de forma que se esparza sobre el procesador cuando se vuelva a  poner el ventilador, pero sin derramarse.
   * Limpiar el exterior con trapo seco para quitar el polvo
   * Lmpiar con otro trapo el exterior con espuma limpiadora
   * Cerrar
 * Para equipos Portátiles no usar limpia contactos o espuma limpiadora directamente en el teclado, con un trapo humedo de alcohol limpiarlo 
4. Después de la limpieza física encender computador, correr fusion inventory; agregando el nombre del usuario en el campo de comentarios si no es posbile en el campo para eso.  Correr antimalware en windows 7.   Si se detecta malware crear un tiquete en la categoría vulneración.
5. Retornar el equipo al puesto del usuario.
6. Si la persona está, encender el equipo con el usuario y verificar que opera su escritorio, y que opere Chrome, Office y el correo.   Si la persona no está ingresar con cuenta de gestor de soporte y verifica Chrome y Office.
7. Ejecutar actualizaciones y solicitarle al usuario no apagar hasta que se completen y reiniciar cuando solicite.
8. El mismo día de la limpieza, escribirle correo al usuario (con copia a coordinador del SIG y asesor en TI) indicando la terminación del procedimiento y solicitando responder por correo (con copia a todos los receptores) si algo no quedó bien.   En caso de portátiles de la oficina de Recursos Físicos o equipos sin usuario el correo debe ir a coordinador del SIG y Asesor en TI.
9. Cerrar tiquete (recordar que si hay malware debe emplearse un tiquete nuevo).
