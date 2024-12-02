---
layout: post
title: "Criterio di Routh"
categories: TdS
tags: Control Egineering
---
# Premesse

Consideriamo un polinomio di grado n

$$
p(\lambda) = a_n\lambda^n + a_{n-1}\lambda^{n-1} + \ldots +a_1\lambda + a_0 \ \ \ \ (i)
$$

Nella sua forma fattorizzata

$$
p(\lambda)=a_n(\lambda-\lambda_1)\cdots(\lambda-\lambda_n)
$$


<!--excerpt-->
# Premesse

Consideriamo un polinomio di grado n

$$
p(\lambda) = a_n\lambda^n + a_{n-1}\lambda^{n-1} + \ldots +a_1\lambda + a_0 \ \ \ \ (i)
$$

Nella sua forma fattorizzata

$$
p(\lambda)=a_n(\lambda-\lambda_1)\cdots(\lambda-\lambda_n)
$$

Supponiamo che abbia tutte radici con parte reale negativa

$$
p(\lambda)=a_n(\lambda+|\lambda_1|)\cdots(\lambda+|\lambda_n|)  \ \ \ \ (ii)
$$

Qualora vi siano termini associati a radici complesse e coniugate

$$
(\lambda - \lambda_i)(\lambda-\lambda_i^*)=[(\lambda +|\alpha|)^2+\omega^2]
$$

Se si svolge la $(ii)$ per riottenere la $(i)$ ogni termine è somma di prodotti tra quantità positive moltiplicate per $a_n$, quidni

## CN tutte radici a parte reale negativa

Se un polinomio ha tutte radici a parte reale negativa allora è completo e tutti i suoi coefficienti hanno lo stesso segno (quello di $a_n$).

### Oss. 1

La mancanza di qualche coefficiente può solo significare la presenza di qualche radice a parte reale positiva o nulla

### Oss. 2

La presenza di qualche coefficiente con segno diverso da $a_n$ implica la presenza di qualche radice a parte reale positiva

# Criterio di Routh

$$
p(\lambda) = a_n\lambda^n + a_{n-1}\lambda^{n-1} + \ldots +a_1\lambda + a_0
$$

Costruiamo la seguente tabella

$$
\begin{multline}
n \ \ \ \ | \ a_n \ a_{n-2} \ a_{n-4} \ \ \ \ \ \ldots \\
n-1 \ | \ a_{n-1} \ a_{n-3} \ a_{n-5} \ \ldots \\
n-2 \ | \ b_{n-2} \ b_{n-3} \ b_{n-4} \ \ldots \\
n-3 \ | \ c_{n-3} \ c_{n-4} \ c_{n-5} \ \ldots \\
\vdots \\
1 \ | \ r_1 \\
0 \ | \ s_1
\end{multline}
$$

Dove i coefficienti delle righe successive si calcolano come:

$$
b_1 = \frac{\begin{vmatrix} a_n & a_{n-2} \\
a_{n-1} & a_{n-3}
\end{vmatrix} }
{-a_{n-1}} \ \ \ \ 
b_2 = \frac{\begin{vmatrix} a_n & a_{n-4} \\
a_{n-1} & a_{n-5}
\end{vmatrix} }
{-a_{n-1}} \ \ \ \ \ldots
$$

$$
c_1 = \frac{\begin{vmatrix} a_{n-1} & a_{n-3} \\
b_{n-2} & b_{n-3}
\end{vmatrix} }
{-b_{n-2}} \ \ \ \ c_2 = \frac{\begin{vmatrix} a_{n-1} & a_{n-5} \\
b_{n-2} & b_{n-4}
\end{vmatrix} }
{-b_{n-2}} \ \ \ \ \ldots
$$

E così via fino ad esaurire tutti i termini.

## Teorema di Routh

La prima colonna $a_n, \ a_{n-1}, \ b_{n-2}, \ c_{n-3}, \ldots$ si interpreta come i coefficienti del polinomio nella regola di Cartesio.

Il polinomio ha tutte radici a parte reale negativa $\iff$ci sono solo permanenze.

Ad ogni variazione corrisponde una radice a parte reale positiva.

## Operazioni ammissibili

E’ possibile moltiplicare una riga della tabella per uno scalare strettamente positivo.

## Casi di eccezione (i)

Una riga (dispari) ha $j-1$ zeri e poi elementi non nulli.

Sostituire tale riga  con una ottenuta sommando all’i-esimo elemento della riga l’elemento di posto $(i+j)$ della stessa riga moltiplicati per $(-1)^j$.

Ex.

$$
3 \ |\  0 \ 1  \Rightarrow 3 \ |\ -1 \ 1
$$

## Caso di eccezione (ii)

Una riga (dispari) ha tutti zeri.

Considerare il polinomio quadratico associato alla riga superiore: sostituire la riga con tutti zeri con i coefficienti del polinomio quadratico derivato.

Ex.

$$
\begin{multline}
4 \ | \ 1 \ 3 \ 1 \ \\
3 \ | \ 0 \ 0
\end{multline}
$$

Il polinomio quadratico è 

$$
p^{(4)}(\lambda) = \lambda ^ 4 + 3\lambda ^ 2 + 1
$$

Derivando si ottiene

$$
\frac{d}{d\lambda}p^{(4)}(\lambda) = 4\lambda^3 + 6 \lambda
$$

La nuova riga 3 diventa

$$
3 \ | \ 4 \ 6
$$

