# Laboratorio TELEFONIKA

Este laboratorio pone a prueba la capacidad del alumno para detectar malas prácticas en el desarrollo web y explotar una exposición de credenciales en una landing page, de esta forma los alumnos lograran comprender:


- Analisis de código fuente HTML en busca de errores de seguridad.
- Detectar credenciales filtradas de forma inapropiada.
- Conectarse a través de SSH como un usuario descubierto.
- Acceder a una flag sin necesidad de escalar privilegios.


## Especificaciones de la maquina 🖥️

- **Sistema:** Ubuntu Server (o Debian sin GUI)
- **Servidor web:** Apache o Nginx
- **Ruta del sitio:** `/var/www/html/index.html`
- **Contenido vulnerable:** Formulario con comentario HTML oculto:

```html
<!-- Boss, I will put the credentials right here so you can test: larry:TELEFONIKA25 -->
```

- **Usuario:** `larry`  
- **Contraseña:** `TELEFONIKA25`  
- **Flag:** `/home/larry/flag.txt`  
- **Contenido de la flag:**  
  `4GEEKS{D0nt_3XP0S3_TH3_cR3d3nt14ls_L1K3_TH15!!!}`  
- **Nota:** `larry` no tiene permisos de `sudo`.

### Credenciales de la maquina

```bash
servername: telefonika-lab
username: student
password: 4geeks-lab
```


## Pasos esperados por el alumno

1. **Realiza reconocimiento de red para identificar la máquina.**
   - Utiliza herramientas como `nmap`, `netdiscover` o `arp-scan`.
   - Debe detectar una IP con los puertos **80 (HTTP)** y **22 (SSH)** abiertos.

2. **Accede al sitio web desde el navegador.**
   - Introduce la IP descubierta en el navegador para cargar la landing page de TELEFONIKA.

3. **Revisa el código fuente del sitio web.**
   - Debe identificar un comentario HTML con nombre de usuario y contraseña expuestos.

4. **Conéctate por SSH utilizando las credenciales encontradas.**
   - Inicia sesión como `larry` usando:
     ```bash
     ssh larry@<IP>
     ```
     Contraseña: `TELEFONIKA25`

5. **Encuentra y lee la flag.**
   - Está ubicada en el home de `larry` como `flag.txt`:
     ```bash
     cat ~/flag.txt
     ```