# Metoda verosimilaritatii maxime

Fie $x_1, \dots, x_n$ valorile observate ale unei selectii $X_1, \dots, X_n$ de volum $n$ dintr-o populatie $X$ avand densitatea $f(x, \theta)$ ce depinde de parametrul necunoscut $\theta$.

Definim functia de verosimilitate drept $L(\theta) = f(x_1, \theta) \cdot \dots f(x_n, \theta)$ cu proprietatea ca $\displaystyle\frac{d \ln L(\theta)}{d\theta} = 0$

## Cazul discret

In cazul in care variabila aleatoare $X$ este discreta, in formula anterioara densitatea $f(x, \theta)$ se inlocuieste cu probabilitatea $P(X=x)$ ca variabila aleatoare $X$ sa ia valoarea $x$. In acest caz, functia de verosimilitate devine:

$L(\theta) = P(X = x_1) \cdot \dots P(X = x_n) = \\
= P(X_1 = x_1) \cdot \dots P(X_n = x_n) = \\
= P(X_1 = x_1, \dots, X_n = x_n)$

### Exemplu

O urna contine un numar necunoscut de bile albe si negre. Sa se estimeze probabilitatea $p$ a extragerii unei bile albe din urna. Consideram o selectie de volum $n$ din urna (cu intoarcerea in urna a bilei extrase inainte de urmatoarea extragere). 

Notam cu $1$ extragerea unei bile albe din urna si cu $0$ extragerea unei bile negre. Populatia este descrisa de variabila aleatoare $X$ avand functia de probabilitate $f(x, p) = P(X = x) = \begin{cases}p, x = 1 \\ 1-p, x = 0 \\ 0, \text{in rest}\end{cases} = \begin{cases}p^x(1-p)^{1-x}, x=0,1 \\ 0, \text{in rest}\end{cases}$

$L(p) = \displaystyle\prod_{i=1}^n p^{x_i}(1-p)^{1-x_i} = p^{\displaystyle\sum_{i=1}^n x_i}(1-p)^{\displaystyle n-\sum_{i=1}^n x_i}$

$\ln L(p) = \displaystyle  \ln p \cdot \sum_{i=1}^n x_i + \ln(1-p) \cdot \left(n - \sum_{i=1}^n x_i\right)$

$\displaystyle\frac{d \ln L(p)}{dp} = \frac{1}{p} \cdot \sum_{i=1}^n x_i - \frac{1}{1-p} \cdot \left( n - \sum_{i=1}^n x_i\right ) = 0$

## Cazul continuu

### Exemplu

Fie $X$ o variabila aleatoare continua cu densitatea $f:[0, \infty) \times (0, \infty) \rightarrow (0, \infty) = \displaystyle\frac{x^2}{16\theta^3} e^{\displaystyle -\frac{x}{2\theta}}$. Pentru o selectie de volum $n$, determinati un estimator al parametrului $\theta$ prin metoda verosimilitatii maxime.

$\displaystyle L(\theta) = f(x_1, \theta) \cdot \dots f(x_n, \theta) = \frac{\displaystyle\prod_{i=1}^n x_i}{16^n \theta^{3n}} e^{-\displaystyle\frac{\displaystyle\sum_{i=1}^n x_i}{2\theta}}$

$\ln L(\theta) = \displaystyle-\frac{1}{2\theta}\sum_{i=1}^n x_i + \ln \prod_{i=1}^n x_i - n \ln 16 - 3n\ln \theta$

$\displaystyle\frac{d\ln L(\theta)}{d\theta} = -\frac{3n}{\theta} + \frac{\displaystyle\sum_{i=1}^n x_i}{2\theta^2} = 0$

Notam $\displaystyle\frac{1}{\theta} = t$

$\displaystyle -3n \cdot t +t^2 \frac{\displaystyle\sum_{i=1}^n x_i}{2} = 0 \\
t(-3n + t \displaystyle\frac{\displaystyle\sum_{i=1}^n x_i}{2}) = 0$

**Cazul I**

$t = 0$

**Cazul II**

$t = \displaystyle \frac{6n}{\displaystyle\sum_{i=1}^n x_i} \implies \theta = \frac{\displaystyle\sum_{i=1}^n}{6n} = \frac{\overline{x}}{6}$