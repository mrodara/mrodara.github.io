# Recursos de Informática · Manuel Jesús Rodríguez Arabi

Sitio web educativo de **Manuel Jesús Rodríguez Arabi**, profesor de Informática del **IES Al-Ándalus**. Reúne materiales de consulta, presentaciones, ejercicios y actividades para el alumnado de sus módulos.

**Sitio web:** [mrodara.github.io](https://mrodara.github.io/)

## Contenidos

Los materiales se organizan por módulos. La disponibilidad varía entre secciones; algunas unidades todavía no tienen recursos publicados.

| Módulo | Página | Contenido disponible |
| --- | --- | --- |
| Implantación de Aplicaciones Web | [IAW](mods/iaw.md) | Presentaciones, guías, actividades y enlaces de consulta. |
| Servicios de Red e Internet | [SRI](mods/sri.md) | Presentaciones, tutoriales, actividades y recursos sobre servicios de red. |
| Despliegue de Aplicaciones Web | [DAW](mods/daw.md) | Recursos y enlaces de apoyo. |
| Seguridad y Alta Disponibilidad | [SAD](mods/sad.md) | Materiales y recursos de consulta. |
| Horas de Libre Configuración | [HLC](mods/hlc.md) | Recursos de apoyo al módulo. |
| Programación de Inteligencia Artificial | [PIA](mods/pia.md) | Recursos de la primera unidad. |

La portada enlaza IAW, SRI y una entrada denominada POO. La página [POO](mods/poo.md) contiene actualmente el encabezado de Programación de Inteligencia Artificial, por lo que esa entrada necesita revisión.

## Organización del repositorio

| Ruta | Descripción |
| --- | --- |
| `index.md` | Portada y acceso a los módulos destacados. |
| `mods/` | Páginas de los módulos y enlaces a sus materiales. |
| `presentaciones/` | Presentaciones en PDF y PowerPoint de IAW y SRI. |
| `documentos/` | Guías, actividades y otros archivos descargables. |
| `images/` | Imágenes utilizadas en el sitio. |
| `_config.yml` | Título, descripción y configuración de Jekyll. |
| `_layouts/`, `_includes/`, `_sass/`, `assets/` | Plantillas, estilos y recursos del tema. |
| `script/` | Utilidades heredadas del tema para instalación y comprobación. |
| `docs/` | Documentación de colaboración y soporte heredada del tema. |

## Vista previa local

El sitio utiliza **Jekyll** y el tema **Modernist**, con configuración para GitHub Pages. Necesitas Ruby, RubyGems y Bundler para ejecutarlo localmente. Las dependencias se declaran en `Gemfile` y `jekyll-theme-modernist.gemspec`.

Desde la raíz del repositorio:

```sh
bundle install
bundle exec jekyll serve
```

Abre [http://localhost:4000](http://localhost:4000) para consultar la vista previa. Detén el servidor con `Ctrl+C`.

Como alternativa, `script/bootstrap` instala Bundler y ejecuta `bundle install`. La instalación de gemas depende de los permisos y de la configuración de Ruby del equipo.

La gemspec heredada declara Ruby `>= 2.4` y Jekyll `> 3.5` y `< 5.0`; esos límites no garantizan compatibilidad con cualquier combinación de versiones actual.

## Actualizar los materiales

- Edita `index.md` para cambiar los accesos de la portada.
- Edita la página correspondiente en `mods/` para añadir o actualizar recursos de un módulo.
- Guarda las presentaciones en `presentaciones/` y los demás materiales descargables en `documentos/`, y enlázalos desde la página del módulo.
- Revisa la vista previa y los enlaces antes de publicar los cambios.

Para comprobar que Jekyll genera el sitio sin iniciar un servidor:

```sh
bundle exec jekyll build
```

El script `script/cibuild` conserva comprobaciones del tema original: construcción del sitio, validación HTML, RuboCop y generación de la gema. No es una suite específica de los contenidos educativos.

## Tema y licencia

El sitio parte de [Modernist](https://github.com/pages-themes/modernist), tema para Jekyll de Steve Smith (orderedlist), con contribuciones de GitHub. El repositorio conserva sus archivos y personalizaciones locales.

El archivo [LICENSE](LICENSE) contiene la licencia **CC0 1.0 Universal**. Los materiales de terceros y los recursos externos enlazados pueden estar sujetos a sus propias licencias y condiciones de uso.
