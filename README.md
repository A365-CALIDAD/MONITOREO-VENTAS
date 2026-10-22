# Monitoreo de Calidad de Ventas

Dashboard estático para el seguimiento del monitoreo de calidad de ventas de Claro Ecuador.

## Qué muestra

- Llamadas monitoreadas, % de venta válida (meta 90%), % con error crítico, TMO promedio y última llamada.
- Llamadas por día (válidas / no válidas) y cumplimiento por criterio de la ficha.
- Ranking por asesor (clic para filtrar todo el tablero) y resultado por producto.
- Detalle de llamadas con buscador y una revisión de inconsistencias de la base.

Cada llamada (fecha + teléfono) se cuenta una sola vez, con su evaluación más reciente.

## Fuente de datos

`index.html` lee en el navegador la hoja de Google Sheets definida en las constantes `SHEET_ID` y `GID`, exportada como CSV, y se actualiza cada `REFRESCO_MIN` minutos o con el botón **Actualizar**. La hoja debe estar compartida como "cualquier persona con el enlace puede ver". Si no lo está, se puede usar **Cargar CSV** con un archivo descargado de la hoja.

Los teléfonos se usan solo para identificar duplicados y no se muestran en el dashboard. Ten en cuenta que, al ser pública, cualquiera con el enlace de la hoja puede ver sus datos.

## Publicación

GitHub Pages puede publicar este repositorio desde la rama `main` y la carpeta raíz (Settings → Pages). No se requieren credenciales ni backend.

Para probarlo localmente, sirve la carpeta con un servidor HTTP (por ejemplo `py -m http.server`); abrir el archivo directamente con doble clic no permite leer la hoja.
