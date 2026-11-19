+++
title = "Glosario, repaso y recursos"
weight = 11
+++

## Glosario (selección de términos clave)

| Término | Definición breve | Ejemplo rápido |
|---------|------------------|----------------|
| Latencia | Tiempo entre evento y respuesta | Sensor vibra → parada máquina |
| SLA | Acuerdo formal de nivel de servicio | Disponibilidad 99.9% mensual |
| TCO | Coste total de propiedad | Hardware + energía + personal |
| ROI | Retorno sobre inversión | (Beneficio - Coste)/Coste |
| Multicloud | Uso de varios proveedores | Base datos en GCP + cómputo en AWS |
| Nube híbrida | Mezcla privada/pública integrada | Datos sensibles on‑prem, web pública |
| Edge computing | Procesar cerca del origen | Gateway filtra datos sensores |
| Fog computing | Capa intermedia agregadora | Router regional analiza tráfico |
| Mist computing | Procesamiento en el sensor | Wearable detecta arritmia |
| IaaS | Infraestructura como servicio | VM en AWS EC2 |
| PaaS | Plataforma gestionada | App Engine despliegue rápido |
| SaaS | Software listo para usar | CRM Salesforce |
| FaaS | Función bajo demanda | Lambda procesa imagen |
| FinOps | Gestión financiera nube continua | Etiquetado costes + dashboards |
| Contenerización | Empaquetar app + dependencias | Docker image microservicio |
| Orquestación | Gestionar contenedores a escala | Kubernetes despliegue rolling |
| IaC | Infraestructura como código declarativa | Terraform crea VPC |
| mTLS | Autenticación mutua de extremos | Dispositivo edge ↔ servidor seguro |
| TPM | Módulo hardware seguro | Almacena claves cifrado |
| Quantization | Reducir precisión numérica en modelo | INT8 en vez de FP32 |
| Cold start | Latencia inicial en FaaS | Primera invocación lenta |


## Preguntas globales de repaso (test rápido)

1. ¿Qué diferencia clave hay entre mist y edge en términos de latencia y alcance?
2. ¿Por qué FinOps requiere procesos iterativos y no auditorías puntuales?
3. ¿Qué criterio primario usarías para decidir entre PaaS y FaaS en una API de baja frecuencia?
4. ¿Cómo mitigar el lock-in al adoptar un servicio PaaS propietario?
5. ¿Qué métricas reunirías en un piloto edge de visión artificial?
6. ¿Por qué la nube híbrida puede reducir riesgo regulatorio?
7. ¿Cuál es el impacto de la quantization en inferencia y precisión?
8. ¿Cómo se calcula a alto nivel un ROI de migración a nube?
9. ¿Qué papel cumple la redundancia geográfica en continuidad?
10. Explica un caso donde FaaS no es buena elección.
11. ¿Qué relación existe entre TCO y decisiones de arquitectura?
12. ¿Cómo ayuda una tabla de clasificación de cargas (critical / sensitive / experimental)?
13. ¿Por qué mTLS es relevante en entornos edge distribuidos?
14. ¿Qué ventajas ofrece contenerización frente a VMs en densidad?
15. ¿Cuándo preferirías un modelo as-a-service en edge frente a comprar hardware?
16. Describe un patrón para reducir coste de transferencia de datos.
17. ¿Qué diferencia hay entre escalabilidad horizontal y vertical en la práctica cloud?
18. ¿Cómo detectar sobredimensionamiento sistemático en facturas cloud?
19. ¿Qué práctica acelera rollback seguro de modelos en edge?
20. Resume en una frase el valor estratégico de la nube.
