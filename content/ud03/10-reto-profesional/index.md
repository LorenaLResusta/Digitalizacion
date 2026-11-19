+++
title = "Reto profesional"
weight = 10
+++

1. **Nuestro centro en la nube**
2. **Lleva a la nube tu negocio**
3. **Diseña tu propio software como servicio (SaaS)**

> Objetivo general: aplicar los conceptos de la unidad (modelos de servicio, costes, seguridad, edge/fog, ROI y despliegue) en tres retos escalonados que simulan situaciones reales. Cada reto puede abordarse individualmente o en equipos de 2–3 personas. Se recomienda escoger UNO principal y, opcionalmente, documentar comparativamente los otros dos.

## 1. Nuestro centro en la nube (Transformación educativa)
**Enunciado breve:** Migrar (de forma simulada) la infraestructura digital de un centro educativo tradicional hacia un modelo híbrido y escalable en la nube optimizando costes, disponibilidad y continuidad pedagógica.

**Contexto inicial:**

El centro dispone de:

- Servidor local antiguo (files + Moodle) con picos de saturación en evaluaciones.
- Copias de seguridad manuales en discos externos.
- Aulas con PCs heterogéneos y latencia variable.
- Presupuesto limitado y necesidad de tele‑enseñanza flexible.

**Objetivos específicos:**

- Evaluar modelo IaaS vs PaaS vs SaaS para LMS y repositorios.
- Diseñar plan de migración por fases minimizando interrupciones.
- Implementar (simulada/contenedores) un entorno reproducible.
- Estimar TCO y ROI a 1 y 3 años.
- Incorporar medidas básicas de seguridad y cumplimiento (RGPD).

**Competencias trabajadas:** Análisis coste/beneficio, arquitectura híbrida, backup & recovery, seguridad básica, documentación técnica, trabajo colaborativo.

**Fases de trabajo (propuesta):**

1. Relevamiento: inventario de servicios, usuarios, criticidad, dependencias.
2. Modelado: diagrama actual vs. objetivo (incluye edge si procede para laboratorios locales).
3. Diseño técnico: selección de servicios nube (ej: object storage + managed DB + SSO).
4. Plan de migración: orden, ventanas de cambio, rollback y pruebas.
5. Evaluación económica: tabla TCO/ROI + riesgos + plan de optimización.
6. Entregables finales y presentación ejecutiva (máx. 8 diapositivas).

**Entregables mínimos:**

| Entregable | Descripción | Formato sugerido |
|------------|-------------|------------------|
| Inventario inicial | Listado activos, SLA requerido | Markdown / CSV |
| Diagramas arquitectura | Actual y objetivo (lógica + componentes) | Draw.io / PlantUML |
| Plan migración | Fases, dependencias, riesgos, rollback | Markdown |
| Análisis costes | TCO actual vs proyectado + ROI | Hoja cálculo + resumen |
| Seguridad & backup | Controles, periodicidad, cifrado, retención | Markdown |
| Presentación ejecutiva | Resumen para dirección | PDF / PPT |

**Criterios de evaluación:** claridad técnica, viabilidad, justificación económica, gestión de riesgos, presentación.

**Rúbrica (extracto):**

| Criterio | Básico (5) | Adecuado (7) | Avanzado (9-10) |
|----------|------------|--------------|-----------------|
| Arquitectura objetivo | Parcial, incompleta | Coherente y funcional | Optimizada con resiliencia y escalado |
| Costes/ROI | Cálculos genéricos | Detalle anual razonable | Escenarios + sensibilidad |
| Seguridad/Backup | Menciones sueltas | Procedimientos definidos | Integrado con controles + pruebas |
| Plan migración | Lineal | Fases claras con hitos | Gestión riesgos + rollback sólido |
| Comunicación | Texto denso | Resumen entendible | Mensaje ejecutivo contundente |

**Herramientas sugeridas:** PlantUML / Draw.io, hoja de cálculo, Terraform (mock), contenedores (Docker Compose), documentación en Markdown.

**Checklist rápido:** inventario completo; diagrama objetivo; plan fases; costes comparativos; controles seguridad; plan backup/tests; presentación final.

---

## 2. Lleva a la nube tu negocio (Modernización PyME)
**Enunciado breve:** Una pequeña empresa de comercio electrónico on‑premise desea ampliar catálogo, internacionalizar y reducir indisponibilidades. Se pide propuesta de migración priorizando escalabilidad, observabilidad y optimización de costes.

**Riesgos actuales:** caídas en rebajas, backups manuales, falta de monitoreo proactivo, tiempos de despliegue lentos.

**Objetivos específicos:**

- Proponer arquitectura escalable (autoscaling + CDN + base de datos gestionada).
- Incluir pipeline CI/CD básico.
- Definir métricas clave (latencia, error rate, coste por transacción).
- Incorporar estrategia FinOps inicial (etiquetado, presupuestos, alertas).
- Definir plan de continuidad ante picos (campañas, Black Friday).

**Fases sugeridas:**

