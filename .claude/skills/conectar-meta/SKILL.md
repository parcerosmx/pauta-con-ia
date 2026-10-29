---
name: conectar-meta
description: Conecta a Claude con la cuenta de anuncios de Meta (Facebook e Instagram) del negocio, por el conector oficial de Meta o, si no se puede, por el navegador. Elige la cuenta, la anota en la ficha y deja todo en modo de sólo lectura. Úsalo en el primer uso o cuando digan «conecta mi cuenta», «no ves mis anuncios», «conecta Meta», «mi primer uso».
---

# Conectar Meta

Primer uso. Al terminar, Claude ve la cuenta de anuncios del negocio y la ficha dice cuál es. **Aquí no se cambia nada
en la cuenta.**

## Paso 0 · La ficha
Si no existe `mi-negocio/ficha.md`, créala copiando `plantillas/ficha.md` (y `plantillas/bitacora.md` →
`mi-negocio/bitacora.md`, más la carpeta `mi-negocio/informes/`).

## Paso 1 · ¿Ya está el conector?
Busca entre tus herramientas las del conector de Meta (se llaman `ads_…`, por ejemplo `ads_get_ad_accounts`).

- **Si están:** salta al paso 3.
- **Si no están:** el proyecto ya trae `.mcp.json` con el conector oficial (`https://mcp.facebook.com/ads`). Explícale
  al dueño, en 4 líneas, qué es y qué no:
  - Es el conector **oficial de Meta**: Claude lee tus campañas y, sólo si tú lo apruebas, hace cambios.
  - Entras **tú** con tu Facebook; Claude nunca ve tu contraseña.
  - Tú eliges qué cuenta de anuncios compartes. Puedes quitarle el acceso cuando quieras.
  - Es gratis mientras Meta lo tenga en beta.

## Paso 2 · Conectarlo (lo hace el dueño, Claude guía)
Dale **una** de estas dos rutas, la primera por defecto:

**A. Desde la app de Claude (la más fácil, sirve también en el chat):**
1. En la app de Claude: **Personalizar → Conectores → + → Agregar conector personalizado**.
2. Nombre: `Meta Ads`. URL: `https://mcp.facebook.com/ads`. **Agregar**.
3. **Conectar** → se abre Facebook → entra con la cuenta que administra los anuncios → elige el negocio y **sólo la
   cuenta de anuncios de tu negocio** → acepta.
4. Vuelve aquí y dime «listo». (Si en Code no aparece, cierra y abre esta sesión.)

**B. Desde este proyecto:** al abrir la carpeta, la app pregunta si permite el servidor `meta-ads` del proyecto:
**Permitir**. Cuando avise que Meta necesita autenticarse, toca **Conectar** y sigue los mismos pasos de Facebook.

Errores comunes, en una línea cada uno:
- «La app no está disponible» en Facebook → entra con el Facebook que **sí** tiene un rol en el negocio.
- No ves tu cuenta → no la marcaste: desconecta, vuelve a conectar y márcala.
- El plan gratis de Claude permite un solo conector personalizado.

Si después de dos intentos no se puede, ofrece el navegador (`pauta-en-el-navegador`) y anótalo en la ficha.

## Paso 3 · Elegir la cuenta
Lista las cuentas de anuncios a las que hay acceso (nombre, ID, moneda, estado). Si hay varias, pregunta con opciones
**cuál es la del negocio**. Las demás **no se consultan nunca**, aunque aparezcan.

Lee de esa cuenta, sin cambiar nada: la página de Facebook y el Instagram ligados, las campañas activas (nombre,
objetivo, gasto de los últimos 7 días) y el número de WhatsApp al que mandan los anuncios, si se ve.

## Paso 4 · Anotar y confirmar
Llena la sección «La cuenta» de la ficha y enséñasela al dueño en 6 líneas para que confirme. Pregunta, con opciones,
sólo lo que no se pudo leer: dirección del local de hoy, horario de cocina, y si ha pasado algo que parta los números
(mudanza, cierre, cambio de carta) con su fecha.

Cierra con una línea: «Listo, ya veo tu cuenta. No toqué nada.» Si la ficha no tiene el techo, di que lo siguiente que
sirve es calcularlo con una foto del cierre de caja (`mi-techo`).

## Reglas
- Aquí **sólo se lee**. Para las herramientas que escriben, cuando la app pregunte, el dueño elige **«Permitir una
  vez»**.
- Claude nunca escribe contraseñas ni códigos: el inicio de sesión es del dueño.
