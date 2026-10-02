<!--
PROPOSAL_TEMPLATE.md — v1.1 (homologación de variables, 22/09/2026)

Plantilla del brief LIGERO de una oportunidad. Para usarla: copia este fichero
a outputs/<repo>/src/PROPOSAL_<id>.md, rellena los campos y pega la oferta
en "Job Description" tal cual — sin reformatear, sin resumir.

Esto NO es el mismo formato que el PROPOSAL_<id>.md narrativo (MOTIVATION /
WHAT I BRING / PROJECT / CLOSING) que a veces llega ya redactado desde el
sistema TOS y que procesa `proposal_to_scheme.py`. Son dos rutas de entrada
distintas al mismo `SCHEME.md` — usa esta cuando partes de una oferta en
crudo (un job description, un mensaje de un reclutador, un enlace pegado como
texto) y no de una narrativa ya escrita:

  Ruta A (narrativa ya escrita, formato antiguo):
    PROPOSAL_<id>.md (narrativo) -> proposal_to_scheme.py -> SCHEME.md borrador

  Ruta B (brief en crudo, este fichero):
    PROPOSAL_<id>.md (este brief) + FACT_SHEETS.md -> Claude (ver CLAUDE.md
    en la raíz del repo) redacta SCHEME.md directamente -> tu revisión

En la Ruta B no hay script determinista intermedio: es Claude quien lee este
brief y FACT_SHEETS.md, selecciona qué logros/certificaciones/cifras de
FACT_SHEETS.md son relevantes para ESTA oferta concreta (nunca vuelca el
fichero entero) y redacta el `SCHEME.md` siguiendo MICROSITE_TEMPLATE.<idioma>.md
y las reglas de MICROSITE_SCHEME.md. Repite igual que la Ruta A: `SCHEME.md`
sigue siendo el único fichero que se revisa y aprueba a mano antes de construir
el sitio (build.py) — este brief no se toca después de escrito.

v1.1 (22/09/2026) — homologación de nombres de campo con SCHEME.md, acordada
tras detectar que v1.0 usaba un vocabulario propio (inglés, "Title Case") que
no coincidía ni con SCHEME.md ni consigo mismo (mezclaba "Fecha" en español
con el resto en inglés). Cambios:
  - Role Position -> rol_u_oportunidad · Customer -> cliente_u_organizacion ·
    Language -> idioma · Type -> tipo · Repo -> repo · Fecha -> fecha.
    Mismos nombres que en SCHEME.md — el campo NO se traduce según el idioma
    del contenido, igual que ya regía en SCHEME.md.
  - tipo pasa a usar el mismo enum que SCHEME.md (candidatura-empleo |
    oferta-freelance | candidatura-formacion) en vez de uno propio
    (job-application | freelance-project | training-application) — elimina
    la tabla de traducción de valores que antes hacía falta para decidir
    email_contacto (ver CLAUDE.md paso 6 y MICROSITE_SCHEME.md).
  - Job Description (campo de una línea) -> resumen_oferta, para no chocar
    de nombre con la sección "## Job Description" de más abajo (el texto
    íntegro de la oferta), que mantiene su encabezado tal cual.
  - Nuevo campo: cv_pdf — declara desde el brief si habrá CV adjunto y con
    qué nombre de fichero, en vez de descubrirlo a mano después (ver abajo).
  - repo se mantiene como campo propio, distinto de slug (SCHEME.md): repo es
    el nombre de carpeta tal cual lo escribes; slug es su forma normalizada
    en minúsculas y con guiones — se deriva de repo, no se declara aparte.
-->
---
rol_u_oportunidad: "Technical Project Manager"
cliente_u_organizacion: "ACCIONA"
idioma: es                      # en | es — idioma en el que se redactará SCHEME.md
tipo: oferta-freelance           # candidatura-empleo | oferta-freelance | candidatura-formacion — mismo vocabulario que SCHEME.md
repo: "Acciona-PM"              # nombre de la carpeta en outputs/<repo>/ y, más adelante, del repo
                                 # de GitHub publicado en proposals.josegalindo.net/<repo>/; el
                                 # slug de SCHEME.md se deriva de este en minúsculas y con guiones
fecha: "2026-10-02"
cv_pdf: "CV_Jose Galindo.pdf"                   # nombre del fichero que vas a añadir a assets/, tal cual lo tengas
                                 # hoy (ej. "Jose Galindo_SPM.pdf") — o vacío si no hay CV. Al
                                 # redactar SCHEME.md se renombra a la convención cv-<slug>.pdf y
                                 # se conecta el botón "Download CV" desde el primer borrador
resumen_oferta: "Technical PM freelance en ACCIONA: gestión de la demanda de negocio y enlace con equipos técnicos (cloud, datos, IA); 160h/mes, 12 meses renovables, híbrido en Madrid"            # resumen de una línea; el texto completo va en la sección de abajo
---

