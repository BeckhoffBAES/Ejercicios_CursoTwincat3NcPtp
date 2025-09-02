## 3. Configuración Eje PLC ##
### Cuestionario ###
1. ¿Qué librería de PLC permite controlar un eje NC?
2. ¿Cómo se llama el FB que vincula el eje NC con PLC?
3. ¿Qué FB permite habilitar el eje desde PLC?
4. ¿Qué FB permite hacer un movimiento absoluto a una posición?
5. ¿Puedo dejar sin asignar las dinámicas del FB del punto 4? Si la respuesta es si, que dinámicas se usan en tal caso?
6. ¿La entrada Execute de los FB's de motion trabaja por nivel o flanco ascendente?
7. ¿Cuando se resetean las salidas de un FB (done, error...) de motion?
8. ¿Los FB's de motion se deben llamar de forma cíclica?
9. ¿En que variable del AXIS_REF se puede consultar la posición y velocidad actual del eje?
10. ¿En que variable del AXIS_REF se puede consultar el error de seguimiento del eje?
11. ¿Qué acción del AXIS_REF se debe llamar para que se actualicen todos los valores que nos envia el eje NC a través de la estructura NcToPlc?

### Práctico ###
1. Crea un FB llamado FB_Axis que tenga definidos los siguientes FB's: Axis (tipo AXIS_REF), MC_Power, MC_Reset, MC_MoveAbsolute, MC_Jog, MC_Halt, MC_Stop como variables d'entrada. Haz la llamada de todos los FB's anteriores en el cuerpo principal del FB. Asigna el Axis a cada bloque.  
2. Crea dos instancias del FB_Axis en un GVL llamado GVL_Ejes. Complia y vincula los dos ejes creados en el módulo anterior.
3. Crea un programa Motion que llame a los FB_Axis. Comprueba el correcto funcionamiento del MC_Power y MC_Jog escribiendo valores a sus entradas desde el editor de PLC de TwinCAT. 
4. Crea una secuencia en el programa Motion que habilite los dos ejes y haga un posicionado absoluto a 0 a una velocidad del 30 % de la velocidad máxima del eje con las dinámicas por defecto. Usa el FB_Axis para la implementación.
5. Modifica el FB_Axis y el programa Motion para obtener la misma funcionalidad del módulo anterior (02_EjeNC).


