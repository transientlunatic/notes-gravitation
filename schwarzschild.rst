***********************
The Schwarzchild metric
***********************

There are four major classical tests of general relativity

#. advance of pericentre

#. light deflection

#. redshift

#. time delay

Geodesics of the Schwarzschild metric
=====================================

The geodesics of a test particle in the Schwarzchild metric satisfy the
geodesic equation ([eq:112]) with the proper time, :math:`\tau` as the
affine parameter,

.. math::

   \label{eq:141}
     \dv{\tau}\qty(g_{\lambda\nu} \dv{x^{\nu}}{\tau} ) - \half \pdv{g_{\mu \nu}}{x^{\lambda}} \dv{x^{\mu}}{\tau} \dv{x^{\nu}}{\tau} = 0

 The metric is static, and symmetrical, so is independent of :math:`t`
and :math:`\phi`, thus if :math:`\lambda \in \set{0,3}` the second term
vanishes. The metric is also orthogonal, so

.. math:: \dv{\tau} \qty( g_{tt} \dv{t}{\tau}) = \dv{\tau} \qty( g_{\phi \phi} \dv{\phi}{\tau}) = 0

 Integrating these gives

.. math:: g_{tt} \dv{t}{\tau} = \text{constant}, \qquad g_{\phi \phi} \dv{\phi}{\tau} = \text{constant}

 The geodesic equation for :math:`\lambda=2` (:math:`\theta`) follows
from equation ([eq:112])

.. math::

   \label{eq:142}
     \dv{\tau} \qty( r^2 \dv{\theta}{\tau} ) - \half  \pdv{\theta} \qty( r^2 \sin[2](\theta) )\qty[ \dv{\phi}{\tau}]^2 = 0

 which reduces to

.. math::

   \label{eq:143}
     r^2 \dv[2]{\theta}{\tau} + 2 r \dv{r}{\tau} \dv{\theta}{\tau} - r^2 \sin(\theta) \cos(\theta) \qty(\dv{\phi}{\tau})^2 = 0

 This has a particular solution when :math:`\theta=\pi/2`, which fixes
the orbit of a test particle to lie in the equatorial plane of the
coordinate system, thus

.. math:: \dv{\theta}{\tau} = 0

 We then also have

.. math::

   \label{eq:144}
     \dv{t}{\tau} = \frac{k}{1 - \frac{2M}{r}}, \qquad \dv{\phi}{\tau} = \frac{h}{r^2}

 For :math:`k`, :math:`h` constant. The geodesic differential equation
for :math:`r` can then be found from the general geodesic equation,

.. math::

   \label{eq:145}
     -1 = g_{tt} \qty( \dv{t}{\tau} )^2 + g_{rr} \qty(\dv{r}{\tau})^2 + g_{\phi \phi} \qty( \dv{\phi}{\tau} )^2

 which reduces to

.. math::

   \label{eq:146}
     \qty( \dv{r}{\tau} )^2 = k^2 - 1 - \frac{h^2}{r^2} + \frac{2M}{r} \qty(1+ \frac{h^2}{r^2})

Planetary orbits in Newtonian gravity
=====================================

In Newtonian mechanics a test mass orbiting another mass :math:`M` on
the equatorial plane has equations of motion of the form

.. math::

   \label{eq:147}
     r^2 \dv{\phi}{t} = h , \qquad \dv[2]{r}{t} = - \frac{M}{r^2} + r \qty( \dv{\phi}{t} )^2

 To solve the second equation we normally change variables,
:math:`t \to u =
1/r` and :math:`t \to \phi`. We have

.. math:: \dv{\phi}{t} = hu^2

 so

.. math::

   \label{eq:148}
     \dv{r}{t} = \dv{t} \qty(\frac{1}{u}) = - \frac{1}{u^2} \dv{u}{\phi} \dv{\phi}{t} = - h \dv{u}{\phi}

 so

.. math::

   \label{eq:149}
     \dv[2]{u}{\phi} = -u + \frac{M}{h^2}

 which has a solution

.. math::

   \label{eq:150}
     u = \frac{M}{h^2} \qty( 1+ e \cos(\phi))

 which is an ellipse with eccentricity :math:`e`, semi-major axis
