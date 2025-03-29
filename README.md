# Predicción de precios de acciones mediante simulación estocástica: Aplicación de cadenas de Markov y métodos de Monte Carlo

Este proyecto implementa un modelo estocástico para simular la evolución futura del precio de acciones bursátiles, utilizando el Movimiento Geométrico Browniano (MGB) y el método de simulación de Monte Carlo. El enfoque está orientado a la predicción de trayectorias probables bajo incertidumbre, y ha sido validado con datos reales de empresas como Apple (AAPL), Microsoft (MSFT) y Google (GOOGL).

---

## Características

- Descarga automática de datos históricos desde Yahoo Finance.
- Estimación de parámetros estadísticos a partir de retornos logarítmicos.
- Simulación de trayectorias usando Monte Carlo y Euler-Maruyama.
- Visualización de trayectorias con bandas de confianza.
- Mapas de calor de densidad de trayectorias.
- Análisis de volatilidad y métricas de error (MAE y RMSE).

## Requisitos

- Python ≥ 3.7
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `yfinance`

Puedes instalar las dependencias con:

```bash
pip install -r requirements.txt
```

## Uso del modelo

``` bash
from montecarlo_predictor import MonteCarloStockPredictor

predictor = MonteCarloStockPredictor(
    ticker='AAPL',
    start_date='2020-01-01',
    end_date='2024-01-01',
    end_prediction_date='2025-01-01',
    num_simulations=10000
)

predictor.simulate()
predictor.plot_simulation()
predictor.heat_plot_simulation()
predictor.analyze_volatility()
predictor.evaluate_prediction_accuracy()

```