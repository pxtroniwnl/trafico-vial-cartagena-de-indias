# 🚦 Sistema Inteligente de Alerta de Tráfico Vehicular - Cartagena (Fase 1)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![OSMnx](https://img.shields.io/badge/Library-OSMnx-orange.svg)](https://osmnx.readthedocs.io/)
[![Computer Vision](https://img.shields.io/badge/AI-Computer%20Vision-green.svg)](https://roboflow.com/)

Este repositorio contiene la **Fase 1** de un proyecto integral diseñado para monitorear, analizar y alertar sobre el estado del tráfico vehicular en puntos estratégicos de Cartagena de Indias. 

## 📌 Visión del Proyecto
El objetivo es construir un sistema de alerta temprana que combine la rigurosidad de la **Teoría de Grafos** con la precisión de la **Inteligencia Artificial (Visión Artificial)**, superando las limitaciones de los datos públicos actuales.

---

## 🏗️ Roadmap del Proyecto

### Fase 1: Identificación de Puntos Críticos (Estado Actual)
Debido a la baja granularidad de los datos públicos (datos agregados en PowerBI o peajes que no representan la realidad urbana), hemos optado por un **Análisis de Grafos** de la infraestructura vial.
- **Metodología:** Modelado de la red vial de Cartagena como un Multidígrafo usando `OSMnx`.
- **Análisis:** Uso de *Betweenness Centrality* para detectar cuellos de botella matemáticos donde el flujo colapsa obligatoriamente.
- **Resultado:** Selección de los 10 puntos neurálgicos donde se recolectará data primaria.

### Fase 2: Recolección de Datos con Visión Artificial
Dada la falta de datasets públicos confiables para puntos específicos como Ternera o la Bomba del Amparo, se propone:
- **Dataset Custom:** Creación de un dataset propio mediante capturas en campo (cámaras de dispositivos móviles y futuras cámaras especializadas).
- **Anotación:** Uso de la plataforma **Roboflow** para el etiquetado de vehículos, motos y peatones.
- **Modelado:** Entrenamiento de modelos de detección (YOLO/Object Detection) para cuantificar la densidad vehicular en tiempo real.

### Fase 3: Sistema de Alerta y Dashboard de Control
- **Entrega de Valor:** Desarrollo de un Dashboard interactivo para las autoridades de tránsito.
- **Acción:** Generación de alertas automáticas cuando el modelo de IA detecte niveles de congestión superiores al umbral crítico.
- **Muestra al Público:** Interfaz accesible para el ciudadano cartagenero.

---

## 🛠️ Stack Tecnológico (Fase 1)
- **Modelado de Red:** `OSMnx` & `OpenStreetMap`.
- **Cómputo de Alta Eficiencia:** `NetworKit` (Algoritmo de Brandes paralelizado).
- **Análisis de Datos:** `Pandas` y `NumPy`.
- **Próximamente:** `Roboflow` y modelos de IA para Visión Artificial.

## 📍 Análisis de Ubicaciones (Basado en Grafos)
El modelo actual ha identificado los siguientes puntos como los candidatos ideales para la fase de recolección de imágenes (Visión Artificial):

| Ranking | Punto Estratégico | Importancia | Acción Sugerida |
| :--- | :--- | :--- | :--- |
| 1 | **Bomba del Amparo** | 0.1598 | Instalación de cámara de prueba |
| 2 | **Sector Ternera / Diagonal 32** | 0.1342 | Monitoreo de flujo de entrada |
| 3 | **Sector Bazurto** | 0.0895 | Análisis de congestión mixta |
| ... | ... | ... | ... |

---