:math:`a`, and a focus at :math:`r=0`. :math:`h` is related to the
semi-latus rectum

.. math:: \ell = \frac{h^2}{M} = a(1-e^2)

Advance of pericentre
=====================

Performing a similar procedure on equation ([eq:146]), with :math:`r \to
u` and :math:`\tau \to \phi`, we find

.. math::

   \label{eq:151}
     h^2 \qty( \dv{u}{\phi})^2 = \qty(k^2 - 1) - h^2u^2 + 2 Mu \qty( 1+h^2u^2)

 Differentiating this, and cancelling the common :math:`\dv{u}{\phi}`,

.. math::

   \label{eq:152}
     \dv[2]{u}{\phi}  = -u + \frac{M}{h^2} + 3 Mu^2

 This tiny :math:`3Mu^2` component is the additional contribution from
GR; for the Earth’s orbit the ratio of this to the :math:`M/h^2`
quantity is around :math:`3\e{-8}`. We can gain a good approximation to
equation ([eq:152]) by replacing the :math:`u` by a :math:`u^2` term on
the right hand of the Newtonian equivalent, so

.. math::

   \label{eq:153}
     \dv[2]{u}{\phi} = -u + \frac{M}{h^2} + 3 \frac{M^3}{h^4} \qty( 1 + 2e \cos(\phi) + e^2 \cos[2](\phi) )

+[mark=none,domain=0:5000,samples=1200, muted-green, line width=1]
1/(1+0.6\*cos(0.9\*x));

decomposing :math:`u` into :math:`u = u~N + u~{GR}`, and then
subtracting the Newtonian component

.. math::

   \label{eq:155}
     \dv[2]{u~{GR}}{\phi} = -u~{GR} + 3 \frac{M^3}{h^4} \qty(1+ 2e \cos(\phi) + e^2 \cos[2](\phi) )

 Noting

.. math::

   \label{eq:154}
     \cos[2](\phi) = \half (1 + \cos(2 \phi) )

 then

.. math::

   \label{eq:156}
     \dv[2]{u~{GR}}{\phi} + u~{GR} = 3 \frac{M^3}{h^4} \qty( 1 + \frac{e^2}{2} + 2e \cos(\phi) + \frac{e^2}{2} \cos(2 \phi) )

 The right-hand side has the form
:math:`A + B \cos(\phi) + C \cos(2 \phi)` for constants :math:`A,B,C`.

.. math::

   \begin{aligned}
       u~{GR} &= A \\ &= \half B \phi \sin(\phi) \\ &= - \frac{1}{3} C \cos(2 \phi)
     \end{aligned}

with the correction to the Newtonian orbit given by the sum of these
integrals. The first and third terms add a negligible constant, and a
tiny wiggle, but the second term is secular, so increases constantly.
Thus

.. math::

   \label{eq:157}
     u = \frac{M}{h^2} \qty( 1+ e \cos(\phi) + \frac{3M^2}{h^2} e \phi \sin(\phi) )

 given that the :math:`3M^2/h^2` term is very small, and making small
angle approximations, :math:`\cos(\beta)\approx 1` and
:math:`\sin(\beta)\approx \beta`, and recalling that

.. math:: \cos(\alpha-\beta) = \cos(\alpha) \cos(\beta) + \sin(\alpha) \sin(\beta)

 we can rewrite equation ([eq:157]) as

.. math::

   \label{eq:158}
     u  =\frac{M}{h^2} \qty[1 + e \cos( \qty( 1 - \frac{3M^2}{h^2}) \phi )]

 Comparing this to the Newtonian analogue it’s clear that the solution
is elliptical and periodic with a period

.. math::

   \label{eq:159}
     P = \frac{2 \pi}{1 - 3M^2/h^2} > 2 \pi

 so the ellipse precesses, and the pericentre line advances by an amount
:math:`\Delta` in every orbit,

.. math::

   \label{eq:160}
     \Delta = 2 \pi \qty( 1 - \frac{3M^2}{h^2})^{-1} - 2 \pi \approx \frac{6 \pi M^2}{h^2} = \frac{6 \pi M}{a(1-e^2)}

