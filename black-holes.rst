***********
Black Holes
***********

.. include:: macros

Beyond white dwarfs and neutron stars
=====================================

Is it always justified to assume that the centre of a star has a finite
pressure and density? Degenerate remnants represent a class of objects
where the central pressure is only maintained by quantum degeneracies;
what happens if the gravitational collapse is capable of overbalancing
these? This becomes a problem if the coordinate radius of the star
satisfies :math:`r=2M`, at the Schwarzschild surface. At this point the
Schwarzschild metric misbehaves.

The Schwarzschild surface
=========================

In order to understand the misbehaviour of the metric when
:math:`g_{rr} =
2M`, and whether this is a physical problem with spacetime, or a
coordinate problem, we can consider a particle falling across the
:math:`r=2M` surface. Suppose the particle starts at a coordinate radius
:math:`R>2M`, and is released at a coordinate time :math:`t=0`, and
proper time :math:`\tau=0` in the particle’s rest frame. Then

.. math:: \left( \dv{r}{\tau} \right)^2 = k^2 - 1 - \frac{h^2}{r^2} + \frac{2M}{r} \left( 1+ \frac{h^2}{r^2}\right)

and

.. math:: \dv{\phi}{\tau} = \frac{h}{r^2}

For a radial trajectory :math:`h=0`, and

.. math:: \left( \dv{r}{\tau}\right)^2 = k^2 -1 + \frac{2M}{r}

and as it is initially at rest,

.. math:: k^2-1=- \frac{2M}{R} \implies \left( \dv{r}{\tau}\right)^2 = \frac{2M}{r}-\frac{2M}{R}

Given that the particle is falling inwards,

.. math:: \dd{\tau} = - \frac{\dd{r}}{\sqrt{\frac{2M}{r} - \frac{2M}{R}}}

So the elapsed proper time experienced by the particle as it falls from
:math:`r=R` to :math:`r=2M` is

.. math::

   \label{eq:231}
     \Delta \tau = \int_{2M}^R \frac{\dd{r}}{\sqrt{\frac{2M}{r} - \frac{2M}{R}}}

This integral is finite, and so the particle reaches the surface in a
finite time. What about the interval in coordinate time?

.. math:: \dv{t}{\tau} = \frac{k}{1-\frac{2M}{r}} = \frac{\sqrt{1- \frac{2M}{R}}}{1-\frac{2M}{r}}

so

.. math:: \dd{t} = - \frac{\sqrt{1 - \frac{2M}{R}}}{\sqrt{\frac{2M}{r} - \frac{2M}{R}} \left( 1 - \frac{2M}{r}\right)} \dd{r}

and so

.. math::

   \label{eq:233}
     \Delta t = \int_{2M}^R  \frac{\sqrt{1 - \frac{2M}{R}}}{\sqrt{\frac{2M}{r} - \frac{2M}{R}} \left( 1 - \frac{2M}{r}\right)} \dd{r}

This integral diverges as :math:`r \to 2M`, so it takes an infinite
amount of coordinate time to reach the radius. The same is true for a
photon. Thus an external observer sees the particle taking an infinite
time to fall into the black hole.

Clearly, the problem with the metric at the Schwarzschild surface is
merely a coordinate singularity. There are no physical consequences in
the local frame of the particle as it crosses the singularity, but this
singularity is the event horizon, and it has effects on the future
movement of the particle. Once this surface is crossed it is impossible
to return, as all trajectories cause the particle to move to a smaller
coordinate radius, unless the particle can exceed the speed of light.

Inside the event horizon
========================

Recall that the interval, :math:`\dd{s}^2` between neighbouring events—
:math:`(t,x,y,z)` and :math:`(t+\dd{t}, x+\dd{x}, y+\dd{y}, z+\dd{z})`
in some coordinate system—can be null :math:`\dd{s}^2=0`, spacelike
(:math:`\dd{s}^2>0`), or timelike (:math:`\dd{s}^2<0`). In a spacelike
interval there will be a Lorentz frame, :math:`S'` in which the events
occur at the same coordinate time, so :math:`\dd{t}=0`. If
:math:`\dd{s}^2>0` the two events cannot lie on the worldline of a
material particle, as an observer in :math:`S'` would see it in two
places at the same time, violating causality.

Consider neighbouring events for a particle at rest inside the event
horizon, with :math:`\dd{r} = \dd{\theta} = \dd[\phi] = 0`, but
:math:`\dd{t} \neq
0`, then

.. math:: \dd{s}^2 = - \left( 1 - \frac{2M}{r} \right) \dd{t}^2

Since :math:`r<2M` it follows that this interval must be positive, so
cannot lie on the worldline of the particle, and so a particle cannot
remain stationary; in effect :math:`t` and :math:`r` have changed role
as coordinate labels.

To overcome the misbehaviour of the coordinates at a radius :math:`r=2M`
we introduce a new time coordinate,

.. math::

   \label{eq:234}
     \tilde{t} = t+2M \log( \frac{r}{2M} - 1 )

 taking :math:`\dd{\theta} = \dd{\phi} = 0`,

