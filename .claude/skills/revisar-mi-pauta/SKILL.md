---
name: revisar-mi-pauta
description: La lectura semanal de la pauta de Meta (la del lunes): qué pasó en los últimos 7 días contra la vara escrita de cada campaña, cuánto costó cada conversación de ida y vuelta contra el techo, y UNA recomendación para la semana. Sólo lee. Úsalo cuando digan «cómo van mis anuncios», «la revisión del lunes», «qué hago esta semana», «¿está funcionando la pauta?».
---

# Revisar mi pauta

Lectura de la semana. **Sólo se lee.** Lee antes la ficha, la bitácora (varas vigentes y último cambio) y
`conocimiento/00-lo-esencial.md`. Si no hay techo en la ficha, dilo en una línea y usa la lectura igual.

## Paso 1 · Leer la cuenta (fresca, nunca de un informe viejo)
De la cuenta de la ficha, últimos 7 días y los 7 anteriores, **por día** (`time_increment: 1`) y por campaña /
conjunto / anuncio:
- gasto, alcance, frecuencia;
- conversaciones: iniciadas, respondidas y **de ida y vuelta** (`messaging_user_depth_2_message_send`);
- reparto del gasto entre anuncios de cada conjunto;
- estado real (`effective_status`) y presupuesto diario vigente;
- para cumpleaños: qué meses tiene la capa y qué día es hoy (si es día 20 o después y la capa es del mes en curso,
  toca rotar).

## Paso 2 · Lo que dice el dueño de la sala
Una sola pregunta, con opciones: «¿Cómo estuvo la semana en el local?» (más gente que la anterior · igual · menos ·
«no sé»). Y si hay palabras clave en WhatsApp: «¿cuántos mensajes con la palabra X te llegaron?». Si no sabe, se sigue.

## Paso 3 · Leer contra la vara
Por cada campaña: su costo por conversación de ida y vuelta, su semáforo de la bitácora y su % del techo. Busca sólo
estas señales:
- **Capa de cumpleaños vencida** (`04`).
- **Un anuncio con >80%** del gasto de su conjunto, o anuncios con <5% que alguien quiere «juzgar» (`05`).
- **Frecuencia subiendo y costo por persona nueva duplicado** contra su primera semana: el anuncio se agotó.
- **Gasto con la cocina cerrada** (`03`).
- **Caída en el segundo mensaje del cliente**: es la atención del WhatsApp, no la pauta (`03`).
- Algo **cambió sin estar en la bitácora**: mira el registro de actividad.

## Paso 4 · El entregable
En el chat, máximo 12 líneas, y guardado en `mi-negocio/informes/AAAA-MM-DD.md`:

```
📅 Leído el <fecha> a las <hora>. Semana <del…al…>.
💸 Gastaste <$> (la semana anterior <$>).
💬 <n> conversaciones de ida y vuelta a <$> cada una = <x>% de tu techo.
🟢/🟡/🔴 por campaña: <nombre> <$ por conversación> → <sube / se queda / baja según su vara>
👉 Esta semana haría UNA cosa: <el cambio>, porque <el número>. Cuesta <$ más o menos al día>.
🧊 Lo demás se queda quieto hasta <fecha de lectura>.
```

Si lo que toca es no hacer nada, se dice así: «Esta semana no tocaría nada: <campaña> se lee el <fecha>».

## Reglas
- **Una recomendación por semana**, nunca una lista. Si la bitácora dice que algo se lee después, no se propone
  tocarlo.
- Con pocos datos (menos de ~20 conversaciones por campaña) se dice «todavía no hay con qué decidir».
- Se compara contra semanas del mismo tipo (no una semana de festival contra una normal, ni antes y después de una
  mudanza).
- Para hacer el cambio, el dueño dice «hazlo» → `hacer-un-cambio`.