Gravitational light deflection
==============================

The deflection of light occurs in the Newtonian framework, provided
photons have mass, but is formally predicted by General relativity for
all particles with energy.

Newtonian deflection
--------------------

Consider the path of a photon passing by a mass :math:`M`; the orbit of
the photon will be a hyperbola with :math:`M` at one focus, so

.. math:: r(\phi) = \frac{ r~{min} (e+1) }{1+e \cos(\phi) }

for :math:`e>1` the eccentricity, and :math:`r~{min}` the closest
distance the photon approaches to :math:`M`.

+[mark=none,domain=-100:100,samples=300, muted-green, line width=1]
0.2\*(1.6+1)/(1+1.6\*cos(x)); (axis cs:90, 0.52) – (axis cs:90, 0.7);
(axis cs:90,0.7) to (axis cs:98.5,0.67); (axis cs:90,0.6) node[right]
:math:`\frac{\Delta\pi}{2}`;

Before and after the encounter the photon has asymptotic directions

.. math::

   \label{eq:161}
     \phi = \pm \qty( \frac{\pi}{2} + \frac{\Delta \phi}{2})

 for :math:`\Delta \phi` the total deflection angle. Just like for an
elliptical orbit we require

.. math:: r^2 \dv{\phi}{t} = h

 for :math:`h` constant,

.. math:: h^2 = M \ell = Ma (e^2 - 1) = Ma (e-1)(e+1) = M r~{min}(e+1)

 with :math:`\ell` the semi-latus rectum. The photon must also satisfy
an energy equation,

.. math::

   \label{eq:162}
     \half v^2 - \frac{M}{r} = \half \qty[ \qty( \dv{r}{t} )^2 + r^2 \qty( \dv{\phi}{t} )^2 ] - \frac{M}{r} = E~{tot}

 for the terms in the brackets the radial and transverse velocity
components. Since

.. math:: \dv{r}{t} = \dv{r}{\phi} \dv{\phi}{t}

.. math::

   \label{eq:163}
     \frac{h^2}{2r^2} \qty[ \frac{1}{r^2} \qty(\dv{r}{\phi})^2 + 1] - \frac{M}{r} = E~{tot}

 Then from the equation of the orbit,

.. math::

   \label{eq:164}
     \dv{r}{\phi} = \frac{r~{min}(e+1)e \sin(\phi)}{(1+e \cos(\phi))^2} = \frac{r^2 e \sin(\phi)}{r~{min} (e+1)}

 Substituting for :math:`h` in the energy equation,

.. math::

   \label{eq:165}
     E~{tot} = \frac{M(e-1)}{2 r~{min}}

 We can see that :math:`r \to \infty` when :math:`\cos(\phi) = -1/e`,
and letting :math:`v=c=1`, for :math:`r \to \infty` we have

.. math::

   \label{eq:166}
     E~{tot} = \half

 Rearranging equation ([eq:165]), and since :math:`e\gg 1`

.. math::

   \label{eq:167}
     e = 1 + \frac{r~{min}}{M} \approx \frac{r~{min}}{M}

 So the outgoing photon has an asymptotic direction

.. math::

   \label{eq:168}
     \cos(\phi) = \cos( \frac{\pi}{2} + \frac{\Delta \phi}{2} ) = - \sin( \frac{\Delta \phi}{2}) = - \frac{M}{r~{min}}

 Since :math:`\Delta \phi \ll 1`,

.. math::

   \label{eq:169}
     \Delta \phi = \frac{2M}{r~{min}}

Relativistic deflection
-----------------------

The geodesics for a photon can be found in a similar way to those for
masses in section [sec:geod-schw-metr], but the affine parameter is
:math:`s`, since a photon has a proper time :math:`\tau = 0`. We find

.. math::

   \begin{aligned}
       \dv{t}{s} &= \frac{k}{1 - 2 \frac{M}{r}} \\ \dv{\phi}{s} &= \frac{h}{r^2}
     \end{aligned}

For the :math:`\theta` equation there is a particular solution
:math:`\theta=\frac{\pi}{2}`, and also

