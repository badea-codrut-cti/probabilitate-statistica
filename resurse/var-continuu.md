# Variabile aleatoare de tip continuu

O variabila aleatoare de tip continuu este o variabila aleatoare care ia valori intr-o multime continua.

## Notatie

Daca $S \subset \R, \{X \in S\}$ este evenimentul ca $X$ ia valori in $S$

De exemplu:

- $\{X\in(a,b)\} = \{a < X < b\}$
- $\{X \in (-\infty, c]\} = \{X \le c\}$
- $\{X \in (c, \infty)\} = \{X > c\}$

## Functia de densitate de probabilitate

Joaca rolul functiei masa de probabilitate pentru v.a. discrete.

Fie $X$ o v.a. de tip continuu. O functie $f:\R\rightarrow\R$ este o functie de densitate de probabilitate a lui X daca:

- $f(n) \ge 0 \space \forall \space n \in\R$
- $\displaystyle\int_{-\infty}^\infty f(x) dx = 1$
- $\forall \space S \subseteq \R, P(X \in S) = \displaystyle\int_S f(x) dx$

$P(a < X < b) = \displaystyle\int_a^b f(x) dx \\
P(x \le c) = \displaystyle\int_{-\infty}^c f(x) dx \\
P(X = a) = 0$

### Exemplu

Determinati $c \in \R$ astfel incat functia $f$ sa fie densitate de probabilitate si calculati $P(X > 3)$, unde $f:\R\rightarrow\R,\\ f(x) = \begin{cases}\displaystyle\frac{c}{2}, 1 < x < 5 \\ 0, \text{in rest}\end{cases}$ 

$\displaystyle\int_{-\infty}^\infty f(x) dx = 1 \implies \displaystyle \int_{-\infty}^1 0 dx + \int_1^5 \frac{c}{2}dx + \int_5^\infty 0dx = 1\\
\int_1^5 \frac{c}{2}dx = 1 \\
2c = 1 \implies c = \frac{1}{2}$

$P(X > 3) = \displaystyle\int_3^5 \frac{1}{4} dx = \frac{5-3}{4} = \frac{1}{2}$

## Media si variatia $E(X), Var(X)$

$E(X) = \displaystyle\int_{-\infty}^\infty xf(x) dx$

$Var(X) = \displaystyle\int_{-\infty}^\infty (x - E(x))^2 dx = E(X^2) - (E(X))^2\\
E(X^2) = \displaystyle\int_{-\infty}^\infty x^2 f(x) dx$

### Exemplu

Determinati $E(X)$ si $Var(X)$, daca $X$ are functia de densitate de probabilitate $f(x) = \lambda e^{-\lambda x}, x > 0$ ($X$ are repartitie exponentiala).

$E(X) = \displaystyle\int_0^\infty x f(x) dx = -\int_0^\infty x(e^{-\lambda x})' = \left . -x e^{\displaystyle -\lambda x}\right |_0^\infty + \int_0^\infty e^{-\lambda x}dx = \left. -\frac{e^{-\lambda x}}{\lambda} - xe^{-\lambda x} \right|_0^\infty = \\
= \frac{e^0}{\lambda} + 0\cdot e^0 + \lim_{x\rightarrow \infty} -\frac{e^{-\lambda x}}{\lambda} - xe^{-\lambda x} = \frac{1}{\lambda}$

$E(X^2) = \displaystyle\int_0^\infty x^2 f(x) dx = \int_0^\infty x^2\lambda e^{-\lambda x} = -\int_0^\infty x^2 (e^{-\lambda x})' dx = \left . -x^2 e^{-\lambda x} \right |_0^\infty + \frac{2}{\lambda}\int_0^\infty x\lambda e^{-\lambda x} = \frac{2}{\lambda} \cdot \frac{1}{\lambda} - \lim_{x\rightarrow\infty} x^2e^{-\lambda x} = \frac{2}{\lambda ^2}$

$Var(X) = E(X^2) - (E(X))^2 = \displaystyle\frac{2}{\lambda^2} - \frac{1}{\lambda^2} = \frac{1}{\lambda^2}$

## Functie de densitate comuna

Fie $X, Y$ variabile comune aleatoare definite pe acelasi spatiu de probabilitate.

Functia $f:\R\times\R\rightarrow\R$ este o functie de densitate comuna pentru variabilele aleatoare $X, Y$ daca:

- $f(x, y) = 0 \space \forall \space x, y\in\R$
- $\displaystyle\int_{-\infty}^\infty\int_{-\infty}^\infty f(x,y) dxdy = 1$
- Fie $S \subseteq \R^2, P((X,Y) \in S) =\displaystyle {\int\int}_S f(x,y) dxdy$

## Repartitii marginale

Daca $f:\R\times\R\rightarrow\R$ este functia de densitate comuna a variabilelor $X, Y$, atunci $X$ si $Y$ au densitatile marginale $f_X, f_Y$, unde $f_X, f_Y : \R \rightarrow \R$:

- $f_X(x) = \displaystyle\int_{-\infty}^\infty f(x, y) dy, x\in\R$
- $f_Y(y) = \displaystyle\int_{-\infty}^\infty f(x, y) dx, y\in\R$

## Variabile aleatoare independente

$X, Y$ independente $\iff f(x, y) = f_X(x) \cdot f_Y(y) \space \forall \space x,y\in\R$

### Exemplu

Demonstrati ca v.a. $X, Y$ cu functia de densitate comuna $f(x,y) = 6e^{\displaystyle-(2x + 3y)}, x,y > 0$ sunt independente.

$f_X = \displaystyle\int_0^\infty 6e^{\displaystyle-(2x + 3y)} dy = \left . -2e^{\displaystyle -2x - 3y} \right |_0^\infty = 2e^{\displaystyle -2x}$

$f_Y = \displaystyle\int_0^\infty 6e^{\displaystyle-(2x + 3y)} dx = \left. -3e^{\displaystyle -2x - 3y} \right |_0^\infty = -3e^{\displaystyle-3y}$

$f_X \cdot f_Y = 6e^{-2x -3y} = f(x,y) \implies X,Y$ independente

## Covariatia si corelatia

$E(X Y) = \displaystyle\int_{-\infty}^\infty\int_{-\infty}^\infty x y f(x,y)dxdy$

$Cov(X, Y) = E(X Y) - E(X)E(Y)$

$Corr(X, Y) = \displaystyle\frac{Cov(XY)}{\sqrt{Var(X)} \sqrt{Var(Y)}}$ - coeficientul de corelatie

