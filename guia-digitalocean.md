# Guía DigitalOcean + Cloudflare - Subir tu Web

## Tu configuración actual:
- ✅ Dominio: llardo.qzz.io (DigitalOcean)
- ✅ DNS: Cloudflare 
- ✅ Certificado SSL: Cloudflare (seguridad 100%)

## Opción RECOMENDADA para ti: Static Site en DigitalOcean

### Paso 1: Crear App Static en DigitalOcean
1. Ve a tu panel de DigitalOcean
2. Ve a "Apps" en el menú lateral
3. Haz clic en "Create App"
4. Selecciona "Static Site"
5. **Importante**: Elige "GitHub" como fuente (necesitarás crear repo)

### Paso 2: Preparar GitHub (súper fácil)
1. Ve a GitHub.com
2. Crea nuevo repositorio: `llardo-web`
3. Sube estos archivos:
   - index.html
   - script.js  
   - responsive.css
   - hero-bg.jpg
   - features-bg.jpg
   - about-bg.jpg

### Paso 3: Conectar DigitalOcean con GitHub
1. En DigitalOcean Apps, autoriza conexión con GitHub
2. Selecciona tu repositorio `llardo-web`
3. Configura:
   - Source Directory: `/`
   - Output Directory: `/`
   - Build Command: (dejar vacío)

### Paso 4: Configurar el dominio
1. En App Settings → Domains
2. Haz clic en "Add Domain"
3. Escribe: `llardo.qzz.io`
4. DigitalOcean te dará un CNAME

### Paso 5: Actualizar Cloudflare
1. Ve a Cloudflare → DNS
2. Crea registro:
   ```
   Type: CNAME
   Name: @
   Target: [el CNAME que te dio DigitalOcean]
   Proxy: ON (nube naranja)
   ```

### Paso 6: Deploy y Listo!
1. DigitalOcean desplegará automáticamente
2. Tu web estará en https://llardo.qzz.io/

## Alternativa: Droplet (más avanzada)

Si quieres más control:

### Paso 1: Crear Droplet
1. DigitalOcean → Droplets → Create
2. Elige: Ubuntu 20.04, $5/mes
3. Región: la más cercana a ti
4. SSH key (o password temporal)

### Paso 2: Conectar por SSH
```bash
ssh root@tu-ip-droplet
```

### Paso 3: Instalar servidor web
```bash
# Actualizar sistema
apt update && apt upgrade -y

# Instalar nginx
apt install nginx -y

# Configurar nginx para tu dominio
nano /etc/nginx/sites-available/llardo
```

### Paso 4: Subir archivos
```bash
# En tu computadora, desde la carpeta con los archivos
scp -r * root@tu-ip-droplet:/var/www/html/
```

### Paso 5: Configurar Cloudflare
Igual que arriba, pero apuntando a la IP de tu droplet.

## ¿Cuál opción elegir?

**Static Site (RECOMENDADA para ti):**
- ✅ No necesitas conocimientos técnicos
- ✅ Despliegue automático desde GitHub
- ✅ SSL automático
- ✅ Gratis hasta cierto límite
- ✅ Perfecto para sitios estáticos

**Droplet:**
- ✅ Más control y flexibilidad
- ✅ Puedes agregar backend más adelante
- ❌ Requiere conocimientos básicos de Linux
- ❌ $5/mes mínimo

## Solución de problemas comunes:

### "No carga la página"
1. Verifica que los archivos están en GitHub
2. Mira los logs en DigitalOcean Apps
3. Asegúrate que Cloudflare apunta correctamente

### "Sin estilos o imágenes"
1. Verifica las rutas en index.html
2. Asegúrate que subiste todos los archivos

### "Error SSL"
1. En Cloudflare, asegúrate que SSL está en "Full"
2. Espera 5-10 minutos para propagación

## ¿Necesitas ayuda paso a paso?

Dime exactamente:
1. ¿Puedes acceder a tu panel de DigitalOcean?
2. ¿Tienes cuenta de GitHub?
3. ¿Prefieres la opción fácil (Static Site) o la avanzada (Droplet)?

Te ayudo con capturas de pantalla y pasos específicos para que no te quedes atascado. ¡DigitalOcean + Cloudflare es una combinación poderosa y segura! 🔒✨