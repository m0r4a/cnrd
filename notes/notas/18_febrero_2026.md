# 18 de Febrero - Continuidad de Negocio y Objetivos

## Objetivos del Negocio

### El Marco SMART

Al definir objetivos técnicos o de negocio, asegúrate de utilizar los criterios [SMART](https://www.atlassian.com/es/agile/project-management/smart-goals):

- **Específico:**

  Define de forma clara y sin ambigüedades qué se quiere lograr o mejorar.

- **Medible:**

  Cuantifica o sugiere un indicador claro de progreso.

- **Alcanzable:**

  Establece metas realistas considerando los recursos, presupuesto y tiempo disponibles.

- **Relevante:**

  Alineado fuertemente con los objetivos generales del negocio o de la arquitectura.

- **Tiempo determinado:**

  Especifica una fecha límite estricta para su cumplimiento.

!!! example "Ejemplo SMART: Entorno de Desarrollo en Kubernetes"

    Implementar un entorno de desarrollo funcional con [Kubernetes](https://kubernetes.io/es/docs/concepts/overview/) antes del 23 de febrero de 2026, asegurando que el clúster pueda desplegarse automáticamente desde código y que permita publicar al menos 7 microservicios accesibles vía Ingress.

    **Desglose SMART:**

    - **Específico:**

      Entorno de desarrollo en Kubernetes con 7 microservicios.

    - **Medible:**

      Clúster desplegable automáticamente + 7 microservicios expuestos.

    - **Alcanzable:**

      Alcance definido y cuantificable para el equipo.

    - **Relevante:**

      Refuerza las capacidades en arquitectura distribuida e infraestructura del área.

    - **Tiempo definido:**

      23 de febrero de 2026.

---

### Objetivos de Recuperación: RTO, RPO y MBCO

Definir el tiempo de inactividad aceptable y la pérdida de datos tolerada es el núcleo de cualquier plan de recuperación de desastres ([DRP](https://aws.amazon.com/es/disaster-recovery/)).

!!! example "RTO (Objetivo de Tiempo de Recuperación)"

    Diseñar, implementar y validar un plan de recuperación que garantice un RTO máximo de 30 minutos para la plataforma principal antes del 15 de marzo de 2026, realizando al menos 1 simulacro a la semana de desastre documentado y demostrando recuperación completa del servicio dentro del tiempo objetivo.

!!! example "RPO (Objetivo de Punto de Recuperación)"

    Garantizar la retención y sincronización para no perder más de 15 minutos de transacciones de datos ante una falla crítica de base de datos.

!!! example "MBCO (Objetivo Mínimo de Continuidad del Negocio)"

    Mantener la operación a un mínimo del 40% de la capacidad total del despacho de mercancía durante las primeras 24 horas posteriores a un incidente disruptivo.

**Consideraciones Clave para los Objetivos de Continuidad:**

- **Ser coherente con la política de continuidad:**

  La política general define el nivel de riesgo aceptable de la organización. Tus objetivos técnicos no deben sobredimensionar la infraestructura (gastando dinero de más) ni subdimensionarla (asumiendo riesgos inaceptables).

- **Ser medibles:**

  Requieren instrumentación y pruebas. Si no lo mides, es solo una esperanza.

- **Tener en cuenta requisitos aplicables:**

  Considerar siempre obligaciones legales, normativas o compromisos contractuales de disponibilidad (SLA).

- **Ser comunicados y actualizados:**

  Deben revisarse periódicamente y comunicarse a todos los *stakeholders* clave del negocio y TI.

---

## Planificación en el BCMS

### Planificación de Cambios (Plan y Política)

Al introducir cambios dentro del Sistema de Gestión de Continuidad del Negocio (BCMS), se deben evaluar rigurosamente los siguientes factores:

- **Propósito:**

  La razón arquitectónica o de negocio que justifica la modificación.

- **Consecuencias:**

  Impactos potenciales y efectos cascada que podría traer el cambio a los servicios actuales.

- **Integridad del BCMS:**

  Garantizar que el sistema general y la postura de resiliencia no se degraden por el cambio.

- **Disponibilidad de Recursos:**

  Validar que se cuenta con el presupuesto financiero, personal capacitado, documentación actualizada, proveedores de terceros listos y componentes físicos necesarios.

- **Asignación de Responsables:**

  Mapeo claro de roles sobre quién ejecuta, quién supervisa y quién aprueba.

---

### Planificación de Prevención (Cláusula 6 - ISO 22301:2019)

La norma [ISO 22301](https://www.iso.org/standard/75106.html) para sistemas de gestión de continuidad de negocio clasifica los controles en distintas categorías de acción:

- **Prevención**

- **Corrección**

- **Mitigación**

- **Detectivo**

- **Compensatorio**

- **Disuasión**

!!! tip "Enfoque Proactivo vs Reactivo"

    El mensaje central aquí es que tu BCP (*Business Continuity Plan*) y DRP no deben componerse exclusivamente de medidas **compensatorias** o reactivas. Es imperativo integrar controles **preventivos** sólidos desde el diseño de la arquitectura para evitar que los incidentes se materialicen en primer lugar.

---

### Relación entre Riesgo y BIA

Es crucial entender la diferencia entre estas dos herramientas de análisis en la resiliencia de TI:

- **Riesgo:**

  Identifica las amenazas y vulnerabilidades; te dice **qué** puede salir mal o qué evento disruptivo es probable que ocurra.

- **BIA (Análisis de Impacto al Negocio):**

  Evalúa las consecuencias; te dice **cuánto** te va a impactar operativa y financieramente si ese riesgo llega a materializarse.

---

### Monitoreo de Desempeño

- **Medición continua:**

  Se requiere instrumentación técnica (telemetría, logs, dashboards) y auditorías de procesos para verificar empíricamente que los RTOs, RPOs y controles preventivos funcionan bajo las expectativas durante operaciones normales y simulacros.
