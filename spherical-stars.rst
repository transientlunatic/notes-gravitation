*************************
Models of spherical stars
*************************

In Newtonian theory the stability of stars is described in terms of
hydrostatic equilibrium. In the framework of General Relativity this is
similar, leading to the Oppenheimer-Volkoff equation.

Components of the Einstein tensor
=================================

The stellar interior will have a metric of the form

.. math::

   \dd{s}^2 = -e^\nu \dd{t}^2 + e^{\lambda} \dd{r}^2 + r^2 \qty(
   \dd{\theta}^2 + \sin[2](\theta) \dd{\phi}^2 )

where :math:`\nu` and :math:`\lambda` are functions of :math:`r`. The
Ricci tensor will have components

.. math::

   \label{eq:193}
     R_{tt} = \half e^{\nu-\lambda} \qty( \nu'' + \half \nu'^2 - \half \nu' \lambda' + \frac{2}{r} \nu')

.. math::

   \label{eq:201}
     R_{rr} = - \half \qty( \nu'' + \half \nu'^2 - \half \nu' \lambda' - \frac{2}{r} \lambda')

.. math::

   \label{eq:202}
     R_{\theta \theta} = 1 - e^{- \lambda} \qty( 1 + \frac{r}{2} ( \nu' - \lambda') )

.. math::

   \label{eq:203}
     R_{\phi \phi} = R_{\theta \theta} \sin[2](\theta)

with all other components zero. The metric is orthogonal, so

.. math::

   \begin{aligned}
       g^{tt} &= - e^{- \nu} \\ g^{rr} &= e^{- \lambda} \\ g^{\theta \theta} &= r^{-2} \\ g^{\phi \phi} &= (r^2 \sin[2](\theta) )^{-1}
     \end{aligned}

again, with all other terms zero. The Ricci and metric tensors are
orthogonal, so the Ricci scalar has the expression

.. math::

   \label{eq:204}
     R = g^{\mu \nu} R_{\mu \nu} = g^{tt}R_{tt} + g^{rr} R_{rr} + g^{ \theta \theta} R_{\theta \theta} + g^{\phi \phi} R_{ \phi \phi}

 after making the appropriate substitutions, we find

