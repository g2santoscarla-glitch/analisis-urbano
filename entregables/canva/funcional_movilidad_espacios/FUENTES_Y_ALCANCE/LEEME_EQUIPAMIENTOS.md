# Equipamientos básicos · San Juan Bautista y entorno

Datos preparados el 5 de noviembre de 2026. CRS de los GeoJSON: ETRS89 / UTM zona 30N, EPSG:25830. Las distancias son al límite del barrio en línea recta, no recorridos ni áreas de servicio.

## Archivos listos para dibujar

- `equipamientos_1km.geojson` y `.csv`: 62 equipamientos con coordenadas oficiales, categoría, titularidad documentada, nombre, fuente y enlace. Se han filtrado geométricamente a 1.000 m del límite de San Juan Bautista; el rectángulo inicial del servicio no se confunde con ese radio.
- `equipamientos_500m.geojson`: 24 puntos dentro del barrio o a un máximo de 500 m de su límite, para un plano cercano.
- `equipamientos_dentro_sjb.geojson`: 9 puntos dentro del barrio.

Los nueve puntos internos son cuatro docentes públicos (CEIP San Juan Bautista, IES San Juan Bautista, El Encinar y Gigantes y Cabezudos), el Centro Cultural San Juan Bautista, el Centro Deportivo Municipal San Juan Bautista, la instalación básica San Juan Bautista–Cidamón y dos hospitales privados (HM Nuevo Belén y Hospital Universitario Arturo Soria/Clinsa).

Los centros de salud de atención primaria de la fuente sanitaria están fuera del límite del barrio. Vicente Muzas queda a unos 453 m del límite; Canal de Panamá, a unos 613 m. Esa distancia no acredita ni niega cobertura sanitaria ni accesibilidad peatonal.

## Titularidad y categorías

Los colegios, escuelas infantiles, educación especial y FP se seleccionan de categorías explícitas públicas del directorio municipal. Se contrastaron en la ficha municipal las cuatro entradas de IES: todas indican `Titularidad Público`.

Los seis hospitales y clínicas de la consulta rectangular inicial se contrastaron con su ficha municipal: todos indican `Titularidad Privado`. Cuatro quedan dentro del buffer real de 1 km. Por tanto, los hospitales cercanos no deben simbolizarse como equipamientos sanitarios públicos. Las fichas guardadas identifican los nombres publicados; no se sustituyen por marcas comerciales actuales sin otra fuente.

El directorio sanitario identifica los centros de atención primaria como Servicio Madrileño de Salud. Los centros culturales y deportivos proceden de capas oficiales municipales. La descripción del servicio deportivo cita información de 2021; no se presenta como una medición de capacidad o apertura actual.

## Fuentes oficiales

- Geoportal del Ayuntamiento de Madrid, SIGMA `GEOPORTAL/POIs_PUNTOS_DE_INTERES_TODOS/MapServer/0`: ubicación y categoría de docentes y hospitales. Consulta 05/11/2026.
- SIGMA `BIENESTAR_SOCIAL/CENTROS_DE_SALUD_DE_ATENCIÓN_PRIMARIA/MapServer/0`: centros de salud y titularidad sanitaria. Consulta 05/11/2026.
- SIGMA `CULTURA/CENTROS_CULTURALES/MapServer/5`: centros culturales municipales. Consulta 05/11/2026.
- SIGMA `GEOPORTAL/EQUIPAMIENTOS_DEPORTIVOS/MapServer/0` y `/2`: centros deportivos municipales e instalaciones básicas. Referencia de la descripción: 2021; consulta 05/11/2026.
- Fichas de `www.madrid.es`: titularidad de hospitales e institutos. Las páginas HTML y sus hashes se conservan.

Las capas que devolvían geometría nula se restituyeron exclusivamente a partir de la consulta oficial de extensión de un único elemento puntual. Se comprobó ancho y alto de extensión iguales a cero; no se interpolaron direcciones ni se asignaron centroides de calle. Los manifiestos `fuentes_descargas.json`, `fuentes_extensiones.json` y `fuentes_fichas_titularidad.json` conservan originales y SHA-256.

No se acreditan capacidad, horarios, atención al público, accesibilidad de entrada, calidad del servicio ni pertenencia a una zona de adscripción sanitaria o escolar. Los puntos son localizaciones oficiales del equipamiento, no mediciones de uso.
