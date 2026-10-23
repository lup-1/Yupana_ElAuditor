# EQUIPO YUPANA-PE

## 1. Presentación del equipo

**YUPANA-PE** es un equipo que desarrolla una propuesta de solución tecnológica para mejorar la auditoría, revisión y control de información en proyectos del sector AEC (Architecture, Engineering and Construction: arquitectura, ingeniería y construcción).

El proyecto **YUPANA — El Auditor** busca reducir el trabajo manual y los errores derivados de manejar presupuestos, metrados y avances de obra en archivos y canales separados, combinando automatización, análisis de datos e inteligencia artificial.

## 2. Integrantes y áreas de contribución

| Integrante | Área de contribución propuesta |
|---|---|
| Marco Antonio Huamani Ipurre | Gestión de proyectos AEC, planificación, metrados y control contractual de obra. |
| Jonathan José Frias Martínez | Análisis de presupuestos, costos unitarios y valorizaciones. |
| Lucía Berioska Meléndez Castro | Desarrollo en Python, lógica de programación y procesamiento de datos. |
| Brayan Jared Gonzales Callejas | Automatizaciones e integración de herramientas No-Code, como n8n o Make. |
| Cristina Solangel Tarazona Silva | BIM, revisión técnica de expedientes y control de calidad. |

*Nota: las áreas indicadas son una distribución inicial de responsabilidades y pueden ajustarse según la experiencia y las funciones acordadas por el equipo.*

## 3. Problema identificado

En proyectos de construcción, la información de presupuestos, metrados, valorizaciones y avances suele estar distribuida entre hojas de Excel, correos, mensajes y otros documentos. La revisión manual de estas fuentes puede generar:

- Duplicidad de información y dificultades para identificar la versión vigente.
- Inconsistencias entre cantidades, partidas, costos y avances reportados.
- Demoras en la revisión y elaboración de informes.
- Errores de digitación, cálculos repetidos y falta de trazabilidad.
- Detección tardía de desviaciones que pueden afectar el costo o el plazo de obra.

## 4. Objetivo del proyecto

Diseñar y desarrollar un prototipo funcional que centralice y procese información de obra, automatice verificaciones y genere resultados trazables para apoyar la auditoría y el control de proyectos AEC.

La solución busca asistir al usuario en la identificación de diferencias y alertas. No reemplaza la revisión ni el criterio del profesional responsable.

## 5. Módulos propuestos

### YUPANA-COST — Auditoría de costos

- Procesamiento de presupuestos y análisis de partidas.
- Revisión de costos unitarios, subtotales y totales.
- Identificación de valores faltantes, duplicados o potencialmente inconsistentes.

### YUPANA-CONTROL — Seguimiento de avances

- Análisis de avances físicos y económicos.
- Comparación de valores planificados y reportados.
- Clasificación preliminar de desviaciones mediante estados como **NORMAL**, **LEVE**, **ALERTA** y **CRÍTICA**, según reglas que el equipo defina y documente.

### YUPANA-REVISA — Verificación cruzada

- Comparación entre presupuestos, metrados y reportes de avance.
- Identificación de diferencias entre fuentes.
- Generación de observaciones para revisión técnica.

### YUPANA-TRACE — Trazabilidad

- Registro de la fuente de cada dato utilizado.
- Documentación de reglas, cálculos y resultados.
- Control de versiones de archivos e informes, cuando la implementación lo permita.

## 6. Flujo de trabajo previsto

1. **Recepción de archivos:** por ejemplo, `Presupuesto.xlsx`, `Metrados.xlsx` y `Avance_Mensual.xlsx`.
2. **Extracción y normalización:** lectura de tablas, encabezados, partidas, unidades y cantidades.
3. **Validación:** revisión de campos vacíos, formatos y valores atípicos.
4. **Verificación cruzada:** comparación de datos entre los archivos disponibles.
5. **Evaluación de reglas:** ejecución de cálculos y criterios de control definidos por el equipo.
6. **Clasificación de observaciones:** presentación de diferencias y alertas para revisión.
7. **Generación del informe:** elaboración de un reporte con resultados, observaciones y referencias a los datos de origen.

## 7. Arquitectura tecnológica propuesta

| Componente | Tecnología o herramienta | Uso previsto |
|---|---|---|
| Procesamiento de datos | Python, Pandas y OpenPyXL | Lectura, transformación y análisis de hojas de cálculo. |
| Inteligencia artificial | Modelos de lenguaje (LLM) | Apoyo en interpretación de texto y explicación de observaciones, con validación de resultados. |
| Automatización | n8n o Make | Orquestación de tareas e integración de herramientas. |
| Archivos de entrada y salida | Excel y reportes documentales | Intercambio de información e informes de resultados. |
| Control de versiones | Git y GitHub | Gestión del código, documentación y cambios del proyecto. |
| Organización y diseño | Miro y herramientas colaborativas | Mapeo de procesos, arquitectura y planificación. |

*La arquitectura es una propuesta inicial. Las tecnologías definitivas dependerán de las pruebas del prototipo y de los requisitos del proyecto.*

## 8. Entregables previstos

- Repositorio documentado y control de versiones.
- Prototipo para procesar archivos de ejemplo.
- Reglas de validación y comparación documentadas.
- Informe de auditoría generado a partir de los datos procesados.
- Casos de prueba con resultados verificables.
- Documentación de limitaciones, supuestos y oportunidades de mejora.

## 9. Criterios de evaluación del MVP

El equipo podrá evaluar el prototipo con indicadores como:

- Porcentaje de verificaciones que producen resultados correctos frente a casos revisados manualmente.
- Número de inconsistencias detectadas en un conjunto de prueba conocido.
- Tiempo requerido para procesar archivos y generar el informe.
- Trazabilidad de las observaciones hasta sus datos de origen.
- Facilidad para reproducir un análisis con los mismos archivos y reglas.

Los valores objetivo deben definirse después de construir una línea base y preparar casos de prueba.

## 10. Calidad, seguridad y limitaciones

- Probar los cálculos con casos controlados y contrastarlos con resultados de referencia.
- Mantener separadas las reglas deterministas de cálculo y las explicaciones generadas por IA.
- No presentar una alerta automática como prueba definitiva de error: las observaciones requieren revisión profesional.
- Utilizar datos ficticios o anonimizados cuando sea posible y evitar subir al repositorio público información confidencial de obras, clientes o personas.
- Documentar supuestos, limitaciones, versiones y cambios relevantes.

---

**Equipo:** YUPANA-PE  
**Proyecto:** YUPANA — El Auditor  
**Sector de aplicación:** AEC (arquitectura, ingeniería y construcción)  
**Propósito:** automatizar la revisión y el control de presupuestos, metrados y avances de obra con análisis de datos, IA y trazabilidad.
