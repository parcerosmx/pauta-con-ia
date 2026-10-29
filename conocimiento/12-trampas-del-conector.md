# Trampas del conector y de las métricas de Meta

Para Claude. Salieron de meses de usar el conector oficial (`mcp.facebook.com/ads`) y la API de Meta en una cuenta
real.

## Lectura

- **El gasto se lee por día (`time_increment: 1`) o por campaña**, nunca del total de la cuenta: el total puede traer
  cobros que no son de la pauta (en esa cuenta, un cobro fraudulento ya reportado aparecía fijo en cualquier fecha).
- **Conversación que vale = `messaging_user_depth_2_message_send`** (el cliente escribe un segundo mensaje).
  `messaging_conversation_replied_7d` puede venir vacía en cuentas nuevas: si se lee esa, parece que nadie contesta.
  Siempre se pide la escalera completa (iniciadas → respondidas → segundo mensaje) antes de concluir.
- **Los números caducan.** Un informe de hace dos días no sirve para decidir hoy: se vuelve a leer. Ya pasó que una
  recomendación de pausar se copió de un informe viejo y los datos frescos decían lo contrario.
- **Advantage+ público:** dos conjuntos con nombres distintos («abierto» y «segmentado») pero los dos con la expansión
  de Meta prendida entregan al mismo público. Se revisa `targeting` antes de compararlos.
- **Un dataset (píxel) compartido entre dos sitios** se lee desglosado por dominio, o sus totales mienten.
- **Ventanas cortas:** con menos de ~20 resultados por anuncio no hay ganador. Se dice.

## Escritura

- **Todo lo nuevo se crea con `status: PAUSED`.** Se enseña la vista previa (la herramienta de vista previa del
  anuncio) y se activa sólo con el OK.
- **Después de cada escritura se vuelve a leer** el objeto (`effective_status`, `daily_budget`, `targeting`). Editar un
  presupuesto ya dejó un conjunto en pausa sin pedirlo.
- **Presupuestos en centavos:** la API pide el presupuesto en la unidad mínima de la moneda (100 = 1 peso). Se
  confirma el número en pesos con el dueño antes de mandarlo.
- **Zona por coordenadas:** `custom_locations` con latitud, longitud y radio en km. El centro se verifica en un mapa.
- **Registro de actividad:** `act_<id>/activities`. Con `limit=500` falla; se usa `limit=200` y se pagina.
- **La primera vez que Claude usa una herramienta que escribe**, la app pregunta «Permitir una vez / Permitir
  siempre». Para las que escriben, **«una vez»**.
- Si una herramienta falla o no existe, no se insiste: se le dice al dueño en una línea y se ofrece hacerlo en el
  navegador (`pauta-en-el-navegador`) o que él lo haga en el Administrador de anuncios.
