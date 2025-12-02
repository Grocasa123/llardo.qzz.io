# Guía Completa de Migración - Llardo Web

## Opción 1: Subir archivos directamente (más fácil)

### Paso 1: Preparar los archivos
1. Tienes 4 archivos principales:
   - `index.html` (página principal)
   - `script.js` (animaciones y efectos)
   - `responsive.css` (diseño responsivo)
   - `hero-bg.jpg`, `features-bg.jpg`, `about-bg.jpg` (imágenes de fondo)

### Paso 2: Métodos de subida

#### Método A: FTP/SFTP
```bash
# Conectar por FTP (si tu hosting lo permite)
ftp llardo.qzz.io
# Usuario: tu_usuario
# Contraseña: tu_contraseña

# Subir archivos
put index.html
put script.js  
put responsive.css
put *.jpg
```

#### Método B: Panel de Control (cPanel/Plesk)
1. Accede a tu panel de control del hosting
2. Busca "Gestor de Archivos" o "File Manager"
3. Navega al directorio `/public_html/` o `/www/`
4. Sube todos los archivos

#### Método C: WordPress (si usas WP)
1. Instala plugin "File Manager"
2. Ve a WP Admin → File Manager
3. Sube archivos a la raíz del sitio

## Opción 2: Usar la web actual como plantilla

### Si tu hosting actual tiene un editor:
1. Accede al editor de tu sitio actual
2. Ve a "Páginas" → "Página Principal"
3. Cambia a "Editor de Código" o "HTML"
4. Reemplaza TODO el contenido con el código de `index.html`
5. Sube `script.js` y `responsive.css` como archivos separados
6. Actualiza las rutas en el HTML:
   ```html
   <link rel="stylesheet" href="/responsive.css">
   <script src="/script.js"></script>
   ```

## Opción 3: WordPress Avanzado

### Si usas WordPress y quieres mantenerlo:
1. Crea una nueva página en WP
2. Instala plugin "Insert PHP" o "Code Snippets"
3. Copia el contenido de `index.html` en la página
4. Sube los archivos adicionales al directorio `/wp-content/uploads/`

## Opción 4: Reemplazo Total (recomendado)

### Paso 1: Backup actual
```bash
# Si tienes acceso SSH
zip -r backup_llardo_$(date +%Y%m%d).zip /var/www/html/
```

### Paso 2: Limpieza y subida
1. Borra todo el contenido actual (¡haz backup primero!)
2. Sube solo estos archivos:
   - index.html
   - script.js
   - responsive.css
   - hero-bg.jpg
   - features-bg.jpg
   - about-bg.jpg

## Verificación y Testing

### Después de subir:
1. Accede a https://llardo.qzz.io/
2. Verifica que:
   - ✅ La página carga correctamente
   - ✅ Las animaciones funcionan
   - ✅ Los colores se ven bien
   - ✅ Es responsiva en móvil
   - ✅ Las imágenes se cargan

### Si algo no funciona:
1. Abre la consola del navegador (F12)
2. Mira si hay errores en "Console"
3. Verifica que todos los archivos se cargaron
4. Comprueba las rutas de los archivos

## Solución de Problemas Comunes

### Problema: "Página en blanco"
- Solución: Verifica que `index.html` esté en la raíz
- Asegúrate de que el hosting soporte HTML5

### Problema: "Sin estilos/CSS"
- Solución: Verifica la ruta de `responsive.css`
- Asegúrate de que el archivo se haya subido correctamente

### Problema: "Sin animaciones"
- Solución: Verifica que `script.js` esté cargado
- Mira la consola por errores de JavaScript

### Problema: "Sin imágenes"
- Solución: Verifica que las imágenes .jpg estén subidas
- Comprueba las rutas en el CSS

## Contacto para Ayuda

Si necesitas ayuda adicional:
1. Verifica la documentación de tu hosting
2. Contacta soporte técnico de tu proveedor
3. Consulta foros de tu plataforma específica

## Notas Importantes

- **Backup**: Siempre haz backup antes de cambios
- **DNS**: Los cambios pueden tardar 24-48 horas en propagarse
- **Cache**: Limpia la caché del navegador después de subir
- **SSL**: Asegúrate de que tu dominio tenga HTTPS activo

¡Tu web está lista para impresionar! 🚀