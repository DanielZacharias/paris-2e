# Les Deux Étoiles — París 2★ Michelin 2026

Página de una sola vista para elegir restaurante entre Lu, Rodri y Daniel: las 21 mesas de
dos estrellas Michelin de París (guía 2026) cruzadas con puntajes de Google Maps y precios
aproximados por persona.

**Publicada en:** https://danielzacharias.github.io/paris-2e/

## Cómo se guardan los puntajes

Los puntajes (1–5) y los comentarios se comparten entre los tres y se actualizan solos cada
8 segundos. No hay backend propio: cada persona tiene su propio documento en
[textdb.online](https://textdb.online), un store de texto gratuito y sin cuenta.

- Una fila escribe **solo** en el documento de esa persona, así dos personas cargando filas
  distintas nunca se pisan. Si dos editan la *misma* fila a la vez, queda el último cambio.
- Todo queda además en `localStorage` como respaldo: si el store no responde, la página sigue
  andando y no se pierde nada localmente.
- Las claves son aleatorias y no están listadas en ningún índice, pero **no hay autenticación**:
  cualquiera que tenga el link puede leer y escribir. Es una lista de restaurantes, no un secreto.

El ranking del grupo está al pie a propósito, para no sesgar la votación de quien recién entra.

## Dar de baja

Es una página pensada para durar unos días. Para borrarla junto con su URL:

```bash
gh repo delete DanielZacharias/paris-2e --yes
```

Los documentos de textdb caducan solos por falta de uso.
