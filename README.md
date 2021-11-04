# Entorno de Desarrollo 
- Entorno Docker para usar en DAW
- Clone el directorio en su espacio de trabajo

    ```bash
    git clone git@github.com:dawish21/entorno.git
    ```

## Gestionar el servicio
-  Acceda a la consola y vaya hasta el directorio "entorno"
    `cd entorno`
- Desde ahí ya se puede:
    - Iniciar servicio:
        `docker-compose up -d`
    - Parar servicio
        `docker-compose down`
    - Ver máquinas corriendo
        `docker-compose ps`

# Variantes de este entorno

- Vamos a crear distintos entornos.
- Cada rama de este repositorio configura un entorno diferente.

# Configuración de esta rama

- Se definen varios servicios
  - proxy: recibe todas las peticiones web y las reparte entre los distintos servicios http (apace). Usamos la imagen jwilder/nginx-proxy
  - web1: sitio web de ejemplo. Imagen php:7.3-apache
  - web2: sitio web de ejemplo. Imagen php:7.3-apache
- Ya puedes acceder por el puerto 80 a dos sitios distintos.
- No olivdes configurar correctamente el /etc/hosts

    ```
    127.0.0.1	web1.com www.web1.com
    127.0.0.1	web2.com 
    ```
