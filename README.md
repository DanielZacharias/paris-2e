# Les Étoiles — Michelin París 2026, con tope de precio

Página de una sola vista para elegir restaurante entre Lu, Rodri y Daniel: 39 mesas de París
—18 de una estrella que entran en €200 por persona y 21 de dos estrellas— cruzadas con los
puntajes de Google Maps y con la apertura del viernes 25 y sábado 26 de septiembre de 2026.

El tope de precio (€120 / €150 / €200) filtra por lo que sale la **cena**, no por el precio
"desde": si no, un lugar de €480 con almuerzo de €150 pasaría el filtro de una cena de €200.

**Publicada en:** https://danielzacharias.github.io/paris-2e/

## Cómo se guardan los puntajes

Los puntajes (1–5) y los comentarios se comparten entre los tres y se actualizan solos cada
8 segundos. No hay backend propio: cada persona tiene su propio documento en
[textdb.online](https://textdb.online), un store de texto gratuito y sin cuenta.

- Una fila escribe **solo** en el documento de esa persona, así dos personas cargando filas
  distintas nunca se pisan. Si dos editan la *misma* fila a la vez, queda el último cambio.
- Todo queda además en `localStorage` como respaldo.
- Las claves son aleatorias, pero **no hay autenticación**: cualquiera con el link puede leer
  y escribir. Es una lista de restaurantes, no un secreto.

## Sobre los días

Los campos `vie` y `sat` de cada restaurante indican si **abre** esa noche, según la web
oficial de cada uno consultada en julio de 2026. No es disponibilidad de mesa: eso hay que
pedirlo en su sistema de reservas.

Solo se consultaron para los que entran en €200; el resto queda en `"nc"` (sin consultar) y
la ficha lo dice, en vez de aparentar un dato que no se buscó. De los consultados, 18 abren
el viernes 25 y 8 el sábado 26.

## Dar de baja

```bash
gh repo delete DanielZacharias/paris-2e --yes
```

Los documentos de textdb caducan solos por falta de uso.
