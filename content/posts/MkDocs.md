---
title: "Guía para un sitio web de documentación con MkDocs Material y GitHub Pages"
date: 2025-09-02
tags: ["mkdocs", "github", "ci/cd", "documentación", "despliegue", "tutorial"]
draft: false
---
## Introducción al proyecto
Este documento detalla una guía paso a paso para la creación y publicación de un sitio web de documentación y blog utilizando **MkDocs Material**. La idea es que se pueda publicar de manera gratuita en **GitHub Pages** con **SSL (HTTPS)** y, lo más importante, que se configure un pipeline de **Integración Continua/Despliegue Continuo (CI/CD)** para automatizar las actualizaciones.

### Requisitos previos
Antes de arrancar, se necesitan un par de herramientas instaladas:
* **Python:** Es el único requisito principal, ya que MkDocs es una biblioteca de Python.
* **VS Code:** Si bien no es obligatorio, facilita mucho la edición de los archivos Markdown y la ejecución de comandos en la terminal integrada.

## Pasos para la configuración y el despliegue
Aquí están los pasos para levantar el sitio, configurarlo, y publicarlo usando Git y GitHub Actions.

### 1. Configuración inicial del proyecto
Primero, hay que armar la estructura inicial.
1.  **Crear la carpeta del proyecto:** Hacé una nueva carpeta y abrila en VS Code.
2.  **Crear y activar un entorno virtual:** Esto aísla las dependencias del proyecto.
    * `python -m venv virtual_environment`
    * Para activarlo en Windows: `virtual_environment\Scripts\activate`

---
### 2. Instalación y creación del sitio
Una vez que tenés el entorno listo, instalamos MkDocs y creamos el sitio.
1.  **Instalar MkDocs Material:** `pip install mkdocs-material`
2.  **Iniciar un nuevo proyecto:** `mkdocs new .`
3.  **Servir el sitio web localmente:** Con este comando podés ver el sitio en tu navegador mientras lo vas armando. `mkdocs serve`

---
### 3. Configuración y personalización del sitio
El archivo clave para esto es `mkdocs.yml`, donde se configura todo, desde el tema hasta los plugins.
* **Añadir el tema Material:** Tenés que especificar el tema en el archivo.
    ```yaml
    theme:
      name: material
    ```
* **Configurar la navegación y las páginas:** Se definen la estructura de los menús y las páginas. Creá los archivos `.md` en la carpeta `docs/` y organizalos en la sección `nav` del `mkdocs.yml`.
* **Añadir funcionalidades:** Se activan características como búsqueda, modo oscuro/claro y la opción de copiar código.
* **Configurar los plugins:** Los plugins son fundamentales para funcionalidades como las etiquetas (`tags`), el blog y el resaltado de código.

---
### 4. Control de versiones y publicación
Para publicar el sitio en GitHub Pages, tenés que usar Git.
1.  **Inicializar un repositorio Git:** `git init`
2.  **Crear un archivo `.gitignore`:** Esto es importante para no subir archivos innecesarios. `virtual_environment/` y `site/` son los más comunes.
3.  **Hacer el primer commit:**
    * `git add .`
    * `git commit -m "Initial commit"`
4.  **Publicar en GitHub:** Creá un repositorio en GitHub y subí tu código.

---
### 5. Configuración del pipeline CI/CD con GitHub Actions
Este es el paso mágico que automatiza el despliegue.
1.  **Configurar GitHub Pages:** En la configuración de tu repositorio en GitHub, elegí **GitHub Actions** como fuente de despliegue.
2.  **Crear el archivo de workflow:** En la carpeta `.github/workflows/`, creá un archivo YAML (por ejemplo, `ci.yml`). Este archivo va a definir las acciones automáticas, como construir el sitio (`mkdocs build`) y desplegarlo.
3.  **Realizar el commit y el push del workflow:** Subí el archivo `ci.yml` a tu repositorio. Esto va a disparar la primera ejecución del `pipeline` y tu sitio se publicará.

---
### 6. Verificación y actualización automática
Una vez que el `pipeline` de GitHub Actions termine, tu sitio va a estar en línea. Cada vez que hagas un `git push`, los cambios se van a reflejar automáticamente en tu sitio público en cuestión de minutos, sin que tengas que hacer nada más.

Esta es una manera muy eficiente de mantener un sitio de documentación siempre actualizado.