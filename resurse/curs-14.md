# Examen 2023 Nr 2

## Subiectul 1 (1p)

Ina vrea sa calatoreasca maine in alt oras. Probabilitatile de a calatori daca
ploua, respectiv daca nu ploua sunt 0.46 si 0.70. Daca probabilitatea de a ploua maine
este 0.40, determinati probabilitatea ca Ina sa mearga maine in alt oras.

$A$ - evenimentul de a ploua

$P(A) = 0.4$

$B$ - evenimentul de a calatori in alt oras

$P(B|A) = 0.46$

$P(B|\overline{A}) = 0.7$

$P(B) = P(B|A) \cdot P(A) + P(B|\overline{A}) \cdot P(\overline{A}) = 0.46 \cdot 0.4 + 0..7 \cdot 0.6 = 0.604$

## Subiectul 2 (1p)

Fie $X$ o variabila aleatoare repartizata uniform, $X \approx U[0,2]$ si $Y = \displaystyle\frac{1}{2-X}$. Determinati o densitate de probabilitate a variabilei aleatoare $Y$.

$f_X(x) = \begin{cases}\displaystyle\frac{1}{2}, x \in [0,2] \\ 0, \text{in rest}\end{cases}$

$F_X(x) = \displaystyle\int_{-\infty}^{\displaystyle\frac{1}{2}} f_X(x) dx = \begin{cases}0, x < 0 \\\displaystyle\frac{x}{2}, x\in[0,2] \\ 1, x > 2\end{cases}$

$\displaystyle P(Y \le y) = P\left(\frac{1}{2-x} \le y\right) = P\left(2-x \ge \frac{1}{y}\right) = P\left(-x \ge \frac{1}{y} - 2\right) = P\left(x \le 2 - \frac{1}{y}\right)$

$\displaystyle 2 - \frac{1}{y} < 0 \implies \frac{1}{y} > 2$

$\displaystyle F_Y(y) = F_X\left(2-\frac{1}{y}\right) = \begin{cases}0, \displaystyle 2-\frac{1}{y} \le 0\\ \displaystyle\frac{1}{2}\left(2-\frac{1}{y}\right), 2-\frac{1}{y} \in [0,2] \\
1, \displaystyle 2-\frac{1}{y} > 2 \end{cases}$

$F_Y(y) = \begin{cases}0, y < \displaystyle\frac{1}{2} \\ 1 - \displaystyle\frac{1}{2y}, y \in \left[0,\frac{1}{2}\right]\\1, y < 0\end{cases}$ 

Ultima ramura nu este relevanta deoarece $X$ ia valori intre $0$ si $2$, astfel $Y$ nu o sa ia valori negative.

$f_Y(y) = F_Y'(y) = \begin{cases}0, y\in[0,2]\\\displaystyle\frac{1}{2y^2}, y\in\left[\frac{1}{2}, \infty\right)\end{cases}$

## Subiectul 3 (1p)

Ema este interesata de a gasi relatia dintre conditiile atmosferice si intarzierile
trenurilor cu care face naveta. Ea a inregistrat intr-o perioada lunga de timp daca
vremea este insorita, noroasa, ploioasa sau daca a nins, precum si intarzierile
trenurilor. Inregistrarile sunt in tabelul de mai jos.

Vremea|Trenuri venite la timp|Trenuri intarziate|Total
---|---|---|---
Insorita|5|5|10
Noroasa|15|5|20
Ploioasa|30|20|50
Cu zapada|10|10|20
Total|60|40|100

Determinati repartitia conditionata de starea vremii a trenurilor intarziate.

$P(\text{Intarziate} | \text{Insorit}) = \displaystyle\frac{P(\text{Intarziate} \cap \text{Insorit})}{P(\text{Insorit})} = \frac{1}{2}$

$P(\text{Intarziate} | \text{Noros}) = \displaystyle\frac{P(\text{Intarziate} \cap \text{Noros})}{P(\text{Insorit})} = \frac{1}{4}$

$P(\text{Intarziate} | \text{Ploaie}) = \displaystyle\frac{P(\text{Intarziate} \cap \text{Ploaie})}{P(\text{Insorit})} = \frac{2}{5}$

$P(\text{Intarziate} | \text{Zapada}) = \displaystyle\frac{P(\text{Intarziate} \cap \text{Zapada})}{P(\text{Insorit})} = \frac{1}{2}$

## Subiectul 4 (1p)

Fie $X$ si $Y$ variabile aleatoare cu functia de densitate comuna

