---
layout: post
title: "Teoria stabilità interna T.D."
categories: TdS
tags: Control Egineering
---
## Def. punto di equilibrio

$$
\begin{align*}
x(t+1) = f(x,u) \\
x_e \ | \  f(x_e, 0) = x_e
\end{align*}
$$

<!--excerpt-->


## Definizioni epsilon-delta

$$
\begin{align*}
\text{S.A: } \ \forall \varepsilon >0 \ \exists \delta_{\varepsilon}>0 : \ \|x_0-x_e\| \leq \delta_{\varepsilon} \Rightarrow \|x(t)-x_e\| \leq \varepsilon \\
\text{S.S: } \ \text{S.A} \ + \lim_{t \to \infty} \|x(t)-x_e\| =0 \\ 
\text{Inst: } \ \exists \varepsilon >0 \ | \ \forall \delta_{\varepsilon}>0 \ \exists \ x_0: \ \|x_0-x_e\| \leq \delta_{\varepsilon} \bigwedge\|x(t)-x_e\| > \varepsilon
\end{align*}
$$

## Linearizzazione attorno a punti di equilibrio

$$
x(t+1) = f(x,u)= f(x_e,0) +\frac{\partial}{\partial x}f(x,u)|_{x =x_e \ u = 0}(x-x_e) + +\frac{\partial}{\partial u}f(x,u)|_{x =x_e \ u = 0}u + o(\|x\|, \|u\|) \\  \\
\boxed{A = \frac{\partial}{\partial x}f(x,u)|_{x =x_e \ u = 0} \ \ \ B = \frac{\partial}{\partial u}f(x,u)|_{x =x_e \ u = 0}} \\ \\
\text{posto } z(t) = x(t) - x_e \Rightarrow z(t+1)=x(t+1)- x_e \\ 
\boxed{z(t+1) = Az + Bu}
$$

### I Teo. Lyapunov

$$
\begin{align}
z=0 \ \text{ S.A. } \Rightarrow \ x_e  \ \text{ S.A. }  \\
z=0 \ \text{ Inst. } \Rightarrow \ x_e  \ \text{ Inst. } \\
z=0 \ \text{ S.S. Nulla si può dire} 
\end{align}
$$

## Stabilità LTI

$$
\begin{align}
\text{S.A: } \|\Phi(t)\|\le \Phi_0 \ \bigwedge \ \lim_{t \to \infty} {\Phi(t)} = 0  \iff |\text{Re}(\Lambda)| < 1 \\
 \text{S.S: } \|\Phi(t)\|\le \Phi_0 \iff \ |\text{Re}(\Lambda)| \le 1\\ 
\text{Inst: } \ldots \iff \exists \lambda \in \Lambda \ | \ \ \text{Re}(\lambda) > 1
\end{align}
$$

## Teo. Lyapunov

$$
\begin{align}
\text{S.A: } V(x(t)) > 0 \ \bigwedge \ V(x(t+1)) - V(x(t)) < 0 \ \text{ in } \ I_{x_e}\\
 \text{S.S: } V(x(t)) > 0 \ \bigwedge \ V(x(t+1)) - V(x(t)) \le 0 \ \text{ in } \ I_{x_e}\\ 
\text{Inst: } V(x(t)) > 0 \ \bigwedge \ V(x(t+1)) - V(x(t)) > 0 \ \text{ in } \ I_{x_e}\\
\end{align}
$$

### Funzione candidata più semplice

$$
V(x(t)) = \frac{1}{2}(x(t) - x_e)^TM(x(t) - x_e) \ \text{ con } \ M >0
$$

## Teo. Lyapunov LTI

$$
\begin{multline}
\text{Se } \exists ! \ Q > 0 \ \ \text{    e simmetrica soluzione di:} \\
A^TQA - Q = -P \\
\text{comunque presa } P>0 \ \ \text{  (simmetrica)}\\
\text{allora } x_e=0 \text{ è stabile asintoticamente.} \\
\text{Vale anche il viceversa.}
\end{multline}
$$


