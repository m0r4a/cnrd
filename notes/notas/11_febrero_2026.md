# 11 de Febrero 2026 - Políticas y Gestión de Riesgos en BCMS (ISO 22301)

!!! info "Recapitulación Inicial"

    La sesión inició con un repaso sobre los conceptos de BCP y DRP. Se definió la **resiliencia operacional** de forma práctica como: *"Estirar lo máximo que se pueda sin romperse"*.

---

## ISO 22301:2019

### Política de Continuidad de Negocio

La política es el documento maestro que rige el Sistema de Gestión de Continuidad del Negocio (BCMS). Debe ser un documento formal que contenga: versión, fecha, clave de identificación, responsable, alcance definido, marco teórico, y sobre todo, debe ser clara, concisa y medible.

### Dueño vs. Custodio de la Información

Es fundamental separar las responsabilidades sobre los datos y activos en la organización:

- **Dueño de la Información (Data Owner):**

  Es la persona con el nivel jerárquico más alto en el área que genera o utiliza los datos. Por ejemplo, el Director de Finanzas (CFO) es el dueño de los archivos y registros financieros confidenciales. En el caso del documento de continuidad de negocio, el dueño suele ser el CISO o el director encargado del BCMS.

- **Custodio de la Información (Data Custodian):**

  Es el área técnica o proceso (generalmente TI o Seguridad de la Información) responsable de velar porque esa información mantenga su [Confidencialidad, Integridad y Disponibilidad (Triada CIA)](https://es.wikipedia.org/wiki/Seguridad_de_la_informaci%C3%B3n#Principios_de_la_seguridad_de_la_informaci%C3%B3n).



[Image of Information Security CIA triad]


---

### Ciclo de Vida y Cumplimiento de Políticas

No basta con escribir el documento. Para garantizar (*enforce*) que las políticas se cumplan, se debe seguir un ciclo continuo y no detenerse en los primeros pasos:

1. **Hacer la política:**

   Redacción y aprobación formal del documento.

2. **Informar la política:**

   Capacitación, educación y concientización a todo el personal involucrado. Muchas organizaciones se detienen aquí, asumiendo que el trabajo ha terminado.

3. **Medir efectividad:**

   Establecer KPIs y métricas efectivas evaluando a los responsables definidos en el documento. Una excelente herramienta para medir el conocimiento y la respuesta de los responsables es el [Tabletop Exercise (Ejercicio de simulación de escritorio)](https://www.cisa.gov/resources-tools/services/cisa-tabletop-exercises-packages), donde se discute un escenario ficticio de desastre para evaluar la toma de decisiones.

4. **Mejora continua:**

   Basado en el ciclo perpetuo de **Analizar -> Medir -> Mejorar**. Las políticas deben evolucionar con el negocio y los resultados empíricos de las mediciones.

---

### Rendición de Cuentas (Accountability)

- **¿Quién tiene la rendición de cuentas definitiva?**

  La responsabilidad última (*accountability*) siempre recae en el nivel jerárquico más alto de la organización, es decir, el CEO, el Consejo de Administración o los Accionistas.

---

## Gestión de Incidentes y Comunicación

### Orden de Respuesta ante un Incidente

¿Qué se hace primero: Contener, Investigar, Recuperar o Informar? 

La respuesta técnica y operativa correcta es que **depende** de la naturaleza del incidente, aunque la contención suele ser la prioridad inmediata para mitigar la propagación del daño.

### Comunicación en Crisis

- **¿Quién comunica y qué se comunica?**

  La decisión de quién activa el plan y quién se encarga de las comunicaciones depende directamente del impacto. Se debe evaluar meticulosamente qué tipo de información ha sido afectada:

  - Pública.

  - Privada.

  - Interna.

  - Confidencial:

    - Procesos de negocio críticos.

    - Información de empleados.

    - Información de clientes, que se subdivide en datos regulados como [PII (Personally Identifiable Information)](https://www.imperva.com/learn/data-security/pii-personally-identifiable-information/) y [PHI (Protected Health Information)](https://www.hhs.gov/hipaa/for-professionals/privacy/laws-regulations/index.html).

---

## Integración en los Procesos de Negocio

El BCMS no es un silo de TI; debe estar intrínsecamente incorporado en los procesos operativos reales de la organización y alineado con la misión, visión y objetivos corporativos.

!!! note "El Valor Indirecto de la Seguridad y Continuidad"

    Puede ser complejo aterrizar la misión y visión de la empresa con controles técnicos o análisis de riesgos. Sin embargo, si TI y Seguridad de la Información no protegen la integridad, confidencialidad y disponibilidad, el negocio no podrá operar, vender su producto o prestar su servicio. Aunque TI no siempre genere ingresos directos, aporta un valor indirecto incalculable al garantizar la supervivencia operativa.

---

## Acciones para Abordar Riesgos y Oportunidades

En el marco de la gestión ISO, se deben evaluar ambas caras de la moneda ante la incertidumbre:

- **Riesgo:** Probabilidad de que un evento afecte *negativamente* a los objetivos.

- **Oportunidad:** Probabilidad de que un evento afecte *positivamente* a los objetivos.

### Identificación de Riesgos

- **Evaluación integral:**

  No se limita a los sistemas; abarca cualquier evento que tenga un impacto económico o de viabilidad de negocio.

- **Identificación de activos y recursos críticos:**

  Saber qué es lo que realmente importa proteger y mantener operativo.

- **Riesgos sobre el propio BCMS:**

  Identificar qué sucede si el sistema de gestión falla por sí mismo. Por ejemplo, el riesgo de no tomar en serio los simulacros de recuperación o los escenarios internos que podrían llevar al fracaso absoluto de la política de continuidad.

### Tratamiento del Riesgo



Una vez identificado un riesgo operativo o tecnológico, existen cuatro posturas para tratarlo:

1. **Transferir:**

   Pasar el riesgo financiero o técnico a un tercero (ej. contratar un seguro de ciberseguridad o mover la carga a un proveedor de nube pública con un SLA estricto).

2. **Evitar:**

   Cambiar el plan, el proceso o la arquitectura para no exponerse a esa amenaza (ej. decidir no almacenar números de tarjetas de crédito en bases de datos propias para evitar el riesgo de robo).

3. **Aceptar:**

   Reconocer el riesgo y su impacto, decidiendo conscientemente no actuar debido a que el costo de mitigación supera con creces el impacto potencial.

4. **Mitigar:**

   Implementar controles técnicos, arquitectónicos o administrativos para reducir la probabilidad o el impacto del riesgo a un nivel aceptable para el negocio.
