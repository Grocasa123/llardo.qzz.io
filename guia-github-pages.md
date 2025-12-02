# Guía Super Fácil - Subir tu Web con GitHub Pages

## ¿Qué tienes actualmente?
- Dominio: llardo.qzz.io (de DigitalOcean)
- DNS: Cloudflare (esto es perfecto)
- GitHub: Tienes CNAME y README (excelente)

## Opción MÁS FÁCIL: GitHub Pages (GRATIS y Rápido)

### Paso 1: Preparar tu GitHub
1. Ve a GitHub.com y accede a tu cuenta
2. Crea un nuevo repositorio llamado: `llardo.qzz.io`
3. **IMPORTANTE**: El nombre del repositorio DEBE ser exactamente tu dominio

### Paso 2: Subir los archivos a GitHub
1. En tu repositorio nuevo, haz clic en "Upload files"
2. Sube estos 6 archivos:
   - index.html
   - script.js
   - responsive.css
   - hero-bg.jpg
   - features-bg.jpg
   - about-bg.jpg

### Paso 3: Activar GitHub Pages
1. Ve a Settings → Pages (en tu repositorio)
2. En "Source" selecciona "Deploy from a branch"
3. Selecciona "main" branch y "/ (root)"
4. Haz clic en Save

### Paso 4: Configurar tu dominio
1. En Settings → Pages, ve a "Custom domain"
2. Escribe: `llardo.qzz.io`
3. Haz clic en "Save"

### Paso 5: Configurar Cloudflare (¡Esto es importante!)
1. Ve a Cloudflare.com y accede a tu cuenta
2. Busca tu dominio llardo.qzz.io
3. Ve a "DNS" → "Records"
4. Crea estos registros:
   ```
   Type: CNAME
   Name: @ 
   Target: tu-usuario-de-github.github.io
   Proxy status: ON (nube naranja)
   ```

### Paso 6: Esperar (5-10 minutos)
- GitHub tarda unos minutos en desplegar
- Cloudflare tarda unos minutos en propagar los DNS

### Paso 7: Verificar
- Accede a: https://llardo.qzz.io/
- ¡Tu web debería estar funcionando!

## ¿No tienes GitHub? Crearlo es súper fácil:

1. Ve a GitHub.com
2. Crea cuenta gratuita
3. Verifica tu email
4. Sigue los pasos de arriba

## ¿No funciona? Prueba estos fixes:

### Fix 1: Verifica GitHub Pages
- Ve a Settings → Pages en tu repo
- Mira si hay algún error de compilación
- Asegúrate que los archivos se subieron correctamente

### Fix 2: Verifica Cloudflare
- En Cloudflare, asegúrate que el CNAME apunta correctamente
- Prueba desactivando el proxy temporalmente (nube gris)

### Fix 3: Verifica el dominio
- En DigitalOcean, asegúrate que los nameservers apuntan a Cloudflare
- Debe mostrar: `ns1.cloudflare.com`, `ns2.cloudflare.com`

## Alternativa: Si GitHub no funciona

### Opción B: Netlify (también gratis)
1. Ve a Netlify.com
2. Arrastra tu carpeta con los archivos
3. Conecta tu dominio en Domain Settings
4. Configura Cloudflare igual que arriba

## ¿Necesitas ayuda paso a paso?

Dime exactamente en qué paso estás y te ayudo con capturas de pantalla y detalles específicos.

## Archivos que necesitas subir:

✅ index.html (la página principal)
✅ script.js (las animaciones)
✅ responsive.css (el diseño)
✅ hero-bg.jpg (imagen fondo)
✅ features-bg.jpg (imagen sección)
✅ about-bg.jpg (imagen about)

¡Con GitHub Pages tu web estará online en menos de 10 minutos! 🚀