1. Auditoría plataforma actual (componentes + cuellos de botella).
2. Arquitectura target (front estático + API + DB gestionada + cache + CDN).
3. Estrategia de datos (migración, consistencia, backups automáticos).
4. Pipeline Dev → Prod (tests, build, despliegue azul/verde simplificado).
5. Monitoreo + alertas (APM, logs agregados, coste por servicio).
6. Optimización costes (instancias reservadas, escalado dinámico, storage por tier).

**Entregables clave:** diagrama componentes; tabla métricas + umbrales; pipeline descrito; plan migración datos; estimación coste mensual; plan respuesta picos.

**Tabla métricas ejemplo:**

| Métrica | Objetivo inicial | Umbral alerta |
|--------|------------------|---------------|
| Latencia P95 API | < 300 ms | 450 ms |
| Error rate 5xx | < 1% | 3% |
| Disponibilidad | 99.5% | 99% |
| Coste / pedido | < 0.25 € | 0.35 € |

**Riesgos y mitigación (ejemplo):**

| Riesgo | Impacto | Mitigación |
|--------|---------|------------|
| Migración DB fallida | Alto | Pruebas réplica + rollback snapshot |
| Coste inesperado CDN | Medio | Presupuesto + alertas coste |
| Picos súbitos | Alto | Autoescalado + warmup |

**Rúbrica abreviada:** innovación arquitectura (20%), realismo costes (20%), robustez pipeline (20%), monitoreo/FinOps (20%), claridad exposición (20%).

**Herramientas sugeridas:** Docker / Kubernetes (minikube opcional), GitHub Actions, Prometheus/Grafana (o mock), CDN conceptual, Terraform (borrador), calculadora costes proveedor.

**Extra opcional:** prototipo mínimo (landing + endpoint API) desplegado en un servicio gratuito o contenedor local con documentación de despliegue.

---

## 3. Diseña tu propio software como servicio (SaaS)
**Enunciado breve:** Concebir un micro‑SaaS (ej: tablero de métricas IoT, gestor de reservas, mini‑LMS) definiendo propuesta de valor, arquitectura multicliente (multi‑tenant) y estrategia de monetización y escalado.

**Objetivos específicos:**

- Definir segmento cliente y pain principal.
- Diseñar arquitectura multi‑tenant (aislamiento lógico / BD por esquema o pool).
- Plan de pricing y métricas de negocio (ARR, churn, CAC aproximado hipotético).
- Estrategia de onboarding y minimización de cold start (si usa FaaS).
- Seguridad básica (autenticación, segregación datos, cifrado en tránsito).

**Modelo de datos mínimo (ejemplo):** Tenants, Users, Subscriptions, UsageEvents.

**Fases sugeridas:**

1. Propuesta de valor y elevator pitch (máx. 60 palabras).
2. Diagramas arquitectura (lógica + datos + flujo autenticación).
3. Esquema multi‑tenant y estrategia escalado (vertical/horizontal, cache, colas).
4. Plan de monetización + costes unitarios estimados.
5. MVP funcional (mock o CLI / endpoint) + documentación API.
6. Observabilidad inicial (logging estructurado + métricas básicas).

**Entregables mínimos:** pitch, diagrama, modelo datos, descripción tenant isolation, plan pricing, endpoints API (tabla), riesgo y mitigación, roadmap MVP → M3 → M6.

**Tabla ejemplo endpoints:**

| Endpoint | Método | Descripción | Auth |
|----------|--------|-------------|------|
| /api/v1/login | POST | Autenticación usuario | JWT |
| /api/v1/tenants | GET | Lista tenants (admin) | mTLS + rol |
| /api/v1/metrics | GET | Métricas agregadas | Token |

**Rúbrica (componentes):**

| Área | Básico | Completo | Excelente |
|------|--------|----------|-----------|
| Multi‑tenant | Separación superficial | Aislamiento claro | Estrategia escalado flexible |
| Monetización | Plan único | Tiers definidos | Elastic billing + métricas |
| Arquitectura | Monolito simple | Componentes modulares | Event‑driven + resiliencia |
| Seguridad | Login simple | Roles + cifrado tránsito | Zero‑trust elementos base |
| Observabilidad | Logs básicos | Métricas clave | Trazas + dashboards |

**Métricas negocio iniciales:** MRR proyectado, churn previsto, coste infra por tenant, coste adquisición (estimación hipotética), margen bruto estimado.

**Herramientas sugeridas:** OpenAPI/Swagger, Docker, Serverless framework (opcional), SQLite/PostgreSQL (mock), Postman/Bruno, tablero métricas ligero.

**Extensión opcional:** Pequeño script de provisioning para crear un tenant nuevo (shell / PowerShell / Python) demostrando automatización.

---

**Sugerencia de presentación final (para cualquiera de los retos):**

1. Problema y contexto (1 diapositiva)
2. Objetivos y métricas clave
3. Arquitectura / Diseño
4. Plan de ejecución / Migración / Roadmap
5. Costes y ROI / Pricing
6. Seguridad y riesgos
7. Observabilidad / Operación continua
8. Conclusiones y próximos pasos

**Consejo:** Limitar la documentación textual extensa y priorizar diagramas claros + tablas sintéticas. Incluir referencias a fuentes utilizadas (calculadoras costes, guías proveedor, etc.).
