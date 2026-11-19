+++
title = "4. Datos, seguridad y necesidades futuras"
weight = 5
+++

## 4.1 Tratamiento de datos masivos

El proyecto debe definir:

- **Qué datos** se recogerán en cada área.
- **Dónde** se almacenarán y cómo se integrarán (UD05).
- **Qué indicadores** se calcularán y quién los verá.
- **Qué análisis** o modelos de IA se aplicarán y para qué decisiones.
- **Quién es responsable** de la calidad de cada dato.

## 4.2 Análisis de brechas de seguridad por área

Para cada área digitalizada se analizan los riesgos:

| Área | Activo | Amenaza | Probabilidad | Impacto | Medida |
|------|--------|---------|--------------|---------|--------|
| Comercial | CRM con datos de clientes | Robo de credenciales | Media | Alto | Doble factor, mínimo privilegio |
| Administración | Datos bancarios y facturas | Fraude por suplantación (*phishing*) | Media | Alto | Verificar cambios de cuenta por otro canal, formación |
| Sistemas | Plataforma de cursos | Caída o ransomware | Baja | Muy alto | Copias 3-2-1, plan de continuidad |
| Producción | Archivos de vídeo | Borrado accidental | Media | Medio | Versionado y papelera con retención |

## 4.3 Necesidades presentes y futuras

Un buen proyecto piensa en **escalabilidad**: ¿la solución servirá si la empresa duplica clientes?, ¿se podrá añadir IA más adelante?, ¿se puede cambiar de proveedor sin perder los datos? Elegir estándares abiertos y soluciones que exporten los datos en formatos comunes reduce la dependencia de un proveedor.
