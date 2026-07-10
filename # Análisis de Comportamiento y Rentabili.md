# Análisis de Comportamiento y Rentabilidad: ConnectaTel

Este proyecto consiste en un análisis exhaustivo de los datos de usuarios de ConnectaTel para entender el comportamiento de consumo y la rentabilidad de sus diferentes planes de telefonía.

## 🎯 Objetivo del Proyecto
El objetivo principal es determinar qué plan (Básico o Premium) resulta más rentable para la compañía y si existen diferencias estadísticamente significativas en los ingresos generados por los usuarios según su ubicación geográfica (NY-NJ vs. otras regiones), con el fin de proporcionar recomendaciones estratégicas basadas en datos.

## 📊 Datasets Utilizados
El análisis se realizó utilizando la siguiente estructura de datos:
* `users`: Información demográfica de los clientes (edad, ciudad, fecha de registro, plan).
* `calls`: Registro detallado de llamadas (duración, fecha).
* `messages`: Registro de mensajes de texto enviados.
* `internet`: Registro de sesiones de consumo de datos.
* `plans`: Detalles técnicos y costos de cada plan (cuotas base, límites, costo por exceso).

## 🚀 Etapas del Análisis
1. **Preprocesamiento de datos:** Limpieza de valores nulos, corrección de tipos de datos (fechas, numéricos) y eliminación de registros inconsistentes.
2. **Ingeniería de variables:** Agregación de consumos mensuales por usuario para obtener métricas consolidadas (minutos, mensajes y datos).
3. **Cálculo de ingresos:** Desarrollo de una función de facturación para calcular el ingreso mensual total por usuario, incluyendo pagos base y recargos por uso excedente.
4. **Análisis Exploratorio (EDA):** Visualización de distribuciones de consumo y detección de *outliers* mediante histogramas y diagramas de caja (*boxplots*).
5. **Análisis Estadístico:** Aplicación de pruebas de hipótesis (T-Student) para validar si existen diferencias significativas en los ingresos entre planes y regiones.
6. **Insight Ejecutivo:** Elaboración de recomendaciones comerciales accionables para los *stakeholders*.

## 💻 Cómo ejecutar el Notebook
Este proyecto ha sido desarrollado en Python. Para ejecutarlo, puedes utilizar **Google Colab**:

1. Sube el archivo `.ipynb` a tu unidad de **Google Drive**.
2. Asegúrate de tener los archivos CSV en la misma carpeta o actualiza las rutas de carga (`pd.read_csv(...)`).
3. Abre el archivo desde **Google Colab**.
4. Ejecuta las celdas en orden (de arriba a abajo) para asegurar que las variables se carguen correctamente.

## ⚙️ Guía de Reproducción
Para ejecutar el análisis sin errores, asegúrate de tener instaladas las siguientes librerías:

```bash
pip install pandas seaborn matplotlib scipy numpy