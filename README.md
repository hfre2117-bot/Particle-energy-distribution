# Particle-energy-distribution
We have data on particle energies and we want to plot an energy histogram and find the average energy.
import numpy as np
import matplotlib.pyplot as plt

# شبیه‌سازی داده‌ها (مثلاً انرژی ذرات)
n_events = 10000
mean_energy = 500  # MeV
sigma_energy = 100  # MeV

energies = np.random.normal(mean_energy, sigma_energy, n_events)

# رسم هیستوگرام
plt.hist(energies, bins=50, range=(0,1000), color='skyblue', edgecolor='black')
plt.title("Energy Distribution")
plt.xlabel("Energy [MeV]")
plt.ylabel("Counts")
plt.grid(True)
plt.show()

# محاسبه میانگین و انحراف معیار
mean = np.mean(energies)
sigma = np.std(energies)
print(f"Mean energy: {mean:.2f} MeV, Sigma: {sigma:.2f} MeV")
