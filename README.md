# Pauta con IA

**Que Claude maneje la pauta de Meta (Facebook e Instagram) de tu restaurante, con lo que aprendí pagando la mía.**

Para dueños de restaurantes, cafeterías, taquerías, heladerías y cualquier negocio de comida que paga anuncios (o
quiere empezar) y no sabe si le están trayendo gente. Claude lee tu cuenta, te dice qué pasó en palabras simples y te
propone **un** cambio por semana. **Nada se activa, se gasta ni se borra sin tu OK.**

Hecho por **Mao Pinzón**, ingeniero de software con restaurante · [maopinzon.com/pauta-ia](https://maopinzon.com/pauta-ia)

---

## Cómo se usa, en 5 pasos

**1 · La carpeta.** Instala la app de Claude en tu computadora y entra a la pestaña **Code**. Pega el
[prompt de instalación](PROMPT-DE-INSTALACION.md): Claude baja esta carpeta y te explica todo.

**2 · Conecta tu cuenta.** Con el **conector oficial de Meta** (`https://mcp.facebook.com/ads`): entras tú con tu
Facebook y eliges qué cuenta de anuncios compartes. Si no se puede, Claude trabaja en el **navegador**.

**3 · Tu techo.** Le mandas una foto del reporte de ventas de tu caja y Claude calcula **cuánto puedes pagar por cada
cliente nuevo**. Con ese número se juzga todo, no con lo que diga Meta.

**4 · La revisión.** Dile **«revisa mi cuenta»**: zona, botones, objetivos, horario, quién cambió qué. Y cada lunes,
**«¿cómo van mis anuncios?»**: lo que pasó, lo que costó cada conversación y **una** cosa para esta semana.

**5 · Campañas y cambios, con tu OK.** **«Arma una campaña de cumpleaños»**: Claude te propone todo, lo crea **en
pausa**, te enseña la vista previa y la activa sólo cuando dices «actívala». Cada cambio queda en tu bitácora.

## Qué le puedes pedir

| Dile… | Skill | Qué hace |
|---|---|---|
| «conecta mi cuenta» | `conectar-meta` | Te guía para conectar Meta y llena tu ficha |
| «¿cuánto puedo pagar por cliente?», una foto de tu caja | `mi-techo` | Tu techo por mesa nueva y cuántas mesas tiene que traer la pauta |
| «revisa mi cuenta», «audita lo que dejó la agencia» | `auditar-mi-cuenta` | Lo que está bien, lo que está mal y qué cambiar primero |
| «¿cómo van mis anuncios?» | `revisar-mi-pauta` | La lectura del lunes, con una sola recomendación |
| «arma una campaña», «pautemos los cumpleaños» | `armar-campana` | La propuesta, la creación en pausa y la vista previa |
| «sube el presupuesto», «pausa…», «rota los cumpleaños» | `hacer-un-cambio` | Un cambio, verificado y anotado |
| «¿qué pautan los demás?» | `que-pautan-otros` | Lo que anuncian otros negocios de comida |
| «hazlo en el navegador» | `pauta-en-el-navegador` | Lo mismo, en el Administrador de anuncios |

## Lo que aprendí, para que no lo pagues tú

`conocimiento/` tiene lo que aprendió mi restaurante en el Centro de Mérida, con tres locales y una agencia de por
medio, cada cosa con su nivel de evidencia (🟢 medido · 🟡 observado · 🔴 hipótesis). Lo esencial:

- **El juez es la sala, no Meta.** «¿Dónde nos viste?» al cobrar y una palabra clave por anuncio en WhatsApp.
- **WhatsApp, y la conversación de ida y vuelta.** Costó de 11 a 30 pesos cada una.
- **Cumpleaños y grupos** son el mejor anuncio, si cambias el mes cerca del día 20.
- **El plato para compartir** trae mesas; el individual, parejas.
- **Meta mete todo el dinero en un anuncio.** Para comparar, un conjunto por pieza.
- **No cambies todo cada semana.** Escribe la vara antes y congela cuatro semanas.

## Qué necesitas

- Una **Mac** o una **PC con Windows**, y la app de **Claude** con un plan de pago (Pro o Max), que incluye Claude Code.
- Ser **administrador** (o tener permiso para anunciar) de la cuenta de anuncios de tu negocio en Meta.
- Una foto del reporte de ventas de tu caja, para calcular tu techo.

## Lo que NO hace

- **No gasta sin tu OK.** Nada se activa, se sube ni se crea sin que digas que sí, cambio por cambio.
- **No borra.** Pausa. Borrar en Meta no se deshace.
- **No escribe tus contraseñas ni tu tarjeta**, ni toca pagos, límites de gasto o permisos de tu Business Manager.
- **No inventa tu comida ni tu local con IA** para un anuncio: usa tus videos y fotos reales.
- **No promete resultados.** Te dice qué pasó, con su fecha y su nivel de evidencia, y qué haría yo.

## Tus datos

Lo de tu negocio (ficha, bitácora, informes) vive en `mi-negocio/`, en tu computadora, y no se sube a ningún lado.
El acceso a tu cuenta de Meta lo das tú y lo quitas cuando quieras (Facebook → Configuración → Integraciones de
empresas).

---

Licencia MIT. Úsalo y cámbialo como quieras, citando de dónde salió.
