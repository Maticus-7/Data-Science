<div style="display:flex; align-items:center; gap:14px; margin-bottom:18px;">
    <img src="https://i.postimg.cc/J7sf3Lq4/Group.png" alt="FUTURA" style="height:70px;"/>
    <div>
        <div style="font-size:22px; font-weight:700; line-height:1.25;">FUTURA, Data y Analítica Avanzada</div>
        <div style="font-size:16px; line-height:1.35;">Caso aplicado — Segmentación no supervisada</div>
        <div style="font-size:14px; color:#555; line-height:1.35;">KDD Internet Usage · Caso 17</div>
    </div>
</div>

---

**Incluye enunciado del caso, guía de análisis y criterios de solución.**

# Usuarios de Internet — Personas Digitales

## Resumen Ejecutivo

Dataset **KDD Internet Usage** con **10,108 filas** y **71 variables de trabajo**. El caso está diseñado para **Segmentación no supervisada** en un contexto de investigación de mercado, adopción digital y diseño de audiencias.

---

## 1. Contexto de Negocio

Este caso permite trabajar un problema accionable: descubrir perfiles de usuarios digitales según demografía, acceso, hábitos de compra, uso web y actitudes hacia internet. El dataset reúne señales propias del dominio y permite conectar el análisis exploratorio con una decisión práctica.

**Decisión que se espera soportar:** el equipo debe transformar el análisis en una recomendación concreta para investigación de mercado, adopción digital y diseño de audiencias. La entrega debe dejar claro qué se prioriza, qué se predice o qué segmentos se accionan, y qué haría el stakeholder con los resultados.

---

## 2. Objetivo del Proyecto

**Objetivo principal:**
Descubrir perfiles de usuarios digitales según demografía, acceso, hábitos de compra, uso web y actitudes hacia internet.

**Objetivos específicos:**
- Auditar calidad de datos, valores atípicos, codificaciones y variables que puedan generar leakage.
- Preparar variables numéricas, categóricas, fechas, texto o geografía según corresponda.
- Construir una solución reproducible de segmentación no supervisada.
- Interpretar resultados con lenguaje de negocio y recomendaciones accionables.
- Documentar restricciones éticas, operativas y de despliegue.

### 2.1 Instrucciones para el Estudiante

El estudiante debe construir una solución no supervisada para descubrir grupos interpretables. La variable `who_pays_for_access_work` es una referencia para perfilar o contrastar resultados; no debe usarse para formar los clusters salvo que el docente indique lo contrario.

**Preguntas que debe responder el trabajo:**
- ¿Qué variables se usan para formar segmentos y por qué son apropiadas para el negocio?
- ¿Qué variables se excluyen por ser identificadores, targets de referencia o información redundante?
- ¿Cuántos segmentos se recomiendan y qué evidencia respalda esa decisión?
- ¿Cómo se llama cada segmento y qué rasgos lo diferencian de los demás?
- ¿Qué acción concreta tomaría el negocio para cada segmento?

**No se acepta:** entregar clusters sin nombres de negocio, elegir k sin justificación, usar la variable de referencia como input, o presentar gráficos sin recomendaciones accionables.

---

## 3. Stakeholders y Audiencia

| Stakeholder | Rol | Interés principal |
|---|---|---|
| Sponsor de negocio | Dueño del problema | Mejorar decisiones, priorización o eficiencia |
| Equipo operativo | Usuario | Aplicar predicciones, segmentos o alertas en procesos reales |
| Analytics / Data Science | Ejecutor | Preparar datos, modelar, validar e interpretar |
| Riesgo / Compliance | Consultado | Revisar sesgos, privacidad, trazabilidad y uso responsable |
| Dirección | Informado | Evaluar impacto, límites y retorno esperado |

---

## 4. Dataset

### 4.1 Descripción General

| Campo | Detalle |
|---|---|
| **Nombre** | KDD Internet Usage |
| **Fuente** | OpenML |
| **URL** | https://www.openml.org/d/43920 |
| **Licencia** | OpenML / verificar ficha fuente |
| **Filas totales** | 10,108 |
| **Variables** | 71 |
| **Variable objetivo / referencia** | `who_pays_for_access_work` |
| **Tipo de problema** | Segmentación no supervisada |
| **Case ID** | 17 |
| **Dataset original** | openml_43920 |
| **Fecha de descarga** | 2026-07-01 |
| **Hash MD5** | `3cbc1f6fccc5c9aba9a1f7de56d09ef1` |

