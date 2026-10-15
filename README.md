# Recursos docentes de Manuel Jesús Rodríguez Arabi

Este repositorio contiene el código fuente de [mrodara.github.io](https://mrodara.github.io), una web de recursos y ejercicios para los módulos profesionales impartidos por Manuel Jesús Rodríguez Arabi en el IES Al-Ándalus. El sitio se genera con Jekyll, utiliza una adaptación local del tema Modernist y se publica mediante GitHub Pages.

## Consultar los recursos

La [portada del sitio](index.md) da acceso actualmente a estos módulos:

- [Implantación de Aplicaciones Web (IAW)](mods/iaw.md)
- [Servicios de Red e Internet (SRI)](mods/sri.md)
- [Programación Orientada a Objetos (POO)](mods/poo.md)

El directorio `mods/` también contiene páginas de otros módulos. Cada página reúne, según el contenido disponible, presentaciones, actividades prácticas, tutoriales, vídeos y enlaces de consulta. Los materiales descargables se almacenan principalmente en `documentos/` y `presentaciones/`.

## Ejecutar el sitio en local

### Requisitos

- Ruby
- RubyGems
- Bundler

### Puesta en marcha

```bash
git clone https://github.com/mrodara/mrodara.github.io.git
cd mrodara.github.io
script/bootstrap
bundle exec jekyll serve
```

La web estará disponible en [http://localhost:4000](http://localhost:4000). Para detener el servidor, pulsa `Ctrl+C`.

`script/bootstrap` instala Bundler y las dependencias declaradas por el proyecto. Si ya dispones de Bundler, también puedes preparar el entorno con `bundle install`.

## Estructura esencial

| Ruta | Responsabilidad |
| --- | --- |
| `index.md` | Portada y navegación principal del sitio. |
| `mods/` | Páginas Markdown de los módulos profesionales. |
| `documentos/` | Documentos y materiales descargables. |
| `presentaciones/` | Presentaciones servidas desde el propio repositorio. |
| `images/` y `assets/` | Imágenes, estilos, JavaScript y otros recursos visuales. |
| `_config.yml` | Configuración de Jekyll y del sitio. |
| `_layouts/`, `_includes/` y `_sass/` | Personalización local del tema Modernist. |
| `script/` | Preparación del entorno, construcción y validaciones. |

Jekyll genera el sitio en `_site/`. Este directorio es un artefacto local y no debe añadirse al control de versiones.

## Publicación con GitHub Pages

El repositorio corresponde al sitio de usuario `mrodara.github.io` y su rama principal es `master`. El flujo de publicación previsto es:

1. Crear una rama de trabajo desde `master`.
2. Editar el contenido y comprobarlo en local.
3. Subir la rama al repositorio remoto y abrir una Pull Request con destino a `master`.
4. Revisar y fusionar la Pull Request.
5. Comprobar la publicación en [mrodara.github.io](https://mrodara.github.io).

Para que el último paso sea automático, la configuración de GitHub Pages del repositorio debe usar la rama `master` como fuente de publicación.

## Contribución y mantenimiento

Antes de proponer un cambio:

1. Trabaja en una rama con un propósito concreto.
2. Mantén los enlaces relativos cuando el recurso pertenezca a este repositorio.
3. Si incorporas un módulo a la navegación pública, actualiza también `index.md`.
4. Comprueba que el sitio se construye:

   ```bash
   bundle exec jekyll build
   ```

5. Para ejecutar todas las validaciones incluidas en el repositorio, usa:

   ```bash
   script/cibuild
   ```

6. Crea commits descriptivos y abre una Pull Request contra `master`.

No edites directamente `_site/`: corrige siempre los archivos fuente Markdown, las plantillas o los recursos originales.

## Licencia

Consulta el archivo [LICENSE](LICENSE) para conocer las condiciones aplicables al contenido del repositorio.
