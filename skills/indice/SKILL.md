---
name: indice
description: "Índice de los 53 formularios de Marcas, patentes y propiedad intelectual. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Marcas, patentes y propiedad intelectual: índice de formularios

> Plugin `formularios-marcas-patentes-y-propiedad-intelectual` · 53 formularios · normativa revisada el 25-11-2026.

## Qué es

Para proteger y explotar intangibles: licencias y cesiones de marca, patente, modelo de utilidad y diseño, know-how y secretos empresariales, contratos de edición, producción audiovisual y musical, cesión de derechos de autor y obras por encargo, y acciones por infracción.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Contrato de licencia de marca en exclusiva»
- «Contrato de cesión de derechos de autor de una obra por encargo»
- «Acuerdo de licencia de know-how»

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-marcas-patentes-y-propiedad-intelectual:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Contratos, pactos y cláusulas (47)

| Código | Formulario | Skill |
|---|---|---|
| MER-0697 | Contrato de edición de una obra entre autor y editor | `contrato-edicion-obra-entre-autor-editor-mer-0697` |
| MER-0699 | Contrato marco de gestión integral de la producción musical (360 grados) | `contrato-marco-gestion-integral-produccion-musical-360-mer-0699` |
| MER-0701 | Contrato de cesión de un secreto empresarial | `contrato-cesion-secreto-empresarial-mer-0701` |
| MER-0702 | Contrato de licencia de un secreto empresarial | `contrato-licencia-secreto-empresarial-mer-0702` |
| MER-0704 | Cesión de derechos de imagen (contrato) | `cesion-derechos-imagen-contrato-mer-0704` |
| MER-0705 | Contrato de traducción de una obra con cesión al editor | `contrato-traduccion-obra-cesion-editor-mer-0705` |
| MER-0706 | Contrato de cesión de patente con cláusula sobre inteligencia artificial | `contrato-cesion-patente-clausula-sobre-inteligencia-mer-0706` |
| MER-0707 | Contrato de servicios de auditoría técnica sobre la validez de una patente | `contrato-servicios-auditoria-tecnica-sobre-validez-mer-0707` |
| MER-0708 | Contrato de licencia de marca de la Unión Europea para España | `contrato-licencia-marca-union-europea-espana-mer-0708` |
| MER-0709 | Licencia de patente (contrato) | `licencia-patente-contrato-mer-0709` |
| MER-0710 | Contrato de comunidad sobre una marca | `contrato-comunidad-sobre-marca-mer-0710` |
| MER-0711 | Contrato de comunidad sobre una patente | `contrato-comunidad-sobre-patente-mer-0711` |
| MER-0712 | Contrato de interpretación o ejecución musical | `contrato-interpretacion-ejecucion-musical-mer-0712` |
| MER-0713 | Contrato de edición de una obra musical | `contrato-edicion-obra-musical-mer-0713` |
| MER-0714 | Contrato de edición de una obra literaria | `contrato-edicion-obra-literaria-mer-0714` |
| MER-0715 | Contrato de representación de una obra teatral | `contrato-representacion-obra-teatral-mer-0715` |
| MER-0716 | Contrato de cesión o licencia exclusiva de derechos de autor | `contrato-cesion-licencia-exclusiva-derechos-autor-mer-0716` |
| MER-0717 | Contrato de venta de una marca registrada | `contrato-venta-marca-registrada-mer-0717` |
| MER-0718 | Contrato de colaboración en proyectos de investigación y desarrollo (I+D) | `contrato-colaboracion-proyectos-investigacion-mer-0718` |
| MER-0719 | Contrato de cesión o licencia no exclusiva de derechos de autor | `contrato-cesion-licencia-no-exclusiva-derechos-autor-mer-0719` |
| MER-0720 | Contrato de autorización no exclusiva de obra artística por entidad de gestión | `contrato-autorizacion-no-exclusiva-obra-artistica-mer-0720` |
| MER-0722 | Contrato por el que el licenciatario de una marca concede una sublicencia | `contrato-licenciatario-marca-concede-sublicencia-mer-0722` |
| MER-0724 | Contrato de licencia de uso de conocimientos técnicos (know how) | `contrato-licencia-uso-conocimientos-tecnicos-know-how-mer-0724` |
| MER-0725 | Contrato de transmisión definitiva de conocimientos técnicos (know how) | `contrato-transmision-definitiva-conocimientos-tecnicos-mer-0725` |
| MER-0726 | Contrato entre autor o artista y productor de fonogramas | `contrato-entre-autor-artista-productor-fonogramas-mer-0726` |
| MER-0727 | Contrato de encargo y cesión de una obra musical | `contrato-encargo-cesion-obra-musical-mer-0727` |
| MER-0728 | Contrato de encargo de un guion al guionista | `contrato-encargo-guion-guionista-mer-0728` |
| MER-0729 | Contrato de cesión temporal de una obra de arte para su exposición al público | `contrato-cesion-temporal-obra-arte-exposicion-publico-mer-0729` |
| MER-0730 | Contrato de dirección y realización de una obra audiovisual | `contrato-direccion-realizacion-obra-audiovisual-mer-0730` |
| MER-0731 | Contrato de transmisión de una marca con fines de fiducia | `contrato-transmision-marca-fines-fiducia-mer-0731` |
| MER-0732 | Contrato de cesión de una marca por tiempo limitado | `contrato-cesion-marca-tiempo-limitado-mer-0732` |
| MER-0733 | Contrato de cesión de derechos de autor para su publicación en una revista o periódico | `contrato-cesion-derechos-autor-publicacion-revista-mer-0733` |
| MER-0735 | Contrato de cesión de los derechos de explotación de un guion | `contrato-cesion-derechos-explotacion-guion-mer-0735` |
| MER-0736 | Contrato de cesión de los derechos de explotación de una tesis doctoral | `contrato-cesion-derechos-explotacion-tesis-doctoral-mer-0736` |
| MER-0737 | Contrato de exposición pública de una obra de arte con fines de venta | `contrato-exposicion-publica-obra-arte-fines-venta-mer-0737` |
| MER-0738 | Contrato por el que se encarga la creación de una obra a su autor | `contrato-encarga-creacion-obra-autor-mer-0738` |
| MER-0739 | Contrato de encargo de una obra multimedia | `contrato-encargo-obra-multimedia-mer-0739` |
| MER-0740 | Contrato de producción de una obra por encargo | `contrato-produccion-obra-encargo-mer-0740` |
| MER-0741 | Contrato de edición de una obra colectiva | `contrato-edicion-obra-colectiva-mer-0741` |
| MER-0742 | Contrato de distribución de obras de arte | `contrato-distribucion-obras-arte-mer-0742` |
| MER-0743 | Contrato de producción de un documental | `contrato-produccion-documental-mer-0743` |
| MER-0744 | Contrato de coproducción de una serie de televisión | `contrato-coproduccion-serie-television-mer-0744` |
| MER-0745 | Contrato de cesión de derechos de explotación de una obra por su autor | `contrato-cesion-derechos-explotacion-obra-autor-mer-0745` |
| MER-0746 | Contrato de licencia de marca y de know how con canon mensual y royalties anuales | `contrato-licencia-marca-know-how-canon-mensual-mer-0746` |
| MER-0747 | Contrato de cesión de un modelo de utilidad | `contrato-cesion-modelo-utilidad-mer-0747` |
| MER-0748 | Contrato de licencia exclusiva de un modelo de utilidad | `contrato-licencia-exclusiva-modelo-utilidad-mer-0748` |
| MER-0749 | Contrato de cesión de marca en escritura notarial | `contrato-cesion-marca-escritura-notarial-mer-0749` |

### Estatutos, actas, certificaciones y escrituras (3)

| Código | Formulario | Skill |
|---|---|---|
| MER-0698 | Escritura de constitución de hipoteca sobre una marca | `escritura-constitucion-hipoteca-sobre-marca-mer-0698` |
| MER-0721 | Acta de creación de una comunidad de titulares de una patente | `acta-creacion-comunidad-titulares-patente-mer-0721` |
| MER-0734 | Acta de creación de una comunidad de titulares de una marca | `acta-creacion-comunidad-titulares-marca-mer-0734` |

### Escritos de trámite y otros (3)

| Código | Formulario | Skill |
|---|---|---|
| MER-0700 | Distribución de obras musicales en plataformas digitales (contrato) | `distribucion-obras-musicales-plataformas-digitales-mer-0700` |
| MER-0703 | Transferencia de tecnología, Know-How o Secretos empresariales (contrato) | `transferencia-tecnologia-know-how-secretos-mer-0703` |
| MER-0723 | Reglamento interno de la comunidad de bienes titular de una marca | `reglamento-interno-comunidad-bienes-titular-marca-mer-0723` |
