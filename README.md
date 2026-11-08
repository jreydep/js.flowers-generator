# ASCII Flowers 🌸

Generador procedural de flores mediante caracteres ASCII, utilizando JavaScript y Canvas.

El proyecto explora la generación de formas florales a través de parámetros configurables, variaciones aleatorias y composición por componentes.

## Características

- Generación procedural de flores.
- Diferentes tipos de flores y configuraciones.
- Variaciones en pétalos, pistilo, tallo y hojas.
- Generación pseudoaleatoria mediante Mulberry32.
- Renderizado mediante HTML Canvas.
- Representación textual ASCII.
- Configuración centralizada de parámetros.
- Herramientas de depuración para analizar la generación.

## Instalación

No requiere instalación de dependencias, servidor ni proceso de compilación.

Puedes clonar el repositorio:

```bash
git clone https://github.com/jreydep/js.flower-generator.git
```

Y abrir `index.html` directamente en el navegador.

## GitHub Pages

El proyecto puede ejecutarse directamente desde GitHub Pages, sin necesidad de backend.

Una vez habilitado GitHub Pages en la configuración del repositorio, estará disponible en:

https://jreydep.github.io/js.flowers-generator/

## Configuración

Los parámetros de generación están agrupados en diferentes objetos para facilitar su modificación.

### FONT

Configuración tipográfica utilizada durante el renderizado.

- `family`: familia tipográfica.
- `size`: tamaño de fuente.
- `lineHeight`: referencia utilizada para las métricas tipográficas.

### GRID

Configuración de la cuadrícula sobre la que se construye la flor.

- `cellWidth`: anchura de cada celda.
- `cellHeight`: altura de cada celda.
- `columns`: número de columnas calculado dinámicamente.
- `rows`: número de filas calculado dinámicamente.

### COLORS

Paletas de colores utilizadas en los diferentes componentes:

- `background`: fondo.
- `petals`: pétalos.
- `pistil`: pistilo.
- `stem`: tallo.

### LEAVES

Parámetros de generación de las hojas:

- `characters`: caracteres disponibles.
- `colors`: colores disponibles.
- `irregularity`: irregularidad de la forma.
- `length`: longitud.
- `width`: anchura.
- `variation`: variaciones de longitud, anchura y ángulo.

### PISTIL

Parámetros del centro de la flor:

- `characters`: caracteres disponibles.
- `colors`: colores disponibles.
- `irregularity`: irregularidad de la forma.
- `variation`: variaciones de luminosidad del color.

### PETALS

Configuración de los pétalos:

- `characters`: caracteres disponibles.
- `colors`: colores disponibles.
- `distributions`: distribución angular de los pétalos.
- `shapes`: formas disponibles y sus características geométricas.
- `variation`: variaciones de ángulo, curvatura, bordes, color, longitud y anchura.

Las distribuciones permiten controlar el comportamiento angular de los pétalos, desde una disposición uniforme hasta distribuciones con mayor irregularidad.

### STEM

Parámetros de generación del tallo:

- `characters`: caracteres disponibles.
- `colors`: colores disponibles.
- `curvature`: curvatura.
- `irregularity`: irregularidad.
- `variation`: variaciones de color y curvatura.

### FLOWER_TYPES

Define las características particulares de cada tipo de flor.

Incluye parámetros relativos al pistilo, pétalos, capas, tallo y hojas.

Actualmente están definidos los tipos Daisy y Sunflower. La generación activa utiliza Sunflower.

### DEBUG

Conjunto de categorías que permiten activar información de depuración:

- `ascii`: representación textual de la flor.
- `boundaries`: análisis de caracteres fuera de los límites de la cuadrícula.
- `dimensions`: dimensiones ocupadas por cada componente.
- `metrics`: métricas tipográficas y dimensiones de las celdas.
- `seed`: semilla utilizada en la generación.

## Semillas y generación aleatoria

El proyecto utiliza un generador pseudoaleatorio basado en Mulberry32.

Es importante distinguir entre:

- **Random:** el generador pseudoaleatorio que produce una secuencia de valores.
- **Seed:** el valor inicial utilizado para establecer el estado del generador.

La semilla inicializa el generador, pero no representa por sí sola una descripción completa de la flor.

La secuencia generada depende también del orden de las operaciones y de la configuración utilizada.

### Reproducción de generaciones

**WORK IN PROGRESS**

La reproducción completa de una generación requiere conservar información adicional a la semilla, como el tipo de flor y la versión de la configuración y del generador.

## Tecnologías

- HTML5
- CSS3
- JavaScript
- Canvas API

No utiliza frameworks ni dependencias externas.

## Licencia

Este proyecto se distribuye bajo la licencia MIT.

Consulta el archivo `LICENSE` para conocer sus condiciones.
