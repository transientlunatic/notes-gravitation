*************************************
Static models with spherical symmetry
*************************************

Orthogonal Metrics
==================

An orthogonal metric takes the form

.. math::

   \label{eq:78}
     \tensor{g}{_{\alpha \beta}} = 0 \qquad\forall\alpha \neq \beta

 implying that there are no cross-terms in the invariant interval. Thus

.. math::

   \label{eq:79}
     \dd{s}^2 = \tensor{g}{_{\alpha \alpha}} (\dd{x}^{\alpha})^2

 The components of a metric will not be orthogonal in every coordinate
system; suppose that :math:`\tensor{g}{_{\alpha \beta}}` are the metric
components in a particular coordinate system where the metric is
orthogonal. Let :math:`\tensor{g'}{_{\mu \nu}}` be the components of the
metric in another coordinate system, then

.. math::

   \begin{aligned}
     \label{eq:80}
     \tensor{g'}{_{\mu \nu}} &= \pdv{x^{\alpha}}{x'^{\mu}} \pdv{x^{\beta}}{x'^{\nu}} \tensor{g}{_{\alpha \beta}} \\
   &= \pdv{x^{\alpha}}{x'^{\mu}} \pdv{x^{\alpha}}{x'^{\nu}} \tensor{g}{_{\alpha \alpha}} \\
   {  \mathrel{{\ooalign{\hidewidth$\not\phantom{=}$\hidewidth\cr$\implies$}}}}\tensor{g'}{_{\mu \nu}} &= 0 \qquad \forall \mu' \neq \nu' \nonumber\end{aligned}

The orthogonal metric components are closely related to the question of
whether the coordinate system has orthogonal basis vectors. If we have a
coordinate system with basis vectors :math:`\set{\vec{e}_i}`, and two
vectors :math:`\vec{A} = A^i \vec{e}_i`,
:math:`\vec{B} = B^i \vec{e}_i`, then

.. math:: \vec{A} \vdot \vec{B} = (A^i \vec{e}_i) \vdot (B^j \vec{e}_j) = A^i B^j (\vec{e}_i \vdot \vec{e}_j)

 so it follows

.. math:: \tensor{g}{_{ij}} = \vec{e}_i \vdot \vec{e}_j

 and :math:`\tensor{g}{_{ij}} = 0` iff :math:`\vec{e}_i` and
:math:`\vec{e}_j` are orthogonal.

We normally want to choose a coordinate system in which the metric
coefficients are orthogonal, to simplify the expressions for geometrical
objects; if the contravariant metric components are orthogonal then the
diagonal terms are simply the reciprocal of the covariant diagonal
terms. To see this, we know

.. math:: g^{\gamma \beta} g_{\gamma\gamma} = \delta^{\beta}_{\gamma} \quad\therefore \quad  g^{\gamma\gamma} = \frac{1}{g_{\gamma \gamma}}

 The Christoffel symbols also take a simple form in an orthogonal
metric,

.. math::

   \begin{aligned}
       \label{eq:109}
       \Gamma^{\lambda}_{\mu \nu} &= 0 \qquad \text{for } \lambda, \mu, \nu \text{ all different.} \\
       \Gamma^{\lambda}_{\lambda \mu} = \Gamma^{\lambda}_{\mu \lambda} &= \quad \frac{g_{\lambda\lambda , \lambda}}{2 g_{\lambda \lambda}}\\
       \Gamma^{\lambda}_{\mu \mu} &= - \frac{g_{\mu \mu, \lambda}}{2 g_{\lambda \lambda}} \\
       \Gamma^{\lambda}_{\lambda \lambda} &= \quad \frac{g_{\lambda
           \lambda, \lambda}}{2 g_{\lambda \lambda}}
     \end{aligned}

For an affine parameter :math:`s` the geodesic equation takes the form

.. math:: \dv{s} \qty( g_{\lambda \nu} \dv{x^{\nu}}{s} ) - \half \pdv{g_{\mu \nu}}{x^{\lambda}} \dv{x^{\mu}}{s} \dv{x^{\nu}}{s} = 0

 for an orthogonal metric this reduces to

.. math::

   \label{eq:112}
     \dv{s} \qty( g_{\lambda \lambda} \dv{x^{\lambda}}{s} ) - \half 
     \pdv{g_{\mu \mu}}{x^{\lambda}} \qty( \dv{x^{\mu}}{s} )^2 = 0

Spherically symmetric metrics
=============================

Spherically symmetric solutions to the field equations are suitable for
describing the spacetime inside and around stars. In flat Minkowski
spacetime a polar coordinate system can be used to give an invariant
interval

.. math::

   \label{eq:115}
     \dd{s}^2 = - \dd{t}^2 + \dd{r}^2 + r^2 \qty( \dd{\theta}^2 + \sin^2{\theta} \dd{\phi}^2 )

 Surfaces of constant :math:`r` and :math:`t` have the geometry of a
2-sphere with an interval

.. math::

   \label{eq:116}
     \dd{\ell}^2 = r^2 \qty( \dd{\theta}^2 + \sin^2{\theta} \dd{\phi}^2 )

 Thus a spacetime is spherically symmetric if every point in the
spacetime lies on a 2D surface which is a 2-sphere. Labelling the
coordinates :math:`(r', t, \theta, \phi)` then every point in a
spherically symmetric spacetime lies on a 2D surface, given by

.. math::

   \label{eq:117}
     \dd{\ell}^2 = f(r', t) \qty[ \dd{\theta}^2 + \sin^2{\theta} \dd{\phi}^2]

 with :math:`\sqrt{f}` the radius of curvature of the 2-sphere.

In curved spacetime there is no trivial relation between the angular
coordinates of the two-sphere and the remaining coordinates at each
point in spacetime, but if we define

.. math::

   \label{eq:118}
     r^2  = f(r', t)

 and we can line-up the origins of the 2-sphere coordinate systems
:math:`(\theta, \phi)` for points in spacetime with different values of
:math:`r`. Spherical symmetry requires that any radial path in the space
is orthogonal to the 2D spheres on which the points along the radial
path lie, implying

.. math::

   \label{eq:119}
     g_{r \theta} = g_{r \phi} = 0

 So the spacetime metric is reduced to the form

.. math::

   \label{eq:120}
     \begin{split}
       \dd{s^2} = g_{tt} \dd{t^2} + 2 g_{tr} \dd{r}\dd{t} + 2 g_{t
         \theta} \dd{\theta}\dd{t} \\+ g_{rr} \dd{r^2} + r^2
       \qty(\dd{\theta^2} + \sin[2](\theta) \dd{\phi^2})
     \end{split}

 Considering the curve with :math:`r`, :math:`\theta`, and :math:`\phi`
are constant, which is a worldline of a particle in spacetime with
constant spatial coordinates; this curve must also be orthogonal to
2-spheres on which each point lies, otherwise there would be a preferred
direction in spacetime. Thus

.. math::

   \label{eq:121}
     g_{t\theta} = g_{t \phi} = 0

 so the general form for a metric in a spherically symmetric spacetime
is

.. math::

   \label{eq:122}
     \begin{split}
       \dd{s^2} = g_{tt} \dd{t^2} + 2 g_{tr} \dd{r}\dd{t} + g_{rr}
       \dd{r^2} \\+ r^2 \qty( \dd{\theta^2} + \sin[2](\theta)
       \dd{\phi^2})
     \end{split}

 For :math:`g_{tt}`, :math:`g_{tr}`, and :math:`g_{rr}` arbitrary
functions of :math:`r` and :math:`t`.

Static Spacetime
================

In s static spherically symmetric spacetime we can find a time
coordinate :math:`t` where

#. all metric components are independent of :math:`t`

#. the metric is unchanged under a time-reversal operation, :math:`t \to
     -t`.

The second property implies :math:`g_{tr}=0`, meaning that the interval
is

.. math::

   \label{eq:123}
     \dd{s^2} = - e^{\nu} \dd{t^2} + e^{\lambda} \dd{r^2} + r^2 \qty(\dd{\theta^2} + \sin[2](\theta) \dd{\phi^2})

 which is orthogonal. The functions :math:`\nu(r)` and
:math:`\lambda(r)` replace :math:`g_{tt}` and :math:`g_{rr}`,since the
exponential function is strictly positive for all :math:`r`, this is
legitimate, provided :math:`g_{tt}<0` and :math:`g_{rr}>0`.

The Christoffel symbols for this spacetime are

.. math::

   \begin{aligned}
       \label{eq:124}
       \Gamma^t_{rt}=\Gamma^t_{tr} &= \half \nu' & \Gamma^{\theta}_{r \theta} = \Gamma^{\theta}_{\theta r} &= \frac{1}{r} \\
       \Gamma^r_{tt} &= \half \nu' e^{\nu-\lambda} & \Gamma^{\theta}_{\phi \phi} &= - \sin(\theta) \cos(\theta) \\
       \Gamma^r_{rr} &= \half \lambda' & \Gamma^{\phi}_{r \phi} = \Gamma^{\phi}_{\phi r} &= \frac{1}{r} \\
       \Gamma^r_{\theta \theta} &= - r e^{- \lambda} &
       \Gamma^{\phi}_{\theta \phi} = \Gamma^{\phi}_{\phi \theta} &=
       \cot(\theta)
     \end{aligned}

.. math:: \Gamma^r_{\phi\phi}  = -r e^{-\lambda} \sin[2](\theta)

The Ricci tensor is given by

.. math::

   \label{eq:125}
     R_{\lambda \nu} = \Gamma^{\tau}_{\lambda \nu} \Gamma^{\sigma}_{\tau\sigma} - \Gamma^{\tau}_{\lambda \sigma} \Gamma^{\sigma}_{\tau\nu} + \Gamma^{\sigma}_{\lambda\nu,\sigma} - \Gamma^{\sigma}_{\lambda\sigma,\nu}

 so

.. math::

   \begin{aligned}
       \label{eq:126}
       R_{tt} &= \half e^{\nu-\lambda} \qty( \nu'' + \half \nu'^2 - \half \nu' \lambda' + \frac{2}{r} \nu') \\
       \label{eq:129}
       R_{rr} &= - \half \qty( \nu'' + \half \nu'^2 - \half \nu' \lambda' - \frac{2}{r} \lambda') \\
       \label{eq:130}
       R_{\theta\theta} &= 1 - e^{-\lambda} \qty[1+\frac{r}{2}(\nu'-\lambda')] \\
       \label{eq:131}
       R_{\phi\phi}&= R_{\theta\theta} \sin[2](\theta)
     \end{aligned}

The Schwarzschild metric
========================

We can derive the metric for the spacetime exterior to a star from the
static spherically symmetric metric; the Schwarzchild metric; if the
star is in an isolated region of space we can assume all components of
the Ricci tensor to be zero, so

.. math::

   \label{eq:127}
     e^{\lambda-\nu}R_{tt}+R_{rr} = \frac{\nu'+\lambda'}{r}=0

 which implies that :math:`\nu+\lambda` is constant. At a large distance
from the star the metric should reduce to special relativity, so as

.. math:: r \to \infty, \quad e^{\nu}\to 1, e^{\lambda} \to 1 \implies \nu \to 0, \lambda \to 0

 and so :math:`\nu+\lambda=0`, giving

.. math::

   \label{eq:128}
     e^{\nu} = e^{-\lambda}

 This lets us eliminate :math:`\nu` from the :math:`R_{\theta\theta}`
expression, equation , so

.. math::

   \label{eq:132}
     e^{-\lambda} (1-\lambda'r) = 1 \implies \dv{r} \qty(r e^{-\lambda})=1

 Integrating this we get

.. math::

   \label{eq:133}
     e^{\nu} = e^{-\lambda} = 1 + \frac{\alpha}{r}

 where :math:`\alpha` is a constant.

Consider a material test particle, with so little rest mass that it does
not disturb the metric, which is released from rest, then

.. math::

   \label{eq:134}
     \dd{x^j}{\tau} = 0 \quad j = 1,2,3

 for :math:`\tau` the proper time, and

.. math::

   \label{eq:135}
     \dv{x^0}{\tau} \equiv \dv{t}{\tau} \neq 0

 Realling that

.. math:: g_{\alpha\beta} \dv{x^{\alpha}}{\tau} \dv{x^{\beta}}{\tau} = -1

 then

.. math::

   \label{eq:136}
     \dv{t}{\tau} = e^{- \frac{\nu}{2}}

 Applying the geodesic equations, equation , at the instance that the
particle is released this reduces to

.. math::

   \label{eq:137}
     \dv[2]{r}{\tau} + \Gamma_{tt}^r \qty( \dv{t}{\tau})^2 =0

 Substituting the Christoffel symbol and equation we obtain

.. math::

   \label{eq:138}
     \dv[2]{r}{t} = \frac{\alpha}{2 r^2}

 In the limit of a weak field this reduces to Newtonian gravity,

.. math::

   \label{eq:139}
     \dv[2]{r}{t} = - \frac{GM}{r^2}

 for :math:`M` the mass of the star, meaning :math:`\alpha = -2GM =-2M`
for :math:`G=1`. Thus the invariant interval is

.. math::

   \label{eq:140}
   \begin{split}
     \dd{s^2} = - \qty(1-\frac{2M}{r}) \dd{t^2} + \frac{\dd{r^2}}{\qty(1-\frac{2M}{r})} \\
   + r^2 \dd{\theta^2} + r^2 \sin[2](\theta) \dd{\phi^2}
   \end{split}
