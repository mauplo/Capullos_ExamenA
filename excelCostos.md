# LIGA EXCEL

https://docs.google.com/spreadsheets/d/1rDiiTGEdZiyK6rk4RqW9uh5g03G_49IIjP2iGCFmP-o/edit?usp=sharing
---

# Justificaciones de distribución de esfuerzo por rol (comparativas)

> En cada funcionalidad se explica **por qué** ciertos roles concentran **más días/porcentaje** que otros, sin detallar tareas específicas.

---

## Login
- **Sr. FullStack (↑)**: Mayor peso por la **integración con la API externa (ITAM)**, manejo de tokens/sesión y compatibilidad entre ambientes; el front es ligero.
- **Desarrollo Back (↑)**: Incrementa por **endpoints/seguridad/timeouts**; depende de terceros y exige robustez.
- **PM (→)**: Participación **moderada** por coordinación multi-cuenta/entorno y validación de acceso.
- **Diseño y UX (↓)**: **Bajo** porque la UI es minimalista y los flujos son estándar.

---

## Ver Menú
- **Diseño (↑)**: Se prioriza **legibilidad y jerarquía visual**; el usuario consulta el menú con frecuencia.
- **UX Intern / Desarrollo Front (↗)**: **Relevante** por filtros, estados vacíos y rendimiento percibido; impacto directo en uso diario.
- **Sr. FullStack (→)**: **Moderado** para asegurar orquestación y manejo de errores de red.
- **Desarrollo Back (↓)**: **Menor**; son consultas simples sin lógica compleja.
- **IA (Sr./Intern) (↓)**: **Ligero**; se deja **preparado** para ranking/relevancia futura, sin ser el foco inicial.

---

## Editar Menú
- **Sr. FullStack / Desarrollo Front (↑)**: Suben por **formularios de edición**, validaciones y consistencia con inventario; riesgo de errores del usuario.
- **Desarrollo Back (↗)**: **Importante** para reglas/consistencia de datos entre productos e inventario.
- **PM (→)**: **Moderado** por coordinación de flujos y permisos.
- **Diseño (→)**: **Medio** para claridad de formularios; **UX no se prioriza** al no ser uso masivo.

---

## Hacer Pedido
- **Diseño y UX Intern (↑)**: Alto porque la **experiencia de compra** impacta conversión/rapidez; uso constante.
- **PM (↗)**: **Elevado** por coordinación end-to-end y casos límite (totales, disponibilidad, confirmación).
- **Desarrollo Back / Front (→)**: **Equilibrado**; lógica de totales/estado + feedback inmediato.
- **Sr. FullStack (→)**: **Moderado** para consistencia y reglas de negocio; menos que en login/pagos.

---

## Endpoints Pagos
- **Sr. FullStack (↑) / Desarrollo Back (↑)**: **Protagonistas** por seguridad, webhooks, idempotencia y conciliación.
- **PM (→)**: **Moderado** por coordinación con la pasarela/sandbox.
- **Diseño/UX/Front (↓)**: **Mínimos**; el foco es backend y cumplimiento.

---

## Recomendación de Producto (IA)
- **Sr. IA Engineer (↑) / IA Intern (↗)**: **Altos** por preparación de datos, selección de enfoque y experimentación; componente analítico central.
- **PM (→)**: **Moderado** para metas (CTR/attach) y privacidad.
- **Desarrollo Front (→)**: **Medio** para integrar recomendaciones sin fricción.
- **Diseño (→) / UX Intern (→)**: **Medios** para presentación clara y **explicabilidad ligera** (“por compras previas”).

---

## Predicción de Inventario (IA)
- **Sr. IA Engineer (↑↑)**: **Mayor carga** por modelado de series, validación y manejo de drift; es el núcleo técnico.
- **IA Intern (↗)**: **Significativo** en limpieza/backtesting.
- **Desarrollo Back (→)**: **Medio** para jobs/APIs y exposición de resultados.
- **Diseño (→)**: **Medio** para visualizaciones/alertas comprensibles.
- **PM (→)**: **Moderado** para alinear horizontes y SLAs.

---

## Update Inventario
- **Sr. FullStack (↑)**: **Alto** por foco en **rendimiento y fluidez** (uso en piso/operación); experiencia rápida y robusta.
- **Desarrollo Front / UX Intern (↗)**: **Relevantes** por flujos de edición masiva y errores prevenibles.
- **Diseño (→)**: **Medio** para formularios compactos y estados de confirmación.

---

## Completar Ticket
- **Sr. FullStack (↑)**: **Alto** por sincronización final con inventario, eventos y idempotencia del cierre.
- **PM (↗)**: **Elevado** para reglas de cierre, tiempos de ciclo y notificaciones.
- **UX Intern / Desarrollo Front (→)**: **Medios** para rapidez y claridad de estados terminales.
- **Diseño (↓)**: **Bajo**; prima la funcionalidad/eficacia sobre la estética.

---

### Criterios transversales que explican las diferencias
- **Frecuencia de uso del usuario final** (menú, pedido, update): ↑ Diseño/UX/Front.
- **Dependencias externas y riesgo técnico** (login/pagos): ↑ Sr. FullStack/Back.
- **Carga analítica/modelado** (IA): ↑ Sr. IA Engineer/IA Intern.
- **Orquestación y alineación inter-equipo**: ↑ PM.
- **Impacto operativo inmediato** (tiempos de atención/errores): ↑ FullStack/Front/UX.
