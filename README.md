# Minimax Random Reshuffling in Every Convex Regime

## Abstract

Random reshuffling is the standard implementation of stochastic gradient descent on finite sums, but its finite-time theory was incomplete. A recent upper bound shows that, for every reasonable constant step size and every number of epochs, averaging all within-epoch iterates incurs

$$
\frac{D^2}{\eta nK} + \min\\{\eta,\eta^2 nL\\}\sigma_\star^2 .
$$

It was open whether this interpolation between stochastic gradient descent and reshuffling is sharp.

We prove a matching lower bound after the natural smoothness cap. Consequently, the minimax error of optimally tuned constant-step random reshuffling is

$$
\Theta\left( \min\left\\{ LD^2,\ \frac{LD^2}{nK} + \min\left\\{ \frac{\sigma_\star D}{\sqrt{nK}},\ \left(\frac{L\sigma_\star^2 D^4}{nK^2}\right)^{1/3} \right\\} \right\\} \right) .
$$

The result holds for every $K$ and every $n\ge 32$. It closes both restrictions in the previous convex lower bound, which needed $\eta=O(1/(nL))$ and many epochs and concerned epoch endpoints. We also match the separate average and maximum component smoothness parameters whenever the effective active count $n\bar L/\widehat L$ is at least a constant.

The proof uses an asymmetric random-permutation bridge. Its new ingredient is to set the active curvature to $\ell=\min\\{L,1/(161\eta n)\\}$. The same small-effective-step bridge then produces $\eta^2 nL\sigma_\star^2$ for small steps and $\eta\sigma_\star^2$ for large steps. A common contraction inequality controls every within-epoch iterate, while an orthogonal deterministic coordinate covers the finite-horizon transient. The hard instances are three-dimensional, component convex, and have exact smoothness and variance parameters.

## Main results

**Theorem (All-regime fixed-step lower bound).** There is a universal $c>0$ such that, for every $n\ge 32$, $K\ge 1$, $L,D,\sigma>0$, and $0<\eta\le 1/(6L)$, there is an instance in $\mathcal{F}_n(L,D,\sigma)$ with $\sigma_\star=\sigma$, $\lVert x_{1,0}-x_\star\rVert=D$, and component smoothness exactly $L$ for which

$$
\mathbb{E}[f(\bar x)-f(x_\star)] \ge c\min\left\\{ LD^2,\ \frac{D^2}{\eta nK} + \min\\{\eta,\eta^2 nL\\}\sigma^2 \right\\} .
$$

The instance has dimension three. It may depend on the tested step $\eta$, as is standard for a minimax lower bound.

**Theorem (Heterogeneous minimax rate).** If $n\bar L/\widehat L\ge 34$, then

$$
\mathfrak{M}_{n,K}(\bar L,\widehat L,D,\sigma) \asymp \min\left\\{ \bar L D^2,\ \frac{\widehat L D^2}{nK} + \min\left\\{ \frac{\sigma D}{\sqrt{nK}},\ \left(\frac{\bar L\sigma^2 D^4}{nK^2}\right)^{1/3} \right\\} \right\\} .
$$

The constants are universal.

## Files

- `main.pdf` — the paper.
- `supplement.pdf` — full proofs and supporting lemmas.
- `*.ots` — OpenTimestamps proofs establishing the existence date of each file.
