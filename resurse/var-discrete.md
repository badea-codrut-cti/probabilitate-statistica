# Variabile aleatoare discrete

Se numeste variabila aleatoare reala pe campul de evenimente $(\Omega, K)$ orice aplicatie $X:\Omega\rightarrow\R$ pentru care $\{\omega:X(\omega)\in I\}\in K$ oricare ar fi intervalul $I$ al dreptei reale.

Variabilele aleatoare care iau o multime reala finita sau numarabila de valori se numesc variabile aleatoare discrete.

## Notatie

Vom nota o variabila aleatoare discreta printr-un tablou cu doua linii: 
 - pe prima linie vom trece valorile posibile ale variabilei
 - pe a doua linie probabilitatea corespunzatoare fiecarei valori

### Exemplu: fetele unui zar

$Y: \begin{pmatrix}1 & 2 & 3 & 4 & 5 & 6 \\ 
\frac{1}{6} & \frac{1}{6} & \frac{1}{6} & \frac{1}{6} & \frac{1}{6} & \frac{1}{6}
\end{pmatrix}$

## Media unei variabile aleatoare

$E(X) = x_1 p_1 + x_2 p_2 + \dots + x_n p_n$

$E(X^2) = x_1^2 p_1 + \dots + x_n^2 p_n$

### Proprietati ale mediei

- $E(X+Y) = E(X) + E(Y)$
- $E(c\cdot X) = c\cdot E(X)$
- $X \le Y \implies E(X) \le E(Y)$
- daca $X, Y$ variabile aleatoare independente $\implies E(XY) = E(X) E(Y)$

### Exemplu

Se arunca doua zaruri. Sa se calculeze valoarea medie a numarului total de puncte.

- $X$ numar total de puncte
- $X_1$ numar de puncte la primul zar
- $X_2$ numar de puncte la al doilea zar

$E(X_1) = E(X_2) = 1 \cdot \frac{1}{6} + 2 \cdot \frac{1}{6} + \dots + 6 \cdot \frac{1}{6} = \frac{6\cdot7}{12} = \frac{7}{2}, E(X) = E(X_1) + E(X_2) \implies E(X) = \frac{7}{2} + \frac{7}{2} = 7$

## Variatia unei variabile aleatoare $X$

$Var(X) = E(X^2) - (E(X))^2$

### Abaterea mediei patratica

$\sigma = \sqrt{Var(X)}$

<pb/>

### Proprietati

- $Var(X) \ge 0$
- $Var(c \cdot X) = c^2 Var(X), c \in\R$
- Daca $X_1, \dots, X_n$ sunt independente doua cate doua atunci $Var(X_1 + \dots + X_n) = Var(X_1) + \dots + Var(X_n)$
- Inegalitate Cebisev $P(|X - m| \ge K \sigma) \le \frac{1}{K^2}, K \in \R$

### Exemplu

Se dau 3 urne

- $U_1$ contine o bila alba si o bila neagra
- $U_2$ contine 2 bile albe si 7 bile negre
- $U_3$ contine o bila alba si 3 bile negre

Din fiecare urna se extrage cate o bila. Se cer valoarea medie si abaterea medie patratica a numarului de bile albe obtinute in cele 3 extrageri.

Fie $X_1, X_2, X_3$ numarul de bile albe respectiv din prima, a doua si a treia urna.

$X$ - numarul total de bile albe extrase.

$X = X_1 + X_2 + X_3$

$X_1: \begin{pmatrix}1 & 0 \\ 
\frac{1}{2} & \frac{1}{2}
\end{pmatrix}, X_2: \begin{pmatrix}1 & 0 \\ 
\frac{2}{9} & \frac{7}{9}
\end{pmatrix}, X_3: \begin{pmatrix}1 & 0 \\ 
\frac{1}{4} & \frac{3}{4}
\end{pmatrix}$

$E(X) = E(X_1) + E(X_2) + E(X_3) = \frac{1}{2} + \frac{2}{9} + \frac{1}{4} = \frac{18 + 8 + 9}{36} = \frac{35}{36}$

$Var(X_1) = E(X_1^2) - (E(X_1))^2 = \frac{1}{2} - \frac{1}{4} = \frac{1}{4}$

$Var(X_2) = \frac{2}{9} - \frac{4}{81} = \frac{14}{81}$

$Var(X_3) = \frac{1}{4} - \frac{1}{16} = \frac{3}{16}$

$X_1, X_2, X_3$ sunt independente $\implies Var(X) = Var(X_1) + Var(X_2) + Var(X_3) = \frac{1}{4} + \frac{14}{81} + \frac{3}{16}$

Abaterea medie patratica: $\sigma = \sqrt{Var(X)}$

# Vectori aleatori

Daca $X_1, \dots, X_n$ sunt variabile aleatoare, atunci $X = (X_1, \dots, X_n)$ se numeste vector aleator $n$ dimensional.


$n = 2: X = (X_1, X_2)$ se numeste vector aleator bidimensional.

## Vectori aleatori discreti


- $X$ ia valorile $x_1, \dots, x_n$
- $Y$ ia valorile $y_1, \dots, y_m$

Vectorul $(X, Y)$ ia valorile $(x_1, y_1), (x_1, y_2), \dots, (x_n, y_m)$

Fie probabilitatile $P_{ij} = P(X = x_i, Y = y_j), i=\overline{1,n}, j=\overline{1,m}$

Reprezentam astfel:

