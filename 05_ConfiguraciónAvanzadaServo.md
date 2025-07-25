## 5. Configuración Avanzada Servo ##
### Cuestionario ###
1. ¿Cuando se cambia un parámetro del drive AX8000 en el DM2 dónde se queda guardado, en el propio drive o en el *startup list*?
2. ¿Después de cambiar algún parámetro del DM2 debo activar configuración?
3. ¿En que pantalla del DM2 se puede ver el listado de parámetros del canal 1 del AX8206?
4. Comprueba la configuración de corriente del AX8206. ¿Qué valor tiene la corriente de pico de cada canal respecto la corriente nominal? ¿Hasta que valor es posible configurarla?
![](/images/ConfigCorrienteCanalesAX8000.png)
5. ¿En que pantalla del DM2 puedo invertir el sentido de giro del servo?
6. ¿Para que sirve el control de módulo del AX8000?
7. ¿Para que sirve el *position offset* del AX8000?
8. ¿Qué necesito configurar en el DM2 para poder hacer un control de par con el AX8000 con límite de velocidad?
9. ¿En que pantalla del DM2 puedo configurar la reacción del drive ante un error?

### Práctico ###
1. Añade el par actual en el *process data* de los dos canales del AX8206 y verifica su valor a través del AXIS_REF.
2. Consulta el código de error del drive mediante la librería TC2_MC2_drive. 
3. Consulta el histórico de errores del drive mediante la librería Tc3_EtherCATDiag.
4. Configura que la reacción ante un error de drive sea por rampa con una deceleración que permita para el eje con un máximo de 0.5s desde máxima velocidad. 
5. Haz un tunning manual de las constantes del bucle de posición y velocidad para minimizar el error de seguimiento sin que el eje vibre ni genere ruido. <br> 
:warning: NOTA: Utilitza la función de *reversing sequence* para generar un movimiento alternativo entre 0º y 3600º (10 vueltas) con el tiempo mínimo posible.