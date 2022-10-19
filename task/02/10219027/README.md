# 10219027
Syafitra Salam


## materi sebelumnya
Metode Runge-Kutta Orde-4, Metode Euler, Transformasi Fourier, Metode Monte-Carlo


## materi paling menarik
+ Materi Runge-Kutta orde-4, hal ini disebabkan metode ini dapat menyelesaikan berbagai permasalah di Fisika yang berkaitan dengan persamaan diferensial yang diubah ke dalam bentuk numerik. Pendekatan yang dilakukan juga sesuai dengan hasil analitik.


## materi paling membosankan
+ Materi transformasi Fourier karena materi ini hanya bisa diaplikasikan pada permasalahan Fisika yang berkaitan dengan sinyal atau persamaan lainnya yang saling invers. Keterbatasan pengaplikasiannya membuat materi ini kurang menarik. Selain itu, materi ini juga sulit untuk dipahami.


## materi yang sudah dipami
+ Runge-Kutta, Euler, Monte-Carlo karena materi ini sangat sederhana sehingga mudah dipahami. Pengaplikasiannya juga jelas dan dapat memodelkan berbagai permasalahan Fisika yang cukup jelas seperti sistem pegas.


## materi yang belum dipahami
+ Transformasi Fourier karena materi ini cukup rumit. Pengaplikasiannya di dunia Fisika juga kurang.


## contoh program
+ Buat suatu contoh program dalam Python dan sertakan di sini dengan hasil keluarnnya.

```python
# contoh program python
import matplotlib.pyplot as plt
import numpy as np

def rk4(r, t, h): 
  k1 = h*f(r, t)
  k2 = h*f(r+0.5*k1, t+0.5*h)
  k3 = h*f(r+0.5*k2, t+0.5*h)
  k4 = h*f(r+k3, t+h)
  return (k1 + 2*k2 + 2*k3 + k4)/6

def f(r, t):
  alpha = 10
  beta = 0.001
  gamma = 2
  delta = 0.002
  x, y = r[0], r[1]
  fxdot = x*(alpha - beta*y)
  fydot = -y*(gamma - delta*x)
  return np.array([fxdot, fydot], float)

h=0.005
tpoints = np.arange(0, 3000, 1)
xpoints, ypoints = [], []
r = np.array([100, 3000], float)

for t in tpoints:
  xpoints.append(r[0])
  ypoints.append(r[1]) 
  r += rk4(r, t, h)

plt.plot(tpoints, xpoints)
plt.plot(tpoints, ypoints)
plt.xlabel("Time")
plt.ylabel("Population")
plt.title("Predator-Prey using Runge-Kutta 4")
plt.savefig("Predator-Prey Runge-Kutta 4.png")
plt.show()
print(xpoints[0])

Hasilnya adalah

![PR SPSF](https://user-images.githubusercontent.com/113664571/196596097-647fa6a3-547e-4afd-a246-a4c6c8d8eefb.PNG)

```
```


## cara perkuliahan
+ Menurut saya perkuliahan sudah berjalan dengan baik. Hanya saja, akses ke COMLABS masih sulit di awal semester hingga sekarang.


## topik sistem fisis
+ Topik sistem fisis yang menurut saya menarik untuk dikaji adalah molecular dynamics dan density functional theory karena kedua sistem fisis ini berkaitan dengan topik yang sedang saya kerjakan pada tugas akhir. Selain itu, kedua topik ini dapat memodelkan pergerakan molekul (molecular dynamics) dan memberikan gambaran densitas dan bandstructure dari material (DFT).


## simulasi dan visualisasi
+ Topik yang ingin saya simulasi dan visualisasikan adalah density functional theory karena topik ini menurut dapat menentukan sifat-sifat material seperti densitas, bandstructure, vibrasi fonon dan lain sebagainya. Hasil perhitungan ini berkaitan dan akan membantu topik tugas akhir saya jika bisa saya simulasikan. Beberapa pustaka python yang mungkin akan saya gunakan adalah matplotlib.org, numpy, dan DFTpy
