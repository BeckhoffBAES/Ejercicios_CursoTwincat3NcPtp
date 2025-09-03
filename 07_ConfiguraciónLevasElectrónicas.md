## 7. Levas Electrónicas ##
### Cuestionario ###
1. ¿Qué diferencia hay entre un sincronismo lineal y una leva electrónica?
2. ¿Qué permite la TE1510?
3. ¿Qué limitación tiene la TE1510 cuando se usa sin licencia?
4. ¿Qué permite la TF5050?
5. ¿Qué función tiene la FB MC_CamTableSelect?
6. ¿Qué función tiene la FB MC_CamIn?
7. ¿Qué función tiene la FB MC_CamOut?
8. ¿Qué dos tipos de tablas existen des del punto de definición de los puntos?
9. ¿Qué diferencia hay entre un acoplamiento relativo o absoluto?
10. ¿Qué FB permite saber el ID de la tabla que está activada en el esclavo?

### Práctico ###
1. Utilizando la TE1510 crea una tabla de tipo *motion function point* y activala desde el proyecto de Motion. Usa un eje NC como master y el otro como seguidor. 
2. Añade al FB_Axis los FB's de MC_CamIN_v2, MC_CamTableSelect y MC_MoveVelocity. 
3. Modifica la leva según la tabla siguiente con el TE1510. 

| Posición Master   | Posición Eslavo   | Tipo de movimiento    |
| --------          | -------           | -------               |
| 0                 | 0                 |
| 1440              | 720               | aceleración (interpolación (Poly5_MM))
| 2160              | 1440              | velocidad constante (Synchron (Poly1))
| 3600              | 2160              | deceleración (interpolación (Poly5_MM))

4. Añade a la secuencia de PLC realizada en los módulos anteriores, el acople de la leva del punto 3 contra el canal 2 y el posterior movimiento en velocidad del master (canal 1). Usa el interruptor SF11 para iniciar y reiniciar la secuencia. Verifica el movimiento del esclavo con un proyecto de scope.    