### 4.2 Diccionario de Variables

| Variable | Tipo | Descripción | Comentario |
|---|---|---|---|
| `actual_time` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: actual time. | Perfil digital |
| `age` | categórica | Atributo demográfico declarado por el usuario digital: age. | Perfil digital |
| `community_building` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community building. | Perfil digital |
| `community_membership_family` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community membership family. | Perfil digital |
| `community_membership_hobbies` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community membership hobbies. | Perfil digital |
| `community_membership_none` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community membership none. | Perfil digital |
| `community_membership_other` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community membership other. | Perfil digital |
| `community_membership_political` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community membership political. | Perfil digital |
| `community_membership_professional` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community membership professional. | Perfil digital |
| `community_membership_religious` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community membership religious. | Perfil digital |
| `community_membership_support` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: community membership support. | Perfil digital |
| `country` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: country. | Perfil digital |
| `disability_cognitive` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: disability cognitive. | Perfil digital |
| `disability_hearing` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: disability hearing. | Perfil digital |
| `disability_motor` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: disability motor. | Perfil digital |
| `disability_not_impaired` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: disability not impaired. | Perfil digital |
| `disability_not_say` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: disability not say. | Perfil digital |
| `disability_vision` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: disability vision. | Perfil digital |
| `education_attainment` | categórica | Indicador socioeconómico, de gasto, vivienda o activo del hogar: education attainment. | Hogar / socioeconomía |
| `falsification_of_information` | categórica | Variable de negocio identificable como falsification of information; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `gender` | categórica | Atributo demográfico declarado por el usuario digital: gender. | Perfil digital |
| `household_income` | categórica | Indicador socioeconómico, de gasto, vivienda o activo del hogar: household income. | Hogar / socioeconomía |
| `how_you_heard_about_survey_banner` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey banner. | Perfil digital |
| `how_you_heard_about_survey_friend` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey friend. | Perfil digital |
| `how_you_heard_about_survey_mailing_list` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey mailing list. | Perfil digital |
| `how_you_heard_about_survey_others` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey others. | Perfil digital |
| `how_you_heard_about_survey_printed_media` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey printed media. | Perfil digital |
| `how_you_heard_about_survey_remebered` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey remebered. | Perfil digital |
| `how_you_heard_about_survey_search_engine` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey search engine. | Perfil digital |
| `how_you_heard_about_survey_usenet_news` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey usenet news. | Perfil digital |
| `how_you_heard_about_survey_www_page` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: how you heard about survey www page. | Perfil digital |
| `major_geographical_location` | categórica | Variable de negocio identificable como major geographical location; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `major_occupation` | categórica | Indicador socioeconómico, de gasto, vivienda o activo del hogar: major occupation. | Hogar / socioeconomía |
| `marital_status` | categórica | Característica sociodemográfica del cliente: marital status. | Perfil del cliente |
| `most_import_issue_facing_the_internet` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: most import issue facing the internet. | Perfil digital |
| `opinions_on_censorship` | categórica | Variable de negocio identificable como opinions on censorship; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `primary_computing_platform` | categórica | Variable de negocio identificable como primary computing platform; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `primary_language` | categórica | Variable de negocio identificable como primary language; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `primary_place_of_www_access` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: primary place of www access. | Perfil digital |
| `race` | categórica | Categoría racial registrada; variable sensible que debe evaluarse con cautela. | Variable clínica |
| `not_purchasing_bad_experience` | categórica | Variable de negocio identificable como not purchasing bad experience; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_bad_press` | categórica | Medición ambiental o meteorológica: not purchasing bad press. | Sensor ambiental |
| `not_purchasing_cant_find` | categórica | Variable de negocio identificable como not purchasing cant find; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_company_policy` | categórica | Indicador de tenencia, contribución o propensión aseguradora relacionado con not purchasing company policy. | Seguros |
| `not_purchasing_easier_locally` | categórica | Variable de negocio identificable como not purchasing easier locally; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_enough_info` | categórica | Variable de negocio identificable como not purchasing enough info; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_judge_quality` | categórica | Variable de negocio identificable como not purchasing judge quality; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_never_tried` | categórica | Variable de negocio identificable como not purchasing never tried; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_no_credit` | categórica | Variable de negocio identificable como not purchasing no credit; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_not_applicable` | categórica | Variable de negocio identificable como not purchasing not applicable; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_not_option` | categórica | Variable de negocio identificable como not purchasing not option; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_other` | categórica | Variable de negocio identificable como not purchasing other; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_prefer_people` | categórica | Variable de negocio identificable como not purchasing prefer people; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_privacy` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: not purchasing privacy. | Perfil digital |
| `not_purchasing_receipt` | categórica | Variable de negocio identificable como not purchasing receipt; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_security` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: not purchasing security. | Perfil digital |
| `not_purchasing_too_complicated` | categórica | Variable de negocio identificable como not purchasing too complicated; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_uncomfortable` | categórica | Variable de negocio identificable como not purchasing uncomfortable; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `not_purchasing_unfamiliar_vendor` | categórica | Atributo operacional del viaje de taxi: not purchasing unfamiliar vendor. | Movilidad |
| `registered_to_vote` | categórica | Variable de negocio identificable como registered to vote; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `sexual_preference` | categórica | Variable de negocio identificable como sexual preference; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `web_ordering` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: web ordering. | Perfil digital |
| `web_page_creation` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: web page creation. | Perfil digital |
| `who_pays_for_access_dont_know` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: who pays for access dont know. | Perfil digital |
| `who_pays_for_access_other` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: who pays for access other. | Perfil digital |
| `who_pays_for_access_parents` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: who pays for access parents. | Perfil digital |
| `who_pays_for_access_school` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: who pays for access school. | Perfil digital |
| `who_pays_for_access_self` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: who pays for access self. | Perfil digital |
| `willingness_to_pay_fees` | categórica | Variable de negocio identificable como willingness to pay fees; revisar distribución, codificación y relación con la variable objetivo o los segmentos. | Analizar en EDA |
| `years_on_internet` | categórica | Indicador de acceso, hábito, actitud o contexto declarado por usuarios de internet: years on internet. | Perfil digital |
| `who_pays_for_access_work` | categórica | Variable de referencia para perfilar segmentos: who pays for access work; no se usa para formar clusters. | Referencia externa |

### 4.3 Notas sobre Calidad de Datos

- Revisar faltantes, outliers, consistencia de codificación y cardinalidad antes del modelado.
- Tratar con cuidado variables sensibles, identificadores, fechas y campos de texto.
- Confirmar que la variable objetivo o de referencia se use de acuerdo con el tipo de problema.
- Registrar explícitamente qué columnas se excluyen y justificar si se eliminan por identificador, leakage, privacidad, baja utilidad o disponibilidad operacional.
- Mantener separación entre datos de entrenamiento y evaluación; toda imputación, codificación o escalamiento debe aprenderse solo con entrenamiento.

---

## 5. Plan de Análisis

### 5.1 Análisis Exploratorio de Datos (EDA)

Explorar distribuciones, cardinalidad, correlaciones, outliers, valores faltantes y relación entre variables clave y la decisión de negocio.

**Mínimo esperado:** incluir resumen de calidad de datos, distribución de la variable objetivo o de referencia, análisis de al menos cinco variables relevantes y tres hallazgos escritos en lenguaje de negocio.

### 5.2 Estadística Inferencial

Formular hipótesis de negocio y contrastarlas con pruebas apropiadas: chi-cuadrado, t-test, ANOVA, pruebas no paramétricas o intervalos de confianza según el tipo de variable.

**Mínimo esperado:** plantear al menos dos hipótesis verificables, mostrar el resultado estadístico y explicar si cambia alguna decisión del negocio.

### 5.3 Análisis Multivariante

Aplicar reducción dimensional, análisis de correlación, análisis de correspondencias, embeddings o mapas de segmentos para entender relaciones simultáneas.

**Mínimo esperado:** mostrar relaciones entre variables, redundancias, grupos de variables o patrones multivariados que ayuden a seleccionar features o interpretar segmentos.

### 5.4 Preparación del Dataset y Feature Engineering

Codificar categóricas, escalar numéricas, derivar variables temporales/geográficas, excluir identificadores y controlar leakage.

**Mínimo esperado:** explicar el pipeline final, listar variables eliminadas, describir transformaciones y justificar cualquier variable derivada.

### 5.5 Modelado Predictivo / Segmentación

**Tipo de problema:** Segmentación no supervisada
**Variable objetivo o referencia:** `who_pays_for_access_work`

Comparar K-Means/K-Prototypes, clustering jerárquico y HDBSCAN o Gower según mezcla de variables. Las variables de referencia no deben usarse para formar clusters.

**Mínimo esperado:** comparar alternativas, separar validación de entrenamiento, justificar la configuración final y explicar los errores, drivers o segmentos en términos de negocio.

---

## 6. Métricas de Éxito

| Métrica | Uso |
|---|---|
| Silhouette | Medir separación entre segmentos |
| Davies-Bouldin | Penalizar clusters solapados |
| Estabilidad por remuestreo | Validar que segmentos no dependan de una semilla |
| Perfilabilidad | Confirmar que cada cluster tenga rasgos de negocio claros |
| Accionabilidad | Traducir cada segmento a una estrategia concreta |

---

## 7. Entregables Esperados

1. Notebook reproducible con EDA, limpieza, preparación de variables y comparación de métodos de segmentación.
2. Justificación de variables usadas para formar clusters y variables excluidas o usadas solo para perfilar.
3. Comparación de al menos tres configuraciones o métodos de segmentación.
4. Perfil de cada segmento con tamaño, rasgos diferenciales, nombre de negocio y riesgos de interpretación.
5. Recomendación de acciones por segmento y forma de usar los segmentos en una decisión real.

### 7.1 Formato de Entrega

| Entregable | Contenido mínimo |
|---|---|
| Notebook técnico | Código ejecutable, EDA, limpieza, preparación, modelado o segmentación, métricas y conclusiones. |
| Resumen ejecutivo | Una página o sección final con problema, hallazgos, recomendación, impacto esperado y límites. |
| Tabla de variables usadas | Variables incluidas, excluidas y motivo de exclusión cuando aplique. |
| Evidencia de validación | Métricas, gráficos, matriz de confusión, residuales o perfiles de segmento según el caso. |
| Recomendación accionable | Decisión concreta para el stakeholder, priorización propuesta y riesgos de implementación. |

---

## 8. Criterios de Evaluación

| Criterio | Peso | Qué debe verse en la entrega |
|---|---:|---|
| Entendimiento del negocio | 15% | Problema formulado como decisión real, stakeholder claro y uso esperado de la solución. |
| Calidad y preparación de datos | 20% | Auditoría de faltantes, outliers, tipos, cardinalidad, leakage, variables excluidas y pipeline reproducible. |
| Análisis exploratorio e inferencial | 15% | Hallazgos visuales y estadísticos conectados con hipótesis de negocio, no solo gráficos descriptivos. |
| Modelado o segmentación | 25% | Comparación metodológica, validación correcta, métricas apropiadas y justificación técnica del resultado elegido. |
| Interpretación y recomendación | 20% | Drivers, errores o perfiles explicados en lenguaje de negocio, con acciones concretas y límites de uso. |
| Presentación reproducible | 5% | Notebook ordenado, código ejecutable, conclusiones visibles y anexos suficientes para revisar el trabajo. |

**Criterio específico del caso:** La evaluación debe incluir estabilidad, separación, perfilabilidad, tamaño de segmentos y acciones diferenciadas por segmento.

---

## 9. Checklist Antes de Entregar

- [ ] El notebook corre de inicio a fin sin depender de rutas absolutas personales.
- [ ] El dataset usado corresponde a `dataset.csv` del caso y la variable objetivo o referencia coincide con la metadata.
- [ ] Excluí identificadores, variables con leakage y campos que no estarían disponibles al momento de decidir.
- [ ] Documenté decisiones de limpieza, imputación, codificación y escalamiento.
- [ ] Confirmé que la variable de referencia no fue usada para construir clusters.
- [ ] Cada cluster tiene nombre de negocio, tamaño, rasgos diferenciales y acción recomendada.
- [ ] Incluí al menos tres hallazgos de negocio sustentados por datos.
- [ ] La recomendación final indica qué hacer, con quién hacerlo, por qué y con qué cautelas.
- [ ] La presentación ejecutiva puede leerse sin revisar el código.