.. math::

   \label{eq:205}
     \begin{split}
       R = - e^{-\lambda} \qty[ \qty( \nu'' + \half \nu'^2 - \half \nu' \lambda' ) + \frac{\nu' - \lambda'}{r}]\\
   {}+\frac{2}{r^2} \qty[1 - e^{- \lambda} \qty( 1+ \frac{(\nu' - \lambda')r}{2})]
     \end{split}

 The fully covariant Einstein tensor is

.. math:: G_{\mu \nu} = R_{\mu \nu} - \half g_{\mu \nu} R

 so

.. math::

   \begin{aligned}
       G_{tt} &= \frac{e^{\nu}}{r^2} \qty[ 1+ e^{-\lambda} (r \lambda' -1) ] \\
   G_{rr} &= \frac{\nu'}{r} - \frac{e^{\lambda}}{r^2} \qty( 1 - e^{- \lambda}) \\
   G_{\theta \theta} &= r^2 e^{- \lambda} \qty[ \frac{\nu''}{2} + \frac{\nu'^2}{4} - \frac{\nu' \lambda'}{4} + \frac{\nu'-\lambda'}{2r}] \\
   G_{\phi \phi} &= \sin[2](\theta) G_{\theta \theta}
     \end{aligned}

Components of the energy-momentum tensor
========================================

For a perfect fluid the energy-momentum tensor, in fully covariant form
has components

.. math:: T^{\mu \nu} = (\rho + P) u^{\mu} u^{\nu} + P g^{\mu \nu}

for :math:`\rho` the mass-energy density, and :math:`P` the pressure,
while :math:`u^{\mu}` are the four velocity components of a fluid
element. Seeking a static solution has
:math:`u^{i} = 0, i = \set{1,2,3}`, so from the geodesic equation

.. math::

   \label{eq:206}
     g_{tt}(u^t)^2 = -1 \implies u^t = e^{- \frac{\nu}{2}}

 thus

.. math::

   \begin{aligned}
       T_{tt} &= \rho e^{\nu} \\
   T_{rr} &= P e^{\lambda} \\
   T_{\theta \theta} &= P r^2 \\
   T_{\phi \phi} &= P r^2 \sin[2](\theta)
     \end{aligned}

Einstein’s equations
====================

In fully covariant form

.. math:: G_{\mu \nu} = 8 \pi T_{\mu \nu}

 so

.. math::

   \begin{aligned}
   \label{eq:207}
       \frac{e^{\nu}}{r^2} \qty[  1+ e^{-\lambda} (r \lambda' -1) ] &= 8 \pi \rho e^{\nu} \\
   \label{eq:208}
       \frac{\nu'}{r} - \frac{e^{\lambda}}{r^2} (1-e^-\lambda) &= 8 \pi P e^{\lambda} \\
   \label{eq:209}
   r^2 e^{-\lambda} \qty[ \frac{\nu''}{2} + \frac{\nu'^2}{4} - \frac{\nu' \lambda'}{4} + \frac{\nu'-\lambda'}{2r}] &= 8 \pi P r^2
     \end{aligned}

Solution of the first Einstein equation
=======================================

By cancelling the :math:`e^{\nu}` term in equation ([eq:207]), and
rearranging,

.. math::

   \label{eq:210}
     \dv{r} \qty[ r(1-e^{-\lambda})] = 8 \pi \rho r^2

 Then introducing the mass function, :math:`m(r)`, defined as

.. math::

   \label{eq:211}
     \dv{m}{r} = 4 \pi \rho r^2 = \half \dv{r} \qty[r (1-e^{-\lambda})]

 and integrating,

.. math::

   \label{eq:212}
     r(1-e^{-\lambda}) = 2m +C

 where :math:`C` is a constant of integration, equal to zero unless the
star is singular at :math:`r=0`. Thus

.. math::

   \label{eq:213}
     e^{-\lambda} = 1 - \frac{2m}{r}

The Oppenheimer-Volkoff equation
================================

Rearranging equation ([eq:208]), with some straight-forward algebra,

.. math::

   \label{eq:214}
     \dv{\nu}{r} = e^{\lambda} \qty[8 \pi P r + \frac{1}{r} (1-e^{-\lambda})] = 2 \qty[\frac{4 \pi P r^3 + m}{r(r-2m)}]

 Then, considering conservation of mass-energy,
:math:`\tensor{T}{^{\alpha
    \beta}_{;\beta}} = \qty[(\rho +P) u^{\alpha}u^{\beta} + P
g^{\alpha \beta}]_{;\beta}= 0`, then

.. math::

   \label{eq:215}
   \begin{split}
     (\rho + P)_{;\beta} u^{\alpha} u^{\beta} + (\rho+P)(u^{\alpha})_{; \beta} u^{\beta} \\ + (\rho+P) u^{\alpha}(u^{\beta})_{; \beta} + P_{,\beta} g^{\alpha \beta} + Pg^{\alpha \beta}_{; \beta} = 0
   \end{split}

 This is infact a set of four equations, as :math:`\alpha` is a free
index, so with just :math:`\alpha \equiv r`,

.. math::

   \label{eq:215}
   \begin{split}
     (\rho + P)_{;\beta} u^{r} u^{\beta} + (\rho+P)(u^{r})_{; \beta} u^{\beta} \\ + (\rho+P) u^{r}(u^{\beta})_{; \beta} + P_{,\beta} g^{r \beta} + Pg^{r \beta}_{; \beta} = 0
   \end{split}

 But since :math:`u^r=0` two of these terms vanish, and the derivatives
of the metric tensor are all zero, so the last term drops out too. We
then have the simplification

.. math::

   \label{eq:216}
     ( \rho +P)(u^r)_{;t} u^t + \dv{P}{r} g^{rr} = 0

 then

.. math::

   \label{eq:217}
     u^r_{;t} = \Gamma^r_{tt} u^t = \half \nu' e^{\nu-\lambda} e^{-\nu/2} = \half e^{-\lambda} \nu' e^{\nu/2}

 Thus

.. math::

   \label{eq:218}
     \half(\rho + P) e^{-\lambda} \dv{\nu}{r} + e^{- \lambda} \dv{P}{r} = 0 \implies \dv{\nu}{r} = - \frac{2}{(\rho+P)} \dv{P}{r}

 and using this to eliminate :math:`\nu'` from equation ([eq:214]),

.. math::

   \label{eq:219}
     \dv{P}{r} = - \frac{(\rho + P)(4 \pi P r^3 + m)}{r(r-2m)}

 which is the *Oppenheimer-Volkoff* equation. In the weak-field limit,
:math:`P \ll \rho` implies :math:`4 \pi P r^3 \ll m`, and the metric
will be almost flat, so :math:`m \ll r`, so this simplifies to

.. math::

   \label{eq:220}
     \dv{P}{r} = - \frac{\rho m}{r^2}

 which is the Newtonian hydrostatic equilibrium equation.

Solving the O-V equation
========================

There are three unknown functions in the O-V equation, :math:`P(r)`,
:math:`\rho(r)`, and :math:`m(r)`, but the latter two are related, so we
need an additional relation, an equation of state, to link all three, in
the form

.. math:: P(r) = P(\rho(r))

 For a fluid which is in local thermodynamic equilibrium there is always
a relation between pressure, density, and entropy, of the form

.. math:: P=P(\rho,S)

 In most astrophysical situations we can regard :math:`S` as constant.
In practice, to solve this system we need boundary conditions.

Take :math:`P=P_0` and :math:`m=0` at :math:`r=0`, and integrate
outwards to :math:`P=0` at the surface of the star, where :math:`r=R`
and :math:`m=M`, where :math:`M` is the mass constant in the exterior
Schwarzschild metric. This then allows us to find :math:`\nu` and
:math:`\lambda` to form a complete expression for the metric inside the
star. The effect of GR compared to Newtonian mechanics will be to
steepen the pressure gradient within the star.

An exact solution for a star with constant density
==================================================

Suppose that the density is constant, and :math:`\rho=\rho_0` (implying,
rather concerningly, an infinite sound speed!), and integrating equation
([eq:211]), and retrieve

.. math::

   \label{eq:221}
     m(r) = \frac{4}{3} \pi \rho_0 r^3

 This can be substituted into the O-V equation, giving

.. math::

   \label{eq:222}
     \dv{P}{r} = - \frac{4}{3} \pi r \frac{(\rho_0+P)(\rho_0 + 3 P)}{(1 - \frac{8 \pi \rho_0 r^2}{3})}

 thus

.. math::

   \begin{aligned}
     \label{eq:223}
     \frac{\dd{P}}{(\rho_0 +P)(\rho_0 + 3P)} &= \frac{1}{2 \rho_0} \qty[\frac{3 \dd{P}}{(\rho_0 + 3P)} - \frac{\dd{P}}{(\rho_0 +P)}] \\ &= - \frac{4 \pi}{3} \frac{r \dd{r}}{\qty(1 - \frac{8 \pi \rho_0 r^2}{3})}\end{aligned}

 and integrating both sides,

.. math::

   \label{eq:224}
     \log( \rho_0 + 3P) - \log(\rho_0 + P) = \half \log(1 - \frac{8 \pi \rho_0 r^2}{3}) + C

 for a constant :math:`C`, which can be written

.. math::

   \label{eq:225}
     \frac{\rho_0 + 3P}{\rho_0+P} = A \qty( 1 - \frac{8 \pi \rho_0 r^2}{3})^{1/2}

 when :math:`r=0` we have :math:`P=P_0`, so we can express :math:`A` in
terms of density and central pressure,

.. math:: A = \frac{\rho_0 + 3 P_0}{\rho_0 +P_0}

 Then

.. math::

   \begin{aligned}
     \label{eq:226}
     \frac{\rho_0 + 3P}{\rho_0 + P} &= \frac{\rho_0 + 3P_0}{\rho_0 + P_0}  \qty( 1 - \frac{8 \pi \rho_0 r^2}{3})^{1/2} \nonumber\\
   &=  \frac{\rho_0 + 3P_0}{\rho_0 + P_0} \qty( 1 - \frac{2m}{r})^{1/2}\end{aligned}

 at the surface of the star :math:`P=0` so the left hand reduces to
:math:`1`, so

.. math::

   \label{eq:227}
     \frac{\rho_0 + 3P_0}{\rho_0 + P_0} \qty( 1 - \frac{2m}{r})^{1/2} = 1

 for :math:`M` the Schwarzschild mass, and :math:`R` is the coordinate
radius of the star. We can obtain an expression for :math:`P` as a
function of :math:`r` by rearranging,

.. math::

   \label{eq:228}
     P_0 = \frac{\rho_0 \qty[ 1 - \qty( 1 - \frac{2M}{R} )^{1/2}]}{3 \qty( 1 - \frac{2M}{R})^{1/2} - 1}

Buchdahl’s Theorem
==================

From equation ([eq:228]), it can be seen that as :math:`P_0 \to \infty`
when :math:`3 \qty(1- \frac{2M}{R})^{1/2} \to 1`, that is, when
:math:`M/R \to
4/9`. Clearly there can be no static star with uniform density with a
radius smaller than :math:`9M/4`, as they would require an infinite
internal pressure. If we require the exterior metric to be well-behaved
then stars with a radius less than :math:`2M` should be excluded, as the
Schwarzschild metric misbehaves at this point, with timelike intervals
becoming spacelike, and vice versa.

As a result we can exclude the possibility of a uniform static star with
these properties, and *Buchdahl’s theorem* is a rigorous proof of this.