.. math:: \frac{\theta}{s}=0

 so

.. math::

   \label{eq:170}
     \qty( \dv{r}{s})^2 = k^2 - \frac{h^2}{r^2} + \frac{2 M h^2}{r^3}

 Making the change of variables :math:`r \to u = 1/r`, and
:math:`s \to \phi`, then

.. math::

   \label{eq:171}
     \dv[2]{u}{\phi} + u = 3 M u^2

 Ignoring the right hand side, a particular integral is

.. math::

   \label{eq:172}
     u = \frac{\cos(\phi)}{r~{min}}

 Following the same approach as before, and using equation ([eq:172]) to
substitute into the right hand side of equation ([eq:171]),

.. math::

   \label{eq:173}
     \dv[2]{u}{\phi} + u = \frac{3M}{r^2~{min}} \cos[2](\phi) = \frac{3M}{2 r^2~{min}} (1 + \cos(2 \phi))

 A particular integral for this approximation is then

.. math::

   \label{eq:174}
     u = \frac{3M}{2 r^2~{min}} \qty(1 - \frac{1}{3} \cos(2 \phi) )

 and it follows that the general solution to equation ([eq:171]) is

.. math::

   \label{eq:175}
     u = \frac{\cos(\phi)}{r~{min}} + \frac{3M}{2 r^2~{min}} \qty( 1 - \frac{1}{3} \cos(2 \phi) )

 we can rewrite this using the asymptotic directions of the photon, so
the outgoing photon has

.. math::

   \label{eq:176}
     u = \frac{\cos( \frac{\pi}{2} + \frac{\Delta \phi}{2})}{r~{min}} + \frac{3 M}{2 r^2~{min}} \qty[1-\frac{1}{3} \cos(\pi + \Delta \phi) ]

 which simplifies to

.. math::

   \label{eq:177}
       u = -\frac{\sin(\frac{\Delta \phi}{2})}{r~{min}} + \frac{3 M}{2 r^2~{min}} \qty[1-\frac{1}{3} \cos(\Delta \phi) ]

 and since :math:`\Delta \phi \ll 1`,

.. math::

   \label{eq:178}
     u = - \frac{\Delta \phi}{2 r~{min}} + \frac{2M}{r^2~{min}}

 Then setting :math:`u=0` (i.e. :math:`r \to \infty`), we get the
general relativisitic result,

.. math::

   \label{eq:179}
     \Delta \phi = \frac{4 M}{r~{min}} \equiv \frac{4 GM}{c^2 r~{min}} = \frac{2 R~S}{r~{min}}

 This is twice the Newtonian deflection. If we take :math:`r~{min}` to
be a solar radius, and :math:`M` to be a solar mass, we find the
deflection caused by the sun to be :math:`1.77` arcseconds, which was
observed by Arthur Eddington during a solar eclipse.

Lensing
-------

(O) at (0,0) :math:`O`; (M) at (5,0) :math:`M`; (P) at (5,2) :math:`P`;
(S) at (10,0) :math:`S`; (O) to (P); (O) to (M); (2.5, 0) node
[fill=white] :math:`D_L`; (M) to (S); (7.5,0) node [fill=white]
:math:`D_S-D_L`; (P) to (M); (5,1) node [fill=white] :math:`R~E`; (S’)
at (10,4) :math:`S'`; (P) to (S’); (0:1) to (22:1); at (11:1.5)
:math:`\theta~E`; (P) to (S); (S) – +(0:-1) to +(-22:-1); at
(:math:`(S)+(-11:-1.5)`) :math:`\beta`; (:math:`(P)+(22:1)`) to
(:math:`(P)+(-22:1)`); (:math:`(P)+(0:.75)`) node :math:`\alpha`;

Consider a light ray from a distant source (see figure [fig:lensing])
being deflected through an angle :math:`\alpha` by a mass :math:`M`. The
angle of deflection is small, so can be approximated by a thin-lensing
situation, with the lens lying along the line :math:`OP`, with :math:`P`
a distance :math:`R~E` from :math:`M`. The ray path is then approximated
by :math:`OP` and :math:`PS`. By symmetry all points on the locus
described by :math:`R~E` produce lensing, so a ring is formed (figure
[fig:lensing-2]), which is called an *Einstein ring*.