$f_{X,Y}(s,t) = \begin{cases}c(se^{-3t} + e^{-t}), 0 < s < 1, 0 < t < \infty \\ 0, \space \text{altfel}\end{cases}$

Determinati $Cov(X,Y)$

$f_X(s) = \displaystyle\int_0^\infty c(se^{-3t} + e^{-t}) dt = cs \int_0^\infty e^{-3t}dt + c\int_0^\infty e^{-t} dt = -\frac{cs}{3} \cdot \left. e^{-3t}\right|_0^\infty -c \left. e^{-t} \right|_0^\infty = \frac{cs}{3} + c$

$\displaystyle\int_0^1 \frac{cs}{3} + c ds = 1 \iff \left. \frac{c}{3} \frac{s^2}{2}\right|_0^1 = 1 \iff c = \frac{6}{7}$

$f_X(s) = \displaystyle \frac{2}{7} s + \frac{6}{7}$
$\displaystyle f_Y(t) = \int_0^1 f_{X,Y} ds = \int_0^1 \frac{6}{7}(se^{-3t} + e^{-t}) ds = \frac{6}{7} \left. e^{-3t} \frac{s^2}{2}\right|_0^1 = \frac{6}{7}e^{-t}, t > 0$

$E(X) = \displaystyle\int_0^1 sf_X(s) ds = \int_0^1 \frac{2}{7} s^2 + \frac{6}{7} s ds = \left. \frac{2}{7} \frac{s^3}{3}\right|_0^1 + \left. \frac{6}{7} \frac{s^2}{2}\right|_0^1 = \frac{2}{21} + \frac{3}{7} = \frac{11}{21}$

$E(Y) = \displaystyle\int_0^\infty t f_Y(t) dt = \int_0^\infty t \frac{3}{7} e ^{-3t} + t \frac{6}{7}e^{-t} dt = \frac{1}{7} \int_0^\infty 3t e^{-3t} dt + \frac{6}{7} \int_0^\infty t e^{-t}dt = \frac{1}{7} \Gamma(2) + \frac{6}{7}\Gamma(2) = 1$

$E(XY) = \displaystyle\int_0^\infty\int_0^1 stf_{X,Y}(s,t) ds dt = \int_0^\infty \left(\int_0^1 s^2 t e^{-3t} \frac{6}{7} + s t e ^{-t} \frac{6}{7} ds\right)dt = \int_0^\infty \frac{2}{7} t e^{-3t} dt + \int_0^\infty \frac{3}{7} t e^{-t} dt = \\
= \frac{2}{7}\frac{1}{9}\Gamma(2) + \frac{3}{7}\Gamma(2) = \frac{29}{63}$

$Cov(X,Y) = \displaystyle E(XY) - E(X)E(Y) = \frac{29}{63} - \frac{11}{21} \cdot 1 = -\frac{4}{63}$

### Subiectul 5 (1p)

Fie $X_1, \dots, X_n$ variabile aleatoare independente si identic repartizate $\text{Bernoulli}(p)$. Este $\overline{X}$ estimator nedeplasat pentru $p$? Atinge el marginea inferioara Rao-Cramer?

Nu o sa avem MIRC la examen.

### Subiectul 6 (1p)

Fie $X_1, \dots, X_n$ variabile aleatoare independente si identic repartizate cu functia de densitate de repartitie

$f(x|\sigma) = \displaystyle\frac{1}{\sigma} e^{-\displaystyle\frac{x}{\sigma}}, x \ge 0$.

Determinati un estimator pentru $\sigma$ prin metoda verosimilitatii maxime.

$L(\sigma | x_1, x_2, \dots, x_n) = \displaystyle\prod_{i=1}^n \frac{1}{\sigma} e^{-\displaystyle\frac{x}{\sigma}} = \frac{1}{\sigma^n} e^{-\displaystyle\frac{1}{\sigma}\sum_{i=1}^n x_i}$

$\displaystyle \ln L(\sigma) = -n\ln\sigma - \frac{1}{\sigma} n \overline{x}$

$\displaystyle\frac{\partial \ln L(\sigma)}{\partial \sigma} = 0 \iff \frac{n\overline{x}}{\sigma^2} - \frac{n}{\sigma} = 0 \iff \sigma = \overline{x}$

$\displaystyle\frac{\partial^2 \ln L(\sigma)}{\partial^2 \sigma}(\overline{x}) = -2n\overline{x}\frac{1}{\overline{x}^3} + \frac{n}{\overline{x}^2} = -n\frac{1}{\overline{x}} \le 0 \implies \sigma = \overline{x}$ punct de maxim global