## Job Description

Technical Project Manager

Dedicación:

160h / mes

Duración:

12 meses

Modalidad:

Híbrido

Ubicación:

N/A

Fecha de inicio:

29/09/2026

Idiomas:

Español
Inglés
Acerca de la compañía

ACCIONA es uno de los mayores grupos empresariales de España y un referente mundial en infraestructuras sostenibles y energía renovable. Tiene más de 68.500 profesionales en más de 60 países y en 2025 facturó más de 20.000 millones de euros, con un beneficio neto de 803 millones.

Diseña, construye y opera infraestructuras de gran escala: autopistas, ferrocarriles, hospitales, puertos y plantas desaladoras que abastecen de agua a millones de personas. Su cartera de infraestructuras supera los 120.000 millones de euros. A través de ACCIONA Energía gestiona 14,6 GW de capacidad renovable instalada en todo el mundo, y es accionista de referencia de Nordex, uno de los grandes fabricantes mundiales de aerogeneradores. Casi el 90% de sus ventas corresponde a actividades sostenibles según la taxonomía europea.

La posición se incorpora a un equipo de 7 personas situado entre tecnología y negocio. Este equipo es el punto de conexión entre las áreas de negocio del grupo y los equipos especializados de DevOps, desarrollo, datos, despliegues e IA.

Shakers impulsa
tu carrera profesional

Forma parte de una comunidad exclusiva y accede a grandes oportunidades

Compensación superior. Gana hasta un 30% más que en un contrato tradicional.

Proyectos Full-time. El 85% de nuestros proyectos son a tiempo completo

Aumenta tus ingresos. Accede a mini-proyectos exclusivos para sumar más sin perder flexibilidad

Requisitos

Descripción general del proyecto
Buscamos un Project Manager técnico que se encargue de la gestión de la demanda y haga de enlace entre negocio y tecnología. La persona recibirá necesidades de negocio muy variadas, desde incidencias operativas hasta nuevos proyectos de IA. Su trabajo será entenderlas, darles forma y dirigirlas al equipo adecuado, y en algunos casos montar el proyecto desde cero y llevarlo hasta su puesta en marcha.

Es un rol con vocación de continuidad, dentro de un equipo cercano y con apoyo directo de la responsable del área. El stack tecnológico se está replanteando y hoy combina GCP y Azure, con AWS en evaluación.

Modalidad: híbrido, con 2-3 días presenciales en oficina, sobre todo en la fase inicial. Hay un comité de equipo semanal los miércoles.

Ubicación: Madrid

Duración: larga duración, con renovación anual

Fecha de arranque: inmediata

Urgencia: alta

Idiomas: español. Inglés profesional.

Funciones
Gestionar la demanda que llega de las áreas de negocio: analizar cada necesidad, concretarla y dirigirla a la solución y al equipo más adecuados.

Coordinarse con los equipos técnicos (DevOps, desarrollo, datos, despliegues, IA) para pedir a cada uno lo que corresponda.

Mediar entre áreas de negocio y alinear necesidades comunes, por ejemplo junto al equipo de gobierno del dato.

Definir y arrancar nuevos proyectos desde cero.

En proyectos completos, coordinar a los proveedores, la planificación, los plazos y la metodología.

Impulsar la gestión del cambio en las áreas de negocio, incluida la adopción de nuevas tecnologías como la IA.

Requisitos imprescindibles del perfil
Experiencia como Project Manager con background técnico en IT y capacidad para comunicarse con perfiles de negocio.

Experiencia en gestión de stakeholders y gestión de la demanda en organizaciones grandes y complejas.

Capacidad de aprendizaje y de abstracción, y comodidad trabajando en entornos con incertidumbre.

Empatía, proactividad, diplomacia y mano izquierda.

Requisitos valorables
Certificación PMP

Conocimiento de Jira y ServiceNow

Nivel de inglés profesional

Experiencia en gestión del cambio

Experiencia coordinando proveedores externos

Conocimiento de ACCIONA o del sector de la construcción

Puntos atractivos del proyecto/cliente
Proyecto estable y de larga duración, con presupuesto renovado cada año.

Trabajo directo con el cliente final, sin intermediarios.

Proyectos muy variados, incluidas iniciativas de IA, en pleno replanteamiento del stack cloud.

Equipo pequeño y cercano, con acompañamiento directo de la responsable.

Exposición directa a la capa de negocio de un grupo internacional.

Flexibilidad en la modalidad de trabajo.

Habilidades

JIRA
ServiceNow
PMP (Project Management Professional)
Planificación de proyectos
Gestión del cambio
Proactividad
Gestión de stakeholders

Información adicional
Acciona, que busca un PM tech freelance para recoger la demanda de las áreas, darle forma y llevarla al equipo adecuado (cloud, datos, IA...) 🛠️ 12 meses + renovación, full time, híbrido en Madrid e incorporación inmediata.