The ring has an angular radius :math:`\theta~E`, which can be found by
considering the distance :math:`D_L` to the lens and :math:`D_S` to the
source, from the observer at :math:`O`. Then (see figure [fig:lensing])

.. math:: \theta~E + \beta = \alpha

 and

.. math:: \theta~E = \frac{R~E}{D_L}

 also

.. math:: \beta = \frac{R~E}{D_S - D_L} = \theta~E \frac{D_L}{D_S-D_L}

 Then, making appropriate substitutions,

.. math::

   \label{eq:180}
     \theta~E + \theta~E \frac{D_L}{D_S-D_L} = \theta~E \frac{D_S}{D_S - D_L} = \frac{4M}{R~E} = \frac{4M}{D_L \theta~E}

 Thus

.. math::

   \label{eq:181}
     \theta~E = \sqrt{ \frac{4M (D_S-D_L)}{D_SD_L} }

 then, substituting :math:`x = D_L/D_S`,

.. math::

   \label{eq:182}
     \theta~E = \sqrt{ \frac{4M(1-x)}{D_S x}}

If the lensing mass is not a spherically symmetric distribution exactly
aligned between the observer and the source the ring is not produced,
but instead an (odd) number of images are formed with an angular
separation on the order of :math:`\theta~E`.

We can make some simplifications to get some convenient equations for
lensing. Suppose the source is a distant quasar lensed by a foreground
galaxy, then

.. math::

   \label{eq:183}
     \theta~E \approx 3" \sqrt{ \frac{M}{10^{12} M_{\odot}} \frac{10^9\, \text{pc}}{D_S} \frac{(1-x)}{x} }

 This regime is *strong lensing*, and separations are on the order of a
few arcseconds. Several hundreds of examples of strong lenses exist.

If the source objects are within the Galaxy,

.. math::

   \label{eq:184}
     \theta~E \approx 0.9\, \text{mas} \sqrt{ \frac{M}{M_{\odot}} \frac{10\,\text{kpc}}{D_S} \frac{(1-x)}{x}}

 So the images are close enough that resolving them is difficult (but
within the power of e.g. GAIA), and this regime is *gravitational
microlensing*.

(O) at (0,0) :math:`O`; (M) at (5,0); (P) at (5,2); (P’) at (5,-2) ; (S)
at (10,0) :math:`S`; (O) to (P); (O) to (P’); (S’) at (10,4); (P) to
(S’); (0:1) to (22:1); at (11:1.5) :math:`\theta~E`; (P) to (S) (P’) to
(S); (:math:`(P)+(22:1)`) to (:math:`(P)+(-22:1)`);
(:math:`(P)+(0:.75)`) node :math:`\alpha`; (S) ellipse (2 and 4); (M)
circle (0.05) node [above] :math:`M`;

Gravitational redshift
======================

Suppose light is emitted with the coordinates :math:`(t_e,r_e)` in the
Schwarzschild metric, and travels along a radial null geodesic to reach
an observer at an event :math:`(t_o, r_o)`, then

.. math::

   \label{eq:185}
     \dd{s}^2 = 0 = - \qty( 1 - \frac{2M}{r} ) \dd{t}^2 + \frac{\dd{r}^2}{1 - 2M/r}

 thus

.. math::

   \label{eq:186}
     \int_{t_e}^{t_o} \dd{t} = t_o - t_e = \int_{r_e}^{r_o} \frac{\dd{r}}{1 - 2M/r}

 A wave with rest-frame frequency :math:`\nu_0` will have wavecrests
leave :math:`r_e` at :math:`t_e` and :math:`t_e + \Delta t_e`, which
reach :math:`r_o` at :math:`t_o` and :math:`t_o+\Delta t_e`, so the
proper time difference between emissions is

.. math::

   \label{eq:187}
     \Delta \tau_e = \Delta t_e \sqrt{1 - \frac{2M}{r_e}} \equiv \frac{1}{\nu_e} \equiv {\lambda_e}

 and between detections is

