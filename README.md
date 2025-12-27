# SIASIC-Santander: Sistema de Análisis Sísmico Integral

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Geopandas](https://img.shields.io/badge/Geopandas-0.14+-green.svg)](https://geopandas.org/)
[![Folium](https://img.shields.io/badge/Folium-0.15+-red.svg)](https://python-visualization.github.io/folium/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Sistema completo de análisis, visualización y exportación de datos sísmicos para la región de Santander, Colombia. Herramienta de investigación especializada en el estudio del Nido Sísmico de Bucaramanga.

## Descripción del Proyecto

SIASIC-Santander (Sistema de Análisis Sísmico Integral de Colombia - Santander) es una herramienta de investigación desarrollada para analizar y visualizar la actividad sísmica en el departamento de Santander, con énfasis especial en el fenómeno del Nido Sísmico de Bucaramanga, una zona de sismicidad intermedia única en el mundo.

### Características Principales

**Análisis de Datos Sísmicos**
- Clasificación automática de sismos por profundidad
- Identificación de eventos del Nido Sísmico de Bucaramanga (140-180 km)
- Análisis temporal y espacial de la sismicidad
- Procesamiento de datos de múltiples fuentes

**Visualizaciones Profesionales**
- Mapas interactivos de epicentros con Folium
- Gráficas estadísticas con Plotly y Matplotlib
- Visualización de patrones temporales
- Mapas de calor de concentración sísmica
- Análisis por profundidad y magnitud

**Exportación GIS**
- Shapefile (.shp) para ArcGIS Desktop/Pro
- GeoJSON para aplicaciones web
- KML para Google Earth
- CSV con coordenadas geográficas
- Archivos listos para ArcGIS Online

**Clasificación por Profundidad**
- Superficial: < 70 km
- Intermedio: 70-140 km
- Nido Sísmico: 140-180 km (zona de investigación)
- Profundo: > 180 km

## Contexto Geológico

### El Nido Sísmico de Bucaramanga

El Nido Sísmico de Bucaramanga es una zona de sismicidad intermedia (140-180 km de profundidad) localizada bajo el departamento de Santander. Este fenómeno geológico es de gran interés científico debido a:

- **Profundidad única**: Actividad sísmica concentrada a profundidades intermedias
- **Alta frecuencia**: Mayor cantidad de eventos sísmicos comparado con otras regiones
- **Importancia científica**: Uno de los pocos nidos sísmicos documentados en el mundo
- **Ubicación**: Región central de Santander (municipios de Los Santos, Zapatoca, Villanueva)

### Región de Estudio

**Área Geográfica:**
- Departamento: Santander, Colombia
- Zona focal: Nido Sísmico de Bucaramanga
- Cobertura: Región centro-oriental de Colombia
- Coordenadas aproximadas: 6.5°N - 7.5°N, 72.5°W - 73.5°W

## Estructura del Proyecto

```
siasic-santander/
├── README.md                      # Este archivo
├── LICENSE                        # Licencia MIT
├── .gitignore                     # Exclusiones de Git
├── requirements.txt               # Dependencias Python
└── SIASIC_Santander_Analisis.ipynb  # Notebook principal de análisis
```

## Stack Tecnológico

### Librerías Core

```
Python 3.8+
├── Procesamiento de Datos
│   ├── pandas
│   ├── numpy
│   └── datetime
├── Visualización
│   ├── matplotlib
│   ├── seaborn
│   ├── plotly
│   └── folium
├── Análisis Geoespacial
│   ├── geopandas
│   ├── shapely
│   └── pyshp
└── Utilidades
    └── warnings
```

### Capacidades GIS

- **Geopandas**: Manipulación de datos geoespaciales
- **Shapely**: Geometrías y operaciones espaciales
- **Folium**: Mapas interactivos web
- **Pyshp**: Creación de Shapefiles

## Instalación y Uso

### Opción 1: Google Colab (Recomendado)

El notebook está optimizado para Google Colab:

1. Abrir el archivo `SIASIC_Santander_Analisis.ipynb` en Google Colab
2. Ejecutar la primera celda para instalar dependencias
3. Ejecutar todas las celdas secuencialmente
4. Descargar los archivos generados

### Opción 2: Instalación Local

```bash
# Clonar repositorio
git clone https://github.com/Daniromero1410/siasic-santander.git
cd siasic-santander

# Crear entorno virtual
python -m venv venv
source venv/bin/activate  # Linux/Mac
# o
venv\Scripts\activate  # Windows

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar Jupyter Notebook
jupyter notebook SIASIC_Santander_Analisis.ipynb
```

## Funcionalidades Principales

### 1. Carga y Procesamiento de Datos

```python
# Carga automática de datos sísmicos
# Procesamiento de fechas y coordenadas
# Clasificación por profundidad
# Extracción de información geográfica
```

**Datos procesados:**
- Coordenadas geográficas (latitud, longitud)
- Profundidad hipocentral
- Magnitud y tipo de magnitud
- Fecha y hora del evento
- Municipio y departamento
- Clasificación por profundidad

### 2. Visualizaciones Generadas

**Mapas Interactivos**
- Mapa de epicentros con clasificación por profundidad
- Mapa de calor de concentración sísmica
- Visualización de municipios afectados

**Gráficas Estadísticas**
- Distribución temporal de sismos
- Análisis por profundidad
- Distribución por magnitud
- Análisis por municipio
- Tendencias mensuales

**Gráficas de Investigación**
- Perfil de profundidad vs. magnitud
- Análisis del Nido Sísmico
- Comparación Santander vs. otras regiones

### 3. Exportación de Datos

**Formatos GIS disponibles:**

```bash
# Archivos generados automáticamente:
├── santander_sismos_2024.shp      # Shapefile completo
├── santander_sismos_2024.dbf      # Base de datos
├── santander_sismos_2024.shx      # Índice espacial
├── santander_sismos_2024.prj      # Proyección (WGS84)
├── santander_sismos_2024.geojson  # GeoJSON
├── santander_sismos_2024.kml      # Google Earth
└── santander_sismos_2024.csv      # CSV con coordenadas
```

**Uso en ArcGIS:**
1. Abrir ArcGIS Pro/Desktop
2. Agregar datos → Shapefile
3. Seleccionar `santander_sismos_2024.shp`
4. Listo para análisis espacial

**Uso en QGIS:**
1. Capa → Añadir capa vectorial
2. Seleccionar `santander_sismos_2024.shp` o `.geojson`
3. Aplicar simbología por profundidad

## Metodología de Análisis

### 1. Adquisición de Datos

**Fuentes:**
- Red Sismológica Nacional de Colombia (RSNC)
- Servicio Geológico Colombiano (SGC)
- Observatorios regionales

**Período de análisis:**
- Año 2024 (actualizado continuamente)
- Eventos con magnitud ≥ 4.0

### 2. Procesamiento

**Filtrado:**
- Eliminación de eventos duplicados
- Validación de coordenadas
- Verificación de profundidades

**Clasificación:**
- Asignación de categoría de profundidad
- Identificación de región (Santander/otras)
- Extracción de información municipal

### 3. Análisis Estadístico

**Métricas calculadas:**
- Frecuencia de eventos por mes
- Distribución de magnitudes
- Concentración espacial
- Profundidad promedio por zona

### 4. Visualización

**Mapas:**
- Sistema de coordenadas: WGS84 (EPSG:4326)
- Simbología por profundidad
- Tamaño proporcional a magnitud

## Resultados de Investigación

### Estadísticas 2024

**Total de eventos analizados:** 51 sismos  
**Eventos en Santander:** 34 (66.7%)  
**Eventos del Nido Sísmico:** 35 (68.6%)

**Distribución por Profundidad:**
- Nido Sísmico (140-180 km): 35 eventos
- Intermedio (70-140 km): 6 eventos
- Superficial (< 70 km): 10 eventos

**Magnitudes:**
- Rango: 4.0 - 5.1
- Magnitud promedio: 4.3
- Evento más fuerte: M 5.1 (Tarazá)

**Municipios más afectados:**
1. Los Santos - 13 eventos
2. Zapatoca - 10 eventos
3. Otros municipios de Santander

### Observaciones Clave

1. **Concentración en Nido Sísmico**: 68.6% de los eventos ocurren entre 140-180 km
2. **Actividad constante**: Eventos distribuidos durante todo el año
3. **Zona focal**: Municipios de Los Santos y Zapatoca
4. **Magnitudes moderadas**: La mayoría entre M 4.0 - 4.5

## Aplicaciones

### Investigación Científica
- Estudio del Nido Sísmico de Bucaramanga
- Análisis de patrones de sismicidad
- Investigación geofísica regional

### Gestión de Riesgo
- Identificación de zonas de alta actividad
- Monitoreo de tendencias sísmicas
- Apoyo a planes de emergencia

### Educación
- Material didáctico para geociencias
- Visualización de fenómenos sísmicos
- Divulgación científica

### Planificación Territorial
- Insumos para mapas de amenaza sísmica
- Información para uso de suelo
- Datos para estudios de vulnerabilidad

## Contribuciones al Conocimiento

### Aspectos Innovadores

1. **Sistema Integrado**: Combina análisis, visualización y exportación
2. **Enfoque Regional**: Especializado en Santander y Nido Sísmico
3. **Automatización**: Procesamiento automático de datos
4. **Interoperabilidad**: Múltiples formatos de exportación GIS

### Publicaciones y Difusión

Este proyecto genera insumos para:
- Artículos científicos sobre el Nido Sísmico
- Informes técnicos de sismicidad regional
- Material educativo sobre geociencias
- Bases de datos públicas de sismicidad

## Limitaciones y Trabajo Futuro

### Limitaciones Actuales

- Datos limitados a eventos M ≥ 4.0
- Cobertura temporal de un año (2024)
- Dependencia de fuentes públicas de datos
- Sin análisis de mecanismos focales

### Desarrollos Futuros

**Corto plazo:**
- Ampliación de base de datos histórica
- Integración de más fuentes de datos
- Análisis de series temporales
- Dashboard interactivo web

**Mediano plazo:**
- Modelos predictivos de sismicidad
- Análisis de clustering espacial
- Integración con datos geológicos
- API para acceso a datos

**Largo plazo:**
- Sistema de monitoreo en tiempo real
- Alertas automáticas
- Integración con redes sociales
- Aplicación móvil

## Referencias

### Datos Sísmicos

- Red Sismológica Nacional de Colombia (RSNC)
- Servicio Geológico Colombiano (SGC)
- USGS Earthquake Catalog

### Literatura Científica

- Schneider et al. (1987): "The Bucaramanga Nest, Colombia"
- Cortés & Angelier (2005): "Current states of stress in the northern Andes"
- Vargas & Mann (2013): "Tearing and Breaking Off of Subducted Slabs"
- SGC (2020): "Mapa de Amenaza Sísmica de Colombia"

## Autor

**Daniel Romero**  
Ingeniero de Software 

**Afiliación:**  
Universidad de Santander (UDES)  
Bucaramanga, Santander, Colombia

**Contacto:**  
- Email: danielromero.software@gmail.com
- LinkedIn: [daniromerosoftware](https://www.linkedin.com/in/daniromerosoftware)
- GitHub: [Daniromero1410](https://github.com/Daniromero1410)

## Agradecimientos

- Servicio Geológico Colombiano por los datos sísmicos
- Red Sismológica Nacional de Colombia
- Universidad de Santander (UDES)
- Comunidad científica dedicada al estudio del Nido Sísmico de Bucaramanga

## Licencia

MIT License - Ver archivo LICENSE para detalles

Este software se proporciona con fines de investigación y educación. Los datos sísmicos son propiedad de sus fuentes originales y están sujetos a sus respectivas licencias.

## Citación

Si utiliza este proyecto en su investigación, por favor cite:

```bibtex
@software{romero2024siasic,
  author = {Romero, Daniel},
  title = {SIASIC-Santander: Sistema de Análisis Sísmico Integral},
  year = {2025},
  publisher = {GitHub},
  journal = {Repositorio GitHub},
  howpublished = {\url{https://github.com/Daniromero1410/siasic-santander}}
}
```

---

**Versión:** 2.0  
**Última actualización:** Diciembre 2025 
**Estado:** En desarrollo activo  
**Tipo:** Proyecto de Investigación
