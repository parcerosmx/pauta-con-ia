---
name: auditar-mi-cuenta
description: Revisión a fondo, una sola vez, de lo que hay en la cuenta de anuncios de Meta (lo que dejó una agencia, lo heredado de antes): zona, botones sin destino, objetivo contra optimización, horario, públicos repetidos, anuncios que nunca jugaron y quién cambió qué. Sólo lee. Úsalo cuando digan «revisa mi cuenta», «qué tengo prendido», «audita lo que dejó la agencia», «por qué gasto tanto», o al tomar una cuenta nueva.
---

# Auditar mi cuenta

Se hace una vez al empezar (o al cambiar de agencia o de local). **Sólo se lee; no se cambia nada.** Lee antes la
ficha, `conocimiento/00-lo-esencial.md` y `conocimiento/12-trampas-del-conector.md`. Dimensiona: 🟡 media.

## Qué se revisa (de las campañas con gasto en los últimos 30 días)

| # | Pregunta | Cómo | Vara |
|---|---|---|---|
| 1 | ¿La zona contiene el local de hoy? | `targeting.geo_locations` de cada conjunto contra las coordenadas de la ficha | todos los círculos lo contienen (`07`) |
| 2 | ¿Cada anuncio tiene botón y un destino que se pueda contar? | creativo: llamada a la acción y enlace / WhatsApp | sin destino = dinero sin camino (`11`) |
| 3 | ¿El objetivo de campaña y la optimización del conjunto dicen lo mismo? | `objective` vs `optimization_goal` | conversaciones → WhatsApp; ojo con «visitas a la página» (`03`) |
| 4 | ¿Tiene horario lo que depende de la cocina? | horario del conjunto + gasto por hora | gasto con la cocina cerrada (`03`) |
| 5 | ¿Hay conjuntos que compiten por el mismo público? | `targeting` (Advantage+ prendido en los dos) | (`12`) |
| 6 | ¿Cómo se reparte el dinero entre anuncios? | gasto por anuncio dentro de cada conjunto | uno >80% → separar; <5% no se juzga (`05`) |
| 7 | ¿Cuánto cuesta cada conversación de ida y vuelta, y contra el techo? | `messaging_user_depth_2_message_send` | dividir entre el techo (`01`) |
| 8 | ¿Qué plato muestra cada anuncio? | vista previa del anuncio | para compartir o individual (`03`) |
| 9 | ¿Quién cambió qué en el último mes? | registro de actividad de la cuenta | cuántos cambios, quién (`05`, `09`) |
| 10 | ¿Quién tiene acceso? | lo que se pueda leer; si no, se le pregunta al dueño | el negocio es administrador (`09`) |

Si la cuenta tiene muchas campañas, puedes repartir la lectura en subagentes (uno por campaña) que **sólo lean** y
devuelvan su fila de la tabla.

## El entregable
Una página en `mi-negocio/informes/AAAA-MM-DD-auditoria.md` y, en el chat, **sólo esto**:

1. **Fecha y hora de lectura.**
2. **Lo que está bien** (2–3 líneas).
3. **Lo que está mal, ordenado por cuánto dinero se lleva**, cada uno con: qué es, cuánto se gastó ahí en 30 días
   (en pesos redondeados), qué haría yo, y su nivel 🟢/🟡/🔴.
4. **Lo que falta para medir en la sala** (`02`): si no hay «¿dónde nos viste?» ni palabra clave en WhatsApp, es lo
   primero.

No se propone más de **3 cambios**, y se dice cuál va primero. Para hacerlos, el dueño dice «hazlo» y se usa
`hacer-un-cambio` (o `armar-campana` si hay que construir algo nuevo).

## Reglas
- Nada de lo que veas se toca aquí, aunque sea obvio.
- Si un número acusa al equipo del negocio («no contestan»), primero revisa la métrica (`02`, `12`).
- Lo que una agencia reportó se compara con el registro de actividad, sin adjetivos: hechos y fechas.