$X/Y$|$y_1$|$y_2$|$\dots$|$y_m$
---|---|---|---|---
$x_1$|$p_{11}$|$p_{12}$|$\dots$|$p_{1m}$
$x_2$|$p_{21}$|$p_{22}$|$\dots$|$p_{2m}$
$\vdots$|$\vdots$|$\vdots$|$\vdots$|$\vdots$
$x_n$|$p_{n1}$|$p_{n2}$|$\dots$|$p_{nm}$

Suma tuturor probabilitatilor e 1.

### Repartitiile marginale ale variabilelor $X$ si $Y$

Variabilele X si Y au repartitiile date de urmatoarele tablouri

$X: \begin{pmatrix}x_1 & x_2 & \dots & x_n \\ 
p_1 & p_2 & \dots & p_n
\end{pmatrix}, 
Y: \begin{pmatrix}y_1 & y_2 & \dots & y_m \\ 
q_1 & q_2 & \dots & q_m
\end{pmatrix}$

unde 
 - $p_i = \displaystyle\sum_{j=1}^m P_{ij}, i=\overline{1,n}$
 - $q_j = \displaystyle\sum_{i=1}^n P_{ij}, j=\overline{1,m}$

$X$ si $Y$ sunt variabile aleatoare independente $\iff P(X=x_i ; Y=y_j) = P(X = x_i) P(Y = y_j) \forall i = \overline{1,n}, j=\overline{1,m} \iff P_{ij} = p_i \cdot q_j$

### Media variatiei $X \cdot Y$

$E(X \cdot Y) = \displaystyle\sum_{i=1}^n\sum_{j=1}^m x_i y_j p_{ij}$

### Covariatia variabilelor $X$ si $Y$

$Cov(X, Y) = E(X\cdot Y) - E(X)E(Y)$

### Coeficientul de corelatie al variabilelor $X$ si $Y$

$\rho_{XY} = \displaystyle\frac{Cov(X, Y)}{\sqrt{Var(X)} \sqrt{Var(Y)}}$

$\rho_{XY} \in [-1, 1]$

### Exemplu

- $X$ ia valorile $0, 1, 2$
- $Y$ ia valorile $-1, 1$

$X/Y$|$-1$|$1$
---|---|---
0|$\displaystyle\frac{1}{6}$|$\displaystyle\frac{1}{6}$
1|$\displaystyle\frac{1}{12}$|$\displaystyle\frac{3}{12}$
2|$0$|$\displaystyle\frac{1}{3}$

a) Repartitia lui $X$

$P(x = 0) = \frac{1}{6} + \frac{1}{6} = \frac{1}{3}\\
P(x = 1) = \frac{1}{12} + \frac{3}{12} = \frac{1}{3} \\
P(x = 2) = \frac{1}{3}$

$X: \begin{pmatrix}0 & 1 & 2 \\ 
\frac{1}{3} & \frac{1}{3} & \frac{1}{3}
\end{pmatrix}$

b) Repartitia lui $Y$

$P(y = -1) = \frac{1}{6} + \frac{1}{12} + 0 = \frac{1}{4}\\
P(y = 1) = \frac{1}{6} + \frac{3}{12} + \frac{1}{3} = \frac{3}{4}$

$Y: \begin{pmatrix}-1 & 1 \\ 
\frac{1}{4} & \frac{3}{4}
\end{pmatrix}$

c) Sunt variabilele $X$ si $Y$ independente?

$P(X = 0; Y = 1) \ne P(X = 0) \cdot P(Y = 1) \implies X$ si $Y$ sunt dependente

d) $Cov(X, Y)$ si $\rho_{XY}$

$Cov(X, Y) = E(X\cdot Y) - E(X)E(Y)$

$E(XY) = 0 \cdot (-1) \cdot \frac{1}{6} + 0 \cdot 1 \cdot \frac{1}{6} + 1 \cdot (-1) \cdot \frac{1}{12} + 1 \cdot 1 \cdot \frac{3}{12} + 2 \cdot (-1) \cdot 0 + 2 \cdot 1 \cdot \frac{1}{3} = -\frac{1}{12} + \frac{3}{12} + \frac{2}{3} = \frac{10}{12}$

$E(X) = 0 \cdot \frac{1}{3} + 1 \cdot \frac{1}{3} + 2 \cdot \frac{1}{3} = 1\\
E(Y) = -1 \cdot \frac{1}{4} + \frac{3}{4} = \frac{1}{2}$

$E(X^2) = 0^2 \cdot \frac{1}{3} + 1^2 \cdot \frac{1}{3} + 2^2 \cdot \frac{1}{3} = \frac{1}{3} + \frac{4}{3} = \frac{5}{3}\\
E(Y^2) = (-1)^2 \cdot \frac{1}{4} + 1^2 \frac{3}{4} = 1$

$Var(X) = E(X^2) - (E(X))^2 = \frac{5}{3} - 1 = \frac{2}{3}\\
Var(Y) = E(Y^2) - (E(Y))^2 = 1 - \frac{1}{4} = \frac{3}{4}$

$Cov(X,Y) = \frac{10}{12} - \frac{1}{2} = \frac{1}{3}$

$\rho_{XY} = \displaystyle\frac{Cov(X,Y)}{\sqrt{Var(X)}\sqrt{Var(Y)}} = \frac{\frac{1}{3}}{\sqrt{\frac{2}{3} \cdot \frac{3}{4}}} = \frac{\sqrt{2}}{3}$

