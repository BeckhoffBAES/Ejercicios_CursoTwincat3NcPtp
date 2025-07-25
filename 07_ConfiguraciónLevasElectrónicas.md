## 7. Levas Electrónicas ##
### Cuestionario ###
1. ¿Qué diferencia hay entre un sincronismo lineal y una leva electrónica?
2. ¿Qué permite la TE1510?
3. ¿Qué limitación tiene la TE1510 cuando se usa sin licencia?
4. ¿Qué permite la TF5050?

### Práctico ###
1. Utilizando la TE1510 crea una leva y activala. Usa un eje NC como master y el otro como seguidor. 
2. Modifica el FB_Axis y el programa de motion para obtener la misma funcionalidad que el punto anterior.
3. Modifica la leva según la tabla de más abajo. Los dos ejes deben partir de 0º y el acople debe ser en absoluto. Verifica el comportamiento con un proyecto de scope.

| Posición Master   | Posición Eslavo   | Tipo de movimiento    |
| --------          | -------           | -------               |
| 0º                | 0º                |
| 360*4º            | 360*2º            | aceleración
| 360*2º            | 360*2º            | velocidad constante
| 360*4º            | 360*2º            | deceleración

    

