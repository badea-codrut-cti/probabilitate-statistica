## Problema 3 iunie 2022

Fie $X$ o variabila aleatoare continua cu densitatea de repartitie

### Metoda verosimilitatii maxime

$\displaystyle f:(0,1) \times \left(\frac{1}{2}, 1\right)\rightarrow(0,\infty), f(x, \theta) = \frac{\theta}{1-\theta} x^{\displaystyle\frac{2\theta - 1}{1-\theta}}$

Fie $X_1, X_2, \dots X_n$ iid cu valori de selectie $x_1, x_2, \dots x_n$

$L(\theta | x_1, x_2, \dots x_n) = \displaystyle\prod_{i=1}^n f(x_i) = \prod_{i=1}^n \frac{\theta}{1-\theta} x_i^{\displaystyle\frac{2\theta - 1}{1-\theta}} = \left(\frac{\theta}{(1-\theta)}\right)^n \left(\prod_{i=1}^n x_i\right)^{\displaystyle\frac{2\theta - 1}{1 - \theta}}$

$\displaystyle\ln (L(\theta)) = n \ln \theta - n \ln (1-\theta) + \frac{2\theta-1}{1-\theta}\sum_{i=1}^n \ln x_i$

Fie $\alpha = \displaystyle\sum_{i=1}^n \ln x_i$

$\displaystyle\frac{\partial \ln(L(\theta))}{\partial\theta} = \frac{n}{\theta} + \frac{n}{1-\theta} + \frac{2-2\theta + 2\theta - 1}{(1-\theta)^2} \alpha = \frac{n}{\theta} + \frac{n}{1-\theta} + \frac{1}{(1-\theta)^2}\alpha \implies$

$\implies \displaystyle\frac{n}{\theta} + \frac{n}{1-\theta} + \frac{1}{(1-\theta)^2}\alpha = 0 \left| \cdot (1-\theta)^2 \theta \right . \implies \\
\implies n(1-\theta)^2 + n(1-\theta)\theta + \theta\alpha = 0 \implies \\
\implies n - 2n\theta + n\theta^2 + n\theta - n\theta^2 + \theta\alpha = 0 \implies \\
\implies \theta(\alpha - n) + n = 0 \implies \\
\implies \theta = -\frac{n}{\alpha - n} = \frac{n}{n - \displaystyle\sum_{i=1}^n \ln x_i}$

$\hat\theta = \displaystyle\frac{n}{n-\displaystyle\sum_{i=1}^n \ln X_i}$

$\displaystyle\frac{\partial^2 \ln(L(\theta))}{\partial^2 \theta} = -\frac{n}{\theta^2} + \frac{n}{(1-\theta)^2} + \frac{2\alpha}{(1-\theta)^3}$

$\displaystyle\frac{\partial^2 \ln(L(\theta))}{\partial^2 \theta}\left(\frac{n}{n-\alpha}\right) = -\frac{n \cdot (n-\alpha)}{n} + \frac{n}{\displaystyle \left(1 - \frac{n}{n-\alpha}\right)^2} + \frac{2\alpha}{\displaystyle \left(1-\frac{n}{n-\alpha}\right)^3} = \\
= n-\alpha + \frac{n}{\displaystyle 1 - \frac{2n}{n-\alpha} + \frac{n^2}{(n-\alpha)^2}} + \frac{2\alpha}{\displaystyle \left(1-\frac{n}{n-\alpha}\right)^3} = \\
= n - \alpha + \frac{n(n-\alpha)^2}{(n-\alpha)^2 - 2n(n-\alpha) + n^2} + \frac{2\alpha}{\displaystyle \left(1-\frac{n}{n-\alpha}\right)^3}$

### Metoda momentelor

$E(X) = \overline{X} = \displaystyle\int_0^1 \frac{\theta}{1-\theta} x^{\displaystyle\frac{2\theta - 1}{1-\theta} + 1}dx = \int_0^1 \frac{\theta}{1-\theta}x^{\displaystyle\frac{\theta}{1-\theta}} dx = \frac{\theta}{1-\theta} \left. x^{\displaystyle\frac{1}{1-\theta}} (1-\theta)\right|_0^1 = \theta \left. x^{\displaystyle\frac{1}{1-\theta}}\right |_0^1 = \theta \implies \\
\implies \hat\theta = \overline{X}$ estimator

Daca nu ni se cere in mod explicit ce metoda sa folosim, daca functia contine $e$ probabil este mai usor de aplicat metoda verosimilitatii. 

## Problema 4 septembrie 2022

a) O moneda este aruncata de 100 de ori si se obtine cap de 59 de ori. Fie $\theta$ probabilitatea evenimentului de a obtine cap dintr-o singura aruncare. Determinati o estimatie a parametrului $\theta$ prin metoda verosimilitatii maxime.

$\theta = P(A), A $ evenimentul de a obtine cap dintr-o singura aruncare.

Fie $X_1, X_2, \dots X_n$ iid repartizate $\text{Bern}(\theta)$.

$X \approx \begin{pmatrix}0 & 1 \\ 1-p & p\end{pmatrix}$

$f_X(x) = \theta^x(1-\theta)^{1-x}$

$L(\theta|x_1, x_2, \dots x_n) = \displaystyle\prod_{i=1}^n f(x_i) = \prod_{i=1}^{59} f(1) \cdot \prod_{i=60}^{100} f(0) = \theta^{59} (1-\theta)^{41}$

$\ln L(\theta) = 59 \ln \theta + 41 \ln (1-\theta)$

$\displaystyle\frac{\partial\ln L(\theta)}{\partial\theta} = \frac{59}{\theta} - \frac{41}{1-\theta} = 0 \implies\\
\implies 59 (1-\theta) - 41\theta = 0 \implies \\
\implies 59 - 59\theta -41\theta = 0 \implies \\
\implies 59 - 100\theta = 0 \implies \theta = \frac{59}{100}$

b) Fie $X_1,\dots X_n$ o selectie de volum $n$ dintr-o repartitie $\text{Exp}(\lambda)$. Determinati o estimatie a parametrului $\lambda$ prin metoda verosimilitatii maxime.

Fie $X_1,\dots X_n$ iid cu valorile $x_1, \dots x_n$

$f(x) = \lambda e^{-\lambda x}, x > 0$

Presupunem ca $x_1, \dots x_n > 0$

$L(\lambda|x_1, \dots, x_n) = \displaystyle\prod_{i=1}^n \lambda e^{-\lambda x_i} = \lambda^n e^{-\lambda \displaystyle\sum_{i=1}^n x_i} = \lambda^n e^{\displaystyle -n\lambda \overline{x}}$

$\displaystyle \ln L(\lambda) = n\ln\lambda - n\lambda\overline{x}$

$\displaystyle\frac{\partial\ln L(\theta)}{\partial\theta} = \frac{n}{\lambda} - n\overline{x} \implies \lambda = \frac{1}{\overline{x}} \implies \hat\lambda = \frac{1}{\overline{X}}$

$\displaystyle\frac{\partial^2\ln L(\theta)}{\partial^2\theta} = -\frac{n}{\lambda^2} \\
\displaystyle\frac{\partial^2\ln L(\theta)}{\partial^2\theta}\left(\frac{1}{\overline{x}}\right) = -n\overline{x}^2 < 0 \implies \lambda = \frac{1}{\overline{x}}$ punct de maxima 