# PINN w bibliotece DeepXDE dla problemu Lotka–Volterry

Projekt przedstawia zastosowanie **Physics-Informed Neural Networks (PINN)** do rozwiązania układu równań różniczkowych Lotki–Volterry z wykorzystaniem biblioteki **DeepXDE**.

Celem projektu jest pokazanie, w jaki sposób sieć neuronowa może być uczona nie tylko na podstawie danych, ale również z wykorzystaniem równań opisujących dynamikę badanego układu.

---

## Opis problemu

Model Lotki–Volterry opisuje zależności pomiędzy dwiema populacjami:

- ofiarami,
- drapieżnikami.

Klasyczny układ równań ma postać:

\[
\frac{dx}{dt} = \alpha x - \beta xy
\]

\[
\frac{dy}{dt} = \delta xy - \gamma y
\]

gdzie:

- `x(t)` – liczebność populacji ofiar,
- `y(t)` – liczebność populacji drapieżników,
- `α` – współczynnik wzrostu populacji ofiar,
- `β` – współczynnik interakcji drapieżnik–ofiara,
- `δ` – współczynnik wzrostu populacji drapieżników,
- `γ` – współczynnik śmiertelności drapieżników.

---

## Physics-Informed Neural Networks

Physics-Informed Neural Networks są sieciami neuronowymi, których funkcja kosztu uwzględnia nie tylko błąd względem danych treningowych, ale również zgodność rozwiązania z równaniami różniczkowymi opisującymi dany problem.

W projekcie sieć neuronowa aproksymuje funkcje:

\[
x(t)
\]

oraz

\[
y(t)
\]

a podczas treningu minimalizowany jest błąd wynikający z niespełnienia równań Lotki–Volterry oraz warunków początkowych.

---

## Technologie

Projekt został wykonany w języku **Python**.

Wykorzystane biblioteki:

- DeepXDE
- PyTorch
- NumPy
- SciPy
- Matplotlib
- Pandas

Środowisko:

- Google Colab
- Jupyter Notebook

---

## Struktura projektu

```text
PINN-Lotka-Volterra/
│
├── PINN_Lotka_Volterra.ipynb
├── README.md
└── Sprawozdanie_PINN_Lotka_Volterra.pdf
