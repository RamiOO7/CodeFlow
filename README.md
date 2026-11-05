# CodeFlow

App web (PWA) para aprender a programar con lecciones cortas, preguntas y prácticas. Funciona sin conexión y se puede instalar en el móvil.

**Lenguajes:** Python · JavaScript · Java · C

## Características

- Lecciones breves con quizzes y ejercicios prácticos
- Instalable como app (PWA) y funciona offline
- Cuentas locales (usuario y contraseña), con progreso guardado por usuario en cada dispositivo
- Varios lenguajes a la vez, cambiables desde Ajustes
- 5 temas de color y menú inferior estilo burbuja
- Sin dependencias ni build: HTML + JS puro

## Probarlo

Demo: `https://TU_USUARIO.github.io/CodeFlow/`

En local, sirve la carpeta con cualquier servidor estático (el service worker no funciona con `file://`):

```bash
python3 -m http.server 8000
```

y abre <http://localhost:8000>.

## Estructura

```
index.html              App completa
sw.js                   Service worker (caché offline)
manifest.webmanifest    Configuración PWA
icon-192.png, icon-512.png
l/                      Lecciones por lenguaje (JSON)
```

## Añadir lecciones

Cada archivo de `l/` es una lista de secciones con lecciones (`n` nombre, `i` icono, `t` teoría, `q` preguntas `texto|op1|op2|op3|índiceCorrecto`, `p` práctica con regex `r`).

## Licencia

MIT © 2026 RamiOO7. Ver [LICENSE](LICENSE).
