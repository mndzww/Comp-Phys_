import matplotlib.pyplot as plt
import numpy as np
import time

# Global Var.
t_min = 0
t_max = 20
a = 10
b = 1

# Initial Var. (Numeric)
dt = 0.1
Nstep = int((t_max - t_min) / dt)
t = np.linspace(t_min, t_max, Nstep)
v_numeric = np.zeros(Nstep)
v_numeric[0] = 0  # Initial velocity

# Euler Method for solving dv/dt = a - b*v
for i in range(Nstep - 1):
    v_numeric[i + 1] = v_numeric[i] + (a - b * v_numeric[i]) * dt

# Initial Var. (Analytic)
Ngrid = 200
T_a = np.linspace(t_min, t_max, Ngrid)
v_analytic = a / b * (1 - np.exp(-b * T_a))

# Plot both Numeric and Analytic
plt.plot(t, v_numeric, label='Numeric Solution')
plt.plot(T_a, v_analytic, '--r', label='Analytic Solution')
plt.xlabel('Time (s)')
plt.ylabel('Velocity (m/s)')
plt.title('Velocity vs Time (Frictional Force with Velocity-dependent Coefficient)')
plt.legend()
plt.grid(True)
plt.show()
