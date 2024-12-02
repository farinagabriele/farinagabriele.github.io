layout: post
title: "Forma implicita ed esplicita in Zeta"
categories: TdS
tags: Control Egineering
---
# Forma implicita

$$
\begin{cases}
x(t+1) = Ax(t) + Bu(t)\\
y(t) = Cx(t) + Du(t) \\
\end{cases}
$$

<!--excerpt-->
Applichiamo la trasformata Zeta ad entrambe le relazioni ambo i membri

$$
\begin{cases}
\mathcal{Z}\{x(t+1)\} = \mathcal{Z}\{Ax(t) + Bu(t)\}\\
\mathcal{Z}\{y(t)\} = \mathcal{Z}\{Cx(t) + Du(t)\} \\
\end{cases}
$$

Applicando le proprietà di linearità e ritardo unitario otteniamo

$$
\begin{cases}
zX(z) - zx(0) = AX(z) + BU(z)\\
Y(z) = CX(z) + DU(z) \\
\end{cases}
$$

Consideriamo solo la prima relazione

$$

(zI-A)X(z) = zx(0) + BU(z)\\

$$

$$

X(z) = z(zI-A)^{-1}x(0) + (zI-A)^{-1}BU(z)\\

$$

# Forma Esplicita

$$
\begin{cases}
x(t)=\Phi(t)x_0 + \sum_{\tau = 0}^{t-1}\mathcal{H}(t-\tau)u(\tau)\\ \\
y(t) = \Psi(t)x_0 + \sum_{\tau = 0}^{t-\tau}W(t-\tau)u(\tau)

\end{cases}
$$

