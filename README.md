# soc-ia

Sistema de Optimización de Centros Ambulatorios basado en Inteligencia Artificial.
Prototipo desarrollado como Trabajo Fin de Máster del Máster en Aplicaciones de
Inteligencia Artificial en Salud (CEMP, España, 2025-2026).

## Problema

Asignación óptima de box/recinto, profesional y bloque horario en un Centro de
Especialidades Ambulatorias Adosado (CEAA) del sistema de salud chileno. El
escenario de trabajo es una unidad cardiovascular (ecocardiografía, Holter y
prueba de esfuerzo). El problema está documentado en el desafío ECO-SD #11
(Hospital San José de Melipilla).

SOC-IA no prioriza listas de espera: consume esa información desde sistemas
externos de priorización y se concentra en el uso y la asignación de espacios clínicos.

## Aviso sobre los datos

**Todos los datos de este repositorio son sintéticos.** Se generaron con parámetros
estándar provisorios (`parametros.yaml`, marcados como ESTÁNDAR_PROVISORIO) y con la
misma estructura que tendrían datos operacionales reales. Los resultados del EDA
muestran el comportamiento del modelo con esos parámetros, **no hallazgos reales de
ningún establecimiento**. Este repositorio no contiene datos de pacientes ni datos
institucionales.

## Contenido

| Elemento | Descripción |
|---|---|
| `parametros.yaml` | Parámetros del generador (estándar provisorio) |
| `ceaa_dataset.csv` | Dataset sintético de operación semanal de boxes |
| `01_...ipynb` | Generación del dataset sintético |
| `02_EDA_CEAA.ipynb` | Análisis exploratorio (ocupación, subutilización, brechas) |
| `figuras/` | Gráficos generados por el EDA |

## Hoja de ruta

- [x] Fase 1: dataset sintético y EDA
- [ ] Fase 2A: optimizador MILP (PuLP)
- [ ] Fase 2B: simulación de escenarios (SimPy)
- [ ] Fase 3: clasificador de brecha y regresor de horas (con SHAP)
- [ ] Fase 4: aplicación Streamlit
- [ ] Fase 5: validación

## Nivel de madurez

El TFM alcanza TRL 3-5. El cierre de brecha hacia TRL 5-9, exigido por el desafío
ECO-SD, corresponde a la etapa posterior al TFM.

## Stack

Python · Google Colab · PuLP · SimPy · scikit-learn · SHAP · Streamlit

## Autoría

© 2026 Paula Belmar. Todos los derechos reservados Santiago, Chile
