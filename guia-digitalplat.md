# Guía DigitalPlat - Subir tu Web a llardo.qzz.io

## Tu configuración:
- ✅ Dominio: llardo.qzz.io (DigitalPlat)
- ✅ Panel de control: https://dash.domain.digitalplat.org/
- ✅ Cloudflare (para DNS)

## Opción MÁS FÁCIL: Subir archivos directamente

### Paso 1: Acceder a tu panel DigitalPlat
1. Ve a: https://dash.domain.digitalplat.org/panel/main
2. Inicia sesión con tu cuenta
3. Busca "Gestor de Archivos" o "File Manager"

### Paso 2: Subir los archivos
1. Navega hasta encontrar "Gestor de Archivos"
2. Busca la carpeta `/public_html/` o `/www/`
3. Si no existe, créala
4. Sube estos 6 archivos:
   - index.html
   - script.js
   - responsive.css
   - hero-bg.jpg
   - features-bg.jpg
   - about-bg.jpg

### Paso 3: Verificar la estructura
Tu estructura debe verse así:
```
/public_html/
├── index.html
├── script.js
├── responsive.css
├── hero-bg.jpg
├── features-bg.jpg
└── about-bg.jpg
```

### Paso 4: Configurar Cloudflare (si no está hecho)
1. Ve a Cloudflare.com
2. Asegúrate que tu dominio llardo.qzz.io esté agregado
3. En DNS Records, debe haber:
   ```
   Type: A
   Name: @
   IPv4: [IP de tu hosting DigitalPlat]
   Proxy: ON (nube naranja)
   ```

## Si no encuentras "Gestor de Archivos"

### Alternativa 1: FTP
1. En DigitalPlat, busca "Configuración FTP"
2. Anota:
   - Servidor FTP
   - Usuario FTP
   - Contraseña FTP
3. Usa un programa como FileZilla:
   - Host: [servidor FTP]
   - Usuario: [usuario FTP]
   - Contraseña: [contraseña FTP]
   - Puerto: 21
4. Sube los archivos a la carpeta `/public_html/`

### Alternativa 2: WordPress (si usas WP)
1. Accede a tu WordPress
2. Instala plugin "File Manager"
3. Ve a WP File Manager
4. Sube los archivos a la raíz

### Alternativa 3: cPanel (si tu hosting lo tiene)
1. Busca en DigitalPlat el enlace a cPanel
2. En cPanel, busca "File Manager"
3. Sube los archivos a `/public_html/`

## Verificación

Después de subir los archivos:
1. Accede a: https://llardo.qzz.io/
2. Debes ver tu web con:
   - ✅ Diseño azul oscuro elegante
   - ✅ Animaciones al hacer scroll
   - ✅ Imágenes de fondo
   - ✅ Efectos glassmorphism

## Si no funciona:

### Problema 1: "Página en blanco"
- Verifica que index.html esté en la raíz
- Asegúrate que el archivo no esté corrupto

### Problema 2: "Sin estilos"
- Verifica que responsive.css esté subido
- Mira la consola del navegador (F12) por errores

### Problema 3: "Sin animaciones"
- Verifica que script.js esté subido
- Asegúrate que el hosting permite JavaScript

### Problema 4: "Sin imágenes"
- Verifica que los 3 archivos .jpg estén subidos
- Asegúrate que los nombres coinciden exactamente

## ¿Necesitas ayuda específica?

Dime exactamente qué ves en tu panel de DigitalPlat:
1. ¿Ves "Gestor de Archivos"?
2. ¿Ves "cPanel"?
3. ¿Ves "Configuración FTP"?
4. ¿Tu sitio usa WordPress?

Con una captura de pantalla o describiendo lo que ves, te doy los pasos exactos para tu caso específico.

## Archivos que DEBES subir:

✅ index.html (obligatorio - página principal)
✅ script.js (obligatorio - animaciones)  
✅ responsive.css (obligatorio - diseño)
✅ hero-bg.jpg (imagen fondo hero)
✅ features-bg.jpg (imagen sección características)
✅ about-bg.jpg (imagen sección about)

¡Tu web con estilo aceternity-ui estará online en minutos! 🚀✨