.. math::

   \label{eq:235}
     \dd{s}^2 = - \left(1 - \frac{2M}{r} \right) \dd{\tilde{t}}^2 + \frac{4M}{r} \dd{r} \dd{\tilde{t}} + \left( 1 + \frac{2M}{r}\right) \dd{r}^2

which has no coordinate singularity at :math:`r=2M` (but has one at
:math:`r=0`, which is a *physical* singularity).

We can then obtain the equations of the null cones by setting
:math:`\dd{s}^2=0`, dividing through by :math:`\dd{r}^2`, and solving
for :math:`\dv{\tilde{t}}{r}`, leaving a quadratic equation with roots
at

.. math::

   \label{eq:236}
     \dv{\tilde{t}}{r} = \left\{-1, \frac{1 + 2M/r}{1-2M/r} \right}

As :math:`r` approaches the Schwarzschild radius the light cones start
to tip over, and at :math:`r=R~s` the null cone has a vertical edge, so
all timelike geodesics then point inwards.

Luminosity and Hawking radiation
================================

Redshifting
-----------

Just how “black” is a black hole? Shouldn’t we see the light emitted by
the star just before it collapsed eternally frozen at the event horizon?
Light from the collapsing star is redshifted as it climbs out of the
star’s gravity field, with the redshift, :math:`z`,

.. math::

   \label{eq:237}
     z \equiv \frac{\lambda~o - \lambda~e}{\lambda~e} = \sqrt{\frac{1 - 2M/r~o}{1-2M/r~e}} -1  = \sqrt{\frac{r~e (r~o-R~s)}{r~o (r~e - R~s)}} - 1

which diverges as :math:`r~e \to R~s`. The bolometric luminosity of the
star, compared to its constant luminosity :math:`L~c`, ignoring
relativistic effects is

.. math:: L(t_0) = \frac{L~c}{(1+z)^2}

This can be understood by considering the energy of each photon
received by the observer is redshifted by a factor :math:`(1+z)`, and
the arrival times are increased by the same factor, so the luminosity is
reduced by the square. The light ray, on a null geodesic, satisfies

.. math:: \int_{t~e}^{t~o} \dd{t} = \int_{r~e}^{r~o} \frac{\dd{r}}{1-2M/r} \equiv  \int_{r~e}^{r~o} \frac{\dd{r}}{1-R~s/r}

Then

.. math:: t~o - t~e = r~o - r~e - R~s \log( \frac{r~o - R~s}{r~e - R~s} )

and, taking :math:`t_0 = 0`

.. math:: \log( \frac{r~e - R~s}{r~o - R~s} ) = left[\frac{t~o - (r~o - r~e)}{R~s} \right]

.. math::

   \implies \frac{r~e - R~s}{r~o - R~s} =
   \frac{r~o}{r~e}\frac{1}{(1+z)^2} \propto \exp( - \frac{t~o}{R~s} )

The, reintroducing the speed of light, :math:`c`,

.. math:: \frac{L(t~o)}{L~c} \propto \exp( - \frac{c t~o}{R~s} )

The luminosity of the star falls off exponentially in the time taken for light to cross the Schwarzschild radius.

Hawking radiation
-----------------

The effects of quantum field theory in a curved spacetime do, however, allow black holes to have a very faint luminosity—a process known as Hawking radiation.
This basically relies on the Uncertainty Principle allowing energy to be “borrowed” from the vacuum on a timescale :math:`\Delta t`, where

.. math:: \Delta t = \frac{\hbar}{\Delta E}

This allows the temporary production of virtual photon pairs; if this occurs on the edge of the event horizon the negative energy member of the pair may fall into the black hole, leaving the positive energy photon free to propagate outside the black hole, and the negative energy one free to propagate inside the black hole.
This radiation has a black body profile at infinity,

.. math:: E_{\infty} = \frac{h}{8 \pi M}

This means that a black hole has a thermodynamic temperature, and since it is emitting energy, it must be losing mass.
The luminosity of a black hole can be derived using the Stefan-Boltzmann law, and is proportional to the product of the area of the event horizon, :math:`A`, and the fourth power of the temperature, :math:`T^4`, so

.. math::

   \begin{aligned}
     A &= 4 \pi R^2 = 4 \pi (2M)^2 = 16 \pi M^2 \nonumber\\
   \implies L & \propto M^{-2} \nonumber\\
   \implies \dot{M} & \propto M^{-2} \nonumber\end{aligned}

 Thus the lifetime of the black hole is :math:`\tau \propto M^3`, and
eventually we find

.. math::

   \label{eq:240}
     \left( \frac{\tau}{10^{10}\,\text{yr}} \right) = \left( \frac{M}{10^{12}\,\kilogram} \right)^3

Black hole thermodynamics
-------------------------

The Hawking area theorem, which predates the work on Hawking radiation,
states that

.. math:: \dv{A}{t} \ge 0

which has an analogy in thermodynamics: entropy. The discovery of
Hawking radiation firmed-up this analogy, by attaching a temperature to
a black hole. For a Schwarzschild black hole,

