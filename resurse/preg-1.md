$X \approx f_\theta, \theta = ?$

$X = X_1, X_2, \dots, X_n$

$\theta, \cos(X_2) \\
2X_3 + X_1 + 3\\
e^{X_5}$

Vrem un estimator de varianta cat mai mica pentru ca estimarea sa fie cat mai stabila la schimbarea esantionului.

# Marginea Inferioara Rao Cramer

nu este dependenta de esantion.

$\text{MIRC} = \displaystyle\frac{1}{I_n(\theta)}$ 

$I_n(\theta) = n$ - volumul esantionului

$I_1(\theta) = \displaystyle E\left(\left(\frac{\partial\ln f_\theta(X)}{\partial\theta}\right)^2\right)$

$I_1(\theta) = \displaystyle -E(\frac{\partial^2}{\partial\theta^2} \ln f_\theta(X))$

## Teorema Rao Cramer

Plecam de la un estimator **nedeplasat** (i.e multimea estimatorilor in care caut nu este multimea tuturor estimatorilor). 

## Estimator nedeplasat

Fie $\hat{\theta}$ un estimator nedeplasat pentru $\theta$. Atunci $Var(\hat{\theta})\ge\text{MIRC}$

In plus, daca are loc egalitate (i.e $Var(\hat{\theta}) = \text{MIRC}$) atunci $\hat{\theta}$ este un estimator eficient.

Estimator nedeplasat inseamna $E(\hat{\theta}) = \theta$.

### Exemplu

a) Sa se estimeze folosind, la alegere, una din metodele de estimare cunoscute, valoarea parametrului $\theta$ pentru o v.a. $X$ definita prin densitatea

$f(x, \theta) = \displaystyle\frac{x^2}{2\theta^3}e^{-\displaystyle\frac{x}{\theta}}, x> 0, \theta > 0$

Este $\hat{\theta}$ un estimator nedeplasat?

Metoda verosimilitatii maxime

Fie $X_1, X_2, \dots, X_n$ independente identic distribuite cu valorile de selectie $x_1, \dots, x_n$

$L(\theta / x_1, x_2, \dots, x_n) = \displaystyle\prod_{i=1}^n f_\theta(x_i) = \prod_{i=1}^n \frac{x_i^2}{2\theta^3} e^{-\displaystyle\frac{x_i}{\theta}} = \frac{1}{2^n\theta^{3n}} e^{-\displaystyle\frac{1}{\theta}\sum_{i=1}^n x_i}\prod_{i=1}^n x_i^2$

$\overline{x} = \displaystyle\frac{1}{n}\sum_{i=1}^n x_i$

$\ln L(\theta) = \displaystyle -\frac{n}{\theta}\overline{x} - n\ln (2\theta^3) + \ln(\prod_{i=1}^n x_i^2)=\\
= -n \ln2 - 3n\ln\theta + \ln(\prod_{i=1}^n x_i^2) - \frac{n}{\theta}\overline{x} \implies \\
\implies \frac{\partial \ln L(\theta)}{\partial \theta} = -\frac{3n}{\theta} + n\overline{x} \cdot \frac{1}{\theta^2}$

dar $\displaystyle\frac{\partial \ln L(\theta)}{\partial \theta} = 0 \implies -\frac{3n}{\theta} + n\overline{x}\frac{1}{\theta^2} = 0$

$\displaystyle -3\theta + \overline{x} = 0 \implies \theta = \frac{\overline{x}}{3} \implies \hat{\theta} = \frac{\overline{X}}{3}$

Verificam ca punctul $\theta = \displaystyle\frac{\overline{x}}{3}$ (punct critic) este punct de maxim local.

$\displaystyle\left.\frac{\partial^2 \ln L(\theta)}{\partial \theta^2}\right|_{\theta = \displaystyle\frac{\overline{x}}{3}} = \left.3n\frac{1}{\theta^2} - 2n\overline{x} \frac{1}{\theta^3}\right|_{\theta = \displaystyle\frac{\overline{x}}{3}} = \left.n\frac{1}{\theta^2}\left(3-2\overline{x}\frac{1}{\theta}\right)\right|_{\theta = \displaystyle\frac{\overline{x}}{3}} = n \frac{9}{\overline{x}^2}\left(3-2\overline{x} \frac{3}{\overline{x}}\right) < 0 \implies$ 

$\implies\displaystyle \theta = \frac{\overline{x}}{3}$ punct de maxim local

Verificam daca estimatorul obtinut este sau nu deplasat (este sau nu unbiased).

$\displaystyle E(\hat{\theta}) = E(\frac{\overline{X}}{3}) = \frac{1}{3} E(\overline{X}) = \frac{1}{3} E(\frac{1}{n} \sum_{i=1}^n X_i), X_i$ independente $\implies \displaystyle E(\hat{\theta}) = \frac{1}{3n}\sum_{i=1}^n E(X_i)$

Fie $\displaystyle m = E(X) = \int_{-\infty}^\infty x f(x) dx, x > 0, \theta > 0 \implies m = \int_{0}^\infty x f(x) dx =$

