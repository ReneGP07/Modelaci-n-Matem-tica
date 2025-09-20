<h1 align="center">📐 Modelación Matemática con Python & PuLP</h1>

<p align="center">
Ejercicios y soluciones que uso para mis clases en FIME-UANL y como bitácora rumbo a mi 
<strong>Maestría en Ciencias con enfoque en Inteligencia Artificial y Optimización</strong>.
Todo es reproducible, con código comentado y validaciones claras.
</p>

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white">
  <img alt="Jupyter" src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white">
  <img alt="PuLP" src="https://img.shields.io/badge/OR-Tools-PuLP-0078D4">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-green">
</p>

---

## 🧭 Tabla de contenido
- [Qué hay aquí](#-qué-hay-aquí)
- [Estructura](#-estructura)
- [Instalación rápida](#-instalación-rápida)
- [Cómo correr](#-cómo-correr)
- [Datos (OP / TSP)](#-datos-op--tsp)
- [Estilo de trabajo](#-estilo-de-trabajo)
- [Roadmap](#-roadmap)
- [Contribuir](#-contribuir)
- [Autor](#-autor)
- [Licencia](#-licencia)

---

## 🗂️ Qué hay aquí
- **`TSP.ipynb`** — Viajante: Held-Karp (DP) y modelo MTZ (ILP con PuLP).
- **`SetCovering.ipynb`** — Set Covering con variables enteras.
- **`OrienteeringProblem.ipynb`** — Orienteering con presupuesto y premios.
- **`JSSP.ipynb`** — Job Shop Scheduling (formulación base + ejemplo).
- **`PULPPackage.ipynb`** — Mini-guía de PuLP (vars, restricciones, solver).
- **`Tarea1_Modelacion_Matematica.ipynb`** — Tarea 1 resuelta (modelo+validación+gráficas).
- **`Tarea2_Modelacion_Matematica.ipynb`** — Tarea 2 resuelta (holguras, restricciones activas).
- **PDFs** (`Intro_OptCO.pdf`, `MetodosPL.pdf`, `Prog_Entera.pdf`, `BAndB.pdf`) — teoría de apoyo.

> Varios notebooks dibujan la **región factible**, marcan **restricciones activas/holguras** y validan que la solución cumple el modelo.

---

## 🌳 Estructura
Modelacion-Matematica/
├─ assets/ # datos de ejemplo (e.g., op.csv)
├─ TSP.ipynb
├─ SetCovering.ipynb
├─ OrienteeringProblem.ipynb
├─ JSSP.ipynb
├─ PULPPackage.ipynb
├─ Tarea1_Modelacion_Matematica.ipynb
├─ Tarea2_Modelacion_Matematica.ipynb
└─ docs/ (opcional) # figuras para README/reportes


---

## ⚙️ Instalación rápida
```bash
  # Recomendado: entorno virtual
  python -m venv .venv
  # Windows
  .venv\Scripts\activate
  # macOS / Linux
  source .venv/bin/activate
  
  pip install -U pip
  pip install jupyter pulp numpy pandas matplotlib scipy
  # (Opcional) para grafos:
  # pip install networkx
  
  # Clonar
  git clone https://github.com/<tu-usuario>/Modelacion-Matematica.git
  cd Modelacion-Matematica
  
  # Arrancar Jupyter
  jupyter notebook
  # o
  jupyter lab
---

▶️ Cómo correr
# Clonar
git clone https://github.com/<tu-usuario>/Modelacion-Matematica.git
cd Modelacion-Matematica

# Arrancar Jupyter
jupyter notebook
# o
jupyter lab


Abre el notebook que quieras y ejecuta las celdas de arriba hacia abajo.

📊 Datos (OP / TSP)

Algunos notebooks esperan assets/op.csv. Formato recomendado:

id,x,y,prize
0,12.3,45.6,0
1,20.1,50.2,8
2,35.0,30.0,10


id=0 es el depósito (sin premio).

Si el archivo no existe, algunos notebooks generan un dataset demo en assets/op.csv para que todo corra y luego lo reemplazas por tus datos reales.

💡 Tip de portabilidad: evito rutas absolutas tipo /mnt/data; uso rutas relativas (assets/...) para que funcione en Windows, macOS o Linux sin cambiar nada.


✍️ Estilo de trabajo

Enunciado

Modelo (variables, objetivo, restricciones)

Implementación (Python/PuLP)

Validación (holguras, restricciones activas, suma de arcos, etc.)

Gráficas (región factible, tour TSP/OP, anotaciones)

La idea es que cualquier estudiante (o yo en modo madrugada ☕) pueda reproducir y entender el flujo sin perderse.

🗺️ Roadmap

 Heurísticos TSP/OP (2-opt, 3-opt, GRASP).

 Problemas extra: Knapsack, Facility Location, VRP básico.

 Exportadores a CSV/LaTeX para tablas de reportes.

 Pequeños datasets curados para prácticas.

🤝 Contribuir

Haz un fork del repo

Crea una rama: git checkout -b feature/mi-mejora

Haz commit: git commit -m "feat: agrego heurístico 2-opt"

Push: git push origin feature/mi-mejora

Abre un Pull Request ✨

👤 Autor

René Guzmán Pérez — FIME UANL
Estudiante de la Maestría en Ciencias (IA y Optimización).
Me apasiona aterrizar modelos en código y usarlos en clase.
