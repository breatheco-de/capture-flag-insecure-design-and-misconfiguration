# Telefonika - Análisis de código expuesto

En este laboratorio deberás analizar una página web aparentemente simple, descubrir credenciales filtradas de forma inapropiada y acceder a un sistema a través de SSH para obtener una flag. En este laboratorio aprenderás:

- Análisis de código fuente HTML
- Detección de malas prácticas en desarrollo web
- Acceso remoto vía SSH
- Lectura de flags en sistemas Linux


<how-to-start>
   
## 🌱 Cómo iniciar este laboratorio

Sigue las siguientes instrucciones para comenzar:

1. **Descarga la máquina virtual** desde este enlace:

<onlyfor withbanner="true" permission="get_private_link">
   
```url
   https://storage.googleapis.com/cybersecurity-machines/telefonika-lab.ova
```
</onlyfor>

2. **Importa la máquina** en tu gestor de virtualización preferido (VirtualBox, VMware, etc.).
3. Una vez iniciada la máquina, ¡ya puedes comenzar con el laboratorio!

</how-to-start>


## 📄 Instrucciones

Estás frente al sitio web de una empresa de servicios de internet y telefonía llamada **TELEFONIKA**. Tu tarea es analizar cómo está construida la página y descubrir si hay alguna vulnerabilidad aprovechable.


1. **Descubre la dirección IP de la máquina TELEFONIKA.**
   - La máquina está conectada a la misma red que tú, pero su IP no ha sido proporcionada.
   - Utiliza herramientas como `nmap` para escanear la red.

2. **Accede al sitio web alojado en el servidor.**
   - Abre tu navegador y visita la IP asignada.
   - Observa el contenido del formulario.

3. **Inspecciona el código fuente.**
   - ¿Hay algún comentario que no debería estar allí?
   - Pon atención a posibles fugas de información.

4. **Usa la información encontrada para conectarte por SSH.**
   - Si encuentras credenciales, intenta acceder al sistema.
   - El objetivo es entrar como un usuario del sistema real.

5. **Busca la flag.**
   - Revisa el directorio personal del usuario al que lograste acceder.
   - No se requiere escalar privilegios.



**Recuerda:** a veces las claves no están ocultas... solo mal puestas.

¡Feliz hackeo!
