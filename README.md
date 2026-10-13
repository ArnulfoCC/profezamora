# profezamora.com

Sitio de los cursos de posgrado de Alexander Zamora. Es un sitio estático: solo archivos HTML, CSS y los materiales descargables. No necesita servidor ni base de datos y se publica gratis con GitHub Pages.

## Estructura

```
index.html                      Portada: catálogo de cursos, cómo usar el sitio, sobre el profe
404.html                        Página de error
CNAME                           Dominio del sitio (profezamora.com); no borrar
assets/site.css                 Estilos del sitio (los interactivos traen los suyos)
assets/favicon.svg              Ícono
cursos/
  matematicas/
    index.html                  Página del curso: sesiones y materiales
    interactivo.html            Página interactiva (pestañas por sesión, taller, funciones de Excel)
    materiales/                 Word, Excel y PowerPoint descargables
  planeacion/
    index.html
    interactivo.html
    materiales/
```

## Cómo actualizar

- **Cambiar un material:** reemplace el archivo en `cursos/<curso>/materiales/` con el mismo nombre. Si cambia el nombre, actualice el enlace en el `index.html` del curso.
- **Cambiar una página interactiva:** reemplace `interactivo.html` por la nueva versión completa.
- **Agregar un curso:** copie la carpeta `cursos/planeacion/` con otro nombre, edite su `index.html` (título, sesiones, lista de materiales) y agregue una tarjeta en la sección `#cursos` de `index.html`.
- **Texto de la portada:** todo está en `index.html`; la sección "Sobre el profe" es la que más conviene personalizar.

Cada cambio se publica al subirlo a la rama `main` del repositorio; GitHub Pages tarda uno o dos minutos en reflejarlo.

## Cómo se reportan errores y mejoras

En la pestaña **Issues** del repositorio hay dos formularios: *Error en el material* y *Sugerencia de mejora*. Cada reporte queda numerado, se discute ahí y se cierra cuando el material se corrige. Para abrir uno hace falta una cuenta de GitHub (gratis); quien no la tenga puede escribirle al profe y nosotros lo registramos.

## Versiones por semestre

Al cierre de cada semestre se marca el material con una etiqueta (`2026-2`, `2027-1`...). Así el material que vio cada grupo queda congelado aunque se siga mejorando para el siguiente. Las etiquetas están en la pestaña **Tags** del repositorio.

## Qué no está en el sitio (a propósito)

Los guiones docentes, los solucionarios y las guías con respuestas para el docente se quedan en la carpeta privada. Cuando el sitio tenga acceso con usuario (etapa 2) podrán ir en una zona del profe.

## Dominio

El sitio se sirve desde GitHub Pages con el dominio `profezamora.com`. En el registrador del dominio deben existir estos registros DNS:

| Tipo  | Nombre | Valor                                   |
|-------|--------|-----------------------------------------|
| A     | @      | 185.199.108.153                         |
| A     | @      | 185.199.109.153                         |
| A     | @      | 185.199.110.153                         |
| A     | @      | 185.199.111.153                         |
| CNAME | www    | `<usuario-de-github>.github.io`         |

Después, en el repositorio: Settings → Pages → Custom domain: `profezamora.com` y marcar "Enforce HTTPS" cuando el certificado esté listo (puede tardar hasta un día por la propagación del DNS).

## Hoja de ruta

1. **Vitrina y repositorio (este sitio).** Probar el material en clase y mejorarlo.
2. **Espacios por materia con acceso de estudiantes.** Registro con correo (Supabase), avisos y entregas, zona del profe con los solucionarios.
3. **Cursos abiertos y cursos pagos.** Pagos con Wompi o Mercado Pago, o venta a través de Hotmart; tutor con IA sobre el material de cada curso.
