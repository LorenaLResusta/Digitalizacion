

# 🧾 TAREA 1 – Plan de Gestión de Riesgos: Despacho Legal Solutions

## Escenario

Despacho de abogados en Sevilla con 4 empleados y un único ordenador compartido.

## Objetivo

Elaborar un plan de gestión de riesgos para proteger la información confidencial de clientes, garantizar la continuidad del trabajo y reducir vulnerabilidades técnicas y humanas con presupuesto limitado (≤ 500 €).

---

## 1. Introducción

* **Contexto:** Despacho con 2 abogados, 1 secretaria y 1 auxiliar administrativo.
* **Objetivo del plan:** Evitar pérdida de datos, accesos indebidos y paradas del servicio.
* **Alcance:** Ordenador compartido, red WiFi y documentos de clientes.

---

## 2. Inventario de Activos

| Activo                   | Tipo        | Descripción                                    | Valor | Importancia |
| ------------------------ | ----------- | ---------------------------------------------- | ----- | ----------- |
| Expedientes de clientes  | Información | Documentos legales confidenciales              | Alto  | Crítica     |
| PC de escritorio         | Físico      | Único ordenador del despacho                   | Medio | Alta        |
| Emails y correspondencia | Información | Comunicación con clientes y juzgados           | Alto  | Alta        |
| Conexión WiFi            | Servicio    | Internet compartido, sin seguridad avanzada    | Medio | Media       |
| Personal del despacho    | Humano      | Conocimiento jurídico y gestión de expedientes | Alto  | Alta        |

---

## 3. Análisis de Amenazas

| Amenaza                    | Descripción                                    | Activos Afectados   | Origen              | Probabilidad |
| -------------------------- | ---------------------------------------------- | ------------------- | ------------------- | ------------ |
| **Malware**                | Virus o spyware recibido por correo o descarga | PC, expedientes     | Humano intencionado | Alta         |
| **Fallo de hardware**      | Daño físico o desgaste del disco               | PC, datos           | Técnico             | Media        |
| **Pérdida de información** | Borrado o error humano                         | Expedientes, emails | Humano accidental   | Media        |
| **Exposición de datos**    | Cliente visualiza información confidencial     | Confidencialidad    | Humano accidental   | Alta         |

---

## 4. Valoración de Riesgos

| Amenaza                   | Probabilidad | Impacto | Nivel de Riesgo | Prioridad |
| ------------------------- | ------------ | ------- | --------------- | --------- |
| Exposición de información | Alta         | Alto    | ALTO            | 1         |
| Malware                   | Alta         | Medio   | ALTO            | 2         |
| Fallo de hardware         | Media        | Alto    | ALTO            | 3         |
| Error humano              | Media        | Medio   | MEDIO           | 4         |

---

## 5. Tipos de Malware y su Prevención

| Tipo de Malware | Descripción                         | Prevención                                   |
| --------------- | ----------------------------------- | -------------------------------------------- |
| **Virus**       | Infecta archivos ejecutables        | Antivirus actualizado y análisis programados |
| **Troyano**     | Se oculta como programa legítimo    | No descargar software no verificado          |
| **Ransomware**  | Encripta archivos y exige rescate   | Backups frecuentes + formación al usuario    |
| **Spyware**     | Roba datos personales o contraseñas | Evitar webs dudosas y usar antimalware       |
| **Adware**      | Muestra publicidad invasiva         | Revisar extensiones y limpiar navegador      |
| **Keylogger**   | Registra pulsaciones del teclado    | Usar contraseñas seguras y MFA               |

---

## 6. Plan de Mejora de Seguridad

### 6.1 Medidas Técnicas

* Instalar antivirus profesional (≈ 60 €).
* Implementar copia de seguridad semanal en disco externo (≈ 80 €).
* Crear **usuarios individuales con contraseñas seguras**.
* Configurar WiFi WPA3 y cambiar contraseña cada 3 meses.

### 6.2 Política de Contraseñas

* Longitud mínima: **12 caracteres**.
* Debe incluir: mayúsculas, minúsculas, números y símbolos.
* Prohibido usar fechas de nacimiento, nombres o “1234”.
* Renovación obligatoria cada **90 días**.
* Recomendado activar **doble autenticación (MFA)**.

### 6.3 Medidas Organizativas

* Política de uso del ordenador (solo laboral).
* Prohibir abrir correos o adjuntos sin verificar remitente.
* Bloquear pantalla al dejar el puesto.

### 6.4 Medidas Físicas

* Reubicar el ordenador fuera de la vista de clientes.
* Uso de filtro de privacidad en pantalla (≈ 30 €).

### 6.5 Formación del Personal

* Sesión básica sobre ciberseguridad y RGPD.
* Procedimiento de copias de seguridad.

💰 **Coste total estimado:** 170 €
⏳ **Plazo de implementación:** 1 mes
🎯 **Prioridad global:** Alta

---

## 7. Conclusiones

El principal riesgo es la exposición o pérdida de datos.
Con las medidas propuestas, el despacho podrá proteger la información sensible, evitar interrupciones y cumplir el RGPD con una inversión mínima.

---

# 💻 TAREA 2 – Plan de Gestión de Riesgos IT: DevTech Solutions

## Escenario

Consultoría informática en Málaga con 6 empleados y una infraestructura con servidor físico, estaciones de trabajo, red y almacenamiento NAS.

