layout: post
title: "Teoria stabilità interna T.C."
categories: TdS
tags: Control Egineering
---
## Def. punto di equilibrio

$$
\begin{multline}
\dot{x} = f(x,u) \\
x_e \ | \  f(x_e, 0) = 0
\end{multline}
$$

<!--excerpt-->
## Definizioni epsilon-delta

$$
\begin{multline}
\text{S.A: } \ \forall \varepsilon >0 \ \exist \delta_{\varepsilon}>0 : \ \|x_0-x_e\| \leq \delta_{\varepsilon} \Rightarrow \|x(t)-x_e\| \leq \varepsilon \\
\text{S.S: } \ \text{S.A} \ + \lim_{t \to \infty} \|x(t)-x_e\| =0 \\ 
\text{Inst: } \ \exist \varepsilon >0 \ | \ \forall \delta_{\varepsilon}>0 \ \exist \ x_0: \ \|x_0-x_e\| \leq \delta_{\varepsilon} \bigwedge\|x(t)-x_e\| > \varepsilon
\end{multline}
$$

## Linearizzazione attorno a punti di equilibrio

$$
\begin{multline}
\dot{x} = f(x,u)= \cancel{f(x_e,0)} +\frac{\partial}{\partial x}f(x,u)|_{x =x_e \ u = 0}(x-x_e) + +\frac{\partial}{\partial u}f(x,u)|_{x =x_e \ u = 0}u + o(\|x\|, \|u\|) \\  \\
\boxed{A = \frac{\partial}{\partial x}f(x,u)|_{x =x_e \ u = 0} \ \ \ B = \frac{\partial}{\partial u}f(x,u)|_{x =x_e \ u = 0}} \\ \\
\text{posto } z = x - x_e \Rightarrow \dot{z}=\dot{x} \\ 
\boxed{\dot{z} = Az + Bu}
\end{multline}
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
\text{S.A: } \|\Phi(t)\|\le \Phi_0 \ \bigwedge \ \lim_{t \to \infty} {\Phi(t)} = 0  \iff \text{Re}(\Lambda) < 0 \\
 \text{S.S: } \|\Phi(t)\|\le \Phi_0 \iff \text{Re}(\Lambda) \le 0\\ 
\text{Inst: } \ldots \iff \exist \lambda \in \Lambda \ | \ \text{Re}(\lambda) > 0
\end{align}
$$

## Teo. Lyapunov

$$
\begin{align}
\text{S.A: } V(x) > 0 \ \bigwedge \ \dot{V}(x) < 0 \ \text{ in } \ I_{x_e}\\
 \text{S.S: } V(x) > 0 \ \bigwedge \ \dot{V}(x) \le 0 \ \text{ in } \ I_{x_e}\\ 
\text{Inst: } V(x) > 0 \ \bigwedge \ \dot{V}(x) > 0 \ \text{ in } \ I_{x_e}\\
\end{align}
$$

### Funzione candidata più semplice

$$
V(x) = \frac{1}{2}(x - x_e)^TM(x - x_e) \ \text{ con } \ M >0
$$

## Teo. Lyapunov LTI

$$
\text{Se } \exist! \ Q > 0 \ \ \text{    e simmetrica soluzione di:} \\
A^TQ + QA = -P \\
\text{comunque presa } P>0 \ \ \text{  (simmetrica)}\\
\text{allora } x_e=0 \text{ è stabile asintoticamente.} \\
\text{Vale anche il viceversa.}
$$

