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
* **Optimización:** Formulario estructurado con menús desplegables obligatorios: Tipo de vidrio (*Monolítico/Laminado*), Medidas exactas, Instalación de origen (*Lavadora, Selladora, Carga*), Prioridad (*Normal/Alta*) y Tipo de no conformidad (*Defecto de máquina, Rayado, Rotura por operario*). Se eliminan los fallos de interpretación.

### 2️⃣ Mesa de Corte (Receptor/Ejecutor)
* **Acción:** Recibe una cola dinámica visual de pedidos pendientes de reposición.
* **Optimización:** En lugar de esperar un lote masivo de papeles, el cortador visualiza las incidencias al instante. Puede "colar" estratégicamente las reposiciones dentro de sus tiempos muertos de corte, optimizando el aprovechamiento del material y desatascando pedidos críticos. Al terminar, actualiza el estado a "Completado" con un solo clic.

### 3️⃣ Panel de Oficina y Dirección (Auditoría)
* **Acción:** Supervisión centralizada del estado de la fábrica.
* **Optimización:** Control total de tiempos de gestión (*Lead Time*) desde que se genera el reporte hasta que se corta. Permite monitorizar de forma inmediata los picos de roturas para aplicar medidas de control de calidad preventivas y evitar pérdidas económicas.

---

## 🛠️ Stack Tecnológico Utilizado
* **Frontend:** HTML5, CSS3 (Diseño UI intuitivo y adaptado a pantallas táctiles de entorno industrial), JavaScript.
* **Backend & Base de Datos:** **Firebase Realtime Database** (Garantiza que los cambios de estado se reflejen en la mesa de corte en menos de 1 segundo sin necesidad de recargar la página).
* **Autenticación:** Firebase Auth (Control estricto de acceso por roles de operario y oficina).

---

## 📈 Impacto Operativo Estimado
* **Reducción del 100%** de errores por mala caligrafía.
* **Eliminación de tiempos de espera muertos** al transformar un proceso por lotes rígido en un flujo continuo y dinámico.
* **Trazabilidad total** para la toma de decisiones financieras y logísticas en dirección.
