# Series de Tiempo — Universidad Javeriana Cali
### Maestría en Ciencia de Datos
**Autor:** Juan Sebastian Torres Romero

---

## Descripción

Este repositorio contiene los talleres del curso de Análisis de Series de Tiempo. Cada entregable aplica métodos progresivamente más sofisticados sobre la serie mensual de **personas Ocupadas (miles) en las 13 principales ciudades de Colombia** (enero 2001 – junio 2019, 222 observaciones).

Los datos provienen del repositorio del curso:
```
https://raw.githubusercontent.com/dagudelo30/Series-de-tiempo---Javeriana-Cali/main/intro-moving_average/datosEmpleo.xlsx
```

---

## Estructura

```
├── taller1/
│   ├── notebook_taller1.ipynb   # Promedio Móvil (MA)
│   └── informe_taller1.pdf      # Informe — máx. 1 página
│
├── taller2/
│   ├── notebook_taller2.ipynb   # Suavización Exponencial Holt-Winters
│   └── informe_taller2.pdf      # Informe — máx. 1 página
│
└── taller3/
    ├── notebook_taller3.ipynb   # Comparación de modelos + validación de supuestos
    └── informe_taller3.pdf      # Informe — máx. 1 página
```

---

## Resumen de resultados

| Taller | Métodos evaluados | Mejor modelo | RMSE |
|--------|-------------------|--------------|------|
| Taller 1 | Promedio Móvil MA(2, 3, 4, 5) | MA(2) | 169.19 |
| Taller 2 | SES, Holt, HW Aditivo, HW Multiplicativo | HW ETS(A,A,M) | 59.64 |
| Taller 3 | Regresión lineal, cuadrática, estacional, tend+estac, HW | HW ETS(A,A,M) | 59.64 |

El modelo Holt-Winters Multiplicativo con tendencia **ETS(A,A,M)** se consolida como el mejor pronóstico a lo largo de los tres entregables, con un RMSE de **59.64** sobre el periodo de prueba (ene–jun 2019).

### Pronóstico final jul–dic 2019 — HW ETS(A,A,M)

| Mes | Pronóstico (miles) | LI 95% | LS 95% |
|-----|--------------------|--------|--------|
| Jul-2019 | 10.898 | 10.683 | 11.136 |
| Ago-2019 | 10.915 | 10.658 | 11.158 |
| Sep-2019 | 10.994 | 10.723 | 11.265 |
| Oct-2019 | 11.132 | 10.852 | 11.432 |
| Nov-2019 | 11.151 | 10.831 | 11.464 |
| Dic-2019 | 11.064 | 10.727 | 11.375 |

---

## Dependencias

```python
numpy
pandas
matplotlib
statsmodels
scikit-learn
scipy
openpyxl
```

Instalación:
```bash
pip install numpy pandas matplotlib statsmodels scikit-learn scipy openpyxl
```

---

## Profesor

Diego Fernando Agudelo — Universidad Javeriana Cali
