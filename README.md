# Ex.-2-Lab-Experiment-Time-Series-Analysis-and-Decomposition

## Name: PREM PRASANTH J

## Roll no: 2305001028

## Department: CSE

## AIM

To perform time series analysis and decomposition on the monthly average temperature of a city using Python. We will use simple sample temperature data for 12 months and decompose it into:

Observed = Trend + Seasonal + Residual

## PROGRAM

### i) Python Code

```python
import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose

sales_data = [
    120, 115, 130, 140, 150, 160,
    155, 165, 175, 180, 210, 250
]

dates = pd.date_range(start="2025-01-01", periods=12, freq="ME")

data = pd.Series(sales_data, index=dates)

print("Monthly E-Commerce Sales ($1k):")
print(data)

plt.figure(figsize=(10, 5))
plt.plot(data.index, data.values, marker="o", color="blue")
plt.title("Monthly E-Commerce Sales Analysis")
plt.xlabel("Month")
plt.ylabel("Sales ($1,000s)")
plt.grid(True)
plt.show()

# Decompose time series
result = seasonal_decompose(data, model="additive", period=12)
result.plot()
plt.show()
```

## OUTPUT
<img width="940" height="712" alt="image" src="https://github.com/user-attachments/assets/5dc79a1e-7889-415f-8317-cf3aa4cccd2d" />

## RESULT

Thus, the time series data were successfully analyzed and decomposed using Python. The observed data were separated into trend, seasonal, and residual components using the seasonal decomposition method.
