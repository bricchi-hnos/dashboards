# Bricchi Stand Apache — App de Contactos Expo 2026

## Cómo subir a Vercel (5 minutos)

### Opción A: Drag & Drop (más fácil, sin cuenta GitHub)
1. Ir a https://vercel.com → Sign up con Google o email
2. En el dashboard, buscar "Add New → Project"
3. Elegir "Deploy from local folder" o usar la CLI
4. Subir los archivos: index.html, sw.js, manifest.json, vercel.json

### Opción B: Via GitHub (recomendado para actualizar fácil)
1. Crear repo en GitHub con estos 4 archivos
2. Conectar en Vercel → automático

## Qué hace cada archivo
- `index.html` — La app completa (formulario + lista + exportación)
- `sw.js` — Service Worker: hace que funcione offline
- `manifest.json` — Permite instalar como app en el celu
- `vercel.json` — Configuración del hosting

## Antes de ir a la expo
1. Subir a Vercel → obtener URL (ej: bricchi-expo.vercel.app)
2. Cada vendedor abre esa URL en su celu CON SEÑAL
3. Chrome/Safari la cachea automáticamente → funciona offline
4. OPCIONAL: "Agregar a pantalla de inicio" para acceso rápido

## En el stand
- Formulario: Nombre + Celular + Producto + Observaciones
- Guardar → aparece modal para mandar WhatsApp automático
- Tab "Contactos" → ver todos los guardados del día
- Botón CSV → descarga archivo para abrir en Excel

## Al terminar el día
1. Cada vendedor exporta su CSV
2. Se mandan los 3 archivos por WhatsApp/email
3. Se unen en Excel

## Notas técnicas
- Datos en localStorage del navegador (no se borran al cerrar)
- Funciona 100% sin internet (después de primera carga)
- Compatible Chrome Android / Safari iPhone
- El CSV tiene BOM UTF-8 para que Excel lo lea bien
