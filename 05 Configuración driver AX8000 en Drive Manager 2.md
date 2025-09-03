## 5. Configuración driver AX8000 en Drive Manager 2 ##
### Cuestionario ###
1. ¿Qué TE necesito instalar previamente para configurar drives Beckhoff en TwinCAT?
2. ¿Para que se usan los 4 interruptores del frontal del kit AX8000?
3. ¿Si ya dispongo de Ejes NC préviamente creados en el proyecto que debo responder al siguiente mensaje al escanear la red EtherCAT?
![](/images/LinkDriveToNCDialog.png)
4. ¿Que debo responder si estoy escaneando por primera vez la red EtherCAT?
![](/images/ScanMotorDialog.png)
5. ¿Qué proyecto debo agregar a la solución de TwinCAT para configurar un drive Beckhoff?
6. ¿Cuando sale el siguiente dialogo, que puedo configurar en el?
![](/images/DM2InitDialog.png)
7. ¿Como debo configurar la carga en el Drive Manager 2 (DM2) si dispongo de un husillo de paso 10 mm?
8. ¿Como debo configurar la carga en el Drive Manager 2 (DM2) si dispongo un sistema mecánico con reductora i=20 y una polea de diámetro 100 mm?
9. ¿Como debo configurar la carga en el Drive Manager 2 (DM2) si dispongo un sistema mecánico con reductora i=10 y un plato rotativo de 360º?
10. ¿En que pestaña del DM2 puedo ver los parámetros del eje NC que configura el DM2 en función de la carga configurada y la placa motor del servo? 
11. ¿Que significa el siguiente estado del display del AX8000? <br>
![](/images/AX8000SafeyStateDisplay.png)
12. ¿Cuando se cambia un parámetro del drive AX8000 en el DM2 dónde se queda guardado, en el propio drive o en el *startup list*?
13. ¿Después de cambiar algún parámetro del DM2 debo activar configuración?
14. ¿En que pantalla del DM2 se puede ver el listado de parámetros del canal 1 del AX8206?
15. Comprueba la configuración de corriente del AX8206. ¿Qué valor tiene la corriente de pico de cada canal respecto la corriente nominal? ¿Hasta que valor es posible configurarla?
![](/images/ConfigCorrienteCanalesAX8000.png)
16. ¿En que pantalla del DM2 puedo invertir el sentido de giro del servo?
17. ¿Para que sirve el control de módulo del AX8000?
18. ¿Para que sirve el *position offset* del AX8000?
19. ¿Qué necesito configurar en el DM2 para poder hacer un control de par con el AX8000 con límite de velocidad?
20. ¿En que pantalla del DM2 puedo configurar la reacción del drive ante un error?

### Práctico ###
1. Instala el paquete necesario para configurar un drive Beckhoff. 
2. Pon en marcha el demo kit de AX8000 para que los dos eje NC de los módulos anteriores sean ejes reales y no simulados. 
3. Activa la función del eje NC del *reversing secuence* y comprueba que el eje se mueve. Activa el STO y revisa los errores en el DM2. Restaura el sistema para que vuelva a funcionar.
4. Añade el par actual en el *process data* de los dos canales del AX8206 y verifica su valor a través del AXIS_REF.
5. Consulta el código de error del drive mediante la librería TC2_MC2_drive. 
6. Consulta el histórico de errores del drive mediante la librería Tc3_EtherCATDiag.
7. Configura que la reacción ante un error de drive sea por rampa con una deceleración que permita parar el eje con un máximo de 0.5s desde máxima velocidad. 
8. Haz un tunning manual de las constantes del bucle de posición y velocidad para minimizar el error de seguimiento sin que el eje vibre ni genere ruido. <br> 
:warning: NOTA: Utilitza la función de *reversing sequence* para generar un movimiento alternativo entre 0º y 3600º (10 vueltas) con el tiempo mínimo posible sin que salte el error de seguimiento (*lag error*).