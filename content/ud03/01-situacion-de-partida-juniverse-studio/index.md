+++
title = "Situación de partida: Juniverse Studio"
weight = 1
+++

## 0.1 Contexto

Estudio creativo/educativo que desarrolla pequeños proyectos multimedia y prototipos formativos. Infraestructura local heredada, crecimiento orgánico sin estandarización y necesidad emergente de colaborar en remoto y escalar picos (campañas formativas / talleres online).

## 0.2 Actores / Stakeholders

| Actor | Interés principal | Dolor actual | Nivel de influencia |
|-------|-------------------|--------------|---------------------|
| Dirección | Costes predecibles y ROI | Gastos puntuales de hardware | Alta |
| Equipo técnico | Automatizar despliegues | Mantenimiento manual servidores | Alta |
| Docentes / creadores | Estabilidad y acceso remoto | Caídas en picos de uso | Media |
| Estudiantes / usuarios | Experiencia fluida | Latencias y tiempos de carga | Media |
| Compliance / legal | Protección datos y RGPD | Copias dispersas | Media |

## 0.3 Problemática inicial

- Infraestructura fragmentada (NAS + PC improvisado como servidor) sin redundancia.
- Copias de seguridad manuales y no verificadas.
- Crecimiento de contenidos multimedia saturando almacenamiento local.
- Escalabilidad reactiva: se compra hardware tras cada saturación.
- Ausencia de métricas (uso CPU, transferencia, coste por proyecto).
- Riesgo de downtime en talleres remotos y evaluaciones.

## 0.4 Objetivos iniciales (visión)

| Nº | Objetivo | Criterio éxito (indicador) | Horizonte |
|----|----------|---------------------------|-----------|
| 1 | Estabilizar servicio contenidos | <1 caída crítica / trimestre | 3 meses |
| 2 | Estandarizar backups | 100% tareas backup verificadas semanal | 2 meses |
| 3 | Reducir coste picos | -25% coste puntual hardware (vs histórico) | 6 meses |
| 4 | Obtener métricas uso | Dashboard básico recursos y tráfico | 2 meses |
| 5 | Preparar migración modular nube | Plan fases aprobado por dirección | 3 meses |

## 0.5 Restricciones

- Presupuesto anual limitado (priorizar OPEX gradual).
- Dependencia de algunos archivos binarios grandes (vídeo crudo) que penalizan migración completa inmediata.
- Personal técnico reducido (1 perfil mixto dev/infra).
- Ventanas de mantenimiento restringidas (horario fuera de talleres).

## 0.6 Riesgos y mitigación (preliminar)

| Riesgo | Impacto | Prob. | Mitigación | Indicador alerta |
|--------|---------|-------|-----------|------------------|
| Pérdida datos por error humano | Alto | Media | Política backup 3-2-1 + verificación | Informe semanal verificación |
| Sobrecoste nube inicial | Medio | Alta | Pilotos controlados + tagging costes | Desviación >15% presupuesto |
| Lock-in servicio propietario | Medio | Media | Diseño híbrido + formatos abiertos | % componentes portables |
| Downtime en formación | Alto | Media | CDN + caché y pre-test sesiones | Latencia P95 > 500 ms |
| Falta de adopción interna | Medio | Media | Formación y guías de uso | Encuesta satisfacción interna |

## 0.7 Métricas baseline (a recopilar)

- Tiempo medio de recuperación ante caída (MTTR actual estimado > 2h).
- Uso promedio CPU almacenamiento improvisado (>70% en picos).
- Tamaño dataset multimedia (≈ X TB, medir real al iniciar).
- Frecuencia real de backups completos (actual: ad-hoc / irregular).
- Latencia media acceso remoto a contenidos (medir para fijar SLA interno).

## 0.8 Estado actual vs. objetivo (resumen)

| Área | Estado actual | Objetivo deseado | Gap principal |
|------|---------------|------------------|---------------|
| Almacenamiento | NAS único sin verificación | Storage escalable + versionado | Falta redundancia |
| Backups | Manuales no auditados | Automatizados + verificados | Procedimiento |
| Despliegues | Manual / scripts sueltos | Pipeline reproducible | Automatización |
| Observabilidad | Nula | Dashboard básico recursos y costes | Telemetría |
| Escalabilidad | Reactiva (compra hardware) | Predictiva (autoescalado / CDN) | Cultura & tooling |
| Costes | Picos CAPEX imprevisibles | OPEX controlado y etiquetado | Modelado costes |
| Seguridad | Accesos compartidos | Control roles + cifrado en tránsito | Gobierno |

## 0.9 Próximos pasos propuestos

1. Inventario técnico detallado (activos, tamaños, dependencias).
2. Clasificación datos (crítico / sensible / general) para priorizar migración.
3. Prueba piloto almacenamiento objeto + CDN para contenidos estáticos.
4. Implementar política backup automatizada (script + logs verificación).
5. Instrumentar métricas básicas (uso CPU, espacio, latencia) y panel.
6. Definir arquitectura objetivo fase 1 (híbrida mínima) y plan de coste.

> Nota: Esta “Situación de partida” sirve como documento vivo: tras recopilar métricas reales, actualizar baseline y revisar riesgos antes de ejecutar la primera fase de migración.
