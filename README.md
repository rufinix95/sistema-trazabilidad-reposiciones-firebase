# 🏭 Sistema Cloud de Trazabilidad y Gestión de Reposiciones en Tiempo Real

## 📝 Visión General del Proyecto
Este proyecto nace como una solución tecnológica para erradicar las ineficiencias, pérdidas de tiempo y errores humanos derivados del uso de flujos de trabajo basados en papel en una planta de fabricación de doble acristalamiento.

A través de una **WebApp conectada a una base de datos NoSQL en tiempo real (Firebase)**, el sistema digitaliza por completo el flujo de incidencias (roturas o defectos en los cristales) desde la línea de ensamble hasta las mesas de corte y el control de dirección en oficina.

---

## 🎯 El Problema del Mundo Real (Tradicional)
Durante más de una década, la gestión de roturas se realizaba de manera analógica: anotando las incidencias en hojas de papel que el responsable acumulaba durante la jornada laboral. Esto provocaba tres graves problemas operativos:

1. **Cuellos de Botella Temporales:** Al entregarse las hojas en mano en horarios fijos (ej. a las 12:00h), las mesas de corte recibían picos de trabajo inmanejables, retrasando las cargas urgentes de transporte programadas para primera hora de la tarde.
2. **Errores de Caligrafía y Datos:** La escritura a mano provocaba confusiones fatales en dimensiones y materiales (ej. confundir un '2' con un '8'), generando rechazos de piezas y duplicando el desperdicio de material.
3. **Opacidad en Dirección:** Oficina carecía de métricas en tiempo real. Era imposible calcular el tiempo medio de resolución de una incidencia o identificar qué estaciones generaban más mermas hasta que el dinero ya se había perdido.

---

## 🚀 La Solución Digital (Arquitectura del Sistema)
El software optimiza el flujo dividiendo los accesos en **3 roles de usuario específicos**, comunicados instantáneamente mediante la nube:

### 1️⃣ Operario de Línea (Emisor)
* **Acción:** Registra la rotura de forma inmediata desde un terminal en la zona de ensamble.
* **Optimización:** Formulario estructurado con menús desplegables obligatorios: Tipo de vidrio, Medidas exactas, Instalación de origen y Tipo de no conformidad. Se eliminan los fallos de interpretación.

### 2️⃣ Mesa de Corte (Receptor/Ejecutor)
* **Acción:** Recibe una cola dinámica visual de pedidos pendientes de reposición.
* **Optimización:** El cortador visualiza las incidencias al instante. Puede "colar" estratégicamente las reposiciones dentro de sus tiempos muertos de corte, optimizando el material y desatascando pedidos críticos.

### 3️⃣ Panel de Oficina y Dirección (Auditoría y Analítica)
* **Acción:** Supervisión centralizada y toma de decisiones basada en datos.
* **Optimización:** Control total de tiempos de gestión. El sistema **calcula automáticamente la duración exacta** desde la creación hasta la compleción de cada reposición (Auditoría de Lead Time). Permite monitorizar picos de roturas para aplicar medidas de control de calidad preventivas.

### 📄 Generación de Reportes PDF
El sistema incluye un módulo de informes que permite **exportar listados filtrados de reposiciones a formato PDF** con un solo clic. Esto asegura la trazabilidad histórica para auditorías de calidad y control de material, eliminando la necesidad de archivar papeles físicos.

---

## 🛠️ Stack Tecnológico Utilizado
* **Frontend:** HTML5, CSS3, JavaScript.
* **Backend & Base de Datos:** **Firebase Realtime Database** (Garantiza reflejo de cambios en <1s).
* **Autenticación:** Firebase Auth (Control estricto de acceso por roles).

---

## 📈 Impacto Operativo Estimado
* **Reducción del 100%** de errores por mala caligrafía.
* **Eliminación de tiempos de espera muertos** al transformar un proceso por lotes rígido en un flujo continuo y dinámico.
* **Trazabilidad total y analítica de tiempos** para la toma de decisiones financieras en dirección.
