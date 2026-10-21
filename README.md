# Inflación en Argentina, 2017-2026

Análisis de la inflación mensual e interanual en Argentina con el IPC nivel general nacional del INDEC.

## Por qué hice este análisis

Quería entender cómo evolucionó la inflación en Argentina en los últimos 9 años y qué tan extremo fue el pico de 2023-2024 comparado con el resto del período. Usé datos oficiales para reconstruir la serie completa y mirar dos medidas: la variación mensual y la interanual.

Lo que más me llamó la atención es que, aunque la inflación bajó muchísimo desde el máximo, el promedio mensual de 2026 (2,4%) sigue siendo más alto que el de 2017 (1,9%).

## Datos

- **Fuente:** API de series de tiempo del Gobierno argentino (datos.gob.ar), que publica las series del INDEC.
- **Serie:** `148.3_INIVELNAL_DICI_M_26`, IPC nivel general nacional, base diciembre 2016.
- **Período:** enero 2017 a agosto 2026 (116 meses, sin meses faltantes).



## Hallazgos principales

- El pico de inflación mensual fue en **diciembre de 2023**, con **25,5%** en un solo mes.
- La inflación interanual tocó su máximo en **abril de 2024**, con **289,4%**.
- El promedio mensual pasó de 1,9% en 2017 a 10,0% en 2023, y bajó a 2,3% en 2025.
- El último dato disponible es **33,5% interanual en agosto de 2026**.



## Cómo correrlo

Necesitás Python 3.12 y Git. En la terminal:

```
git clone https://github.com/joaco3250/inflacion-argentina.git
cd inflacion-argentina
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
jupyter notebook analisis.ipynb
```

Después ejecutá todas las celdas de arriba hacia abajo. (En Mac o Linux, el paso de activación es `source .venv/bin/activate`.)

## Limitaciones

- Solo usa el IPC nivel general nacional: no distingue rubros ni regiones.
- El promedio anual es un promedio simple de los meses, y 2026 es un año parcial.



## Herramientas

Hecho con Python, pandas y matplotlib.