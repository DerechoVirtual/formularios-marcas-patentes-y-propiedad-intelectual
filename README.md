# Marcas, patentes y propiedad intelectual

> Plugin de Claude Code `formularios-marcas-patentes-y-propiedad-intelectual` · **53 formularios** · Mercantil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para proteger y explotar intangibles: licencias y cesiones de marca, patente, modelo de utilidad y diseño, know-how y secretos empresariales, contratos de edición, producción audiovisual y musical, cesión de derechos de autor y obras por encargo, y acciones por infracción.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 53 está al final):

- **Contratos, pactos y cláusulas** (47). Por ejemplo: Contrato de edición de una obra entre autor y editor; Contrato marco de gestión integral de la producción musical (360 grados); Contrato de cesión de un secreto empresarial.
- **Estatutos, actas, certificaciones y escrituras** (3). Por ejemplo: Escritura de constitución de hipoteca sobre una marca; Acta de creación de una comunidad de titulares de una patente; Acta de creación de una comunidad de titulares de una marca.
- **Escritos de trámite y otros** (3). Por ejemplo: Distribución de obras musicales en plataformas digitales (contrato); Transferencia de tecnología, Know-How o Secretos empresariales (contrato); Reglamento interno de la comunidad de bienes titular de una marca.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Contrato de licencia de marca en exclusiva»
   - «Contrato de cesión de derechos de autor de una obra por encargo»
   - «Acuerdo de licencia de know-how»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-marcas-patentes-y-propiedad-intelectual:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-edicion-obra-entre-autor-editor-mer-0697`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 2.923 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-marcas-patentes-y-propiedad-intelectual@formularios-marcas-patentes-y-propiedad-intelectual`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-marcas-patentes-y-propiedad-intelectual
/plugin install formularios-marcas-patentes-y-propiedad-intelectual@formularios-marcas-patentes-y-propiedad-intelectual
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-marcas-patentes-y-propiedad-intelectual`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-marcas-patentes-y-propiedad-intelectual/releases/latest/download/formularios-marcas-patentes-y-propiedad-intelectual.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (53)

| Código | Formulario | Skill |
|---|---|---|
| MER-0697 | Contrato de edición de una obra entre autor y editor | `contrato-edicion-obra-entre-autor-editor-mer-0697` |
| MER-0698 | Escritura de constitución de hipoteca sobre una marca | `escritura-constitucion-hipoteca-sobre-marca-mer-0698` |
| MER-0699 | Contrato marco de gestión integral de la producción musical (360 grados) | `contrato-marco-gestion-integral-produccion-musical-360-mer-0699` |
| MER-0700 | Distribución de obras musicales en plataformas digitales (contrato) | `distribucion-obras-musicales-plataformas-digitales-mer-0700` |
| MER-0701 | Contrato de cesión de un secreto empresarial | `contrato-cesion-secreto-empresarial-mer-0701` |
| MER-0702 | Contrato de licencia de un secreto empresarial | `contrato-licencia-secreto-empresarial-mer-0702` |
| MER-0703 | Transferencia de tecnología, Know-How o Secretos empresariales (contrato) | `transferencia-tecnologia-know-how-secretos-mer-0703` |
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
| MER-0721 | Acta de creación de una comunidad de titulares de una patente | `acta-creacion-comunidad-titulares-patente-mer-0721` |
| MER-0722 | Contrato por el que el licenciatario de una marca concede una sublicencia | `contrato-licenciatario-marca-concede-sublicencia-mer-0722` |
| MER-0723 | Reglamento interno de la comunidad de bienes titular de una marca | `reglamento-interno-comunidad-bienes-titular-marca-mer-0723` |
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
| MER-0734 | Acta de creación de una comunidad de titulares de una marca | `acta-creacion-comunidad-titulares-marca-mer-0734` |
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

## Privacidad

Ver `PRIVACY.md`.