.. math::

   \label{eq:188}
     \Delta \tau_o = \Delta t_e \sqrt{1 - \frac{2M}{r_o}} \equiv \frac{1}{\nu_o} \equiv \lambda_o

 so the redshift, :math:`z`, is

.. math::

   \label{eq:189}
     z = \frac{\lambda_o - \lambda_e}{\lambda_e} = \sqrt{ \frac{1-2M/r_o}{1-2M/r_e}} - 1 = \sqrt{\frac{r_e(r_o-R~S)}{r_o(r_e-R~S)}}-1

 for :math:`R~S` the Schwarzschild radius of the mass :math:`M`.

Gravitational time delay
========================

Gravitational time delay has two constributions; a geometric one, and a
gravitational one, the Shapiro effect.

Taking the Schwarzschild invariant interval, and introducing

.. math::

   \label{eq:190}
     r = R \qty(1+\frac{M}{2R})^2

 then assuming a weak gravitational field, with :math:`M \ll r` and so
:math:`M \ll R`,

.. math::

   \label{eq:191}
     r approx R \qty(1+ \frac{M}{R})

 and noting

.. math:: 1 - \frac{2M}{r} = \frac{r-2M}{r}

 we can produce the Schwarzschild metric in the form

.. math::

   \label{eq:192}
   \begin{split}
     \dd{s}^2 = - \qty( \frac{1-M/R}{1+M/R} ) \dd{t}^2 + \qty(\frac{1+M/R}{1-M/R}) \dd{r}^2 \\
   +R^2 \qty( 1 + \frac{M}{R})^2 \qty[ \dd{\theta}^2 + \sin[2](\theta) \dd{\phi}^2]
   \end{split}

 Using the binomial expansion,

.. math:: (1+x)^n \approx 1+ nx

 and, noting that to first order :math:`\dd{r} = \dd{R}`,

.. math::

   \label{eq:194}
     \begin{split}
       \dd{s}^2 = - \qty(1 - \frac{2M}{R}) \dd{t}^2 \\
   + \qty(1+\frac{2M}{R}) \qty[ \dd{R}^2 + R^2 \dd{\theta}^2 + R^2 \sin[2](\theta) \dd{\phi}^2]
     \end{split}

 Then, defining the Cartesian coordinates,

.. math::

   \label{eq:195}
     X = R \sin(\theta) \cos(\theta), \quad Y=R \sin(\theta) \sin(\phi), \quad Z = R \cos(\theta)

 and introducing the gravitational potential,

.. math:: \psi = - \frac{GM}{R}

 The interval becomes

.. math::

   \label{eq:196}
     \dd{s}^2 = -(1+2\psi) \dd{t}^2 + (1-2\psi) [\dd{X}^2 + \dd{Y}^2 + \dd{Z}^2]

Consider a photon which propagates from a source at :math:`A` to an
observer at :math:`B` past a deflecting mass :math:`M`, which is small,
so we assume the trajectory is straight in space, and align the
coordinates so the :math:`z`-axis is along the line of propagation, so
:math:`\dd{x}=\dd{y}=0`, so

.. math::

   \label{eq:197}
     \dd{s}^2 = - (1+2 \phi) \dd{t}^2 + (1-2 \psi) \dd{z}^2

 Since :math:`\dd{s}^2 = 0`, to first order,

.. math::

   \label{eq:198}
     \dd{t}^2 = \frac{1-2\psi}{1+2\psi} \dd{z}^2 \approx (1-2\psi)^2 \dd{z}^2

 Then :math:`\int \dd{t} = \int(1-2\phi) \dd{z}`, so

.. math::

   \label{eq:199}
     t~B - t~A = (z~B - z~A) - 2 \int_{z~A}^{z~B} \psi(z) \dd{z}

 With the second term being the time delay due to gravity,

.. math::

   \label{eq:200}
     \delta t~{grav} = -2 \int_{z~A}^{z~B} \psi(z) \dd{z} \equiv -\frac{2}{c^3} \int_{z~A}^{z~B} \psi(z) \dd{z}