$\displaystyle = \int_0^\infty x \frac{x^2}{2\theta^3} e^{-\displaystyle\frac{x}{\theta}}dx$

$\displaystyle\Gamma(\alpha) = \int_0^\infty x^{\alpha-1}e^{-x}dx, \alpha > 0$

Schimbare de variabila $\displaystyle\frac{x}{\theta} = t$

$dx = \theta dt$

$x = 0 \implies t = 0 \\
x \rightarrow\infty \implies t \rightarrow \infty$

$\displaystyle\int_0^\infty \frac{1}{2}t^3 e^{-t} \theta dt = \frac{\theta}{2} \int_0^\infty t^3 e^{-t} dt = \frac{\theta}{2} \Gamma(4)$

$\Gamma(n) = (n-1)!$

$m = \displaystyle\frac{\theta}{2} 3! = 3\theta$

$E(\hat{\theta}) = \displaystyle\frac{1}{3n} \sum_{i=1}^n E(X_i) = \frac{1}{3n} \sum_{i=1}^n 3\theta = \frac{1}{3n} 3n\theta = \theta \implies \hat{\theta}$ este un estimator nedeplasat.

Daca $E(\hat{\theta}) \ne \theta$ atunci este un estimator deplasat.

b) Calculati MIRC pentru v.a. $X$. Atinge $Var(\hat{\theta})$ MIRC?

Pentru a evalua daca estimatorul este si eficient, calculam intai MIRC, apoi comparam cu varianta estimatorului.

$I_1(\theta) = \displaystyle E\left(\left(\frac{\partial\ln f_\theta(X)}{\partial\theta}\right)^2\right)$

$\displaystyle\ln(f_\theta(x)) = \ln\left(\frac{x^2}{2\theta^3} e^{-\displaystyle\frac{x}{\theta}}\right)= \ln \frac{x^2}{2\theta^3} - \frac{x}{\theta} = 2\ln x - \ln 2 - 3\ln \theta - \frac{x}{\theta}$

$\displaystyle\frac{\partial \ln f_\theta(x)}{\partial\theta} = -\frac{3}{\theta} + \frac{x}{\theta^2}$


$\displaystyle\left(\frac{\partial \ln f_\theta(x)}{\partial\theta}\right)^2 = \frac{x^2}{\theta^4} - \frac{6x}{\theta^3} + \frac{9}{\theta^2}$

$\displaystyle I_1(\theta) = E\left(\frac{X^2}{\theta^4} - \frac{6X}{\theta^3} + \frac{9}{\theta^2}\right) = \frac{1}{\theta^4} E\left(X^2\right) - \frac{6}{\theta^3} E(X) + \frac{9}{\theta^2}$

$\displaystyle E(X^2) = \int_0^\infty x^2 f_\theta(x) dx = \int_0^\infty\frac{x^4}{2\theta^3} e^{-\displaystyle\frac{x}{\theta}}dx$

Facem aceeasi schimbare de variabila $\displaystyle\frac{x}{\theta} = t, dx = \theta dt$

$\displaystyle E(X^2) = \int_0^\infty \frac{\theta^4 t^4}{2\theta^3} e^{-t} \theta dt = \frac{\theta^2}{2}\int_0^\infty t^4dt = \frac{\theta^2}{2} \Gamma(5) = \frac{\theta^2}{2} 4! = 12\theta^2$

$\displaystyle I_1(\theta) = \frac{9}{\theta^2} - \frac{6}{\theta^3} 3\theta + \frac{1}{\theta^4} 12\theta^2 = \frac{3}{\theta^2}$

$\text{MIRC} = \displaystyle\frac{1}{n\cdot I_1(\theta)} = \frac{\theta^2}{3n}$

Calculam $\displaystyle Var(\hat{\theta}) = Var\left(\frac{\overline{X}}{3}\right) = \frac{1}{9} Var\left(\overline{X}\right) = \frac{1}{9} Var\left(\frac{1}{n}\sum_{i=1}^n X_i\right) = \frac{1}{9n^2} Var\left(\sum_{i=1}^n X_i\right)$ (varianta scoate constantele la patrat)

$= \displaystyle\frac{1}{9n^2}\sum_{i=1}^n Var(X_i) = \frac{1}{9n^2} \sum_{i=1}^n\sigma^2 \\
\sigma^2 = Var(X)  = E\left(X^2\right) - (E(x))^2 = 12 \theta^2 - (3\theta)^2 = 3\theta^2$

$\displaystyle Var(\hat{\theta}) = \frac{1}{9n^2} 3n\theta^2 = \frac{\theta^2}{3n} = \text{MIRC}$

Cum varianta estimatorului coincide cu MIRC, estimatorul este unul eficient.

## Aplicarea metodei momentelor pentru aceeasi problema

$\displaystyle E_\theta(X) = \overline{X} \implies 3\theta = \overline{X} \implies \hat{\theta} = \frac{\overline{X}}{3}$

In Aceasta problema a fost o intamplare (fericita) ca estimatorii obtinuti prin cele doua metode au fost egali. In general, ei sunt diferiti, iar estimatorul mai bin este cel dat de metoda verosimilitatii maxime.