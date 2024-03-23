CONFIRACION DEL USUARIO JENKINS:
El uso del comando sudo (comando para la ejecución de llamadas al sistema para usuarios administradores), el uso de la contraseña para la ejecución de cada comando siempre se hace presente, por lo que el flujo de ejecución del pipeline siempre se verá interrumpido por falta de permisos . Pero para poder evitar esto y que Jenkins pueda seguir con su ejecución, debemos modificar el archivo /etc/sudoers.tmp.
    
    1. Ejecutamos el comando “visudo”
    2. Nos dirigimos a la parte de especificación de privilegios de usuarios
    3.Ingresamos la siguiente sentencia:
        a. jenkins ALL=(ALL:ALL) NOPASSWD:ALL
        b. NOPASSWD:ALL → Especificamos que este usuario no ingrese la clave
        ada vez que ejecuta un comando como sudo.



CONFIGURACION DE MAIL (Extended E-mail Notification)

    1. Sobre el menú principal de jenkins, nos dirigimos hacia “Administrar Jenkins”.
    2. Ingresamos a la sección de sistemas “System”.
    3. En la seccion de E-mail 
        a. Ingresamos correo, con el cual enviaremos la notificación (SMTP SERVER)
        b. Definimos el puerto SMTP, en este caso el puerto: 465 (SMTP PORT)
        c. Definimos el tipo de texto a enviar, en este caso será un texto plano, aunque también puede ser un texto con formato HTML para una mejor personalización.
           (Default Content Type)
        e. Configuramos el servidor saliente (Servidor de correo saliente): ej --> smtp.gmail.com
    4. Ingresamos en la casilla de configuración avanzada, el cual nos desplegara otro formulario con datos que anteriormente ingresamos, pero volvemos a ingresar (Usuario y 
       Puerto), pero con la diferencia de que ahora es necesario el ingreso de la contraseña del Usuario.


