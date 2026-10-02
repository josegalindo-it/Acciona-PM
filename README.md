# Acciona-PM

Micro-site de propuesta de José Galindo para el rol de Technical Project Manager en ACCIONA (gestión de la demanda de negocio y enlace con los equipos técnicos: DevOps, desarrollo, datos, despliegues e IA), 160 h/mes, 12 meses con renovación anual, modalidad híbrida en Madrid, a través de la plataforma freelance Shakers.

- **Publicado en:** GitHub Pages, rama `main`, raíz del repo (`index.html`).
- **Tipo:** `oferta-freelance`.
- **Idioma:** español (`idioma: es`). El CV adjunto está en inglés.
- **Fuente de contenido:** [`src/SCHEME.md`](src/SCHEME.md) — es el único fichero que se edita a mano. Basado en `MICROSITE_TEMPLATE.es.md` v0.4 (incluye la sección obligatoria "Plan y riesgos").
- **Origen:** brief en crudo [`src/PROPOSAL_Acciona-PM.md`](src/PROPOSAL_Acciona-PM.md) (Ruta B: oferta de Shakers pegada íntegra), a partir del cual `SCHEME.md` se redactó con `FACT_SHEETS.md` como fuente de identidad, cifras y certificaciones.
- **Derivado:** `src/SCHEME.yaml` se genera automáticamente a partir del `.md`. No editar directamente: los cambios se pierden en la siguiente regeneración.
- **Modos de contenido usados:** "Qué aporto" en modo *logros*. "Arquitectura conceptual" en modo *puntos* (entrada de demanda, derivación, proyectos, alineación entre áreas, límite).
- **CV:** [`assets/cv-acciona-pm.pdf`](assets/cv-acciona-pm.pdf), enlazado desde el botón "Descargar CV" del hero (`botones_hero` → `destino: cv`, resuelto contra `cv_pdf`).
- **URL publicada:** declarada en `url_publicada` dentro de `src/SCHEME.md` (`https://proposals.josegalindo.net/Acciona-PM/`).
- **Cliente:** ACCIONA, tal como figura en la oferta.

## ESTADO: borrador sin revisar (`version_documento: "0.2"`)

Este `SCHEME.md` es un borrador, no un entregable listo para enviar. Antes de publicarlo, revisa en `src/SCHEME.md`:

- El H1, la cita del hero y los títulos `###` de sección son sugerencias de posicionamiento (marcadas como DRAFT), no copy aprobado.
- "Plan y riesgos" (primera semana y riesgos) está redactado a partir de la propia oferta, no de `FACT_SHEETS.md`; confirma que refleja cómo quieres abordar el arranque.
- Jira (Mapfre), ServiceNow (Banc Sabadell), gestión del cambio y uso de IA entraron por declaración de Jose, no constan en `FACT_SHEETS.md`.
- `url_publicada` se infirió de la convención `proposals.josegalindo.net/<repo>/`; confírmala al publicar.
- Sube `version_documento` a `"1.0"` cuando lo apruebes.

## Qué subir al repositorio

Sube la carpeta tal cual: `index.html`, `assets/` (con el PDF del CV, sin él el botón de descarga queda roto), `src/` y este `README.md`.

## Cómo regenerar el sitio

1. Editar `src/SCHEME.md` (si cambia el contenido, subir `version_documento` y anotar el motivo en su historial interno).
2. Ejecutar, desde el repo `microsite-toolkit`: `python3 build.py outputs/Acciona-PM` — produce `src/SCHEME.yaml` e `index.html`.
3. Revisar `index.html` localmente antes de hacer commit.
4. `git add`, `git commit`, `git push` — GitHub Pages republica automáticamente.

## Histórico

- v0.1 (2026-10-02) — borrador redactado por Claude (Ruta B) desde `PROPOSAL_Acciona-PM.md` y `FACT_SHEETS.md`. CV renombrado a la convención `cv-acciona-pm.pdf`.
- v0.2 (2026-10-02) — añadidos Jira, ServiceNow, gestión del cambio y uso de IA por declaración de Jose; sin experiencia declarada en construcción ni energía.
