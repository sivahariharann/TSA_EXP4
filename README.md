# Ex.No:04   FIT ARMA MODEL FOR TIME SERIES
# Date: 11-03-2026



### AIM:
To implement ARMA model in python.
### ALGORITHM:
1. Import necessary libraries.
2. Set up matplotlib settings for figure size.
3. Define an ARMA(1,1) process with coefficients ar1 and ma1, and generate a sample of 1000

data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

4. Display the autocorrelation and partial autocorrelation plots for the ARMA(1,1) process using
plot_acf and plot_pacf.
5. Define an ARMA(2,2) process with coefficients ar2 and ma2, and generate a sample of 10000

data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

6. Display the autocorrelation and partial autocorrelation plots for the ARMA(2,2) process using
plot_acf and plot_pacf.
### PROGRAM:
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.arima_process import ArmaProcess
from statsmodels.graphics.tsaplots import plot_acf
from statsmodels.graphics.tsaplots import plot_pacf
plt.rcParams["figure.figsize"] = (12,6)
plt.plot(date, volume)
plt.title("Original Data")
plt.xlabel("Date")
plt.ylabel("Volume")
ar1 = np.array([1, -0.6])
ma1 = np.array([1, 0.4])
arma1 = ArmaProcess(ar1, ma1)
sample1 = arma1.generate_sample(nsample=1000)
plt.plot(sample1)
plt.title("Simulated ARMA(1,1) Process")
plt.xlim(0,1000)
plt.show()
ar2 = np.array([1, -0.5, 0.25])
ma2 = np.array([1, 0.4, 0.3])
arma2 = ArmaProcess(ar2, ma2)
sample2 = arma2.generate_sample(nsample=10000)
plt.plot(sample2)
plt.title("Simulated ARMA(2,2) Process")
plt.xlim(0,10000
plt.show()
plot_pacf(volume)
plt.title("Partial Autocorrelation of Original data PACF ")
plot_pacf(sample1)
plt.title("Partial Autocorrelation - ARMA(1,1)")
plt.show()
plt.show()
plot_acf(sample1)
plt.title("Autocorrelation - ARMA(1,1)")
plt.show()
plot_acf(sample2)
plt.title("Autocorrelation - ARMA(2,2)")
plt.show()
plot_pacf(sample2)
plt.title("Partial Autocorrelation - ARMA(2,2)")
plt.show()
```
OUTPUT:

ORIGINAL DATA:
<img width="1001" height="547" alt="image" src="https://github.com/user-attachments/assets/db732155-0d0f-435a-ba60-5bf245de2e76" />

SIMULATED ARMA(1,1) PROCESS:
<img width="997" height="528" alt="image" src="https://github.com/user-attachments/assets/538fc623-5cbe-4b64-a036-ba8e6518a793" />



Partial Autocorrelation
<img width="1002" height="528" alt="image" src="https://github.com/user-attachments/assets/7110f9d6-e246-4b94-8126-fecea0bc0ad8" />

Autocorrelation
<img width="1002" height="528" alt="image" src="https://github.com/user-attachments/assets/8893ebf5-8027-4769-b427-a80ed4f04d80" />




SIMULATED ARMA(2,2) PROCESS:
<img width="1002" height="528" alt="image" src="https://github.com/user-attachments/assets/4e1e87cd-bac7-4458-a0e1-8e42c616f957" />

Partial Autocorrelation
<img width="1002" height="528" alt="image" src="https://github.com/user-attachments/assets/996ccebd-a0d3-405f-9b83-671895149d7d" />



Autocorrelation
<img width="1002" height="528" alt="image" src="https://github.com/user-attachments/assets/05856c4c-9026-4681-ac5a-2e45feb5a0fd" />

RESULT:
Thus, a python program is created to fir ARMA Model successfully.