.. math:: \dd{A} = 32 \pi M \dd{M}

 or

.. math:: \dd{M} = \frac{1}{32 \pi M} \dd{A} = \frac{\hbar}{8 \pi k M} \dd{\left(\frac{Ak}{4 \hbar}\right)}

 Thus

.. math:: \dd{E} = T \dd{S}

 This only applies to a classical black hole, however, since Hawking
radiation reduces the mass and hence the area of the event horizon.

Rotating black holes
====================

The treatment of rotating reference frames is substantially more
complicated than static ones, but an example of a more general black
hole than the Schwarzschild one, the Kerr black hole, requires this
treatment, as it is rotating.

The Kerr metric is characterised by the constants :math:`M` and
:math:`J`, which can be found by requiring that the metric must
reproduce Newtonian behaviour in the weak-field limit. :math:`M` is the
Newtonian mass of the star, and :math:`J` is the magnitude of the total
angular momentum. Writing :math:`a \equiv J/M`, the form of the metric
is

.. math::

   \begin{aligned}
     \dd{s}^2 &= - \frac{\Delta - a^2 \sin[2](\theta)}{\rho^2} - 4a \frac{Mr \sin[2](\theta)}{\rho^2} \dd{t} \dd{\phi} \nonumber\\
    & \qquad {}+ \frac{(r^2+a^2)^2 -a^2 \Delta \sin[2](\theta)}{\rho^2} \sin[2](\theta) \dd{\phi}^2 \nonumber\\
   & \qquad {}+ \frac{\rho^2}{\Delta} \dd{r}^2 + \rho^2 \dd{\theta}^2\end{aligned}

 having defined :math:`\Delta = r^2 - 2Mr + a^2` and
:math:`\rho^2 = r^2 + a^2
\cos[2](\theta)`. This metric is clearly non-diagonal, and this
introduces the phenomenon of frame-dragging.

Conservation of four momentum on geodesics
------------------------------------------

A material particle has a geodesic equation

.. math:: \dv{v^{\alpha}}{\tau} + \Gamma^{\alpha}_{\beta \delta} v^{\beta} v^{\delta} = \left( \pdv{v^{\alpha}}{x^{\beta}} v^{\beta} + \Gamma^{\alpha}_{\beta \delta} v^{\beta} v^{\delta} \right) = v^{\beta} \tensor{v}{^{\alpha}_{;\beta}} = 0

 The mixed form is

.. math:: v^{\alpha} v_{\beta;\alpha} = 0

 Introducing the four momentum, :math:`p^{\alpha} = m v^{\alpha}`, for
:math:`m` the particle rest mass, then

.. math::

   \label{eq:238}
     p^{\alpha} p_{\beta;\alpha} = 0

 Or,

.. math:: p^{\alpha}p_{\beta,\alpha} = \Gamma^{\gamma}_{\beta \alpha} p^{\alpha} p_{\gamma} = \half g^{\gamma \nu} \left( g_{\nu \beta,\alpha} + g_{\nu \alpha, \beta} - g_{\alpha \beta, \nu}\right) p^{\alpha} p_{\gamma}

 Which, after contraction and index permutation reduces to

.. math:: p^{\alpha} p_{\beta,\alpha} = \half g_{\nu \alpha, \beta} p^{\nu} p^{\alpha}

 which can then be expressed as

.. math::

   \label{eq:239}
     m v^{\alpha} \pdv{p_{\beta}}{x^{\alpha}} = m \dv{x^{\alpha}}{\tau} \pdv{p_{\beta}}{x^{\alpha}} = m \dv{p_{\beta}}{\tau} = \half g_{\nu \alpha,\beta} p^{\nu} p^{\alpha}

 If all the components of the metric are independent of the coordinate
:math:`x^{\beta}` hen the right hand side is zero, implying that
:math:`p^{\alpha}` is constant along the geodesic.

Frame dragging
--------------

The components of the Kerr metric are independent of :math:`\phi`, but a
material particle moving on a geodesic conserves the :math:`p_{\phi}`
component of its four momentum. The contravariant component
:math:`p^{\phi}` is

.. math::

   p^{\phi} = g^{\phi \alpha} p_{\alpha} = g^{\phi \phi} p_{\phi} +
   g^{\phi t} p_t

In an orthogonal metric the second term would be zero, but the Kerr
metric is non-orthogonal. Similarly, for :math:`p^t`,

.. math:: p^t = g^{t\alpha} p_{\alpha} =  g^{tt} p_t + g^{t \phi} p_{\phi}

 A particle with :math:`p_{\phi}=0` will have

.. math:: p^t = m \dv{r}{\tau}, \qquad p^{\phi} = m \dv{\phi}{\tau}

 So

.. math::

   \dv{\phi}{t} = \frac{p^{\phi}}{p^t} = \frac{g^{\phi t}}{g^{tt}}
   \neq 0

 Thus a distance observer sees an angular velocity: an irrotational
particle free-falling in a Kerr metric gains angular momentum.