## Objetivo

Analizar los riesgos técnicos y de negocio, proponiendo mejoras realistas en seguridad, continuidad y control de acceso.

---

## 1. Inventario de Activos IT

| Activo                  | Tipo        | Descripción                         | Valor | Importancia |
| ----------------------- | ----------- | ----------------------------------- | ----- | ----------- |
| Servidor Dell PowerEdge | Hardware    | Servidor principal con CRM y BBDD   | Alto  | Crítica     |
| Equipos de desarrollo   | Hardware    | PCs de los desarrolladores          | Medio | Alta        |
| NAS Synology            | Hardware    | Copias de seguridad y repositorio   | Alto  | Crítica     |
| Código fuente           | Información | Software desarrollado para clientes | Alto  | Crítica     |
| Red corporativa         | Servicio    | VLAN, firewall, VPN                 | Alto  | Alta        |
| Personal técnico        | Humano      | Conocimiento y gestión de sistemas  | Alto  | Alta        |

---

## 2. Análisis de Amenazas

| Amenaza             | Descripción                                  | Activos Afectados     | Origen       | Probabilidad |
| ------------------- | -------------------------------------------- | --------------------- | ------------ | ------------ |
| **Ransomware**      | Encriptación del servidor por vulnerabilidad | Servidor, CRM, BBDD   | Intencionado | Alta         |
| **Fallo RAID**      | Fallo de uno de los discos del servidor      | Datos críticos        | Técnico      | Media        |
| **USB infectado**   | Introducción accidental de malware           | Equipos, repositorios | Accidental   | Media        |
| **Acceso indebido** | Cliente entra a repositorio ajeno            | Datos confidenciales  | Humano       | Alta         |

---

## 3. Valoración de Riesgos

| Amenaza         | Probabilidad | Impacto  | Nivel de Riesgo | Prioridad |
| --------------- | ------------ | -------- | --------------- | --------- |
| Ransomware      | Alta         | Muy Alto | MUY ALTO        | 1         |
| Acceso indebido | Alta         | Alto     | ALTO            | 2         |
| Fallo RAID      | Media        | Alto     | ALTO            | 3         |
| USB infectado   | Media        | Medio    | MEDIO           | 4         |

---

## 4. Plan de Mejora Técnica

### 4.1 Hardening

* Aplicar políticas de contraseñas seguras y MFA.
* Desactivar servicios innecesarios en Windows Server.
* Configurar actualizaciones automáticas (patch management).

### 4.2 Backup / Recuperación

* Estrategia **3-2-1** (3 copias, 2 medios, 1 fuera del sitio).
* Verificación de backups diarios con Veeam.
* Pruebas de restauración trimestrales.

### 4.3 Control de Acceso

* Implementar RBAC (roles diferenciados por función).
* Segregar accesos a repositorios por cliente.

### 4.4 Monitorización

* Logs centralizados (Wazuh / SIEM).
* Alertas automáticas ante accesos anómalos.

### 4.5 Formación

* Capacitación en desarrollo seguro.
* Procedimiento formal de respuesta ante incidentes.

💰 **Coste estimado:** 400 €
⏳ **Plazo:** 2 meses
🎯 **Prioridad:** Alta

---

## 5. Conclusiones

Los principales riesgos son **ransomware, fallos del RAID y accesos indebidos**.
El plan refuerza la seguridad, garantiza la continuidad del negocio y mejora el cumplimiento del RGPD e ISO 27001.

---

# 🧩 TAREA 3 – Plan de Gestión Ampliado: Integración Global y Mejora Continua

## Objetivo

Combinar las lecciones de ambos casos (Legal y DevTech) para crear una guía de gestión de riesgos universal para pymes sin departamento IT.

---

## 1. Estrategia Unificada

* Clasificar activos por tipo y criticidad.
* Implementar backups periódicos y verificados.
* Definir políticas de contraseñas y acceso.
* Formar al personal mínimo una vez al año.

---

## 2. Medidas Clave de Bajo Coste

| Medida                         | Coste Estimado | Beneficio                    |
| ------------------------------ | -------------- | ---------------------------- |
| Antivirus profesional          | < 100 €        | Protección contra malware    |
| Disco externo o NAS básico     | < 150 €        | Copias de seguridad seguras  |
| Políticas de contraseñas + MFA | 0 €            | Mayor control de acceso      |
| Revisión mensual de seguridad  | 1 h interna    | Detección temprana de fallos |

---

## 3. Cultura de Seguridad

* Cada empleado es responsable de su equipo y datos.
* Ningún cliente debe ver información en pantalla.
* Cualquier incidente debe documentarse y analizarse.

---

## 4. Mantenimiento Continuo

| Actividad                 | Frecuencia | Responsable             |
| ------------------------- | ---------- | ----------------------- |
| Copias de seguridad       | Semanal    | Administrador designado |
| Actualización de software | Mensual    | Usuario avanzado        |
| Revisión de contraseñas   | Trimestral | Todos los empleados     |
| Formación en seguridad    | Anual      | Dirección               |

---

## 5. Conclusión Global

Una pyme puede alcanzar un nivel de **ciberseguridad aceptable sin gran presupuesto** si:

1. Sabe **qué proteger**,
2. Mantiene **hábitos constantes**, y
3. **Forma al personal** para no ser el eslabón débil.

---

