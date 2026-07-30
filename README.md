# Une Étoile — los 1★ de París hasta €200

Página de una sola vista para elegir restaurante entre Lu, Rodri y Daniel: 17 mesas de una
estrella Michelin en París que entran en €200 por persona, cruzadas con los puntajes de
Google Maps y con la apertura del viernes 25 y sábado 26 de septiembre de 2026.

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

Del set actual, 16 de 17 abren el viernes 25 y solo 7 el sábado 26.

## Dar de baja

```bash
gh repo delete DanielZacharias/paris-2e --yes
```

Los documentos de textdb caducan solos por falta de uso.
