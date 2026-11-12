# Guía de buceo en el Caribe colombiano

Página web con inicio de sesión (Firebase Authentication) y contenido administrable guardado en Firestore (proyecto **buceo-base-de-datos**).

## Estructura del contenido

Toda la información vive en la colección **`contenido`** de Firestore. Cada documento tiene un campo `tipo` que define en qué sección aparece:

| tipo | Sección de la página | Campos principales |
|---|---|---|
| `destino` | ¿Dónde sumergirse? + tabla comparativa | titulo, subtitulo, descripcion, etiquetas, ilustracion, imagenUrl, atractivo, condiciones, nivel, epoca, orden |
| `nivel` | ¿Qué nivel necesitas? | titulo, subtitulo, lista, estilo, orden |
| `temporada` | ¿Cuándo ir? | meses, titulo, descripcion, orden |
| `consejo` | Consejos para bucear | titulo, descripcion, orden |
| `noticia` | Noticias y eventos | titulo, fecha, descripcion, imagenUrl, orden |
| `galeria` | Galería | titulo, imagenUrl, descripcion, orden |
| `perfil` | ¿A dónde voy según mi perfil? | subtitulo, titulo, descripcion, orden |

El contenido se agrega, edita y borra desde el botón **✏️ Administrar** después de iniciar sesión. Las secciones vacías no se muestran a los visitantes.

## Archivos

- `index.html`: la página completa.
- `firestore.rules`: reglas de seguridad para pegar en Firestore → Reglas.
