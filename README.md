import matplotlib.pyplot as plt

# Definir la función de la regla de Cowling
def dosis_infantil(t, a):
    return ((t + 1) / 24) * a

# Valores de t (edad del niño)
edades = list(range(19))  # Edades de 0 a 18 años
dosis_adulto = 500  # Dosis de un adulto en mg

# Calcular las dosis infantiles para distintos valores de t y a = 500 mg
dosis_infantiles = [dosis_infantil(t, dosis_adulto) for t in edades]

# Graficar la función
plt.figure(figsize=(8, 6))
plt.plot(edades, dosis_infantiles, marker='o', linestyle='-')
plt.title('Dosis Infantil según la Edad del Niño (Dosis Adulto = 500 mg)')
plt.xlabel('Edad del Niño (años)')
plt.ylabel('Dosis Infantil (mg)')
plt.grid(True)
plt.show()
