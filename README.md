Modelación Matemática

Ejercicios y soluciones de Modelación Matemática usando Python y PuLP.
Este repo lo uso para mis clases en FIME-UANL y como bitácora de aprendizaje rumbo a mi Maestría en Ciencias con enfoque en Inteligencia Artificial y Optimización. La idea es tener ejemplos claros, reproducibles y con código comentado.

¿Qué hay aquí?

TSP.ipynb — Formulación del viajante (TSP)

DP de Held-Karp y modelo MTZ en ILP (PuLP).

SetCovering.ipynb — Set Covering con enteras.

OrienteeringProblem.ipynb — Orienteering (OP) con presupuesto y premios.

JSSP.ipynb — Job Shop Scheduling (formulación base y ejemplo).

PULPPackage.ipynb — Guía rápida de PuLP (variables, restricciones, solver).

Tarea1_Modelacion_Matematica.ipynb — Tarea 1 resuelta, con estilo “explico, modelo, implemento y valido”.

Tarea2_Modelacion_Matematica.ipynb — Tarea 2 resuelta, mismo formato (holguras, restricciones activas, gráficas).

PDFs (Intro_OptCO.pdf, MetodosPL.pdf, Prog_Entera.pdf, BAndB.pdf) — teoría de apoyo (métodos, enteras, branch & bound, etc.).

Nota: algunos notebooks generan gráficas y marcan restricciones activas/holguras para validar que la solución sí cumple el modelo.

Requisitos

Python 3.10+

Jupyter Notebook o JupyterLab

Paquetes clave: pulp, numpy, pandas, matplotlib, scipy

Puedes instalar así:

pip install jupyter pulp numpy pandas matplotlib scipy


(If needed: pip install networkx para algunas visualizaciones en grafos.)

Cómo correr
# Clonar
git clone https://github.com/<tu-usuario>/Modelacion-Matematica.git
cd Modelacion-Matematica

# Arrancar Jupyter
jupyter notebook


Abres el notebook que quieras y ejecutas las celdas de arriba hacia abajo.

Datos (OP / TSP)

Algunos notebooks usan un CSV tipo assets/op.csv. Formato recomendado:

id,x,y,prize
0, 12.3, 45.6, 0
1, 20.1, 50.2, 8
2, 35.0, 30.0, 10
...


id=0 es el depósito (sin premio).

Si no existe assets/op.csv, el notebook crea un dataset demo para que todo corra y luego puedas reemplazarlo por tus datos reales.

Estructura / Estilo

Cada ejercicio sigue esta lógica: enunciado → modelo → implementación → validación → gráfica.

Prefiero soluciones reproducibles (semillas fijas, salidas claras en consola y plots limpios).

Donde aplica, muestro dos caminos: exacto (DP/ILP) y heurístico/simple, para comparar.

Roadmap (lo que quiero ir sumando)

Heurísticos para TSP/OP (2-opt, 3-opt, GRASP).

Más problemas clásicos: Knapsack, Facility Location, VRP básico.

Scripts para exportar resultados a CSV/LaTeX (tablas rápidas para reportes).

Licencia

MIT. Úsalo libremente con crédito.

Contacto

¿Dudas o mejoras? Abre un Issue o un PR.
Me sirve mucho el feedback porque esto también lo uso en mis clases y para afinar mi formación en IA y Optimización.

Notas rápidas

Si PuLP no detecta solver externo, usa CBC (viene integrado).

En Windows, evita rutas absolutas tipo /mnt/data; uso rutas relativas (assets/…) para que corra en cualquier SO.

Si quieres, también te dejo un requirements.txt mínimo:

jupyter
pulp
numpy
pandas
matplotlib
scipy
