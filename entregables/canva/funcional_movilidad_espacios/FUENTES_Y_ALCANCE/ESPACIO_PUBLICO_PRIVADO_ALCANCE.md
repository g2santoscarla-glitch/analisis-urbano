# Espacio público y parcelario · cuatro barrios

Se han revisado los archivos oficiales disponibles y se ha consultado el Inventario de bienes inmuebles del Ayuntamiento de Madrid, edición 2025. Ámbito: San Juan Bautista (156), San Pascual (155), La Piovera (162) y El Salvador (208).

## Resultado cartográfico utilizable

`espacios_publicos_parcelario_4barrios.geojson` permite representar seis componentes con geometría original en EPSG:25830:

1. **Parques y viveros municipales PV24**: Parque Juan Pablo II, Quinta de los Molinos y Quinta de Torre Arias, dentro de los límites del ámbito. Su contrato identifica parques y viveros municipales; no incorpora puertas ni horarios.
2. **Verde inventariado ZV21**: superficies de conservación municipal, incluidas glorietas y zonas ajardinadas. No todas son parques ni espacios transitables.
3. **Calles y viario cartografiado**: superficie oficial del Callejero municipal. Representa la red física, no un deslinde registral de dominio público.
4. **Tejido parcelado de titularidad no determinada**: parcelas catastrales fuera de los componentes anteriores. No se las clasifica como privadas por descarte.
5. **Otros espacios de titularidad no determinada**: superficie restante, en gris neutro.
6. **Espacio edificado**: huella superpuesta a los componentes anteriores; contiene edificios de cualquier titularidad y no se debe sumar nuevamente a las áreas de las clases base.

Las cinco clases base son excluyentes y cubren el 100 % de cada barrio. No se han simplificado ni desplazado geometrías. Las superficies y la comprobación están en los CSV y JSON de validación.

## Título y leyenda recomendados

**«Espacio de uso público y tejido parcelado: lectura física»**.

En la leyenda: «Calles y viario», «Parques municipales», «Verde en conservación», «Tejido parcelado: titularidad no determinada», «Espacio edificado» y «Otros espacios sin clasificar».

Nota visible: **«La distinción es física y funcional. Catastro no publica la propiedad en esta descarga: el parcelario y la huella no equivalen automáticamente a propiedad privada.»**

Es válido explicar que la red de calles y parques estructura el uso público y que la implantación de parcelas y edificios delimita otros espacios. No es válido publicar una proporción de propiedad privada o identificar todas las zonas parceladas como privadas.

## Nueva comprobación de inmuebles municipales

El directorio oficial 300025-0, recurso 300025-64, contiene 1.547 inmuebles en 2025: 1.215 registros en subepígrafe «DOMINIO PÚBLICO» y 332 «PATRIMONIAL». El régimen patrimonial también pertenece al Ayuntamiento y no significa propiedad privada.

La tabla no tiene coordenadas, geometrías ni referencias catastrales. Las direcciones simples se han cruzado con coincidencia exacta única de tipo de vía, nombre y número en el Callejero oficial de octubre de 2026. Los puntos que quedan dentro de los cuatro barrios se guardan en `bienes_municipales_puntos_4barrios.geojson` y CSV. Sirven para identificar inmuebles municipales localizados y para contrastar equipamientos.

Un punto representa el portal oficial asociado al inmueble inventariado. No permite adjudicar toda la parcela a un único titular ni determinar acceso público a todos sus espacios. Los registros sin coincidencia exacta única no se geolocalizan. La comprobación se documenta en `bienes_municipales_geocodificacion_control.json`.

## Fuentes

- Dirección General del Catastro: INSPIRE Cadastral Parcels, Madrid, actualización ATOM 21/08/2026. Descarga original y SHA en `resultados/atlas_mapas_4barrios/especial/fuente_parcelario.json`.
- Ayuntamiento de Madrid, Geoportal/SIGMA: Callejero, Edificios/Alturas y Límites administrativos; consultas originales 04/11/2026.
- Ayuntamiento de Madrid, conservación de zonas verdes ZV21 y parques/viveros PV24; capas MEDIO_AMBIENTE/CONSERVACION_ZZVV/4 y /5, consulta original 04/11/2026.
- Ayuntamiento de Madrid: [Inventario de bienes inmuebles, 2025](https://datos.madrid.es/dataset/300025-0-inventario-bienes/resource/300025-64-inventario-bienes/download/300025-64-inventario-bienes.csv), consulta 05/11/2026. Copia CSV original y manifiesto SHA en este directorio.
- Callejero municipal, numeraciones vigentes de octubre de 2026; original temporal `/tmp/callejero_vigente_numeraciones_202610.csv`. Fuente y SHA verificables en `resultados/bloques_sociales/apoyo/agentes_callejero_fuente.json`.

Se conservan las fuentes y los entregables anteriores sin modificarlos. Esta cartografía no sustituye a una comprobación registral de propiedad o de dominio público.
